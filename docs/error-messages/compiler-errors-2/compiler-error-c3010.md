---
title: "Compilerfehler C3010 | Microsoft Docs"
ms.custom: ""
ms.date: "11/04/2016"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-csharp"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "C3010"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "C3010"
ms.assetid: e959d038-bba6-432a-9c0a-0470474de7d9
caps.latest.revision: 6
author: "corob-msft"
ms.author: "corob"
manager: "ghogen"
caps.handback.revision: 6
---
# Compilerfehler C3010
[!INCLUDE[vs2017banner](../../assembler/inline/includes/vs2017banner.md)]

'Bezeichnung': Aussprung aus strukturiertem Block von OpenMP ist nicht zulässig.  
  
 Code kann nicht in einen oder aus einem OpenMP\-Block springen.  
  
 Im folgenden Beispiel wird C3010 generiert:  
  
```  
// C3010.c // compile with: /openmp int main() { #pragma omp parallel { #pragma omp parallel { goto lbl3; } } lbl3:;   // C3010 }  
```