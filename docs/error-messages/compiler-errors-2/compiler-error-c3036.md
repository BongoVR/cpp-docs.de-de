---
title: "Compilerfehler C3036"
ms.custom: na
ms.date: "12/03/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: na
ms.suite: na
ms.technology: 
  - "devlang-csharp"
ms.tgt_pltfrm: na
ms.topic: "article"
f1_keywords: 
  - "C3036"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "C3036"
ms.assetid: 10c6993e-bc42-4a07-85c7-cdc34ac30906
caps.latest.revision: 7
caps.handback.revision: "7"
ms.author: "corob"
manager: "ghogen"
---
# Compilerfehler C3036
[!INCLUDE[vs2017banner](../../assembler/inline/includes/vs2017banner.md)]

"Operator": Ungültiges Operatortoken in der "reduction"\-Klausel von OpenMP.  
  
 Eine [reduction](../../parallel/openmp/reference/reduction.md)\-Klausel wurde nicht ordnungsgemäß angegeben.  
  
 Im folgenden Beispiel wird C3036 generiert:  
  
```  
// C3036.cpp // compile with: /openmp static float a[1000], b[1000], c[1000]; void test1(int first, int last) { static float dp = 0.0f; #pragma omp for nowait reduction(.:dp)   // C3036 // try the following line instead // #pragma omp for nowait reduction(+: dp) for (int i = first ; i <= last ; ++i) dp += a[i] * b[i]; }  
```