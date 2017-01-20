---
title: "MSBuild Error MSB3185"
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
  - "MSBuild.GenerateManifest.NoEntryPoint"
helpviewer_keywords: 
  - "MSB3185"
ms.assetid: 032c63c5-d662-42ba-84e1-e3ccca8cee05
caps.latest.revision: 11
caps.handback.revision: "11"
ms.author: "mblome"
manager: "douge"
---
# MSBuild Error MSB3185
**MSB3185: Der EntryPoint wurde für das Manifest nicht angegeben.**  
  
 Dieser Fehler wird generiert, wenn in einem Manifest kein Einstiegspunkt angegeben ist.  Dieser Fehler kann sich sowohl auf das Anwendungs\- als auch auf das Bereitstellungsmanifest beziehen.  
  
### So beheben Sie diesen Fehler  
  
-   Wenn Sie die GenerateApplicationManifest\-Aufgabe verwenden, müssen Sie einen gültigen Einstiegspunkt angeben oder die TargetFrameworkVersion\-Eigenschaft auf "v3.5" oder höher festlegen.  Für ein Anwendungsmanifest ist eine EXE\-Datei ein gültiger Einstiegspunkt.  
  
-   Wenn Sie die GenerateDeploymentManifest\-Aufgabe verwenden, müssen Sie in den Manifesten gültige Einstiegspunkte angeben.  Für ein Bereitstellungsmanifest ist ein Anwendungsmanifest ein gültiger Einstiegspunkt.  
  
## Siehe auch  
 <xref:Microsoft.Build.Tasks.Deployment.ManifestUtilities.ApplicationManifest.HostInBrowser*>   
 <xref:Microsoft.Build.Tasks.GenerateApplicationManifest.TargetFrameworkVersion*>   
 [Seite "Veröffentlichen", Projekt\-Designer](../Topic/Publish%20Page,%20Project%20Designer.md)   
 [\<PackageFiles\>\-Element](../Topic/%3CPackageFiles%3E%20Element%20\(Bootstrapper\).md)   
 [MSBuild Error MSB3116](../misc/msbuild-error-msb3116.md)   
 [MSBuild Error MSB3117](../misc/msbuild-error-msb3117.md)   
 [MSBuild Error MSB3118](../misc/msbuild-error-msb3118.md)   
 [MSBuild Error MSB3174](../misc/msbuild-error-msb3174.md)