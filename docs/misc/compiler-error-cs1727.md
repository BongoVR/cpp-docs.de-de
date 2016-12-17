---
title: "Compilerfehler CS1727"
ms.custom: na
ms.date: "12/15/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: na
ms.suite: na
ms.technology: 
  - "devlang-csharp"
ms.tgt_pltfrm: na
ms.topic: "article"
f1_keywords: 
  - "CS1727"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS1727"
ms.assetid: 66478a58-e0f6-4886-b940-5473ad485a01
caps.latest.revision: 5
caps.handback.revision: "5"
ms.author: "wiwagn"
manager: "wpickett"
---
# Compilerfehler CS1727
Der Fehlerbericht kann ohne Autorisierung nicht automatisch gesendet werden. Wechseln Sie zu "", um das Senden des Fehlerberichts zu autorisieren.  
  
 Auf der im Fehlertext aufgeführten Website wird erläutert, wie die automatische Fehlerberichterstattung für Befehlszeilentools von [!INCLUDE[vsprvslong](../error-messages/compiler-errors-1/includes/vsprvslong_md.md)] aktiviert wird.  
  
## Beispiel  
 Im folgenden Beispiel wird CS1727 generiert.  
  
```  
// CS1727.cs // compile with: /errorreport:send // CS1727 expected class Test { static void Main(){} }  
```  
  
## Siehe auch  
 [\/errorreport \(Set Error Reporting Behavior\)](../Topic/-errorreport%20\(C%23%20Compiler%20Options\).md)