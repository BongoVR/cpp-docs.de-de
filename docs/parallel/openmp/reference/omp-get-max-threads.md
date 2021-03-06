---
title: Omp_get_max_threads | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-parallel
ms.topic: reference
f1_keywords:
- omp_get_max_threads
dev_langs:
- C++
helpviewer_keywords:
- omp_get_max_threads OpenMP function
ms.assetid: f47c3725-3e40-469f-8bc8-a1e47f264cc3
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: 303e037d3fbeaf1958918c2ac78346bdcf01cf2a
ms.sourcegitcommit: 7019081488f68abdd5b2935a3b36e2a5e8c571f8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/07/2018
---
# <a name="ompgetmaxthreads"></a>omp_get_max_threads
Gibt eine ganze Zahl, die gleich oder größer als die Anzahl der Threads, die verfügbar sind, wenn einem parallelen Bereich ohne [Num_threads](../../../parallel/openmp/reference/num-threads.md) an diesem Punkt im Code definiert wurden.  
  
## <a name="syntax"></a>Syntax  
  
```  
int omp_get_max_threads( )  
```  
  
## <a name="remarks"></a>Hinweise  
 Weitere Informationen finden Sie unter [3.1.3 Omp_get_max_threads-Funktion](../../../parallel/openmp/3-1-3-omp-get-max-threads-function.md).  
  
## <a name="example"></a>Beispiel  
  
```  
// omp_get_max_threads.cpp  
// compile with: /openmp  
#include <stdio.h>  
#include <omp.h>  
  
int main( )   
{  
    omp_set_num_threads(8);  
    printf_s("%d\n", omp_get_max_threads( ));  
    #pragma omp parallel  
        #pragma omp master  
        {  
            printf_s("%d\n", omp_get_max_threads( ));  
        }  
  
    printf_s("%d\n", omp_get_max_threads( ));  
  
    #pragma omp parallel num_threads(3)  
        #pragma omp master  
        {  
            printf_s("%d\n", omp_get_max_threads( ));  
        }  
  
    printf_s("%d\n", omp_get_max_threads( ));  
}  
```  
  
```Output  
8  
8  
8  
8  
8  
```  
  
## <a name="see-also"></a>Siehe auch  
 [Funktionen](../../../parallel/openmp/reference/openmp-functions.md)