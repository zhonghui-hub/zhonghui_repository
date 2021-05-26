# W2V_TextRank

## 简介
文本自动摘要算法：用Word2Vec改进的TextRank算法

## 结果对比：在5000个中文文本样本上的结果
![](/jpg/result.jpg)

## 评价指标
ROUGE1&2 ROUGE SU4 R&F[参考论文](http://www.aclweb.org/anthology/W04-1013)

## 使用说明
可以直接在命令行中运行编译好的jar包，jar包及训练好的Word2Vec模型可以在[这里下载](https://pan.baidu.com/s/1c2H4Aa8) ,密码为：7qvd
> java -jar W2V_TextRank.jar <参数>

## 参数说明
| 参数 | 说明 | 
|:---------------------|:--------|
| -m | 指定摘要算法：textrank / w2v_textrank,目前支持这两种方法。| 
| -n | 指定生成的摘要的最大字数| 
| -input | 指定输入文件路径（待摘要文本文件路径）|
| -output| 指定输出文件路径（生成的摘要文本文件路径） | 
| -w2v | 指定训练好的Word2Vec模型路径，可以在上面资源下载地址中下载已在中文维基百科上训练好Word2Vec模型文件，使用者也可以使用自己训练好的Word2Vec模型| 

## 示例
```
java -jar W2V_TextRank.jar –m w2v_textrank -n 60 –input ./article.txt –output ./summay.txt -w2v ./wiki_zh_word2vec.model
```
## 效果展示
### 原文：
四海网讯网讯，近日，有媒体报道称：章子怡真怀孕了!报道还援引知情人士消息称，“章子怡怀孕大概四五个月，预产期是年底前后，现在已经不接工作了。”这到底是怎么回事?消息是真是假?针对此消息，23日晚8时30分，华西都市报记者迅速联系上了与章子怡家里关系极好的知情人士，这位人士向华西都市报记者证实说：“子怡这次确实怀孕了。她已经36岁了，也该怀孕了。章子怡怀上汪峰的孩子后，子怡的父母亲十分高兴。子怡的母亲，已开始悉心照料女儿了。子怡的预产期大概是今年12月底。”当晚9时，华西都市报记者为了求证章子怡怀孕消息，又电话联系章子怡的亲哥哥章子男，但电话通了，一直没有人<Paragraph>接听。有关章子怡怀孕的新闻自从2013年9月份章子怡和汪峰恋情以来，就被传N遍了!不过，时间跨入2015年，事情却发生着微妙的变化。2015年3月21日，章子怡担任制片人的电影《从天儿降》开机，在开机发布会上几张合影，让网友又燃起了好奇心：“章子怡真的怀孕了吗?”但后据证实，章子怡的“大肚照”只是影片宣传的噱头。过了四个月的7月22日，《太平轮》新一轮宣传，章子怡又被发现状态不佳，不时深呼吸，不自觉想捂住肚子，又觉得不妥。然后在8月的一天，章子怡和朋友吃饭，在酒店门口被风行工作室拍到了，疑似有孕在身!今年7月11日，汪峰本来在上海要举行演唱会，后来因为台风“灿鸿”取消了。而消息人士称，汪峰原来打算在演唱会上当着章子怡的面宣布重大消息，而且章子怡已经赴上海准备参加演唱会了，怎知遇到台风，只好延期，相信9月26日的演唱会应该还会有惊喜大白天下吧。
### 人工摘要：
知情人透露章子怡怀孕后，父母很高兴。章母已开始悉心照料。据悉，预产期大概是12月底.
### W2V_TextRank：
报道还援引知情人士消息称，“章子怡怀孕大概四五个月，预产期是年底前后，现在已经不接工作了。”
