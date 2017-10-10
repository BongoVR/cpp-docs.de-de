---
title: Compilerfehler C2523 | Microsoft Docs
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- cpp-tools
ms.tgt_pltfrm: 
ms.topic: error-reference
f1_keywords:
- C2523
dev_langs:
- C++
helpviewer_keywords:
- C2523
ms.assetid: 7951b700-8f37-45a0-beb4-a79ae0ced72e
caps.latest.revision: 9
author: corob-msft
ms.author: corob
manager: ghogen
ms.translationtype: MT
ms.sourcegitcommit: 35b46e23aeb5f4dbfd2a0dd44b906389dd5bfc88
ms.openlocfilehash: d9ec6a9196498f210e680acf17efd34ac84faf77
ms.contentlocale: de-de
ms.lasthandoff: 10/10/2017

---
# <a name="compiler-error-c2523"></a>Compilerfehler C2523
' Klasse:: ~ Identifier': Destruktor/Finalizer Tag Konflikt  
  
 Der Name des Destruktors muss der Klassenname mit einer Tilde (`~`). Der Konstruktor noch der Destruktor werden nur Member, die den gleichen Namen wie die Klasse haben.  
  
 Im folgende Beispiel wird C2523 generiert:  
  
```  
// C2523.cpp  
// compile with: /c  
class A {  
   ~B();    // C2523  
   ~A();   // OK  
};  
```
