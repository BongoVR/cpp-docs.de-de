---
title: "Erweiterungsmethoden m&#252;ssen mindestens einen Parameter deklarieren."
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
  - "vbc36552"
  - "bc36552"
helpviewer_keywords: 
  - "BC36552"
ms.assetid: a8cc8cdd-cdb5-42ca-b5a1-c9a71abd46eb
caps.latest.revision: 15
caps.handback.revision: "15"
ms.author: "shoag"
manager: "wpickett"
---
# Erweiterungsmethoden m&#252;ssen mindestens einen Parameter deklarieren.
Erweiterungsmethoden müssen mindestens einen Parameter deklarieren. Der erste Parameter gibt den zu erweiternden Typ an.  
  
 Eine Erweiterungsmethode ohne Parameter ist ungültig, weil der erste Parameter den Datentyp angibt, der von der Methode erweitert wird. Der erste Parameter wird an die Instanz des Datentyps gebunden, der die Methode aufruft.  
  
 **Fehler\-ID:** BC36552  
  
### So beheben Sie diesen Fehler  
  
-   Fügen Sie einen Parameter des Typs hinzu, der von Ihrer Methode erweitert wird.  
  
## Beispiel  
 Der erste Parameter im folgenden Beispiel gibt an, dass die `Print`\-Methode den `String`\-Datentyp erweitert.  
  
```  
<Extension()> _ Public Sub Print (ByVal str As String) Console.WriteLine(str) End Sub  
```  
  
 Wenn die Erweiterungsmethode wie folgt aufgerufen wird, wird der Parameter `str` in der Methode an `greeting` gebunden, d. h. die Instanz von `String`, die `Print` aufruft. Der Compiler verwendet `greeting` als das Argument der Erweiterungsmethode `Print`.  
  
```  
Dim greeting As String = "Hello" greeting.Print()  
```  
  
## Siehe auch  
 [Erweiterungsmethoden](../Topic/Extension%20Methods%20\(Visual%20Basic\).md)   
 [Procedure Parameters and Arguments](../Topic/Procedure%20Parameters%20and%20Arguments%20\(Visual%20Basic\).md)   
 [Procedures](../Topic/Procedures%20in%20Visual%20Basic.md)