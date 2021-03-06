---
title: 'Idiasymbol:: Get_container |Microsoft 文档'
ms.custom: ''
ms.date: 11/04/2016
ms.technology: vs-ide-debug
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- IDiaSymbol::get_container method
ms.assetid: 24e832eb-80b3-484c-a41b-11477ec9de99
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: e4a04a505b694d5ed4081b12a39815256ed68d3e
ms.sourcegitcommit: 3d10b93eb5b326639f3e5c19b9e6a8d1ba078de1
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/18/2018
ms.locfileid: "31462907"
---
# <a name="idiasymbolgetcontainer"></a>IDiaSymbol::get_container
此函数可检索为表示此符号父/容器符号的指针。  
  
## <a name="syntax"></a>语法  
  
```C++  
HRESULT get_container(  
   IDiaSymbol **pRetVal  
);  
```  
  
#### <a name="parameters"></a>参数  
 `pRetVal`  
 [out]返回一个指向`IDiaSymbol`包含有关容器的此符号的信息。  
  
## <a name="return-value"></a>返回值  
 如果成功，返回，则为 S_OK;否则，返回 S_FALSE 或错误代码。  
  
> [!NOTE]
>  返回值为 S_FALSE 表示属性不是可用于符号。  
  
## <a name="requirements"></a>要求  
  
|需求|描述|  
|-----------------|-----------------|  
|标头：|dia2.h|  
|版本:|DIA SDK v8.0|  
  
## <a name="see-also"></a>请参阅  
 [IDiaSymbol](../../debugger/debug-interface-access/idiasymbol.md)