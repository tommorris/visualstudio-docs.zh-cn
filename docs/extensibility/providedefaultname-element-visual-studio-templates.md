---
title: ProvideDefaultName 元素 （Visual Studio 模板） |Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- vs-ide-general
ms.topic: conceptual
f1_keywords:
- http://schemas.microsoft.com/developer/vstemplate/2005#ProvideDefaultName
helpviewer_keywords:
- ProvideDefaultName element [Visual Studio project templates]
ms.assetid: 7b0e7b20-fd6b-42e2-81d0-e5100cea0528
author: gregvanl
ms.author: gregvanl
manager: douge
ms.workload:
- vssdk
ms.openlocfilehash: a187df0e50a2948ab6f1ef3a0fffea651dca23b9
ms.sourcegitcommit: 06db1892fff22572f0b0a11994dc547c2b7e2a48
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/08/2018
ms.locfileid: "39636007"
---
# <a name="providedefaultname-element-visual-studio-templates"></a>ProvideDefaultName 元素 （Visual Studio 模板）
指定是否[!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)]项目系统将生成的模板中的默认名称**添加新项**或**新项目**对话框。  
  
 \<VSTemplate >  
 \<TemplateData >  
 \<ProvideDefaultName >  
  
## <a name="syntax"></a>语法  
  
```xml  
<ProvideDefaultName> true/false </ProvideDefaultName>  
```  
  
## <a name="attributes-and-elements"></a>特性和元素  
 下列各节描述了特性、子元素和父元素。  
  
### <a name="attributes"></a>特性  
 无。  
  
### <a name="child-elements"></a>子元素  
 无。  
  
### <a name="parent-elements"></a>父元素  
  
|元素|描述|  
|-------------|-----------------|  
|[TemplateData](../extensibility/templatedata-element-visual-studio-templates.md)|必需的元素。<br /><br /> 将此模板分类并定义此模板在 **“新建项目”** 或 **“添加新项”** 对话框中的显示方式。|  
  
## <a name="text-value"></a>文本值  
 需要一个文本值。  
  
 文本必须是`true`或`false`，，该值指示是否生成中的模板的默认名称**添加新项**或**新项目**对话框。  
  
## <a name="remarks"></a>备注  
 `ProvideDefaultName` 是可选元素。 默认值为 `true`。  
  
 如果`ProvideDefaultName`元素是`false`，则**名称**对应的框**添加新项**并**新项目**对话框还包含值`<Enter_name>`。  
  
 使用[DefaultName](../extensibility/defaultname-element-visual-studio-templates.md)指定项目的默认名称或项中的元素**添加新项**并**新项目**对话框。 时的值`ProvideDefaultName`元素是`true`，省略`DefaultName`元素的项目填充模板的名称，即从值的对话框[名称](../extensibility/name-element-visual-studio-templates.md)元素。
  
## <a name="example"></a>示例  
 下面的代码示例设置`ProvideDefaultName`元素`false`。  
  
```  
<VSTemplate Type="Item" Version="3.0.0"  
    xmlns="http://schemas.microsoft.com/developer/vstemplate/2005">  
    <TemplateData>  
        <Name>MyClass</Name>  
        <Description>My custom C# class.</Description>  
        <Icon>Icon.ico</Icon>  
        <ProjectType>CSharp</ProjectType>  
        <ProvideDefaultName>false</ProvideDefaultName>  
    </TemplateData>  
    <TemplateContent>  
        <ProjectItem>MyClass.cs</ProjectItem>  
    </TemplateContent>  
</VSTemplate>  
```  
  
## <a name="see-also"></a>请参阅  
 [Visual Studio 模板架构参考](../extensibility/visual-studio-template-schema-reference.md)   
 [创建项目和项模板](../ide/creating-project-and-item-templates.md)
