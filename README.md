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

APP LAYER: HTTPS请求检测恶意软件, EMAIL，HTTPS载荷聚合检测

TRANS/IP: 网络流数据

DL/PHY: SNR/IEEE802.11 MAC协议

FUTHER WORK：5(未来方法)

DL/PHY 导言

### LI:

APP LAYER: DNS(DGA), 广告插入

FUTHER WORK: 1(数据) 2(面向连接网络) 4(3种攻击)

APP LAYER 导言

### HU:

TRANS/IP: TLS, IP ENTROPY, Traceroute-DoS, PFA

DL/PHY: autoencoder

TRANS/IP导言

FUTHER WORK: 3(不同层)
