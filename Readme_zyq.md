## 2021/07/19/16:55 

Average install and rating in different categories

## 2021/07/20/17:28	

./zyq/demozyq.twb

应用个数：免费APP的个数8886个，付费APP总共只有约400个。

价格分布：付费APP的价格从$0.99到$400不等。

平均下载量：免费应用占压倒性优势。

平均reviews：除了$6.99价位外，免费应用占压倒性优势，这是因为这个价位的APP不多，而其中的我的世界、侠盗猎车手等游戏特别火爆，拉高了平均值。

平均rating：和价格没有明显关系。

个人意见：install和reviews应该比price的决定因素更大，评论数多了，rating才更具普遍性，表明应用更可能符合大多数人的需求。在rating相近的情况下，推荐更多人用的应用；若installs/reviews也相近，再考虑推荐价格更低的应用，总之是Price的权值低一些比较好。

提一个关于installs的问题：大家觉得怎么处理只有几百人几十人评论而rating接近5.0的APP排行的位置？我个人觉得这样的高评分可能不太有普适性，不该排在高下载量应用的后面，所以需要让install在公式中有一个关键权值来避免这种现象。

## 2021/07/21/10:35	data cleaning

### Cleaning Process

googleplaystore.csv

1. 每个APP只保留一条记录
2. rating：将Nah值替换为0.0
3. size：将单位为Mb的数据换算为用Kb表示，并把后缀K去掉
4. installs：去掉后缀+，当成数值处理
5. price：去掉符号$，处理成数值
6. Last Update：统一为M/D/Y格式



1. Remove duplicate records of each app.
2. Rating: Replace Nah value with 0.0
3. Size: Convert MB to KB, and remove the rear mark "K".
4. Installs: remove the sign "+" and consider it a numerical value.
5. Price: Remove the sign "$", and consider it a numerical value.
6. Last update: Unified as M / D / Y format

googleplaystore_user_reviews.csv

​			删除评论信息为空的条目

​			Delete items with empty comments.

## 2021/07/21/

### 中位数比较

installs：由于installs的取值比较模糊，看不出定价本身的明显关系，只能得知超过50000的应用定价均分布在$0~$13.99内。

reviews：由于付费应用本身较少（753个，免费应用8886个），而某些特定售价的应用更少甚至只有一个应用，中位数就是其本身

## 关于price的问题

- 



Dear Dr Danny,

I am Zhao Yingqi from SWS-BDAV-group 5.

We have considered your suggestions this afternoon and discussed about them. I think we misunderstand the "Critical business question" and consider it is task-like and is equal to the motivation of our Project. And we should find some important factors and solve it hence. Actually we stand in the shoes of general public all the while and believe that the merely significant motivation is that there should be a recommendation that reflects what are the characteristics of apps that users prefer. Therefore, we concentrate on finding contributing factors and consider questions like what's the most popular category or what the appropriate size scope of a game app, etc.,  may not attract our audience.

However, we find that we can't get sufficient facts from data that can lead to a sound recommendation. I realize that we may have considered it from a too high and ambitious perspective.

Should we rectify our guideline and focus more on appropriate charts and smooth storytelling? Can we choose questions like whether rating of an app contributes to its installations, of which the answers can be got directly from visualization of data, as one of our business-critical questions?

We're looking forward to your advice.

regards

Zhao Yingqi





Dear Dr Danny

“then consider what are the business critical questions for your GENERAL PUBLIC audience.”

I wonder what public audience means? Is it means speaker should say things useful for public or say things with few commercial terms that all public can easily understand?

regard

Zhao Yingqi
