---
title: Compilerwarnung (Stufe 4) C4515 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C4515
dev_langs:
- C++
helpviewer_keywords:
- C4515
ms.assetid: 167b5177-3f89-418b-b6c8-7de634f6b28f
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 42bdf6edbd55f533a01c5c430ed328ded7e71dde
ms.sourcegitcommit: 76b7653ae443a2b8eb1186b789f8503609d6453e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/04/2018
---
# <a name="compiler-warning-level-4-c4515"></a>Compilerwarnung (Stufe 4) C4515
'Namespace': Namespace verwendet selbst  
  
 Ein Namespace ist rekursiv verwendet.  
  
 Im folgenden Beispiel wird C4515 generiert:  
  
```  
// C4515.cpp  
// compile with: /W4  
namespace A  
{  
   using namespace A; // C4515  
}  
  
int main()  
{  
}  
```