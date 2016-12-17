---
title: "Der Operator &#39;&lt;operator&gt;&#39; muss einen zweiten Parameter vom Typ &#39;Integer&#39; aufweisen"
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
  - "BC33041"
  - "vbc33041"
helpviewer_keywords: 
  - "BC33041"
ms.assetid: 5cd56f6d-2f0f-49de-a8e6-59bdb57bdb1d
caps.latest.revision: 9
caps.handback.revision: "9"
ms.author: "shoag"
manager: "wpickett"
---
# Der Operator &#39;&lt;operator&gt;&#39; muss einen zweiten Parameter vom Typ &#39;Integer&#39; aufweisen
Ein Bitverschiebungsoperator ist mit einem zweiten Parameter von einem anderen Typ als `Integer` deklariert.  
  
 Wenn Sie den rechten \(`>>`\) oder linken \(`<<`\) Verschiebeoperator in einem Ausdruck verwenden, geben Sie den Betrag der Verschiebung im zweiten Operanden an. Für diesen Operanden gestattet Ihnen [!INCLUDE[vbprvb](../dotnet/includes/vbprvb_md.md)] die Angabe beliebiger Datentypen, die sich zu `Integer` erweitern lassen. Die Definition des zweiten Operanden ist jedoch streng `Integer`. Wenn Sie eine Klasse oder Struktur mit einem Bitverschiebungsoperator für diese Klasse oder Struktur definieren, muss die Definition `Integer` für den zweiten Operanden angeben.  
  
 **Fehler\-ID:** BC33041  
  
### So beheben Sie diesen Fehler  
  
-   Ändern Sie die Definition des Bitverschiebungsoperators so, dass ein `Integer`\-Wert zurückgegeben wird.  
  
## Siehe auch  
 [Operator Procedures](../Topic/Operator%20Procedures%20\(Visual%20Basic\).md)   
 [Operator Statement](../Topic/Operator%20Statement.md)   
 [How to: Define an Operator](../Topic/How%20to:%20Define%20an%20Operator%20\(Visual%20Basic\).md)   
 [How to: Define a Conversion Operator](../Topic/How%20to:%20Define%20a%20Conversion%20Operator%20\(Visual%20Basic\).md)   
 [Bit Shift Operators](../Topic/Bit%20Shift%20Operators%20\(Visual%20Basic\).md)