# 疫情背景下的周边游需求图谱分析

keywords:`2018-2021` 、`茂名市` 、`本地旅游图谱`、`新冠疫情时期`, `周边游` 

#### 人员构成：

- **组长**：查资料、协作、解决困难、救火、鼓励师
- **技术主力**：数据处理、数据建模、技术实现、模型调试
- **论文**：看论文，学习论文写作格式，了解技术动态， 高大上

#### 工具

* jieba
* pandas
* sklearn / pyTorch
* gensim 

关于nltk: 英文文本处理

## 任务一：微信公众号文章分类

1. 现成keywords = [
   "旅游",     "活动",     "节庆",     "特产",   "交通",
   "酒店",     "景区",     "景点",     "文创",   "文化",
   "乡村旅游", "民宿",     "假日",     "假期",   "游客",
   "采摘",     "赏花",     "春游",     "踏青",   "康养",
   "公园",     "滨海游",   "度假",     "农家乐", "剧本杀",
   "旅行",     "徒步",     "工业旅游", "线路",   "自驾游",
   "团队游",   "攻略",     "游记",     "包车",   "玻璃栈道",
   "游艇",     "高尔夫",   "温泉"]
2. 关键词提取: TF-IDF, TextRank
3. 人工分拣： 界限？0，1· 文旅

#### jieba

地址： https://github.com/fxsjy/jieba

没有文档！

- **分词**：`jieba.cut`
  - paddle模式：利用PaddlePaddle深度学习框架
- **自定义词典**: `jieba.load_userdict`
- **关键词提取**: `jieba.analyse.extract_tags`
- **词性标注**: `jieba.posseg.POSTokenizer()`
  - 实体
  - 形容词
- Tokenize:
  - 将文本分为更小的单元
  - token可以是字、词、词组 (subword, n-gram characters)
- ChineseAnalyzer for Whoosh搜索引擎
- 命令行分词

#### gensim

https://gensim.apachecn.org/#/blog/tutorial/1

## 任务二：周边游产品热度分析



## 任务三：本地旅游图谱构建与分析

### 知识图谱工具：

#### 博拉图：

视频：https://www.bilibili.com/video/BV1BL4y1e7vt

地址： https://bolatu.xlore.cn/Index 

#### SmartKG - Excel:

视频：https://www.bilibili.com/video/BV1xK411w7S4/

地址： https://github.com/microsoft/SmartKG 

#### 数眼

http://shuyantech.com/

demo:  [复旦大学](http://shuyantech.com/cndbpedia/kggraph?entity=复旦大学)



其他：neo4j， 知识图谱课程，不要过多投入，要开箱即用。赛后可以作为兴趣方向，深入研究。

可视化分析： 词云图

### 关联规则分析

度量： Support、confidence、 lift

相关算法：Apriori、FP-Growth / - skelearn

## 任务四： 疫情前后旅游产品需求的变化分析

基于历史数据，本地图谱分析，前后变化，写信：旅游业发展意见

微信公众号爬取： https://www.jianshu.com/p/8efa73f0c6e6 

搜狗微信：https://weixin.sogou.com/