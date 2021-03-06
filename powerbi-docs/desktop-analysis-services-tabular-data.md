---
title: "在 Power BI Desktop 中使用 Analysis Services 表格数据"
description: "Power BI Desktop 中的 Analysis Services 表格数据"
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
ms.openlocfilehash: 66f94abb9439154ab9d24ae6c352dd8b139c1a72
ms.sourcegitcommit: 7249ff35c73adc2d25f2e12bc0147afa1f31c232
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/25/2018
---
# <a name="using-analysis-services-tabular-data-in-power-bi-desktop"></a>在 Power BI Desktop 中使用 Analysis Services 表格数据
借助 Power BI Desktop，你有两种方法可以连接到 SQL Server Analysis Services 表格模型并从中获取数据：通过使用实时连接浏览或选择项目并将其导入到 Power BI Desktop。

让我们仔细了解下。

**通过使用实时连接浏览** – 使用实时连接时，表格模型或透视中的项目（如表格、列和度量值）会显示在 Power BI Desktop 字段列表中。 你可以使用 Power BI Desktop 的高级可视化效果和报表工具以全新且高度交互的方式浏览你的表格模型。

在进行实时连接时，表格模型中的数据不会导入到 Power BI Desktop 中。 每次与可视化效果进行交互时，Power BI Desktop 都将查询表格模型，并计算你所看到的结果。 你看到的始终是最新的数据。 请记住，表格模型是高度安全的。 在 Power BI Desktop 中显示的项目取决于你对连接到的表格模型所具有的权限。

当你在 Power BI Desktop 中创建了动态报表后，可以将它们发布到 Power BI 站点进行共享。 当使用与表格模型的实时连接将 Power BI Desktop 文件发布到 Power BI 站点时，管理员必须安装并配置本地数据网关。 若要了解详细信息，请参阅[本地数据网关](service-gateway-onprem.md)。

**选择项目并导入到 Power BI Desktop 中** – 使用此选项进行连接时，你可以在表格模型或透视中选择项目（如表、列和度量值），并将其加载到 Power BI Desktop 模型中。 你可以使用 Power BI Desktop 的高级查询编辑器进一步调整你所需查询的内容。 你可以使用 Power BI Desktop 的建模功能进一步对数据进行建模。 Power BI Desktop 和表格模型之间不会保持实时连接。 接着，你可以脱机浏览你的 Power BI Desktop 模型或将其发布到 Power BI 站点。

## <a name="to-connect-to-a-tabular-model"></a>连接到表格模型
1. 在 Power BI Desktop 中，在**开始**选项卡上，单击**获取数据**。
   
   ![](media/desktop-analysis-services-tabular-data/pbid_sqlas_getdata.png)
2. 单击 **SQL Server Analysis Services 数据库**，然后单击**连接**。
   
   ![](media/desktop-analysis-services-tabular-data/pbid_sqlas_getdata_as.png)
3. 输入服务器名称并选择连接模式。 
   
   ![](media/desktop-analysis-services-tabular-data/pbid_sqlas_getdata_as_server.png)
4. 此步骤取决于你所选的连接模式：

* 如果你正在进行实时连接中，请在导航器中选择“表格”模型或透视。
  
  ![](media/desktop-analysis-services-tabular-data/pbid_sqlas_getdata_as_live.png)
* 如果你选择了选择项目并获取数据，请在导航器中选择“表格”模型或透视。 你可以进一步仅选择特定的表或列进行加载。 若要在加载前对数据进行调整，请单击“编辑”以打开查询编辑器。 准备就绪时，单击“加载”将数据导入到 Power BI Desktop 中。

![](media/desktop-analysis-services-tabular-data/pbid_sqlas_getdata_as_select.png)

## <a name="frequently-asked-questions"></a>常见问题
**问：**我是否需要一个本地数据网关？

**答：**这个需要视情况而定。 如果你使用 Power BI Desktop 实时连接到表格模型，但不打算发布到 Power BI 站点，则不需要网关。 另一方面，如果你确实想将其发布到 Power BI 站点，则数据网关是必需的，以确保 Power BI 服务与你的本地 Analysis Services 服务器之间的通信安全。 请务必在安装数据网关之前与 Analysis Services 服务器管理员联系。

如果你选择了选择项目并获取数据，则你会将表格模型数据直接导入到 Power BI Desktop 文件中，因此不需要网关。

**问：**从 Power BI 服务实时连接到表格模型与从 Power BI Desktop 中实时连接到表格模型之间有什么区别？

**答：**当从 Power BI 服务中的站点将表格模型实时连接到组织中的本地 Analysis Services 数据库时，需要本地数据网关来确保它们之间的通信安全。 当从 Power BI Desktop 实时连接到表格模型时，因为 Power BI Desktop 和要连接到的 Analysis Services 服务器都是在组织中本地运行的，因此不需要网关。 但是，如果将 Power BI Desktop 文件发布到 Power BI 站点，则需要网关。

**问：**如果我创建了实时连接，我能否连接到同一个 Power BI Desktop 文件中的其他数据源？

**答：**不能。 你不能在同一文件中浏览实时数据并连接到其他类型的数据源。 如果你已导入数据或连接到 Power BI Desktop 文件中的另一个数据源，你则需要新建一个文件来实时浏览。

**问：**如果我创建了实时连接，我可以在 Power BI Desktop 中编辑模型或进行查询吗？

答案：可以在 Power BI Desktop 中创建报表级别度量值，但当浏览实时数据时会禁用所有其他查询和建模功能。

**问：**如果我创建了实时连接，它是安全的吗？

**答：**是的。 你当前的 Windows 凭据用于连接到 Analysis Services 服务器。 在实时浏览时，你不能在 Power BI 服务或 Power BI Desktop 中使用基本或存储的凭据。

**问：**在导航器中，我看到模型和透视。 有什么区别？

**答：**透视是表格模型的特定视图。 它可能仅包含特定的表、列或度量值，具体取决于独特的数据分析需求。 表格模型始终包含至少一个透视，其中能包含模型中的所有内容。 如果你不确定应选择哪个，请与你的管理员联系。

## <a name="to-change-the-server-name-after-initial-connection"></a>初始连接后更改服务器名称
使用实时浏览连接创建 Power BI Desktop 文件后，可能会出现你想要将连接切换到其他服务器的情况。 例如，如果当你在连接到开发服务器时创建了 Power BI Desktop 文件，在发布到 Power BI 服务前，你想要将连接切换至生产服务器。

1. 从功能区中选择**编辑查询**。
   
   ![](media/desktop-analysis-services-tabular-data/pbid_sqlas_chname_editquery.png)
2. 输入新的服务器名称。
   
   ![](media/desktop-analysis-services-tabular-data/pbid_sqlas_chname_dialog.png)

