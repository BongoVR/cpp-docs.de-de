---
title: Win32-Anwendung-Assistenten | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-windows
ms.topic: conceptual
f1_keywords:
- vc.appwiz.win32.overview
dev_langs:
- C++
helpviewer_keywords:
- Win32 Application Wizard
- Win32 Project Wizard
ms.assetid: 5d7b3a5e-8461-479a-969a-67b7883725b9
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- uwp
ms.openlocfilehash: 18885e36b5f598a8b1dd6128c29a9e520128dcb2
ms.sourcegitcommit: d55ac596ba8f908f5d91d228dc070dad31cb8360
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/08/2018
---
# <a name="win32-application-wizard"></a>Win32-Anwendungs-Assistent
Mit dem Win32-Anwendungs-Assistenten von Visual C++ können Sie einen von vier Projekttypen erstellen (siehe die Überschriften in der folgenden Tabelle). Sie können zusätzliche Optionen festlegen, die für den jeweils geöffneten Projekttyp geeignet sind. Der folgenden Tabelle können Sie entnehmen, welche Optionen für die einzelnen Anwendungstypen verfügbar sind.  
  
|Art der Unterstützung|Konsolenanwendung|Ausführbare (Windows-)Anwendung|Dynamic Link Library|Statische Bibliothek|  
|---------------------|-------------------------|----------------------------------------|---------------------------|--------------------|  
|**Leeres Projekt**|Ja|Ja|Ja|Nein|  
|**Symbole exportieren**|Nein|Nein|Ja|Nein|  
|**Vorkompilierter Header**|Nein|Nein|Nein|Ja|  
|**ATL-Unterstützung**|Ja|Nein|Nein|Nein|  
|**MFC-Unterstützung**|Ja|Nein|Nein|Ja|  
  
## <a name="overview"></a>Übersicht  
 Auf der Seite für diesen Assistenten werden die aktuellen Projekteinstellungen für die von Ihnen erstellte Win32-Anwendung beschrieben. Die folgenden Optionen sind standardmäßig aktiviert:  
  
-   Das Projekt ist eine Windows-Anwendung.  
  
-   Das Projekt ist nicht leer.  
  
-   Das Projekt enthält keine Exportsymbole.  
  
-   Das Projekt verwendet keine vorkompilierte Headerdatei (diese Option ist nur für statische Bibliotheksprojekte verfügbar).  
  
-   Das Projekt unterstützt weder MFC noch ATL.  
  
 Zum Ändern dieser Standardeinstellungen klicken Sie in der linken Spalte des Assistenten auf die Registerkarte [Anwendungseinstellungen](../windows/application-settings-win-32-project-wizard.md) , und nehmen Sie die gewünschten Änderungen vor.  
  
 Nach Erstellung einer Windows-Desktopanwendung können Sie mit dem Assistenten für [generischen](../ide/generic-cpp-class-wizard.md) Code generische C++-Klassen hinzufügen. Sie können weitere Elemente, wie HTML-Dateien, Headerdateien, Ressourcen oder Textdateien, hinzufügen.  
  
> [!NOTE]
>  Es können keine ATL-Klassen hinzugefügt werden. MFC-Klassen können nur solchen Windows-Desktopanwendungstypen hinzugefügt werden, die MFC unterstützen (siehe vorangehende Tabelle).  
  
 Die vom Assistenten erstellten Projektdateien können im **Projektmappen-Explorer**angezeigt werden. Weitere Informationen zu den vom Assistenten erstellten Dateien im Projekt finden Sie in der projekteigenen Datei "Readme.txt". Weitere Informationen zu den Dateitypen finden Sie unter [Für Visual C++-Projekte erstellte Dateitypen](../ide/file-types-created-for-visual-cpp-projects.md).  
  
## <a name="see-also"></a>Siehe auch  
 [Erstellen einer leeren Windows-Desktopanwendung](../windows/creating-an-empty-windows-desktop-application.md)   
 [Visual C++-Projekttypen](../ide/visual-cpp-project-types.md)