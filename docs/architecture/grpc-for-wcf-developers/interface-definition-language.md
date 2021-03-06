---
title: Interface 定义 Language-适用于 WCF 开发人员的 gRPC
description: 引入协议缓冲区 IDL。
ms.date: 09/02/2019
ms.openlocfilehash: 1f304502bd0091f753a3d2f7854298f4bbf983f1
ms.sourcegitcommit: f348c84443380a1959294cdf12babcb804cfa987
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/12/2019
ms.locfileid: "73967632"
---
# <a name="interface-definition-language"></a>接口定义语言

使用 WCF，服务可以使用 Web 服务定义语言（WSDL）（在运行时使用 .NET 反射动态生成）公开说明元数据。 如果使用的是平台中立的绑定（如 SOAP over HTTP），开发人员可以使用此元数据来生成这些服务的客户端。

gRPC 从协议缓冲区使用接口定义语言（IDL）。 协议缓冲区 IDL 是一种独立于平台的自定义语言，具有开放规范。 开发人员 `.proto` 文件中编写代码，以描述服务及其输入和输出。 然后，可以使用这些 `.proto` 文件为客户端和服务器生成特定于语言或平台的存根，允许多个不同的平台进行通信。 通过共享 `.proto` 文件，团队可生成代码以使用他人的服务而无需进行代码依赖。

Protobuf IDL 的优点之一就是作为一种自定义语言，它允许 gRPC 完全语言和平台不可知，而不是 favoring 其他任何技术。

Protobuf IDL 还设计用于读取和写入，而 WSDL 旨在用作计算机可读/可写格式。 更改 WCF 服务的 WSDL 通常需要更改服务代码本身，运行服务并从服务器重新生成 WSDL 文件。 与此相反，使用 `.proto` 文件时，更改很简单，可与文本编辑器一起应用，并自动流过生成的代码。 Visual Studio 2019 在保存时在后台生成 `.proto` 文件;使用其他编辑器（如 VS Code）时，将在生成项目时应用更改。

与 XML 进行比较时，尤其是 SOAP，使用 Protobuf 编码的消息具有很多优点。 Protobuf 消息往往比作为 SOAP XML 序列化的数据更小，并通过网络对它们进行编码、解码和传输变得更快。

与 SOAP 相比，Protobuf 的潜在缺点是，因为消息不能人工读取，所以调试消息内容需要额外的工具。

> [!TIP]
> gRPC*支持*服务器反射以动态访问服务而无需预编译的存根，尽管它更适用于通用工具，而不是特定于应用程序的客户端。 有关 gRPC Server 反射的详细信息，请参阅 GitHub 上的[gRPC/gRPC](https://github.com/grpc/grpc/blob/master/doc/server-reflection.md)存储库。

> [!NOTE]
> 与 Wcf-nettcp 绑定一起使用的 WCF 二进制格式比 Protobuf 更接近紧凑性和性能，但 Wcf-nettcp 只能在 .NET 客户端和服务器之间使用，而 Protobuf 是一个跨平台解决方案。

>[!div class="step-by-step"]
>[上一页](approach.md)
>[下一页](network-protocols.md)
