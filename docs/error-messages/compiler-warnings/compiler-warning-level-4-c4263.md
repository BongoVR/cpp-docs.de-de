---
title: Compilerwarnung (Stufe 4) C4263 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C4263
dev_langs:
- C++
helpviewer_keywords:
- C4263
ms.assetid: daabb05d-ab56-460f-ab6c-c74d222ef649
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 883b36e524f3631811cf503ebc695e3c4ad53da2
ms.sourcegitcommit: 76b7653ae443a2b8eb1186b789f8503609d6453e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/04/2018
---
# <a name="compiler-warning-level-4-c4263"></a>Compilerwarnung (Stufe 4) C4263
'Funktion': Memberfunktion überschreibt keine virtuelle Memberfunktion Basisklasse nicht  
  
 Definition einer Funktion hat den gleichen Namen wie eine virtuelle Funktion in einer Basisklasse jedoch nicht dieselbe Anzahl bzw. Art von Argumenten. So wird effektiv die virtuelle Funktion in der Basisklasse ausgeblendet.  
  
 Diese Warnung ist standardmäßig deaktiviert. Weitere Informationen finden Sie unter [Standardmäßig deaktivierte Compilerwarnungen](../../preprocessor/compiler-warnings-that-are-off-by-default.md) .  
  
 Im folgenden Beispiel wird C4263 generiert:  
  
```  
// C4263.cpp  
// compile with: /W4  
#pragma warning(default:4263)  
#pragma warning(default:4264)  
class B {  
public:  
   virtual void func();  
};  
  
class D : public B {  
   void func(int);   // C4263  
};  
  
int main() {  
}  
```