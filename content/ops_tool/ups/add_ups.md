---
title: "添加 UPS 电源"
description: 本小节主要介绍如何提添加 UPS 电源。
draft: false
weight: 1
---

## 功能描述

当市电线路故障时，支持给集群持续性供电，并且当 UPS 电量降低到一定阙值时，支持虚拟机关机和集群关机。

## 场景描述

该任务主要用于指导用户在云平台的运维工具中添加 UPS 电源。

## 前提条件

- 已获得**云平台**的登录账户和密码。

- UPS 电源必须配置 SNMP 卡。

## 操作步骤

1. 登录管理平台。

2. 在顶部导航栏，选择**运维工具** > **UPS 电源**，进入 **UPS 电源**列表页面。

   ![add_ups_1](../../_images/add_ups_1.png)

3. 点击**添加**，在弹出的添加窗口中，输入 UPS 电源名称，设置各项目参数后，点击**添加**即可。

   ![add_ups_2](../../_images/add_ups_2.png)

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
    <td>IP </td>
    <td>	UPS 电源配置的 SNMP 卡 IP 地址。</td>
   </tr>
   <tr>
    <td> UPS 版本</td>
    <td>支持选择 1、2c 或 2。</td>
   </tr>
   <tr>
    <td>OID</td>
    <td> UPS 电源所配置的 SNMP 卡的对象标识符。</td>
   </tr>
   </table>

4. 返回 UPS 电源列表，新添加的 UPS 电源已显示在列。当前列表主要显示 UPS 名称、UPS 网络连通状态（正常、待机）、剩余电量、UPS IP、OID 库、关机策略信息。

   ![add_ups_3](../../_images/add_ups_3.png)



