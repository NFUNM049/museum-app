# museum-app
期末博物馆动静结合api项目


文档名称 | 博物馆动静结合小程序需求文档
-|-
产品名称 | 博物馆服务助手
文档状态 | 已完成
文档作者 | 林晓君
发布日期 | 2019-12-21

### PRD 价值主张设计

#### 背景
根据调查，市面上并无辅助多动症群体和残障者群体使用的博物馆功能的app。面对观众群体的多样性 ，需要重视对残疾人和特别文化需求者这两类特殊观众开展服务 ，满足他们的文化需求，也有服务应对与进一步提升服务的需要存在。

#### 加值宣言 

为了方便多动症群体和残障者群体，给与他们在博物馆展览的过程中更好的观展体验。在拥有基本博物馆app功能的同时，我们团队开发了一个面对这些群体的其他功能来提高了他们的观展体验。同时也有利于博物馆创造了一个更加包容和公众广泛参与的环境。

* 第1个主要功能是使用室内地图实现交互性强的室内地图应用，可以进行室内搜索、室内路线规划等服务，还可以为特殊群体快速找到残疾人通道、残疾人厕所、残疾人目标、残疾人电梯等服务设施。

* 第2个功能是使用语音合成为游客提供语音导览的服务，只要有手机就可以进行导览服务、了解展品。

#### 核心价值 
为多动症患者和残障人士提供室内路线规划以及语音导览的功能，以提高这个群体在博物馆的观展体验，满足他们的文化需求。

#### 用户痛点
1.残障者游客想要走残疾人通道，但是找不到该通道，同时周围也没有工作人员可以进行询问。
2.部分游客不喜欢阅读展品介绍；游客无法进行视觉观看，需要语音导览辅助了解展品。

#### 目的
提升多动症和残障群体在博物馆的体验。

#### 目标用户
面对来博物馆观看展览的多动症和残障群体。

#### 用户需求（使用的人工智能要反映到需求列表中）
用户案例 | 使用api | 重要程度
-- | --| --
用户想要进行博物馆内搜索目标地点 | 室内地图 | 重要
用户不想看干巴巴的文字解释 | 语音合成 |重要

#### 功能
1.博物馆室内地图可实现展区位置的快速引导，残疾人通道、卫生间等服务场所的快速查找。后期希望实现并通过人流分析，为博物馆决策优化提供很好的依据。 （难点：博物馆不支持室内定位，需联系官方进行数据采集。） 
2.语音导览。为用户进行与语音的导览。

#### 用户应用场景
1，lingling带他患有多动症的小侄子去博物馆看展，他担心小侄子静不下心到处乱跑。他打开博物馆app发现竟然可以室内导航，他跟着地图指示很快找到最想看的展览区，没有在路上浪费太多时间。游览过程中，lingling使用了app中语音导览给小侄子，语音导览清晰易懂，小侄子听得十分认真和入神。

2.小荣行动不便，依靠自动轮椅行动。今天他想要去看博物馆的展览，由于行动不便他不能逛完全部展览，但是他又想看到喜欢的展览。这时他在博物馆的宣传栏中发现了博物馆app的宣传，app里能够为用户提供语音导览以及室内导览服务，这简直太好啦！跟着清晰的地图和导航，小荣没有在路上和找路上花费太多时间，很快找到了目的地，去哪都方便，还提供了专用通道、专用厕所等博物馆内导航服务，而且语音导览为小荣进行展览的讲解，比起看文字，听语音讲解更加方便。小荣对这个app十分满意，它解决了他不少问题。

### 原型
* [原型](http://nfunm049.gitee.io/museum-app)，可自行点击查看。
* [原型下载入口](https://gitee.com/NFUNM049/museum-app)，有需要自行下载。

主要功能原型展示：

![博物馆1.png](https://upload-images.jianshu.io/upload_images/9455364-6db64ff29dd85442.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

![博物馆2.png](https://upload-images.jianshu.io/upload_images/9455364-8bba8ea167d3dc01.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

![博物馆3.png](https://upload-images.jianshu.io/upload_images/9455364-8532bd4ec4d6133f.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

### api的选择与使用
#### api的选择
##### 1.语音合成

* 服务商：百度语音合成
* 服务：基于业界领先的深度神经网络技术，提供高度拟人、流畅自然的语音合成服务，让您的应用、设备开口说话，更具个性。
* 选择比较分析：我选择了百度、阿里云、科大讯飞、azure的语音合成进行比较分析，总体来说都不差，但是百度的语音服务会更加容易调用，它的语音和声调标准，个人觉得是最接近真人的语音服务。同时也提供多场景的音库，更加契合使用场景；提供语速音速可调节服务，满足个性化需求；多种调用方式，满足各种需求。另外，购买语音合成服务将会有一定程度上的优惠，性价比高。

![百度语音合成.png](https://upload-images.jianshu.io/upload_images/9455364-1b6bfd75dc20c10b.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

* 代码调用：

![语音合成代码.png](https://upload-images.jianshu.io/upload_images/9455364-21a3f995951853dd.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)


##### 2.室内地图

* 服务商：百度室内地图
* 服务：商场、火车站、机场找店、找物、找人；停车场找车位定位爱车；医院找科室；实时定位老人小孩位置防止意外发生……百度地图为您提供最*  专业的室内地图和定位服务，帮您解决室内的一切难题。
* 选择比较分析：我选择了百度和高德地图的室内地图进行对比分析，二者市场占有以及好评率差不多，但是百度的定价较低，可以节省成本。并且百度结合WI-FI、气压计、蓝牙地磁传感器等定位技术更加先进。

![百度室内地图.png](https://upload-images.jianshu.io/upload_images/9455364-6beb0251e19070d0.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

* 使用此功能需要联系百度官方进行数据采集。无代码展示。

#### api的使用

1.[语音合成](https://azure.microsoft.com/zh-cn/services/cognitive-services/text-to-eech/)

2.[室内地图](http://lbsyun.baidu.com/products/products/indoor)
