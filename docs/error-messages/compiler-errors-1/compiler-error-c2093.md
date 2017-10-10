---
title: Compiler-Fehler C2093 generiert | Microsoft Docs
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- cpp-tools
ms.tgt_pltfrm: 
ms.topic: error-reference
f1_keywords:
- C2093
dev_langs:
- C++
helpviewer_keywords:
- C2093
ms.assetid: 17529a70-9169-46b5-9fc6-57a5ce224e6a
caps.latest.revision: 9
author: corob-msft
ms.author: corob
manager: ghogen
ms.translationtype: MT
ms.sourcegitcommit: 35b46e23aeb5f4dbfd2a0dd44b906389dd5bfc88
ms.openlocfilehash: 329c5250067c1d7db275326c6a3debb73d389cf6
ms.contentlocale: de-de
ms.lasthandoff: 10/09/2017

---
# <a name="compiler-error-c2093"></a>Compiler-Fehler C2093 generiert
'variable1': kann nicht mit der Adresse der automatischen Variablen 'variable2' initialisiert werden  
  
 Beim Kompilieren mit ["/ Za"](../../build/reference/za-ze-disable-language-extensions.md), das Programm versucht, die Adresse einer automatischen Variablen als Initialisierer zu verwenden.  
  
 Im folgende Beispiel wird C2093 generiert:  
  
```  
// C2093.c  
// compile with: /Za /c  
void func() {  
   int li;   // an implicit auto variable  
   int * s[]= { &li };   // C2093 address is not a constant  
  
   // OK  
   static int li2;  
   int * s2[]= { &li2 };  
}  
```
