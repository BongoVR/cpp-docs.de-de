---
title: "Compilerwarnung (Stufe 1) C4027 | Microsoft Docs"
ms.custom: ""
ms.date: "11/04/2016"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-csharp"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "C4027"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "C4027"
ms.assetid: f30d57b9-20c4-4284-8686-566d9f0ca7fc
caps.latest.revision: 6
author: "corob-msft"
ms.author: "corob"
manager: "ghogen"
caps.handback.revision: 6
---
# Compilerwarnung (Stufe 1) C4027
[!INCLUDE[vs2017banner](../../assembler/inline/includes/vs2017banner.md)]

Funktion ohne Liste formaler Parameter deklariert  
  
 Die Funktionsdeklaration weist keine formalen Parameter auf, aber es sind formale Parameter in der Funktionsdefinition bzw. übergebene Parameter in einem Aufruf verfügbar. Für nachfolgende Aufrufe dieser Funktion wird davon ausgegangen, dass die Funktion übergebene Parameter der Typen akzeptiert, die in der Funktionsdefinition oder dem Aufruf gefunden wurden.