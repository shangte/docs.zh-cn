---
title: 安装 F#
description: 了解如何以各种F#不同的方式安装。
ms.date: 12/20/2019
ms.openlocfilehash: 302e04f7cf3271516dff88d9d5f18f620b6ede80
ms.sourcegitcommit: 30a558d23e3ac5a52071121a52c305c85fe15726
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/25/2019
ms.locfileid: "75346566"
---
# <a name="install-f"></a>安装 F\#

可以通过多种方式安装 F#，具体取决于环境。

## <a name="install-f-with-visual-studio"></a>使用 Visual Studio 安装 F#

1. 如果是首次下载[Visual Studio](https://visualstudio.microsoft.com/downloads/?utm_medium=microsoft&utm_source=docs.microsoft.com&utm_campaign=inline+link&utm_content=download+vs2019) ，则会先安装 Visual Studio 安装程序。 从安装程序安装适当版本的 Visual Studio。

   如果已安装 Visual Studio，请选择要添加F#到的版本旁边的 "修改"。

2. 在 "工作负荷" 页上，选择 " **ASP.NET" 和 "web 开发**" 工作负载，其中包括F#和 .net Core 对 ASP.NET Core 项目的支持。

3. 选择右下角的 "**修改**"，安装所选的所有内容。

   然后，可以F#通过选择 "在 Visual Studio 安装程序中**启动**" 打开 Visual Studio。

## <a name="install-f-with-visual-studio-code"></a>使用 Visual Studio Code 安装 F#

1. 确保已安装[git](https://git-scm.com/download)并可用于你的路径。 可以通过在命令提示符下输入 `git --version` 并按**enter**来验证它是否已正确安装。

2. 安装[.NET Core SDK](https://dotnet.microsoft.com/download)和[Visual Studio Code](https://code.visualstudio.com)。

3. 选择扩展图标，然后搜索 "Ionide 入门"：

   [ionide-fsharp](https://marketplace.visualstudio.com/items?itemName=Ionide.Ionide-fsharp) 是在 Visual Studio Code 中支持 F# 所需的唯一插件。 然而，也可以安装[Ionide FAKE](https://marketplace.visualstudio.com/items?itemName=Ionide.Ionide-FAKE) 来获取[FAKE](https://fake.build/) 支持，以及安装[Ionide paket](https://marketplace.visualstudio.com/items?itemName=Ionide.Ionide-Paket) 来获取 [paket](https://fsprojects.github.io/Paket/) 支持。 FAKE 和 Paket 是分别用于生成项目和管理依赖项的其他 F# 社区工具。

## <a name="install-f-with-visual-studio-for-mac"></a>使用 Visual Studio for Mac 安装 F#

在 [Visual Studio for Mac](https://visualstudio.microsoft.com/vs/mac/?utm_medium=microsoft&utm_source=docs.microsoft.com&utm_campaign=inline+link) 中会默认安装 F#，无论选择哪种配置。

安装完成后，选择 "**启动 Visual Studio**"。 还可以通过 macOS 上的查找器打开 Visual Studio。

## <a name="install-f-on-a-build-server"></a>在F#生成服务器上安装

如果通过 .NET SDK 使用 .NET Core 或 .NET Framework，只需在生成服务器上安装 .NET SDK。 它包含你所需的一切。

如果使用的是 .NET Framework 而**不**是使用 .net SDK，则需要将[Visual Studio 生成工具 SKU](https://visualstudio.microsoft.com/thank-you-downloading-visual-studio/?sku=BuildTools&rel=16)安装到 Windows Server 上。 在安装程序中，选择 " **.net 桌面生成工具**"，然后选择 "安装程序" 菜单右侧的 "  **F#编译器**" 组件。
