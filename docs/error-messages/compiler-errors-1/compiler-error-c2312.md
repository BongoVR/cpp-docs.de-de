---
title: Compilerfehler C2312 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2312
dev_langs:
- C++
helpviewer_keywords:
- C2312
ms.assetid: c8bcfd06-12c1-4323-bb53-ba392d36daa4
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: ba85254d32ef6b92266d0556aa7f5eb760f1835e
ms.sourcegitcommit: 76b7653ae443a2b8eb1186b789f8503609d6453e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/04/2018
---
# <a name="compiler-error-c2312"></a>Compilerfehler C2312
"Ausnahme1": wurde aufgefangen durch "Ausnahme2" in Zeilennummer  
  
 Derselbe Ausnahmetyp wird durch zwei Handler aufgefangen.  
  
 Im folgenden Beispiel wird C2312 generiert:  
  
```  
// C2312.cpp  
// compile with: /EHsc  
#include <eh.h>  
int main() {  
    try {  
        throw "ooops!";  
    }  
    catch( signed int ) {}  
    catch( int ) {}   // C2312  
}  
```