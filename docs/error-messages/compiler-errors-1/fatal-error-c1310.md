---
title: Schwerwiegender Fehler C1310 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C1310
dev_langs:
- C++
helpviewer_keywords:
- C1310
ms.assetid: ac48aa51-8023-42fe-b844-3f8bf228fbef
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: c226b61dd722eb4ed32de6c8885c575b64ba2448
ms.sourcegitcommit: 76b7653ae443a2b8eb1186b789f8503609d6453e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/04/2018
---
# <a name="fatal-error-c1310"></a>Schwerwiegender Fehler C1310
Profilgesteuerte Optimierungen sind bei OpenMP nicht verfügbar.  
  
 Sie sind nicht in der Lage, ein Modul mit [/LTCG: PGI](../../build/reference/ltcg-link-time-code-generation.md) zu verknüpfen, das mit [/GL](../../build/reference/gl-whole-program-optimization.md)kompiliert wurde.  
  
 Das folgende Beispiel generiert C1310:  
  
```  
// C1310.cpp  
// compile with: /openmp /GL /link /LTCG:PGI  
// C1310 expected  
int main()  
{  
   int i = 0, j = 10;  
  
   #pragma omp parallel  
   {  
      #pragma omp for  
      for (i = 0; i < 0; i++)   
         --j;  
   }  
}  
```