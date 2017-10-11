---
title: Compilerfehler C3005 | Microsoft Docs
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- cpp-tools
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- C3005
dev_langs:
- C++
helpviewer_keywords:
- C3005
ms.assetid: 30bad565-e79f-4c3f-82cb-a74bd0baab8f
caps.latest.revision: 6
author: corob-msft
ms.author: corob
manager: ghogen
ms.translationtype: MT
ms.sourcegitcommit: 35b46e23aeb5f4dbfd2a0dd44b906389dd5bfc88
ms.openlocfilehash: 711b5083146f4b9a77d65746601eba264f0d41b9
ms.contentlocale: de-de
ms.lasthandoff: 10/10/2017

---
# <a name="compiler-error-c3005"></a>Compilerfehler C3005
'Fehlertext': Für die 'Direktive'-Direktive von OpenMP wurde ein unerwartetes Token gefunden.  
  
 Eine OpenMP-Direktive wurde nicht ordnungsgemäß formatiert.  
  
 Im folgenden Beispiel wird C3005 generiert.  
  
```  
// C3005.c  
// compile with: /openmp  
int main()  
{  
   #pragma omp parallel + for   // C3005  
}  
```  
  
 C3005 kann auch auftreten, wenn Sie in derselben Zeile wie das Pragma eine öffnende geschweifte Klammer einfügen.  
  
```  
// C3005b.c  
// compile with: /openmp  
int main() {  
   #pragma omp parallel {   // C3005 put open brace on next line  
   lbl2:;  
   }  
   goto lbl2;  
}  
```
