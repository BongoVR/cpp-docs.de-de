---
title: Compiler-Fehler C3185 generiert | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C3185
dev_langs:
- C++
helpviewer_keywords:
- C3185
ms.assetid: 5bf96279-043c-4981-9d02-b4550071b192
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: ce6eea7c9a40f9dd38bf6892995eaa52ac540de7
ms.sourcegitcommit: 76b7653ae443a2b8eb1186b789f8503609d6453e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/04/2018
---
# <a name="compiler-error-c3185"></a>Compiler-Fehler C3185 generiert
"TypeId" verwendet für verwalteten oder WinRT-Typ "Typ"; verwenden Sie stattdessen "Operator".  
  
 Sie können nicht angewendet werden die [Typeid](../../cpp/typeid-operator.md) Operator, um ein verwaltetes oder WinRT-Typ; verwenden Sie [Typeid](../../windows/typeid-cpp-component-extensions.md) stattdessen.  
  
 Im folgenden Beispiel wird C3185 generiert und gezeigt, wie Sie diesen Fehler beheben:  
  
```  
// C3185a.cpp  
// compile with: /clr  
ref class Base {};  
ref class Derived : public Base {};  
  
int main() {  
   Derived ^ pd = gcnew Derived;  
   Base ^pb = pd;  
   const type_info & t1 = typeid(pb);   // C3185  
   System::Type ^ MyType = Base::typeid;   // OK  
};  
```  
