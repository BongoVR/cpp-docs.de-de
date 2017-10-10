---
title: Compilerfehler C2274 | Microsoft Docs
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- cpp-tools
ms.tgt_pltfrm: 
ms.topic: error-reference
f1_keywords:
- C2274
dev_langs:
- C++
helpviewer_keywords:
- C2274
ms.assetid: 8e874903-f499-45ef-8291-f821eee4cc1c
caps.latest.revision: 9
author: corob-msft
ms.author: corob
manager: ghogen
ms.translationtype: MT
ms.sourcegitcommit: 35b46e23aeb5f4dbfd2a0dd44b906389dd5bfc88
ms.openlocfilehash: 4315d1cfef9a0583b1f44c8caa264378e32f1a35
ms.contentlocale: de-de
ms.lasthandoff: 10/09/2017

---
# <a name="compiler-error-c2274"></a>Compilerfehler C2274
'Typ': Unzulässiger als rechts neben "."-Operator  
  
 Ein Typ wird als der Rechte Operand des ein Memberzugriffsoperator (.).  
  
 Dieser Fehler kann verursacht werden, indem Sie versuchen, eine Konvertierung für einen benutzerdefinierten Typ zugreifen. Verwenden Sie das Schlüsselwort `operator` zwischen dem Zeitraum und `type`.  
  
 Im folgenden Beispiel wird C2286 generiert:  
  
```  
// C2274.cpp  
struct MyClass {  
   operator int() {  
      return 0;  
   }  
};  
  
int main() {  
   MyClass ClassName;  
   int i = ClassName.int();   // C2274  
   int j = ClassName.operator int();   // OK  
}  
```
