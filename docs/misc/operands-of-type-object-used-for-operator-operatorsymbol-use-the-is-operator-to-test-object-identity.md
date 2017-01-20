---
title: "F&#252;r den &quot;&lt;Operatorsymbol&gt;&quot;-Operator werden Operanden vom Typ &quot;Object&quot; verwendet. Verwenden Sie den Is-Operator, um die Objektidentit&#228;t zu testen"
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
  - "vbc42018"
  - "BC42018"
helpviewer_keywords: 
  - "BC42018"
ms.assetid: 3fc640a7-7dab-4c14-b25d-a5794dbba59d
caps.latest.revision: 12
caps.handback.revision: "12"
ms.author: "shoag"
manager: "wpickett"
---
# F&#252;r den &quot;&lt;Operatorsymbol&gt;&quot;-Operator werden Operanden vom Typ &quot;Object&quot; verwendet. Verwenden Sie den Is-Operator, um die Objektidentit&#228;t zu testen
Ein Ausdruck verwendet das `=` mit einem oder beiden Operanden des [Object Data Type](../Topic/Object%20Data%20Type.md).  
  
 Verwenden Sie den `Is`\- oder den `IsNot`\-Operator, um zu bestimmen, ob zwei Objektverweise auf die gleiche Objektinstanz verweisen. Siehe "Vergleichen von Objekten" in [Comparison Operators in Visual Basic](../Topic/Comparison%20Operators%20in%20Visual%20Basic.md).  
  
 Wenn eine Variable oder ein Ausdruck `Object` ergibt, muss der Compiler die *späte Bindung* durchführen, die zur Laufzeit zusätzliche Vorgänge verursacht. Sie setzt die Anwendung zudem möglichen Laufzeitfehlern aus. Wenn Sie z. B. ein <xref:System.Windows.Forms.Form> einer `Object`\-Variablen zuweisen und dann mit dem `=`\-Operator verwenden, löst die Laufzeit eine <xref:System.InvalidCastException> aus, da Visual Basic ein <xref:System.Windows.Forms.Form>\-Objekt nicht in einen Datentyp konvertieren kann, der für den Wertvergleich geeignet ist. Selbst wenn beide Operanden den Typ <xref:System.Windows.Forms.Form> ergeben, tritt bei dem Vorgang ein Fehler auf, weil `=` nicht für <xref:System.Windows.Forms.Form>\-Operanden definiert ist.  
  
 Standardmäßig ist diese Meldung eine Warnung. Informationen zum Ausblenden von Warnungen oder zum Behandeln von Warnungen als Fehler finden Sie unter [Konfigurieren von Warnungen in Visual Basic](../Topic/Configuring%20Warnings%20in%20Visual%20Basic.md).  
  
 **Fehler\-ID:** BC42018  
  
### So beheben Sie diesen Fehler  
  
-   Verwenden Sie den `Is`\- oder den `IsNot`\-Operator, um zu bestimmen, ob zwei Objektverweise auf die gleiche Objektinstanz verweisen.  
  
## Siehe auch  
 [Comparison Operators in Visual Basic](../Topic/Comparison%20Operators%20in%20Visual%20Basic.md)   
 [Is Operator](../Topic/Is%20Operator%20\(Visual%20Basic\).md)   
 [How to: Determine Whether Two Objects Are Related](../Topic/How%20to:%20Determine%20Whether%20Two%20Objects%20Are%20Related%20\(Visual%20Basic\).md)   
 [How to: Determine Whether Two Objects Are Identical](../Topic/How%20to:%20Determine%20Whether%20Two%20Objects%20Are%20Identical%20\(Visual%20Basic\).md)