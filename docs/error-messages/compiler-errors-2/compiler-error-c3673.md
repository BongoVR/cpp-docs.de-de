---
title: Compilerfehler C3673 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C3673
dev_langs:
- C++
helpviewer_keywords:
- C3673
ms.assetid: bb6d2079-05af-4e2c-be0e-75c892e6c590
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 5359115064abc96d2a2091dfaf029ca49575f733
ms.sourcegitcommit: 76b7653ae443a2b8eb1186b789f8503609d6453e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/04/2018
---
# <a name="compiler-error-c3673"></a>Compilerfehler C3673
'Typ': Klasse verfügt nicht über einen Kopierkonstruktor  
  
 Ein benutzerdefinierten Konstruktor ist erforderlich, um Objekte der Ref-CLR-Typen zu kopieren. Weitere Informationen finden Sie unter [C++-Stapelsemantik für Referenztypen](../../dotnet/cpp-stack-semantics-for-reference-types.md).  
  
## <a name="example"></a>Beispiel  
 Im folgende Beispiel wird C3673 generiert.  
  
```  
// C3673.cpp  
// compile with: /clr  
public ref struct R {  
public:  
   R() {}  
   // Uncomment the following line to resolve.  
   // R(R% p) {}  
};  
  
int main() {  
   R r;  
   R s = r;   // C3673  
}  
```  
  
## <a name="example"></a>Beispiel  
 Im folgende Beispiel wird C3673 generiert.  
  
```  
// C3673_b.cpp  
// compile with: /clr /c  
// C3673 expected  
using namespace System;  
[AttributeUsage(AttributeTargets::Class)]  
ref class MyAttr : public Attribute {  
public:  
   MyAttr() {}  
   // Uncomment the following line to resolve.  
   // MyAttr(int i) {}  
   property int Priority;  
   property int Version;  
};  
  
[MyAttr]   
ref class ClassA {};   // OK, no arguments  
  
[MyAttr(Priority = 1)]   
ref class ClassB {};   // OK, named argument  
  
[MyAttr(123)]  
ref class ClassC {};   // Positional argument  
  
[MyAttr(123, Version = 1)]  
ref class ClassD {};   // Positional and named  
```