---
ms.openlocfilehash: d6c658f306dd4792e3cb5dbdc9471043ca95a071
ms.sourcegitcommit: d55e14eb63588830c0ba1ea95a24ce6c57ef8c8c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/11/2019
ms.locfileid: "67859188"
---
### <a name="httpruntimeappdomainapppath-throws-a-nullreferenceexception"></a>HttpRuntime.AppDomainAppPath 引发 NullReferenceException

|   |   |
|---|---|
|详细信息|在 .NET Framework 4.6.2 中，当检索包含空字符的 <code>P:System.Web.HttpRuntime.AppDomainAppPath</code> 值时，运行时会引发 <code>T:System.NullReferenceException</code>。在 .NET Framework 4.6.1 及早期版本中，运行时将引发 <code>T:System.ArgumentNullException</code>。|
|建议|可执行以下任一操作来应对此更改：<ul><li>如果应用程序是在 .NET Framework 4.6.2 上运行，请处理 <code>T:System.NullReferenceException</code>。</li><li>升级到 .NET Framework 4.7，这将还原以前的行为并引发 <code>T:System.ArgumentNullException</code>。</li></ul>|
|范围|边缘|
|版本|4.6.2|
|类型|重定目标|
|受影响的 API|<ul><li><xref:System.Web.HttpRuntime.AppDomainAppPath?displayProperty=nameWithType></li></ul>|

