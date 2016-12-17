---
title: "Konvertierungsoperatoren k&#246;nnen keine Konvertierung in einen Schnittstellentyp durchf&#252;hren."
ms.custom: na
ms.date: "12/15/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: na
ms.suite: na
ms.technology: 
  - "devlang-visual-basic"
ms.tgt_pltfrm: na
ms.topic: "article"
f1_keywords: 
  - "vbc33025"
  - "bc33025"
helpviewer_keywords: 
  - "BC33025"
ms.assetid: 7e13dfa3-2b70-4ca6-a8ec-159131fd2c4c
caps.latest.revision: 9
caps.handback.revision: "9"
ms.author: "shoag"
manager: "wpickett"
---
# Konvertierungsoperatoren k&#246;nnen keine Konvertierung in einen Schnittstellentyp durchf&#252;hren.
Ein Konvertierungsoperator wird mit einem Schnittstellentyp als Rückgabetyp deklariert.  
  
 Zum Zeitpunkt der Kompilierung geht [!INCLUDE[vbprvb](../dotnet/includes/vbprvb_md.md)] davon aus, dass eine vordefinierte Konvertierung von einem beliebigen Verweistyp in eine beliebige Schnittstelle vorhanden ist. Eine derartige Konvertierung kann zur Laufzeit einen Fehler verursachen. Der Compiler kann jedoch keine Laufzeitergebnisse vorhersagen und lässt daher das Kompilieren solcher Konvertierungen zu.  
  
 Da der Compiler diese Konvertierung als bereits definiert ansieht, lässt er ein erneutes Definieren dieser Konvertierung nicht zu.  
  
 **Fehler\-ID:** BC33025  
  
### So beheben Sie diesen Fehler  
  
-   Entfernen Sie diese Operatordefinition vollständig. Sie ist bereits vordefiniert.  
  
## Siehe auch  
 [Operator Procedures](../Topic/Operator%20Procedures%20\(Visual%20Basic\).md)   
 [Operator Statement](../Topic/Operator%20Statement.md)   
 [How to: Define an Operator](../Topic/How%20to:%20Define%20an%20Operator%20\(Visual%20Basic\).md)   
 [How to: Define a Conversion Operator](../Topic/How%20to:%20Define%20a%20Conversion%20Operator%20\(Visual%20Basic\).md)