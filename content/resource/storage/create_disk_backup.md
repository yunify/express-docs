---
title: "基于硬盘创建备份"
description: 本小节主要介绍如何查看硬盘详情。
draft: false
weight: 2
---

## 场景描述

该任务用于指导用户在指定硬盘的详情页面，针对当前硬盘创建备份。

## 操作步骤

### 创建备份

1. 登录管理平台。

2. 在顶部导航栏，选择**资源** > **存储** > **硬盘**，进入硬盘列表页面。

   ![create_disk_backup_1](../../_images/create_disk_backup_1.png)

3. 点击指定硬盘的名称，进入相应硬盘的详情页面。点击**备份**页签，进入备份页面，点击**新建全量备份链**。

   ![create_disk_backup_2](../../_images/create_disk_backup_2.png)


4. 在弹出的**创建全量备份**窗口中输入名称，点击**创建**即可。

   > **说明：**
   >
   > 新备份链将保存当前所选中资源的全部数据，由于数据量大，因此备份所需时间较长。建议在重要数据版本时使用此备份方式。

   ![create_disk_backup_3](../../_images/create_disk_backup_3.png)

5. 在备份的结构示意图中，点击<img src="../../_images/add_backup.png" style="zoom:50%;" />，创建增量备份，在弹出的**创建增量备份**的窗口中，输入名称并点击**创建**即可。

   > **注意：**
   >
   > 为了保证备份创建成功，正在创建备份时，不可修改实例状态，比如写入数据，停止或重启实例。

   ![create_disk_backup_4](../../_images/create_disk_backup_4.png)

### 管理备份

1. 点击备份所在行右侧的<img src="../../_images/more_operation.png" style="zoom:50%;" />，选择**修改**，在弹出的**修改属性**窗口中，可对当前备份的名称和相应描述进行修改。

   ![create_disk_backup_5](../../_images/create_disk_backup_5.png)

2. 点击备份所在行右侧的<img src="../../_images/more_operation.png" style="zoom:50%;" />，选择**共享备份**，在弹出的**共享备份**窗口输入用户名或用户 ID，可将当前备份共享给其他用户。

   > **说明：**
   >
   > 需为**用户管理**列表中已存在的用户，用户注册可参考用户管理相关内容.

   ![create_disk_backup_6](../../_images/create_disk_backup_6.png)

3. 点击备份所在行右侧的<img src="../../_images/more_operation.png" style="zoom:50%;" />，选择**创建硬盘**，在弹出的**创建硬盘**窗口输入名称，点击**创建**。

   ![create_disk_backup_7](../../_images/create_disk_backup_7.png)

4. 点击备份所在行右侧的<img src="../../_images/more_operation.png" style="zoom:50%;" />，选择**回滚**，在弹出的窗口中点击**回滚**即可。

   ![create_disk_backup_8](../../_images/create_disk_backup_8.png)

5. 点击备份所在行右侧的<img src="../../_images/more_operation.png" style="zoom:50%;" />，选择**删除**，在弹出的窗口中点击**删除**即可。
  
    ![create_disk_backup_9](../../_images/create_disk_backup_9.png)




