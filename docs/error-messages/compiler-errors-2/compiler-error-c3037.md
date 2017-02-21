---
title: "Compilerfehler C3037 | Microsoft Docs"
ms.custom: ""
ms.date: "11/04/2016"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-csharp"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "C3037"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "C3037"
ms.assetid: 9ba8a890-d3c7-4cce-93c5-d358e2bfad28
caps.latest.revision: 7
author: "corob-msft"
ms.author: "corob"
manager: "ghogen"
caps.handback.revision: 7
---
# Compilerfehler C3037
[!INCLUDE[vs2017banner](../../assembler/inline/includes/vs2017banner.md)]

"var": Variable in reduction\-Klausel muss im übergeordneten Kontext freigegeben sein.  
  
 Eine in einer [reduction](../../parallel/openmp/reference/reduction.md)\-Klausel angegebene Variable darf nicht für jeden Thread im Kontext privat sein.  
  
 Im folgenden Beispiel wird C3037 generiert:  
  
```  
// C3037.cpp // compile with: /openmp /c int g_i; int main() { int i; #pragma omp parallel private(g_i) // try the following line instead // #pragma omp parallel { #pragma omp for reduction(+:g_i)   // C3037 for (i = 0 ; i < 10 ; ++i) { g_i += i; } } }  
```