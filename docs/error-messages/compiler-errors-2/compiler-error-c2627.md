---
title: "Compilerfehler C2627 | Microsoft Docs"
ms.custom: ""
ms.date: "11/04/2016"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-cpp"
ms.tgt_pltfrm: ""
ms.topic: "error-reference"
f1_keywords: 
  - "C2627"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "C2627"
ms.assetid: 7fc6c5ac-c7c9-4f0b-ad52-f52252526458
caps.latest.revision: 9
author: "corob-msft"
ms.author: "corob"
manager: "ghogen"
caps.handback.revision: 9
---
# Compilerfehler C2627
[!INCLUDE[vs2017banner](../../assembler/inline/includes/vs2017banner.md)]

'Funktion': Memberfunktion ist in einer anonymen Union nicht zulässig  
  
 In einer [anonymen Union](../../misc/anonymous-unions.md) sind keine Memberfunktionen zulässig.  
  
 Im folgenden Beispiel wird C2627 generiert:  
  
```  
// C2627.cpp  
int main() {  
   union { void f(){} };   // C2627  
   union X { void f(){} };  
}  
```