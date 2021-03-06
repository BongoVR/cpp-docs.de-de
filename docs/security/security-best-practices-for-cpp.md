---
title: Bewährte Sicherheitsmethoden für C++ | Microsoft Docs
ms.custom: ''
ms.date: 05/08/2018
ms.technology:
- cpp-windows
ms.topic: conceptual
f1_keywords:
- securitybestpracticesVC
dev_langs:
- C++
helpviewer_keywords:
- Visual C++, security
- security [C++]
- security [C++], best practices
ms.assetid: 86acaccf-cdb4-4517-bd58-553618e3ec42
author: mikeblome
ms.author: mikeblome
ms.workload:
- cplusplus
ms.openlocfilehash: 35114d2fff4975cfca1681a7f5861c81bd979ef5
ms.sourcegitcommit: 96cdc2da0d8c3783cc2ce03bd280a5430e1ac01d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/10/2018
---
# <a name="security-best-practices-for-c"></a>Empfohlene Vorgehensweisen bezüglich der Sicherheit in C++

Dieser Artikel enthält Informationen über Sicherheitstools und Vorgehensweisen. Ihre Verwendung macht eine Anwendung zwar nicht immun gegen Angriffe, aber sie verringert die Wahrscheinlichkeit erfolgreicher Angriffe.  
  
## <a name="visual-c-security-features"></a>Visual C++-Sicherheitsfeatures

 Diese Sicherheitsfunktionen sind in den Visual C++-Compiler und den Visual C++-Linker integriert:  
  
 [/guard (Ablaufsteuerungsschutz aktivieren)](../build/reference/guard-enable-control-flow-guard.md)  
 Veranlasst den Compiler, die Ablaufsteuerung für indirekte Aufrufziele zum Zeitpunkt der Kompilierung zu analysieren und dann Code einzufügen, um die Ziele zur Laufzeit zu überprüfen.  
  
 [/GS (Puffersicherheitsüberprüfung)](../build/reference/gs-buffer-security-check.md)  
 Der Compiler wird angewiesen, Überlauferkennungscode in Funktionen einzufügen, die Angriffen ausgesetzt sein können. Wenn ein Überlauf erkannt wird, wird die Programmausführung angehalten. Diese Option ist standardmäßig aktiviert.  
  
 [/SAFESEH (Image weist sichere Ausnahmehandler auf)](../build/reference/safeseh-image-has-safe-exception-handlers.md)  
 Der Linker wird angewiesen, dem Ausgabeabbild eine Tabelle mit den Adressen aller Ausnahmehandler hinzuzufügen. Zur Laufzeit verwendet das Betriebssystem diese Tabelle, um sicherzustellen, dass nur rechtmäßige Ausnahmehandler ausgeführt werden. Dadurch wird verhindert, dass in böswilligen Angriffen zur Laufzeit eingeschleuste Ausnahmehandler ausgeführt werden. Diese Option ist standardmäßig deaktiviert.  
  
 [/ NXCOMPAT](../build/reference/nxcompat.md),  [ /NXCOMPAT (kompatibel mit Datenausführungsverhinderung)](../build/reference/nxcompat-compatible-with-data-execution-prevention.md)  
 Diese Compiler- und Linkeroptionen ermöglichen Kompatibilität mit der Datenausführungsverhinderung. DEP schützt die CPU vor der Ausführung von Seiten, die keine Codepages sind.  
  
 [/analyze (Codeanalyse)](../build/reference/analyze-code-analysis.md)  
 Diese Compileroption aktiviert die Codeanalyse, die über potentielle Sicherheitslücken wie Pufferüberlauf, nicht initialisierten Speicher, Dereferenzierung von NULL-Zeigern und Speicherverlusten Bericht erstattet. Diese Option ist standardmäßig deaktiviert. Weitere Informationen finden Sie unter [Codeanalyse für C/C++-Übersicht](/visualstudio/code-quality/code-analysis-for-c-cpp-overview).  
  
 [/DYNAMICBASE (Address Space Layout Randomization verwenden)](../build/reference/dynamicbase-use-address-space-layout-randomization.md)  
 Diese Linkeroption ermöglicht das Erstellen eines ausführbaren Images, das am Anfang der Ausführung an anderen Orten im Arbeitsspeicher geladen werden kann. Durch diese Option lässt sich die Position des Stapels im Arbeitsspeicher auch schlechter vorhersagen.  
  
## <a name="security-enhanced-crt"></a>CRT mit erweiterter Sicherheit  
 Die C-Laufzeitbibliothek (CRT) wurde um sichere Versionen von Funktionen erweitert, die ein Sicherheitsrisiko darstellen, z. B. die aufwerfen, die ungeprüfte `strcpy`-Funktion zum Kopieren von Zeichenfolgen. Da die älteren, nicht sicheren Versionen dieser Funktionen jetzt veraltet sind, verursacht ihre Verwendung Compilerwarnungen. Es wird empfohlen, die sicheren Versionen dieser CRT-Funktionen zu verwenden, anstatt die Compilerwarnungen zu unterdrücken. Weitere Informationen finden Sie unter [Security Features in the CRT](../c-runtime-library/security-features-in-the-crt.md).  
  
## <a name="safeint-library"></a>SafeInt-Bibliothek  
 [SafeInt-Bibliothek](../windows/safeint-library.md) wird verhindert, dass ganze Zahl einen Überlauf und andere als Angriffspunkt geeigneten Fehler, die auftreten können, wenn die Anwendung mathematische Vorgänge ausführt. Die `SafeInt` -Bibliothek umfasst die [SafeInt-Klasse](../windows/safeint-class.md), [SafeIntException-Klasse](../windows/safeintexception-class.md), und mehrere [SafeInt-Funktionen](../windows/safeint-functions.md).  
  
 Die `SafeInt`-Klasse schützt vor Ganzzahlüberlauf und Exploits vom Typ "Division durch 0". Sie können sie zum Behandeln von Vergleichen zwischen Werten unterschiedlicher Typen verwenden. I stellt zwei Fehlerbehandlungsrichtlinien bereit. Gemäß Standardrichtlinie löst die `SafeInt`-Klasse eine `SafeIntException`-Klassenausnahme aus, um zu berichten, warum ein mathematischer Vorgang nicht abgeschlossen werden kann. Gemäß der zweiten Richtlinie beendet die `SafeInt`-Klasse die Programmausführung. Sie können auch eine benutzerdefinierte Richtlinie definieren.  
  
 Jede `SafeInt`-Funktion schützt einen mathematischen Vorgang vor einem als Angriffspunkt geeigneten Fehler. Sie können zwei verschiedene Arten von Parametern verwenden, ohne sie in den gleichen Typ konvertieren zu müssen. Verwenden Sie die `SafeInt`-Klasse, um mehrere mathematische Vorgänge zu schützen.  
  
## <a name="checked-iterators"></a>Überprüfte Iteratoren  
 Ein überprüfter Iterator erzwingt Containergrenzen. Wenn ein überprüfter Iterator außerhalb der zulässigen Grenzen liegt, wird eine Ausnahme generiert und die Programmausführung beendet. Ein überprüfter Iterator der Antwort, die von Werten abhängig sind, die Präprozessordefinitionen zugewiesen sind stellt andere Antwortebenen bereit wie z. B.  **\_SECURE\_SCL\_löst** und  **\_ITERATOR\_DEBUGGEN\_Ebene**. Z. B. am  **\_ITERATOR\_DEBUGGEN\_LEVEL = 2**, ein überprüfter Iterator stellt umfassende korrektheitsüberprüfungen im Debugmodus befindet, die verfügbaren mit erfolgen bestätigt. Weitere Informationen finden Sie unter [überprüfte Iteratoren](../standard-library/checked-iterators.md) und [ \_ITERATOR\_DEBUGGEN\_Ebene](../standard-library/iterator-debug-level.md).  
  
## <a name="code-analysis-for-managed-code"></a>Codeanalyse für verwalteten Code  
 Codeanalyse für verwalteten Code, auch bekannt als FxCop, überprüft Assemblys auf Übereinstimmung mit den .NET Framework-Entwurfsrichtlinien. FxCop analysiert den Code und die Metadaten in jeder Assembly und prüft in den folgenden Bereichen auf Fehler:  
  
-   Bibliotheksentwurf  
  
-   Lokalisierung  
  
-   Namenskonventionen   
  
-   Leistung  
  
-   Sicherheit  
  
## <a name="windows-application-verifier"></a>Windows Application Verifier  
 Der Application Verifier (AppVerifier) kann Ihnen dabei helfen, mögliche Probleme bei der Kompatibilität, der Stabilität und der Sicherheit der Anwendung zu identifizieren.  
  
 Der AppVerifier überwacht, wie eine Anwendung das Betriebssystem verwendet. Dateisystem, Registrierung, Arbeitsspeicher und APIs werden beobachtet, während die Anwendung ausgeführt wird, und es werden Quellcodepatches für die erkannten Probleme empfohlen.  
  
 Sie können den AppVerifier wie folgt verwenden:  
  
-   Auf potenzielle durch allgemeine Programmierfehler verursachte Anwendungskompatibilitätsfehler prüfen.  
  
-   Eine Anwendung auf speicherbezogene Probleme untersuchen.  

-   Potenzielle Sicherheitsprobleme in einer Anwendung aufdecken.  
  
 Der AppVerifier ist Teil der Anwendungskompatibilitäts-Toolkit, in der [Anwendungskompatibilität](http://go.microsoft.com/fwlink/p/?linkid=91277) auf der TechNet-Website.  
  

## <a name="windows-user-accounts"></a>Windows-Benutzerkonten  
 Das Verwenden von Windows-Benutzerkonten, die zur Gruppe der Administratoren gehören, setzt Entwickler und – durch entsprechende Erweiterung – auch Kunden Sicherheitsrisiken aus. Weitere Informationen finden Sie unter [Ausführen als Mitglied der Gruppe "Benutzer"](running-as-a-member-of-the-users-group.md) und [wie Benutzerkontensteuerung (UAC) wirkt sich auf Ihre Anwendung](how-user-account-control-uac-affects-your-application.md).

## <a name="guidance-for-speculative-execution-side-channels"></a>Leitfaden für spekulative Ausführung dienstseitige Kanäle

Informationen zum Identifizieren und zu mindern, gegen spekulative Ausführung clientseitigen Kanal Hardware Schwachstellen in der C++-Software finden Sie unter [C++-Entwicklerleitfaden für Spekulatives Ausführung dienstseitige Kanäle](developer-guidance-speculative-execution.md).

  
## <a name="see-also"></a>Siehe auch  
 <xref:System.Security>   
 [Sicherheit](/dotnet/standard/security/index)   
 [Wie Benutzerkontensteuerung (UAC) die Anwendung beeinflusst](how-user-account-control-uac-affects-your-application.md)
