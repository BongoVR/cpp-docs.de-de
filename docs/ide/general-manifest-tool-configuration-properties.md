---
title: Manifest Tool-Konfigurationseigenschaften (Visual C++) | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-ide
ms.topic: conceptual
f1_keywords:
- VC.Project.VCManifestTool.MergeRulesFile
- VC.Project.VCManifestTool.UseUnicodeResponseFiles
- VC.Project.VCManifestTool.SuppressStartupBanner
- VC.Project.VCManifestTool.UseFAT32Workaround
- VC.Project.VCManifestTool.VerboseOutput
- VC.Project.VCManifestTool.AssemblyIdentity
dev_langs:
- C++
ms.assetid: b99368a5-6819-482c-a06e-f2409290cfd1
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: 1953e7c37c07f66845510efe037015a537aa7baa
ms.sourcegitcommit: 76b7653ae443a2b8eb1186b789f8503609d6453e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/04/2018
---
# <a name="general-manifest-tool-configuration-properties-ltprojectnamegt-property-pages-dialog-box"></a>Tool Allgemein, Manifesttool, Konfigurationseigenschaften, &lt;Projektname&gt; Eigenschaftenseiten (Dialogfeld)
Verwenden Sie das Dialogfeld zu öffnen, geben Sie allgemeine Optionen für [Mt.exe](http://msdn.microsoft.com/library/aa375649).  
  
 Öffnen Sie diese Eigenschaftenseiten-Dialogfeld für den Zugriff auf die Eigenschaftenseiten für das Projekt oder das Eigenschaftenblatt. Erweitern Sie die **Manifesttool** Knoten unter **Konfigurationseigenschaften**, und wählen Sie dann **allgemeine**.  
  
## <a name="uielement-list"></a>UIElement-Liste  
 **Startbanner unterdrücken**  
 **Ja (/ Nologo)** gibt an, dass standardmäßige Copyrightinformationen von Microsoft beim Starten der Manifesttools ausgeblendet werden. Verwenden Sie diese Option, um unerwünschte Ausgaben in Protokolldateien zu unterdrücken, wenn Sie mt.exe als Teil des Buildprozesses oder aus einem Buildumgebung ausführen.  
  
 **Eine ausführliche Ausgabe**  
 **Ja (/ verbose)** gibt an, dass zusätzliche Informationen während der Generierung von Manifesten angezeigt wird.  
  
 **Assemblyidentität**  
 Die Option/Identity verwendet, um eine Identitätszeichenfolge anzugeben die umfasst die Attribute für die [ \<AssemblyIdentity >-Element](/visualstudio/deployment/assemblyidentity-element-clickonce-application). Eine Identitätszeichenfolge beginnt mit dem Wert für die `name` Attribut, und folgen *Attribut* = *Wert* Paare. Die Attribute in einer Identitätszeichenfolge werden durch ein Komma getrennt.  
  
 Im folgenden finden eine Beispiel-Identity-Zeichenfolge:  
  
 `Microsoft.Windows.Common-Controls, processorArchitecture=x86, version=6.0.0.0, type=win32, publicKeyToken=6595b64144ccf1df`  
  
## <a name="see-also"></a>Siehe auch  
 [ClickOnce-Anwendungsmanifest](/visualstudio/deployment/clickonce-application-manifest)   
 [Manifesttool-Eigenschaftenseiten](../ide/manifest-tool-property-pages.md)   
 [Arbeiten mit Projekteigenschaften](../ide/working-with-project-properties.md)   