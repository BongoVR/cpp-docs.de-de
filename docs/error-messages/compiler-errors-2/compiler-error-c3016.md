---
title: Compilerfehler C3016 | Microsoft Docs
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- devlang-cpp
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- C3016
dev_langs:
- C++
helpviewer_keywords:
- C3016
ms.assetid: 3423467e-e8bb-4f35-b4db-7925cafa74c1
caps.latest.revision: 7
author: corob-msft
ms.author: corob
manager: ghogen
translation.priority.ht:
- de-de
- es-es
- fr-fr
- it-it
- ja-jp
- ko-kr
- ru-ru
- zh-cn
- zh-tw
translation.priority.mt:
- cs-cz
- pl-pl
- pt-br
- tr-tr
translationtype: Machine Translation
ms.sourcegitcommit: 0d9cbb01d1ad0f2ea65d59334cb88140ef18fce0
ms.openlocfilehash: 49ccb5cc06a497103a62d6360ebddb16bc063bc7
ms.lasthandoff: 04/12/2017

---
# <a name="compiler-error-c3016"></a>Compilerfehler C3016
"Var": Indexvariable in der For-Anweisung von OpenMP muss einen ganzzahligen Typ mit Vorzeichen aufweisen  
  
 Die Indexvariable in einer `for` -Anweisung von OpenMP muss einen ganzzahligen Typ mit Vorzeichen aufweisen.  
  
 Im folgenden Beispiel wird C3016 generiert:  
  
```  
// C3016.cpp  
// compile with: /openmp  
int main()  
{  
   #pragma omp parallel  
   {  
      unsigned int i = 0;  
      // Try the following line instead:  
      // int i = 0;  
  
      #pragma omp for  
      for (i = 0; i <= 10; ++i)   // C3016  
      {  
      }  
   }  
}  
```
