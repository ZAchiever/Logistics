<font face="黑体" color=blue size=6>物流仿真实训教程攻略（物流公司）</font>
合法摸鱼从你我做起，以下操作会节约你大量的时间同时还可以减少会计的工作量

# 前期准备公司注册
~~战术鸽一会~~
## 接单
交给队友，那种善于拉皮条的那种。负责开价的也是学生他也不知道合适的定价（当然我们也不知道）多谈一下运用一下谈判的技巧或许有意想不到的效果。请记住任何生意都是由商谈的余地的![](https://github.com/ZAchiever/Logistics/blob/master/picture/%E8%A1%A8%E6%83%85%E5%8C%85/%E5%88%92%E6%B0%B4.jpg 'e')。  

不要被想象力限制适当不要脸有奇效，这就算真实的商战这能让你无往不利。我们的队友就成功帮我们省了一大笔费用（不过被友商背刺。。。）

# 运输
## 基础信息
你若完全不想管这些，我这里有现成的程序，点[这里](https://github.com/ZAchiever/Logistics#%E4%BD%BF%E7%94%A8%E6%96%B9%E6%B3%95)进入教程  

以下为运输的的网店分布  
![网点分布](https://raw.githubusercontent.com/ZAchiever/Logistics/master/picture/%E6%8D%95%E8%8E%B7.PNG '图片')
看上去确实很简单，因为点到点之间的路只有一条，看上去就很友好了。  
**为了区分上下区块我个人将上半部分加上A_，下半部分为B_。如XN’我就把它写作A_XN1**。
最开始我们的运输设备(运力一栏左边为原材料数量右边为产成品数量)
|  车型   | 拥有数量  | 运力  |空载每百公里耗油|空载每百公里耗油|
|  ----  | ----  | ---- | ---- | ---- |
| A  | 15 | 720/550 |25L|30L|
| B | 18 | 600/450 |20L|25L|
| C  | 15 | 400/300 |15L|20L|
**运输时每车需要两个司机**
|  司机  |  25人   |  工资1500   |  行程超过25万公里按15元/每公100里加钱   |
|  ----  |  ----  |  ----  |  ----  |

显而易见的是用A车是最赚的，司机略显不够可以开头招募几个。
***
## 实际操作
以下为本公司的实际业务流程
>客户发来运输请求
- 物流公司计算报价（订单一般不会取消为简化流程以下合同一并给出）
- 给出运输合同
- 给出提货单
- 给出托运单
>合同和托运单客户盖章回执  

>提货单给运送目的地的公司盖章回执（这一步骤可以交给客户去完成因为我们联系他们的客户非常麻烦）  
- 物流公司填制记录
1.托运接单的记录(包含起点、终点、托运公司、目的地公司、种类及数量、最早到货时间、最晚到货时间、实际到货时间)
2.填写汽车的调度（以车为单位的记录，记录工作的时间、总里程、总耗油、目前所在的地点）
3.填制司机的调度（以人为单位，记录工作时间、总里程、上次在哪辆车上）
4.运输调度详细记录（以运输计划为单位，每一辆车的运输或铁路运输都算一次，记录运输方式、运输的货物、数量、起运时间、到达时间、总油耗（铁路水路不写）、依旧参与的司机与汽车（水路铁路同上））
[示例点这里](https://github.com/ZAchiever/Logistics/tree/master/storage)
- 将合同发给会计，做记录汇总
- 催收账款，填开发票回执给客户
- 会计做账，将说有凭证上传（合同、托运单、提货单、发票）

# 问题所在
>**大量的表单，耗时耗力**
一笔业务我们需要填制至少三张表单，同时为了详细的记录我们需要修改四张表单，仅仅是填写表单这一项就要耗费大量的精力，甚至需要加班  

>**运输报价麻烦至极**
首先是计算车型和数量,再计算里程最后汇总还要考虑铁路和水路,才能把报价给出需要大量时间和精力

>**有必要但不想填的运输记录**
没一笔业务要想完整的记录需要填的东西是真的多,而且万一哪个地方写错了会计是要找你麻烦的(一点点金额写错会计就很难受).完整的记录是有必要的.

>**可怕的运输逻辑**
看上去业务流程并不复杂,但是如果仔细考量一线就会发现这并不简单.有四个最突出的问题
1.所有人的时间并不统一,前一个客户给的单是5月份的,但下一个客户给的单是四月份的,而且他们的订单发布时间是随机的但都很急你需要在较短的时间给他们相关的合同之类的.
2.有事车并不能装满,这个时候同路捎带就显得非常的有必要,但是时间都是混乱同时如果加上铁路水路需要规模运输同时出发的这个问题该这样去解决呢
3.空载,这个是我们不想看到的,运输的时候再算就很麻烦
4.车的选择,空地最少不代表成本最低,找到最低成本的车不代表你有,你这个时间段端找到的最优解或许一天后有一辆车完成了他手头的任务,你算出的解就不是最优的解,需要考虑时间段,还有其他任务的影响.
# 我的程序
正如你所见以上就是我的程序源代码,再精力了两天的高强度且无聊的工作后我被迫写的.能大幅减少工作
## 便利之处
输入起点 终点 种类 最早起运时间 最晚到货时间后
再输入客户公司名字 客户要发往的公司 客户所在的教室
最后再依次输入 种类 数量
最后按下enter键就可以输出填制好的合同,提货单,托运单还可以吧运输计划填制好.
## 使用方法
1.下载python(建议下载anaconda,安装是勾选添加python到path)
2.进入cmd,输入pip install python-docx #输入后按enter
3.下载源代码,解压
4.复制main.py所在的文件夹的路径即main.py在的那个文件夹
5.cmd输入cd (你刚才复制的路径)
6.输入python main.py
7.按提示输入
8.输出完成后所有表单在文件夹all_you_need里,记录在storage内,_0代表上次的记录(第一次记得删除将初始文件内的东西覆盖到storage内)
9.重复6即可进行下一次填制
## 逻辑上的bug及不足
1.每一笔业务是独立的,这虽然提高了效率,但同时也放弃了同路捎带的机会
2.海外运输需要手动填制.没有写相关逻辑(懒!)
3.循环列表导致列表前的车工作量报表,后面的却可以摸鱼.
4.每次只考虑最找算出的车型,不会动态调整,导致其他车摸鱼.
5.司机会被跨点调用(即不考虑司机位置)
6.自动化不足
# 解决之道
1.固定时间点开始填制,就可以考虑捎带问题,同时也解决了时间的不统一
2.看论文剽窃别人的算法(领域算法,插入算法啥的,目前不想写....)
# 写在最后
自动化的强大的,摸鱼真开心 
