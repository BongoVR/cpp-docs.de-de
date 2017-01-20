---
title: "Das Ereignis &#39;Class_Initialize&#39; wird nicht mehr unterst&#252;tzt."
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
  - "vbc42001"
  - "bc42001"
helpviewer_keywords: 
  - "BC42001"
ms.assetid: 31e7c383-894e-416c-b834-3688cc340ccf
caps.latest.revision: 11
caps.handback.revision: "11"
ms.author: "shoag"
manager: "wpickett"
---
# Das Ereignis &#39;Class_Initialize&#39; wird nicht mehr unterst&#252;tzt.
Das Ereignis 'Class\_Initialize' wird nicht mehr unterstützt. Verwenden Sie 'Sub New', um eine Klasse zu initialisieren.  
  
 Das `Class_Initialize`\-Ereignis aus früheren Versionen von [!INCLUDE[vbprvb](../dotnet/includes/vbprvb_md.md)] wurde durch Klassenkonstruktoren ersetzt.  
  
 Standardmäßig ist diese Meldung eine Warnung. Informationen zum Ausblenden von Warnungen oder zum Behandeln von Warnungen als Fehler finden Sie unter [Konfigurieren von Warnungen in Visual Basic](../Topic/Configuring%20Warnings%20in%20Visual%20Basic.md).  
  
 **Fehler\-ID:** BC42001  
  
### So beheben Sie diesen Fehler  
  
-   Deklarieren Sie mindestens eine `Sub`\-Prozedur namens `New`, um eine Klasse zu initialisieren.`Sub New` wird aufgerufen, wenn eine Klasseninstanz neu erstellt wird.  
  
## Siehe auch  
 [Class\_Initialize Changes in Visual Basic](assetId:///2cd023cf-2869-4836-b08d-43822294beeb)   
 [Classes for Visual Basic 6.0 Users](assetId:///d625222c-cd32-4c8d-b25c-ea71729b88b7)   
 [NICHT IM BUILD: Verwenden von Konstruktoren und Destruktoren](assetId:///548eebe1-86c4-4377-b2f5-447cb8be3d90)