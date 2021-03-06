---
title: "Power BI 服务内容包程序概述"
description: "内容包认证计划"
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
ms.date: 01/04/2018
ms.author: maghan
ms.openlocfilehash: f0a50c0aba1a05c55236192a730c3187cb37c055
ms.sourcegitcommit: 6e693f9caf98385a2c45890cd0fbf2403f0dbb8a
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/30/2018
---
# <a name="overview-of-the-power-bi-service-content-pack-program"></a>Power BI 服务内容包程序概述
内容包是一组全新的内容，允许用户立即获取源中的见解。 内容包通常集中在特定业务方案，提供关于角色、域或工作流的见解。

ISV 可以生成模板内容包，允许客户使用其自己的帐户连接并实例化。 作为域专业人员，他们可以采用业务用户轻易使用的方式解锁数据。 内容包为你的客户提供了临时监视和分析，而无需花费大量精力用在报表基础结构上。 

可以将这些 ISV 生成模板内容包提交到 Power BI 团队，以在 Power BI 内容包库 (app.powerbi.com/getdata/services) 和 Microsoft AppSource (appsource.microsoft.com) 上公开发布。 单击[此处](template-content-pack-experience.md)可查看公用内容包体验的示例。

## <a name="overview"></a>概述
开发并提交模板内容包的常规过程包括多个步骤。

 ![过程](media/service-content-pack-overview/developer-content-pack-overview.png)

1. [查看要求](#requirements)并确保满足这些要求
2. 在 Power BI Desktop 中[生成内容](template-content-pack-authoring.md#queries)
3. 在 PowerBI.com 中[创建仪表板](template-content-pack-authoring.md#dashboard)
4. 在你的组织中[测试内容包](template-content-pack-testing.md)
5. 将内容[提交](template-content-pack-testing.md#submission)到 Power BI 以便发布

<a name="requirements"></a>

## <a name="requirements"></a>要求
若要生成并提交内容包，以在 PowerBI 服务和 AppSource 中发布，必须满足以下要求：

* 必须具有由业务用户使用的 SaaS 应用程序。
* SaaS 应用程序具有可以在 Power BI 中进行可视化的用户数据。
* SaaS 应用程序具有可通过公共 Internet 访问的 API。 理想情况下，API 是基于 REST 的 API 或 OData 数据源。 Power BI 内容包支持多种身份验证类型，如基本身份验证、OAuth 2.0 和 API 密钥。 
* 你的 SaaS 应用程序批准用于发布内容包。 您的请求提交到 pbiservicesapps@microsoft.com。我们将对每次提交的相关性和预期使用情况进行评审。 
* 已签署合作伙伴协议。 你将在[提交步骤](template-content-pack-testing.md#submission)中执行该操作。

请查看[创作](template-content-pack-authoring.md)部分，了解有关技术要求的详细信息。

## <a name="business-scenario"></a>业务方案
内容包提供了侧重于特定业务方案的见解和指标。 了解你的受众和其将从内容包获得的好处，将有助于确保你的用户对你提供的内容满意。

### <a name="tips"></a>提示
* 确认你的受众和其尝试完成的任务  
* 重点关注某个时间段（过去 90 天）或过去 N 个结果  
* 只导入与你的方案相关的表/列  
* 考虑为分开的独特方案提供多个内容包  

## <a name="frequently-asked-questions"></a>常见问题
**可以为我尚未拥有的第三方 SaaS 应用程序生成 Power BI 服务内容包吗？**

不可以，我们目前需要先与 SaaS 应用程序的所有者签署合作伙伴协议，然后才能在服务中发布内容包。

**我的服务没有公共开发人员 API。我仍可以生成直接从数据存储中拉取数据的 Power BI 服务内容包吗？**

不可以，Power BI 服务内容包需要可以通过公共 Internet 访问的开发人员 API。

**服务内容包支持哪种类型的 API，它们可以使用哪些身份验证类型？**

Power BI 服务内容包支持任何 REST API 或 OData 数据源。 Power BI 可以处理多种身份验证类型，包括基本身份验证、OAuth2.0 和 Web API 密钥。 请查看[创作](template-content-pack-authoring.md#dashboard)文章，详细了解技术要求。

**我有关于服务内容包的更多问题。我如何与你联系？**

可以随时通过以下电子邮件向我们发送你的问题：pbiservicesapps@microsoft.com

## <a name="support"></a>支持
开发期间如需支持，请访问 [https://powerbi.microsoft.com/support](https://powerbi.microsoft.com/support)。 该网站有专门人员监视和管理。 客户事件可快速找到通往合适团队的方法。

## <a name="next-step"></a>下一步
[创作](template-content-pack-authoring.md)

