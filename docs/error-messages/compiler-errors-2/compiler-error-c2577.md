---
title: Compilerfehler C2577 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2577
dev_langs:
- C++
helpviewer_keywords:
- C2577
ms.assetid: fc79ef83-8362-40a2-9257-8037c3195ce4
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: af4fb6d5a2d7621df1b11e9040ca7dd4f5551289
ms.sourcegitcommit: 76b7653ae443a2b8eb1186b789f8503609d6453e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/04/2018
---
# <a name="compiler-error-c2577"></a>Compilerfehler C2577
'Member': Destruktor/Finalizer kann einen Rückgabetyp haben  
  
 Einen Destruktor oder Finalizer kann keinen Wert von zurückgeben `void` oder eines anderen Typs. Entfernen Sie die `return` Anweisung aus der Destruktordefinition.  
  
## <a name="example"></a>Beispiel  
 Im folgende Beispiel wird C2577 generiert.  
  
```  
// C2577.cpp  
// compile with: /c  
class A {  
public:  
   A() {}  
   ~A(){  
      return 0;   // C2577  
   }  
};  
```