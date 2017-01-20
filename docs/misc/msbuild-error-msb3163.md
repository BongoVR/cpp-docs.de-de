---
title: "MSBuild Error MSB3163"
ms.custom: na
ms.date: "11/17/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: na
ms.suite: na
ms.technology: 
  - "devlang-csharp"
ms.tgt_pltfrm: na
ms.topic: "article"
f1_keywords: 
  - "MSBuild.GenerateBootstrapper.InvalidComponentsLocation"
helpviewer_keywords: 
  - "MSB3163"
ms.assetid: 35c5efbf-2fd7-478c-bb8e-3c4eabb3e4d4
caps.latest.revision: 6
caps.handback.revision: "6"
ms.author: "mblome"
manager: "douge"
---
# MSBuild Error MSB3163
**MSB3163: Der Buildeingabeparameter ComponentsLocation\=\<Komponentenspeicherort\> ist ungültig.  Der Wert muss entweder "HomeSite", "Relative" oder "Absolute" sein.  "HomeSite" wird als Standardwert verwendet.**  
  
 Dieser Fehler tritt auf, wenn der für die `ComponentsLocation` \-Eigenschaft \(der Speicherort, von dem die erforderlichen Komponenten installiert werden\) angegebene Wert ungültig ist.  `ComponentsLocation` muss einen der drei folgenden Werte aufweisen: `HomeSite`, `Relative` oder `Absolute`.  
  
## Siehe auch  
 [\<PackageFiles\>\-Element](../Topic/%3CPackageFiles%3E%20Element%20\(Bootstrapper\).md)