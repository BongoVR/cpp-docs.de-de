---
title: Compilerfehler C2232 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2232
dev_langs:
- C++
helpviewer_keywords:
- C2232
ms.assetid: 76f302b7-30a7-4a81-9a39-b4edde33b54c
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 504f92a72b500548c2231958afa98ccdc177e12d
ms.sourcegitcommit: 76b7653ae443a2b8eb1186b789f8503609d6453e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/04/2018
---
# <a name="compiler-error-c2232"></a>Compilerfehler C2232
"->": linke Operand ist "Klassenschlüssel" vom Typ, verwenden Sie"."  
  
 Der Operand links vom `->` -Operator ist kein Zeiger. Verwenden Sie den Operator Punkt (.) für eine Klasse, Struktur oder Union.  
  
 Das folgende Beispiel generiert C2232:  
  
```  
// C2232.c  
struct X {  
    int member;  
} x, *px;  
int main() {  
    x->member = 0;   // C2232, x is not a pointer  
  
    px->member = 0;  
    x.member = 0;  
}  
```