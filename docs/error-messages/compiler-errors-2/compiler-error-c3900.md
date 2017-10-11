---
title: Compilerfehler C3900 | Microsoft Docs
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- cpp-tools
ms.tgt_pltfrm: 
ms.topic: error-reference
f1_keywords:
- C3900
dev_langs:
- C++
helpviewer_keywords:
- C3900
ms.assetid: a94cc561-8fa8-4344-9e01-e81ff462fae5
caps.latest.revision: 8
author: corob-msft
ms.author: corob
manager: ghogen
ms.translationtype: MT
ms.sourcegitcommit: 35b46e23aeb5f4dbfd2a0dd44b906389dd5bfc88
ms.openlocfilehash: 29a2210ec372de6f752091a8eb13a4e5eb4f4aa7
ms.contentlocale: de-de
ms.lasthandoff: 10/10/2017

---
# <a name="compiler-error-c3900"></a>Compilerfehler C3900
'Member': im aktuellen Bereich nicht zulässig.  
  
 Eigenschaftenblöcken können Funktionsdeklarationen und Inlinefunktionsdefinitionen nur enthalten. Keine Member als Funktionen sind in Eigenschaftenblöcken zulässig. Keine Typdefinitionen, Operatoren oder Friend-Funktionen sind zulässig. Weitere Informationen finden Sie unter [property](../../windows/property-cpp-component-extensions.md).  
  
 Ereignisdefinitionen können nur über Zugriffsmethoden und Funktionen enthalten.  
  
 Im folgende Beispiel wird C3900 generiert:  
  
```  
// C3900.cpp  
// compile with: /clr  
ref class X {  
   property int P {  
      void set(int);   // OK  
      int i;   // C3900 variable declaration  
   };  
};  
```  
  
 Im folgende Beispiel wird C3900 generiert:  
  
```  
// C3900b.cpp  
// compile with: /clr  
using namespace System;  
delegate void H();  
ref class X {  
   event H^ E {  
      int m;   // C3900  
  
      // OK  
      void Test() {}  
  
      void add( H^ h ) {}  
      void remove( H^ h ) {}  
      void raise( ) {}  
   }  
};  
```
