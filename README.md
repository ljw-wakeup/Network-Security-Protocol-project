# 网络安全协议大作业

目前选定的主题为，查询本课程相关领域最新的研究内容和研究点，并以某个方向为题撰写原创性小论文一篇。

选定的方向为，基于网络的入侵检测。

## 要求

不少于6页，正文字体为5号字体，单倍行距。

英文参考文献如果是会议论文请主要参照2016之后的，而如果是期刊论文则主要参考2017年之后的，直接相关的参考文献不少于8篇。

论文不要拘泥于翻译多篇文献，要从整体上进行把握，反映一个方向。

提交报告请在文末列出详细的参考文献，同时在文中的引用处进行标注。

材料必须是在自己读懂的基础上进行总结的，而不是直接翻译，同时不要将报告变成科普，需要有深度具有学术性。

## 文章框架

### APP LAYER:

1. **Protocol**: DNS(DGA), HTTPS;

2. **content**: AD INJECTION, SPOOF EMAIL;

### TRANS/IP:

1. **Machine learning**: TLS, flow data;

2. **non-ML**: IP ENTROPY, Traceroute-DoS, PFA;

### DL/PHY:

1. **DL**: autoencoder;

2. **PHY**:  Wireless;

### FUTHER WORK

1. DNS database -> data resource / data labeling for ML algorithms
    AGA - attack generate algorithm

2. ATM / MLPS - state-based network IDS
    easy to detect

3. APP layer too many various kinds - middleware; no many methods on direct DL layer and PHY;
    multiple layer co-operate

4. IDS facing: 3 attacks unknow attack - update + specific attack

5. non-proba - information theory - information network

    graph

    true negative; false positive - theoritical limitation

    adverisary AI

## 分工

### LIN:

文章整体润色

DL/PHY 导言

APP LAYER: 基于HTTP的恶意软件检测, 基于HTTP的负载聚合技术, 基于非文本特征的鱼叉式钓鱼邮件检测

TRANS/IP: 使用数据报报头信息进行检测

DL/PHY: 基于信噪比的干扰攻击入侵检测, 基于802.11的欺骗与干扰检测

FUTHER WORK：5(使用非统计方法)

### LI:

文章润色

APP LAYER 导言

APP LAYER: 利用NXDomian流量检测DGA, 通过网页元素表示检测广告注入

FUTHER WORK: 1(数据来源) 2(面向连接型网络) 4(NIDS检测的攻击类型)

### HU:

协调通从绘画

文章整体润色

整体导言部分

TRANS/IP导言

TRANS/IP: 使用TLS证书进行检测, 使用熵和评分方法检测, 检测新型DDoS攻击——目标链路泛洪攻击, 使用有限状态机检测TCP拥塞攻击

DL/PHY: 直接利用字节流进行入侵检测

FUTHER WORK: 3(协议栈各层)
