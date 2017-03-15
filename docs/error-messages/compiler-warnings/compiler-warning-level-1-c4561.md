---
title: "Compilerwarnung (Stufe 1) C4561 | Microsoft Docs"
ms.custom: ""
ms.date: "11/04/2016"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-cpp"
ms.tgt_pltfrm: ""
ms.topic: "error-reference"
f1_keywords: 
  - "C4561"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "C4561"
ms.assetid: 3a10c12c-601b-4b6c-9861-331fd022e021
caps.latest.revision: 9
author: "corob-msft"
ms.author: "corob"
manager: "ghogen"
caps.handback.revision: 9
---
# Compilerwarnung (Stufe 1) C4561
[!INCLUDE[vs2017banner](../../assembler/inline/includes/vs2017banner.md)]

"\_\_fastcall" ist mit dem "\/CLR"\-Schalter inkompatibel: Konvertierung nach "\_\_stdcall" erfolgt  
  
 Die Aufrufkonvention der [\_\_fastcall](../../cpp/fastcall.md)\-Funktion kann nicht mit der [\/clr](../../build/reference/clr-common-language-runtime-compilation.md)\-Compileroption verwendet werden.  Der Compiler ignoriert die Aufrufe von `__fastcall`.  Um die Warnung zu vermeiden, entfernen Sie entweder die **\_\_fastcall** \-Aufrufe oder führen die Kompilierung ohne **\/clr** durch.  
  
 Im folgenden Beispiel wird C4561 generiert:  
  
```  
// C4561.cpp  
// compile with: /clr /W1 /c  
// processor: x86  
void __fastcall Func(void *p);   // C4561, remove __fastcall to resolve  
```