---
title: BSCMAKE-Referenz | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-tools
ms.topic: reference
dev_langs:
- C++
helpviewer_keywords:
- BSCMAKE, reference
- Microsoft Browse Information Maintenance Utility
- browse windows
- browse information files (.bsc), building
- .bsc files, building
- bsc files, building
- BSCMAKE
ms.assetid: b97ad994-1355-4809-98db-6abc12c6fb13
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: de8e71a448c71fd18ba9cba99cb9b7347598489c
ms.sourcegitcommit: be2a7679c2bd80968204dee03d13ca961eaa31ff
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/03/2018
---
# <a name="bscmake-reference"></a>BSCMAKE-Referenz
> [!WARNING]
> Obwohl BSCMAKE weiterhin mit Visual Studio installiert wird, wird es nicht mehr von der IDE verwendet. Seit Visual Studio 2008 werden Browse- und Symbolinformationen automatisch in einer SQL Server-.SDF-Datei im Projektmappenordner gespeichert.  
  
 Das Microsoft Browse Information Maintenance-Programm (BSCMAKE.EXE) erstellt eine neue Browseinformationsdatei (.bsc) aus SBR-Dateien, die während der Kompilierung erstellt wurden. Bestimmte Tools eines Drittanbieters verwenden BSC-Dateien für die Codeanalyse. 
  
 Wenn Sie ein Programm erstellen, können Sie eine Browseinformationsdatei für das Programm automatisch mithilfe von BSCMAKE zum Erstellen der Datei erstellen. Sie müssen nicht wissen, wie BSCMAKE ausgeführt wird, wenn Sie Ihre Browseinformationsdatei in der Visual C++-Entwicklungsumgebung erstellen. Vielleicht möchten Sie dieses Thema jedoch lesen, um die verfügbaren Optionen kennenzulernen.  
  
 Wenn Sie ein Programm außerhalb der Entwicklungsumgebung erstellen, können Sie weiterhin eine benutzerdefinierte BSC-Datei erstellen, die Sie in der Umgebung untersuchen können. Führen Sie BSCMAKE für die SBR-Dateien aus, die Sie während der Kompilierung erstellt haben.  
  
> [!NOTE]
>  Sie können dieses Tool nur von Visual Studio Developer-Eingabeaufforderung starten. Sie können es nicht von einer Systemeingabeaufforderung oder vom Datei-Explorer aus starten.  
  
 Dieser Abschnitt schließt folgende Themen ein:  
  
-   [Erstellen von Browseinformationsdateien: Übersicht](../../build/reference/building-browse-information-files-overview.md)  
  
-   [Erstellen einer BSC-Datei](../../build/reference/building-a-dot-bsc-file.md)  
  
-   [BSCMAKE-Befehlszeile](../../build/reference/bscmake-command-line.md)  
  
-   [BSCMAKE-Befehlszeile](../../build/reference/bscmake-command-file-response-file.md)  
  
-   [BSCMAKE-Optionen](../../build/reference/bscmake-options.md)  
  
-   [BSCMAKE-Exitcodes](../../build/reference/bscmake-exit-codes.md)  
  
## <a name="see-also"></a>Siehe auch  
 [C/C++-Buildtools](../../build/reference/c-cpp-build-tools.md)