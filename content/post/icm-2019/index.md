---
# Documentation: https://wowchemy.com/docs/managing-content/

title: "MCM/ICM 2019 Problem E"
subtitle: "Problem E: What is the Cost of Environmental Degradation"
summary: "美国大学生数学建模竞赛2019问题E资料小结"
authors: []
tags: [数学建模,书签]
categories: []
date: 2019-01-29T23:02:35+08:00
lastmod: 2019-01-29T23:02:35+08:00
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

论文查阅系统：
- [CSU](http://lib.csu.edu.cn/)
- [Web Of Science](http://libdb.csu.edu.cn/resdetail?rid=)
- [ScienceDirect](http://libdb.csu.edu.cn/resdetail?rid=ELSEVIER)
- [万方数据资源系统](http://libdb.csu.edu.cn/resdetail?rid=WF)
- [维普中文期刊](http://libdb.csu.edu.cn/resdetail?rid=VIP)
- [IEEE](http://libdb.csu.edu.cn/go?id=IEEE)


### Keywords

- 环境（退化/保护）成本
- 环境会计
- 环境成本计算
- （虚拟/实际）治理成本
- 生态系统管理/服务
- 生态系统服务功能
- 生态系统服务价值
- 土地开发项目
- 生态系统价值计算
- 价值评估
- 绿色经济核算
- 绿色发展（实践/框架）
- 生物物理量化
- 生物圈
- 生物多样性
  ![](https://i.imgur.com/WNbT5MD.png)

### 主题

环境退化的代价？

- 生态功能的持续性利益建模
  - 效益
    - 供应
      - 食物供应
      - 植物授粉
    - 调节
      - 植物碳固定——能值法？
      - 水（自净、防洪等）——以人类基础设施替代（如净水设施、防洪设施等）
      - 生物多样性——难点
    - 文化
      - 精神
      - 宗教
  - 考虑
    - 定义生态系统服务
    - 等效替代
      水环境退化成本——人工水污染治理花费（查数据）+生物多样性损失建模（？）
      森林退化——空气污染治理成本

### Tasks

1. 建立一个生态服务估值模型
2. 用模型评价不同规模的土地利用项目的成本规模效益分析
3. 基于以上分析模型设计评估模型的有效性
4. 模型对于土地利用项目规划者和管理者有何启示？
5. 模型随着时间变化需要作出怎样的修改？

### Existing Mathods

- NPP(net primary production)
- 元分析
  ![](https://i.imgur.com/9pYXKfu.png)

### References

#### **An ecological perspective on the valuation of ecosystem services**

#### **The value of the world’s ecosystem services and natural capital**
[[paper]](https://www.biodiversity.ru/programs/ecoservices/library/common/doc/Costanza_1997.pdf)
![](https://i.imgur.com/bZwiUwR.png)
![](https://i.imgur.com/Z6R45xK.png)

#### **Valuing ecosystem services: A shadow price for net primary production**：http://sites.bu.edu/cliveg/files/2013/12/arr01.pdf

从两个问题出发：生态系统服务对于传统指标如GDP度量的经济是否有贡献？这种贡献能否被用作隐式的价格来进行计算？
 net primary production 

 - 相关因素
   - 碳固定
   - 蒸腾作用
   - 土地腐蚀（负相关）
   - 生物量
 - 直接
 - 间接
 - 文化（旅行费用法，享乐价格）
   ![](https://i.imgur.com/YXshEKQ.png)
   ![](https://i.imgur.com/0cmDlC9.png)
 - 计算方法
   ![](https://i.imgur.com/7pqhkt9.png)
    ![](https://i.imgur.com/1hVq4MG.png)
    ![](https://i.imgur.com/S7DcEEO.png)
    ![](https://i.imgur.com/KlUqKkW.png)

#### **The history of ecosystem services in economic theory and practice: From early notions to markets and payment schemes**

#### **Valuing a diversity of ecosystem services: The way forward to protects trategic groundwater resources for the future?**

[[link]](http://libdb.csu.edu.cn/rwt/ELSEVIER/https/P75YPLUUMNVXK5UDMWTGT6UFMN4C6Z5QNF/science/article/pii/S1574009918300020)
### Data Sources

- https://www.weather.gov/dmx/
- [美国国家海洋和大气管理局](https://governmentshutdown.noaa.gov/)
- [Penn_World_Table](https://www.rug.nl/ggdc/productivity/pwt/)
- [ScienceBase](https://www.sciencebase.gov/catalog/folder/4f734998e4b046ee287b9d2f)
[[link]](https://www.sciencebase.gov/catalog/item/4fb555ebe4b04cb937751db9)
- [US Landcover](https://archive.usgs.gov/archive/sites/landcover.usgs.gov/uslandcover.html)
[[link]](https://gapanalysis.usgs.gov/gaplandcover/data/download/)
- [Bison Web](https://bison.usgs.gov/#api)
- [美国鱼类栖息地退化图](https://www.sciencebase.gov/catalog/item/565897c8e4b071e7ea540309)
- 美国生态系统恢复的经济影响
- [水资源普查](https://www.sciencebase.gov/catalog/item/5151f07ee4b0f0b3d011a817)
- [欧洲](https://www.eea.europa.eu/data-and-maps)
- [Emerge-nead](https://www.emergy-nead.com/country/data)
- [IPCC](https://www.ipcc.ch/report/ar5/wg1/)
- [IPCC数据分发中心](http://www.ipcc-data.org/)
- [NEAD](https://cep.ees.ufl.edu/nead/)
[[link]](https://en.climate-data.org/info/sources/)
- [欧洲疾病预防控制中心](https://ecdc.europa.eu/en/publications-data?f%5B0%5D=output_types%3A1382&f%5B1%5D=geo%3A485)
- [欧洲环境代理](https://www.eea.europa.eu/themes/climate#tab-datamaps)
- [美国国家能源数据系统](https://www.eia.gov/state/seds/seds-data-complete.php?sid=US)
- [电力数据浏览器](https://www.eia.gov/electricity/data/browser/)
- [NREL美国各州太阳能数据](https://www.nrel.gov/gis/data-solar.html)
- [美国劳动力数据](https://www.bls.gov/cps/tables.htm)
- [美国劳工统计局](https://www.bls.gov/opub/geographic-profile/)
- [Economic Research](https://fred.stlouisfed.org/categories/18)
- [Gloåbal Economic](https://www.theglobaleconomy.com/USA/investment/)
- EmergyDatabase：
[[link1]](https://docs.google.com/spreadsheets/d/1DOopVg2MVumzAsV1_i5U14P2WrkJC8EniXeo6rGtMSU/edit#gid=1338167176)
[[link2]](https://docs.google.com/spreadsheets/d/17FIFQ_FPv1b0moU8vV0Hh5WI1M9OX_q-gvCLp6atLcw/edit#gid=33074211)
- [美国人口普查局](https://www.statedatalab.org/glossary/detail/capital-outlays)
- [国家管道测绘系统](https://pvnpms.phmsa.dot.gov/PublicViewer/)
- [NAICS](https://www.census.gov/eos/www/naics/)
- [美国各州劳动力统计表](https://www.census.gov/topics/employment/labor-force/data/tables.2014.html)
- [排放和发电资源综合数据库](https://www.epa.gov/energy/emissions-generation-resource-integrated-database-egrid-questions-and-answers)
- [德克萨斯州全州图像和GIS数据](https://tnris.org/data-download/#!/statewide)
- [卡尔加里大学图书馆（GIS资源）](https://library.ucalgary.ca/c.php?g=255401&p=1705345)
- [佛罗里达环境保护部](https://ca.dep.state.fl.us/mapdirect/)
- [美国城市开放数据普查](http://us-city.census.okfn.org/dataset/zoning)
- [OpenData_CityOfNetwork](https://opendata.cityofnewyork.us/data/)
- [PURDUE图书馆](http://guides.lib.purdue.edu/c.php?g=353290&p=2378621)
- [The Nature Con](http://maps.tnc.org/gis_data.html)
- [Map of Life](http://species.mol.org/species/map/Perdix_dauurica)
- [气候数据图](https://zh.climate-data.org/%E4%BA%9A%E6%B4%B2/%E5%8D%B0%E5%BA%A6%E5%B0%BC%E8%A5%BF%E4%BA%9A/south-sulawesi/usa-559266/)
- [EPA](https://www.epa.gov/transportation-air-pollution-and-climate-change)

### Baike
 
- [旅行费用法](https://wiki.mbalib.com/wiki/%E6%97%85%E8%A1%8C%E8%B4%B9%E7%94%A8%E6%B3%95)
- 生物量：
  [[link1]](https://zh.wikipedia.org/wiki/%E7%94%9F%E7%89%A9%E9%87%8F)
  [[link2]](https://baike.baidu.com/item/%E7%94%9F%E7%89%A9%E9%87%8F)
- [初级生产](https://en.wikipedia.org/wiki/Primary_production)
  ![](https://i.imgur.com/Ld8j8P7.png)

- Cobb-Douglas生产函数及其优缺点: 
[[link1]](https://en.wikipedia.org/wiki/Cobb%E2%80%93Douglas_production_function)
[[link2]](http://shodhganga.inflibnet.ac.in/bitstream/10603/159915/6/06_chapter%203.pdf)
[[link3]](https://dash.harvard.edu/bitstream/handle/1/3196325/antras_usaggregate.pdf)
- [PWT](https://en.wikipedia.org/wiki/Penn_World_Table)
  ![](https://i.imgur.com/mtpukP7.png)
- 元分析：https://zh.wikipedia.org/wiki/%E5%85%83%E5%88%86%E6%9E%90
- 影子价格
[[link1]]( https://zh.wikipedia.org/wiki/%E5%BD%B1%E5%AD%90%E4%BB%B7%E6%A0%BC)
[[link2]](https://www.zhihu.com/question/23510001)
[[link3]](https://wiki.mbalib.com/wiki/%E5%BD%B1%E5%AD%90%E5%AE%9A%E4%BB%B7%E6%B3%95)
  ![](https://i.imgur.com/LJbh1tw.png)
- [生态服务价值](  https://wiki.mbalib.com/wiki/%E7%94%9F%E6%80%81%E6%9C%8D%E5%8A%A1%E4%BB%B7%E5%80%BC)
  ![](https://i.imgur.com/3oOTxJK.png)
- 环境成本分类
  ![](https://i.imgur.com/XBNXt5F.png)
- [生态系统服务分类](https://cices.eu/cices-structure/)
- [能值法指数解释](https://www.emergy-nead.com/country/explanation)
- [土地利用规划](https://en.wikipedia.org/wiki/Land-use_planning)
- 中国森林生态系统
- [土地使用规划](https://hdc.com.mv/hulhumale/planning-design/)
- ArcGIS交集制表
- [美国风能资源](https://rredc.nrel.gov/wind/pubs/atlas/)
- [劳动力参与率](https://www.google.com/search?q=%E5%8A%B3%E5%8A%A8%E5%8A%9B%E5%8F%82%E4%B8%8E%E7%8E%87&oq=%E5%8A%B3%E5%8A%A8%E5%8A%9B%E5%8F%82%E4%B8%8E%E7%8E%87&aqs=chrome..69i57j0l2.3721j0j7&sourceid=chrome&ie=UTF-8)
- 固定资产投资
- [matlab字符串处理函数](https://www.cnblogs.com/emanlee/archive/2012/09/13/2683912.html)
- [Matlab File Exchange](https://ww2.mathworks.cn/matlabcentral/fileexchange/?requestedDomain=zh)
- [BEA in the classroom](https://www.bea.gov/index.php/resources/learning-center/bea-in-the-classroom)
- [面板数据分析](https://www.zhihu.com/question/21918459)
- 非货币生态系统核算体系
  ![](https://i.imgur.com/GLbO59q.png)
- 国际统一阶段代码
  https://www.iso.org/stage-codes.html#50.20
- 国际标准组织污染、污染控制
  https://www.iso.org/ics/13.020.40/x/
- 温室气体协议
  https://ghgprotocol.org/
- [组织的温室气体排放量化和报告规范及指南](http://www.szmqs.gov.cn/xxgk/qt/ztlm/szbz/szsdfbz_szbz/201412/W020141202347688881182.pdf)
- 能值和变革
  http://www.emergysociety.com/emergy-and-transformity/
- python excel
  https://zhuanlan.zhihu.com/p/23998083
- 加州内化达Public Viewer 
  https://pvnpms.phmsa.dot.gov/PublicViewer/
- 国家空气毒物评估
  https://www.epa.gov/national-air-toxics-assessment
- 2014 National Air Toxics Assessment
  https://gispub.epa.gov/NATA/
- 成本效益分析
  https://www.britannica.com/topic/cost-benefit-analysis
- statisca统计门户网站
  https://www.statista.com/topics/2582/subway/
- [斯坦福确定项目成本与效益](https://web.stanford.edu/group/FRI/indonesia/documents/gittinger/Output/chap2.html)
- plannerWeb：http://plannersweb.com/2013/12/pro-forma-101-what-will-it-cost/
- [Agent-based Model](  https://zh.wikipedia.org/wiki/%E4%B8%AA%E4%BD%93%E4%B8%BA%E6%9C%AC%E6%A8%A1%E5%9E%8B)
  ![](https://i.imgur.com/zteOoEN.png)
- clarkLab
  https://clarklabs.org/
  https://en.wikipedia.org/wiki/TerrSet
- [美国土地利用](https://www.bloomberg.com/graphics/2018-us-land-use/)
- IDRISI
  [part1](https://download.csdn.net/download/liujiantao_1981/9557000)
  [part2](https://download.csdn.net/download/liujiantao_1981/9556996)
  [part3](https://download.csdn.net/download/liujiantao_1981/9556998)
- [时间序列平稳性](https://www.zhihu.com/question/21982358)
- [清洁空气法文本](https://www.epa.gov/clean-air-act-overview/clean-air-act-text)
  
- [us air quality standard](https://www.transportpolicy.net/standard/us-air-quality-standards/)

### Considerations

1. 一个真实的土地利用项目考虑上生态因素后的真实经济成本是？

- 大型
  - 全国铁路网建设
  - 全国管网
  - 水坝
- 小型
  - 元胞自动机多智能体模拟？
    植被面积变化、水文条件可能发生变化、空气可能会有污染（旧式火车）等等。缓冲区分析？