---
title: "Compilerwarnung (Stufe 1) C4155 | Microsoft Docs"
ms.custom: ""
ms.date: "11/04/2016"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-csharp"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "C4155"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "C4155"
ms.assetid: ba233353-09e3-4195-8127-13a27ddd8d70
caps.latest.revision: 7
author: "corob-msft"
ms.author: "corob"
manager: "ghogen"
caps.handback.revision: 7
---
# Compilerwarnung (Stufe 1) C4155
[!INCLUDE[vs2017banner](../../assembler/inline/includes/vs2017banner.md)]

Löschen eines Arrayausdrucks ohne Verwendung der Arrayform von "delete"  
  
 Die Arrayform von **delete** sollte zum Löschen eines Arrays verwendet werden. Diese Warnung tritt nur unter der ANSI\-Kompatibilität \(\/Za\) auf.  
  
## Beispiel  
 Im folgenden Beispiel wird C4155 generiert:  
  
```  
// C4155.cpp // compile with: /Za /W1 #include <stdio.h> int main(void) { int (*array)[ 10 ] = new int[ 5 ] [ 10 ]; array[0][0] = 8; printf_s("%d\n", array[0][0]); delete array;   // C4155 // try the following line instead // delete [] array;   // C4155 }  
```