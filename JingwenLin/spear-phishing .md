https://doi.org/10.1007/978-3-030-00470-5_4

spear-phishing 鱼叉式网络钓鱼邮件

- attackers specifically target individual members of an organization using carefully crafted emails
- only few similarities between different spear-phishing attacks which makes it hard to construct effective defenses.

Common anti-spoofing techniques

- Sender Policy Framework (SPF) 

- DomainKeys Identified Mail

- Domain Message Authentication Reporting & Conformance

- didital signing of emails, such as PGP and S/MIME

  ---

- difficult to implement because  all communication parties shoule adopt the technology but actually not.

- attacker is able to exactly match  the address of a known sender.

本文工作

- discriminate thousands of senders in one mailbox and enables identifying spoofed emails with 90% detection rate and less than 1 false positive in 10,000 emails

模型概述

- receives the mailbox of a user as input ( characteristic traits in the structure of an email, which are independent from textual content and often persist over time) and applies machine learning techniques to generate profiles for all senders in the mailbox, even if only a few emails are available.
- profiles provide a content-agnostic view on the sender and enable us to spot spoofed emails as deviations from the learned profiles.

特征提取：  
- 行为特征（13种）：
  - 附件的类型，数量和顺序，例如交换多个文件时
  - 附加到电子邮件的数字签名和证书以及相应的PGP和S / MIME字段
  - 与其他电子邮件和收件人的关系，例如以References和In-Reply-To标头的形式等等

- 组成特征（客户端及其配置信息）
  - 公共标头的类型，顺序和语法
  - MIME部分中标题的类型，顺序和语法
  - 主题字段中的国际字符编码等等

- 传输特征
  - Received标头的数量和顺序，其中每个跃点由其主机名的哈希表示
  - 在交付过程中从第一个到最后一个跳的时区路径
  - 某些Received标头中提供的传递协议和TLS功能

模型：  
  - 将每个提取的特征表示为特征字符串。
  - 每一维只取0-1，代表该发件人是否有该特征。把每封邮件抽象成0-1向量。
  - 使用kNN和SVM，该方法满足即使只有非常少的训练数据也可用。其中KNN最少只需要两个数据，SVM则需要5个
  - 将攻击者分为三类：对被假冒的发送者一无所知，对被假冒的发送者的域名内基础设施信息部分已知，对被假冒的发送者已知。

结果：  
- 首先计算一个简单的统计量：对于17381发送者，我们计算其特征向量的平均值，并测量17,381个均值向量之间的曼哈顿距离 。结果表明大多数发送者之间的距离大于40.也就是不同sender之间具有较高的特异性。

- SVM分类器在少量可用电子邮件中提供更好的性能，而随着训练大小的增加，kNN分类器超过SVM.
- 随着攻击者对被假冒的发送者越来越了解，其分类器的性能越来越差。
- 传输特征具有最大的辨别力，也最难被伪装。



机器学习更适合于普通攻击，对于熟悉被攻击者的伪造攻击，是比较难的，



