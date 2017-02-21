---
title: "Compilerfehler C3003 | Microsoft Docs"
ms.custom: ""
ms.date: "11/04/2016"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-csharp"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "C3003"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "C3003"
ms.assetid: 22e74f99-bb7f-4518-ab0d-934d5d49bcc7
caps.latest.revision: 6
author: "corob-msft"
ms.author: "corob"
manager: "ghogen"
caps.handback.revision: 6
---
# Compilerfehler C3003
[!INCLUDE[vs2017banner](../../assembler/inline/includes/vs2017banner.md)]

'Direktive': Nach Direktivenklauseln ist kein OpenMP\-Direktivenname zulässig.  
  
 Ein OpenMP\-Direktivenname darf nicht auf eine OpenMP\-Direktivenklausel folgen.  
  
 Im folgenden Beispiel wird C3003 generiert:  
  
```  
// C3003.c // compile with: /openmp int main() { int x, y, z; #pragma omp parallel shared(x, y, z) for   // C3003 }  
```