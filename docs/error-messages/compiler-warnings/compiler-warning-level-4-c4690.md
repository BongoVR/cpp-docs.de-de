---
title: Compilerwarnung (Stufe 4) C4690 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C4690
dev_langs:
- C++
helpviewer_keywords:
- C4690
ms.assetid: 080a0ea1-458b-477b-a37a-4a34c94709ff
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 7c8285fd3763b93c8a320a6cb984168b88d2e9ae
ms.sourcegitcommit: 76b7653ae443a2b8eb1186b789f8503609d6453e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/04/2018
---
# <a name="compiler-warning-level-4-c4690"></a>Compilerwarnung (Stufe 4) C4690
[ emitidl( pop ) ] : Mehr pop- als push-Vorgänge  
  
 Das [emitidl](../../windows/emitidl.md) -Attribut wurde einmal mehr vom Stapel abgerufen als in den Stapel verschoben.  
  
## <a name="example"></a>Beispiel  
 Im folgenden Beispiel wird C4690 generiert.  
  
```  
// C4690.cpp  
// compile with: /c /W4  
[emitidl(pop)];   // C4690  
class x {};  
```