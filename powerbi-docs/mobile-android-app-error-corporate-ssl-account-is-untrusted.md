---
title: "错误： "
corporate: 
ssl: 
certificate: 
is: 
untrusted": 
'-': 
power: 
bi": 
description: "在登录适用于 Power BI 的 Android 应用时，你可能会看到以下消息：“无法进行身份验证，因为你的企业 SSL 证书不受信任"
.": 
services: powerbi
documentationcenter: 
author: maggiesMSFT
manager: kfile
backup: 
editor: 
tags: 
qualityfocus: no
qualitydate: 
ms.service: powerbi
ms.devlang: NA
ms.topic: article
ms.tgt_pltfrm: NA
ms.workload: powerbi
ms.date: 10/13/2017
ms.author: maggies
ms.openlocfilehash: 4ef29c0cab96e21045f30805d7445aa34d37697a
ms.sourcegitcommit: 99cc3b9cb615c2957dde6ca908a51238f129cebb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/13/2017
---
# <a name="error-corporate-ssl-certificate-is-untrusted---power-bi"></a>错误：“企业 SSL 证书不受信任”- Power BI
在登录适用于 Microsoft Power BI 的 Android 移动应用时，你可能会看到以下消息：“无法进行身份验证，因为你的企业 SSL 证书不受此设备信任。 请联系你的公司 IT 管理员。” 

你需要做什么通常取决于你的 Android 设备上的操作系统，但有一些其他问题，可能会导致此错误。

## <a name="on-android-7-or-later"></a>在 Android 7 或更高版本上
查找名为 **Chrome** 的应用的更新，并安装该更新。

## <a name="on-android-6-and-earlier"></a>在 Android 6 及更早版本上
你的设备可能需要 System Webview 的更新的版本。 它可能已经安装在你的设备上，你可能只需单击“**更新**”。

如果 System Webview 未安装在你的设备上：

1. 在 Android 设备上，关闭 Power BI。
2. 打开 Google Play Store 并搜索由 Google Inc 推出的 **System Webview**
3. 安装此应用。
4. 重启 Power BI 应用，然后登录。

## <a name="time-zone-settings"></a>时区设置
你的设备上的时区设置可能有误。 

转到“**设置**” > “**系统**” > “**日期和时间**”以检查时区设置。

## <a name="custom-authentication-server"></a>自定义身份验证服务器
如果你使用的自定义身份验证服务器，则公司身份验证服务器中的 SSL 证书可能无效。 请联系你所在组织的 IT 管理人员寻求帮助。

## <a name="next-steps"></a>后续步骤
* 从 Android 应用商店[下载 Android 应用](http://go.microsoft.com/fwlink/?LinkID=544867)
* 是否有任何问题？ [尝试咨询 Power BI 社区](http://community.powerbi.com/)

