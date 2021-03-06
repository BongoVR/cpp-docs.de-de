---
title: Compilerwarnung (Stufe 4) C4365 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C4365
dev_langs:
- C++
helpviewer_keywords:
- C4365
ms.assetid: af4b4191-bdfd-4dbb-8229-3ba4405df257
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 496f26046803efdd2b67cdc6d5a5ec74a3cbb90d
ms.sourcegitcommit: 76b7653ae443a2b8eb1186b789f8503609d6453e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/04/2018
---
# <a name="compiler-warning-level-4-c4365"></a>Compilerwarnung (Stufe 4) C4365
'Action': Konvertierung von 'type_1' zu 'type_2', signed/unsigned-Konflikt  
  
 Sie haben beispielsweise versucht, einen Wert ohne Vorzeichen in einen Wert mit Vorzeichen zu konvertieren.  
  
 C4365 ist standardmäßig deaktiviert.  Weitere Informationen finden Sie unter [Compiler Warnings That Are Off by Default](../../preprocessor/compiler-warnings-that-are-off-by-default.md).  
  
## <a name="example"></a>Beispiel  
 Im folgenden Beispiel wird C4365 generiert.  
  
```  
// C4365.cpp  
// compile with: /W4  
#pragma warning(default:4365)  
  
int f(int) { return 0; }  
void Test(size_t i) {}  
  
int main() {  
   unsigned int n = 10;  
   int o = 10;  
   n++;  
   f(n);   // C4365  
   f(o);   // OK  
  
   Test( -19 );   // C4365  
}  
```