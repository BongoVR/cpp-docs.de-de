---
title: Compilerfehler C2229 | Microsoft Docs
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- cpp-tools
ms.tgt_pltfrm: 
ms.topic: error-reference
f1_keywords:
- C2229
dev_langs:
- C++
helpviewer_keywords:
- C2229
ms.assetid: 933c7cf2-a463-4e74-b0b4-59dedad987fb
caps.latest.revision: 10
author: corob-msft
ms.author: corob
manager: ghogen
ms.translationtype: MT
ms.sourcegitcommit: 35b46e23aeb5f4dbfd2a0dd44b906389dd5bfc88
ms.openlocfilehash: c54e3affb39cb396df1caaafe6450d5c6ac80f6e
ms.contentlocale: de-de
ms.lasthandoff: 10/09/2017

---
# <a name="compiler-error-c2229"></a>Compilerfehler C2229
Typ "Identifier" wurde ein ungültiger NULL-array  
  
 Ein Member einer Struktur oder ein Bit enthält ein Array der Größe 0 (null), die nicht das letzte Element ist.  
  
 Da Sie als das letzte Element der Struktur der Array 0 (null) Größe aufweisen darf, müssen Sie seine Größe angeben, wenn Sie die Struktur zuordnen.  
  
 Wenn 0 (null) großen Arrays nicht das letzte Element der Struktur ist, kann der Compiler nicht den Offset für die verbleibenden Felder berechnen.  
  
 Im folgende Beispiel wird C2229 generiert:  
  
```  
// C2229.cpp  
struct S {  
   int a[0];  // C2229  zero-sized array  
   int b[1];  
};  
  
struct S2 {  
   int a;  
   int b[0];  
};  
  
int main() {  
   // allocate 7 elements for b field  
   S2* s2 = (S2*)new int[sizeof(S2) + 7*sizeof(int)];  
   s2->b[6] = 100;  
}  
```
