---
title: 'Idiasourcefile:: Get_checksumtype |Microsoft 文档'
ms.custom: ''
ms.date: 11/04/2016
ms.technology: vs-ide-debug
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- IDiaSourceFile::get_checksumType method
ms.assetid: 4c363e61-a6a9-409a-9cc0-d06eb2bee645
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 83d1aa687ec7f19df61031d4ff334751ccabaebd
ms.sourcegitcommit: 3d10b93eb5b326639f3e5c19b9e6a8d1ba078de1
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/18/2018
ms.locfileid: "31461926"
---
# <a name="idiasourcefilegetchecksumtype"></a>IDiaSourceFile::get_checksumType
检索的校验和类型。  
  
## <a name="syntax"></a>语法  
  
```C++  
HRESULT get_checksumType (   
   DWORD* pRetVal  
);  
```  
  
#### <a name="parameters"></a>参数  
 `pRetVal`  
 [out]返回校验和类型。  
  
## <a name="return-value"></a>返回值  
 如果成功，则返回`S_OK`; 否则为返回错误代码。  
  
## <a name="remarks"></a>备注  
 校验和类型是一个值，可以映射到校验和算法。 例如，标准的 PDB 文件格式可以通常具有以下值之一：  
  
|校验和类型|CryptoAPI 标签|描述|  
|-------------------|---------------------|-----------------|  
|0|\<无 >|不存在的校验和。|  
|1|`CALG_MD5`|使用 MD5 哈希算法生成的校验和。|  
|2|`CALG_SHA1`|使用 SHA1 哈希算法生成的校验和。|  
  
 `CryptoAPI`标签是从`ALG_ID`枚举。 哈希算法的详细信息，请查阅`CryptoAPI`部分 Microsoft [!INCLUDE[winsdkshort](../../debugger/debug-interface-access/includes/winsdkshort_md.md)]。  
  
 若要获取源代码文件的实际校验和字节，调用[idiasourcefile:: Get_checksum](../../debugger/debug-interface-access/idiasourcefile-get-checksum.md)方法。  
  
## <a name="see-also"></a>请参阅  
 [IDiaSourceFile](../../debugger/debug-interface-access/idiasourcefile.md)   
 [IDiaSourceFile::get_checksum](../../debugger/debug-interface-access/idiasourcefile-get-checksum.md)