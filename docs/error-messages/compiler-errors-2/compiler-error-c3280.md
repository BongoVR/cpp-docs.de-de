---
title: Compilerfehler C3280 | Microsoft Docs
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- cpp-tools
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- C3280
dev_langs:
- C++
helpviewer_keywords:
- C3280
ms.assetid: 86dc5bbc-8818-4786-a728-9334268d308b
caps.latest.revision: 8
author: corob-msft
ms.author: corob
manager: ghogen
ms.translationtype: MT
ms.sourcegitcommit: 35b46e23aeb5f4dbfd2a0dd44b906389dd5bfc88
ms.openlocfilehash: 4534ac1df55ed5e0810cd0a8d5ce54a5081b929e
ms.contentlocale: de-de
ms.lasthandoff: 10/10/2017

---
# <a name="compiler-error-c3280"></a>Compilerfehler C3280
"Klasse": Eine Memberfunktion eines verwalteten Typs kann nicht als eine nicht verwaltete Funktion kompiliert werden  
  
 Es ist nicht möglich, Memberfunktionen mit verwalteten Klassen als nicht verwaltete Funktionen zu kompilieren.  
  
 Im folgenden Beispiel wird C3280 generiert:  
  
```  
// C3280_2.cpp  
// compile with: /clr  
ref struct A {  
   void func();  
};  
  
#pragma managed(push,off)  
  
void A::func()   // C3280  
{  
}  
  
#pragma managed(pop)  
```  

