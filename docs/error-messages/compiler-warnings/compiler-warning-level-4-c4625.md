---
title: Compilerwarnung (Stufe 4) C4625 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C4625
dev_langs:
- C++
helpviewer_keywords:
- C4625
ms.assetid: 4cc99e50-846c-4784-97da-48b977067851
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 9279d5a9bfa7aa80ae866d290624f1edf888e36b
ms.sourcegitcommit: 76b7653ae443a2b8eb1186b789f8503609d6453e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/04/2018
---
# <a name="compiler-warning-level-4-c4625"></a>Compilerwarnung (Stufe 4) C4625
'derived class': Der Kopierkonstruktor wurde implizit als gelöscht definiert, da ein Basisklassen-Kopierkonstruktor nicht zugreifbar ist oder gelöscht wurde.  
  
 Ein Kopieroperator wurde gelöscht, oder es kann nicht auf diesen in einer Basisklasse zugegriffen werden. Daher wurde er nicht für eine abgeleitete Klasse generiert. Bei jedem Versuch, ein Objekt dieses Typs zu kopieren, wird ein Compilerfehler generiert.  
  
 Diese Warnung ist standardmäßig deaktiviert. Weitere Informationen finden Sie unter [Standardmäßig deaktivierte Compilerwarnungen](../../preprocessor/compiler-warnings-that-are-off-by-default.md) .  
  
## <a name="example"></a>Beispiel  
 Im folgenden Beispiel wird C4625 generiert und gezeigt, wie Sie diesen Fehler beheben.  
  
```  
// C4625.cpp  
// compile with: /W4 /c  
#pragma warning(default : 4625)  
  
struct A {  
   A() {}  
  
private:  
   A(const A&) {}  
};  
  
struct C : private virtual A {};  
struct B :  C {};   // C4625 no copy constructor  
  
struct D : A {};  
struct E :  D {};   // OK  
```