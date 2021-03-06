---
title: Anwendungseinstellungen, Win32 Projektassistent | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-windows
ms.topic: conceptual
f1_keywords:
- vc.appwiz.win32.appset
dev_langs:
- C++
helpviewer_keywords:
- application settings [C++]
- Win32 Project Wizard, application settings
ms.assetid: d6b818f0-9b23-4793-a6c5-df1c8c594bad
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- uwp
ms.openlocfilehash: 55ae50d849a67da69cde6a9c4b1529c34ee4b428
ms.sourcegitcommit: d55ac596ba8f908f5d91d228dc070dad31cb8360
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/08/2018
---
# <a name="application-settings-win-32-project-wizard"></a>Anwendungseinstellungen, Win32-Projekt-Assistent
Auf dieser Seite des Assistenten können Sie Optionen für das Win32-Projekt festlegen.  
  
 **Anwendungstyp**  
 Erstellt den angegebenen Anwendungstyp.  
  
|Option|Beschreibung|  
|------------|-----------------|  
|**Konsolenanwendung**|Erstellt eine Konsolenanwendung. Konsolenprogramme werden mit entwickelt [Konsolenfunktionen](https://msdn.microsoft.com/en-us/library/ms813137.aspx), die im Zeichenmodus-Unterstützung in Konsolenfenstern zeichenmodusunterstützung bieten. Visual C++-Komponente [Laufzeitbibliotheken](../c-runtime-library/c-run-time-library-reference.md) auch Ausgabe und Eingabe in Konsolenfenstern mit standard-e/a-Funktionen, wie z. B. **printf_s()** und **scanf_s()**. Eine Konsolenanwendung hat keine grafische Benutzeroberfläche. Sie kompiliert Code in einer EXE-Datei und kann als eigenständige Anwendung von der Befehlszeile ausgeführt werden.<br /><br /> Sie können einer Konsolenanwendung MFC- und ATL-Unterstützung hinzufügen.|  
|**Windows-Anwendung**|Erstellt ein Win32-Programm. Ein Win32-Programm ist eine ausführbare Anwendung (EXE), die in C oder C++ geschrieben ist und über Aufrufe der Win32-API eine grafische Benutzeroberfläche erstellt.<br /><br /> Sie können einer Windows-Anwendung keine MFC- oder ATL-Unterstützung hinzufügen.|  
|**DLL**|Erstellt eine Win32-Dynamic Link Library (DLL). Eine Win32-DLL ist eine in C oder C++ geschriebene Binärdatei, die anstelle von MFC-Klassenaufrufen Win32-API-Aufrufe verwendet. Sie fungiert als gemeinsam genutzte Funktionsbibliothek, die von mehreren Anwendungen gleichzeitig eingesetzt werden kann.<br /><br /> Sie können einer DLL-Anwendung keine MFC- oder ATL-Unterstützung hinzufügen. Sie können angeben, dass von der DLL Symbole exportiert werden.|  
|**Statische Bibliothek**|Erstellt eine statische Bibliothek. Eine statische Bibliothek ist eine Datei, die Objekte sowie zugehörige Funktionen und Daten enthält, die bei der Erstellung der ausführbaren Datei mit dem Programm verknüpft werden. In diesem Thema erläutert die Erstellung von Startdateien und [Projekteigenschaften](../ide/property-pages-visual-cpp.md) für eine statische Bibliothek. Eine statische Bibliothek bietet die folgenden Vorteile:<br /><br /> -Eine statische Win32-Bibliothek ist hilfreich, wenn die Anwendung, auf dem Sie arbeiten, in der Win32-API anstelle einer MFC-Klassen aufgerufen wird.<br />– Der Verknüpfungsvorgang entspricht dem, ob der Rest der Windows-Anwendung in C oder C++ geschrieben wird.<br />– Sie können eine statische Bibliothek in einer MFC-basierten Programm oder einem MFC-fremden Programm verknüpfen.|  
  
 **Zusätzliche Optionen**  
 Definiert abhängig vom Anwendungstyp die Unterstützung sowie Optionen für die Anwendung.  
  
|Option|Beschreibung|  
|------------|-----------------|  
|**Leeres Projekt**|Legt fest, dass die Projektdateien leer sind. Wenn Sie über eine Gruppe von Quellcodedateien (z. B. CPP-Dateien, Headerdateien, Symbole, Symbolleisten, Dialogfelder usw.) verfügen und in der Visual C++-Entwicklungsumgebung ein Projekt erstellen möchten, müssen Sie zunächst ein leeres Projekt anlegen und die Dateien dem Projekt dann hinzufügen.<br /><br /> Diese Option ist für statische Bibliotheksprojekte nicht verfügbar.|  
|**Symbole exportieren**|Legt fest, dass vom DLL-Projekt Symbole exportiert werden.|  
|**Vorkompilierter Header**|Legt fest, dass das statische Bibliotheksprojekt einen vorkompilierten Header verwendet.|  
|Security Development Lifecycle (SDL)-Prüfungen|Weitere Informationen zu SDL finden Sie unter [Prozessleitfäden Microsoft Security Development Lifecycle (SDL)](../build/reference/sdl-enable-additional-security-checks.md)|  
  
 **Hinzufügen von Unterstützung für**  
 Fügen Sie Unterstützung für eine der in Visual C++ enthaltenen Bibliotheken hinzu.  
  
|Option|Beschreibung|  
|------------|-----------------|  
|**ATL**|Wird in die Projektunterstützung für Klassen in ATL (Active Template Library) integriert. Nur für Win32-Konsolenanwendungen.<br /><br /> **Hinweis** diese Option gibt keine Unterstützung für das Hinzufügen von ATL-Objekten, die mit den ATL-code-Assistenten. Sie können ATL-Objekte nur zu ATL- oder MFC-Projekten mit ATL-Unterstützung hinzufügen.|  
|**MFC**|Wird in die Projektunterstützung für die MFC (Microsoft Foundation Class)-Bibliothek integriert. Nur für Win32-Konsolenanwendungen und statische Bibliotheken.|  
  
## <a name="see-also"></a>Siehe auch  
 [Win32-Anwendungs-Assistent](../windows/win32-application-wizard.md)   
