---
title: 'Datenquelle: Programmgesteuertes Konfigurieren einer ODBC-Datenquelle | Microsoft Docs'
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-data
ms.topic: conceptual
f1_keywords:
- SQLConfigDataSource
dev_langs:
- C++
helpviewer_keywords:
- ODBC data sources, configuring
- SQLConfigDataSource method example
- ODBC connections, configuring
- configuring ODBC data sources
ms.assetid: b8cabe9b-9e12-4d73-ae36-7cb12dee3213
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- data-storage
ms.openlocfilehash: e1f46ad566874d80b45593e7aecfeee2d5d88841
ms.sourcegitcommit: 76b7653ae443a2b8eb1186b789f8503609d6453e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/04/2018
---
# <a name="data-source-programmatically-configuring-an-odbc-data-source"></a>Datenquelle: Programmgesteuertes Konfigurieren einer ODBC-Datenquelle
In diesem Thema wird erläutert, wie ODBC-Datenquellennamen programmgesteuert konfiguriert werden können. Dies ermöglicht es, auf Daten zuzugreifen, ohne den Benutzer dazu zu zwingen, die Namen der Datenquellen explizit mit ODBC-Administrator oder einem anderen Programm anzugeben.  
  
 Normalerweise führt ein Benutzer den ODBC-Administrator aus, um eine Datenquelle zu erstellen, wenn das betreffende Datenbankmanagementsystem (DBMS) diese Operation unterstützt.  
  
 Beim Anlegen einer Microsoft Access-ODBC-Datenquelle mit ODBC-Administrator haben Sie zwei Möglichkeiten: Sie können entweder eine vorhandene MDB-Datei auswählen oder eine neue MDB-Datei erstellen. Es gibt keine Möglichkeit, eine MDB-Datei von einer MFC-ODBC-Anwendung aus programmgesteuert anzulegen. Wenn es daher für die Anwendung erforderlich ist, Daten in einer Microsoft Access-Datenquelle (.mdb-Datei) zu speichern, benötigen Sie wahrscheinlich eine leere MDB-Datei, auf die Sie bei Bedarf zugreifen oder die Sie kopieren können.  
  
 Viele Datenbankmanagementsysteme ermöglichen jedoch das programmgesteuerte Erstellen einer Datenquelle. Einige Datenquellen verwenden eine Verzeichnisangabe für Datenbanken. Als Datenquelle wird also ein Verzeichnis verwendet. Jede Tabelle dieser Datenquelle ist in einer eigenen Datei gespeichert. Im Fall von dBASE ist jede Tabelle in einer eigenen DBF-Datei enthalten. Treiber für andere ODBC-Datenbanken, z. B. Microsoft Access und SQL Server, setzen voraus, dass bestimmte Kriterien erfüllt werden, bevor eine Datenquelle eingerichtet werden kann. Beispielsweise fallen bei Verwendung den SQL Server-ODBC-Treiber einen SQL Server-Computer eingerichtet haben.  
  
##  <a name="_core_sqlconfigdatasource_example"></a> SQLConfigDataSource-Beispiel  
 Im folgenden Beispiel wird die **:: SQLConfigDataSource** ODBC-API-Funktion zum Erstellen einer neuen Excel-Datenquelle aufgerufen, neue Excel-Datenquelle:  
  
```  
SQLConfigDataSource(NULL,ODBC_ADD_DSN, "Excel Files (*.xls)",   
                   "DSN=New Excel Data Source\0"   
                   "Description=New Excel Data Source\0"   
                   "FileType=Excel\0"   
                   "DataDirectory=C:\\EXCELDIR\0"   
                   "MaxScanRows=20\0");  
```  
  
 Beachten Sie, dass es sich bei der Datenquelle um ein Verzeichnis handelt (C:\EXCELDIR), dessen Vorhandensein sichergestellt sein muss. Der Excel-Treiber verwendet Verzeichnisse als Datenquellen und Dateien als einzelne Tabellen, und zwar eine Tabelle pro XLS-Datei.  
  
 Weitere Informationen zum Erstellen von Tabellen finden Sie unter [Datenquelle: Programmgesteuertes Erstellen einer Tabelle in einer ODBC-Datenquelle](../../data/odbc/data-source-programmatically-creating-a-table-in-an-odbc-data-source.md).  
  
 Die folgende Informationen erläutert, die Parameter, die übergeben werden müssen die **:: SQLConfigDataSource** ODBC API-Funktion. Mit **:: SQLConfigDataSource**, müssen Sie die Headerdatei Odbcinst.h eingebunden und die Importbibliothek Odbcinst.lib verwendet werden. Außerdem muss die Datei Odbccp32.dll zur Laufzeit im Ausführungspfad gespeichert sein, bzw. für 16 Bits die Datei Odbcinst.dll.  
  
 Sie können einen ODBC-Datenquellennamen mit ODBC-Administrator oder einem ähnlichen Dienstprogramm erstellen. Manchmal ist es jedoch besser, einen Datenquellennamen direkt aus einer Anwendung heraus anzulegen. So wird der Zugriff ermöglicht, ohne dass der Benutzer ein separates Hilfsprogramm ausführen muss.  
  
 ODBC-Administrator, der normalerweise in der Windows-Systemsteuerung installiert ist, erstellt eine neue Datenquelle, indem er Einträge in die Windows-Registrierung schreibt, bzw. bei 16 Bits in die Datei Odbc.ini. Der ODBC-Treiber-Manager verwendet diese Datei, um die benötigten Informationen über die Datenquelle zu ermitteln. Es ist wichtig zu wissen, welche Informationen in der Registrierung platziert werden, da er mit dem Aufruf bereitstellen, müssen muss **:: SQLConfigDataSource**.  
  
 Obwohl diese Informationen direkt in der Registrierung ohne geschrieben werden konnte **:: SQLConfigDataSource**, jede Anwendung, die Zweck ist der vertrauenden Seite, auf das aktuelle Verfahren, die der Treiber-Manager verwendet, um ihre Daten zu verwalten. Sollte eine spätere Version von ODBC-Treiber-Manager die Datensatzverwaltung für Datenquellen in einer anderen Weise implementieren, wäre eine solche Anwendung nicht mehr funktionsfähig. Soweit möglich, sollte immer eine API-Funktion verwendet werden. Der Code ist z. B. Übertragung von 16-Bit in 32-Bit, bei Verwendung der **:: SQLConfigDataSource** funktionieren, da die Funktion ordnungsgemäß in die Datei Odbc.ini oder in die Registrierung geschrieben.  
  
##  <a name="_core_sqlconfigdatasource_parameters"></a> Parameter von SQLConfigDataSource  
 Das folgende Beispiel erläutert die Parameter von der **:: SQLConfigDataSource** Funktion. Der Großteil dieser Informationen stammt aus der ODBC-API *Programmer's Reference* Lieferumfang von Visual C++, Version 1.5 und höher.  
  
###  <a name="_core_function_prototype"></a> Funktionsprototyp  
  
```  
BOOL SQLConfigDataSource(HWND hwndParent,UINT fRequest, LPCSTR lpszDriver, LPCSTR lpszAttributes);  
```  
  
### <a name="remarks"></a>Hinweise  
  
####  <a name="_core_parameters_and_usage"></a> Parameter und Ihre Verwendung  
 *hwndParent*  
 Das Besitzerfenster für alle Dialogfelder, das der ODBC-Treiber-Manager oder der spezifische ODBC-Treiber erstellt, um vom Benutzer zusätzliche Informationen über die neue Datenquelle anzufordern. Falls durch den `lpszAttributes`-Parameter nicht genügend Informationen bereitstellt werden, wird ein Dialogfeld angezeigt. Die *HwndParent* Parameter möglicherweise **NULL**.  
  
 `lpszDriver`  
 Hierbei handelt es sich um die Treiberbeschreibung. Dies ist der Name, der dem Benutzer an Stelle des physischen Treibernamens, also der DLL, angezeigt wird.  
  
 `lpszAttributes`  
 Die Liste der Attribute in der Form "Schlüsselname=Wert". Diese Zeichenfolgen werden durch NULL-Zeichen getrennt. Zwei aufeinander folgende NULL-Zeichen kennzeichnen das Ende der Liste. Diese Attribute sind in erster Linie treiberspezifische Standardeinträge, die für die neue Datenquelle in die Registrierung geschrieben werden. Ein wichtiger Schlüssel, der in der ODBC-API-Referenz zu dieser Funktion nicht erwähnt wird, ist "DSN" (Data Source Name, Datenquellenname). Hierdurch wird der Name der neuen Datenquelle angegeben. Die übrigen Einträge betreffen den Treiber für die neue Datenquelle. Meist ist es nicht erforderlich, alle Einträge zur Verfügung zu stellen, da der Benutzer durch den Treiber in Dialogfeldern zur Eingabe der neuen Werte aufgefordert werden kann. (Legen Sie *HwndParent* auf **NULL** dies verursachen.) Es können auch explizit Standardwerte bereitgestellt werden, damit der Benutzer nicht zu einer Eingabe aufgefordert wird.  
  
###### <a name="to-determine-the-description-of-a-driver-for-the-lpszdriver-parameter-using-odbc-administrator"></a>So ermitteln Sie mit ODBC-Administrator die Beschreibung eines Treibers für den lpszDriver-Parameter  
  
1.  Starten Sie den ODBC-Administrator.  
  
2.  Klicken Sie auf **Hinzufügen**.  
  
 Hierdurch wird eine Liste der installierten Treiber mit der entsprechenden Beschreibung angezeigt. Verwenden Sie diese Beschreibung für den `lpszDriver`-Parameter. Verwenden Sie hierbei die vollständige Beschreibung, z. B. "Excel-Dateien (*.xls)", einschließlich der Dateinamenerweiterung und der Klammern, sofern diese in der Beschreibung vorhanden sind.  
  
 Wahlweise kann auch die Registrierung oder, bei 16 Bit-Systemen, die Datei Odbcinst.ini durchsucht werden, die eine Liste aller Treibereinträge und Beschreibungen unter dem Registrierungsschlüssel "ODBC Drivers" enthält bzw. der Abschnitt [ODBC Drivers] in der Datei Odbcinst.ini.  
  
 Eine Möglichkeit, die Schlüsselnamen und Werte für den `lpszAttributes`-Parameter zu ermitteln, ist die Untersuchung der Datei ODBC.ini einer bereits konfigurierten Datenquelle, die möglichst mit ODBC-Administrator konfiguriert wurde.  
  
###### <a name="to-find-keynames-and-values-for-the-lpszattributes-parameter"></a>So suchen Sie Schlüsselnamen und Werte für den Parameter lpszAttributes  
  
1.  Führen Sie den Registrierungs-Editor von Windows aus, oder öffnen Sie bei einem 16-Bit-System die Datei Odbc.ini.  
  
2.  Suchen Sie nach den Informationen zu ODBC-Datenquellen mit einer der folgenden Methoden:  
  
    -   Suchen Sie für 32-Bit-Schlüssel **HKEY_CURRENT_USER\Software\ODBC\ODBC. Datenquellen INI\ODBC** im linken Bereich.  
  
         Im rechten Bereich aufgeführt Einträge der Form: "Pub: REG_SZ:*<data source name>*", wobei *<data source name>* ist eine Datenquelle, die mit den erwünschten Einstellungen für den Treiber wurde bereits konfiguriert werden soll um zu verwenden. Wählen Sie die Datenquelle, die Sie möchten, die z. b. SQL Server. Die Elemente nach der Zeichenfolge "pub:" enthalten in der erforderlichen Reihenfolge den zu verwendenden Schlüsselnamen und den Wert für den `lpszAttributes`-Parameter.  
  
    -   Für 16-Bit, suchen Sie den Abschnitt in der Datei Odbc.ini nach [*\<Datenquellenname >*].  
  
         Die Zeilen im Anschluss an diese Zeile haben die Form "Schlüsselname=Wert". Exakt diese Einträge müssen im `lpszAttributes`-Parameter verwendet werden.  
  
 Sie können auch die Dokumentation des Treibers durchsuchen, den Sie verwenden möchten. Sie finden nützliche Informationen in der Onlinehilfe zu diesem Treiber, auf die Sie mit ODBC-Administrator zugreifen können. Diese Hilfedateien sind normalerweise im Verzeichnis WINDOWS\SYSTEM für Windows NT, Windows 3.1 oder Windows 95 platziert werden.  
  
###### <a name="to-obtain-online-help-for-your-odbc-driver"></a>So greifen Sie auf die Onlinehilfe des ODBC-Treibers zu  
  
1.  Starten Sie den ODBC-Administrator.  
  
2.  Klicken Sie auf **Hinzufügen**.  
  
3.  Wählen Sie den Namen des Treibers aus.  
  
4.  Klicken Sie auf **OK**.  
  
 Wenn ODBC-Administrator die Informationen zum Erstellen einer neuen Datenquelle für diesen speziellen Treiber anzeigt, klicken Sie auf **Hilfe**. Hierdurch wird die Hilfedatei für diesen Treiber geöffnet, die in der Regel wichtige Informationen zu dessen Verwendung enthält.  
  
## <a name="see-also"></a>Siehe auch  
 [Datenquelle (ODBC)](../../data/odbc/data-source-odbc.md)