---
title: _com_error::Source | Microsoft Docs
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- cpp-language
ms.tgt_pltfrm: 
ms.topic: language-reference
f1_keywords:
- _com_error::Source
dev_langs:
- C++
helpviewer_keywords:
- Source method [C++]
ms.assetid: 55353741-fabc-4b0c-9787-b5a69bb189f2
caps.latest.revision: 6
author: mikeblome
ms.author: mblome
manager: ghogen
ms.translationtype: HT
ms.sourcegitcommit: 6ffef5f51e57cf36d5984bfc43d023abc8bc5c62
ms.openlocfilehash: 848d402e83c09ff85537115437c8a190d160f984
ms.contentlocale: de-de
ms.lasthandoff: 09/25/2017

---
# <a name="comerrorsource"></a>_com_error::Source
**Microsoft-spezifisch**  
  
 Aufrufe **IErrorInfo:: GetSource** Funktion.  
  
## <a name="syntax"></a>Syntax  
  
```  
  
_bstr_t Source() const;  
  
```  
  
## <a name="return-value"></a>Rückgabewert  
 Gibt das Ergebnis der **IErrorInfo:: GetSource** für die **IErrorInfo** -Objekt erfasst wird, innerhalb der `_com_error` Objekt. Das resultierende BSTR wird in einem `_bstr_t`-Objekt gekapselt. Wenn kein **IErrorInfo** wird aufgezeichnet, es gibt ein leeres `_bstr_t`.  
  
## <a name="remarks"></a>Hinweise  
 Jeder Fehler beim Aufrufen der **IErrorInfo:: GetSource** -Methode wird ignoriert.  
  
 **Ende Microsoft-spezifisch**  
  
## <a name="see-also"></a>Siehe auch  
 [_com_error-Klasse](../cpp/com-error-class.md)
