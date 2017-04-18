---
title: Compilerfehler C3496 | Microsoft Docs
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- devlang-cpp
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- C3496
dev_langs:
- C++
helpviewer_keywords:
- C3496
ms.assetid: e19885f2-677f-4c1e-bc69-e35852262dc3
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
ms.openlocfilehash: 72013d9345361bfbf0ee1dedecb27402850520c8
ms.lasthandoff: 04/12/2017

---
# <a name="compiler-error-c3496"></a>Compilerfehler C3496
"this" wird immer nach Wert erfasst: "&" wird ignoriert.  
  
 Der `this` -Zeiger kann nicht als Verweis erfasst werden.  
  
### <a name="to-correct-this-error"></a>So beheben Sie diesen Fehler  
  
-   Erfassen Sie den `this` -Zeiger nach Wert.  
  
## <a name="example"></a>Beispiel  
 Im folgenden Beispiel wird C3496 generiert, weil ein Verweis auf den `this` -Zeiger in der Erfassungsliste eines Lambdaausdrucks auftritt:  
  
```  
// C3496.cpp  
// compile with: /c  
  
class C  
{  
   void f()  
   {  
      [&this] {}(); // C3496  
   }  
};  
```  
  
## <a name="see-also"></a>Siehe auch  
 [Lambda-Ausdrücke](../../cpp/lambda-expressions-in-cpp.md)
