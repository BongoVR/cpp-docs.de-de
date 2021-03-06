---
title: Omp_set_num_threads | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-parallel
ms.topic: reference
f1_keywords:
- omp_set_num_threads
dev_langs:
- C++
helpviewer_keywords:
- omp_set_num_threads OpenMP function
ms.assetid: dae0bf3f-cd7a-4413-89de-6149ac1f4fa7
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: 335cb283026a019d6c6a03565c5dbec541140db3
ms.sourcegitcommit: 7019081488f68abdd5b2935a3b36e2a5e8c571f8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/07/2018
---
# <a name="ompsetnumthreads"></a>omp_set_num_threads
Die Anzahl der Threads in nachfolgenden parallele Regionen, legt fest, es sei denn, durch Überschreiben einer [Num_threads](../../../parallel/openmp/reference/num-threads.md) Klausel.  
  
## <a name="syntax"></a>Syntax  
  
```  
void omp_set_num_threads(  
   int num_threads  
);  
```  
  
## <a name="remarks"></a>Hinweise  
 wobei  
  
 `num_threads`  
 Die Anzahl der Threads in der parallelen Bereich.  
  
## <a name="remarks"></a>Hinweise  
 Weitere Informationen finden Sie unter [3.1.1 Omp_set_num_threads-Funktion](../../../parallel/openmp/3-1-1-omp-set-num-threads-function.md).  
  
## <a name="example"></a>Beispiel  
 Finden Sie unter [Omp_get_num_threads](../../../parallel/openmp/reference/omp-get-num-threads.md) ein Beispiel der Verwendung von `omp_set_num_threads`.  
  
## <a name="see-also"></a>Siehe auch  
 [Funktionen](../../../parallel/openmp/reference/openmp-functions.md)