---
title: 安全问题 |Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- vs-ide-sdk
ms.topic: conceptual
helpviewer_keywords:
- security [Debugging SDK]
- debugging [Debugging SDK], security
ms.assetid: d6ffff0a-afb4-4f38-86d8-476c881c4e4b
author: gregvanl
ms.author: gregvanl
manager: douge
ms.workload:
- vssdk
ms.openlocfilehash: 6cd4d07721f202169ca0689882ac1a41045a4d61
ms.sourcegitcommit: 71b307ce86c4079cc7ad686d8d5f96a6a123aadd
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/25/2018
ms.locfileid: "39252318"
---
# <a name="security-issues"></a>安全问题
若要调试使用 Visual Studio 的程序，所需的唯一权限是相同的一名开发人员需要运行程序。 这包括大多数情况下的远程调试。 某些情况下，涉及其他服务，如 Internet 信息服务，可能需要更高级别的权限。  
  
 在 Visual Studio 运行时，进程调试管理器 (PDM) 在本地计算机上跟踪调试进程。 远程调用的程序*msvsmon.exe*由开发人员来处理远程调试，并使 PDM 可启动。 (*msvsmon.exe*不是一个服务，必须手动启动，以启用该计算机上远程调试。)当 Visual Studio (或*msvsmon.exe*) 是未运行，没有过程进行跟踪以进行调试。  
  
 开发人员可以调试其开始使用任何特殊权限的程序。 开发人员甚至可以调试该其他人是否相同的安全组的成员由其他人启动的进程。 而且，若要启用远程调试，有必要仅以将所需的文件复制到远程计算机并启动*msvsmon.exe*。 有关详细信息，请参阅[远程调试](../../debugger/remote-debugging.md)。  
  
## <a name="see-also"></a>请参阅  
 [调试任务](../../extensibility/debugger/debugging-tasks.md)   
 [进程调试管理器](../../extensibility/debugger/process-debug-manager.md)   
 [远程调试](../../debugger/remote-debugging.md)
