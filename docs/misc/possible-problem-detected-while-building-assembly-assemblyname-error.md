---
title: "Beim Erstellen der Assembly &quot;&lt;Assemblyname&gt;&quot; wurde m&#246;glicherweise ein Problem entdeckt: &lt;Fehler&gt;"
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
  - "vbc40010"
  - "bc40010"
helpviewer_keywords: 
  - "BC40010"
ms.assetid: 3a4f4a4a-a5ad-4501-bf4c-0fbf25c50734
caps.latest.revision: 11
caps.handback.revision: "11"
ms.author: "shoag"
manager: "wpickett"
---
# Beim Erstellen der Assembly &quot;&lt;Assemblyname&gt;&quot; wurde m&#246;glicherweise ein Problem entdeckt: &lt;Fehler&gt;
Das durch den [!INCLUDE[vbprvb](../dotnet/includes/vbprvb_md.md)]\-Compiler aufgerufene ALink\-Tool meldet einen Fehler beim Erstellen der Assembly. Die folgenden Ursachen sind möglich:  
  
-   Eine signierte Assembly, die auf eine unsignierte Assembly verweist. In diesem Fall sollten Sie prüfen, ob die Assembly, auf die verwiesen wird, Ihre Sicherheitskriterien erfüllt.  
  
-   Erstellen einer 64\-Bit\-Anwendung auf einer 32\-Bit\-Plattform. In diesem Fall müssen Sie sicherstellen, dass 64\-Bit\-Versionen aller Assemblys, auf die verwiesen wird, auf der Zielplattform installiert sind. Bei einer CLR\-Assembly \(Common Language Runtime\) erfolgt dies automatisch, dennoch wird diese Fehlermeldung generiert.  
  
 Diese Meldung ist eine Warnung. Der Compiler fährt mit der Generierung der Assembly fort. Weitere Informationen zum Ausblenden von Warnungen oder zum Behandeln von Warnungen als Fehler finden Sie unter [Konfigurieren von Warnungen in Visual Basic](../Topic/Configuring%20Warnings%20in%20Visual%20Basic.md).  
  
 **Fehler\-ID:** BC40010  
  
### So beheben Sie diesen Fehler  
  
1.  Überprüfen Sie die angegebene Fehlermeldung, und ergreifen Sie entsprechende Maßnahmen.  
  
2.  Kompilieren Sie das Programm erneut, um festzustellen, ob der Fehler erneut auftritt.  
  
3.  Wenn der Fehler erneut auftritt, installieren Sie den [!INCLUDE[vbprvb](../dotnet/includes/vbprvb_md.md)]\-Compiler neu.  
  
4.  Wenn der Fehler nach der Neuinstallation weiterhin besteht, tragen Sie Informationen zu den Umständen zusammen, und benachrichtigen Sie den Produktsupport von Microsoft.  
  
## Siehe auch  
 [PAVEOVER Produktsupport und Barrierefreiheit](assetId:///14e1d293-7b6d-40a6-bf3e-a92f8ee6c88c)   
 [Common Language Runtime Overview](assetId:///0fd9aeae-af10-435f-86d4-e76619741e4a)