---
title: Compilerfehler Fehler C2711 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2711
dev_langs:
- C++
helpviewer_keywords:
- C2711
ms.assetid: 9df9f808-7419-4e63-abdd-e6538ff0871f
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: fb2e5c904d7f6d865b94ea4fb4ba65be4c974f8b
ms.sourcegitcommit: 76b7653ae443a2b8eb1186b789f8503609d6453e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/04/2018
---
# <a name="compiler-error-c2711"></a>Compilerfehler Fehler C2711
'Funktion': Diese Funktion kann nicht als verwaltet kompiliert, erwägen Sie, die nicht verwaltete #pragma verwenden  
  
 Einige Anweisungen werden verhindert, dass den Compiler MSIL für die einschließende Funktion generiert wurde.  
  
 Im folgenden Beispiel wird C2711 generiert:  
  
```  
// C2711.cpp  
// compile with: /clr  
// processor: x86  
using namespace System;  
value struct V {  
   static const t = 10;  
};  
  
void bar() {  
   V::t;  
   __asm int 3   // C2711 inline asm can't be compiled managed  
}  
```