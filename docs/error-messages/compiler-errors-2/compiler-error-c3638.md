---
title: Compilerfehler C3638 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C3638
dev_langs:
- C++
helpviewer_keywords:
- C3638
ms.assetid: 8d8bc5ca-75aa-480e-b6b6-3178fab51b1d
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 3edb1a05323187b4a5dfcc2356da4a1ff8b874de
ms.sourcegitcommit: 76b7653ae443a2b8eb1186b789f8503609d6453e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/04/2018
---
# <a name="compiler-error-c3638"></a>Compilerfehler C3638
'Operator': das standard-Boxing und unboxing Konvertierungsoperatoren können nicht neu definiert werden  
  
 Der Compiler definiert einen Konvertierungsoperator für jede verwaltete Klasse implizites Boxing unterstützt. Dieser Operator kann nicht neu definiert werden.  
  
 Weitere Informationen finden Sie unter [implizites Boxing](../../windows/boxing-cpp-component-extensions.md).  
  
 Im folgende Beispiel wird C3638 generiert:  
  
```  
// C3638.cpp  
// compile with: /clr  
value struct V {  
   V(){}  
   static operator V^(V);   // C3638  
};  
  
int main() {  
   V myV;  
   V ^ pmyV = myV;   // operator supports implicit boxing  
}  
```