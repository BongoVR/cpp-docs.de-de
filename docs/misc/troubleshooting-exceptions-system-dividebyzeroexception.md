---
title: "Problembehandlung bei Ausnahmen: System.DivideByZeroException"
ms.custom: na
ms.date: "11/17/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: na
ms.suite: na
ms.technology: 
  - "devlang-csharp"
ms.tgt_pltfrm: na
ms.topic: "article"
dev_langs: 
  - "JScript"
  - "VB"
  - "CSharp"
  - "C++"
helpviewer_keywords: 
  - "DivideByZeroException-Klasse"
ms.assetid: ddc79201-3ba1-455f-8496-edaad792ccf1
caps.latest.revision: 14
caps.handback.revision: "14"
ms.author: "mblome"
manager: "douge"
---
# Problembehandlung bei Ausnahmen: System.DivideByZeroException
Eine <xref:System.DivideByZeroException>\-Ausnahme wird ausgelöst, wenn versucht wird, eine ganze Zahl oder einen Dezimalwert durch 0 zu teilen.  
  
## Tipps  
 **Der Wert des Nenners darf vor dem Ausführen einer Division nicht 0 sein.**  
 Die Division eines Gleitkommawerts durch 0 ergibt entsprechend den Regeln der IEEE\-Arithmetik entweder positiv unendlich, negativ unendlich oder keine Zahl \(Not a Number, NaN\). Gleitkommaoperationen lösen niemals Ausnahmen aus.  
  
## Siehe auch  
 <xref:System.DivideByZeroException>   
 [Arithmetic Operators in Visual Basic](../Topic/Arithmetic%20Operators%20in%20Visual%20Basic.md)   
 [Use the Exception Assistant](../Topic/How%20to:%20Use%20the%20Exception%20Assistant.md)