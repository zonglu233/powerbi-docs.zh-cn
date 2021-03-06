---
title: "安装 Power BI 报表服务器所要满足的硬件和软件要求"
description: "本文介绍了安装并运行 Power BI 报表服务器所要满足的最低硬件和软件要求。"
services: powerbi
documentationcenter: 
author: markingmyname
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
ms.date: 11/01/2017
ms.author: maghan
ms.openlocfilehash: 44a1af1553aaa28a5f4abab13bad1fafa040003a
ms.sourcegitcommit: 6e693f9caf98385a2c45890cd0fbf2403f0dbb8a
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/30/2018
---
# <a name="hardware-and-software-requirements-for-installing-power-bi-report-server"></a>安装 Power BI 报表服务器所要满足的硬件和软件要求
本文介绍了安装并运行 Power BI 报表服务器所要满足的最低硬件和软件要求。

## <a name="processor-memory-and-operating-system-requirements"></a>处理器、内存和操作系统要求
| 组件 | 要求 |
| --- | --- |
| .NET Framework |4.6<br><br>可以从[适用于 Windows 的 Microsoft.NET Framework 4.6（Web 安装程序）](http://support.microsoft.com/kb/3045560)手动安装 .NET Framework。<br/><br/> 有关 .NET Framework 4.6 的详细信息、建议和指南，请参阅[面向开发者的 .NET Framework 部署指南](http://msdn.microsoft.com/library/ee942965\(v=vs.110\).aspx)。<br/><br/>Windows 8.1 和 Windows Server 2012 R2 中必须有 [KB2919355](http://support.microsoft.com/kb/2919355)，才能安装 .NET Framework 4.6。 |
| 硬盘 |Power BI 报表服务器至少需要 1 GB 的可用硬盘空间。<br><br>托管报表服务器数据库的数据库服务器上必须有额外空间。 |
| 内存 |最小：1 GB<br/><br/> 建议：至少 4 GB |
| 处理器速度 |最小：x64 处理器：1.4 GHz<br/><br/> 建议：2.0 GHz 或更快 |
| 处理器类型 |x64 处理器：AMD Opteron、AMD Athlon 64、支持 Intel EM64T 的 Intel Xeon、支持 EM64T 的 Intel Pentium IV |
| 操作系统 |Windows Server 2016 Datacenter<br><br>Windows Server 2016 Standard<br><br>Windows Server 2012 R2 Datacenter<br><br>Windows Server 2012 R2 Standard<br><br>Windows Server 2012 R2 Essentials<br><br>Windows Server 2012 R2 Foundation<br><br>Windows Server 2012 Datacenter<br><br>Windows Server 2012 Standard<br><br>Windows Server 2012 Essentials<br><br>Windows Server 2012 Foundation<br><br>Windows 10 家庭版<br><br>Windows 10 专业版<br><br>Windows 10 企业版<br><br>Windows 8.1<br><br>Windows 8.1 专业版<br><br>Windows 8.1 企业版<br><br>Windows 8<br><br>Windows 8 专业版<br><br>Windows 8 企业版 |

> [!NOTE]
> 只支持在 x64 处理器上安装 Power BI 报表服务器。
> 
> 

## <a name="database-server-version-requirements"></a>数据库服务器版本要求
SQL Server 用于托管报表服务器数据库。 SQL Server 数据库引擎实例可以是本地或远程实例。 以下是可用于托管报表服务器数据的 SQL Server 数据库引擎受支持的版本：

* SQL Server 2017
* SQL Server 2016
* SQL Server 2014
* SQL Server 2012
* SQL Server 2008 R2
* SQL Server 2008

在远程计算机上创建报表服务器数据库时，需要将连接配置为使用域用户帐户或具有网络访问权限的服务帐户。 如果决定使用远程 SQL Server 实例，请仔细考虑报表服务器应使用哪些凭据来连接到 SQL Server 实例。 有关详细信息，请参阅[配置报表服务器数据库连接](https://docs.microsoft.com/sql/reporting-services/install-windows/configure-a-report-server-database-connection-ssrs-configuration-manager)。

## <a name="considerations"></a>注意事项
Power BI 报表服务器将安装默认值，以配置报表服务器正常运行所需的核心设置。 具体要求如下：

* 在安装完成之后且在配置报表服务器数据库之前，必须有 SQL Server 数据库引擎。 数据库引擎实例托管 Reporting Services 配置管理器将创建的报表服务器数据库。 实际的安装体验不需要有数据库引擎。
* 用于运行安装程序的用户帐户必须是本地管理员组的成员。
* 用于 Reporting Services 配置管理器的用户帐户必须有权在托管报表服务器数据库的数据库引擎实例上访问并创建数据库。
* 安装程序必须能够使用默认值来保留 URL，从而提供对报表服务器和 Web 门户的访问权限。 这些值为端口 80、强通配符以及格式为 ReportServer 和 Reports 的虚拟目录名称。

## <a name="read-only-domain-controller-rodc"></a>只读域控制器 (RODC)
 虽然报表服务器可以安装在包含只读域控制器 (RODC) 的环境中，但 Reporting Services 必须有权访问读/写域控制器，才能正常工作。 如果 Reporting Services 仅有权访问 RODC，那么你可能会在尝试管理服务时看到错误消息。

## <a name="power-bi-reports-and-analysis-services-live-connections"></a>Power BI 报表和 Analysis Services 实时连接
你可以使用针对表格或多维实例的实时连接。 Analysis Services 服务器必须满足正确的版本要求，才能正常工作。

| **服务器版本** | **所需的 SKU** |
| --- | --- |
| 2012 SP1 CU4 或更高版本 |商业智能和企业版 SKU |
| 2014 |商业智能和企业版 SKU |
| 2016 和更高版本 |标准 SKU 或更高版本 |

## <a name="next-steps"></a>后续步骤
[用户手册](user-handbook-overview.md)  
[管理员手册](admin-handbook-overview.md)  
[快速入门：安装 Power BI 报表服务器](quickstart-install-report-server.md)  
[安装报表生成器](https://docs.microsoft.com/sql/reporting-services/install-windows/install-report-builder)  
[下载 SQL Server Data Tools (SSDT)](http://go.microsoft.com/fwlink/?LinkID=616714)

更多问题？ [尝试咨询 Power BI 社区](https://community.powerbi.com/)

