---
title: "管理备份"
description: 本小节主要介绍如何对备份进行管理。
draft: false
weight: 3
---

## 场景描述

该任务用于指导用户对列表内的备份进行管理，包括修改信息、绑定/解绑标签、共享备份、基于备份创建资源、删除备份以及回滚数据等操作。

## 前提条件

已获得**云平台**的登录账户和密码。

## 操作步骤

### 修改属性

1. 登录管理平台。

2. 在顶部导航栏，选择**备份**，进入**备份存储空间**列表页面。

   ![manage_backup_1](../_images/manage_backup_1.png)

3. 点击备份所在行右侧的更多操作<img src="../_images/more_operation.png" style="zoom:50%;" />，选择**修改**，在弹出的**修改属性**的窗口中输入备份的新名称以及相关描述，点击**修改**即可。

   ![manage_backup_2](../_images/manage_backup_2.png)

### 绑定/解绑标签

1. 在顶部导航栏，选择**备份**，进入**备份存储空间**列表页面。

2. 点击备份所在行右侧的更多操作<img src="../_images/more_operation.png" style="zoom:50%;" />，选择 **标签**，点击**绑定标签**，在弹出的**绑定标签**窗口中，选择待绑定至当前备份的标签，点击**绑定**即可。

   > **说明：**
   >
   > - 若当前平台内没有可用的标签，可参考[创建标签](/ops_tool/label/create_label)相关内容。
   > - 可绑定单个或多个标签。

   ![manage_backup_3](../_images/manage_backup_3.png)

3. 点击备份所在行右侧的更多操作<img src="../_images/more_operation.png" style="zoom:50%;" />，选择 **标签**，点击**解绑标签**，在弹出的**解绑标签**窗口中，删除待解绑的标签，点击**确定**即可。

   ![manage_backup_4](../_images/manage_backup_4.png)

### 共享备份

1. 在顶部导航栏，选择**备份**，进入**备份存储空间**列表页面。

2. 点击备份所在行右侧的更多操作<img src="../_images/more_operation.png" style="zoom:50%;" />，选择 **共享备份**，在弹出的**共享备份**窗口中，输入当前备份的分享对象的用户名或用户 ID，点击**共享**即可。

   ![manage_backup_5](../_images/manage_backup_5.png)

3. 点击**正在共享**的备份所在行右侧的更多操作<img src="../_images/more_operation.png" style="zoom:50%;" />，选择 **撤销共享备份**，在弹出的**选择需要撤销共享的用户账号**窗口中，选择待撤销共享的用户，点击**确定**即可。

   ![manage_backup_6](../_images/manage_backup_6.png)

### 基于备份创建镜像

若备份点是基于虚拟主机系统盘创建，则通过该备份点可以创建新的镜像，基于此镜像可以创建多台和备份点相同的虚拟主机。


1. 在顶部导航栏，选择**备份**，进入**备份存储空间**列表页面。

2. 点击基于虚拟主机创建的备份所在行右侧的更多操作<img src="../_images/more_operation.png" style="zoom:50%;" />，选择 **创建镜像**，在弹出的**创建镜像**窗口中，输入镜像名称，点击**创建**即可。

   ![manage_backup_7](../_images/manage_backup_7.png)

3. 在顶部导航栏，点击**资源** > **镜像**，进入镜像列表页面，选择**自有**页签，可查看到基于备份点创建的镜像显示在列，且状态为`可用`。

   ![manage_backup_8](../_images/manage_backup_8.png)


### 基于备份创建硬盘

若备份点是基于硬盘创建，则通过该备份点可以创建新的硬盘，该新硬盘将拥有和备份点相同的数据。

1. 在顶部导航栏，选择**备份**，进入**备份存储空间**列表页面。

2. 点击基于硬盘创建的备份所在行右侧的更多操作<img src="../_images/more_operation.png" style="zoom:50%;" />，选择 **创建硬盘**，在弹出的**创建硬盘**窗口中，输入硬盘名称，点击**创建**即可。

   ![manage_backup_9](../_images/manage_backup_9.png)

3. 在顶部导航栏，点击**资源** > **存储** > **硬盘**，进入硬盘列表页面，可查看到基于备份点创建的硬盘显示在列，且状态为`可用`。

   ![manage_backup_10](../_images/manage_backup_10.png)

### 回滚

1. 在顶部导航栏，选择**备份**，进入**备份存储空间**列表页面。

2. 点击备份的名称进入其详情页面，选择**备份**页签，点击备份链所在行右侧的更多操作<img src="../_images/more_operation.png" style="zoom:50%;" />，选择**回滚**，在弹出的回滚窗口中，点击**回滚**即可。

   ![manage_backup_11](../_images/manage_backup_11.png)

### 删除备份

1. 在顶部导航栏，选择**备份**，进入**备份存储空间**列表页面。

2. 点击备份所在行右侧的更多操作<img src="../_images/more_operation.png" style="zoom:50%;" />，选择 **删除**，在弹出的删除窗口中，点击**删除**即可。

   ![manage_backup_12](../_images/manage_backup_12.png)


