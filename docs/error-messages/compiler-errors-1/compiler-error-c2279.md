---
title: Compilerfehler C2279 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2279
dev_langs:
- C++
helpviewer_keywords:
- C2279
ms.assetid: 1b5c88ef-2336-49b8-9ddb-d61f97c73e14
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: c1eb468ccf5d099745c5d4a30eaec2f38f015a58
ms.sourcegitcommit: 76b7653ae443a2b8eb1186b789f8503609d6453e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/04/2018
---
# <a name="compiler-error-c2279"></a>Compilerfehler C2279
Ausnahmespezifikation kann nicht in einer Typedef-Deklaration angezeigt werden.  
  
 Klicken Sie unter **"/ Za"**, [Ausnahmespezifikationen](../../cpp/exception-specifications-throw-cpp.md) sind in einer Typedef-Deklaration nicht zulässig.  
  
 Im folgende Beispiel wird C2279 generiert:  
  
```  
// C2279.cpp  
// compile with: /Za /c  
typedef int (*xy)() throw(...);   // C2279  
typedef int (*xyz)();   // OK  
```