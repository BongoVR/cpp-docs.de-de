---
title: Compilerfehler C3463 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C3463
dev_langs:
- C++
helpviewer_keywords:
- C3463
ms.assetid: 153efcc0-085c-4615-84ea-d22942618bdf
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: ff9b680fb034a113627bcaecae8ba3cfc442f45e
ms.sourcegitcommit: 76b7653ae443a2b8eb1186b789f8503609d6453e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/04/2018
---
# <a name="compiler-error-c3463"></a>Compilerfehler C3463
"Typ": Der Typ ist im implements-Attribut nicht zulässig.  
  
 Ein ungültiger Typ wurde an das [implements](../../windows/implements-cpp.md) -Attribut übergeben. Beispielsweise können Sie eine Schnittstelle an `implements`übergeben, Sie können aber keinen Zeiger an eine Schnittstelle übergeben.  
  
## <a name="example"></a>Beispiel  
 Im folgenden Beispiel wird C3463 generiert:  
  
```  
// C3463.cpp  
// compile with: /c  
#include <windows.h>  
[object, uuid("00000000-0000-0000-0000-000000000001")]  
__interface X {};  
  
typedef X* PX;  
  
[ coclass, uuid("00000000-0000-0000-0000-000000000002"), implements(interfaces=PX) ]   // C3463  
// try the following line instead  
// [ coclass, uuid("00000000-0000-0000-0000-000000000002"), implements(interfaces=X) ]  
class CMyClass : public X {};  
```