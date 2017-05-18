---
title: Compilerfehler C3001 | Microsoft Docs
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- cpp-tools
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- C3001
dev_langs:
- C++
helpviewer_keywords:
- C3001
ms.assetid: d0e03478-1b44-47e5-8f5b-70415fa1f8bc
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
ms.translationtype: Machine Translation
ms.sourcegitcommit: 0d9cbb01d1ad0f2ea65d59334cb88140ef18fce0
ms.openlocfilehash: a2a82e1a01548b2cd099f9a763181c18d24c4399
ms.contentlocale: de-de
ms.lasthandoff: 04/12/2017

---
# <a name="compiler-error-c3001"></a>Compilerfehler C3001
"Fehler_Text": Es wurde ein OpenMP-Direktivenname erwartet.  
  
 #pragma `omp` muss eine Direktive folgen.  
  
 Im folgenden Beispiel wird C3001 generiert:  
  
```  
// C3001.c  
// compile with: /openmp  
int main()  
{  
   #pragma omp   // C3001 missing token  
}  
```
