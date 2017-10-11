---
title: Compilerfehler C3418 | Microsoft Docs
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- cpp-tools
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- C3418
dev_langs:
- C++
helpviewer_keywords:
- C3418
ms.assetid: 54042c04-3c45-41c1-bad7-90f9ee05a21b
caps.latest.revision: 5
author: corob-msft
ms.author: corob
manager: ghogen
ms.translationtype: MT
ms.sourcegitcommit: 35b46e23aeb5f4dbfd2a0dd44b906389dd5bfc88
ms.openlocfilehash: 0ae644c17a39e574984dc8bb0689955fd1bef2be
ms.contentlocale: de-de
ms.lasthandoff: 10/10/2017

---
# <a name="compiler-error-c3418"></a>Compilerfehler C3418
Der Zugriffsspezifizierer "Spezifizierer" wird nicht unterstützt.  
  
Ein CLR-Zugriffsspezifizierer wurde falsch angegeben.  Weitere Informationen finden Sie unter typsichtbarkeit und membersichtbarkeit in [wie: definieren und Verarbeiten von Klassen und Strukturen (C + c++ / CLI)](../../dotnet/how-to-define-and-consume-classes-and-structs-cpp-cli.md).  
  
## <a name="example"></a>Beispiel  
Im folgenden Beispiel wird C3418 generiert:  
  
```cpp  
// C3418.cpp  
// compile with: /clr /c  
ref struct m {  
internal public:   // C3418  
   void test(){}  
};  
  
ref struct n {  
internal:   // OK  
   void test(){}  
};  
```
