---
title: Compiler-Fehler C2628 generiert | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2628
dev_langs:
- C++
helpviewer_keywords:
- C2628
ms.assetid: 19a25e77-d5be-4107-88d5-0745b6281f98
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: b3f9813f103f59e61093ab82366e50a7ef6dae46
ms.sourcegitcommit: 76b7653ae443a2b8eb1186b789f8503609d6453e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/04/2018
---
# <a name="compiler-error-c2628"></a>Compiler-Fehler C2628 generiert
"Typ1", gefolgt von "Typ2" ist ungültig (haben Sie vergessen ein ";"?)  
  
 Möglicherweise fehlt ein Semikolon.  
  
 Im folgende Beispiel wird C2628 generiert:  
  
```  
// C2628.cpp  
class CMyClass {}  
int main(){}   // C2628 error  
```  
  
 Mögliche Lösung:  
  
```  
// C2628b.cpp  
class CMyClass {};  
int main(){}  
```