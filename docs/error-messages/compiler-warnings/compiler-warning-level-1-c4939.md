---
title: "Compilerwarnung (Stufe 1) C4939 | Microsoft Docs"
ms.custom: ""
ms.date: "11/04/2016"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-csharp"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "C4939"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "C4939"
ms.assetid: 07096008-ba47-436c-a84c-2b03ad90d0b3
caps.latest.revision: 5
author: "corob-msft"
ms.author: "corob"
manager: "ghogen"
caps.handback.revision: 5
---
# Compilerwarnung (Stufe 1) C4939
[!INCLUDE[vs2017banner](../../assembler/inline/includes/vs2017banner.md)]

\#pragma vtordisp ist veraltet und wird in einer der nächsten Versionen von Visual C\+\+ entfernt.  
  
 Das [vtordisp](../../preprocessor/vtordisp.md)\-Pragma wird in einer der nächsten Versionen von Visual C\+\+ entfernt.  
  
## Beispiel  
 Im folgenden Beispiel wird C4939 generiert.  
  
```  
// C4939.cpp // compile with: /c /W1 #pragma vtordisp(off)   // C4939  
```