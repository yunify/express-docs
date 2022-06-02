---
title: "加载密钥至主机"
description: 本小节主要指导用户使用已创建好的 SSH 密钥。
draft: false
weight: 2
---

## 场景描述

该任务主要用于指导用户在云平台内将已创建成功的 SSH 密钥加载至虚拟主机。

## 前提条件

- 已获得**云平台**的登录账户和密码。

- SSH 密钥列表中已存在创建成功的密钥。

## 操作步骤

1. 登录管理平台。

2. 在顶部导航栏，选择**资源** > **SSH 密钥**，进入 SSH 密钥列表页面。
 
   ![use_ssh_1](../../_images/use_ssh_1.png)

3. 点击待使用的密钥所在行右侧的更多操作<img src="../../_images/more_operation.png" style="zoom:50%;" />，选择**已绑定到主机**，点击**绑定**，在弹出的**选择主机**窗口中，选定待绑定的主机，点击**确定**即可。

   > **说明：**
   >
   > 可选择单个或多个虚拟主机进行加载。

   ![use_ssh_2](../../_images/use_ssh_2.png)

4. 返回 SSH 密钥列表页面，可查看 SSH 密钥上所绑定的资源。

   ![use_ssh_3](../../_images/use_ssh_3.png)

4. SSH 密钥加载至虚拟主机成功以后，可通过SSH 密钥访问虚拟主机，详情可参考[连接主机](/resource//virtual/expresscloud/link_virtual)相关内容。






