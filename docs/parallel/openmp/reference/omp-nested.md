---
title: "OMP_NESTED"
ms.custom: na
ms.date: "12/03/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: na
ms.suite: na
ms.technology: 
  - "devlang-cpp"
ms.tgt_pltfrm: na
ms.topic: "article"
f1_keywords: 
  - "OMP_NESTED"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "OMP_NESTED OpenMP environment variable"
ms.assetid: c43f5287-a548-40d0-bd54-0c6b2b9f9a53
caps.latest.revision: 10
caps.handback.revision: "10"
ms.author: "mblome"
manager: "ghogen"
---
# OMP_NESTED
[!INCLUDE[vs2017banner](../../../assembler/inline/includes/vs2017banner.md)]

Gibt an, ob geschachtelter Parallelität aktiviert ist, es sei denn, geschachtelter Parallelität mit `omp_set_nested`aktiviert oder deaktiviert wird.  
  
## Syntax  
  
```  
set OMP_NESTED[=TRUE | =FALSE]  
```  
  
## Hinweise  
 Die `OMP_NESTED` Umgebungsvariable kann über die [omp\_set\_nested](../../../parallel/openmp/reference/omp-set-nested.md)\-Funktion überschrieben werden.  
  
 Der Standardwert in der Visual C\+\+\-Implementierung des OpenMP\-Standards ist `OMP_DYNAMIC=FALSE`.  
  
 Weitere Informationen finden Sie unter [4.4 OMP\_NESTED](../../../parallel/openmp/4-4-omp-nested.md).  
  
## Beispiel  
 Mit dem folgenden Befehl wird die `OMP_NESTED` Umgebungsvariable fest, um AUSZURICHTEN:  
  
```  
set OMP_NESTED=TRUE  
```  
  
 Der folgende Befehl zeigt die aktuelle Einstellung der `OMP_NESTED` Umgebungsvariablen an:  
  
```  
set OMP_NESTED  
```  
  
## Siehe auch  
 [Environment Variables](../../../parallel/openmp/reference/openmp-environment-variables.md)