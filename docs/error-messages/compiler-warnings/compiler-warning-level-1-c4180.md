---
title: "Compilerwarnung (Stufe 1) C4180"
ms.custom: na
ms.date: "12/03/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: na
ms.suite: na
ms.technology: 
  - "devlang-csharp"
ms.tgt_pltfrm: na
ms.topic: "article"
f1_keywords: 
  - "C4180"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "C4180"
ms.assetid: 40c91bd4-37f1-4d59-a4f3-d5ddab68239b
caps.latest.revision: 8
caps.handback.revision: "8"
ms.author: "corob"
manager: "ghogen"
---
# Compilerwarnung (Stufe 1) C4180
[!INCLUDE[vs2017banner](../../assembler/inline/includes/vs2017banner.md)]

Auf Funktionstyp angewendeter Qualifizierer ist ohne Bedeutung; wird ignoriert  
  
 Ein Qualifizierer, z. B. **const**, wird auf einen durch `typedef` definierten Funktionstyp angewendet.  
  
## Beispiel  
  
```  
// C4180.cpp // compile with: /W1 /c typedef int FuncType(void); // the const qualifier cannot be applied to the // function type FuncType const FuncType f;   // C4180  
```