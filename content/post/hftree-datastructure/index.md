---
# Documentation: https://wowchemy.com/docs/managing-content/

title: "哈夫曼编码及其实现"
subtitle: ""
summary: "哈夫曼编码——无损数据压缩的熵编码算法"
authors: []
tags: []
categories: []
date: 2018-12-19T22:55:46+08:00
lastmod: 2018-12-10T22:55:46+08:00
featured: false
draft: false

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder.
# Focal points: Smart, Center, TopLeft, Top, TopRight, Left, Right, BottomLeft, Bottom, BottomRight.
image:
  caption: ""
  focal_point: ""
  preview_only: false

# Projects (optional).
#   Associate this post with one or more of your projects.
#   Simply enter your project's folder or file name without extension.
#   E.g. `projects = ["internal-project"]` references `content/project/deep-learning/index.md`.
#   Otherwise, set `projects = []`.
projects: []
---
## 哈夫曼树

### 哈夫曼树特点

哈夫曼树又称最优二叉树，是一种带权路径长度最短的二叉树。常可用作无损压缩。

- 每个结点只有0或2各子节点
- 同一组权值得到的哈夫曼树可能不唯一
- 权值越大的结点越靠近哈夫曼树的根节点，权值越小的结点越原理哈夫曼树的根节点
- 一棵有n各叶子结点的哈夫曼树共有2n-1个结点
- 带权值的结点都是叶子结点，不带权值的结点都有子结点

### 哈夫曼树构建

此处把哈夫曼树构建过程分为2个步骤：数据组织、构建树

## 数据组织

数据组织包括对原始数据的预处理，如原始数据是一段字符串，考虑使用什么数据结构对字符串中的字符及其发生频率进行组织，发生频率越高的字符认为其权重越大，于是对其“特殊照顾”。如使用链表或数组组织每个字符，每个节点的数据结构可如下：

```java
package com.coolcats.tree;
/**
 * 哈夫曼树二叉树节点
 * @author CoolCats
 */
public class Node {

	public Node left,right;//左子节点
	public int weight;     //右子节点
	public String data;    // 数  据
	
	public Node() {
		
	}

	public Node(String data,int weight) {
		this.data = data;
		this.weight = weight;
	}

	public String toString() {
		return this.data+":"+this.weight;
	}
}
```

而后对节点列表按照其权重大小进行排序，不失一般性，此处升序排序:

```java
/**
	 * 列表排序
	 * 
	 * @param list
	 */
	private void sortList(ArrayList<Node> list) {
		Node minNode = null;
		Node jNode = null;
		for (int i = 0; i < list.size() - 1; i++) {
			int min = i;
			for (int j = i + 1; j < list.size(); j++) {
				minNode = list.get(min);
				jNode = list.get(j);
				if (minNode.weight > jNode.weight) {
					min = j;
				}
			}
			if (min != i) {
				Node tmpNode = list.get(i);
				list.set(i, list.get(min));
				list.set(min, tmpNode);
			}
		}

	}
```

## 构建树

得到了排序后的列表后，就可以构建树了，由于哈夫曼树的特点，小权值的节点尽可能远离根节点、大权值的节点尽可能靠近根节点，并且无法预估根节点到底在什么高度上，所以只能采用自底向上的方式构建哈夫曼树。具体步骤为

1. 输入排序后的列表，
2. 判断列表个数是否大于1，如果是，从中取出最小的两个元素，构造父节点，如果否，跳到4
3. 将父节点添加到列表中，对列表重新排序，回到2
4. 将列表中最后一个元素作为哈夫曼树根节点
   如此便可得到哈夫曼树

### 哈夫曼压缩

所谓哈夫曼压缩，就是利用哈夫曼树的性质实现对文件的无损压缩。
通常来说，数据在计算机中的存储按字节来计算，一个ascii码字符占一个字节，一个汉字字符占2个字节，这种每个字符都通过相同来表达的编码形式称为定长编码。而哈夫曼压缩就是通过变长编码的方式实现对文件的压缩，其思想是根据字符出现的概率来确定编码的长度，出现概率大的字符采用较短的编码来存储，出现概率小的字符采用较长的编码来存储。

## 哈夫曼压缩实现

对于哈夫曼压缩可靠性而言最关键的保证是：任何一个字符的编码前缀都不能是另一个字符的编码。如果将一个节点到其左节点的路径标记为0，到其右节点的路径标记为1，那么，从根节点到每一个叶子节点所得到的哈夫曼编码是唯一的，且任一哈夫曼编码不是其他编码的前缀，满足条件。因此，实现压缩功能只要计算出每个字符的哈夫曼编码即可。在遍历哈夫曼树的同时计算哈夫曼编码的代码如下：

```java
	/**
	 * 后序遍历的同时标记每个节点的哈夫曼编码
	 * 
	 * @param root
	 * @param code
	 */
	private void postOrder(Node root, String code) {
		if (root.left != null)
			// 左路径标记为0
			postOrder(root.left, code + "0");
		if (root.right != null) {
			// 右路径标记为1
			postOrder(root.right, code + "1");
		}
		// 输出哈夫曼树叶子节点编码
		if (root.left == null && root.right == null) {
			System.out.println(root.data + "<>" + code);
			// 将各个字符的哈夫曼编码存储
			map.put(root.data, code);
			map1.put(code, root.data);
		}
	}
```

于是，在存储一个字符串时，只需要遍历这个字符串，取出每个字符对应的哈夫曼编码，每8位作为一个字节存储到文件中即可实现压缩，但要注意，哈夫曼编码的组合并不一定是8的整数倍，这可以通过“补0”来解决，所以存储压缩文件的时候还要把补0的个数记下，以便解压缩。一个demo版的代码如下：

```java
/**
 * 根据给定的路径以及哈夫曼编码将哈夫曼码存进相应的文件中 要存入压缩文件的信息，补了多少个0
* （demo版，效率较低）
* @param path 压缩文件的路径
* @param code 哈夫曼编码
 */
private void hfcode2file(String path, String code) {
	int len = code.length();
	System.out.println("哈夫曼编码长度：" + len);
	int comple = 8 - len % 8;
	if (comple < 8) {
		for (int i = 0; i < comple; i++) {
			code = code + "0";
		}
	} 
	OutputStream out = null;
	DataOutputStream dout = null;
	File file = new File(path);
	try {
		out = new FileOutputStream(file);
		dout = new DataOutputStream(out);
		int count = (len + comple) / 8;
		byte[] b = code.getBytes();
		dout.writeInt(comple);
		dout.write(b);
	} catch (FileNotFoundException e) {
		e.printStackTrace();
	} catch (IOException e) {
		e.printStackTrace();
	} finally {
		try {
			out.close();
			dout.close();
		} catch (IOException e) {
			e.printStackTrace();
		}
		System.out.println("压缩文件完成");
	}
}
```

解压缩就是根据读取文件的位，每读到一个哈夫曼编码（使用哈希表，判断是否存在对应的key）就返回其对应的字符，一直到文件末尾。

```java
	/**
	 * 解压缩
	 * @param path
	 * @return
	 */
	private String file2hfcode(String path) {
		String code = null;
		InputStream in = null;
		DataInputStream din = null;
		int comple;
		File file = new File(path);
		try {
			in = new FileInputStream(file);
			din = new DataInputStream(in);
			comple = din.readInt();
			byte[] bb = new byte[1024];
			int res = din.read(bb);
			code = hfcode2String(bb,res,comple);
		} catch (FileNotFoundException e) {
			e.printStackTrace();
		} catch (IOException e) {
			e.printStackTrace();
		}
		return code;
	}

```

### 问题思考

1. 哈夫曼树的压缩效率如何？
2. 哈夫曼树压缩在什么场景下不适用？
3. 考虑包含中文等非英文国家字符的文件压缩应该如何实现？
   字典压缩（LZ77，LZ88，LZW等）


## 参考文献
[哈夫曼编码维基百科](https://zh.wikipedia.org/wiki/%E9%9C%8D%E5%A4%AB%E6%9B%BC%E7%BC%96%E7%A0%81)

[LZW编码维基百科](https://zh.wikipedia.org/wiki/LZW)

[LZW压缩算法](https://segmentfault.com/a/1190000011425787)