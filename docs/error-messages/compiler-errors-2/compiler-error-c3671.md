---
title: Compilerfehler C3671 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C3671
dev_langs:
- C++
helpviewer_keywords:
- C3671
ms.assetid: d684e4ae-87e2-4424-80bb-6f346652c831
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 50b52bb30b24204e810dc350cdb7fef502a93852
ms.sourcegitcommit: 76b7653ae443a2b8eb1186b789f8503609d6453e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/04/2018
---
# <a name="compiler-error-c3671"></a>Compilerfehler C3671
'Funktion_1': Funktion überschreibt keine 'Funktion_2'  
  
 Bei der expliziten Überschreibungssyntax zu verwenden, generiert der Compiler einen Fehler aus, wenn eine Funktion nicht überschrieben wird.  Finden Sie unter [explizite Überschreibungen](../../windows/explicit-overrides-cpp-component-extensions.md) für Weitere Informationen.  
  
## <a name="example"></a>Beispiel  
 Im folgende Beispiel wird C3671 generiert.  
  
```  
// C3671.cpp  
// compile with: /clr /c  
ref struct S {  
   virtual void f();  
};  
  
ref struct S1 : S {  
   virtual void f(int) new sealed = S::f;   // C3671  
   virtual void f() new sealed = S::f;  
};  
```