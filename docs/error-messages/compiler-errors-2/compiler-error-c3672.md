---
title: Compilerfehler C3672 | Microsoft Docs
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- cpp-tools
ms.tgt_pltfrm: 
ms.topic: error-reference
f1_keywords:
- C3672
dev_langs:
- C++
helpviewer_keywords:
- C3672
ms.assetid: da971041-1766-467a-aecf-1d8655c6cb7a
caps.latest.revision: 6
author: corob-msft
ms.author: corob
manager: ghogen
ms.translationtype: MT
ms.sourcegitcommit: 35b46e23aeb5f4dbfd2a0dd44b906389dd5bfc88
ms.openlocfilehash: f01237ca5ac90ea3def4a6d2733ef8dd700bf738
ms.contentlocale: de-de
ms.lasthandoff: 10/10/2017

---
# <a name="compiler-error-c3672"></a>Compilerfehler C3672
Pseudo-Destruktor Ausdruck kann nur als Teil eines Funktionsaufrufs verwendet werden  
  
 Ein Destruktor wurde falsch aufgerufen.  Weitere Informationen finden Sie unter [Destruktoren](../../cpp/destructors-cpp.md).  
  
## <a name="example"></a>Beispiel  
 Im folgende Beispiel wird C3672 generiert.  
  
```  
// C3672.cpp  
template<typename T>  
void f(T* pT) {  
   &pT->T::~T;   // C3672  
   pT->T::~T();   // OK  
};  
  
int main() {  
   int i;  
   f(&i);  
}  
```
