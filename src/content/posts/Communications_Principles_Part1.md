---
title: 通信原理 第一部分
published: 2025-12-23
pinned: false
description: 通信原理的课程笔记 这是绪论
tags: [课程笔记, Blogging, 通信原理]
category: 课程笔记
licenseName: "CC-BY-4.0"
author: Mints
sourceLink: "https://day-breaklight.github.io/posts/communications_principles_part1/"
draft: false
date: 2025-12-23
pubDate: 2025-12-23
---
难吗？不知道  
这一部分是概述的内容  
### 信息量
信息量：$I = \log_a \frac{1}{p(x)} = -\log_a p(x)$，$I$是消息中所包含的信息量，$p(x)$是消息发生的概率。  

常用单位是比特：$I = \log_2 \frac{1}{p(x)} = -\log_2 p(x)$ 

当有$M$个等概率波形的时候，$p = \frac{1}{M}$，信息量为$I = \log_2 \frac{1}{p} = \log_2 \frac{1}{\frac{1}{M}} = \log_2 M(b)$  

若$M$为2的整幂次，则$M = 2^k$，$I = \log_2 M = \log_2 (2^k) = k$  

$M = 4$，$I = 2$比特，$M = 8$，$I = 3$比特  
### 信息源的熵  

$$
H(X) = -\sum_{i=1}^{M} p(x_i) \log_2 p(x_i)（比特/符号）
$$

### 通信系统的主要性能指标
有效性和可靠性  
#### 有效性

码元传输速率：$R_B = \frac{1}{T}（B，波特）$  

信息传输速率：$R_b$  

二者关系：$R_b = R_B \times H(x)$  

$M$进制每个码元速率等概率时$I = \log_2 M$（b/s），$M = 2$时，码元传输速率和信息传输速率相等。  

频带利用率：  
$$
\eta = \frac{R_B}{B} \quad \text{(Baud/Hz)}
$$
或者：  
$$
\eta = \frac{R_b}{B} \quad \text{(bit/s/Hz)}
$$
#### 可靠性

误码率：  
$$
P_e = \frac{\text{错误码元数}}{\text{传输总码元数}}
$$
误信率：
$$
P_b = \frac{\text{错误比特数}}{\text{传输总比特数}}
$$
二进制有$P_e = P_b$