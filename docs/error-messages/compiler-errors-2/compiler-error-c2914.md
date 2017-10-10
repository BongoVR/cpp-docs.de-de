---
title: Compilerfehler C2914 | Microsoft Docs
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- cpp-tools
ms.tgt_pltfrm: 
ms.topic: error-reference
f1_keywords:
- C2914
dev_langs:
- C++
helpviewer_keywords:
- C2914
ms.assetid: fc6a0592-f53e-4f5a-88cb-780bbed4acf2
caps.latest.revision: 11
author: corob-msft
ms.author: corob
manager: ghogen
ms.translationtype: MT
ms.sourcegitcommit: 35b46e23aeb5f4dbfd2a0dd44b906389dd5bfc88
ms.openlocfilehash: 67bd7d142f77012821b7e464dd73c416088bf48d
ms.contentlocale: de-de
ms.lasthandoff: 10/10/2017

---
# <a name="compiler-error-c2914"></a>Compilerfehler C2914
'Bezeichner': Argument vom Typ nicht ableiten, als Funktionsargument mehrdeutig ist.  
  
 Der Compiler ermitteln nicht, welche überladenen Funktionen für eine generische oder Vorlagenklasse Argument verwenden sollen.  
  
 Im folgenden Beispiel wird C2914 generiert:  
  
```  
// C2914.cpp  
// compile with: /c  
void f(int);  
void f(double);  
template<class T> void g(void (*) (T));  
void h() { g(f); }   // C2914  
// try the following line instead  
// void h() { g<int>(f); }  
```  
  
 C2914 kann auch auftreten, wenn Generika verwendet werden.  Im folgenden Beispiel wird C2914 generiert:  
  
```  
// C2914b.cpp  
// compile with: /clr /c  
void f(int);  
void f(double);  
  
template<class T>   
void gf(void (*) (T));  
  
void h() { gf(f);}   // C2914  
// try the following line instead  
void h() { gf<int>(f); }  
```
