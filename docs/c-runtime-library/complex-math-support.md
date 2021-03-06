---
title: C-Unterstützung für komplexe Mathematik| Microsoft-Dokumentation
ms.custom: ''
ms.date: 03/30/2018
ms.technology:
- cpp-standard-libraries
ms.topic: conceptual
f1_keywords:
- c.complex
dev_langs:
- C++
helpviewer_keywords:
- complex numbers, math routines
- math routines
- complex numbers
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 661e1367ea64713cf7a143f276cd195d54fecf85
ms.sourcegitcommit: be2a7679c2bd80968204dee03d13ca961eaa31ff
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/03/2018
---
# <a name="c-complex-math-support"></a>C-Unterstützung für komplexe Mathematik

Die Microsoft C-Laufzeitbibliothek (C Runtime Library, CRT) stellt komplexe Funktionen in der mathematischen Bibliothek bereit, einschließlich der laut ISO C99 erforderlichen Funktionen. Der Compiler unterstützt nicht direkt die Schlüsselwörter **complex** oder **_Complex**, deshalb nutzt die Microsoft-Implementierung Strukturtypen, um komplexe Zahlen darzustellen.

Diese Funktionen werden implementiert, damit die Sprache ebenso leistungsfähig wie korrekt ist. Da das korrekt gerundete Ergebnis nur sehr teuer errechenbar ist, wurden diese Funktionen dazu entworfen, eine starke Annäherung an das korrekt gerundete Ergebnis zu erzielen. In den meisten Fällen liegt das erzeugte Ergebnis innerhalb von +/-1 an der letzten Nachkommastelle des korrekt gerundeten Ergebnisses, obwohl die Ungenauigkeit auch größer ausfallen kann.

Die komplexe Mathematikroutinen bauen für die Implementierung auf die Gleitkommafunktionen in der mathematischen Bibliothek. Diese Funktionen haben unterschiedliche Implementierungen für verschiedene CPU-Architekturen. Die 32-Bit-x86-CRT hat möglicherweise eine andere Implementierung als die 64-Bit x64 CRT. Darüber hinaus haben möglicherweise einige der Funktionen mehrere Implementierungen für eine bestimmte CPU-Architektur. Eine möglichst effiziente Implementierung wird je nach den von der CPU unterstützten Anweisungssets dynamisch zur Laufzeit ausgewählt. In der 32-Bit-x86-CRT haben einige Funktionen eine x87- und eine SSE2-Implementierung. Wenn eine CPU verwendet wird, die SSE2 unterstützt, wird die schnellere SSE2-Implementierung verwendet. Wenn eine CPU verwendet wird, die SSE2 nicht unterstützt, wird die langsamere x87-Implementierung verwendet. Da verschiedene Implementierungen der Funktionen der mathematischen Bibliothek verschiedene CPU-Anweisungen und andere Algorithmen verwenden, um Ergebnisse zu erzielen, unterscheiden sich die Ergebnisse in den verschiedenen CPUs möglicherweise. In den meisten Fällen liegen die Ergebnisse innerhalb +/-1 ULP des korrekt gerundeten Ergebnisses, die tatsächlichen Ergebnisse können jedoch in den CPUs variieren.

## <a name="types-used-in-complex-math"></a>Typen, die in der komplexen Mathematik verwendet werden

Die Microsoft-Implementierung des Headers „compex.h“ definiert diese Typen als Entsprechungen der nativen, komplexen C99-Standardtypen:

|Standardtyp|Microsoft-Typ|
|-|-|
|**float complex** oder **float _Complex**|**_FComplex**|
|**double complex** oder **double _Complex**|**_DComplex**|
|**long double complex** oder **long double _Complex**|**_LComplex**|

Der Header „math.h“ definiert einen separaten Typ, **struct _complex**, der für die [_cabs](../c-runtime-library/reference/cabs.md)-Funktion verwendet wird. Der Typ **struct _complex** wird nicht von den entsprechenden komplexen mathematischen Funktionen [cabs, cabsf, cabsl](../c-runtime-library/reference/cabs-cabsf-cabsl.md) verwendet.

## <a name="complex-constants-and-macros"></a>Komplexe Konstanten und Makros

**I** wird als komplexer **float**-Typ **_FComplex** definiert, der von `{ 0.0f, 1.0f }` initialisiert wird.

## <a name="trigonometric-functions"></a>Trigonometrische Funktionen

|Funktion|description|
|-|-|
|[cacos, cacosf, cacosl](../c-runtime-library/reference/cacos-cacosf-cacosl.md)|Berechnen des komplexen Arcuscosinuswerts einer komplexen Zahl|
|[casin, casinf, casinl](../c-runtime-library/reference/casin-casinf-casinl.md)|Berechnen des komplexen Arcussinuswerts einer komplexen Zahl|
|[catan, catanf, catanl](../c-runtime-library/reference/catan-catanf-catanl.md)|Berechnen des komplexen Arcustangenswerts einer komplexen Zahl|
|[ccos, ccosf, ccosl](../c-runtime-library/reference/ccos-ccosf-ccosl.md)|Berechnen des komplexen Cosinuswerts einer komplexen Zahl|
|[csin, csinf, csinl](../c-runtime-library/reference/csin-csinf-csinl.md)|Berechnen des komplexen Sinuswerts einer komplexen Zahl|
|[ctan, ctanf, ctanl](../c-runtime-library/reference/ctan-ctanf-ctanl.md)|Berechnen des komplexen Tangenswerts einer komplexen Zahl|

## <a name="hyperbolic-functions"></a>Hyperbolische Funktionen

|Funktion|description|
|-|-|
|[cacosh, cacoshf, cacoshl](../c-runtime-library/reference/cacosh-cacoshf-cacoshl.md)|Berechnen des komplexen hyperbolischen Arcuscosinuswerts einer komplexen Zahl|
|[casinh, casinhf, casinhl](../c-runtime-library/reference/casinh-casinhf-casinhl.md)|Berechnen des komplexen hyperbolischen Arcussinuswerts einer komplexen Zahl|
|[catanh, catanhf, catanhl](../c-runtime-library/reference/catanh-catanhf-catanhl.md)|Berechnet den komplexen hyperbolischen Arcustangens einer komplexen Zahl|
|[ccosh, ccoshf, ccoshl](../c-runtime-library/reference/ccosh-ccoshf-ccoshl.md)|Berechnen des komplexen hyperbolischen Cosinuswerts einer komplexen Zahl|
|[csinh, csinhf, csinhl](../c-runtime-library/reference/csinh-csinhf-csinhl.md)|Berechnen des komplexen hyperbolischen Sinuswerts einer komplexen Zahl|
|[ctanh, ctanhf, ctanhl](../c-runtime-library/reference/ctanh-ctanhf-ctanhl.md)|Berechnet den komplexen hyperbolischen Tangens einer komplexen Zahl|

## <a name="exponential-and-logarithmic-functions"></a>Exponentielle und logarithmische Funktionen

|Funktion|description|
|-|-|
|[cexp, cexpf, cexpl](../c-runtime-library/reference/cexp-cexpf-cexpl.md)|Berechnen der Exponentialzahl zur Basis *e* einer komplexen Zahl|
|[clog, clogf, clogl](../c-runtime-library/reference/clog-clogf-clogl.md)|Berechnen des natürlichen Logarithmus zur Basis *e* einer komplexen Zahl|
|[clog10, clog10f, clog10l](../c-runtime-library/reference/clog10-clog10f-clog10l.md)|Berechnen des Logarithmus zur Basis 10 einer komplexen Zahl|

## <a name="power-and-absolute-value-functions"></a>Potenzfunktionen und Absolutwertfunktionen

|Funktion|description|
|-|-|
|[cabs, cabsf, cabsl](../c-runtime-library/reference/cabs-cabsf-cabsl.md)|Berechnen des komplexen Absolutwerts (auch Norm, Modulo oder Größe genannt) für eine komplexe Zahl|
|[cpow, cpowf, cpowl](../c-runtime-library/reference/cpow-cpowf-cpowl.md)|Berechnen der komplexen Potenzfunktion x<sup>y</sup>|
|[csqrt, csqrtf, csqrtl](../c-runtime-library/reference/csqrt-csqrtf-csqrtl.md)|Berechnen der komplexen Quadratwurzel einer komplexen Zahl|

## <a name="manipulation-functions"></a>Bearbeitungsfunktionen

|Funktion|description|
|-|-|
|[_Cbuild, _FCbuild, _LCbuild](../c-runtime-library/reference/cbuild-fcbuild-lcbuild.md)|Erstellen einer komplexen Zahl aus realen und nicht realen Teilen|
|[carg, cargf, cargl](../c-runtime-library/reference/carg-cargf-cargl.md)|Berechnen des Arguments (also des Phasenwinkels) einer komplexen Zahl|
|[cimag, cimagf, cimagl](../c-runtime-library/reference/cimag-cimagf-cimagl.md)|Berechnen des Imaginärteils einer komplexen Zahl|
|[conj, conjf, conjl](../c-runtime-library/reference/conj-conjf-conjl.md)|Berechnen der konjugierten Zahl einer komplexen Zahl|
|[cproj, cprojf, cprojl](../c-runtime-library/reference/cproj-cprojf-cprojl.md)|Berechnen einer Projektion einer komplexen Zahl auf die Riemannsche Zahlenkugel|
|[creal, crealf, creall](../c-runtime-library/reference/creal-crealf-creall.md)|Berechnen des Realteils einer komplexen Zahl|
|[norm, normf, norml](../c-runtime-library/reference/norm-normf-norml1.md)|Berechnen der quadratischen Größe einer komplexen Zahl|

## <a name="operation-functions"></a>Vorgangsfunktionen

Da komplexe Zahlen keinen nativen Typ im Microsoft-Compiler darstellen, werden die arithmetischen Standardoperatoren nicht für komplexe Typen definiert. Der Einfachheit halber werden diese komplexen mathematischen Bibliotheksfunktionen bereitgestellt, um die beschränkte Bearbeitung komplexer Zahlen im Benutzercode zu ermöglichen:

|Funktion|description|
|-|-|
|[_Cmulcc, _FCmulcc, _LCmulcc](../c-runtime-library/reference/cmulcc-fcmulcc-lcmulcc.md)|Addition zweier komplexer Zahlen|
|[_Cmulcr, _FCmulcr, _LCmulcr](../c-runtime-library/reference/cmulcr-fcmulcr-lcmulcr.md)|Multiplikation einer komplexe Zahl und einer Gleitkommazahl|

## <a name="see-also"></a>Siehe auch

[Universelle C-Laufzeitroutinen nach Kategorie](../c-runtime-library/run-time-routines-by-category.md)<br/>
