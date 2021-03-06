---
title: Compilerwarnung (Stufe 1) C4441 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C4441
dev_langs:
- C++
helpviewer_keywords:
- C4441
ms.assetid: 7fc540a5-e41f-47cf-aa37-b2b699c2685e
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 6c2abf64be0e9b80bb4158b0ed163906adc09945
ms.sourcegitcommit: 76b7653ae443a2b8eb1186b789f8503609d6453e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/04/2018
---
# <a name="compiler-warning-level-1-c4441"></a>Compilerwarnung (Stufe 1) C4441
Aufrufkonvention von 'cc1' ignoriert. 'cc2' stattdessen verwendet  
  
 Memberfunktionen im verwalteten benutzerdefinierten Typen und Generika globale Funktion verwenden, müssen die [__clrcall](../../cpp/clrcall.md) Aufrufkonvention.  Der Compiler verwendet `__clrcall`.  
  
## <a name="example"></a>Beispiel  
 Im folgenden Beispiel wird C4441 generiert.  
  
```  
// C4441.cpp  
// compile with: /clr /W1 /c  
generic <class ItemType>  
void __cdecl Test(ItemType item) {}   // C4441  
// try the following line instead  
// void Test(ItemType item) {}  
  
ref struct MyStruct {  
   void __cdecl Test(){}   // C4441  
   void Test2(){}   // OK  
};  
```