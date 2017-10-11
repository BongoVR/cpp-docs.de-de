---
title: Compilerfehler Fehler C2429 | Microsoft Docs
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- cpp-tools
ms.tgt_pltfrm: 
ms.topic: error-reference
f1_keywords:
- C2429
dev_langs:
- C++
helpviewer_keywords:
- C2429
ms.assetid: 57ff6df9-5cf1-49f3-8bd8-4e550dfd65a0
caps.latest.revision: 9
author: corob-msft
ms.author: corob
manager: ghogen
ms.translationtype: MT
ms.sourcegitcommit: 35b46e23aeb5f4dbfd2a0dd44b906389dd5bfc88
ms.openlocfilehash: 18fd64199ff043b660bb205199b982ee2843cdcd
ms.contentlocale: de-de
ms.lasthandoff: 10/09/2017

---
# <a name="compiler-error-c2429"></a>Compilerfehler Fehler C2429
"*Sprachfunktion*"erfordert compilerkennzeichen"*Compileroption*"  
  
Die Language-Funktion erfordert eine bestimmte Compileroption für die Unterstützung.  
  
Der Fehler C2429: Sprachfunktion 'geschachtelt-Namespace-Definition' erfordert compilerkennzeichen "/ Std:c ++ neueste" wird generiert, wenn Sie versuchen, Sie definieren eine *zusammengesetzten Namespace*, einen Namespace, eine oder mehrere Bereich geschachtelten Namespace-Namen enthält, , starten Visual Studio 2015 Update 3. Zusammengesetzte Namespace Definitionen in C++ vor C ++ 17 sind nicht zulässig. Der Compiler unterstützt zusammengesetzten Namespacedefinitionen bei der [/std:c ++ neueste](../../build/reference/std-specify-language-standard-version.md) -Compileroption angegeben ist:  
```cpp  
// C2429a.cpp  
namespace a::b { int i; } // C2429 starting in Visual C++ 2015 Update 3.  
                          // Use /std:c++latest to fix, or do this:  
// namespace a { namespace b { int i; }}  
  
int main() {  
   a::b::i = 2;  
}  
```  
