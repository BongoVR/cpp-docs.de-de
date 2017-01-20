---
title: "Entweder der Parametertyp oder der R&#252;ckgabetyp dieses Konvertierungsoperators muss dem enthaltenden &lt;Typ&gt;-Typ entsprechen."
ms.custom: na
ms.date: "11/17/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: na
ms.suite: na
ms.technology: 
  - "devlang-visual-basic"
ms.tgt_pltfrm: na
ms.topic: "article"
f1_keywords: 
  - "vbc33022"
  - "bc33022"
helpviewer_keywords: 
  - "BC33022"
ms.assetid: 55baff11-eb35-4c81-bc04-5006524ab450
caps.latest.revision: 9
caps.handback.revision: "9"
ms.author: "shoag"
manager: "wpickett"
---
# Entweder der Parametertyp oder der R&#252;ckgabetyp dieses Konvertierungsoperators muss dem enthaltenden &lt;Typ&gt;-Typ entsprechen.
Eine Definition eines Konvertierungsoperators gibt sowohl den Parameter als auch den Rückgabetyp mit anderen Typen als dem Typ der Klasse oder Struktur an, in der der Operator definiert ist.  
  
 Wenn Sie einen Konvertierungsoperator in einer Klasse oder Struktur definieren, muss er in den oder aus dem Typ der Klasse oder Struktur konvertieren.  
  
 **Fehler\-ID:** BC33022  
  
### So beheben Sie diesen Fehler  
  
-   Ändern Sie den Parametertyp oder den Rückgabetyp in den Typ der Klasse oder Struktur, in der der Operator definiert ist.  
  
## Siehe auch  
 [Operator Procedures](../Topic/Operator%20Procedures%20\(Visual%20Basic\).md)   
 [Operator Statement](../Topic/Operator%20Statement.md)   
 [How to: Define an Operator](../Topic/How%20to:%20Define%20an%20Operator%20\(Visual%20Basic\).md)   
 [How to: Define a Conversion Operator](../Topic/How%20to:%20Define%20a%20Conversion%20Operator%20\(Visual%20Basic\).md)