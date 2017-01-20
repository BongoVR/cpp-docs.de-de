---
title: "&#214;ffnen einer Optionsseite"
ms.custom: na
ms.date: "11/17/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: na
ms.suite: na
ms.technology: 
  - "devlang-csharp"
ms.tgt_pltfrm: na
ms.topic: "article"
helpviewer_keywords: 
  - "Öffnen einer Optionsseite"
  - "Optionen für Extras"
  - "Seite „Optionen“"
ms.assetid: 6f24cbfa-288a-4a57-831b-bc82587de255
caps.latest.revision: 9
caps.handback.revision: "9"
manager: "douge"
---
# &#214;ffnen einer Optionsseite
Sie können eine Optionsseite programmgesteuert anzeigen, damit Benutzer Ihres Pakets dieses während des Setups konfigurieren können. Nach der Installation des Pakets kann ein Benutzer weiterhin über das Dialogfeld **Optionen** auf die Optionsseite zugreifen, um Einstellungen zu ändern.  
  
### So zeigen Sie eine benutzerdefinierte Optionsseite an  
  
1.  Erstellen einer Optionsseite Weitere Informationen finden Sie unter [Optionen \(Seiten\) erstellen](../Topic/Creating%20Options%20Pages.md).  
  
2.  Rufen Sie den <xref:System.Type> der Optionsseite ab, indem Sie das `typeof`\-Schlüsselwort auf den Namen der Klasse anwenden, die die Optionsseite definiert.  
  
3.  Rufen Sie die <xref:Microsoft.VisualStudio.Shell.Package.ShowOptionPage*>\-Methode mithilfe des <xref:System.Type>s der Optionsseite als Parameter ab.  
  
     Das folgende Beispiel zeigt eine Optionsseite namens **HelloWorldOptions**.  
  
     [!CODE [UI_UserSettings_ToolsOptionPages#5](../CodeSnippet/VS_Snippets_VSSDK/ui_usersettings_toolsoptionpages#5)]  
  
### So zeigen Sie eine von Visual Studio definierte Optionsseite an  
  
1.  Suchen Sie im Registrierungsunterschlüssel „HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\VisualStudio\\9.0\\ToolsOptionsPages\\“ den Knoten der anzuzeigenden Optionsseite, die dem Wert des Page\-Schlüssels entspricht.  
  
2.  Erstellen Sie eine <xref:System.ComponentModel.Design.CommandID>\-Instanz, die über die Konstanten <xref:Microsoft.VisualStudio.VSConstants.GUID_VSStandardCommandSet97> und <xref:Microsoft.VisualStudio.VSConstants.VSStd97CmdID> als Parameter verfügt.  
  
     Dadurch wird das Dialogfeld **Optionen** angegeben.  
  
3.  Rufen Sie die <xref:System.ComponentModel.Design.MenuCommandService.GlobalInvoke*>\-Methode mithilfe der <xref:System.ComponentModel.Design.CommandID>\-Instanz sowie mit der GUID\-Zeichenfolge als Parameter auf.  
  
     Das folgende Beispiel zeigt die Registerkarte **Allgemein** auf der Optionsseite **Text\-Editor** an.  
  
     [!CODE [UI_UserSettings_ToolsOptionPages#6](../CodeSnippet/VS_Snippets_VSSDK/ui_usersettings_toolsoptionpages#6)]