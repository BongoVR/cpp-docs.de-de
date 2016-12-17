---
title: "Die statische Variable &quot;&lt;Variablenname&gt;&quot; wurde ohne As-Klausel deklariert. Typ &quot;Object&quot; wird angenommen"
ms.custom: na
ms.date: "11/24/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: na
ms.suite: na
ms.technology: 
  - "devlang-visual-basic"
ms.tgt_pltfrm: na
ms.topic: "article"
f1_keywords: 
  - "vbc42111"
  - "bc42111"
helpviewer_keywords: 
  - "BC42111"
ms.assetid: ca6b625c-21a5-45f7-ac67-282f6993a724
caps.latest.revision: 15
caps.handback.revision: "15"
ms.author: "shoag"
manager: "wpickett"
---
# Die statische Variable &quot;&lt;Variablenname&gt;&quot; wurde ohne As-Klausel deklariert. Typ &quot;Object&quot; wird angenommen
Der Compiler leitet den Datentyp von statischen lokalen Variablen nicht ab. Im folgenden Beispiel ist `Option Strict` auf `Off` festgelegt und der Typ von `m` ist `Object`, unabhängig davon, ob `Option Infer` auf `On` oder `Off` festgelegt ist. Der lokale Typrückschluss findet hier keine Anwendung.  
  
```  
Sub Main() Static m = 10 End Sub  
```  
  
 Standardmäßig ist diese Meldung eine Warnung. Weitere Informationen zum Ausblenden von Warnungen und zum Behandeln von Warnungen als Fehler finden Sie unter [Konfigurieren von Warnungen in Visual Basic](../Topic/Configuring%20Warnings%20in%20Visual%20Basic.md).  
  
 **Fehler\-ID:** BC42111  
  
### So reagieren Sie auf diese Warnung  
  
-   Geben Sie den Datentyp für statische lokale Variablen an.  
  
     Wenn `m` im vorherigen Beispiel vom Typ `Integer` sein soll, geben Sie den Typ in der Deklaration an.  
  
    ```  
    Sub Main() Static m As Integer = 10 End Sub  
  
    ```  
  
## Siehe auch  
 [Dim Statement](../Topic/Dim%20Statement%20\(Visual%20Basic\).md)   
 [NOTINBUILD: Gewusst wie: Erhöhen der Lebensdauer einer Variablen](assetId:///04e7c56c-1db0-4fe5-a678-859a39ec654b)   
 [Local Type Inference](../Topic/Local%20Type%20Inference%20\(Visual%20Basic\).md)   
 [Option Infer Statement](../Topic/Option%20Infer%20Statement.md)   
 [Static](../Topic/Static%20\(Visual%20Basic\).md)