---
title: kritische | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-parallel
ms.topic: reference
f1_keywords:
- Critical
dev_langs:
- C++
helpviewer_keywords:
- critical OpenMP directive
ms.assetid: 2ab87d6d-5ca4-43ae-9f0a-1f517a6a2bab
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: 5cb5747530f4c3aaa7bcfddc7a44c0c8d91e1270
ms.sourcegitcommit: 7019081488f68abdd5b2935a3b36e2a5e8c571f8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/07/2018
---
# <a name="critical"></a>critical
Gibt an, dass der Code wird nur in einem Thread zu einem Zeitpunkt ausgeführt werden.  
  
## <a name="syntax"></a>Syntax  
  
```  
#pragma omp critical [(name)]  
{  
   code_block  
}  
```  
  
## <a name="remarks"></a>Hinweise  
 wobei  
  
 (`name`) (optional)  
 Ein Name zum Identifizieren der kritischen Code. Beachten Sie, dass dieser Name in Klammern eingeschlossen werden muss.  
  
## <a name="remarks"></a>Hinweise  
 Die **kritische** Richtlinie unterstützt kein OpenMP-Klauseln.  
  
 Weitere Informationen finden Sie unter [2.6.2 kritische erstellen](../../../parallel/openmp/2-6-2-critical-construct.md).  
  
## <a name="example"></a>Beispiel  
  
```  
// omp_critical.cpp  
// compile with: /openmp   
#include <omp.h>  
#include <stdio.h>  
#include <stdlib.h>  
  
#define SIZE 10  
  
int main()   
{  
    int i;  
    int max;  
    int a[SIZE];  
  
    for (i = 0; i < SIZE; i++)   
    {  
        a[i] = rand();  
        printf_s("%d\n", a[i]);  
    }  
  
    max = a[0];  
    #pragma omp parallel for num_threads(4)  
        for (i = 1; i < SIZE; i++)   
        {  
            if (a[i] > max)  
            {  
                #pragma omp critical  
                {  
                    // compare a[i] and max again because max   
                    // could have been changed by another thread after   
                    // the comparison outside the critical section  
                    if (a[i] > max)  
                        max = a[i];  
                }  
            }  
        }  
  
    printf_s("max = %d\n", max);  
}  
```  
  
```Output  
41  
18467  
6334  
26500  
19169  
15724  
11478  
29358  
26962  
24464  
max = 29358  
```  
  
## <a name="see-also"></a>Siehe auch  
 [Anweisungen](../../../parallel/openmp/reference/openmp-directives.md)