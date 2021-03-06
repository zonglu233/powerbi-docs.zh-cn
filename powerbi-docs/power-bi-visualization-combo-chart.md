---
title: "教程 - 组合图"
description: "组合图教程，介绍了何时使用组合图，以及如何在 Power BI 服务和 Power BI Desktop 中生成组合图。"
services: powerbi
documentationcenter: 
author: mihart
manager: kfile
backup: 
editor: 
tags: 
featuredvideoid: lnv66cTZ5ho
qualityfocus: monitoring
qualitydate: 
ms.service: powerbi
ms.devlang: NA
ms.topic: article
ms.tgt_pltfrm: NA
ms.workload: powerbi
ms.date: 01/21/2018
ms.author: mihart
ms.openlocfilehash: 9ab6514e2ce5ba81b17f6862eae6c6c76fd9bf7b
ms.sourcegitcommit: c3be4de522874fd73fe6854333b379b85619b907
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/24/2018
---
# <a name="combo-chart-in-power--tutorial"></a>Power BI 中的组合图（教程）
在 Power BI 中，组合图是将折线图和柱形图合并在一起的单个可视化效果。 通过将两个图表合并为一个图表可以进行更快的数据比较。

组合图可以具有一个或两个 Y 轴。

## <a name="when-to-use-a-combo-chart"></a>何时使用组合图
组合图适用情况：

* 具有 X 轴相同的折线图和柱形图时。
* 比较具有不同值范围的多个度量值。
* 在一个可视化效果中说明两个度量值之间的关联。
* 检查一个度量值是否满足另一个度量值定义的目标
* 节省画布空间。

### <a name="prerequisites"></a>先决条件
Power BI 服务和 Power BI Desktop 均支持组合图。 本教程使用 Power BI 服务创建组合图。 若要跟着介绍一起操作，请打开 Power BI 服务，并连接到“零售分析示例”（[说明如下](#create)）。


## <a name="create-a-basic-single-axis-combo-chart"></a>创建基本的单轴组合图
观看如何使用销售和市场营销示例创建组合图。

<iframe width="560" height="315" src="https://www.youtube.com/embed/lnv66cTZ5ho?list=PL1N57mwBHtN0JFoKSR0n-tBkUJHeMP2cP" frameborder="0" allowfullscreen></iframe>

<a name="create"></a> 若要创建自己的组合图，请登录 Power BI 服务，再依次选择**“获取数据”\>示例“零售分析示例”>“连接”>“转至仪表板”\>**。

1. 从“零售分析示例”仪表板中，选择**总商店数**磁贴以打开“零售分析示例”报表。
2. 选择**编辑报表**在编辑视图中打开报表。
3. [添加新报表页](power-bi-report-add-page.md)。
4. 创建按月显示本年度销售额和毛利的组合图。

    a.  从“字段”窗格，选择**销售额** \> **本年度销售额**  >  **值**。

    b.  将**销售额** \> **本年度毛利**拖动到**值**框。

    c.  选择**时间** \> **会计月份**以将它添加到**轴**框。

    ![](media/power-bi-visualization-combo-chart/combotutorial1new.png)
5. 在可视化效果的右上角选择省略号 (...)，然后选择“**按会计月份排序**”。 若要执行升序或降序排序，可能需要选择它两次。

6. 将柱形图转换为组合图。 在选择了柱形图的情况下，从“可视化效果”窗格中选择“折线和簇状柱形图”。

    ![](media/power-bi-visualization-combo-chart/converttocombo_new2.png)
7. 从**字段**窗格，将**销售额** \> **去年销售额**拖动到**行值**存储段。

   ![](media/power-bi-visualization-combo-chart/linevaluebucket.png)

   组合图应如下所示：

   ![](media/power-bi-visualization-combo-chart/combochartdone-new.png)

## <a name="create-a-combo-chart-with-two-axes"></a>创建具有两个轴的组合图
在此任务中，我们会比较毛利和销售额。

1. 新建按“月份”跟踪“去年毛利率”的折线图。  一月的 GM% 是 35%，在四月达到峰值 45%，在七月下降，在八月再次达到峰值。 去年和本年度的销售额是否会呈现类似模式？

   ![](media/power-bi-visualization-combo-chart/combo1_new.png)
2. 将**本年度销售额 > 值**和**去年销售额**添加到折线图。 “去年毛利率”的比例尺比“销售额”的比例尺小得多，因此比较起来非常困难。      

   ![](media/power-bi-visualization-combo-chart/flatline_new.png)
3. 若要使视觉对象更易于查看和解释，请将折线图转换为折线和堆积柱形图。

   ![](media/power-bi-visualization-combo-chart/converttocombo_new.png)
4. 将**去年毛利率**从**列值**拖动到**行值**中。 Power BI 会创建两个坐标轴，这样就可以对数据集使用不同的比例尺；左侧度量值销售额是美元，右侧度量值是百分比。

   ![](media/power-bi-visualization-combo-chart/power-bi-combochart.png)    

## <a name="add-titles-to-the-axes"></a>向轴添加标题
1. 选择滚动油漆刷图标 ![](media/power-bi-visualization-combo-chart/power-bi-paintroller.png)，打开格式窗格。
2. 选择向下箭头以展开 **Y 轴**选项。
3. 对于 **Y 轴（列）**，将“**位置**”设置为“**左**”，将“**标题**”设置为“**打开**”，将“**样式**”设置为“**仅显示标题**”，并将“**显示**”设置为“**百万**”。

   ![](media/power-bi-visualization-combo-chart/power-bi-y-axis-column.png)
4. 在“Y 轴(列)”下，向下滚动并确保将“显示次级内容”设置为“开”。 该操作显示对组合图的折线图部分进行格式化的选项。

   ![](media/power-bi-visualization-combo-chart/power-bi-show-secondary.png)
5. 对于 **Y 轴（行）**，将“**位置**”保留为“**右**”，将“**标题**”设置为“**打开**”，并将“**样式**”设置为“**仅显示标题**”。

   组合图现在显示双轴，它们都具有标题。

   ![](media/power-bi-visualization-combo-chart/power-bi-titles-on.png)

6. （可选）修改文本字体、大小和颜色，并设置其他格式选项，以提升图表的显示效果和可读性。

从这里你可能想要：

* [将组合图添加为仪表板磁贴](service-dashboard-tiles.md)。
* [保存报表](service-report-save.md)。

## <a name="cross-highlighting-and-cross-filtering"></a>交叉突出显示和交叉筛选

突出显示组合图中的列或行可交叉突出显示和交叉筛选报表页上的其他可视化效果，反之亦然。 使用[视觉对象交互](service-reports-visual-interactions.md)可以更改此默认行为。

## <a name="next-steps"></a>后续步骤

[Power BI 报表中的可视化效果概述](power-bi-report-visualizations.md)

[Power BI 中的可视化效果类型](power-bi-visualization-types-for-reports-and-q-and-a.md)

[Power BI - 基本概念](service-basic-concepts.md)

更多问题？ [尝试参与 Power BI 社区](http://community.powerbi.com/)
