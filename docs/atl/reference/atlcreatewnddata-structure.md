---
title: _AtlCreateWndData Struktur | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-atl
ms.topic: reference
f1_keywords:
- ATL::_AtlCreateWndData
- ATL._AtlCreateWndData
- _AtlCreateWndData
dev_langs:
- C++
helpviewer_keywords:
- _AtlCreateWndData structure
- AtlCreateWndData structure
ms.assetid: 76ed5382-bfbf-4b8b-8a29-912688dfd2ae
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: cc8bf88ce5258dc36a06f32ebaa5e2cdf15092fc
ms.sourcegitcommit: be2a7679c2bd80968204dee03d13ca961eaa31ff
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/03/2018
---
# <a name="atlcreatewnddata-structure"></a>_AtlCreateWndData-Struktur
Diese Struktur enthält die Klasse Instanzdaten im Windowing Code in ATL  
  
## <a name="syntax"></a>Syntax  
  
```
    struct _AtlCreateWndData{
    void* m_pThis;
    DWORD m_dwThreadID;
    _AtlCreateWndData* m_pNext;
};
```  
  
## <a name="members"></a>Member  
 **m_pThis**  
 Die **dies** Zeiger verwendet, um den Zugriff auf die Klasseninstanz in Fensterprozeduren abzurufen.  
  
 `m_dwThreadID`  
 Die Thread-ID der aktuellen Klasseninstanz.  
  
 **m_pNext**  
 Zeiger auf die nächste `_AtlCreateWndData` Objekt.  
  
## <a name="requirements"></a>Anforderungen  
 **Header:** atlbase.h  
  
## <a name="see-also"></a>Siehe auch  
 [Strukturen](../../atl/reference/atl-structures.md)





