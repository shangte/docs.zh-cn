---
title: 云本机应用程序呢？
description: 通过 Azure 云和 Windows 容器现代化现有 .NET 应用程序 | 云本机应用程序呢？
ms.date: 04/28/2018
ms.openlocfilehash: cf4c3b24a4eeb62ed84a5fccb294b675d38fcc36
ms.sourcegitcommit: 22be09204266253d45ece46f51cc6f080f2b3fd6
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/08/2019
ms.locfileid: "72318450"
---
# <a name="what-about-cloud-native-applications"></a>云本机应用程序呢？

尽管[云本机](https://azure.microsoft.com/overview/cloudnative/)应用程序并不是本指南的主要重点，但可以帮助你了解此现代化成熟度级别，并将其与云优化应用程序进行区分。

图 4-3 在应用程序现代化成熟度级别中定位云本机应用：

![演示如何定位云本机应用程序的关系图。](./media/what-about-cloud-native-applications/positioning-cloud-native-applications.png)

**图 4-3.** 定位云本机应用程序

云本机现代化成熟度级别通常需要新的开发投资。 迁移到云本机级别通常由尽可能多地现代化应用程序以大幅改进大型应用程序规模的业务需求驱动，方法是：在长期降低成本的同时创建可从应用程序的其他区域单独部署和缩放的自治子系统（微服务），并提高这些自治应用部件（提供巨大的竞争优势）的演变灵活性。

云本机应用程序的主要要素基于微服务体系结构方法，这些方法可以灵活地进行发展，并调整为在部署到本地或云环境的整体式体系结构中难以实现的限制。

图 4-4 显示了云本机模型的主要特征。

![列出云本机主要特征的关系图。](./media/what-about-cloud-native-applications/cloud-native-characteristics.png)

**图 4-4.** 云本机特征

此外，还可以通过添加其他服务（如人工智能 (AI)、机器学习 (ML) 和 IoT）来扩展基本的新式 Web 应用和云本机应用。 可以使用其中任何服务来扩展任何可能的云优化方法。

云本机级别的应用程序的根本区别在于应用程序体系结构。 根据定义，云本机应用程序是基于微服务的应用。 与整体式 Web 应用程序或传统 N 层应用程序相比，云本机应用需要特殊的体系结构、技术和平台。

## <a name="cloud-native-applications-details"></a>云本机应用程序详细信息

对于大型和任务关键型应用程序而言，云本地是一种更高级或更成熟的状态。 云本机应用程序通常需要从头开始创建的体系结构和设计，而不是现代化现有应用程序。 云本机应用程序和更简单的云优化 Web 应用之间的主要区别是，建议使用云本机方法中的微服务体系结构。 云优化应用也可以是整体式 Web 应用或 N 层应用。

[十二因素应用](https://12factor.net/)（与微服务方法密切相关的模式集合）也被视为云本机应用程序体系结构的要求。

[云本机计算基础 (CNCF)](https://www.cncf.io/) 是云本机原则的主要推动者。 Microsoft 是 [CNCF 的 成员](https://azure.microsoft.com/blog/announcing-cncf/)。

有关示例定义以及有关云本机应用程序特征的详细信息，请参阅 Gartner 文章[如何构建和设计云本机应用程序](https://www.gartner.com/doc/3181919/architect-design-cloudnative-applications)。 有关 Microsoft 对如何实现云本机应用程序的具体指导，请参阅 [.NET 微服务：适用于容器化 .NET 应用程序的体系结构](https://aka.ms/microservicesebook)。

如果将整个应用程序迁移到云本机模型，则要考虑的最重要因素是，必须重新架构到基于微服务的体系结构。 由于涉及大型重构过程，因此这显然需要大量开发工作。 对于需要新级别的可伸缩性和长期的灵活性的任务关键型应用程序，通常选择此选项。 但是，可以通过只为几个新方案添加微服务来开始迁移到云本机，最终将应用程序完全重构为微服务。 这是最适合某些方案的增量方法。

## <a name="what-about-microservices"></a>微服务呢？

在考虑组织的云本机应用程序时，了解微服务及其工作原理非常重要。

微服务体系结构是一种高级方法，可以将该方法用于从头开始创建的应用程序，也可以在将现有应用程序发展为云本机应用程序时将该方法用于应用程序。 首先，可以将一些微服务添加到现有应用程序，以了解新的微服务范例。 但很显然，你需要进行构建并编写代码，特别是对于这种类型的体系结构方法。

但是，对于任何新的或新式应用程序，微服务不是必需的。 微服务并不是“万能的”，也不是创建每个应用程序的唯一最佳方法。 使用微服务的方式和时间取决于需要构建的应用程序的类型。

微服务体系结构正成为基于多个独立子系统的分布式和大型或复杂的任务关键型应用程序的首选方法，其形式是自治服务。 在基于微服务的体系结构中，将应用程序生成为可独立开发、测试、版本控制、部署和缩放的一系列服务。 每个服务可以包含任何相关的自治数据库。

有关可使用 .NET Core 实现的微服务体系结构的详细信息，请参阅可下载的 PDF 电子书 [.NET 微服务：适用于容器化 .NET 应用程序的体系结构](https://aka.ms/microservicesebook)。 可以[在线](../../microservices/index.md)获得本指南。

但即使是在微服务提供功能强大的独立部署、强子系统边界和技术多样性的情况下，它们也会带来许多新挑战。 这些挑战与分布式应用程序开发相关，如零碎和独立的数据模型；实现微服务之间的可复原通信；需要最终一致性；以及操作复杂性。 与传统整体式应用程序相比，微服务加深了复杂性。

由于微服务体系结构的复杂性，因此只有特定方案和特定应用程序类型适用于基于微服务的应用程序。 其中包括具有多个不断发展的子系统的大型复杂应用程序。 在这些情况下，值得投资更复杂的软件体系结构，因为它将增强长期灵活性并提高应用程序维护效率。 但对于不太复杂的方案，最好使用整体式应用程序方法或更简单的 N 层方法。

最后要注意的是，即使冒着重复此概念的风险，也不应在应用程序中将微服务用作“全有或全无”。 可以通过基于微服务添加全新小型方案来扩展和改进现有整体式应用程序。 无需从头开始即可使用微服务体系结构方法。 事实上，我们建议通过添加新方案来改进现有整体式或 N 层应用程序。 最终，可以将应用程序细分为自治组件或微服务。 可以沿微服务的方向逐步开始改进整体式应用程序。

在任何情况下，本指南的其余部分都集中于“没有基于微服务的应用”，因为本指南主要旨在实现通常具有整体式或 N 层体系结构的现有应用的现代化。

> [!div class="step-by-step"]
> [上一页](microsoft-technologies-in-cloud-optimized-applications.md)
> [下一页](deploy-existing-net-apps-as-windows-containers.md)
