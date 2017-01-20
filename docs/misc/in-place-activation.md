---
title: "Direkte Aktivierung"
ms.custom: na
ms.date: "11/16/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: na
ms.suite: na
ms.technology: 
  - "devlang-csharp"
ms.tgt_pltfrm: na
ms.topic: "article"
helpviewer_keywords: 
  - "Editoren [Visual Studio-SDK], Benutzerdefiniert:direkte Aktivierung von Ansichten"
ms.assetid: 7d316945-06e0-4d8e-ba3a-0ef96fc75399
caps.latest.revision: 26
caps.handback.revision: "26"
manager: "douge"
---
# Direkte Aktivierung
Wenn die Editor\-Ansicht ActiveX\- oder andere aktive Steuerelemente hostet, müssen Sie die Editor\-Ansicht entweder als ActiveX\-Steuerelement oder als aktives Dokumentdatenobjekt mithilfe des Modells für die direkte Aktivierung implementieren.  
  
## Unterstützung von Menüs, Symbolleisten und Befehlen  
 In Visual Studio kann die Editor\-Ansicht Menüs und Symbolleisten der IDE verwenden. Diese Erweiterungen werden als *OLE in\-place Components* bezeichnet. Weitere Informationen finden Sie unter <xref:Microsoft.VisualStudio.Shell.Interop.IOleInPlaceComponent> und <xref:Microsoft.VisualStudio.Shell.Interop.IOleInPlaceComponentUIManager>.  
  
 Wenn Sie ein ActiveX\-Steuerelement implementieren, können Sie andere eingebettete Objekte hosten. Wenn Sie ein Dokumentdatenobjekt implementieren, wird die Möglichkeit zur Verwendung von ActiveX\-Steuerelementen durch den Fensterrahmen begrenzt.  
  
> [!NOTE]
>  Die Schnittstellen <xref:Microsoft.VisualStudio.OLE.Interop.IOleDocument> und <xref:Microsoft.VisualStudio.OLE.Interop.IOleDocumentView> erlauben eine Trennung von Daten und Ansicht. Allerdings wird diese Funktionalität von Visual Studio nicht unterstützt, und diese Schnittstellen werden nur zur Darstellung des Dokumentansichtsobjekts verwendet.  
  
 Editoren, die den <xref:Microsoft.VisualStudio.Shell.Interop.SOleComponentUIManager>\-Dienst verwenden, können über den Aufruf der Methoden der durch den <xref:Microsoft.VisualStudio.Shell.Interop.SOleComponentUIManager>\-Dienst implementierten <xref:Microsoft.VisualStudio.Shell.Interop.IOleInPlaceComponentUIManager>\-Schnittstelle für die Integration von Menüs, Symbolleisten und Befehlen sorgen. Editoren können auch noch andere Visual Studio\-Funktionen wie die Auswahlnachverfolgung und die Rückgängig\-Funktion mit der entsprechenden Schrittverwaltung bereitstellen. Weitere Informationen finden Sie unter [Erstellen von benutzerdefinierten Editoren und Designern](../Topic/Creating%20Custom%20Editors%20and%20Designers.md).  
  
## Verwendete Objekte und Schnittstellen  
 Die für zum Erstellen der direkten Aktivierung verwendeten Objekte sind in der folgenden Abbildung dargestellt.  
  
 ![Editor mit direkter Aktivierung](../misc/media/vsinplaceactivationeditor.png "vsInPlaceActivationEditor")  
Editor für die direkte Aktivierung  
  
> [!NOTE]
>  Von den Objekten in dieser Zeichnung ist nur das `CYourEditorFactory`\-Objekt zum Erstellen eines Standard\-Editors erforderlich. Wenn Sie einen benutzerdefinierten Editor erstellen, müssen Sie <xref:Microsoft.VisualStudio.Shell.Interop.IVsPersistDocData2> nicht implementieren, da Ihr Editor wahrscheinlich über einen eigenen Mechanismus für die dauerhafte Speicherung verfügt. Weitere Informationen finden Sie unter [Erstellen von benutzerdefinierten Editoren und Designern](../Topic/Creating%20Custom%20Editors%20and%20Designers.md).  
  
 Alle Schnittstellen, die zum Erstellen eines Editors für die direkte Aktivierung implementiert werden, werden an einem einzelnen `CYourEditorDocument`\-Objekt angezeigt. Diese Konfiguration unterstützt jedoch nur eine einzige Ansicht der Dokumentdaten. Weitere Informationen zur Unterstützung von mehreren Ansichten der Dokumentdaten finden Sie unter [Unterstützung mehrerer Dokumentansichten](../Topic/Supporting%20Multiple%20Document%20Views.md).  
  
|Schnittstelle|Objekttyp|Verwendung|  
|-------------------|---------------|----------------|  
|<xref:Microsoft.VisualStudio.Shell.Interop.IOleInPlaceComponent>|Ansicht|Direkte VSPackage\-Objekte können mithilfe des <xref:Microsoft.VisualStudio.Shell.Interop.SOleComponentUIManager>\-Diensts als vollständig integrierte Komponenten der IDE ausgeführt werden. Dieser Dienst integriert Menüs, Symbolleisten und Befehle des Objekts in die IDE und gibt Benachrichtigung bei Zustandsänderungen aus.|  
|<xref:Microsoft.VisualStudio.OLE.Interop.IOleObject>|Ansicht|Basismethode, mit der ein eingebettetes Objekt die Basisfunktionalität für den Container bereitstellt und mit ihm kommuniziert.|  
|<xref:Microsoft.VisualStudio.OLE.Interop.IOleInPlaceActiveObject>|Ansicht|Verwaltet die Aktivierung und Deaktivierung von direkten Objekten und bestimmt, wie viel des direkten Objekts angezeigt werden soll.|  
|<xref:Microsoft.VisualStudio.OLE.Interop.IOleInPlaceObject>|Ansicht|Stellt einen direkten Kanal für die Kommunikation zwischen einem direkten Objekt, dem äußersten Rahmenfenster der zugehörigen Anwendung und dem Dokumentfenster in der Anwendung bereit, die das eingebettete Objekt enthält.|  
|<xref:Microsoft.VisualStudio.OLE.Interop.IOleDocument>|Ansicht|Implementiert ein ActiveX\-Objekt. Die Methoden <xref:Microsoft.VisualStudio.OLE.Interop.IOleDocument> und `T:Microsoft.VisualStudio.OLE.Interop.IOleDocumentView`, die für die Trennung der Dokumentdaten und deren Ansicht sorgen, werden in der IDE nicht verwendet.|  
|<xref:Microsoft.VisualStudio.OLE.Interop.IOleCommandTarget>|Ansicht\/Daten|Bietet die Möglichkeit, das Dokumentdatenobjekt oder das Dokumentansichtsobjekt an der Behandlung von Befehlen zu beteiligen.|  
|<xref:Microsoft.VisualStudio.Shell.Interop.IVsStatusbarUser>|Ansicht|Ermöglicht Aktualisierungen der Statusleiste.|  
|<xref:Microsoft.VisualStudio.Shell.Interop.IVsToolboxUser>|Ansicht|Ermöglicht das Hinzufügen von Elementen zur Toolbox.|  
|<xref:Microsoft.VisualStudio.Shell.Interop.IVsFileChangeEvents>|Daten|Sendet Benachrichtigung über Änderungen an die bearbeitete Datei. \(Diese Schnittstelle ist optional.\)|  
|<xref:Microsoft.VisualStudio.Shell.Interop.IPersistFileFormat>|Daten|Wird zum Aktivieren der Funktion "Speichern unter" für einen Dateityp verwendet.|  
|<xref:Microsoft.VisualStudio.Shell.Interop.IVsPersistDocData>|Daten|Aktiviert die Persistenz für das Dokument. Rufen Sie bei schreibgeschützten Dateien <xref:Microsoft.VisualStudio.Shell.Interop.IVsPersistDocData2.SetDocDataReadOnly*> auf, um das Sperrsymbol bereitzustellen, das die Dateien als schreibgeschützt kennzeichnet.|  
|<xref:Microsoft.VisualStudio.Shell.Interop.IVsDocDataFileChangeControl>|Daten|Bestimmt, ob Änderungen an Dokumentdaten ignoriert werden sollen.|