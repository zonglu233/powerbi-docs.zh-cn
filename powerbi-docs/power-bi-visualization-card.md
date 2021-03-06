---
title: "卡片可视化对象（也称为大数字磁贴）"
description: "在 Power BI 中创建卡片可视化对象"
services: powerbi
documentationcenter: 
author: mihart
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
ms.date: 12/24/2017
ms.author: mihart
ms.openlocfilehash: 1136aae9af4481a1d55ca3d11ed300242aab187b
ms.sourcegitcommit: 74fbbca81a056dda19b3647ae058005aba5296f5
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/03/2018
---
# <a name="card-visualizations"></a>卡片可视化对象
有时在 Power BI 仪表板或报表中想要跟踪的最重要的信息就是一个数字，例如总销售额、同比市场份额或商机总数。 此类可视化对象称为“卡片”。 与几乎所有的本机 Power BI 可视化对象一样，可以使用报表编辑器或“问答”创建卡片。

![卡片可视化对象](media/power-bi-visualization-card/pbi_opptuntiescard.png)

## <a name="create-a-card-using-the-report-editor"></a>使用报表编辑器创建卡片
以下说明使用零售分析示例。 若要继续学习，请[下载](sample-datasets.md)适用于 Power BI 服务 (app.powerbi.com) 或 Power BI Desktop 的示例。   

1. 首先打开一个[空白报表页](power-bi-report-add-page.md)，然后选择“商店”\>“打开商店计数”字段。 如果使用的是 Power BI 服务，则需要在 [“编辑视图”](service-interact-with-a-report-in-editing-view.md) 中打开报表。

    Power BI 将创建一个包含一个数字的柱形图。

   ![](media/power-bi-visualization-card/pbi_rptnumbertilechart.png)
2. 在可视化效果窗格中，选择“卡片”图标。

   ![](media/power-bi-visualization-card/pbi_changechartcard.png)
6. 将鼠标悬停在某个卡片上，选择固定图标 ![](media/power-bi-visualization-card/pbi_pintile.png)，将可视化对象添加到仪表板。

   ![](media/power-bi-visualization-card/power-bi-pin-icon.png)
7. 将磁贴固定到现有仪表板或新仪表板。

   * 现有仪表板：从下拉列表中选择仪表板的名称。
   * 新仪表板：键入新仪表板的名称。
8. 选择**固定**。

   会显示一条成功消息（右上角附近），告知你可视化效果已作为磁贴添加到你的仪表板中。

   ![](media/power-bi-visualization-card/power-bi-pin-success-message.png)
9. 选择“转到仪表板”。 在此处可以对已固定的可视化效果进行[编辑和移动](service-dashboard-edit-tile.md)。


## <a name="create-a-card-from-the-qa-question-box"></a>通过“问答”问题框创建卡片
最简单的方法是使用“问答”问题框制作卡片。 Power BI 服务 (app.powerbi.com) 的仪表板或报表中提供了“问答”问题框。 以下步骤说明如何通过 Power BI 服务仪表板创建卡片。 若要在 Power BI Desktop 中使用“问答”创建卡片，请遵照适用于 Desktop 报表的“问答”预览功能的[这些说明](https://powerbi.microsoft.com/en-us/blog/power-bi-desktop-december-feature-summary/#QandA)。

1. 创建[仪表板](service-dashboards.md)和[获取数据](service-get-data.md)。 此示例使用[机会分析示例](sample-opportunity-analysis.md)。

1. 在仪表板顶部，在提问框中键入你想要了解的有关你的数据的问题。 

   ![](media/power-bi-visualization-card/power-bi-q-and-a-box.png)

>**提示**： 从 Power BI 服务中的报表，[编辑视图](service-reading-view-and-editing-view.md)，选择**提问**从顶部菜单栏中。 在 Power BI Desktop 报表中找到某个已打开的空间，然后双击打开问题框。

3. 例如，在问题框中键入“机会数”。

   ![](media/power-bi-visualization-card/power-bi-q-and-a.png)

   问题框中会提供建议和重述，最后显示总数。  
4. 选择右上角的固定图标 ![](media/power-bi-visualization-card/pbi_pintile.png)，将该卡片添加到仪表板。

   ![](media/power-bi-visualization-card/power-bi-pin.png)
5. 将卡片作为磁贴固定到现有仪表板或新仪表板。

   * 现有仪表板：从下拉列表中选择仪表板的名称。 你的选择仅限当前工作区中的这些仪表板。
   * 新仪表板：键入新仪表板的名称，它将被添加到当前工作区。
6. 选择“固定”。

   会显示一条成功消息（右上角附近），告知你可视化效果已作为磁贴添加到你的仪表板中。  

   ![](media/power-bi-visualization-card/power-bi-success.png)
7. 选择“转到仪表板”以查看新磁贴。 可在该仪表板上进行[重命名、调整大小、添加超链接、重新定位磁贴等操作](service-dashboard-edit-tile.md)。

   ![](media/power-bi-visualization-card/power-bi-pinned.png)

## <a name="considerations-and-troubleshooting"></a>注意事项和疑难解答
- 如果根本看不到问题框，请与系统管理员或租户管理员联系。    
- 如果使用的是 Desktop，而双击报表中的空白区域并未打开“问答”，则可能需要启用“问答”。  选择“文件”>“选项和设置”>“选项”>“预览功能”>“问答”，然后重启 Desktop。


## <a name="next-steps"></a>后续步骤
[Power BI 中的仪表板磁贴](service-dashboard-tiles.md)

[Power BI 中的仪表板](service-dashboards.md)

[Power BI - 基本概念](service-basic-concepts.md)

更多问题？ [尝试参与 Power BI 社区](http://community.powerbi.com/)
