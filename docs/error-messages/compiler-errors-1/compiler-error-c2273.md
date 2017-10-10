---
title: Compilerfehler C2273 | Microsoft Docs
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- cpp-tools
ms.tgt_pltfrm: 
ms.topic: error-reference
f1_keywords:
- C2273
dev_langs:
- C++
helpviewer_keywords:
- C2273
ms.assetid: 3c682c66-97bf-4a23-a22c-d9a26a92bf95
caps.latest.revision: 10
author: corob-msft
ms.author: corob
manager: ghogen
ms.translationtype: MT
ms.sourcegitcommit: 35b46e23aeb5f4dbfd2a0dd44b906389dd5bfc88
ms.openlocfilehash: 58f7f13303b9941cf07e90685d68d7114213ea2d
ms.contentlocale: de-de
ms.lasthandoff: 10/09/2017

---
# <a name="compiler-error-c2273"></a>Compilerfehler C2273
'Typ': unzulässig auf der rechten Seite des Operators "->"  
  
 Ein Typ wird als der Rechte Operand des eine `->` Operator.  
  
 Dieser Fehler kann verursacht werden, indem Sie versuchen, eine Konvertierung für einen benutzerdefinierten Typ zugreifen. Verwenden Sie das Schlüsselwort `operator` zwischen -> und `type`.  
  
 Im folgende Beispiel wird C2273 generiert:  
  
```  
// C2273.cpp  
struct MyClass {  
   operator int() {  
      return 0;  
   }  
};  
int main() {  
   MyClass * ClassPtr = new MyClass;  
   int i = ClassPtr->int();   // C2273  
   int j = ClassPtr-> operator int();   // OK  
}  
```
