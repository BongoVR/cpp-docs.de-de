---
title: 'Handlenulltraits:: Close-Methode | Microsoft Docs'
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-windows
ms.topic: reference
f1_keywords:
- corewrappers/Microsoft::WRL::Wrappers::HandleTraits::HANDLENullTraits::Close
dev_langs:
- C++
helpviewer_keywords:
- Close method
ms.assetid: 6fb2fa0d-df20-45dc-856f-f78497f8bdf9
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- uwp
ms.openlocfilehash: a1319b6a75f92e057975d0f8d2c7e2753df47141
ms.sourcegitcommit: d55ac596ba8f908f5d91d228dc070dad31cb8360
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/08/2018
---
# <a name="handlenulltraitsclose-method"></a>HANDLENullTraits::Close-Methode
Schließt das angegebene Handle.  
  
## <a name="syntax"></a>Syntax  
  
```  
inline static bool Close(  
   _In_ Type h  
);  
```  
  
#### <a name="parameters"></a>Parameter  
 `h`  
 Das Handle zu schließen.  
  
## <a name="return-value"></a>Rückgabewert  
 **"true"** Wenn behandeln `h` geschlossen erfolgreich ist, andernfalls **"false"**.  
  
## <a name="requirements"></a>Anforderungen  
 **Header:** corewrappers.h  
  
 **Namespace:** Microsoft::WRL::Wrappers::HandleTraits  
  
## <a name="see-also"></a>Siehe auch  
 [HANDLENullTraits-Struktur](../windows/handlenulltraits-structure.md)