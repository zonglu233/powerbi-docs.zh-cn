---
title: "如何通过 Power BI 问答将磁贴固定到仪表板"
description: "关于如何从“问答”问题框将磁贴固定到 Power BI 仪表板的文档"
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
ms.date: 01/17/2018
ms.author: mihart
ms.openlocfilehash: a3df29b478675eeeec876863299c0a33073fb381
ms.sourcegitcommit: d803e85bb0569f6b357ba0586f5702c20d27dac4
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/19/2018
---
# <a name="pin-a-tile-to-a-dashboard-from-qa"></a>从问答将磁贴固定到仪表板
## <a name="how-to-pin-a-tile-from-qa"></a>如何从“问答”中固定磁贴
问答是 Power BI 即席报表工具。 需要查找特定见解？ 对你的数据提问，然后就会收到以可视化效果形式显示的答案。

本操作说明将使用 Power BI 服务 (app.powerbi.com) 打开仪表板，使用自然语言提问以创建可视化效果，并将此可视化效果固定到仪表板。 Power BI Desktop 不支持仪表板。 若要了解如何将 Power BI 问答与其他 Power BI 工具和内容结合使用，请参阅 [Power BI 问答概述](power-bi-q-and-a.md)。 

要继续学习，请打开[零售分析示例仪表板](sample-retail-analysis.md)。


1. 打开至少具有一个从报表固定的磁贴的[仪表板](service-dashboards.md)。 在提问后，Power BI 会在将磁贴固定到该仪表板的所有数据集中查找答案。  若要了解详细信息，请参阅[获取数据](service-get-data.md)。
2. 在仪表板顶部的问题框中，键入你想要了解的有关数据的问题。  
   ![](media/service-dashboard-pin-tile-from-q-and-a/power-bi-question-box.png)
3. 例如，当你键入“last year sales by month and territory...”时，  
   ![](media/service-dashboard-pin-tile-from-q-and-a/power-bi-type-q-and-a.png)

   问题框将提供建议。
4. 若要将图表作为磁贴添加到仪表板，请选择画布右上方的大头针 ![](media/service-dashboard-pin-tile-from-q-and-a/pbi_pintile.png)。 如果仪表板已与自己共享，则无法固定任何可视化效果。

5. 将磁贴固定到现有仪表板或新仪表板。

   ![](media/service-dashboard-pin-tile-from-q-and-a/power-bi-pin-to-dashboard.png)

   * 现有仪表板：从下拉列表中选择仪表板的名称。 所做的选择仅限当前工作区中的这些仪表板。
   * 新仪表板：键入新仪表板的名称，它将被添加到当前工作区。

6. 选择“固定”。

   会显示一条成功消息（右上角附近），告知你可视化效果已作为磁贴添加到你的仪表板中。  

   ![](media/service-dashboard-pin-tile-from-q-and-a/power-bi-pin.png)
7. 选择“转到仪表板”以查看新磁贴。 随后，可以在仪表板上执行[重命名、重设大小、添加超链接、重新定位磁贴等操作](service-dashboard-edit-tile.md)。

   ![](media/service-dashboard-pin-tile-from-q-and-a/power-bi-pinned.png)

## <a name="considerations-and-troubleshooting"></a>注意事项和疑难解答
* 开始键入问题时，问答将立即从与当前仪表板关联的所有数据集搜索最佳答案。  “当前仪表板”是顶部导航栏中列出的仪表板。 例如，在属于“mihart”应用工作区的“零售分析示例”仪表板中提出此问题。

  ![](media/service-dashboard-pin-tile-from-q-and-a/power-bi-navbar.png)
* **问答如何知道要使用哪个数据集**？  Power BI 问答有权访问至少有一个可视化效果固定到相应仪表板的所有数据集。

* **看不到提问框**？ 请与 Power BI 管理员联系。 管理员可以禁用 Power BI 问答。


## <a name="next-steps"></a>后续步骤
[重命名、调整大小、添加超链接、重新定位磁贴等](service-dashboard-edit-tile.md)    
[在焦点模式下显示仪表板磁贴](service-focus-mode.md)     
[返回到 Power BI 中的问答](power-bi-q-and-a.md)  
更多问题？ [尝试参与 Power BI 社区](http://community.powerbi.com/)
