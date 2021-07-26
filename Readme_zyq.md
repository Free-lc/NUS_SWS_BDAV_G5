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

## 2021/07/25/ 11:00

## story telling

##### 介绍数据集

数据集的来源，时间范围；数据集介绍：有哪些文件，包含了哪些维度的数据。

##### 背景介绍

###### What is the Motivation?

我们作为一家互联网公司的应用开发者，希望通过分析数据，更直观地看到不同应用的市场表现，并探究那些热门应用是如何取得成功的。

As app developers, we aim at developing superior and popular applications. To achieve this, we should follow voice of users hiding behind numerous feedback data from the Internet. This time, we have got a dataset scrubbed from  Google Play Store. It consist of information about 10 thousands of applications from more than 30 popular categories, including there installation number, rating, reviews, price, content rating, size, etc.  

###### Who are the Target audience?

The general public that includes....





###### What is the intended effect?

让观众了解应用市场当下的热点是什么，以及背后的推动因素。尤其是帮APP developers 开发出更符合市场需要的优秀应用。

背景介绍：数据集的来源，时间范围；数据集介绍：有哪些文件，包含了哪些维度的数据。

### data cleaning 

googleplaystore.csv

起初我们利用筛选器查看各个维度数据的范围，发现其中有异常值，是由于数据错位所致，于是进行手工调整。

At the beginning we used the filter in Excel to look at the range of data of each index. And we found a few outliers caused by misplacement in one row. And we rectified these items manually.

没有评分的应用，默认评分为0.

Then, in terms of apps without rating information, we fill up with zero.

为了便于按数值处理，我们将installations数据的加号去掉，把size的单位统一为kilobyte，把价格前的$去掉。

After that, for the convenience of calculation, we remove the plus mark of installs and the dollar mark of price. Then we convert Mb of app size to Kb, and remove the unit, similarly.

然后我们将最近更新统一为M/D/Y的形式。

根据APP名称删除重复值，每个APP仅保留一个条目。

googleplaystore_user_reviews.csv

首先我们把含有空缺值Nan的条目删掉。接着发现了数据错位并手动调整，和第一个文件一样。

## 2021/07/26/00:48 ppt of Q4

## speech draft of Q about price

### 1

我们首先来看下载量。这两个饼图是基于不同价格区间应用的总下载量制作的。首先来看这个小的，我们可以明显看到免费应用平均下载量的巨大优势，和付费应用相比。换句话说，大多数用户下载免费应用。实际上我们将minor part夸大了，付费部分几乎不可见。

Hello. Now I'll share my analysis of price.

I'll analyse installations and rating as well.

First let's look at the total amount of installation. From this pie chart, you can see a preponderance of free apps. That means more users download them. 

Then let's look at the minor part--paid apps. In fact, it should have been almost invisible.

Look at this big chart. We divide paid apps into some ranges like this.（用鼠标指）And the percentage is the proportion of total installations. 

You can see apps less than $5 here(用鼠标指). Their total installations account for nearly 3 quarters.

So we can conclude that people prefer cheaper apps. For app developers, if you want greater popularity, you'd better control the price. To share the cost, you can insert ads or necessary charge into your apps.

更具体地，我们从里面排除掉免费应用，就得到了这个大饼图。我把价格分为这几个区间：xxxxx。我们可以看到，小于5美元的应用几乎占了总下载量的四分之三。

结论：人们更愿意下载便宜的应用。所以为了获得尽量多的下载量，我们要尽量让应用的价格在较低水平。我们可以通过内置广告或引入额外收费服务to share the cost。

### 2

接下来我们看一些关于rating的有趣的东西。

这是不同价格区间的rating分布

Next, let's see something interesting about rating.

This bar chart is about the distribution of rating in different price ranges.

This is free group and these are paid groups(指). In each group you can see the maximum, minimum and average of rating. And darker color means more installations.

Then you can see the paid apps with more installations, with darker color here. Their ratings are generally above 4. However, not all the popular free apps receive high rating.

That's to say, users are probably more particular about an app if it's paid. So paid apps may depend more on their quality. 

(视时间)For users, that means you can rely  more on installation ranking  when you visit the Google Play Store.









