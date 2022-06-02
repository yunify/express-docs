---
title: "管理 ExpressCloud 主机"
description: 本小节主要介绍如何对ExpressCloud 主机以及已纳管的 Vmware 主机进行管理。
draft: false
weight: 5
---

## 场景描述

该任务主要用于指导用户对已创建成功的 ExpressCloud 主机进行管理

## 前提条件

- 已获得**云平台**的登录账户和密码。

- 平台中已存在 **ExpressCloud 主机**。

## 操作步骤

### 修改主机

1. 登录管理平台。

2. 在顶部导航栏，选择**资源** > **虚拟机**，点击 **ExpressCloud 主机**，进入 ExpressCloud 主机列表页面。


3. 点击主机所在行右侧的更多操作<img src="../../../_images/more_operation.png" style="zoom:50%;" />，选择**修改**，在弹出的**修改属性**的窗口中输入主机的新名称以及相关描述，点击**修改**即可。

   ![manage_virtual_1](../../../_images/manage_virtual_1.png)

### 关闭主机

1. 在顶部导航栏，选择**资源** > **虚拟机**，点击 **ExpressCloud 主机**，进入 ExpressCloud 主机列表页面。


2. 点击主机所在行右侧的更多操作<img src="../../../_images/more_operation.png" style="zoom:50%;" />，选择**关闭**，在弹出的**关机**的窗口中，点击**关机**即可。

   > **注意：**
   >
   > 强制关机可能会导致丢失您未保存的数据，请谨慎操作！

   ![manage_virtual_2](../../../_images/manage_virtual_2.png)

### 启动/重启主机

1. 在顶部导航栏，选择**资源** > **虚拟机**，点击 **ExpressCloud 主机**，进入 ExpressCloud 主机列表页面。


2. 点击已关机的主机所在行右侧的更多操作<img src="../../../_images/more_operation.png" style="zoom:50%;" />，选择**启动**，在弹出的**启动**的窗口中，点击**启动**即可。

   ![manage_virtual_3](../../../_images/manage_virtual_3.png)


3. 点击主机所在行右侧的更多操作<img src="../../../_images/more_operation.png" style="zoom:50%;" />，选择**重启**，在弹出的**重启**的窗口中，点击**重启**即可。

   ![manage_virtual_4](../../../_images/manage_virtual_4.png)

### 迁移虚拟机

1. 在顶部导航栏，选择**资源** > **虚拟机**，点击 **ExpressCloud 主机**，进入 ExpressCloud 主机列表页面。


2. 点击主机所在行右侧的更多操作<img src="../../../_images/more_operation.png" style="zoom:50%;" />，选择**迁移虚拟机**。

- **方式一：** 手动指定计算节点


3. 在弹出的**迁移虚拟机**的窗口中，选择**手动指定计算节点**。

   ![manage_virtual_5](../../../_images/manage_virtual_5.png)

4. 在**迁移虚拟机**的窗口中，点击**选择**，选定当前虚拟机待迁移至的目标计算节点，并点击**确定**。

   ![manage_virtual_6](../../../_images/manage_virtual_6.png)

5. 返回迁移虚拟机界面，点击**迁移**即可。

   ![manage_virtual_7](../../../_images/manage_virtual_7.png)


- **方式二：** 系统指定计算节点

   系统根据各计算节点上资源使用情况，自动将相应的虚拟机迁移至资源充足的计算节点上。

3. 在弹出的**迁移虚拟机**的窗口中，选择**系统指定计算节点**，点击**迁移**即可。

   ![manage_virtual_8](../../../_images/manage_virtual_8.png)


### 制作成镜像

1. 在顶部导航栏，选择**资源** > **虚拟机**，点击 **ExpressCloud 主机**，进入 ExpressCloud 主机列表页面。


2. 点击主机所在行右侧的更多操作<img src="../../../_images/more_operation.png" style="zoom:50%;" />，选择**制作镜像**，在弹出的**制作镜像**窗口中，输入镜像名称，点击**确定**即可。

   ![manage_virtual_32](../../../_images/manage_virtual_32.png)

3. 镜像创建成功后，在顶部导航栏，选择**资源** > **镜像**，点击**自有**，进入自有镜像列表，基于虚拟机创建的镜像已显示在列。

   ![manage_virtual_33](../../../_images/manage_virtual_33.png)
   
### 加入/离开安置策略组

1. 在顶部导航栏，选择**资源** > **虚拟机**，点击 **ExpressCloud 主机**，进入 ExpressCloud 主机列表页面。


2. 点击主机所在行右侧的更多操作<img src="../../../_images/more_operation.png" style="zoom:50%;" />，选择**安置策略组**，点击**加入**，在弹出的**选择要加入的安置策略组**窗口中，指定安置策略组，点击**确定**即可。

   > **注意：**
   >
   > 若平台内没有可用的安置策略组，可参考[创建安置策略组]()相关内容。

   ![manage_virtual_9](../../../_images/manage_virtual_9.png)

3. 点击已加入安置策略组的主机所在行右侧的更多操作<img src="../../../_images/more_operation.png" style="zoom:50%;" />，选择**安置策略组**，点击**离开**，在弹出的**提示**窗口中，点击**离开**即可。

   ![manage_virtual_10](../../../_images/manage_virtual_10.png)


### 修改最大配置

1. 在顶部导航栏，选择**资源** > **虚拟机**，点击 **ExpressCloud 主机**，进入 ExpressCloud 主机列表页面。


2. 关闭正在运行中的虚拟机，详细操作可参考[关闭主机](#关闭主机)相关内容。

3. 点击主机所在行右侧的更多操作<img src="../../../_images/more_operation.png" style="zoom:50%;" />，选择**修改最大配置**，在弹出的**修改最大配置**窗口中，重置当前虚拟主机的**最大 CPU**和**最大内存**，点击**修改**即可。

   ![manage_virtual_11](../../../_images/manage_virtual_11.png)

### 更改配置

1. 在顶部导航栏，选择**资源** > **虚拟机**，点击 **ExpressCloud 主机**，进入 ExpressCloud 主机列表页面。

- **在线更改配置**

2. 点击主机所在行右侧的更多操作<img src="../../../_images/more_operation.png" style="zoom:50%;" />，选择**更改配置**，点击**在线更改配置**，在弹出的**在线更改虚拟机配置**的窗口中，重新选择 **CPU** 和**内存**值，点击**更改配置**即可。

   > **注意：**
   >
   > 若无有效可升级配置，可进入修改操作设置虚拟机的最大可更改配置，详细可参考[修改最大配置](#修改最大配置)相关内容。


   ![manage_virtual_12](../../../_images/manage_virtual_12.png)

- **关机更改配置**

3. 点击已关闭主机所在行右侧的更多操作<img src="../../../_images/more_operation.png" style="zoom:50%;" />，选择**更改配置**，点击**关机更改配置**，在弹出的**更改主机配置**的窗口中，重新设置各参数，并点击**更改配置**即可。

   > **说明：**
   >
   > 支持修改 CPU 核数、CPU 拓扑结构、内存以及系统盘容量。

   ![manage_virtual_13](../../../_images/manage_virtual_13.png)

### 克隆主机

1. 在顶部导航栏，选择**资源** > **虚拟机**，点击 **ExpressCloud 主机**，进入 ExpressCloud 主机列表页面。


2. 点击主机所在行右侧的更多操作<img src="../../../_images/more_operation.png" style="zoom:50%;" />，选择**克隆主机**，在弹出的**克隆主机**窗口中，点击**克隆**即可。

   ![manage_virtual_14](../../../_images/manage_virtual_14.png)

### 加入/离开网络

1. 在顶部导航栏，选择**资源** > **虚拟机**，点击 **ExpressCloud 主机**，进入 ExpressCloud 主机列表页面。

2. 点击主机所在行右侧的更多操作<img src="../../../_images/more_operation.png" style="zoom:50%;" />，选择**网络**，点击**加入网络**，在弹出的**加入网络**窗口中，选择待加入的网络，点击**确定**即可。

   ![manage_virtual_15](../../../_images/manage_virtual_15.png)

3. 若当前虚拟主机已加入其他网络，系统会弹出**切换网络**窗口，用户可根据需要选择**切换网络**来替换当前主机所在网络或**直接添加**其它基础网络。

   ![manage_virtual_16](../../../_images/manage_virtual_16.png)

4. 点击主机所在行右侧的更多操作<img src="../../../_images/more_operation.png" style="zoom:50%;" />，选择**网络**，点击**离开网络**，在弹出的**选择要从主机{主机 ID}离开的网络**窗口中，选择当前虚拟主机待离开的基础网络，点击**确定**即可。

   ![manage_virtual_17](../../../_images/manage_virtual_17.png)

### 挂载/卸载硬盘

1. 在顶部导航栏，选择**资源** > **虚拟机**，点击 **ExpressCloud 主机**，进入 ExpressCloud 主机列表页面。

2. 点击主机所在行右侧的更多操作<img src="../../../_images/more_operation.png" style="zoom:50%;" />，选择**硬盘**，点击**挂载硬盘**，在弹出的**选择硬盘**窗口中，选择待挂载至当前主机的硬盘，点击**确定**即可。

   > **说明：**
   >
   > - 可选择单个或多个硬盘进行挂载。
   > - 若平台内无可用的硬盘，可参考[创建硬盘](/resource/storage/create_disk)相关内容进行创建。

   ![manage_virtual_18](../../../_images/manage_virtual_18.png)

3. 点击主机所在行右侧的更多操作<img src="../../../_images/more_operation.png" style="zoom:50%;" />，选择**硬盘**，点击**卸载硬盘**，在弹出的**选择需要从主机上卸载的硬盘**窗口中，选择待卸载的硬盘，点击**确定**即可。

   ![manage_virtual_19](../../../_images/manage_virtual_19.png)

### 绑定/解绑 SSH 密钥

1. 在顶部导航栏，选择**资源** > **虚拟机**，点击 **ExpressCloud 主机**，进入 ExpressCloud 主机列表页面。

2. 点击主机所在行右侧的更多操作<img src="../../../_images/more_operation.png" style="zoom:50%;" />，选择 **SSH 密钥**，点击**绑定 SSH 密钥**，在弹出的**绑定 SSH 密钥**窗口中，选择待绑定至当前主机的 SSH 密钥，点击**确定**即可。

   > **说明：**
   >
   > 可选择单个或多个 SSH 密钥进行绑定。
   > 若当前平台内没有可用的 SSH 密钥，可参考[创建 SSH 密钥](/resource/ssh/create_ssh)相关内容。

   ![manage_virtual_20](../../../_images/manage_virtual_20.png)

3. 点击主机所在行右侧的更多操作<img src="../../../_images/more_operation.png" style="zoom:50%;" />，选择 **SSH 密钥**，点击**解绑 SSH 密钥**，在弹出的**选择需要从主机上解绑的 SSH 密钥**窗口中，选择待解绑的 SSH 密钥，点击**确定**即可。

   ![manage_virtual_21](../../../_images/manage_virtual_21.png)


### 加入/离开安全组

1. 在顶部导航栏，选择**资源** > **虚拟机**，点击 **ExpressCloud 主机**，进入 ExpressCloud 主机列表页面。

2. 点击主机所在行右侧的更多操作<img src="../../../_images/more_operation.png" style="zoom:50%;" />，选择**安全组**，点击**加入安全组**，在弹出的**选择安全组规则**窗口中，选择待加入的安全组，点击**确定**即可。

   > **说明：**
   >
   > 若当前平台内没有可用的 安全组，可参考[创建安全组规则](/resource/safety/create_safety)相关内容。

   ![manage_virtual_22](../../../_images/manage_virtual_22.png)


4. 点击主机所在行右侧的更多操作<img src="../../../_images/more_operation.png" style="zoom:50%;" />，选择**安全组**，点击**离开安全组**，在弹出的**移除安全组规则**窗口中，点击**确定**即可。

   ![manage_virtual_23](../../../_images/manage_virtual_23.png)


### 绑定/解绑告警策略

1. 在顶部导航栏，选择**资源** > **虚拟机**，点击 **ExpressCloud 主机**，进入 ExpressCloud 主机列表页面。

2. 点击主机所在行右侧的更多操作<img src="../../../_images/more_operation.png" style="zoom:50%;" />，选择 **告警策略**，点击**绑定告警策略**，在弹出的**选择告警策略**窗口中，选择待绑定至当前主机的告警策略，点击**确定**即可。

   > **说明：**
   >
   > 若当前平台内没有可用的告警策略，可参考[创建告警策略](/ops_tool/monitor/create_moitor)相关内容。

   ![manage_virtual_24](../../../_images/manage_virtual_24.png)

3. 点击主机所在行右侧的更多操作<img src="../../../_images/more_operation.png" style="zoom:50%;" />，选择 **告警策略**，点击**解绑告警策略**，在弹出的**选择需要从主机上解绑的告警策略**窗口中，选择待解绑的告警策略，点击**确定**即可。

   ![manage_virtual_25](../../../_images/manage_virtual_25.png)


### 重置系统

1. 在顶部导航栏，选择**资源** > **虚拟机**，点击 **ExpressCloud 主机**，进入 ExpressCloud 主机列表页面。


2. 点击主机所在行右侧的更多操作<img src="../../../_images/more_operation.png" style="zoom:50%;" />，选择**重置系统**，在弹出的**重置系统**的窗口中，重新选择**登录方式**，点击**重置**即可。

   > **注意：**
   >
   > - 重装后，主机的系统盘内所有数据将被清除，恢复到初始状态。
   > - 重置系统盘之前请先备份系统盘数据，以防您的数据丢失。
   > - 重置系统前，请先卸载当前主机上的挂载的硬盘资源。

   ![manage_virtual_26](../../../_images/manage_virtual_26.png)

### 重置密码

1. 在顶部导航栏，选择**资源** > **虚拟机**，点击 **ExpressCloud 主机**，进入 ExpressCloud 主机列表页面。

2. 关闭正在运行中的虚拟机，详细操作可参考[关闭主机](#关闭主机)相关内容。

3. 点击主机所在行右侧的更多操作<img src="../../../_images/more_operation.png" style="zoom:50%;" />，选择**重置密码**，在弹出的**重置密码**窗口中，输入新密码，点击**重置**即可。

   ![manage_virtual_27](../../../_images/manage_virtual_27.png)

### 重置 fstab

1. 在顶部导航栏，选择**资源** > **虚拟机**，点击 **ExpressCloud 主机**，进入 ExpressCloud 主机列表页面。


2. 关闭正在运行中的虚拟机，详细操作可参考[关闭主机](#关闭主机)相关内容。

3. 点击主机所在行右侧的更多操作<img src="../../../_images/more_operation.png" style="zoom:50%;" />，选择**重置 fstab**，在弹出的**重置 fstab** 窗口中，输入主机名，点击**重置**即可。

   > **说明：**
   >
   > - 重置 fstab 将会把当前的 fstab 文件恢复到创建虚机时的状态，以解决因为错误配置 fstab 文件导致的无法开机的问题。
   > - 虚机重启后，请正确配置 fstab 文件，修改完 fstab 请使用 “mount -a” 检查 fstab 文件是否正确。

   ![manage_virtual_28](../../../_images/manage_virtual_28.png)

### 绑定/解绑标签

1. 在顶部导航栏，选择**资源** > **虚拟机**，点击 **ExpressCloud 主机**，进入 ExpressCloud 主机列表页面。

2. 点击主机所在行右侧的更多操作<img src="../../../_images/more_operation.png" style="zoom:50%;" />，选择 **标签**，点击**绑定标签**，在弹出的**绑定标签**窗口中，选择待绑定至当前主机的标签，点击**绑定**即可。

   > **说明：**
   >
   > - 若当前平台内没有可用的标签，可参考[创建标签](/ops_tool/label/create_label)相关内容。
   > - 可绑定单个或多个标签。

   ![manage_virtual_29](../../../_images/manage_virtual_29.png)

3. 点击主机所在行右侧的更多操作<img src="../../../_images/more_operation.png" style="zoom:50%;" />，选择 **标签**，点击**解绑标签**，在弹出的**解绑标签**窗口中，删除待解绑的标签，点击**确定**即可。

   ![manage_virtual_30](../../../_images/manage_virtual_30.png)

### 删除主机

1. 在顶部导航栏，选择**资源** > **虚拟机**，点击 **ExpressCloud 主机**，进入 ExpressCloud 主机列表页面。

2. 点击主机所在行右侧的更多操作<img src="../../../_images/more_operation.png" style="zoom:50%;" />，选择 **删除**，在弹出的**删除**窗口中，点击**删除**即可。

   > **说明：**
   >
   > 删除后资源将在回收站保留 2 小时，请提前备份数据。

   ![manage_virtual_31](../../../_images/manage_virtual_31.png)



