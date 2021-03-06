---
title: "资源图形化"
description: 本小节主要对云平台的物理资源页面中的管理节点进行介绍。
draft: false
weight: 4
---
## 功能描述

资源图形化功能提供整个环境的逻辑拓扑，可从计算节点 (物理机) 到虚拟机再到硬盘三个关联维度的查看拓扑图，可查看计算节点的物理资源使用状况、虚拟机的资源使用情况 (CPU、内存使用率、网卡流量)，以及挂载硬盘（系统盘和数据盘）的用量、性能监控数据。


## 场景描述

该任务主要用于指导用户查看当前平台内整个环境的逻辑拓扑图。
## 前提条件

已获得**云平台**的登录账户和密码。


## 操作步骤

   
### 查看物理节点

1. 登录管理平台。


2. 在顶部导航栏，选择**物理资源** > **资源图形化**，进入资源图形化页面。该页面会显示当前平台内的所有物理节点，以及相应节点上的主机和硬盘资源。

3. 在**资源图形化**页面，点击相应的物理节点图形化标志，该页面会显示所选物理节点上所有运行中和已关机状态的**主机**，右侧卡片显示了当前物理节点上基本信息以及物理和虚拟的 CPU、内存、硬盘使用情况。

   > **说明：**
   > 
   > “绿色”标识的主机状态为运行中，“黄色”标识的主机状态为已关机。


   ![resource_imaging_1](../_images/resource_imaging_1.png)

4. 将鼠标悬停至物理节点详情卡片的相关资源使用情况的进度条上，可显示具体的数值。

   ![resource_imaging_2](../_images/resource_imaging_2.png)

### 查看主机

1. 进入**资源图形化**页面，点击相应的物理节点图形化标志，在**主机**的列表中，点击其中一个虚拟节点，右侧卡片显示了当前虚拟机的基本信息以及 CPU、内存使用率 (%) 和网卡流量情况。

   ![resource_imaging_3](../_images/resource_imaging_3.png)


2. 在**主机**列表右侧的**搜索框**内输入主机名或主机 ID，可对列表进行筛选.


   ![resource_imaging_4](../_images/resource_imaging_4.png)

 ### 查看硬盘

1. 进入**资源图形化**页面，点击相应的物理节点图形化标志，在**主机**的列表中，点击其中一个虚拟节点，在**硬盘**列表中将显示，当前虚拟节点上所挂在的所有硬盘。点击硬盘的图形化标符，右侧卡片将显示该硬盘的基本信息以及当前使用率 (%)、吞吐 Kb/s 和 IOPS。

   ![resource_imaging_5](../_images/resource_imaging_5.png)


















