---
title: "Compilerfehler CS1562"
ms.custom: na
ms.date: "11/17/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: na
ms.suite: na
ms.technology: 
  - "devlang-csharp"
ms.tgt_pltfrm: na
ms.topic: "article"
f1_keywords: 
  - "CS1562"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS1562"
ms.assetid: fbadbcc6-9cf2-4af6-b372-fd4e4da4402e
caps.latest.revision: 7
caps.handback.revision: "7"
ms.author: "wiwagn"
manager: "wpickett"
---
# Compilerfehler CS1562
Für Ausgaben ohne Quelle muss die Option \/out angeben werden.  
  
 Die Kompilierung könnte eine Ausgabedatei erstellt, aber es wurde keine Quellcodedatei als Eingabe verwendet, aus der der Name der Ausgabedatei abgeleitet werden kann. Beispielsweise können Sie versuchen, eine reine Metadaten\- oder reine Ressourcendatei zu kompilieren.  
  
 Verwenden Sie die Compileroption [\/out](../Topic/-out%20\(C%23%20Compiler%20Options\).md) zum Angeben des Namens der Ausgabedatei.