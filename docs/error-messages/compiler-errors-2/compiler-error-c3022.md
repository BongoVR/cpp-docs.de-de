---
title: "Compilerfehler C3022 | Microsoft Docs"
ms.custom: ""
ms.date: "11/04/2016"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-csharp"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "C3022"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "C3022"
ms.assetid: 9f1d444c-6c6e-48d9-9346-69128390aa33
caps.latest.revision: 7
author: "corob-msft"
ms.author: "corob"
manager: "ghogen"
caps.handback.revision: 7
---
# Compilerfehler C3022
[!INCLUDE[vs2017banner](../../assembler/inline/includes/vs2017banner.md)]

"clause": ungültiger Plantyp von "value" für die "directive"\-Direktive von OpenMP  
  
 Ein nicht unterstützter Wert wurde an eine Klausel übergeben.  
  
 Im folgenden Beispiel wird C3022 generiert.  
  
```  
// C3022.cpp // compile with: /openmp /link vcomps.lib #include <stdio.h> #include "omp.h" int main() { int i; #pragma omp parallel for schedule(10)   // C3022 for (i = 0; i < 10; ++i) ; #pragma omp parallel for schedule(x)   // C3022 for (i = 0; i < 10; ++i) ; // OK #pragma omp parallel for schedule(runtime) for (i = 0; i < 10; ++i) ; }  
```