---
title: Compilerfehler C2227 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2227
dev_langs:
- C++
helpviewer_keywords:
- C2227
ms.assetid: d470e8b8-7e15-468b-84fa-37d1a0132271
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 6a23d055dec45693f292978039c5c5108e34e7a9
ms.sourcegitcommit: 76b7653ae443a2b8eb1186b789f8503609d6453e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/04/2018
---
# <a name="compiler-error-c2227"></a>Compilerfehler C2227
Links von „->member“ muss sich ein Zeiger auf Klassen-/Struktur-/Union-/generischen Typ befinden.  
  
 Der Operand auf der linken Seite des `->` ist kein Zeiger auf eine Klasse, Struktur oder Union.  
  
 Das folgende Beispiel generiert C2227:  
  
```  
// C2227.cpp  
int *pInt;  
struct S {  
public:  
    int member;  
} s, *pS = &s;  
  
int main() {  
   pInt->member = 0;   // C2227 pInt points to an int  
   pS->member = 0;   // OK  
}  
```