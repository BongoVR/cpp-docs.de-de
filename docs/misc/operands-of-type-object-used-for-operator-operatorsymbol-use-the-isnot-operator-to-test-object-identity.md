---
title: "F&#252;r den &#39;&lt;Operatorsymbol&gt;&#39;-Operator werden Operanden vom Typ &#39;Object&#39; verwendet. Verwenden Sie den IsNot-Operator, um die Objektidentit&#228;t zu testen."
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
  - "vbc42032"
  - "bc42032"
helpviewer_keywords: 
  - "BC42032"
ms.assetid: f43b163b-f8f6-489d-ba9e-df6398ccc553
caps.latest.revision: 8
caps.handback.revision: "8"
ms.author: "shoag"
manager: "wpickett"
---
# F&#252;r den &#39;&lt;Operatorsymbol&gt;&#39;-Operator werden Operanden vom Typ &#39;Object&#39; verwendet. Verwenden Sie den IsNot-Operator, um die Objektidentit&#228;t zu testen.
Ein Ausdruck verwendet den `<>`\-Operator mit einem oder beiden Operanden des [Object Data Type](../Topic/Object%20Data%20Type.md)s.  
  
 Verwenden Sie den `Is`\- oder den `IsNot`\-Operator, um zu bestimmen, ob zwei Objektverweise auf die gleiche Objektinstanz verweisen. Siehe „Vergleichen von Objekten“ in [Comparison Operators in Visual Basic](../Topic/Comparison%20Operators%20in%20Visual%20Basic.md).  
  
 Wenn eine Variable oder ein Ausdruck `Object` ergibt, muss der Compiler die *späte Bindung* durchführen, die zur Laufzeit zusätzliche Vorgänge verursacht. Sie setzt die Anwendung zudem möglichen Laufzeitfehlern aus. Wenn Sie z. B. ein <xref:System.Windows.Forms.Form> einer `Object`\-Variablen zuweisen und dann mit dem `<>`\-Operator verwenden, löst die Laufzeit eine <xref:System.InvalidCastException> aus, da Visual Basic ein <xref:System.Windows.Forms.Form>\-Objekt nicht in einen Datentyp konvertieren kann, der für den Wertvergleich geeignet ist. Selbst wenn beide Operanden den Typ <xref:System.Windows.Forms.Form> ergeben, tritt bei dem Vorgang ein Fehler auf, weil `<>` nicht für <xref:System.Windows.Forms.Form>\-Operanden definiert ist.  
  
 Standardmäßig ist diese Meldung eine Warnung. Informationen zum Ausblenden von Warnungen oder zum Behandeln von Warnungen als Fehler finden Sie unter [Konfigurieren von Warnungen in Visual Basic](../Topic/Configuring%20Warnings%20in%20Visual%20Basic.md).  
  
 **Fehler\-ID:** BC42032  
  
### So beheben Sie diesen Fehler  
  
-   Verwenden Sie den `Is`\- oder den `IsNot`\-Operator, um zu bestimmen, ob zwei Objektverweise auf die gleiche Objektinstanz verweisen.  
  
## Siehe auch  
 [Comparison Operators in Visual Basic](../Topic/Comparison%20Operators%20in%20Visual%20Basic.md)   
 [IsNot Operator](../Topic/IsNot%20Operator%20\(Visual%20Basic\).md)   
 [How to: Determine Whether Two Objects Are Related](../Topic/How%20to:%20Determine%20Whether%20Two%20Objects%20Are%20Related%20\(Visual%20Basic\).md)   
 [How to: Determine Whether Two Objects Are Identical](../Topic/How%20to:%20Determine%20Whether%20Two%20Objects%20Are%20Identical%20\(Visual%20Basic\).md)