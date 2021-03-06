---
title: 如何应用 Python 搜索路径
description: 简要介绍 Visual Studio 如何在环境和项目中使用 Python 搜索路径。
ms.date: 06/27/2018
ms.prod: visual-studio-dev15
ms.technology: vs-python
ms.topic: conceptual
author: kraigb
ms.author: kraigb
manager: douge
ms.workload:
- python
- data-science
ms.openlocfilehash: 2a02bf78d731764b0725c03cefb4959451a40b9c
ms.sourcegitcommit: 4c60bcfa2281bcc1a28def6a8e02433d2c905be6
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/14/2018
ms.locfileid: "42626778"
---
# <a name="how-visual-studio-uses-python-search-paths"></a>Visual Studio 如何使用 Python 搜索路径

借助典型的 Python 用法，`PYTHONPATH` 环境变量（或 `IRONPYTHONPATH` 等）可为模块文件提供默认搜索路径。 也就是说，当使用 `from <name> import...` 或 `import <name>` 语句时，Python 会搜索下列位置以获得匹配的名称：

1. Python 的内置模块。
1. 包含正在运行的 Python 代码的文件夹。
1. 适用环境变量定义的“模块搜索路径”。 （请参阅核心 Python 文档中的[模块搜索路径](https://docs.python.org/2/tutorial/modules.html#the-module-search-path)和[环境变量](https://docs.python.org/2/using/cmdline.html#envvar-PYTHONPATH)。）

但 Visual Studio 会忽略搜索路径环境变量，即使已为整个系统设置了该变量。 实际上，此变量被忽略的具体原因是整个系统都设置了此变量，从而引发了一些无法自动解答的问题，例如引用的模块是适用于 Python 2.7 还是 Python 3.6+。 它们是否将替代标准库模块？ 开发人员是否注意到此行为，或者它是一个恶意的攻击尝试？

因此，Visual Studio 提供了一种方法，可直接在环境和项目中指定搜索路径。 在 Visual Studio 中运行或调试的代码会接收 `PYTHONPATH` 值（和其他等效变量）中的搜索路径。 通过添加搜索路径，Visual Studio 会在需要时检查这些位置中的库并为它们构建 IntelliSense 数据库（Visual Studio 2017 版本 15.5 及更早版本；构建数据库需要一些时间，具体取决于库的数量）。

若要添加搜索路径，请在”解决方案资源管理器”中右键单击“搜索路径”，选择“将文件夹添加到搜索路径”，并选择要包括的文件夹。 此路径将用于与该项目关联的任何环境。 （如果环境基于 Python 3，在尝试将搜索路径添加到 Python 2.7 模块时，可能会发生错误。）

通过选择“将 Zip 存档添加到搜索路径的”，还可将具有 .zip 或 .egg 扩展的文件添加为搜索路径。 与文件夹一样，将扫描这些文件的内容，并使其对 IntelliSense 可用。

如果定期使用相同的搜索路径，且内容不经常更改，则将其安装到 site-packages 文件夹会更高效。 搜索路径随后会进行分析并存储在 IntelliSense 数据库中，会始终与预期的环境关联且不需要向每个项目添加搜索路径。

### <a name="see-also"></a>请参阅

- [在 Visual Studio 中管理 Python 环境](managing-python-environments-in-visual-studio.md)
- [为项目选择解释器](selecting-a-python-environment-for-a-project.md)
- [对依赖项使用 requirements.txt](managing-required-packages-with-requirements-txt.md)
- [“Python 环境”窗口参考](python-environments-window-tab-reference.md)
