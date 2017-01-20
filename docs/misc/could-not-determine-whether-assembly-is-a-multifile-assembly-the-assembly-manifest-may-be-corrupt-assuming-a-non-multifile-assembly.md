---
title: "Es konnte nicht festgestellt werden, ob „Assembly“ eine Mehrfachdateiassembly ist. Das Assemblymanifest ist m&#246;glicherweise besch&#228;digt. Es wird von einer Nicht- Mehrfachdateiassembly ausgegangen."
ms.custom: na
ms.date: "12/15/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: na
ms.suite: na
ms.technology: 
  - "devlang-csharp"
ms.tgt_pltfrm: na
ms.topic: "article"
f1_keywords: 
  - "vs.tasklisterror.unknownscatterstatusforcopy"
ms.assetid: be49d3f2-b091-488c-8579-e27ef09d9c80
caps.latest.revision: 8
caps.handback.revision: "8"
ms.author: "mblome"
manager: "douge"
---
# Es konnte nicht festgestellt werden, ob „Assembly“ eine Mehrfachdateiassembly ist. Das Assemblymanifest ist m&#246;glicherweise besch&#228;digt. Es wird von einer Nicht- Mehrfachdateiassembly ausgegangen.
Das Projektsystem konnte eine Assembly nicht lesen, auf die im Projekt verwiesen wird. Somit kann das Projektsystem nicht feststellen, ob Sie auf eine Mehrfachdateiassembly verweisen. Daher wird die Assembly möglicherweise nicht ordnungsgemäß in das Ausgabeverzeichnis kopiert.  
  
 **So beheben Sie diesen Fehler**  
  
-   Installieren Sie [!INCLUDE[vsprvs](../assembler/masm/includes/vsprvs_md.md)] neu \(wenn die Assembly im Lieferumfang von [!INCLUDE[vsprvs](../assembler/masm/includes/vsprvs_md.md)] oder von .NET Framework enthalten war\).  
  
     \- oder \-  
  
-   Installieren Sie das entsprechende Drittanbieter\-Steuerelement neu.  
  
     Ein Vorliegen dieses Fehlers verhindert nicht, dass das Projekt erstellt wird. Allerdings kann ein Laufzeitfehler auftreten.  
  
## Siehe auch  
 [Problembehandlung bei fehlerhaften Verweisen](../Topic/Troubleshooting%20Broken%20References.md)   
 [NIB: Gewusst wie: Hinzufügen oder Entfernen von Verweisen mithilfe des Dialogfelds „Verweis hinzufügen“](assetId:///3bd75d61-f00c-47c0-86a2-dd1f20e231c9)   
 [Assemblies in the Common Language Runtime](assetId:///33a0bc6a-6bb3-44c7-ada7-4a046e8c0945)