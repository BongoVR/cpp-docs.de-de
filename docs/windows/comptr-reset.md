---
title: ComPtr::Reset | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-windows
ms.topic: reference
dev_langs:
- C++
ms.assetid: aa6a46f7-f56b-4fd5-add0-7cea55f7abda
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- uwp
ms.openlocfilehash: dd2ce820367b15cb5dad8baf691a835499457a55
ms.sourcegitcommit: d55ac596ba8f908f5d91d228dc070dad31cb8360
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/08/2018
---
# <a name="comptrreset"></a>ComPtr::Reset
Gibt alle Verweise für den Zeiger auf die Schnittstelle an, die diesem ComPtr zugeordnet ist.  
  
## <a name="syntax"></a>Syntax  
  
```  
unsigned long Reset();  
```  
  
## <a name="return-value"></a>Rückgabewert  
 Die Anzahl der freigegeben Verweise, sofern vorhanden.  
  
## <a name="requirements"></a>Anforderungen  
 **Header:** client.h  
  
 **Namespace:** Microsoft::WRL  
  
## <a name="see-also"></a>Siehe auch  
 [ComPtr-Klasse](../windows/comptr-class.md)