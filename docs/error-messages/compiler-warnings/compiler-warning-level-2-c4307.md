---
title: Compilerwarnung (Stufe 2) C4307 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C4307
dev_langs:
- C++
helpviewer_keywords:
- C4307
ms.assetid: 7cca11e9-be61-49e4-8b15-88b84f0cbf07
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 52914fc5825bda5647308c006b853538f3d6225e
ms.sourcegitcommit: 76b7653ae443a2b8eb1186b789f8503609d6453e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/04/2018
---
# <a name="compiler-warning-level-2-c4307"></a>Compilerwarnung (Stufe 2) C4307
'Operator': Überlauf einer ganzzahligen Konstanten  
  
 Der Operator wird in einem Ausdruck verwendet, der eine ganzzahlige Konstante, die für dieses Volume zugewiesene Speicherplatz Überlaufs ausgibt. Sie müssen möglicherweise einen größeren Typ für die Konstante verwenden. Ein **signiert Int** enthält einen kleineren Wert als ein `unsigned int` da die **signiert Int** verwendet ein Bit, die Vorzeichen darstellen.  
  
 Im folgenden Beispiel wird C4307 generiert:  
  
```  
// C4307.cpp  
// compile with: /W2  
int i = 2000000000 + 2000000000;   // C4307  
int j = (unsigned)2000000000 + 2000000000;   // OK  
  
int main()  
{  
}  
```