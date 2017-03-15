---
title: "Compilerfehler C2042 | Microsoft Docs"
ms.custom: ""
ms.date: "11/04/2016"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-csharp"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "C2042"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "C2042"
ms.assetid: e111788f-41ce-405a-9824-a4c1c26059e6
caps.latest.revision: 8
author: "corob-msft"
ms.author: "corob"
manager: "ghogen"
caps.handback.revision: 8
---
# Compilerfehler C2042
[!INCLUDE[vs2017banner](../../assembler/inline/includes/vs2017banner.md)]

Die Schlüsselwörter "signed\/unsigned" schließen sich gegenseitig aus  
  
 Die Schlüsselwörter `signed` und `unsigned` werden innerhalb der gleichen Deklaration verwendet.  
  
 Im folgenden Beispiel wird C2042 generiert:  
  
```  
// C2042.cpp unsigned signed int i;   // C2042  
```  
  
 Mögliche Lösung:  
  
```  
// C2042b.cpp // compile with: /c unsigned int i; signed int ii;  
```