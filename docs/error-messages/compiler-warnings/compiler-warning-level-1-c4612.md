---
title: Compilerwarnung (Stufe 1) C4612 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C4612
dev_langs:
- C++
helpviewer_keywords:
- C4612
ms.assetid: 21ac02b2-51cd-4aff-9b70-d543511d5962
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 0983f5d0bb89eaf1daee94468b318557bc83cd05
ms.sourcegitcommit: 76b7653ae443a2b8eb1186b789f8503609d6453e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/04/2018
---
# <a name="compiler-warning-level-1-c4612"></a>Compilerwarnung (Stufe 1) C4612
Fehler im Namen der Includedatei  
  
 Diese Warnung tritt bei **#pragma include_alias** auf, wenn ein Dateiname falsch ist oder fehlt.  
  
 Die Argumente für die **#pragma Include_alias** Anweisung können die anführung wie in (**"***Filename***"**) oder spitze Klammern wie ( **\< ***Filename***>**), aber beide müssen die gleiche Form.  
  
## <a name="example"></a>Beispiel  
  
```  
// C4612.cpp  
// compile with: /W1 /LD  
#pragma include_alias("StandardIO", <stdio.h>) // C4612  
```