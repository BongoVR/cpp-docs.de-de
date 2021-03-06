---
title: 'CDynamicAccessor:: Getblobsizelimit | Microsoft Docs'
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-data
ms.topic: reference
f1_keywords:
- ATL::CDynamicAccessor::GetBlobSizeLimit
- CDynamicAccessor.GetBlobSizeLimit
- CDynamicAccessor::GetBlobSizeLimit
- GetBlobSizeLimit
- ATL.CDynamicAccessor.GetBlobSizeLimit
dev_langs:
- C++
helpviewer_keywords:
- GetBlobSizeLimit method
ms.assetid: 7131e7c4-6e05-42f3-9d87-110301b672f2
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- data-storage
ms.openlocfilehash: 860b186fc19bcec51c8f1ba3b7cc103b76f4b10d
ms.sourcegitcommit: 76b7653ae443a2b8eb1186b789f8503609d6453e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/04/2018
---
# <a name="cdynamicaccessorgetblobsizelimit"></a>CDynamicAccessor::GetBlobSizeLimit
Ruft die maximale BLOB-Größe in Bytes ab.  
  
## <a name="syntax"></a>Syntax  
  
```cpp
const DBLENGTH GetBlobSizeLimit() const;  
  
```  
  
## <a name="remarks"></a>Hinweise  
 Gibt die Behandlung von Wert BLOB `nBlobSize` entsprechend der Festlegung durch [SetBlobSizeLimit](../../data/oledb/cdynamicaccessor-setblobsizelimit.md).  
  
## <a name="requirements"></a>Anforderungen  
 **Header:** atldbcli.h  
  
## <a name="see-also"></a>Siehe auch  
 [CDynamicAccessor-Klasse](../../data/oledb/cdynamicaccessor-class.md)