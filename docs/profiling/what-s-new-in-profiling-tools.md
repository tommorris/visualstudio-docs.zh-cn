---
title: 分析工具中的新增功能 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology: vs-ide-debug
ms.topic: conceptual
helpviewer_keywords:
- profiling
- what's new
ms.assetid: d4736cc8-8961-4089-be9e-d5190ce8353c
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 0acc7d48967fba4e05d139a6f84107800cea5393
ms.sourcegitcommit: 4667e6ad223642bc4ac525f57281482c9894daf4
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/20/2018
ms.locfileid: "36297772"
---
# <a name="whats-new-in-profiling-tools-in-includevsdev15miscincludesvsdev15mdmd"></a>[!include[vs_dev15](../misc/includes/vs_dev15_md.md)] 中的分析工具的新增功能

诊断工具包括新的可视化功能，有助于确定应用程序中需要修复的问题。 诊断工具现在包括对 ASP.NET 应用程序的支持。

有关其他信息，请参阅 [[!include[vs_dev15](../misc/includes/vs_dev15_md.md)] 的发行说明](/visualstudio/releasenotes/vs2017-relnotes#debuggingdiag)。

工具中新增“摘要”选项卡，可帮助你聚焦性能分析的关键领域。 此选项卡显示已发生多少个事件，可以拍摄堆的快照，以及快速启用 CPU 使用情况数据收集。 此视图显示任何 [Application Insights](https://azure.microsoft.com/en-us/documentation/articles/app-insights-visual-studio/) 或 [UI 分析](/visualstudio/releasenotes/vs2017-relnotes#UIAnalysis)事件。 此外，对于 Visual Studio Enterprise，此视图还显示 IntelliTrace 事件。

![诊断工具“摘要”选项卡](../profiling/media/DiagToolsSummaryTab-2.png "DiagToolsSummaryTab")

CPU 使用情况工具具有[新的可视化功能](../profiling/Beginners-Guide-to-Performance-Profiling.md)，可帮助你识别最有可能导致性能问题的函数。 新的**调用方/被调用方**视图可用于调查所选函数调用和被调用的成本。

![诊断工具调用方和被调用方视图](../profiling/media/DiagToolsCallerCallee.png "DiagToolsCallerCallee")

## <a name="see-also"></a>请参阅

- [Visual Studio 中的分析功能](../profiling/index.md)
- [首先了解分析工具](../profiling/profiling-feature-tour.md)