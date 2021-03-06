---
title: CA2142：不应使用 LinkDemand 保护透明代码
ms.date: 11/04/2016
ms.prod: visual-studio-dev15
ms.technology: vs-ide-code-analysis
ms.topic: reference
f1_keywords:
- CA2142
ms.assetid: 6dc59053-5dd9-4583-bf10-5f339107e59f
author: gewarren
ms.author: gewarren
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 527086fa2b17de0330b394a7041232312f3b1719
ms.sourcegitcommit: 568bb0b944d16cfe1af624879fa3d3594d020187
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/13/2018
ms.locfileid: "45547211"
---
# <a name="ca2142-transparent-code-should-not-be-protected-with-linkdemands"></a>CA2142：不应使用 LinkDemand 保护透明代码
|||
|-|-|
|TypeName|TransparentMethodsShouldNotBeProtectedWithLinkDemands|
|CheckId|CA2142|
|类别|Microsoft.Security|
|是否重大更改|重大|

## <a name="cause"></a>原因
 透明方法需要<xref:System.Security.Permissions.SecurityAction>或其他安全要求。

## <a name="rule-description"></a>规则说明
 需要 Linkdemand 来访问它们的透明方法将引发此规则。 安全透明代码不应负责验证某个操作的安全，因此不应要求权限。 透明方法不会为非特定的安全，因为它们不应作出任何安全决策。 此外，安全关键代码，这会使安全决策，不应依赖透明代码以之前进行此类决定。

## <a name="how-to-fix-violations"></a>如何解决冲突
 若要修复此规则的冲突，请删除透明方法链接要求或此方法标记<xref:System.Security.SecuritySafeCriticalAttribute>属性，如果它正在执行安全检查，如安全要求。

## <a name="when-to-suppress-warnings"></a>何时禁止显示警告
 不禁止显示此规则发出的警告。

## <a name="example"></a>示例
 在以下示例中，将引发规则方法因为该方法是透明的并标有 LinkDemand <xref:System.Security.PermissionSet> ，其中包含<xref:System.Security.Permissions.SecurityAction>。

 [!code-csharp[FxCop.Security.CA2142.TransparentMethodsShouldNotBeProtectedWithLinkDemands#1](../code-quality/codesnippet/CSharp/ca2142-transparent-code-should-not-be-protected-with-linkdemands_1.cs)]

 不禁止显示此规则发出的警告。