---
title: Compilerfehler C2387 | Microsoft Docs
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- cpp-tools
ms.tgt_pltfrm: 
ms.topic: error-reference
f1_keywords:
- C2387
dev_langs:
- C++
helpviewer_keywords:
- C2387
ms.assetid: 6847b8e1-ffac-458d-ab88-0c92f72f2527
caps.latest.revision: 8
author: corob-msft
ms.author: corob
manager: ghogen
ms.translationtype: MT
ms.sourcegitcommit: 35b46e23aeb5f4dbfd2a0dd44b906389dd5bfc88
ms.openlocfilehash: 18233efc81a63a29c1350d1addb67f8ea20e877e
ms.contentlocale: de-de
ms.lasthandoff: 10/09/2017

---
# <a name="compiler-error-c2387"></a>Compilerfehler C2387
'Typ': mehrdeutige Basisklasse  
  
 Der Compiler konnte nicht eindeutig einen Funktionsaufruf auflösen, da die Funktion in mehr als einer Basisklasse vorhanden ist.  
  
 Um diesen Fehler zu beheben, entfernen Sie eine der Basisklassen aus der Vererbung, oder qualifizieren Sie den Funktionsaufruf explizit zu.  
  
 Im folgende Beispiel wird C2387 generiert:  
  
```  
// C2387.cpp  
namespace N1 {  
   struct B {  
      virtual void f() {  
      }  
   };  
}  
  
namespace N2 {  
   struct B {  
      virtual void f() {  
      }  
   };  
}  
  
struct D : N1::B, N2::B {  
   virtual void f() {  
      B::f();   // C2387  
      // try the following line instead  
      // N1::B::f();  
   }  
};  
  
int main() {  
   D aD;  
   aD.f();  
}  
```
