---
title: Compiler-Fehler C2723 generiert | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2723
dev_langs:
- C++
helpviewer_keywords:
- C2723
ms.assetid: 86925601-2297-4cfd-94e2-2caf27c474c4
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 01476218683205d0fb06e81847cfe9727b733158
ms.sourcegitcommit: 76b7653ae443a2b8eb1186b789f8503609d6453e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/04/2018
---
# <a name="compiler-error-c2723"></a>Compiler-Fehler C2723 generiert
„Funktion“: Spezifizierer „Spezifizierer“ ist in Funktionsdefinition unzulässig.  
  
 Der Spezifizierer darf nicht mit einer Funktionsdefinition außerhalb einer Klassendeklaration vorkommen. Der `virtual`-Spezifizierer kann nur in einer Deklaration einer Memberfunktion innerhalb einer Klassendeklaration angegeben werden.  
  
 Im folgenden Beispiel wird C2723 generiert und gezeigt, wie Sie diesen Fehler beheben:  
  
```  
// C2723.cpp  
struct X {  
   virtual void f();  
   virtual void g();  
};  
  
virtual void X::f() {}   // C2723  
  
// try the following line instead  
void X::g() {}  
```