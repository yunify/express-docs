---
title: "管理第三方服务器"
date: 2021-09-06T00:38:25+09:00
description: 本小节主要介绍如何进入用户管理页面查看当前平台内的本地用户。
draft: false
weight: 3
---

## 功能描述

云平台支持对通过第三方登录的用户进行修改和禁用操作。

## 场景描述

该任务用于指导用户在用户管理界面对当前平台内已存在的第三方服务器进行修改和禁用操作。

## 前提条件

已获得**云平台**的登录账户和密码，且平台内已创建相应的**第三方服务器**。


## 操作步骤

### 修改第三方服务器

1. 登录**管理平台**。

2. 在顶部导航栏，选择**用户管理** > **第三方登录**，进入第三方登录列表页面。

   > **说明：**
   >
   > 在**第三方登录**列表页面的搜索框中输入服务器名称，点击`Enter`，找到指定的第三方服务器。

   ![setting_third_user_1](../../_images/setting_third_user_1.png)

3. 点击待修改名称的本地用户所在行右侧的<img src="../../_images/more_operation.png" style="zoom:50%;" />，选择**修改**。

   ![setting_third_user_2](../../_images/setting_third_user_2.png)

4. 在弹出的**修改第三方服务器**的窗口中输入相应参数，点击**修改**即可。可修改的内容包括名称、类型、服务器地址/端口、基准、管理员账户/密码。

   ![setting_third_user_3](../../_images/setting_third_user_3.png)

 ### 禁用/启用服务器

 #### 禁用服务器

1. 登录**管理平台**。

2. 在顶部导航栏，选择**用户管理** > **第三方登录**，进入第三方登录列表页面。 点击待禁用服务器所在行右侧的<img src="../../_images/more_operation.png" style="zoom:50%;" />，选择**禁用服务器**。

   ![setting_third_user_4](../../_images/setting_third_user_4.png)

3. 在弹出的**禁用**的窗口中，点击**禁用**即可。

   > **注意:**
   >
   > 被禁用的第三方服务器下关联的所有账户将无法登录当前平台。

   ![setting_third_user_5](../../_images/setting_third_user_5.png)

4. 返回第三方登录列表，此时弹出**当前服务器被禁用成功**的提示符，且该服务器的状态变为**已禁用**。

   ![setting_third_user_6](../../_images/setting_third_user_6.png)


#### 启用服务器

1. 登录**管理平台**。

2. 在顶部导航栏，选择**用户管理** > **第三方登录**，进入第三方登录列表页面。 点击待恢复的服务器所在行右侧的<img src="../../_images/more_operation.png" style="zoom:50%;" />，选择**启用服务器**。

   ![setting_third_user_7](../../_images/setting_third_user_7.png)

3. 返回第三方登录列表，此时弹出**当前服务器已被恢复**的提示符，此时该服务器状态变为**活跃**。

   ![setting_third_user_8](../../_images/setting_third_user_8.png)


