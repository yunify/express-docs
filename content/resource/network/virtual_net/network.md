---
title: "虚拟网卡"
description: 本小节主要对云平台内资源页面中的虚拟网卡进行介绍。
draft: false
weight: 1
---

## 功能描述

网卡（Nic）是一种虚拟网卡，可以分配到主机，一个主机最多可以绑定 64 张网卡（其中主网卡 1 张，从网卡 63 张），一个网络最多可以有 252 张网卡。

对于物理主机来说，网卡就是服务器的网络设备，用于接入以太网络，和其它计算机进行通信。网卡是基于虚拟化技术模拟的网卡设备，此设备是基于虚拟机所在的物理设备。可以将集群内的虚拟网络统一起来，进行再分配。用户无需关心具体的网卡在什么位置，有需要可直接申请、挂载至主机即可。

用户可在此虚拟网卡功能下创建和管理主机的虚拟网卡（包括主网卡和从网卡），虚拟网卡支持分配给虚拟机及绑定防火墙资源、添加标签等功能。


## 场景描述

该任务主要用于指导用户申请网卡，查看网卡和管理网卡。

## 前提条件

已获得**云平台**的登录账户和密码。

## 操作步骤

### 申请网卡

1. 登录管理平台。

2. 在顶部导航栏，选择**资源** > **网络** > **虚拟网卡**，进入 **虚拟网卡**列表页面。
   
   ![network_1](../../../_images/network_1.png)

3. 点击**申请网卡**，在弹出的申请网卡窗口中，输入**网卡名称**，设置**拷贝数量**并选择相应的**网络**，点击**申请**即可。

  > **注意：**
  > 
  > - 若所选的基础网络未开启 DHCP，则需要用户手动配置内网 IP 地址。
  > - 若所选的基础网络已开启 DHCP，则支持自动分配或手动配置内网 IP。
  > - 若平台内没有可选择的基础网络，可参考[创建 IP 池](/resource/network/ip#创建-ip-池)相关内容。

  ![network_2](../../../_images/network_2.png)

**参数说明**

 <table>
 <tr>
     <th style="width:20%">参数</th> 
     <th style="width:80%">详细说明</th>
  </tr>
  <tr>
     <td> 网卡名称 </td>
     <td> 用户自定义，便于用户浏览和搜索。</td>
  </tr>
  <tr>
     <td> 拷贝数量 </td>
     <td> 填写网卡的数量，可批量申请。</td>
  </tr> 
  <tr>
     <td> 网络</td>
     <td> 点击<b>选择基础网络</b>可选择其中一个 IP 组。</td>
  </tr>  
  <tr>
     <td> 内网 IP</td>
     <td> 选择基础网络后，可填写一个内网 IP，IP 段值范围在 2~253 之间。</td>
  </tr>  
  </table>


### 查看虚拟网卡

1. 登录管理平台。

2. 在顶部导航栏，选择**资源** > **网络** > **虚拟网卡**，进入 **虚拟网卡**列表页面。

3. 点击指定虚拟网卡的名称，进入指定网卡的详情页面。

    ![network_3](../../../_images/network_3.png)

**参数说明**

 <table>
 <tr>
     <th style="width:20%">参数</th> 
     <th style="width:80%">详细说明</th>
  </tr>
  <tr>
     <td> ID </td>
     <td>当前虚拟网卡的 ID，全平台唯一。</td>
  </tr>
  <tr>
     <td>所属用户</td>
     <td>当前虚拟网卡所属的用户的用户名。</td>
  </tr>
  <tr>
     <td>状态</td>
     <td>当前虚拟网卡的状态，包括使用中或可用两种状态。</td>
  </tr>
  <tr>
     <td>角色</td>
     <td>当前虚拟网卡的角色，主网卡或从网卡。</td>
  </tr>
  <tr>
     <td>虚拟机</td>
     <td>当前虚拟网卡所绑定的虚拟主机。</td>
  </tr>
  <tr>
     <td>IP 地址</td>
     <td>当前虚拟网卡所对应的 IP 地址。</td>
  </tr>
  <tr>
     <td>IP 池</td>
     <td>当前虚拟网卡的 IP 地址所属的 IP 池的 ID。</td>
  </tr>
  <tr>
     <td>安全组</td>
     <td>当前虚拟网卡所加入安全组 ID。</td>
  </tr>
  <tr>
     <td>标签</td>
     <td>当前虚拟网卡所绑定的标签。</td>
  </tr>
  <tr>
     <td>创建时间</td>
     <td>当前虚拟网卡创建的时间。</td>
  </tr>
  <tr>
     <td>更新时间</td>
     <td>当前虚拟网卡状态更新的时间。</td>
  </tr>
  <tr>
     <td>监控</td>
     <td>主要显示当前网卡的网络流量和包转发率的监控数据。支持查看实时、最近 6 小时、一天、两周、一个月的监控数据。 </td>
  </tr>
 </table>

### 修改属性

1. 登录管理平台，在顶部导航栏，选择**资源** > **网络** > **虚拟网卡**，进入 **虚拟网卡**列表页面。

2. 进入 **虚拟网卡**列表页面，点击待修改的虚拟网卡所在行右侧的更多操作<img src="../../../_images/more_operation.png" style="zoom:50%;" />，选择**修改**，在弹出的**修改属性**的窗口中输入虚拟网卡的新名称以及相关描述，点击**修改**即可。

    ![network_4](../../../_images/network_4.png)
   
 ### 绑定/解绑主机

1. 登录管理平台，在顶部导航栏，选择**资源** > **网络** > **虚拟网卡**，进入 **虚拟网卡**列表页面。

2. 点击待绑定至主机的虚拟网卡所在行右侧的更多操作<img src="../../../_images/more_operation.png" style="zoom:50%;" />，选择**分配给主机**，在弹出的**选择主机**的窗口中选择相应的主机，点击**确定**即可。

    ![network_5](../../../_images/network_5.png)

3. 点击待解绑的虚拟网卡所在行右侧的更多操作<img src="../../../_images/more_operation.png" style="zoom:50%;" />，选择**解绑主机**，在弹出的**解绑网卡**的窗口中，点击**解绑**即可。

    ![network_6](../../../_images/network_6.png)


### 修改网卡 IP

1. 登录管理平台，在顶部导航栏，选择**资源** > **网络** > **虚拟网卡**，进入 **虚拟网卡**列表页面。


2. 点击虚拟网卡所在行右侧的更多操作<img src="../../../_images/more_operation.png" style="zoom:50%;" />，选择**修改 IP**，在弹出的**修改网卡{网卡 ID}的内网 IP**的窗口中输入新的 IP 地址，点击**修改**即可。

   > **注意：**
   > 
   > - 仅`可用`状态的虚拟网卡支持修改 IP 地址。
   > - 若虚拟网看状态为使用中，则需将其需从虚拟主机上解绑，可参考[解绑主机](#绑定解绑主机)相关内容。

   ![network_7](../../../_images/network_7.png)

### 绑定/解绑标签

1. 登录管理平台，在顶部导航栏，选择**资源** > **网络** > **虚拟网卡**，进入 **虚拟网卡**列表页面。


2. 点击虚拟网卡所在行右侧的更多操作<img src="../../../_images/more_operation.png" style="zoom:50%;" />，选择**标签**，点击**绑定**，在弹出的**绑定标签**的窗口中，选择待绑定至当前虚拟网卡的标签，点击**绑定**即可。

   > **说明：**
   >
   > - 若当前平台内没有可用的标签，可参考[创建标签](/ops_tool/label/create_label)相关内容。
   > - 可绑定单个或多个标签。

   ![network_8](../../../_images/network_8.png)

3. 点击虚拟网卡所在行右侧的更多操作<img src="../../../_images/more_operation.png" style="zoom:50%;" />，选择 **标签**，点击**解绑**，在弹出的**解绑标签**窗口中，删除待解绑的标签，点击**确定**即可。

   ![network_9](../../../_images/network_9.png)

### 删除虚拟网卡

1. 登录管理平台，在顶部导航栏，选择**资源** > **网络** > **虚拟网卡**，进入 **虚拟网卡**列表页面。


2. 点击虚拟网卡所在行右侧的更多操作<img src="../../../_images/more_operation.png" style="zoom:50%;" />，选择**删除**，在弹出的**删除**的窗口中，点击**删除**即可。

   > **注意：**
   > 
   > - 仅**可用**状态的虚拟网卡支持删除。
   > - 若虚拟网看状态为使用中，则需将其需从虚拟主机上解绑，可参考[解绑主机](#绑定解绑主机)相关内容。

   ![network_10](../../../_images/network_10.png)



