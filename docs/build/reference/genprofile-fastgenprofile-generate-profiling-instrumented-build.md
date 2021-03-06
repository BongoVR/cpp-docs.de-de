---
title: / GENPROFILE, / fastgenprofile (Profilerstellung instrumentierenden Build generieren) | Microsoft Docs
ms.custom: ''
ms.date: 03/14/2018
ms.technology:
- cpp-tools
ms.topic: reference
f1_keywords:
- GENPROFILE
- FASTGENPROFILE
- /GENPROFILE
- /FASTGENPROFILE
helpviewer_keywords:
- GENPROFILE
- FASTGENPROFILE
ms.assetid: deff5ce7-46f5-448a-b9cd-a7a83a6864c6
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 05d7961ff46661b8f6df2768591932699c3965d4
ms.sourcegitcommit: be2a7679c2bd80968204dee03d13ca961eaa31ff
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/03/2018
---
# <a name="genprofile-fastgenprofile-generate-profiling-instrumented-build"></a>/GENPROFILE, /FASTGENPROFILE (Profilerstellung instrumentierenden Build generieren)

Gibt die Generierung einer PGD-Datei durch den Linker an, um die profilgesteuerte Optimierung (PGO) zu unterstützen. **/ GENPROFILE** und **/fastgenprofile** verwenden unterschiedliche Standardparameter. Verwendung **/genprofile** , Geschwindigkeit und speicherauslastung während der profilerstellung Genauigkeit vorzuziehen. Verwendung **/fastgenprofile** , geringere speicherauslastung und Geschwindigkeit Genauigkeit vorzuziehen.

## <a name="syntax"></a>Syntax

> **/ GENPROFILE**[**:**{[**COUNTER32**|**COUNTER64**] | [ **EXACT**|**NOEXACT**] | **MEMMAX =**_#_|**MEMMIN =**_#_| [ **Pfad**|**NOPATH** ] | [ **TRACKEH** |**NOTRACKEH** ] | **PGD =**_Filename_}]<br/>
> **/ FASTGENPROFILE**[**:**{[**COUNTER32**|**COUNTER64**] | [ **EXACT**|**NOEXACT**] | **MEMMAX =**_#_|**MEMMIN =**_#_| [ **Pfad**|**NOPATH** ] | [ **TRACKEH** |**NOTRACKEH** ] | **PGD =**_Filename_}]

### <a name="arguments"></a>Argumente

Eines der folgenden Argumente angegeben werden kann, um **/genprofile** oder **/fastgenprofile**. Argumente, die hier aufgeführten getrennt durch einen senkrechten Strich (**|**) Zeichen schließen sich gegenseitig. Verwenden Sie ein Komma (**,**) Zeichen zum Trennen von Optionen.

**COUNTER32** &AMP;#124; **COUNTER64**<br/>
Verwenden Sie **COUNTER32** an die Verwendung von 32-Bit-Prüfpunkt-Leistungsindikatoren und **COUNTER64** 64-Bit-Prüfpunkt-Leistungsindikatoren an. Geben Sie bei **/genprofile**, der Standardwert ist **COUNTER64**. Geben Sie bei **/fastgenprofile**, der Standardwert ist **COUNTER32**.

**EXACT** &#124; **NOEXACT**<br/>
Verwendung **EXACT** um threadsichere Ineinandergreifende Inkremente für Tests anzugeben. **NOEXACT** gibt ungeschützte inkrementoperationen für Tests an. Die Standardeinstellung ist **NOEXACT**.

**MEMMAX**=*Wert*, **MEMMIN**=*Wert*<br/>
Verwendung **MEMMAX** und **MEMMIN** an die maximalen und minimalen Reservierungsgrößen für Trainingsdaten im Arbeitsspeicher. Der Wert entspricht der Größe des in Bytes zu reservierenden Arbeitsspeichers. Standardmäßig werden diese Werte über eine interne Heuristik bestimmt.

**PATH**  &#124; **NOPATH** <br/>
Verwendung **Pfad** auf einen separaten Satz von PGO-Indikatoren für jeden eindeutigen Pfad zu einer Funktion anzugeben. Verwendung **NOPATH** nur einen Satz von Indikatoren für jede Funktion angeben. Geben Sie bei **/genprofile**, der Standardwert ist **Pfad** . Geben Sie bei **/fastgenprofile**, der Standardwert ist **NOPATH** .

**TRACKEH**  &#124; **NOTRACKEH** <br/>
Gibt an, ob zusätzliche Indikatoren verwendet werden sollen, um eine genaue Anzahl beizubehalten, wenn während des Trainings Ausnahmen ausgelöst werden. Verwendung **TRACKEH** um zusätzliche Indikatoren für eine genaue Anzahl anzugeben. Verwenden Sie **NOTRACKEH** um einzelne Indikatoren für Code anzugeben, die keine Ausnahme verwendet behandeln oder, ist nicht auftreten Ausnahmen in Ihren trainingsszenarien.  Geben Sie bei **/genprofile**, der Standardwert ist **TRACKEH** . Geben Sie bei **/fastgenprofile**, der Standardwert ist **NOTRACKEH** .

**PGD**=*Dateiname*<br/>
Gibt einen Basisdateinamen für die PGD-Datei an. Standardmäßig wird vom Linker der Name der ausführbaren Basisbilddatei mit der Erweiterung PGD verwendet.

## <a name="remarks"></a>Hinweise

Die **/genprofile** und **/fastgenprofile** Optionen weisen den Linker aus, um die profilerstellung zur Unterstützung des anwendungstrainings für die profilgesteuerte Optimierung (PGO) erforderliche Datei zu generieren. Diese Optionen sind neu in Visual Studio 2015. Bevorzugen Sie diese Optionen, um die veraltete **/LTCG: PGINSTRUMENT**, **/PGD** und **/POGOSAFEMODE** Optionen und die **PogoSafeMode**,  **VCPROFILE_ALLOC_SCALE** und **VCPROFILE_PATH** Umgebungsvariablen. Die vom Anwendungstraining generierten Informationen zur Profilerstellung werden als Eingabe verwendet, um während der Builderstellung Zieloptimierungen für vollständige Programme durchzuführen. Sie können zusätzliche Optionen festlegen, um die verschiedenen Features für die Profilerstellung während des App-Trainings und der App-Erstellung hinsichtlich der Leistung zu steuern. Vom angegebenen Standardoptionen erzielen **/genprofile** geben die genauesten Ergebnisse, insbesondere bei großen, komplexen Multithread-apps. Die **/fastgenprofile** Option verwendet unterschiedliche Standardwerte für einen geringeren Speicherbedarf und höhere Geschwindigkeiten während des Trainings zu Lasten der Genauigkeit.

Profilerstellungsinformationen aufgezeichnet wird, wenn Sie die instrumentierte app ausführen, nachdem Sie mithilfe von erstellen **/genprofile** von **/fastgenprofile**. Diese Informationen werden erfasst, bei der Angabe der [/useprofile](useprofile.md) (Linkeroption) zum Ausführen der profilerstellung Schritt und dann verwendet, um die optimierte Buildschritt geführt. Weitere Informationen zum Trainieren Ihrer app und Details über die gesammelten Daten finden Sie unter [Profilgesteuerte Optimierung](profile-guided-optimizations.md).

Sie müssen auch angeben, **/LTCG** beim Angeben von **/genprofile** oder **/fastgenprofile**.

### <a name="to-set-this-linker-option-in-the-visual-studio-development-environment"></a>So legen Sie diese Linkeroption in der Visual Studio-Entwicklungsumgebung fest

1. Öffnen Sie das Dialogfeld **Eigenschaftenseiten** des Projekts. Weitere Informationen finden Sie unter [Einstellung von Visual C++-Projekteigenschaften](../../ide/working-with-project-properties.md).

1. Wählen Sie die **Konfigurationseigenschaften** > **Linker** > **Befehlszeile** Eigenschaftenseite.

1. Geben Sie die **/genprofile** oder **/fastgenprofile** Optionen und Argumente in der **Zusatzoptionen** Feld. Wählen Sie **OK** zum Speichern der Änderungen.

### <a name="to-set-this-linker-option-programmatically"></a>So legen Sie diese Linkeroption programmgesteuert fest

- Siehe <xref:Microsoft.VisualStudio.VCProjectEngine.VCLinkerTool.AdditionalOptions%2A>.

## <a name="see-also"></a>Siehe auch

[Festlegen von Linkeroptionen](../../build/reference/setting-linker-options.md)<br/>
[Linkeroptionen](../../build/reference/linker-options.md)<br/>
[/LTCG (Link-Zeitcodegenerierung)](../../build/reference/ltcg-link-time-code-generation.md)<br/>
