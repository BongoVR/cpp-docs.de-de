---
title: Compilerfehler C2473 | Microsoft Docs
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- devlang-cpp
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- C2473
dev_langs:
- C++
helpviewer_keywords:
- C2473
ms.assetid: 6bb7dbf5-b198-490f-860e-fd64d0c2a284
caps.latest.revision: 4
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
ms.openlocfilehash: 30fe7daae04948c01feaa403172ed55ee816ff2f
ms.lasthandoff: 04/12/2017

---
# <a name="compiler-error-c2473"></a>Compilerfehler C2473
"Bezeichner": Hat die Form einer Funktionsdefinition, aber es gibt keine Parameterliste.  
  
 Der Compiler hat einen Codeabschnitt entdeckt, der wie eine Funktion aussieht, aber keine Parameterliste aufweist.  
  
## <a name="example"></a>Beispiel  
 Im folgenden Beispiel wird C2473 generiert.  
  
```  
// C2473.cpp  
// compile with: /clr /c  
class A {  
   int i {}   // C2473  
};  
  
class B {  
   int i() {}   // OK  
};  
```
