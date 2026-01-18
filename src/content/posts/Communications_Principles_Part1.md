---
title: 通信原理 第一部分
published: 2025-12-23
pinned: false
description: 通信原理 绪论
tags: [课程笔记, Blogging, 通信原理]
category: 课程笔记
licenseName: "CC-BY-4.0"
author: Mints
sourceLink: "https://day-breaklight.github.io/posts/communications_principles_part1/"
draft: false
date: 2025-12-23
pubDate: 2025-12-23
---
这里是按照樊昌信的《通信原理》第七版写的，但是我们学校教材并不是这个……算了不重要……  
## 通信系统的端到端框架
![通信原理 概览](/assets/images/communications_principles.png "通信原理 概览")  
### 模拟通信系统
模拟信息源 → 调制器 → 信道 → 调制器 → 受信  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;↑  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;噪声  
**存在的两种变换**
1. 发送端：把连续信息变换成原始点信号（基带信号）（信源）  
接收端：把电信号变换成连续消息（受信）  
2. 调制器：把基带信号变换成合适章信道中传输的信号（调制后，变为已调信号）  
解调器：把传输来的信号变换成基带信号  

**已调信号：经过调制后的信号，已调信号的频谱通常具有带通形式，又称带通信号或频带信号**  
### 数字通信系统  
信息源 → 信源编码 → 加密 → 信道编码 → 数字调制 → 信道 → 数字解调 → 译码 → 解密  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;↑&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;↓  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;噪声源&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;受信 ← 信源译码  
**信源编码**：1. A/D转换 模拟信号转为数字信号  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;2. 提高信息传输的有效性，即通过某种数据压缩技术设法减少码元数目和降低码元速率。  
**信道编码**：信道编码的目的用于增强数字信号的抗干扰能力为了应对噪声，根据一定规则加入保护成分反过程为信道译码  
**加密解密**：保证信息安全  
**调制与解调**：把基带信号的频谱搬移到高频处，形成合适在信道中传输的带通信号  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; ASK FSK PSK DPSK （基带传输调制与解调）  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;接收端可以采用相干解调或非相干解调还原数字基带信号  
**同步**：收发两端的信号时间上保持一致  
### 数字通信的特点（与模拟通信比较）  
1. 抗干扰能力强，噪声不累积（数字接收，仅判断0/1，模拟通信则要恢复所有值  
2. 差错可控，可以使用信道编码技术  
3. 便于用现代数字信号处理技术对数字信道进行处理，变换，储存  
4. 易于集成，使设备微型化  
5. 易于加密，保密性好  
## 重要概念与辨析   
### 模拟信号与数字信号区分  
**模拟信号与数字信号概念**  
模拟信号与数字信号  
按照取值不同：  
模拟信号：电信号参量取值连续（不可数，无穷多），则称之为模拟信号。参量取值连续，可以在时间离散的情况下  
数字信号：电信号的参量取值尽可能是有限个值。  
**<div align="center">模拟信号≠时间连续</div>**  
**<div align="center">数字信号≠时间离散</div>**  
消息传递的方式，是通过电信号来实现，即把消息寄托在电信号的某一个参量上（如幅度、频率、相位等）  

### 通信系统分类  
### 通信系统方式