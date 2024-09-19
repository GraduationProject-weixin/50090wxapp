# [首页查询更多项目](https://github.com/GraduationProject-weixin) 包安装运行


# 50090wxapp体育资讯软件的实现

![picture](https://raw.githubusercontent.com/GraduationProject-springboot/.github/main/img/wx.png)

### 点击播放视频 ▼
[![Watch the video](https://i.sstatic.net/Vp2cE.png)](https://www.bilibili.com/video/BV1BPtKekEv3?p=93)


# 绪论
## 1.1 课题背景
二十一世纪是一个集数字化，网络化，信息化的，以网络为核心的社会。随着互联网的发展，传统生活变得更加方便快捷，许多事物都可以跟互联网相连接，于是就提出了“互联网+”[1]的概念，日常生活离不开计算机更离不开互联网，例如生活中最平常的衣食住行，都有其相关的智能产品，所以科技改变生活，传统的生活方式面对互联网的新浪潮的冲击，已经渐渐退出了历史舞台，相信未来的某一时刻，传统的生活方式将进入全智能化的阶段。

在信息技术迅速发展的今天，计算机技术已经遍及全球，使社会发生了巨大的变革，现今各类智能手机不断更新，智能手机的普遍使用让各种基于手机移动端的APP问世，其中，微信已是时下国内最火的聊天交流APP，备受人们青睐，近年来，微信发展规模越来越大，越来越多的人开始使用微信，目前智能手机系统的普及，人们手机上基本都有了微信，根据去年公布的一组数据中可知，微信去年最高用户量达到10亿多；而建立在微信平台基础上的小程序凭着它不用安装、不占内存、使用便捷、用完即走等众多优点[2]，小程序借着微信平台快速成长，也为各行业的发展带来了极大的便利，这使得基于微信小程序的系统应运而生，为用户提供便利。

基于以上微信的发展，结合目前用户体育资讯查询、足球周边商品购买方面的需求，开发了本基于微信小程序的体育资讯软件，更好的为用户服务。
## 1.2  设计原则
在开始开发项目之前，必须要先考虑项目的实用性、科学性，以及该项目是否能够真正让用户受益并尽可能的发挥项目的作用。因此，在开发前，通过以下几条原则对项目进行判断：

（1）可行性原则。项目需要保证经济可行性和技术可行性，这包括了项目在浏览端、服务端等方面上的经济和技术上是可以达成的。

（2）适应性原则。项目要保证可维护性和可扩展性，这是每个非短期项目都需要考虑的，并且不论是维护还是扩展，都必须要建立在适应用户的正常需求的基础上。

（3）安全性及保密性原则。要充分保证用户信息的安全性和保密性，不能因为开发上的疏忽，导致用户的信息泄露。

（4）系统工程原则。为了确保项目的整体性，在项目调查、项目分析、项目设计、项目开发的过程中，都需遵从项目工程的方法和步骤逐步进行。

（5）统一规划、分期实施、逐步完善原则。项目开发的过程中，要按照规划、分期实施，特别是要注意在项目开发过程中要有条理，从点到面，一步步完善，不要贪图进度，要循环渐进的对项目进行开发。
## 1.3  论文组织结构
本基于微信小程序的体育资讯软件在开发技术的选择上，使用JAVA技术和MYSQL数据库开发。本论文的组织结构如下：

第1章绪论。阐述论文工作的研究背景和设计原则。

第2章系统关键技术介绍。介绍构建基于微信小程序的体育资讯软件进的相关技术。

第3章系统分析。分析基于微信小程序的体育资讯软件的需求，包括系统性能分析、系统功能分析以及系统流程分析等。

第4章系统设计。根据需求分析对系统进行功能模块划分和数据库设计，并构建系统结构图以及数据库E-R图等。

第5章系统的实现。对系统主要功能模块进行界面展示。

第6章系统测试。对系统进行测试工作，发现系统bug，进行修改，确保系统正常稳定的运行。

第7章结论。总结论文的主要工作，提出进一步完善基于微信小程序的体育资讯软件的目标和明确方向。
#
37
# 2 关键技术简介
## 2.1 微信小程序
微信小程序，简称小程序，英文名Mini Program，是一种全新的连接用户与服务的方式，可以快速访问、快速传播，并具有良好的使用体验。

小程序的主要开发语言是JavaScript，它与普通web的开发有很多相似之处。小程序和普通网页开发并不是相同的东西，是有差异的。网页开发的渲染线程和脚本线程是互斥的，而在小程序中，确实分开的，分别在不同的线程之中运行。网页开发的工作者可以运用各种浏览器暴露出来的DOM API，进行DOM选中和操作，但小程序不行，它并没有一个完整的浏览器对象，因此缺失DOM API和BOM API。这样的差别使得前端开发中经常用到的一些库是无法在小程序中运行的。另外，网页开发的工作者在开发网页时所要面对的环境是在各式各样系统上运行的各式各样的浏览器，，而小程序只，只需面对iOS和Android这两道操作系统下的微信就足够了。

小程序和传统的APP相比，有着开发成本更低，获客成本更低，开发周期更短，发展空间更大等的优点。不过，为了体现“用完即走”、“无需安装”等理念，小程序的功能、性能还有大小都受到了制约，可以说是各有利弊。
## ` `2.2 JAVA技术
Java是一种多用途并且强大的编程语言，可用于开发运行在移动设备、台式计算机以及服务器端的软件。Java已及其流行。Java只要编写一次，无论什么地方都可以运行启动。

Java语言是应用很广泛的语言，用它编写出的程序十分可靠安全，并且可以在任何系统平台运行。java在线程机制上也是十分简便，其多线程的机制可以在某一时间内同时执行多个任务不会出现中断，巧妙使用这一特性可以让程序具有更好的实时行为和交互性。

Java可以是高级语言，在c++语言的基础上，取其精华去其糟粕，使其更加强大与实用。Java编程语言提供自动的垃圾回收机制，使程序员可以不用担心内存管理。
## 2.3微信Web开发者工具
为了实现微信小程序编写，腾讯公司推出微信web开发者工具[2]，用来调试编写微信小程序，微信小游戏，微信公众号的编写和调试，该软件是支持微信小程序官方API 和相应的辅助工具和插件，支持微信端的代码编辑，查看，预览，发布。该工具拥有自己的前端代码文件，视图文件是.wxml、样式文件是.wxss、交互则是JS文件[8]，当然还有支持相应的网络框架，通过接口wx.request和后台进行数据传输，通过配置https域名配置跟服务器对接并发布项目，这是一款集开发、预览、发布等功能的微信产品的开发工具，目前还在更新版本。
## 2.4微信小程序API接口
微信小程序API接口是腾讯公司为了微信小程序和微信公众号提供的接口文档，里面包含了各种需要使用的接口技术，例如本项目用到的获取微信用户信息(wx.getUserInfo)、蓝牙通讯传输功能、网络请求(wx.request)、定位功能等，总的来说，小程序API是满足一个程序开发的大部分接口。
## 2.5 MYSQL数据库
MySQL是典型的关系数据库系统，拥有开源免费、稳定、高效等特点，一直是中小型web项目的最佳数据库选择。MySQL作为当今IT领域使用人数最多的开源关系型数据库软件之一，在2018年的数据库使用率排名中位居第二，仅次于目前为止最成功的商业版数据库Orcle[5]。MySQL最大的优势之一就是无偿使用，这也是它成功的关键。

MySQL支持标准化数据库查询语言SQL。MySQL是一款非常适合个人开发者或小型组织开发团体的数据库管理系统，因为它是开源并且免费的，体积小、速度快、成本低以及其最重要的一点开放源码，深受程序设计人员的喜爱，这也让它成为了许许多多中小型开发网站数据库的首选，同时提供了多种开发的连接API。MySQL将数据的存放按照记录之间的关系存放到了不同的表中，减少了数据的冗余并且提高了开发的工作效率。MySQL支持开发中需要用的大型数据库，并能处理数以万计的记录。因为MySQL是开源的软件，所以在项目的预算中的时候不用花费额外的资金，大大降低了开发的总体成本，这也是MySQL数据库在中小型企业和独立的开发者中广泛流行的原因[1]。
#
# 3 系统分析
## 3.1 可行性分析
在系统开发之初要进行系统可行分析，这样做的目的就是使用最小成本解决最大问题，一旦程序开发满足用户需要，带来的好处也是很多的。下面我们将从技术上、经济上、操作上、法律上等方面来考虑这个系统到底值不值得开发。
### 3.1.1 技术可行性
技术可行性是指学习的技术是否能够完成本项目，如果团队本身没有相关的技术储备，而又能够迅速掌握此类技术，那项目应该达不到我们的设计要求。本基于微信小程序的体育资讯软件采用JAVA技术、MYSQL数据库开发设计，作为计算机专业学生，在学校期间就接触到许多关于编程方面的知识，当然也包括各种编程软件，对他们的了解度也比较系统，所以技术开发上面还是有一定把握。
### 3.1.2 经济可行性
经济可行性主要是研究和分析系统的投入和产出的关系，非常明了问题不能产出大于投入。由于自己本身就是学生，还没有正式参加工作，金钱上面一直都处于缺乏状态。所以在开发程序过程中，我是不会花太多经济成本在上面的。针对开发软件和数据库，还有界面设计等在百度上面就可以直接下载，然后根据各种安装视频进行安装，这些资源都是免费的，程序编码阶段使用的源代码在百度上面可以轻松获得，在有网络的环境下就能下载下来，不需要支付任何费用，经济成本很低。所以系统在开发人力、财力要求不高，具有经济可行性。
### 3.1.3 操作可行性
操作可行性主要是针对系统用户而言，一个系统再完美，技术再先进，用户不去使用，或者用户根本不会使用，该系统存在的价值也是不大的。本人自己就是学生，程序开发经验不足，在界面设计上面不会设计太复杂，要讲究简单好看，操作上要方便，不能让用户觉得不流畅。用户一旦进入操作界面，界面上就会有相应提示，跟着操作提示就可以找到对应的功能操作模块，对于用户来说免培训就能使用，没有任何学习成本，因此，操作上是可行性的。
### 3.1.4 法律可行性
开发的基于微信小程序的体育资讯软件所使用到的软件和资料来源都是图书馆、百度文库、百度网页等渠道，并不涉及违法。在个人毕业设计上面，无论源代码还是论文编写内容不存在抄袭行为。

综上所述，我们进行了四个方面的可行性研究，可以看出，该基于微信小程序的体育资讯软件的开发是没有问题的。
## 3.2 系统性能分析
随着互联网的发展，微信小程序越来越完善，现在的生活中充斥着微信小程序，由于小程序方便快捷，基于微信这个大平台，小程序发展是高速的，吃饭可以通过小程序点餐，出去玩可以用小程序打车，因此体育资讯也可以使用小程序。系统性能需求如下：

（1）软件功能清晰明了，尽量多用列表的展示简化用户操作，提升使用者体验，减少下拉菜单这种降低体验的操作。

（2）软件的功能要尽量完整，也要全面。

（3）经常的在以后版本更新完善软件，使得软件保持一个新鲜度，也可以做一些活动来促进用户使用软件。

（4）减少软件使用过程中出错，做好优化，遵循开发逻辑，降低bug的产生率以提升用户体验。
## 3.3 系统功能分析
基于微信小程序的体育资讯软件主要满足两种用户的需求，这两种用户分别为管理员和用户，下面将对这两类用户分别进行功能需求分析。

管理员：管理员用户可对系统后台对系统进行全面的管理，管理员登录后主要实现的功能模块包括个人中心、球员管理、用户管理、教练管理、赛事日程管理、赛事类型管理、联赛积分榜管理、杯赛积分榜管理、足球周边管理、商品类型管理、系统管理以及订单管理。管理员用例图如图3-1所示。

![](/md/blog.002.png)

图 3-1 管理员用例图

用户：用户通过微信平台可进行本系统，注册登录后主要功能模块包括首页、赛事日程、足球周边以及我的（用户充值、购物车、我的订单）。用户用例图如图3-2所示。

![](/md/blog.003.png)

图 3-2 用户用例图
## 3.4 系统流程分析
### 3.4.1登录流程
用户和管理员均具有登录功能，用户登录流程图如图3-3所示

![](/md/blog.004.png)

图3-3登录流程图
### 3.4.2修改密码流程
管理员登录后可进行修改密码操作，修改密码流程图如图3-4所示。

![](/md/blog.005.png)

图3-4修改密码流程图

#
# 4 系统设计
## 4.1 系统设计要求
（1）可用性。目标系统功能齐全，能够完全满足用户需求。

（2）可靠性。能连续准确的处理业务，有较强的容错能力。

（3）保密性。保证系统的物理安全、数据存储和存取的安全与保密、数据传输的安全与保密，做好使用人员的授权管理。

（4）可理解性。用户容易理解和使用该系统。

（5）可维护性和适应性。系统应易于修改、易于扩充、易于维护，能够适应业务不断发展变化的需要。
## 4.2 系统结构设计
系统的设计和划分是系统的核心研究问题，以确定整体结构和功能模块。该系统的结构化设计的思想，是自顶向下的方式将系统分成若干个子系统，以及反过来的子系统分成模块，其被划分成子模块，层划分各计算机可执行模块可迄今用作一个单独的程序。

基于微信小程序的体育资讯软件主要包括用户模块以及管理员模块两大部分，系统结构图如图4-1所示：

![](/md/blog.006.png)

图 4-1  系统结构图
## 4.3 数据库设计
### 4.3.1 数据库E-R图设计
在任何一个系统设计中，数据库都是其中至关重要的一个部分，如何选择适合的数据库并且使其的开发符合程序需要是在设计系统时所要考虑的一个关键性问题。本系统的数据库采用MYSQL进行设计和管理，其具有体积小、速度快的优势。E-R图是一种描述显示数据类型间的关系的数据描述方法，E-R图可以完整地映射出现实模型的关系。

实体与属性之间的关系：E-R图有三种基本成分，分别是实体（即数据对象）、属性、联系。所谓的数据对象是指在工作环境中所涉及到的事务用方框表示，属性则是对该事物特征的一种描述用椭圆表示。模型中的实体可以是具体的人事物也可以是某个概念。本基于微信小程序的体育资讯软件的E-R图如下所示：

1、球员信息实体E-R图如图4-2所示：

![](/md/blog.007.png)

图4-2 球员信息实体的E-R图

2、管理员信息实体E-R图如图4-3所示：

![](/md/blog.008.png)

图4-3 管理员信息实体E-R图

3、赛事类型信息实体图如图4-4所示。

![](/md/blog.009.png)

图4-4 赛事类型信息实体E-R图

4、赛事日程信息实体图如图4-5所示。

![](/md/blog.010.png)

图4-5 赛事日程信息实体E-R图

5、用户信息实体图如图4-6所示。

![](/md/blog.011.png)

图4-6 用户信息实体E-R图

6、订单信息实体图如图4-7所示。

![](/md/blog.012.png)

图4-7  订单信息实体E-R图

7、足球周边信息实体图如图4-8所示。

![](/md/blog.013.png)

图4-8  足球周边信息实体E-R图
### 4.3.2数据库表设计
基于微信小程序的体育资讯软件采用了MYSQL数据库进行系统数据的储存，主要的数据库表的具体设置如下：

表4-1  qiuyuan球员信息表

|列  名|说  明|类 型 ( 长 度 )|备  注|
| - | - | - | - |
|id|编号|bigint(20)|不允许空,主键|
|addtime|创建时间|timestamp|允许空|
|julebumingcheng|俱乐部名称|varchar(200)|允许空|
|guojia|国家|varchar(200)|允许空|
|qiuyuanxingming|球员姓名|varchar(200)|允许空|
|qiuyuanweizhi|球员位置|varchar(200)|允许空|
|qiuyuanshengao|球员身高|int(11)|允许空|
|`qiuyuantizhong|球员体重|int(11)|允许空|
|qiuyuanqiuling|球员球龄|int(11)|允许空|
|qiuyuanguoji|球员国籍|varchar(200)|允许空|
|qiuyuanzhaopian|球员照片|varchar(200)|允许空|

表4-2  users管理员信息表

|列  名|说  明|类 型 ( 长 度 )|备  注|
| - | - | - | - |
|id|编号|bigint(20)|不允许空,主键|
|username|用户名|varchar(100)|允许空|
|password|密码|varchar(100)|允许空|
|role|角色|varchar(100)|允许空|
|addtime|新增时间|timestamp|允许空|

表4-3  saishileixing赛事类型信息表

|列  名|说  明|类 型 ( 长 度 )|备  注|
| - | - | - | - |
|id|编号|bigint(20)|不允许空,主键|
|addtime|创建时间|timestamp|允许空|
|leixing|类型|varchar(200)|允许空|

表4-4  saishiricheng赛事日程信息表

|列  名|说  明|类 型 ( 长 度 )|备  注|
| - | - | - | - |
|id|编号|bigint(20)|不允许空,主键|
|addtime|创建时间|timestamp|允许空|
|saishileixing|赛事类型|varchar(200)|允许空|
|bisairiqi|比赛日期|date|允许空|
|kaishishijian`|开始时间|datetime|允许空|
|jieshushijian|结束时间|datetime|允许空|
|lunci|轮次|varchar(200)|允许空|
|`zhuangtai|状态|varchar(200)|允许空|
|zhudui`|主队|varchar(200)|允许空|
|kedui|客队|varchar(200)|允许空|
|saikuang|赛况|longtext|允许空|
|`zhaopian|照片|varchar(200)|允许空|

表4-5  yonghu用户信息表

|列  名|说  明|类 型 ( 长 度 )|备  注|
| - | - | - | - |
|id|编号|bigint(20)|不允许空,主键|
|addtime|创建时间|timestamp|允许空|
|zhanghao|账号|varchar(200)|允许空|
|mima|密码|varchar(200)|允许空|
|xingming|姓名|varchar(200)|允许空|
|xingbie|性别|varchar(200)|允许空|
|shouji|手机|varchar(200)|允许空|
|youxiang|邮箱|varchar(200)|允许空|
|zhaopian|照片|varchar(200)|允许空|
|jifen|积分|floa|允许空|
|money|余额|floa|允许空|

表4-6  orders订单信息表

|列  名|说  明|类 型 ( 长 度 )|备  注|
| - | - | - | - |
|id|编号|bigint(20)|不允许空,主键|
|addtime|下单时间|timestamp|允许空|
|orderid|订单编号|varchar(200)|允许空|
|tablename|商品表名|varchar(200)|允许空|
|userid|用户编号|bigint(20)|允许空|
|goodid|商品编号|bigint(20)|允许空|
|goodname|商品名称|varchar(200)|允许空|
|picture|商品图片|varchar(200)|允许空|
|buynumber|购买数量|int(11)|允许空|
|price|价格|float|允许空|
|discountprice|折扣价格|float|允许空|
|total|总价格|float|允许空|
|discounttotal|折扣总价格|float|允许空|
|type|支付类型|int(11)|允许空|
|status|状态|varchar(200)|允许空|
|address|地址|varchar(200)|允许空|
|tel`|电话|varchar(200)|允许空|
|consignee|收货人|varchar(200)|允许空|

表4-7  zuqiuzhoubian足球周边信息表

|列  名|说  明|类 型 ( 长 度 )|备  注|
| - | - | - | - |
|id|编号|bigint(20)|不允许空,主键|
|addtime|创建时间|timestamp|允许空|
|shangpinmingcheng|商品名称|varchar(200)|允许空|
|shangpinjiage|商品价格|int(11)|允许空|
|shangpinleixing|商品类型|varchar(200)|允许空|
|shangpinjianjie|商品简介|longtext|允许空|
|shangpintupian|商品图片|varchar(200)|允许空|
|thumbsupnum`|赞数|int(11)|允许空|
|crazilynum|踩数|int(11)|允许空|
|jifen|积分|int(11)|允许空|
|`price|价格|floa|允许空|
#
# 5系统的实现
## 5.1 用户功能模块的实现
### 5.1.1用户注册登录界面
没有账号的用户可首先进行注册操作，注册后可进入登录界面输入用户名和密码进行登录系统，用户注册登录界面的运行效果如图5-1所示.

![](/md/blog.014.png)![](/md/blog.015.png)

图5-1 用户注册登录界面
### 5.1.2首页界面
用户登录后进入系统首页界面，用户可根据需求查看所需信息，首页界面的运行效果如图5-2所示.

![](/md/blog.016.png)

图5-2 首页界面
### 5.1.3赛事日程界面
用户在赛事日程界面可根据条件快速查询所需赛事日程信息，并可选择赛事日程查看详情信息，可选择进行收藏、点赞、踩等，赛事日程界面如图5-3所示。

![](/md/blog.017.png)![](/md/blog.018.png)

图5-3 赛事日程界面
### 5.1.4足球周边界面
用户在可进入足球周边界面查看足球周边商品信息，并可选择查看详情，足球周边界面展示如图5-4所示。

![](/md/blog.019.png)![](/md/blog.020.png)

图5-4  足球周边界面
### 5.1.5我的订单界面
用户可进入我的订单界面查看个人订单信息，我的订单界面如图5-5所示.

![](/md/blog.021.png)

图5-5 我的订单界面
## 5.2 管理员功能模块的实现
### 5.2.1管理员登录界面
管理员要想进入系统后台对系统进行管理，必须进行登录系统后台，管理员登录运行效果图如图5-6所示 。

![](/md/blog.022.png)

图5-6 管理员登录界面
### 5.2.2赛事日程管理界面
管理员可添加、修改和删除赛事日程信息，同时也可查看评论信息，赛事日程管理界面展示如图5-7所示。

![](/md/blog.023.png)

图5-7 赛事日程管理界面
### 5.2.3足球周边管理界面
管理员在足球周边管理界面可查看已有足球周边信息，对已有足球周边信息管理员可进行修改和删除操作，同时管理员也可添加足球周边信息，足球周边管理界面展示如图5-9所示。

![](/md/blog.024.png)

图5-9 足球周边管理界面
### 5.2.4用户管理面
管理员可新增、修改和删除用户信息，用户管理界面如图5-10所示 。

![](/md/blog.025.png)

图5-10 用户管理界面
### 5.2.5球员管理界面
管理员能够增删改查球员信息，球员管理界面如图5-11所示 。

![](/md/blog.026.png)

图5-11  球员管理界面
### 5.2.6订单管理界面
管理员可管理所有订单信息，订单管理界面如图5-12所示 。

![](/md/blog.027.png)

图5-12  订单管理界面

#
# 系统










