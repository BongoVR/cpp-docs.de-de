---
title: Compilerwarnung (Stufe 1) C4552 | Microsoft Docs
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- cpp-tools
ms.tgt_pltfrm: 
ms.topic: error-reference
f1_keywords:
- C4552
dev_langs:
- C++
helpviewer_keywords:
- C4552
ms.assetid: ebbbb5ee-1c19-45bd-b386-41a19630fc76
caps.latest.revision: 
author: corob-msft
ms.author: corob
manager: ghogen
ms.workload:
- cplusplus
ms.openlocfilehash: fb12d5774094040a3caacba8c0cdfe8d8b604252
ms.sourcegitcommit: 8fa8fdf0fbb4f57950f1e8f4f9b81b4d39ec7d7a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/21/2017
---
# <a name="compiler-warning-level-1-c4552"></a>Compilerwarnung (Stufe 1) C4552
'Operator': Operator hat keine Auswirkungen; Operator mit Nebeneffekten erwartet  
  
 Wenn eine Ausdrucksanweisung ein Operator mit keine Nebeneffekt als Anfang der Ausdruck verwendet, ist es wahrscheinlich einen Fehler aus.  
  
 Um diese Warnung zu überschreiben, setzen Sie den Ausdruck in Klammern ein.  
  
 Im folgenden Beispiel wird C4552 generiert:  
  
```  
// C4552.cpp  
// compile with: /W1  
int main() {  
   int i, j;  
   i + j;   // C4552  
   // try the following line instead  
   // (i + j);  
}  
```