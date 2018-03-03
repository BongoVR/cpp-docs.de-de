---
title: Compilerwarnung (Stufe 4) C4510 | Microsoft Docs
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- cpp-tools
ms.tgt_pltfrm: 
ms.topic: error-reference
f1_keywords:
- C4510
dev_langs:
- C++
helpviewer_keywords:
- C4510
ms.assetid: fd28d1d4-ad27-4dad-94c0-9dba46c93180
caps.latest.revision: 
author: corob-msft
ms.author: corob
manager: ghogen
ms.workload:
- cplusplus
ms.openlocfilehash: 4bfef2780f338357b600f8fae28559d4c7c00e49
ms.sourcegitcommit: 8fa8fdf0fbb4f57950f1e8f4f9b81b4d39ec7d7a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/21/2017
---
# <a name="compiler-warning-level-4-c4510"></a>Compilerwarnung (Stufe 4) C4510
'Klasse': Standardkonstruktor konnte nicht generiert werden  
  
 Kann nicht generiert der Compiler einen Standardkonstruktor für die angegebene Klasse und keinen benutzerdefinierten Konstruktor erstellt wurde. Sie werden nicht auf Objekte dieses Typs erstellen können.  
  
 Es gibt mehrere Situationen, die verhindern, dass den Compiler einen Standardkonstruktor generiert einschließlich:  
  
-   Ein Datenmember.  
  
-   Ein Datenmember, der ein Verweis ist.  
  
 Sie müssen einen benutzerdefinierten Standardkonstruktor für die Klasse erstellen, die diese Member initialisiert.  
  
 Im folgenden Beispiel wird C4510 generiert:  
  
```  
// C4510.cpp  
// compile with: /W4  
struct A {  
   const int i;  
   int &j;  
   A& operator=( const A& ); // C4510 expected  
   // uncomment the following line to resolve this C4510  
   // A(int ii, int &jj) : i(ii), j(jj) {}  
};   // C4510  
  
int main() {  
}  
```