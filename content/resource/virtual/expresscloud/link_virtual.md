---
title: "连接 ExpressCloud 主机"
description: 本小节主要介绍如何查看虚拟机相关内容。
draft: false
weight: 2
---


## 场景描述

该任务主要用于指导用户连接并使用已创建成功的虚拟机。

## 前提条件

- 已获得**云平台**的登录账户和密码。

- 平台中已创建 ExpressCloud 主机。


## 浏览器 Web 连接

1. 登录管理平台。

2. 在顶部导航栏点击**资源** > **虚拟机**，进入ExpressCloud主机列表页面，点击指定虚拟主机的**连接远程桌面**图标，将自动打开远程连接 ( VNC ) 的会话窗口。

   ![link_virtual_1](../../../_images/link_virtual_1.png)

3. 输入在创建主机时已设置的用户名和密码，登录即可。

   > **注意：**
   >
   > 若当前主机不接受现有密码，用户可先关闭主机，参考[重置密码](/resource/virtual/expresscloud/manage_virtual#重置密码)相关内容，修改主机密码。

   ![link_virtual_2](../../../_images/link_virtual_2.png)

## 连接 Linux 系统虚拟主机

### 使用用户名密码登录

除了通过 VNC 连接外，用户也可以通过第三方软件连接至虚拟主机，常见的软件有 PuTTY 或 Xshell。

以使用 Putty 软件为例，操作步骤如下。

1. 在 `Session` 页面输入需访问的虚拟机的 IP 地址，点击**Open**。

   <img src="../../../_images/link_virtual_3.png" style="zoom:60%;" />

2. 按照提示输入用户名和密码，按 `Enter`键，即可登录。


### 使用 SSH 密钥登录

> **说明：**
>
> 相对于用户名密码方式，密钥方式拥有更强的安全性，也可以很大程度阻止暴力破解的发生。目前常用的密钥都是非对称性的加密方式，主机内置公钥，而用户则拥有私钥。由于采用非对称加密，入侵者试图通过公钥去破解私钥难度会远远超出密码的破解。


1. 确保 Linux 虚拟机和本地终端设备在同一内网环境中。

2. 在顶部导航栏点击**资源** > **虚拟机**，进入ExpressCloud主机列表页面。

   ![link_virtual_3_1](../../../_images/link_virtual_3_1.png)

3. 点击待连接的虚拟机所在行右侧的更多操作<img src="../../../_images/more_operation.png" style="zoom:50%;" />，点击**SSH 密钥**，选择**绑定 SSH 密钥**，将本地设备的公钥绑定至当前虚拟主机上。

   > **说明：**
   >
   > 将本地设备的公钥添加至云平台内进行管理，可参考[创建 SSH 密钥](/resource/ssh/create_ssh#使用已有公钥)使用已有公钥相关内容。

   ![link_virtual_3_2](../../../_images/link_virtual_3_2.png)

4. 本地设备公钥绑定虚拟主机成功后，在本地设备的 SSH Terminal 终端内输入如下命令，即可建立连接。
   ```
   # ssh root@xx.xx.xx.xx -p 22
   ```
   > **说明：**
   >
   > - xx.xx.xx.xx为虚拟主机的 IP 地址。
   > - 若为 ubuntu 主机，则默认登录用户为 ubuntu，即`ssh ubuntu@xx.xx.xx.xx -p 22`



## 连接 Windows 系统虚拟主机

从安全考虑，平台上的 Windows 主机默认关闭了远程登录，用户需通过浏览器 Web 方式登录到主机，并开启远程登录功能。

1. 进入虚拟机列表页面，打开**远程连接桌面**，连接 Windows Server。

   ![link_virtual_4](../../../_images/link_virtual_4.png)


2. 在 Web 登录页面，点击左上角 Ctrl-Alt-Del ，然后输入设置的密码。
   
   ![link_virtual_5](../../../_images/link_virtual_5.png)

3. 同意内部网络共享。登录后会弹出网络共享的界面，点击**是**，允许 VPC 内部的网络。

4. 在 Windows 主机中，点击下方**文件管理器**，点击 **此电脑** > **计算机** > **系统属性**,打开系统属性.
   
   ![link_virtual_6](../../../_images/link_virtual_6.png)

5. 在弹出的系统设置页面，点击远程桌面，打开**启用远程桌面**的按钮。

   ![link_virtual_7](../../../_images/link_virtual_7.png )


   


