---
title: "连接 Vmware 主机"
description: 本小节主要介绍如何链接相应的 Vmware 主机。
draft: false
weight: 1
---

## 功能描述

该功能实现对现有 Vmware 资源进行纳管，实现在云平台内对所有虚拟主机进行管理。


## 场景描述

该任务用于指导用户创建云链接对已有的 Vmware 资源进行纳管。

## 前提条件

- 云平台已安装 Vmware 纳管组件。

- 已获得云平台的登录账户和密码。


## 操作步骤

1. 登录管理平台。

2. 在顶部导航栏，选择**资源** > **虚拟机**，点击**Vmware 主机**页签，进入 Vmware 主机页面。

   ![create_vmware_1](../../../_images/create_vmware_1.png)

3. 点击**创建云链接**，在弹出的创建云链接窗口中，输入相应参数。

   ![create_vmware_2](../../../_images/create_vmware_2.png)

- **参数说明**
   
   <table>
   <tr>
   <th style="width:30%">参数</th>
   <th style="width:70%">详细说明</th>
   </tr>
   <tr>
    <td> 名称</td>
    <td> 用户自定义，便于搜索与浏览。</td>
   </tr>
   <tr>
    <td> vCenter 地址</td>
    <td> vCenter 的 IP 地址，根据实际情况进行填写。</td>
   </tr>
   <tr>
    <td> 端口</td>
    <td> 远端 Vmware 资源的端口号，根据实际情况进行填写。</td>
   </tr>
   <tr>
    <td> 账户</td>
    <td> 登录远端 Vmware 资源的账户，根据实际情况进行填写。</td>
   </tr>
   <tr>
    <td> 密码</td>
    <td> 登录远端 Vmware 资源的账户密码，根据实际情况进行填写。</td>
   </tr>
   <tr>
    <td> 同步时间设置</td>
    <td> 设置与远端 Vmware 资源同步的时间。</td>
   </tr>
   <tr>
    <td> 忽略书签发证</td>
    <td> 开启后，将会忽略签发证书。</td>
   </tr>
   <tr>
    <td> 协议</td>
    <td> 选择协议类型，目前支持</td>
   </tr>
   </table>

4. 参数配置完成后，点击**测试连接**，验证云连接是否可用。

   > **说明：**
   >
   > 云连接测试成功后，会提示有连接成功的提示标语。否则，提示连接失败。
   
   
5. 测试连接验证成功后，点击**创建**即可。

6. 云连接创建成功后，点击**同步主机**，远端 Vmware 主机将显示在云平台的虚拟机列表页面。

   ![create_vmware_3](../../../_images/create_vmware_3.png)

   
