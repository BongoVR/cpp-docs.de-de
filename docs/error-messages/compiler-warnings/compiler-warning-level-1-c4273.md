---
title: "Compilerwarnung (Stufe 1) C4273 | Microsoft Docs"
ms.custom: ""
ms.date: "11/04/2016"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-cpp"
ms.tgt_pltfrm: ""
ms.topic: "error-reference"
f1_keywords: 
  - "C4273"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "C4273"
ms.assetid: cc18611d-9454-40a4-ad73-69823d5888fb
caps.latest.revision: 9
author: "corob-msft"
ms.author: "corob"
manager: "ghogen"
caps.handback.revision: 9
---
# Compilerwarnung (Stufe 1) C4273
[!INCLUDE[vs2017banner](../../assembler/inline/includes/vs2017banner.md)]

'Funktion': Inkonsistente DLL\-Bindung  
  
 Zwei Definitionen innerhalb einer Datei unterscheiden sich hinsichtlich der Verwendung von [dllimport](../../cpp/dllexport-dllimport.md).  
  
## Beispiel  
 Im folgenden Beispiel wird C4273 generiert.  
  
```  
// C4273.cpp  
// compile with: /W1 /c  
char __declspec(dllimport) c;  
char c;   // C4273, delete this line or the line above to resolve  
```  
  
## Beispiel  
 Im folgenden Beispiel wird C4273 generiert.  
  
```  
// C4273_b.cpp  
// compile with: /W1 /clr /c  
#include <stdio.h>  
extern "C" int printf_s(const char *, ...);   // C4273  
```