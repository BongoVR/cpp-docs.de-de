---
title: Compilerwarnung (Stufe 1) C4216 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C4216
dev_langs:
- C++
helpviewer_keywords:
- C4216
ms.assetid: 211079dc-59d0-42a7-801c-2ddab21d7232
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 2de645b2d036e7ed696a8065bbb9f8212ec5c596
ms.sourcegitcommit: 76b7653ae443a2b8eb1186b789f8503609d6453e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/04/2018
---
# <a name="compiler-warning-level-1-c4216"></a>Compilerwarnung (Stufe 1) C4216
nicht dem Standard entsprechende Erweiterung: long float  
  
 Die Standard-Microsoft-Erweiterungen (/ Ze) behandeln **lange float** als **doppelte**. ANSI-Kompatibilität (["/ Za"](../../build/reference/za-ze-disable-language-extensions.md)) nicht. Verwendung **doppelte** um Kompatibilität zu gewährleisten. Im folgenden Beispiel wird C4216 generiert:  
  
```  
// C4216.cpp  
// compile with: /W1  
float long a;   // C4216  
  
// use the line below to resolve the warning  
// double a;  
  
int main() {  
}  
```