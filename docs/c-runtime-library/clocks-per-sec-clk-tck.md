---
title: "CLOCKS_PER_SEC, CLK_TCK | Microsoft Docs"
ms.custom: ""
ms.date: "11/04/2016"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-cpp"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "CLOCKS_PER_SEC"
  - "CLK_TCK"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "CLK_TCK-Konstante"
  - "CLOCKS_PER_SEC"
ms.assetid: bc285106-383d-44cb-91bf-276ad7de57bf
caps.latest.revision: 6
author: "corob-msft"
ms.author: "corob"
manager: "ghogen"
caps.handback.revision: 6
---
# CLOCKS_PER_SEC, CLK_TCK
[!INCLUDE[vs2017banner](../assembler/inline/includes/vs2017banner.md)]

## Syntax  
  
```  
  
#include <time.h>  
```  
  
## Hinweise  
 Die Zeit in Sekunden ist der Wert, der von der Funktion `clock` zurückgegeben wird, geteilt durch `CLOCKS_PER_SEC`.  `CLK_TCK` ist entsprechend, jedoch veraltet betrachtet.  
  
## Siehe auch  
 [Uhr](../c-runtime-library/reference/clock.md)   
 [Globale Konstanten](../c-runtime-library/global-constants.md)