---
title: Compilerfehler C3645 | Microsoft Docs
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- cpp-tools
ms.tgt_pltfrm: 
ms.topic: error-reference
f1_keywords:
- C3645
dev_langs:
- C++
helpviewer_keywords:
- C3645
ms.assetid: 346da528-ae86-4cd0-9654-f41bee26ac0d
caps.latest.revision: 8
author: corob-msft
ms.author: corob
manager: ghogen
ms.translationtype: MT
ms.sourcegitcommit: 35b46e23aeb5f4dbfd2a0dd44b906389dd5bfc88
ms.openlocfilehash: 43bda10ee2e4f2939061d70cfcf19da950909d03
ms.contentlocale: de-de
ms.lasthandoff: 10/10/2017

---
# <a name="compiler-error-c3645"></a>Compilerfehler C3645
'Funktion': __clrcall kann nicht auf Funktionen in nativen Code kompiliert verwendet werden  
  
 Das Vorhandensein einiger Schlüsselwörter in einer Funktion führt dazu, dass die Funktion in systemeigenem Code kompiliert werden.  
  
## <a name="example"></a>Beispiel  
 Im folgende Beispiel wird C3645 generiert.  
  
```  
// C3645.cpp  
// compile with: /clr /c  
#pragma unmanaged   
int __clrcall dog() {}   // C3645  
```
