---
title: Compilerfehler C2319 | Microsoft Docs
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- devlang-cpp
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- C2319
dev_langs:
- C++
helpviewer_keywords:
- C2319
ms.assetid: 25263e6e-f5ba-4d2c-8727-8c2d8ca2e5ce
caps.latest.revision: 9
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
ms.openlocfilehash: 83856c006effc92319afb7a3afd5360344e7b746
ms.lasthandoff: 04/12/2017

---
# <a name="compiler-error-c2319"></a>Compilerfehler C2319
Auf 'try/catch' muss eine zusammengesetzte Anweisung folgen. '{' fehlt  
  
 Es wurde kein `try` - oder `catch` -Block gefunden, der auf die `try` - oder `catch` -Anweisung folgt. Der Block muss in geschweifte Klammern eingeschlossen werden.  
  
 Im folgenden Beispiel wird C2319 generiert:  
  
```  
// C2319.cpp  
// compile with: /EHsc  
#include <eh.h>  
class C {};  
int main() {  
   try {  
      throw "ooops!";  
   }  
   catch( C ) ;    // C2319  
   // try the following line instead  
   // catch( C ) {}  
}  
```
