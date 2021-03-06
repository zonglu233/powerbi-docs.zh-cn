---
title: "结合使用 Power BI 问答和实时连接"
description: "有关通过实时连接到 Analysis Services 数据和本地数据网关使用 Power BI 问答自然语言查询的文档。"
services: powerbi
documentationcenter: 
author: mihart
manager: kfile
backup: mihart
editor: 
tags: 
qualityfocus: no
qualitydate: 
ms.service: powerbi
ms.devlang: NA
ms.topic: article
ms.tgt_pltfrm: NA
ms.workload: powerbi
ms.date: 01/18/2018
ms.author: mihart
ms.openlocfilehash: 49e0b976fcee8c18edc14f80df2786e5ebf3fedc
ms.sourcegitcommit: d803e85bb0569f6b357ba0586f5702c20d27dac4
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/19/2018
---
# <a name="enable-qa-for-live-connections"></a>启用实时连接问答
## <a name="what-is-on-premises-data-gateway--what-is-a-live-connection"></a>什么是本地数据网关？  什么是实时连接？
可以将 Power BI 中的数据集导入到 Power BI，也可以创建与它们的实时连接。 实时连接数据集通常被称为“本地”。 使用[网关](service-gateway-onprem.md)管理实时连接并使用实时查询来回发送数据和查询。

## <a name="qa-for-on-premises-data-gateway-datasets"></a>关于本地数据网关数据集的问答
如果你想要使用通过网关访问的数据集中的问答，首先你需要启用它们。

启用后，Power BI 将创建数据源的索引，并将该数据的子集上传到 Power BI 以启用提问功能。 创建初始索引可能会需要几分钟时间，当数据更改时，Power BI 会自动维护并更新索引。 使用这些数据集的问答与使用发布到 Power BI 的数据方式是一样的。 这两种情况都支持问答体验的全套功能，包括同时使用数据源和 Cortana。

在 Power BI 中提问后，问答通过使用你的数据集索引确定要构建的最佳视觉对象和用于回答问题的报表工作表。 确定最佳可能答案之后，问答将使用 DirectQuery 通过网关填充图表和图形获取数据源中的实时数据。 这可确保 Power BI 问答的结果始终显示直接来自于基础数据源的最新数据。

由于 Power BI 问答使用你数据源中的文本和架构值来确定如何查询答案的基础模型，因此搜索特定的新的或已删除文本值（如询问与新添加的文本记录相关的客户名称）取决于用最新的值及时更新索引。 Power BI 在 60 分钟窗口切换时间内自动使文本和架构索引保持最新。

有关详细信息，请参阅：

* 什么是[本地数据网关](service-gateway-onprem.md)？
* [Power BI 问答简介](power-bi-q-and-a.md)

## <a name="enable-qa"></a>启用问答
设置数据网关后，请从 Power BI 连接数据。  使用本地数据创建仪表板，或使用本地数据上传 .pbix 文件。  可能已与你共享的仪表板、报表和数据集中已存在本地数据。

1. 在 Power BI 的右上角，选择齿轮图标 ![](media/service-q-and-a-direct-query/power-bi-cog.png)，然后选择**设置**。
   
   ![](media/service-q-and-a-direct-query/powerbi-settings.png)
2. 选择**数据集**，然后选择要为其启用问答的数据集。
   
   ![](media/service-q-and-a-direct-query/power-bi-q-and-a-settings.png)
3. 展开**问答和 Cortana**，选择**启用此数据集的问答**复选框，然后选择**应用**。
   
    ![](media/service-q-and-a-direct-query/power-bi-q-and-a-directquery.png)

## <a name="what-data-is-cached-and-how-is-privacy-protected"></a>缓存哪些数据以及如何保护隐私？
当启用本地数据的问答时，数据的其中一个子集将缓存到服务中。 这是用来保证问答具有良好的性能。 Power BI 可以从缓存中排除长于 24 个字符的值。 当你通过取消选中**启用此数据集的问答**，或当你删除你的数据集时，缓存将在几小时内删除。

## <a name="considerations-and-troubleshooting"></a>注意事项和疑难解答
在此功能的预览版阶段，存在以下限制：

* 最初此功能只可用于 SQL Server 2016 Analysis Services 表格数据源。 此功能非常适合用于处理表格格式数据。 某些功能可用于多维数据源，但多维数据源尚不支持完整的问答体验。 今后将逐渐推出本地数据网关支持的其他数据源。
* 在最初的公共预览版中，并不完全支持 SQL Server Analysis Services 中定义的行级别安全性。 在问答中提问时，输入时“自动完成”的问题可以显示用户不能访问的字符串值。 但是，由于考虑对在模型中定义的 RLS 使用报表和图表视觉对象，因此不能公开任何基础数值数据。 将在接下来的更新中发布选项以控制此行为。
* 仅在使用本地数据网关时支持实时连接。 因此，这不能与个人网关一起使用。

## <a name="next-steps"></a>后续步骤
[本地数据网关](service-gateway-onprem.md)  
[管理数据源 - Analysis Services](service-gateway-enterprise-manage-ssas.md)  
[Power BI - 基本概念](service-basic-concepts.md)  
[Power BI 问答概述](power-bi-q-and-a.md)  

更多问题？ [尝试咨询 Power BI 社区](http://community.powerbi.com/)

