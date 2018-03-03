---
title: Compilerfehler C2577 | Microsoft Docs
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- cpp-tools
ms.tgt_pltfrm: 
ms.topic: error-reference
f1_keywords:
- C2577
dev_langs:
- C++
helpviewer_keywords:
- C2577
ms.assetid: fc79ef83-8362-40a2-9257-8037c3195ce4
caps.latest.revision: 
author: corob-msft
ms.author: corob
manager: ghogen
ms.workload:
- cplusplus
ms.openlocfilehash: c2d48df0ef5d4c5a4dff649a54132e75969d92e6
ms.sourcegitcommit: 8fa8fdf0fbb4f57950f1e8f4f9b81b4d39ec7d7a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/21/2017
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