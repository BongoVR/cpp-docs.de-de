---
title: Compilerfehler C2271 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2271
dev_langs:
- C++
helpviewer_keywords:
- C2271
ms.assetid: ea47bf57-f55d-4171-8e98-95a71d62820e
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 62f2f108d9f2f3ec6a1ba9f20a2937dee53297a4
ms.sourcegitcommit: 76b7653ae443a2b8eb1186b789f8503609d6453e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/04/2018
---
# <a name="compiler-error-c2271"></a>Compilerfehler C2271
'Operator': neu/löschen dürfen keine Modifizierer enthalten formaler Liste  
  
 Der Operator (`new` oder `delete`) mit einem Speichermodell Spezifizierer deklariert ist.  
  
 Im folgende Beispiel wird C2271 generiert:  
  
```  
// C2271.cpp  
// compile with: /c  
void* operator new(size_t) const {   // C2271  
// try the following line instead  
// void* operator new(size_t) {  
   return 0;  
}  
  
struct X {  
   static void* operator new(size_t) const;   // C2271  
   // try the following line instead  
   // void * X::operator new(size_t) const;   // static member operator new  
};  
```