---
title: "Compilerwarnung (Stufe 1) C4293 | Microsoft Docs"
ms.custom: ""
ms.date: "11/04/2016"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-cpp"
ms.tgt_pltfrm: ""
ms.topic: "error-reference"
f1_keywords: 
  - "C4293"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "C4293"
ms.assetid: babecd96-eb51-41a5-9835-462c7a46dbad
caps.latest.revision: 7
author: "corob-msft"
ms.author: "corob"
manager: "ghogen"
caps.handback.revision: 7
---
# Compilerwarnung (Stufe 1) C4293
[!INCLUDE[vs2017banner](../../assembler/inline/includes/vs2017banner.md)]

'Operator' : Eine Verschiebung wurde mit einem negativen oder zu großen Wert aufgerufen, nicht definiertes Verhalten  
  
 Wenn eine Verschiebung mit einem negativen oder zu großen Wert aufgerufen wird, ist das Verhalten des resultierenden Abbildes nicht definiert.  
  
## Beispiel  
 Im folgenden Beispiel wird C4293 generiert:  
  
```  
// C4293.cpp  
// compile with: /c /W1  
unsigned __int64 combine (unsigned lo, unsigned hi) {  
  
   return (hi << 32) | lo;   // C4293  
  
   // try the following line instead  
   // return ( (unsigned __int64)hi << 32) | lo;  
}  
```