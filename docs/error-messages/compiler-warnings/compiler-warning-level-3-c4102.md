---
title: Compilerwarnung (Stufe 3) C4102 | Microsoft Docs
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- cpp-tools
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- C4102
dev_langs:
- C++
helpviewer_keywords:
- C4102
ms.assetid: 349f308a-daf3-48c6-bd53-6c38b73f8880
caps.latest.revision: 6
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
ms.openlocfilehash: 97b607c06b5695f06355bf87d39bc6daa53b57d5
ms.contentlocale: de-de
ms.lasthandoff: 04/12/2017

---
# <a name="compiler-warning-level-3-c4102"></a>Compilerwarnung (Stufe 3) C4102
"Marke": Unreferenzierte Marke  
  
 Die Marke wurde definiert, es wurde jedoch nie darauf verwiesen. Die Marke wird vom Compiler ignoriert.  
  
 Im folgenden Beispiel wird C4102 generiert:  
  
```  
// C4102.cpp  
// compile with: /W3  
int main() {  
   int a;  
  
   test:   // C4102, remove the unreferenced label to resolve  
  
   a = 1;  
}  
```
