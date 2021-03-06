---
title: CRT-Bibliotheksfunktionen | Microsoft-Dokumentation
ms.custom: ''
ms.date: 03/13/2018
ms.technology:
- cpp-standard-libraries
ms.topic: conceptual
f1_keywords:
- c.runtime
dev_langs:
- C++
helpviewer_keywords:
- MSVCR71.dll
- libraries [C++], multithreaded
- library files, run-time
- LIBCMT.lib
- LIBCP.lib
- LIBCPMT.lib
- run-time libraries, C
- CRT, release versions
- MSVCP71.dll
- LIBC.lib
- libraries [C++]
- libraries [C++], run-time
- linking [C++], libraries
ms.assetid: a889fd39-807d-48f2-807f-81492612463f
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 4b20fa6862a835ca913a2865a651112584966af3
ms.sourcegitcommit: be2a7679c2bd80968204dee03d13ca961eaa31ff
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/03/2018
---
# <a name="crt-library-features"></a>CRT-Bibliotheksfunktionen

In diesem Thema werden die verschiedenen LIB-Dateien erläutert, die die C-Laufzeitbibliotheken sowie ihre zugeordneten Compileroptionen und Präprozessordirektiven bilden.

## <a name="c-run-time-libraries-crt"></a>C-Laufzeitbibliotheken (CRT)

Die CRT (C Run-time Library, C-Laufzeitbibliothek) ist Bestandteil der C++-Standardbibliothek, die die ISO C99-Standardbibliothek umfasst. Die Visual C++-Bibliotheken, die die CRT implementieren, unterstützen die Entwicklung von nativem Code und Mischungen aus nativem und verwaltetem Code. Alle Versionen der CRT unterstützen Multithreaded-Entwicklung. Die meisten Bibliotheken unterstützen sowohl statisches Linken (Binden), um die Bibliothek direkt in Ihren Code einzubinden, oder dynamisches Linken, damit in Ihrem Code allgemeine DLL-Dateien verwendet werden können.

Ab Visual Studio 2015 wurde die CRT in neue Binärdateien umgestaltet. Die UCRT (Universal CRT) enthält die Funktionen und globalen Elemente, die durch die Standard-C99 CRT-Bibliothek exportiert werden. Die UCRT ist nun eine Windows-Komponente und wird als Bestandteil von Windows 10 bereitgestellt. Die statische Bibliothek, die DLL-Importbibliothek und die Headerdateien für die UCRT sind jetzt im Windows 10 SDK zu finden. Wenn Sie Visual C++ installieren, installiert Visual Studio-Setup die Teilmenge des Windows 10 SDKs, die erforderlich ist, um die UCRT verwenden zu können. Sie können die UCRT unter jeder Version von Windows verwenden, die von Visual Studio 2015 und späteren Versionen unterstützt wird. Sie können die URCT über vcredist für unterstützte Versionen von Windows neu verteilen, die nicht Windows 10 sind. Weitere Informationen finden Sie unter [Redistributing Visual C++ Files](../ide/redistributing-visual-cpp-files.md).

In der folgenden Tabelle sind die Bibliotheken aufgelistet, die die UCRT implementieren.

|Bibliothek|Zugehörige DLL|Eigenschaften|Option|Präprozessordirektiven|
|-------------|--------------------|---------------------|------------|-----------------------------|
|libucrt.lib|Keiner|Bindet die UCRT statisch in Ihren Code ein.|**/MT**|_MT|
|libucrtd.lib|Keiner|Die Debugversion der UCRT für statisches Linken. Nicht neu verteilbar.|**/MTd**|_DEBUG, _MT|
|ucrt.lib|ucrtbase.dll|DLL-Importbibliothek für die UCRT.|**/MD**|_MT, _DLL|
|ucrtd.lib|ucrtbased.dll|DLL-Importbibliothek für die Debugversion der UCRT. Nicht neu verteilbar.|**/MDd**|_DEBUG, _MT, _DLL|

Die vcruntime-Bibliothek enthält Visual C++-CRT-implementierungsspezifischen Code, beispielsweise Ausnahmebehandlungs- und Debugunterstützung, Laufzeitprüfungen und Typinformationen, Implementierungsdetails und bestimmte erweiterte Bibliotheksfunktionen. Diese Bibliothek ist speziell entsprechend der Version des verwendeten Compilers.

In der folgenden Tabelle sind die Bibliotheken aufgelistet, die die vcruntime-Bibliothek implementieren.

|Bibliothek|Zugehörige DLL|Eigenschaften|Option|Präprozessordirektiven|
|-------------|--------------------|---------------------|------------|-----------------------------|
|libvcruntime.lib|Keiner|Wird statisch in Ihren Code eingebunden.|**/MT**|_MT|
|libvcruntimed.lib|Keiner|Die Debugversion für statisches Linken. Nicht neu verteilbar.|**/MTd**|_MT, _DEBUG|
|vcruntime.lib|vcruntime\<Version>.dll|DLL-Importbibliothek für die vcruntime.|**/MD**|_MT, _DLL|
|vcruntimed.lib|vcruntime\<Version>d.dll|DLL-Importbibliothek für die Debug-vcruntime. Nicht neu verteilbar.|**/MDd**|_DEBUG, _MT, _DLL|

Der Code, von dem die CRT initialisiert wird, befindet sich in einer von mehreren Bibliotheken, je nachdem, ob die CRT-Bibliothek statisch oder dynamisch gebunden wird oder als systemeigener, verwalteter oder gemischter Code vorliegt. Dieser Code verwaltet den CRT-Start, die interne threadbezogene Dateninitialisierung und die Beendigung. Der Code ist speziell entsprechend der Version des verwendeten Compilers. Diese Bibliothek wird immer statisch gebunden, auch wenn eine dynamisch gebundene UCRT verwendet wird.

In der folgenden Tabelle sind die Bibliotheken aufgelistet, die die CRT-Initialisierung und -Beendigung implementieren.

|Bibliothek|Eigenschaften|Option|Präprozessordirektiven|
|-------------|---------------------|------------|-----------------------------|
|LIBCMT.lib|Bindet den systemeigenen CRT-Startcode statisch in Ihren Code ein.|**/MT**|_MT|
|libcmtd.lib|Bindet die Debugversion des systemeigenen CRT-Startcode statisch ein. Nicht neu verteilbar.|**/MTd**|_DEBUG, _MT|
|msvcrt.lib|Statische Bibliothek für den systemeigenen CRT-Startcode zur Verwendung mit DLL UCRT und vcruntime.|**/MD**|_MT, _DLL|
|msvcrtd.lib|Statische Bibliothek für die Debugversion des systemeigenen CRT-Startcodes zur Verwendung mit DLL UCRT und vcruntime. Nicht neu verteilbar.|**/MDd**|_DEBUG, _MT, _DLL|
|msvcmrt.lib|Statische Bibliothek für den gemischten systemeigenen und verwalteten CRT-Startcode zur Verwendung mit DLL UCRT und vcruntime.|**/clr**||
|msvcmrtd.lib|Statische Bibliothek für die Debugversion des gemischten systemeigenen und verwalteten CRT-Startcodes zur Verwendung mit DLL UCRT und vcruntime. Nicht neu verteilbar.|**/clr**||
|msvcurt.lib|**Veraltet** Statische Bibliothek für die ausschließlich verwaltete CRT.|**/clr:pure**||
|msvcurtd.lib|**Veraltet** Statische Bibliothek für die Debugversion der ausschließlich verwalteten CRT. Nicht neu verteilbar.|**/clr:pure**||

Wenn Sie Ihr Programm über die Befehlszeile ohne eine Compileroption verknüpfen, die die C-Laufzeitbibliothek angibt, verwendet der Linker die statisch verknüpften CRT-Bibliotheken: „libcmt.lib“, „libvcruntime.lib“ und „libucrt.lib“.

Die Verwendung der statisch verknüpften CRT bedeutet, dass alle von der C-Laufzeitbibliothek gespeicherten Zustandsinformationen für diese CRT-Instanz lokal sind. Wenn Sie bei einer statisch verknüpften CRT [strtok, _strtok_l, wcstok, _wcstok_l, _mbstok, _mbstok_l](../c-runtime-library/reference/strtok-strtok-l-wcstok-wcstok-l-mbstok-mbstok-l.md) verwenden, ist die Position des `strtok`-Parsers nicht mit dem `strtok`-Zustand verbunden, der im Code des gleichen Prozesses (jedoch in einer anderen DLL oder EXE) verwendet wird, welcher mit einer anderen Instanz der statischen CRT verknüpft ist. Im Gegensatz dazu teilen dynamisch verknüpfte CRT den Zustand für sämtlichen Code innerhalb eines Prozesses, der dynamisch mit der CRT verknüpft ist. Bei den neuen sichereren Versionen dieser Funktionen wie `strtok_s` tritt dieses Problem nicht auf.

Da eine durch das Verknüpfen mit einer statischen CRT erstellten DLL ihren eigenen CRT-Zustand besitzt, wird in einer DLL das statische Verknüpfen mit einer CRT nicht empfohlen, es sei denn, dass die daraus resultierenden Konsequenzen verstanden werden und erwünscht sind. Wenn Sie z. B. [_set_se_translator](../c-runtime-library/reference/set-se-translator.md) in einer ausführbaren Datei aufrufen, die die DLL lädt, die mit ihrer eigenen statischen CRT verknüpft ist, werden alle vom Code in der DLL generierten Hardwareausnahmen vom Konvertierungsprogramm nicht erfasst, wohingegen die vom Code in der Hauptausführungsdatei generierten Hardwareausnahmen erfasst werden.

Wenn Sie den **/clr** -Compilerschalter verwenden, wird der Code mit der statischen Bibliothek msvcmrt.lib verknüpft. Die statische Bibliothek stellt einen Proxy zwischen dem verwalteten Code und der systemeigenen CRT bereit. Die statisch verknüpfte CRT (Option **/MT** oder Option **/MTd** ) können Sie nicht mit **/clr**verwenden. Verwenden Sie stattdessen die dynamisch verknüpften Bibliotheken (**/MD** oder **/MDd**).

Weitere Informationen zur Verwendung der CRT mit **/clr** finden Sie unter [Gemischte (native und verwaltete) Assemblys](../dotnet/mixed-native-and-managed-assemblies.md).

Um eine Debugversion der Anwendung zu erstellen, muss das [_DEBUG](../c-runtime-library/debug.md)-Flag definiert sein und die Anwendung muss mit einer Debugversion von einer dieser Bibliotheken verknüpft sein. Weitere Informationen zur Verwendung der Debugversionen der Bibliotheksdateien finden Sie unter [CRT-Debugverfahren](/visualstudio/debugger/crt-debugging-techniques).

Diese Version der CRT ist nicht vollständig mit dem Standard C99 konform. Insbesondere der \<tgmath.h>-Header und die CX_LIMITED_RANGE/FP_CONTRACT-Pragmamakros werden nicht unterstützt. Für bestimmte Elemente, etwa die Bedeutung von Parameterbezeichnern in Standard-E/A-Funktionen, werden standardmäßig frühere Interpretationen verwendet. Sie können die /Zc-Compileroptionen für Konformität verwenden und Linkeroptionen angeben, um einige Aspekte der Bibliothekskonformität zu steuern.

## <a name="c-standard-library"></a>C++-Standardbibliothek

|C++-Standardbibliothek|Eigenschaften|Option|Präprozessordirektiven|
|----------------------------|---------------------|------------|-----------------------------|
|libcpmt.lib|Multithreaded, statischer Link|**/MT**|_MT|
|msvcprt.lib|Multithreaded, dynamischer Link (Importbibliothek für MSVCP*version*.dll)|**/MD**|_MT, _DLL|
|libcpmtd.lib|Multithreaded, statischer Link|**/MTd**|_DEBUG, _MT|
|msvcprtd.lib|Multithreaded, dynamischer Link (Importbibliothek für MSVCP*version*D.DLL)|**/MDd**|_DEBUG, _MT, _DLL|

Wenn Sie eine Releaseversion des Projekts erstellen, wird abhängig von der ausgewählten Compileroption (Multithreaded, DLL, /clr) eine der grundlegenden C-Laufzeitbibliotheken (libcmt.lib, msvcmrt.lib, msvcrt.lib) standardmäßig verknüpft. Wenn Sie eine der [Headerdateien der C++-Standardbibliothek](../standard-library/cpp-standard-library-header-files.md) in den Code einfügen, wird von Visual C++ eine C++-Standardbibliothek automatisch zur Kompilierzeit eingebunden. Zum Beispiel:

```cpp
#include <ios>
```

Für die binäre Kompatibilität kann mehr als eine DLL-Datei von einer einzelnen Importbibliothek angegeben werden. Versionsupdates führen womöglich *dot-Bibliotheken* ein, separate DLLs, die neue Bibliotheksfunktionen enthalten. Beispielsweise wurde durch Visual Studio 2017 15.6 „msvcp140_1.dll“ eingeführt, um zusätzliche Standardbibliotheksfunktionen zu unterstützen, ohne die von „msvcp140.dll“ unterstützte ABI zu unterbrechen. Die „msvcprt.lib“-Importbibliothek, die im Toolset für Visual Studio 2017 Version 15.6 enthalten ist, unterstützt beide DLLs, und die Komponente vcredist installiert für diese Version beide DLLs. Sobald eine dot-Bibliothek geliefert wird, verfügt sie über eine feste ABI und wird nie über eine Abhängigkeit auf einer späteren dot-Bibliothek verfügen.

## <a name="what-problems-exist-if-an-application-uses-more-than-one-crt-version"></a>Welche Probleme gibt es, wenn in einer Anwendung mehrere CRT-Version verwendet werden?

Wenn Sie mehrere DLL- oder EXE-Dateien besitzen, dann verfügen Sie möglicherweise auch über mehr als eine CRT-Instanz, unabhängig davon, ob Sie verschiedene Versionen von Visual C++ verwenden. Das statische Verknüpfen der CRT mit mehreren DLLs kann das gleiche Problem darstellen. Entwickler, bei denen dieses Problem mit statischen CRTs auftritt, sollen mit **/MD** kompilieren, um die CRT-DLL zu verwenden. Wenn Ihre DLLs CRT-Ressourcen über die DLL-Grenze hinaus übergeben, treten möglicherweise Probleme mit nicht übereinstimmenden CRTs auf, und Sie müssen Ihr Projekt mit Visual C++ neu kompilieren.

Wenn das Programm mehr als eine CRT-Version verwendet, muss beim Übergeben bestimmter CRT-Objekte (wie z. B. Dateihandles, Gebietsschemas und Umgebungsvariablen) über DLL-Grenzen hinweg sorgfältig vorgegangen werden. Weitere Informationen zu diesen Problemen und den jeweiligen Lösungsmöglichkeiten finden Sie unter [Potenzielle Fehler bei der Übergabe von CRT-Objekten über DLL-Grenzen](../c-runtime-library/potential-errors-passing-crt-objects-across-dll-boundaries.md).

## <a name="see-also"></a>Siehe auch

[C-Laufzeitbibliotheksreferenz](../c-runtime-library/c-run-time-library-reference.md)
