+++
author = "roxlong"
title = "无线通信协议面试"
date = "2024-11-13"
description = "协议工程师岗位面试问题"
tags = [
    "无线通信",
    "LTE",
]
+++

## 1. 3GPP协议介绍
3GPP（第三代合作伙伴计划）是一个国际合作组织，由七个电信标准开发组织（ARIB、ATIS、CCSA、ETSI、TSG、ITU和TTA）组成。该组织共同制定和维护2G、3G、4G、LTE-Advanced和5G移动网络的技术规范。3GPP还与其他服务商（如手机制造商、移动网络运营商、软件供应商和电信公司）合作，以确保最新技术的发展。

## 2. 手机入网流程
手机入网（LTE空口接入、UE接入）的流程如下：
- **PLMN选择请求**：手机根据SIM卡对应的运营商扫描该运营商的频段。
- **小区搜索**：接收天线信号，完成下行时频同步获取频点和PCI。
- **系统消息接收**：接收天线的MIB、SIB，天线配置以及天线的择偶标准。
- **小区选择与驻留**：根据S准则，天线满足S>0就选择。
- **ATTACH**：附着入网，从空闲态进入连接态。
- **移动支持**：不停地搜索邻小区、取得同步并估计RSRP，决定是否进行小区重选。

## 3. LTE物理层技术
LTE物理层技术概要：
- **物理层信号处理流程**：信道编码（CRC、Turbo）、加扰、调制（星座图映射）、映射到资源栅格（OFDM调制）、按照MIMO模式发射信号。
- **LTE帧格式**：LTE的发射信号以10ms一帧的方式向外发射。每个帧又被分为10个1ms的子帧。每一个子帧包括两个0.5ms的时隙。每个时隙包含六到七个OFDM符号。一个时隙中具体是六个还是七个OFDM符号依赖于循环前缀的长度。
- **OFDM信号**：大带宽信号，同时发射大量正交经过调制（qpsk）的子载波，传输信息，按照时频资源栅格，可以在某些子载波上传用户数据、参考序列、控制信息等。
- **信号类型**：数据、同步信号、参考信号等。

## 4. LTE技术概览
LTE即长期演进，是3GPP制定的通用移动通信系统技术标准，主要指4G的通信协议。主要了解它的关键技术、空口接入流程、物理层技术包括无线帧结构等方面。

## 5. 英文自我介绍
Hello interviewer, my name is XX, studying in XX, XX major, familiar with C/C++ programming language, familiar with wireless communication protocol. And, I like XX, XX, XX these activities. I hope to join your company and work together.

## 6. LTE的四大关键技术
- **正交频分复用OFDM**：利用大量正交的子载波来传输信息，频带利用率极高，相比3G能达到3倍左右。
- **多输入多输出MIMO技术**：分为空间分解、空间复用两张，前者可以获得更好的信号质量，后者可以获得更高的传输速率。
- **自适应调制编码技术AMC**：根据链路的传输情况来自适应的选择调制编码的方式乃至分配不同的频谱资源块，来获得更高的传输效率。
- **小区抗干扰技术**：为解决相邻小区间的同频干扰，可以采取频率复用技术，如四个相邻小区，他们的中心区域使用同样的频带，边缘位置则利用剩余的频带进行频率区分，减少同频干扰。

## 7. Wi-Fi协议概览
Wi-Fi是一种允许电子设备连接到一个无线局域网（WLAN）的技术标准，通常使用2.4G或5G射频频段。它用的协议是802.11系列协议，主要运用了OFDM调制、直接序列扩频、跳频等技术。连接Wi-Fi的过程主要有三步，扫描、认证、关联。

## 8. 1G~5G技术演进
- **1G**：模拟信号，采用FDMA频分多址技术。
- **2G**：数字信号时代，采用TDMA时分多址技术。
- **3G**：采用码分多址技术，重邮研究出了第一块TD-SCDMA芯片（时分双工同步码分多址）。
- **4G**：采用OFDMA正交频分多址技术和MIMO多输入多输出，带宽更大速率更高，即LTE协议。
- **5G**：采用OFDMA，但有更高频率、更高带宽，引入了大规模MIMO、网络切片、LDPC码等新技术。

## 9. 高效率、高保密性协议设计
从保密性来说，可以采用直接序列扩频，使用伪随机码扩频，然后可以使用加扰、交织、跳频通信这些技术。从效率来看，可以采用高级的编码技术和高阶调制技术，如使用LDPC、Turbo等纠错码、使用64、256QAM等对子载波进行调制然后使用OFDM。还可以使用HARQ技术来结合纠错编码和检错编码的优势，保证效率。进一步还可以使用自适应链路方案，根据信道情况，选择最适合的编码调制方案。
