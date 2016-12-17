---
title: "Der Wert „System.Runtime.InteropServices.DispIdAttribute“ kann nicht auf &lt;Typname&gt; angewendet werden, da „Microsoft.VisualBasic.ComClassAttribute“ 0 (null) f&#252;r die Standardeigenschaft reserviert."
ms.custom: na
ms.date: "10/29/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: na
ms.suite: na
ms.technology: 
  - "devlang-visual-basic"
ms.tgt_pltfrm: na
ms.topic: "article"
f1_keywords: 
  - "vbc32505"
  - "bc32505"
helpviewer_keywords: 
  - "BC32505"
ms.assetid: a7d5b948-2d72-48b1-8baf-bfaae36b0128
caps.latest.revision: 8
caps.handback.revision: "8"
ms.author: "shoag"
manager: "wpickett"
---
# Der Wert „System.Runtime.InteropServices.DispIdAttribute“ kann nicht auf &lt;Typname&gt; angewendet werden, da „Microsoft.VisualBasic.ComClassAttribute“ 0 (null) f&#252;r die Standardeigenschaft reserviert.
Ein <xref:System.Runtime.InteropServices.DispIdAttribute>\-Attributblock gibt einen DISPID\-Wert von o \(null\) an. Dieser ist von `COMClassAttribute` für die Standardeigenschaft der Klasse reserviert, auf die der Wert angewendet wird.  
  
 Die Dispatch\-ID \(DISPID\) wird in COM als Argument für die `IDispatch:Invoke`\-Methode verwendet, um auf die Eigenschaften und Methoden zuzugreifen, die von einem COM\-Objekt verfügbar gemacht werden.  
  
 **Fehler\-ID:** BC32505  
  
### So beheben Sie diesen Fehler  
  
-   Geben Sie in <xref:System.Runtime.InteropServices.DispIdAttribute> einen DISPID\-Wert größer als 0 \(null\) an.  
  
## Siehe auch  
 <xref:System.Runtime.InteropServices.DispIdAttribute>   
 [NICHT IM BUILD: In Visual Basic verwendete Attribute](assetId:///22231318-8a40-49af-9245-e0aab723563b)   
 [NICHT IM BUILD: Anwendung von Attributen](assetId:///2b1703ed-4437-49b3-bc0b-568094324f47)   
 [ComClassAttribute\-Klasse](assetId:///5c2f0835-9210-47dc-bc59-5c1769953574)