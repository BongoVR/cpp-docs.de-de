---
title: Compilerfehler C2448 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2448
dev_langs:
- C++
helpviewer_keywords:
- C2448
ms.assetid: e255df3c-f861-4b4d-a193-8768cef061a5
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: bcc62d7aeba0a128c9b736586e6c1502227de717
ms.sourcegitcommit: 76b7653ae443a2b8eb1186b789f8503609d6453e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/04/2018
---
# <a name="compiler-error-c2448"></a>Compilerfehler C2448
'Bezeichner': im Funktionsformat Initialisierer anscheinend einer Funktionsdefinition  
  
 Definition der Funktion ist falsch.  
  
 Dieser Fehler kann durch eine Programmiersprache C-Parameterliste im alten Stil verursacht werden.  
  
 Im folgende Beispiel wird C2448 generiert:  
  
```  
// C2448.cpp  
void func(c)  
   int c;  
{}   // C2448  
```