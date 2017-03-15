---
title: "Compilerfehler C3060 | Microsoft Docs"
ms.custom: ""
ms.date: "11/04/2016"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-csharp"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "C3060"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "C3060"
ms.assetid: 6282bb92-0546-4b59-9435-d3840bf93bdb
caps.latest.revision: 6
author: "corob-msft"
ms.author: "corob"
manager: "ghogen"
caps.handback.revision: 6
---
# Compilerfehler C3060
[!INCLUDE[vs2017banner](../../assembler/inline/includes/vs2017banner.md)]

'Member': Eine Friend\-Funktion kann nicht mit einem qualifizierten Namen innerhalb einer Klasse definiert werden \(sie kann nur deklariert werden\).  
  
 Eine Friend\-Funktion wurde mit einem qualifizierten Namen definiert. Das ist nicht zulässig.  
  
 Im folgenden Beispiel wird C3060 generiert:  
  
```  
// C3060.cpp class A { public: void func(); }; class C { public: friend void A::func() { }   // C3060 // Try the following line and the out of class definition: // friend void A::func(); }; // void A::func(){}  
```