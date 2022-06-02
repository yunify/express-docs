---
title: "创建安全组"
description: 本小节主要介绍创建安全组的基本流程。
draft: false
weight: 1
---

## 功能描述

安全组类似防火墙功能，通过策略配置对单台或多台云服务器的网络访问进行控制，极大地提高一个内部网络或主机的安全性，并过滤不安全的服务，从而降低内部网络或云服务器的风险。

## 场景描述

该任务主要用于指导用户在云平台内创建安全组。

## 前提条件

已获得**云平台**的登录账户和密码。

## 操作步骤

1. 登录云平台。

2. 在顶部导航栏，选择**资源** > **安全** ，进入安全列表页面。

   ![create_safety_1](../../_images/create_safety_1.png)

3. 点击**创建安全组**，在弹出的**创建安全组**的窗口中，输入**安全组名称**，点击**确定**。

   ![create_safety_2](../../_images/create_safety_2.png)

4. 在跳转至的**添加安全组规则**的界面，设置各项参数，点击**确定**即可。

   ![create_safety_3](../../_images/create_safety_3.png)

- **参数说明**
 <table>
 <tr>
     <th style="width:20%">参数</th> 
     <th style="width:80%">详细说明</th>
  </tr>
  <tr>
     <td> 规则名称 </td>
     <td> 用户自定义，便于用户浏览和搜索。</td>
  </tr>
  <tr>
     <td> 预设规则 </td>
     <td> 用户自行选择，支持 ping、ping6、ssh、http、https、ftp、remote、openvpn、pptp、l2tp、gre 以及 ipip。</td>
  </tr> 
  <tr>
     <td> 优先级</td>
     <td> 安全组规则的优先级决定规则应用至网络流量的顺序，数字越小优先级越高</td>
  </tr>  
  <tr>
     <td> 规则</td>
     <td> 
     <li>下行规则可控制 Internet 用户对服务器的访问规则（如仅向用户开放网站访问);</li>
     <li>上行规则可控制服务器可访问的 Internet 访问(如让服务器仅能访问微信 API)，从而全面的保护业务安全；</li>
     </td>
  </tr>  
  <tr>
     <td>协议 </td>
     <td>安全组支持多种协议设置，常用 TCP、 UDP</td>
  </tr>  
  <tr>
     <td>起始端口</td>
     <td>1~65525，可点击右侧标志，选择已创建的 IP /端口集合</td>
  </tr>  
  <tr>
     <td>结束端口</td>
     <td>1~65525，可点击右侧标志，选择已创建的 IP /端口集合</td>
  </tr> 
  <tr>
     <td>目标 IP</td>
     <td>不填写则表示所有 IP 地址，可点击右侧标志，选择已创建的 IP/端口集合。</td>
  </tr>   
  </table>

