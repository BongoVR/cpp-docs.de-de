---
title: Compilerwarnung (Stufe 1) C4822 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C4822
dev_langs:
- C++
helpviewer_keywords:
- C4822
ms.assetid: 0f231a30-2eb0-4722-aaa0-e2d19d3e7eea
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: d9491d522c65eba3599c3618d510c57b55682876
ms.sourcegitcommit: 76b7653ae443a2b8eb1186b789f8503609d6453e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/04/2018
---
# <a name="compiler-warning-level-1-c4822"></a>Compilerwarnung (Stufe 1) C4822
"Member": Lokale Klassenmemberfunktion enthält keinen Text.  
  
 Eine lokale Klassenmemberfunktion wurde deklariert, aber nicht in der Klasse definiert. Um eine lokale Klassenmemberfunktion verwenden zu können, müssen Sie sie in der Klasse definieren. Sie können Sie nicht in der Klasse deklarieren und außerhalb der Klasse definieren.  
  
 Jede Definition außerhalb der Klasse für eine lokale Klassenmemberfunktion erzeugt einen Fehler.  
  
 Im folgenden Beispiel wird C4822 generiert.  
  
```  
// C4822.cpp  
// compile with: /W1  
int main() {  
   struct C {  
      void func1(int);   // C4822  
      // try the following line instead  
      // void func1(int){}  
  };  
}  
```