---
title: "Compilerwarnung (Stufe 1) C4087 | Microsoft Docs"
ms.custom: ""
ms.date: "11/04/2016"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-csharp"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "C4087"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "C4087"
ms.assetid: 546e4d57-5c8e-422c-8ef1-92657336dad5
caps.latest.revision: 6
author: "corob-msft"
ms.author: "corob"
manager: "ghogen"
caps.handback.revision: 6
---
# Compilerwarnung (Stufe 1) C4087
[!INCLUDE[vs2017banner](../../assembler/inline/includes/vs2017banner.md)]

"Funktion": Mit "void"\-Parameterliste deklariert  
  
 Die Funktionsdeklaration hat keine formalen Parameter, aber der Funktionsaufruf hat tatsächlich Parameter. Zusätzliche Parameter werden entsprechend der Aufrufkonvention der Funktion übergeben.  
  
 Diese Warnung gilt für den C\-Compiler.  
  
## Beispiel  
  
```  
// C4087.c // compile with: /W1 int f1( void ) { } int main() { f1( 10 );   // C4087 }  
```