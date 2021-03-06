---
title: 'Srwlocksharedtraits:: Unlock-Methode | Microsoft Docs'
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-windows
ms.topic: reference
f1_keywords:
- corewrappers/Microsoft::WRL::Wrappers::HandleTraits::SRWLockSharedTraits::Unlock
dev_langs:
- C++
helpviewer_keywords:
- Unlock method
ms.assetid: 33cdead9-1900-4094-b18e-38fcf1a0bd28
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- uwp
ms.openlocfilehash: 95be5ae4c9db7bff4ecbfb4705904f4e48c160e0
ms.sourcegitcommit: d55ac596ba8f908f5d91d228dc070dad31cb8360
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/08/2018
---
# <a name="srwlocksharedtraitsunlock-method"></a>SRWLockSharedTraits::Unlock-Methode
Gibt die exklusive Kontrolle über das angegebene SRWLock-Objekt frei.  
  
## <a name="syntax"></a>Syntax  
  
```  
inline static void Unlock(  
   _In_ Type srwlock  
);  
```  
  
#### <a name="parameters"></a>Parameter  
 `srwlock`  
 Ein Handle für ein SRWLock-Objekt.  
  
## <a name="return-value"></a>Rückgabewert  
  
## <a name="requirements"></a>Anforderungen  
 **Header:** corewrappers.h  
  
 **Namespace:** Microsoft::WRL::Wrappers::HandleTraits  
  
## <a name="see-also"></a>Siehe auch  
 [SRWLockSharedTraits-Struktur](../windows/srwlocksharedtraits-structure.md)