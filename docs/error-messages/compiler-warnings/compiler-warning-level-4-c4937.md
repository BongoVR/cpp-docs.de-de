---
title: Compilerwarnung (Stufe 4) C4937 | Microsoft Docs
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- devlang-cpp
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- C4937
dev_langs:
- C++
helpviewer_keywords:
- C4937
ms.assetid: 2bb9f0e7-bbd6-4697-84de-95955e32ae29
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
ms.openlocfilehash: 655bf5154f66e2f641321adbd395c2bc5694e148
ms.lasthandoff: 04/12/2017

---
# <a name="compiler-warning-level-4-c4937"></a>Compilerwarnung (Stufe 4) C4937
'Text1' und 'Text2' sind als Argumente für 'Direktive' nicht differenzierbar.  
  
 Aufgrund der Art und Weise, wie der Compiler Argumente zu Direktiven verarbeitet, können Namen, die für den Compiler eine Bedeutung haben, z. B. Schlüsselwörter mit mehreren Textdarstellungen (Varianten mit einfachem und doppeltem Unterstrich), nicht unterschieden werden.  
  
 Beispiele solcher Zeichenfolgen sind __cdecl und \__forceinline.  Beachten Sie, dass unter „/Za“ nur die Varianten mit doppeltem Unterstrich aktiviert sind.  
  
 Im folgenden Beispiel wird C4937 generiert:  
  
```  
// C4937.cpp  
// compile with: /openmp /W4  
#include "omp.h"  
int main() {  
   #pragma omp critical ( __leave )   // C4937  
   ;  
  
   // OK  
   #pragma omp critical ( leave )  
   ;  
}  
```
