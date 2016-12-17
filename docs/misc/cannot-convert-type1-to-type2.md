---
title: "Der Typ &#39;Typ1&#39; kann nicht in &#39;Typ2&#39; konvertiert werden."
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
  - "bc31193"
  - "vbc31193"
helpviewer_keywords: 
  - "BC31193"
ms.assetid: f25a9f5b-7741-4cd6-b85a-b19037ed8e49
caps.latest.revision: 5
caps.handback.revision: "5"
ms.author: "shoag"
manager: "wpickett"
---
# Der Typ &#39;Typ1&#39; kann nicht in &#39;Typ2&#39; konvertiert werden.
Der Typ 'Typ1' kann nicht in 'Typ2' konvertiert werden. Rufen Sie mit der Value\-Eigenschaft den Zeichenfolgenwert des ersten Elements von „parentElement“ ab.  
  
 Es wurde versucht, ein XML\-Literal implizit in einen bestimmten Typ umzuwandeln. Das XML\-Literal kann nicht implizit in den angegebenen Typ umgewandelt werden.  
  
 **Fehler\-ID:** BC31193  
  
### So beheben Sie diesen Fehler  
  
-   Verwenden Sie die `Value`\-Eigenschaft des XML\-Literals, um auf dessen Wert als `String` zu verweisen. Verwenden Sie die `CType`\-Funktion, eine weitere Typkonvertierungsfunktion, oder die <xref:System.Convert>\-Klasse, um den Wert in den angegebenen Typ umzuwandeln.  
  
## Siehe auch  
 <xref:System.Convert>   
 [Accessing XML in Visual Basic](../Topic/Accessing%20XML%20in%20Visual%20Basic.md)   
 [Type Conversion Functions](../Topic/Type%20Conversion%20Functions%20\(Visual%20Basic\).md)   
 [XML Literals](../Topic/XML%20Literals%20\(Visual%20Basic\).md)   
 [XML](../Topic/XML%20in%20Visual%20Basic.md)