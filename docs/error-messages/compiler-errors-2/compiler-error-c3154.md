---
title: Compiler-Fehler C3154 generiert | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C3154
dev_langs:
- C++
helpviewer_keywords:
- C3154
ms.assetid: 78005c74-eaaf-4ac2-88ae-6c25d01a302a
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 33afc69bb44488d56b51797c72f2cd5ea4105420
ms.sourcegitcommit: 76b7653ae443a2b8eb1186b789f8503609d6453e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/04/2018
---
# <a name="compiler-error-c3154"></a>Compiler-Fehler C3154 generiert
Erwartet ',', bevor Sie mit den Auslassungspunkten. Nicht durch Trennzeichen getrennte Auslassungszeichen werden unter Parameter Array-Funktionen nicht unterstützt.  
  
 Eine Variablen argumentsfunktion wurde nicht ordnungsgemäß deklariert.  
  
 Weitere Informationen finden Sie unter [Variablenargumentlisten (...) (C + C++ / CLI) ](../../windows/variable-argument-lists-dot-dot-dot-cpp-cli.md).  
  
## <a name="example"></a>Beispiel  
 Im folgende Beispiel wird C3154 generiert.  
  
```  
// C3154.cpp  
// compile with: /clr  
ref struct R {  
   void Func(int ... array<int> ^);   // C3154  
   void Func2(int i, ... array<int> ^){}   // OK  
   void Func3(array<int> ^){}   // OK  
   void Func4(... array<int> ^){}   // OK  
};  
  
int main() {  
   R ^ r = gcnew R;  
   r->Func4(1,2,3);  
}  
```