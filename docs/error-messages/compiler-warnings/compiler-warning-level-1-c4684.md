---
title: Compilerwarnung (Stufe 1) C4684 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C4684
dev_langs:
- C++
helpviewer_keywords:
- C4684
ms.assetid: e95f1a83-2784-4b05-ae94-12148e056e26
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: cba83467e4705323eaecd990a7c5c32777990ffb
ms.sourcegitcommit: 76b7653ae443a2b8eb1186b789f8503609d6453e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/04/2018
---
# <a name="compiler-warning-level-1-c4684"></a>Compilerwarnung (Stufe 1) C4684
'Attribut': Warnung!! Attribut kann dazu führen, dass ungültige codegenerierung: mit Vorsicht verwenden  
  
 Sie verwendet ein Attribut, das im Allgemeinen nicht verwendet werden soll.  
  
 Im folgenden Beispiel wird C4684 generiert:  
  
```  
// C4684.cpp  
// compile with: /W1 /LD  
 [module(name="xx")]; // C4684 expected  
[no_injected_text];  
```