---
title: Compilerfehler C3057 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C3057
dev_langs:
- C++
helpviewer_keywords:
- C3057
ms.assetid: b0b2ba88-9c74-4bec-bf60-8fc72eade34c
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: de369f3442956a124624ab730aa60694a98733ca
ms.sourcegitcommit: 76b7653ae443a2b8eb1186b789f8503609d6453e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/04/2018
---
# <a name="compiler-error-c3057"></a>Compilerfehler C3057
'Symbol': Die dynamische Initialisierung von threadprivate-Symbolen wird derzeit nicht unterstützt.  
  
 Der initialisierte Wert eines Symbols, der in einer [threadprivate](../../parallel/openmp/reference/threadprivate.md) -Klausel verwendet wird, muss zum Zeitpunkt der Kompilierung bekannt sein.  
  
 Im folgenden Beispiel wird C3057 generiert:  
  
```  
// C3057.cpp  
// compile with: /openmp /c  
extern int f();  
int x, y = f();  
int a, b;  
#pragma omp threadprivate(x, y)   // C3057  
  
#pragma omp threadprivate(a, b)  
  
int main() {  
   // Delete the following 4 lines to resolve.  
   #pragma omp parallel copyin(x, y)  
   {  
      x = y;  
   }  
  
   #pragma omp parallel copyin(a, b)  
   {  
      a = b;  
   }  
}  
```  
  
 Im folgenden Beispiel wird C3057 generiert:  
  
```  
// C3057b.cpp  
// compile with: /openmp /c  
extern int Initialize();  
int main() {  
   #pragma omp parallel  
   {  
      static int var = Initialize();  
      #pragma omp threadprivate(var)   // C3057  
   }  
  
   // OK  
   #pragma omp parallel  
   {  
      static int var2;  
      static bool initialized2;  
      #pragma omp threadprivate(var2, initialized2)  
      if (!initialized2) {  
         var2 = Initialize();  
         initialized2 = true;  
      }  
   }  
}  
```