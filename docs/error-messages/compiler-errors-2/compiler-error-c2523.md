---
title: Compilerfehler C2523 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2523
dev_langs:
- C++
helpviewer_keywords:
- C2523
ms.assetid: 7951b700-8f37-45a0-beb4-a79ae0ced72e
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 4546e576ced8d57a35c4c4861f29824a8d91d910
ms.sourcegitcommit: 76b7653ae443a2b8eb1186b789f8503609d6453e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/04/2018
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