---
title: "Problembehandlung bei IntelliSense in C++-Projekten"
ms.custom: na
ms.date: "11/17/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: na
ms.suite: na
ms.technology: 
  - "devlang-csharp"
ms.tgt_pltfrm: na
ms.topic: "article"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - ".ncb-Dateien"
  - "IntelliSense, Problembehandlung bei Fehlern in C++-Projekten"
  - "ncb-Dateien"
  - "Problembehandlung bei IntelliSense"
  - "Problembehandlung in Visual C++, IntelliSense"
ms.assetid: 72e4eb39-66d3-403d-8da7-00ed288a1899
caps.latest.revision: 20
caps.handback.revision: "20"
ms.author: "mblome"
manager: "douge"
---
# Problembehandlung bei IntelliSense in C++-Projekten
Die Ausführung von IntelliSense kann unter bestimmten Bedingungen unterbrochen werden.  Anhand des folgenden Verfahrens können Sie feststellen, warum IntelliSense in Verbindung mit Ihren C\+\+\-Projekten nicht funktioniert.  
  
### So prüfen Sie IntelliSense\-Fehler in C\+\+\-Projekten  
  
1.  Stellen Sie sicher, dass das Visual C\+\+\-Projekt keine Kompilierungsfehler enthält.  
  
    1.  Wenn das Projekt ein Makefile\-Projekt ist, informieren Sie sich unter [Gewusst wie: Aktivieren von IntelliSense für Makefile\-Projekte](../ide/how-to-enable-intellisense-for-makefile-projects.md).  
  
2.  Stellen Sie sicher, dass sich "stdafx.h" im Includepfad befindet.  Weitere Informationen zu Includepfaden in Visual C\+\+\-Projekten finden Sie unter [\#include\-Direktive](../preprocessor/hash-include-directive-c-cpp.md) und [\/I \(Zusätzliche Includeverzeichnisse\)](../build/reference/i-additional-include-directories.md).  
  
## Einschränkungen von IntelliSense  
 IntelliSense ist in C\+\+\-Projekten unter den folgenden Umständen nicht funktionsfähig:  
  
-   Der Cursor befindet sich in einem Codekommentar.  
  
-   Sie schreiben ein Zeichenfolgenliteral.  
  
-   Ein Syntaxfehler wurde oberhalb des Cursors gefunden.  
  
-   Die Lösung besteht entweder aus der Syntax für verwaltetes C\+\+ oder der vorherigen Managed Extensions for C\+\+\-Syntax.  
  
-   IntelliSense wird nicht vollständig unterstützt, wenn Sie mehrfach mit der `#include`\-Direktive auf eine Headerdatei verweisen, und die Bedeutung dieser Headerdatei ändert sich aufgrund der unterschiedlichen Makrozustände, die mit der `#define`\-Direktive definiert werden.  Mit anderen Worten: Wenn eine Headerdatei mehrfach eingefügt wird und sich die entsprechende Verwendung bei unterschiedlichen Makrozustandswerten ändert, treten bei IntelliSense möglicherweise Fehler auf.  
  
## Siehe auch  
 [Troubleshooting IntelliSense](assetId:///c1b3adb9-0d48-4770-a51e-392ed818c484)   
 [Gewusst wie: Organisieren von Projektausgabedateien für Builds](../ide/how-to-organize-project-output-files-for-builds.md)