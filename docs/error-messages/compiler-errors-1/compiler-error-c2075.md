---
title: "Compilerfehler C2075 | Microsoft Docs"
ms.custom: ""
ms.date: "11/04/2016"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-csharp"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "C2075"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "C2075"
ms.assetid: 8b1865d2-540b-4117-b982-e7a58a0b6cf7
caps.latest.revision: 7
author: "corob-msft"
ms.author: "corob"
manager: "ghogen"
caps.handback.revision: 7
---
# Compilerfehler C2075
[!INCLUDE[vs2017banner](../../assembler/inline/includes/vs2017banner.md)]

"Bezeichner": für die Initialisierung eines Arrays sind geschweifte Klammern erforderlich  
  
 Der angegebene Arrayinitialisierer war nicht in geschweifte Klammern eingeschlossen.  
  
 Im folgenden Beispiel wird C2075 generiert:  
  
```  
// C2075.c int main() { int i[] = 1, 2, 3 };   // C2075 }  
```  
  
 Mögliche Lösung:  
  
```  
// C2075b.c int main() { int j[] = { 1, 2, 3 }; }  
```