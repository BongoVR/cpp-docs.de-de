---
title: "Verwenden Sie &quot;FileGetObject&quot; statt &quot;FileGet&quot;, wenn ein Argument des Typs &quot;Object&quot; verwendet wird"
ms.custom: na
ms.date: "11/17/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: na
ms.suite: na
ms.technology: 
  - "devlang-visual-basic"
ms.tgt_pltfrm: na
ms.topic: "article"
ms.assetid: 090b8088-895a-482a-9362-606596bac304
caps.latest.revision: 9
caps.handback.revision: "9"
ms.author: "shoag"
manager: "wpickett"
---
# Verwenden Sie &quot;FileGetObject&quot; statt &quot;FileGet&quot;, wenn ein Argument des Typs &quot;Object&quot; verwendet wird
Die `FileGet`\-Methode enthält ein Argument vom Typ `Object`.`FileGetObject` sollte anstelle von `FileGet` verwendet werden, um Mehrdeutigkeiten zu vermeiden.  
  
 Beachten Sie, dass die von `My.Computer.Filesystem` bereitgestellte Funktionalität benutzerfreundlicher und leistungsfähiger als `FileGet` oder `FileGetObject` ist.  
  
### So beheben Sie diesen Fehler  
  
1.  Ersetzen Sie `FileGet` durch `FileGetObject`.  
  
2.  Wandeln Sie das `Object`\-Argument in einen spezifischeren Typ um.  
  
## Siehe auch  
 [NICHT IM BUILD: FileGetObject\-Funktion](assetId:///3eda786b-d1ee-4b44-9dd7-0ea6bff072c0)   
 [My.Computer.FileSystem Object](../Topic/My.Computer.FileSystem%20Object.md)