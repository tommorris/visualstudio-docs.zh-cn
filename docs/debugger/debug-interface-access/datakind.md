---
title: DataKind |Microsoft 文档
ms.custom: ''
ms.date: 11/04/2016
ms.technology: vs-ide-debug
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- DataKind enumeration
ms.assetid: b64be708-22d6-4360-99e7-8f4e6b196de7
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: c3de9ef6128c3cd5ca6eae80a257b3dc2982cd0f
ms.sourcegitcommit: 3d10b93eb5b326639f3e5c19b9e6a8d1ba078de1
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/18/2018
ms.locfileid: "31458185"
---
# <a name="datakind"></a>DataKind
指示数据值的特定范围。  
  
## <a name="syntax"></a>语法  
  
```C++  
enum DataKind {   
   DataIsUnknown,  
   DataIsLocal,  
   DataIsStaticLocal,  
   DataIsParam,  
   DataIsObjectPtr,  
   DataIsFileStatic,  
   DataIsGlobal,  
   DataIsMember,  
   DataIsStaticMember,  
   DataIsConstant  
};  
```  
  
## <a name="elements"></a>元素  
 DataIsUnknown  
 无法确定 data 符号。  
  
 DataIsLocal  
 数据项是一个本地变量。  
  
 DataIsStaticLocal  
 数据项是静态局部变量。  
  
 DataIsParam  
 数据项是正式参数。  
  
 DataIsObjectPtr  
 数据项是一个对象指针 (`this`)。  
  
 DataIsFileStatic  
 数据项是文件范围内的变量。  
  
 DataIsGlobal  
 数据项是全局变量。  
  
 DataIsMember  
 数据项是一个对象成员变量。  
  
 DataIsStaticMember  
 数据项是类的静态变量。  
  
 DataIsConstant  
 数据项是一个常量值。  
  
## <a name="remarks"></a>备注  
 此枚举中的值由[idiasymbol:: Get_datakind](../../debugger/debug-interface-access/idiasymbol-get-datakind.md)方法。  
  
## <a name="requirements"></a>要求  
 标头： cvconst.h  
  
## <a name="see-also"></a>请参阅  
 [枚举和结构](../../debugger/debug-interface-access/enumerations-and-structures.md)   
 [IDiaSymbol::get_dataKind](../../debugger/debug-interface-access/idiasymbol-get-datakind.md)