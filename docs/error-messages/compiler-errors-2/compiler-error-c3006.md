---
title: Compilerfehler C3006 | Microsoft Docs
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-tools
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords: C3006
dev_langs: C++
helpviewer_keywords: C3006
ms.assetid: 449082ec-fd45-4c47-8ab3-ba6a719e4dc4
caps.latest.revision: "6"
author: corob-msft
ms.author: corob
manager: ghogen
ms.workload: cplusplus
ms.openlocfilehash: 486fbfef98c262ab77e5219c12734af854afbc3a
ms.sourcegitcommit: 8fa8fdf0fbb4f57950f1e8f4f9b81b4d39ec7d7a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/21/2017
---
# <a name="compiler-error-c3006"></a>Compilerfehler C3006
"Klausel": In der Klausel für die "directive"-Direktive von OpenMP fehlt ein erwartetes Argument.  
  
 Bei einer OpenMP-Direktive fehlt ein erwartetes Argument.  
  
 Im folgenden Beispiel wird C3006 generiert:  
  
```  
// C3006.c  
// compile with: /openmp  
int main()  
{  
   #pragma omp parallel shared   // C3006  
   // Try the following line instead:  
   // #pragma omp parallel shared(x) {}  
  
}  
```