---
title: "Compilerfehler C2150"
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
  - "C2150"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "C2150"
ms.assetid: 21e82a10-c1d4-4c0d-9dc6-c5d92ea42a31
caps.latest.revision: 9
caps.handback.revision: "9"
ms.author: "corob"
manager: "ghogen"
---
# Compilerfehler C2150
[!INCLUDE[vs2017banner](../../assembler/inline/includes/vs2017banner.md)]

'identifizierer': Das Bitfeld muss den Typ 'int', 'signed int' oder 'unsigned int' aufweisen  
  
 Bitfelder müssen `int`, `signed` `int` oder `unsigned` `int` sein.  
  
 Im folgenden Beispiel wird C2150 generiert:  
  
```  
// C2150.cpp // compile with: /c struct A { float a : 8;    // C2150 int i : 8;   // OK };  
```