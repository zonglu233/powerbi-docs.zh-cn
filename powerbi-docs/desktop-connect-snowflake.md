---
title: "在 Power BI Desktop 中连接到 Snowflake 计算仓库"
description: "轻松地连接到并使用 Power BI Desktop 中的 Snowflake 计算仓库"
services: powerbi
documentationcenter: 
author: davidiseminger
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
ms.date: 01/24/2018
ms.author: davidi
ms.openlocfilehash: f82c0c2f0fa07e083a06ef3265001e60d797a0ed
ms.sourcegitcommit: 7249ff35c73adc2d25f2e12bc0147afa1f31c232
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/25/2018
---
# <a name="connect-to-snowflake-in-power-bi-desktop"></a>在 Power BI Desktop 中连接到 Snowflake
在 Power BI Desktop 中，你可以连接到 **Snowflake** 计算仓库，并可如同使用 Power BI Desktop 中任何其他数据源一样使用基础数据。 

> [!NOTE]
> 此外，在使用 **Snowflake** 连接器的计算机上，你必须使用匹配 **Power BI Desktop** 32 位或 64 位安装的体系结构安装 **Snowflake ODBC 驱动程序**。 只需按照以下链接操作，并[下载合适的 Snowflake ODBC 驱动程序](http://go.microsoft.com/fwlink/?LinkID=823762)。
> 
> 

## <a name="connect-to-a-snowflake-computing-warehouse"></a>连接到 Snowflake 计算仓库
若要连接到 Snowflake 计算仓库，请从 Power BI Desktop 中的“开始”功能区选择“获取数据”。 选择左侧类别中的“数据库”，然后便会看到“Snowflake”。

![](media/desktop-connect-snowflake/connect_snowflake_2b.png)

在出现的 **Snowflake** 窗口中，将你的 Snowflake 计算仓库名称键入或粘贴到框中，然后选择“**确定**”。 请注意，可以选择将数据直接**导入**到 Power BI 中，或使用 **DirectQuery**。 可以了解有关[使用 DirectQuery](desktop-use-directquery.md) 的详细信息。

![](media/desktop-connect-snowflake/connect_snowflake_3.png)

出现提示时，输入你的用户名和密码。

![](media/desktop-connect-snowflake/connect_snowflake_4.png)

> [!NOTE]
> 一旦输入用户名和密码以连接特定 Snowflake 服务器，Power BI Desktop 在后续连接尝试中就会使用这些凭据。 可以通过“文件”>“选项和设置”>“数据源设置”来修改这些凭据。
> 
> 

连接成功后，将会出现“导航器”窗口，并显示服务器上可用的数据。你可以从这些数据中选择要在 **Power BI Desktop** 中导入和使用的一个或多个元素。

![](media/desktop-connect-snowflake/connect_snowflake_5.png)

你可以**加载**选定的表，该操作将把整个表格加载到 **Power BI Desktop**中，或者你也可以**编辑**查询，这将打开**查询编辑器**，以便筛选和优化要使用的数据集，然后将优化后的数据集加载到 **Power BI Desktop** 中。

## <a name="next-steps"></a>后续步骤
你可以使用 Power BI Desktop 连接到各种数据。 有关数据源的详细信息，请参阅下列资源：

* [Power BI Desktop 入门](desktop-getting-started.md)
* [Power BI Desktop 中的数据源](desktop-data-sources.md)
* [使用 Power BI Desktop 调整和合并数据](desktop-shape-and-combine-data.md)
* [通过 Power BI Desktop 连接到 Excel 工作簿](desktop-connect-excel.md)   
* [直接将数据输入到 Power BI Desktop 中](desktop-enter-data-directly-into-desktop.md)   

