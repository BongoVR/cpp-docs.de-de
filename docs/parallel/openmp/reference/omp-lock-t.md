---
title: "omp_lock_t | Microsoft Docs"
ms.custom: ""
ms.date: "11/04/2016"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-cpp"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "omp_lock_t"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "omp_lock_t OpenMP data type"
ms.assetid: 51b80629-4ffc-4b8a-95c7-1af048f1f286
caps.latest.revision: 7
author: "mikeblome"
ms.author: "mblome"
manager: "ghogen"
caps.handback.revision: 7
---
# omp_lock_t
[!INCLUDE[vs2017banner](../../../assembler/inline/includes/vs2017banner.md)]

Ein Typ, der den Status einer Sperre hält, ob die Sperre verfügbar wird oder wenn ein Thread eine Sperre besitzt.  
  
 Die folgende Funktion verwenden **omp\_lock\_t**:  
  
-   [omp\_init\_lock](../../../parallel/openmp/reference/omp-init-lock.md)  
  
-   [omp\_destroy\_lock](../../../parallel/openmp/reference/omp-destroy-lock.md)  
  
-   [omp\_set\_lock](../../../parallel/openmp/reference/omp-set-lock.md)  
  
-   [omp\_unset\_lock](../../../parallel/openmp/reference/omp-unset-lock.md)  
  
-   [omp\_test\_lock](../../../parallel/openmp/reference/omp-test-lock.md)  
  
 Weitere Informationen finden Sie unter [3.2 Lock Functions](../../../parallel/openmp/3-2-lock-functions.md).  
  
## Beispiel  
 Weitere Informationen finden Sie unter [omp\_init\_lock](../../../parallel/openmp/reference/omp-init-lock.md) als ein Beispiel für die Verwendung von **omp\_lock\_t**.  
  
## Siehe auch  
 [Data Types](../../../parallel/openmp/reference/openmp-data-types.md)