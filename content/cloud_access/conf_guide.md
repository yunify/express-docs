---
title: "公有云接入配置指南"
description: 本小节主要对公有云接入的功能和概念进行介绍。
draft: false
weight: 2
---

## 前提条件

在进行公有云接入配置之前，用户需满足如下要求：


- 用户需提前了解如何创建 VLAN。
- 本地网络具备连接外网的能力（internet网络）
- 需要预先在物理交换设备上划分三个或以上用于公有云接入业务需要使用的 VLAN，其中一个 VLAN 需要有外网访问能力，并在 **IP 池** 管理功能中，添加好相应信息（包括 IP 网段，VLAN-ID）。
- 需提前熟悉云端光格 SD-WAN 和 VPC 服务的使用方法，可参考 [光格 SD-WAN](https://docsv3.qingcloud.com/sd-wan/sdwan_new/intro/10_sdwan/) 和 [VPC](https://docsv3.qingcloud.com/network/vpc/intro/10_intro/)相关文档。

## 配置指南

### 网络拓扑图

![conf_guide_1](../_images/conf_guide_1.png)

此拓扑图中，在本地物理交换设备定义了三个VLAN：
- VLAN 1000 网段：172.31.46.0/24
- VLAN 2000 网段：139.198.255.33/25 (具备访问外网的能力) 
- VLAN 3000 网段：172.31.45.128/25 (网关IP：172.31.45.254)

### 步骤1：准备工作

1. 登录管理平台。

2. 在顶部导航栏，选择**公有云接入**，进入使用公有云接入服务的页面。

   ![conf_guide_2](../_images/conf_guide_2.png)

3. 点击**立即部署，一键上云**，弹出步骤引导界面，了解公有云接入服务的基本步骤。

   ![conf_guide_3](../_images/conf_guide_3.png)

### 步骤2：启动虚拟光盒

1. 在激活并配置云端 光格SD-WAN 服务页面，点击**启用虚拟光盒，获取设备序列号**启用本地光盒。

   ![conf_guide_4](../_images/conf_guide_4.png)

2. 在弹出的**启用虚拟光盒**的窗口中，点击**WAN 口**右侧的**选择**。

   ![conf_guide_5](../_images/conf_guide_5.png)

3. 选择本地交换机设备定义好的具备外网访问能力的 VLAN 为虚拟光盒的 **WAN 口**网络 IP，点击**确定**。

   ![conf_guide_6](../_images/conf_guide_6.png)

4. 在**启用虚拟光盒**的窗口中，点击 **LAN 口** 右侧的**选择**，选定 LAN 口网络 IP，点击**确定**。

   ![conf_guide_7](../_images/conf_guide_7.png)

5. 启用虚拟光盒以后，平台会自动生成相应的设备序列号。

   > **说明：**
   >
   > 记录当前生成的**设备序列号**，已备后续使用。

   ![conf_guide_8](../_images/conf_guide_8.png)

### 步骤3：激活虚拟光盒

1. 登录 [QingCloud WEB](https://console.qingcloud.com/) 平台。

2. 点击**工单** > **创建工单** > **SD-WAN** > **光盒**，提交工单并提供激活公有云接入服务生成的虚拟光盒序列号。

   ![conf_guide_9](../_images/conf_guide_9.png)


### 步骤4：配置路由通信

1. 待光盒激活成功后，在公有云控制管理平台内，选择**产品与服务** > **SD-WAN（新版）** > **SD-WAN（新版）**  ，进入 SD-WAN 页面。

   ![conf_guide_10](../_images/conf_guide_10.png)

2. 点击**创建连接云网**，在弹出的**创建连接云网**的界面中，输入云网名称和相应的描述，点击**创建连接云网**。

   ![conf_guide_11](../_images/conf_guide_11.png)


3. 点击左侧导航栏中的**接入点**，进入接入点页面，选择**硬件光盒配置**页签，点击**创建接入点**。

   ![conf_guide_12](../_images/conf_guide_12.png)

4. 在弹出的**创建接入点**页面内，配置接入点的**基本信息**和**购买信息**，点击**立即创建**即可。

   ![conf_guide_13](../_images/conf_guide_13.png)

- **参数说明**

   <table>
   <tr>
   <th style="width:15%">配置项</th>
   <th style="width:15%">参数</th>
   <th style="width:70%">详细说明</th>
   </tr>
   <tr>
   <td rowspan="5">基本信息</td>
    <td> 接入点名称</td>
    <td> 用户自定义，便于搜索与浏览。</td>
   </tr>
   <tr>
    <td>接入点类型</td>
    <td>需选择光盒 2 号。</td>
   </tr>
   <tr>
    <td>部署方式</td>
    <td>	双机部署方式，默认支持主备设备高可用方式运行。</td>
   </tr>
   <tr>
    <td>关联连接云网</td>
    <td>	选择关联的连接云网，若您没有创建连接云网，系统将自动为用户创建默认连接云网。</td>
   </tr>
   <tr>
   <td>高级设置</td>
   <td>
    需勾选 LAN 配置
    <li>网段：设置 VCPE 的私有 IP 地址段。</li>
    <li>网关：网关 IP 不是 VCPE 所在虚拟机网卡地址，是 HA 状态下虚 IP 地址，不能和 VCPE 所在虚拟机的 IP 地址一致。</li>
    <li>DHCP 服务：勾选后，开启自动分配 IP 网络地址协议。</li>
    <li>DHCP 起始地址：自动分配的 IP 的起始地址。</li>
    <li>DHCP 结束地址：自动分配的 IP 的结束地址。</li>
   </td>
   </tr> 
   <tr>
   <td rowspan="2">购买信息</td>
    <td> 计费方式</td>
    <td> 目前支持按需计费。</td>
   </tr>
   <tr>
    <td> 带宽上限</td>
    <td>支持设置的带宽范围为 1 Mbps ～ 100 Mbps。</td>
   </tr>
   </table>



5. 光盒激活成功后，返回本地环境，点击**已在云端配置成功，下一步**。

   ![conf_guide_14](../_images/conf_guide_14.png)

6. 添加本地路由转发，选择本地需要与云端互通的本地路由，本指南选择了 VLAN1000 做为与云端互通的本地网络。
    
    > **注意：**
    >
    > 本指南划分了 3 个 VLAN 用作示例，本地与云端互通的网络需要排除 WAN 口 和 LAN 口 使用的 VLAN 2000 和 VLAN 3000。本指南选择了 VLAN1000 做为与云端互通的本地网络 ，配置成功后 VLAN1000 下的所创建的虚拟主机均与云端互通。

   ![conf_guide_15](../_images/conf_guide_15.png)


7. 填写目标网络，目标网络填写虚拟光盒 LAN 口所在 VLAN3000（本指南）的网关地址：172.31.45.254。

    ![conf_guide_16](../_images/conf_guide_16.png)


8. 在**配置本地与云端通信路由**页面，点击**光格 SD-WAN 网关接入点** > **配置参照表**，查看配置参照表，点击**确定**。

   ![conf_guide_17](../_images/conf_guide_17.png)

9. 登录 [QingCloud WEB](https://console.qingcloud.com/) 平台，进入 SD-WAN **接入点**列表页面。

   ![conf_guide_18](../_images/conf_guide_18.png)

10. 点击接入点的名称/ ID，进入当前接入点的详情页面，选择**网关配置**。

   ![conf_guide_19](../_images/conf_guide_19.png)

11. 点击端口右侧的`修改`，在弹出的**修改网关配置**的窗口中，将虚拟光盒 LAN 配置内网段 & 网关 IP 更改为与上述**配置参照表**内提供的一致。

   > **注意：**
   >
   >  修改完成后，返回接入点详情页面，点击**应用修改**，使得修改生效。

   ![conf_guide_20](../_images/conf_guide_20.png)

12. 在当前接入点的详情页面，选择**网络管理 **页签，点击**静态路由** > **添加静态路由**。

   ![conf_guide_21](../_images/conf_guide_21.png)

13. 在弹出的**添加静态路由**窗口中，添加光盒的静态路由，路由信息跟上述**配置参照表**内提供的一致即可。

    > **注意：**
    >
    >  添加完成后，需点击**应用修改**，使之生效。
   
    ![conf_guide_22](../_images/conf_guide_22.png)



14. 配置路由通信完成后，返回本地环境，点击**配置成功，下一步**

### 步骤5：连接测试

1. 在本地环境的**现在测试您的业务是否连接成功**页面，添加本地主机以及云端主机 IP 地址。

    ![conf_guide_23](../_images/conf_guide_23.png)

2. 点击**开始检测**，耐心等待检测完成。

    ![conf_guide_24](../_images/conf_guide_24.png)

3. 待本地业务与云端业务连接成功之后，点击**完成部署**即可。

    ![conf_guide_25](../_images/conf_guide_25.png)
    ![conf_guide_26](../_images/conf_guide_26.png)  
