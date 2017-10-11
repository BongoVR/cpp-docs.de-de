---
title: Compilerfehler C3821 | Microsoft Docs
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- cpp-tools
ms.tgt_pltfrm: 
ms.topic: error-reference
f1_keywords:
- C3821
dev_langs:
- C++
helpviewer_keywords:
- C3821
ms.assetid: 2b327c7a-5faf-443c-ae82-944fae25b4df
caps.latest.revision: 12
author: corob-msft
ms.author: corob
manager: ghogen
ms.translationtype: MT
ms.sourcegitcommit: 35b46e23aeb5f4dbfd2a0dd44b906389dd5bfc88
ms.openlocfilehash: 47e0a2ed3c824ed1598f7e998d4966b95cc9233b
ms.contentlocale: de-de
ms.lasthandoff: 10/10/2017

---
# <a name="compiler-error-c3821"></a>Compilerfehler C3821
'Funktion': verwaltete Typ oder die Funktion kann nicht in eine nicht verwaltete Funktion verwendet werden  
  
 Funktionen mit Inlineassembly oder [Setjmp](../../c-runtime-library/reference/setjmp.md) Werttypen oder verwaltete Klassen sind nicht zulässig. Um diesen Fehler zu beheben, entfernen Sie die Inlineassembly und `setjmp` oder entfernen Sie die verwalteten Objekte.  
  
 C3821 kann auch auftreten, wenn Sie versuchen, die automatische Speicherung in einer Vararg-Funktion verwenden.  Weitere Informationen finden Sie unter [Variablenargumentlisten (...) (C + C++ / CLI) ](../../windows/variable-argument-lists-dot-dot-dot-cpp-cli.md) und [C++-Stapelsemantik für Referenztypen](../../dotnet/cpp-stack-semantics-for-reference-types.md).  
  
## <a name="example"></a>Beispiel  
 Im folgenden Beispiel wird C3821 generiert.  
  
```  
// C3821a.cpp  
// compile with: /clr /c  
public ref struct R {};  
void test1(...) {  
   R r;   // C3821  
}  
```  
  
## <a name="example"></a>Beispiel  
 Im folgenden Beispiel wird C3821 generiert.  
  
```  
// C3821b.cpp  
// compile with: /clr  
// processor: /x86  
ref class A {  
   public:  
   int i;  
};  
  
int main() {  
   // cannot use managed classes in this function  
   A ^a;     
  
   __asm {  
      nop  
   }  
} // C3821  
```  

