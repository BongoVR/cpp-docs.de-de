---
title: "Compilerfehler C2275"
ms.custom: na
ms.date: "12/03/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: na
ms.suite: na
ms.technology: 
  - "devlang-cpp"
ms.tgt_pltfrm: na
ms.topic: "error-reference"
f1_keywords: 
  - "C2275"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "C2275"
ms.assetid: c1eafa71-48de-46e0-82f3-b575538ef205
caps.latest.revision: 7
caps.handback.revision: "7"
ms.author: "corob"
manager: "ghogen"
---
# Compilerfehler C2275
[!INCLUDE[vs2017banner](../../assembler/inline/includes/vs2017banner.md)]

'Bezeichner': Ungültige Verwendung dieses Typs als Ausdruck  
  
 In einem Ausdruck wird der Operator `->` mit einem `typedef`\-Bezeichner verwendet.  
  
 Im folgenden Beispiel wird C2275 generiert:  
  
```  
// C2275.cpp  
typedef struct S {  
    int mem;  
} *S_t;  
void func1( int *parm );  
void func2() {  
    func1( &S_t->mem );   // C2275, S_t is a typedef  
}  
```