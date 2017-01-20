---
title: "&#39;&lt;Schl&#252;sselwort&gt;&#39; ist innerhalb einer Struktur ung&#252;ltig."
ms.custom: na
ms.date: "11/16/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: na
ms.suite: na
ms.technology: 
  - "devlang-visual-basic"
ms.tgt_pltfrm: na
ms.topic: "article"
f1_keywords: 
  - "bc30044"
  - "vbc30044"
helpviewer_keywords: 
  - "BC30044"
ms.assetid: 252510cf-e084-47e4-9592-4aa8f94fabe4
caps.latest.revision: 8
caps.handback.revision: "8"
ms.author: "shoag"
manager: "wpickett"
---
# &#39;&lt;Schl&#252;sselwort&gt;&#39; ist innerhalb einer Struktur ung&#252;ltig.
Strukturen sind Werttypen, keine Verweistypen. Eine Struktur ist keine aus einer Klasse erstellte Instanz, daher sind die Schlüsselwörter `Me`, `MyClass` und `MyBase` in einer Struktur bedeutungslos.  
  
 **Fehler\-ID:** BC30044  
  
### So beheben Sie diesen Fehler  
  
-   Ändern Sie die Struktur in eine Klasse, oder entfernen Sie das Schlüsselwort aus der Prozedur.  
  
## Siehe auch  
 [Me](assetId:///a65973c7-cf06-4547-9b25-9fba885525c2)   
 [MyClass – löschen](assetId:///5db36f9b-f796-4b6a-ba34-cac1fde6eb62)   
 [MyBase \- löschen](assetId:///52491d06-6451-4f6f-9aa6-8fab59bbc2b9)   
 [Inheritance Basics](../Topic/Inheritance%20Basics%20\(Visual%20Basic\).md)