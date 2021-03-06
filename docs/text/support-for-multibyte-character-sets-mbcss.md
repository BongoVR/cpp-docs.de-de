---
title: Unterstützung von Mehrbyte-Zeichensätzen (MBCS) | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-windows
ms.topic: conceptual
f1_keywords:
- _mbcs
dev_langs:
- C++
helpviewer_keywords:
- MBCS [C++], about MBCS
- character sets [C++], multibyte
- multibyte characters [C++]
- MBCS [C++]
ms.assetid: b498733c-a1e1-45e3-8f26-d6da3cb5f2dd
author: ghogen
ms.author: ghogen
ms.workload:
- cplusplus
ms.openlocfilehash: 7b0381b570cbf9e900d44ac075876e63b6be14a8
ms.sourcegitcommit: d55ac596ba8f908f5d91d228dc070dad31cb8360
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/08/2018
---
# <a name="support-for-multibyte-character-sets-mbcss"></a>Unterstützung von Mehrbyte-Zeichensätzen (MBCS)
Mehrbyte-Zeichensätze (MBCS) sind ein älterer Ansatz, mit dem die erforderliche Unterstützung von Zeichensätzen sichergestellt wird, die nicht mit einem Byte pro Zeichen dargestellt werden können, z. B. Japanisch und Chinesisch. Wenn Sie Neuentwicklungen ausführen, sollten Sie Unicode für alle Textzeichenfolgen außer Systemzeichenfolgen verwenden, die nicht für die Endbenutzer sichtbar sind. MBCS ist eine ältere Technologie und wird nicht für Neuentwicklungen empfohlen.  
  
 Bei den gängigsten MBCS-Implementierungen handelt es sich um Doppelbyte-Zeichensätze (DBCS). Visual C++ im Allgemeinen und MFC im Besonderen sind vollständig DBCS-aktiviert.  
  
 Beispiele finden Sie in den MFC-Quellcodedateien.  
  
 Für Plattformen, die in Ländern mit umfangreichen Zeichensätzen verwendet werden, stellt MBCS die beste Alternative zu Unicode dar. MFC unterstützt MBCS durch Verwendung internationalisierbarer Datentypen und C-Laufzeitfunktionen. Es empfiehlt sich, im Code ebenso vorzugehen.  
  
 Unter MBCS werden Zeichen in ein oder zwei Bytes codiert. In zwei Bytes breiten Zeichen zeigt das erste oder führende Byte an, dass es selbst und das nächste Byte als ein einziges Zeichen zu interpretieren sind. Das erste Byte stammt aus einem Bereich mit Codes, die zur Verwendung als führende Bytes reserviert sind. Welche Bytebereiche als führende Bytes verwendet werden können, hängt von der jeweils verwendeten Codepage ab. Von der japanischen Codepage 932 wird z. B. der Bereich von 0 x 81 bis 0 x 9 F für führende Bytes verwendet, während von der koreanischen Codepage 949 hierfür ein anderer Bereich verwendet wird.  
  
 Beachten Sie bei der MBCS-Programmierung alle der nachfolgenden Punkte.  
  
 MBCS-Zeichen in der Umgebung  
 MBCS-Zeichen können in Dateinamen, Verzeichnisnamen und vergleichbaren Zeichenfolgen vorkommen.  
  
 Bearbeitungsvorgänge  
 Bearbeitungsvorgänge in MBCS-Anwendungen sollten auf Zeichen und nicht auf Bytes basieren. Von der Einfügemarke sollte kein Zeichen geteilt werden, mit der NACH RECHTS-TASTE sollte man um ein Zeichen nach rechts gelangen usw. **Löschen Sie** sollte ein Zeichen löschen **Rückgängig** sollte erneut eingefügt werden.  
  
 Zeichenfolgenbehandlung  
 In Anwendungen, die MBCS verwenden, wirft die Behandlung von Zeichenfolgen besondere Probleme auf. Da dieselbe Zeichenfolge breite und normale Zeichen enthalten kann, sind unbedingt Überprüfungen auf führende Bytes vorzusehen.  
  
 Unterstützung der Laufzeitbibliothek  
 Die C-Laufzeitbibliothek und MFC unterstützen die Einzelbyte-, MBCS- und Unicode-Programmierung. Einzelbyte-Zeichenfolgen werden mit verarbeitet die `str` Funktionsreihe zur Laufzeit, MBCS-Zeichenfolgen werden mit den entsprechenden verarbeitet `_mbs` Funktionen und Unicode-Zeichenfolgen werden mit den entsprechenden verarbeitet *wcs* Funktionen. In Implementierungen von Memberfunktionen der MFC-Klasse werden portable Laufzeitfunktionen verwendet, die unter den richtigen Voraussetzungen der normalen `str`-Funktionsreihe, den MBCS-Funktionen oder den Unicode-Funktionen zugeordnet werden, wie unter "MBCS/Unicode-Portabilität" beschrieben.  
  
 MBCS/Unicode-Portabilität  
 Mit der Headerdatei Tchar.h können Sie Einzelbyte-, MBCS- und Unicode-Anwendungen aus denselben Quellen erstellen. TCHAR.h definiert Makros mit dem Präfix *_tcs* , ordnen die `str`, `_mbs`, oder *wcs* Funktionen, die nach Bedarf. Definieren Sie zur Erstellung von MBCS das Symbol **_MBCS**. Definieren Sie zur Erstellung von Unicode das Symbol **_UNICODE**. Standardmäßig **_MBCS** für MFC-Anwendungen definiert ist. Weitere Informationen finden Sie unter [Zuordnungen für generischen Text in Tchar.h](../text/generic-text-mappings-in-tchar-h.md).  
  
> [!NOTE]
>  Verhalten ist nicht definiert, wenn Sie beide definieren **_UNICODE** und **_MBCS**.  
  
 Von den Headerdateien Mbctype.h und Mbstring.h werden MBCS-spezifische Funktionen und Makros definiert, die in bestimmten Fällen benötigt werden. Mit `_ismbblead` können Sie z. B. ermitteln, ob ein bestimmtes Byte einer Zeichenfolge ein führendes Byte ist.  
  
 Codieren Sie international Portieren des Programms mit [Unicode](../text/support-for-unicode.md) oder Mehrbyte-Zeichensätzen (MBCS).  
  
## <a name="what-do-you-want-to-do"></a>Wie möchten Sie vorgehen?  
  
-   [MBCS im Programm aktivieren](../text/international-enabling.md)  
  
-   [Sowohl Unicode-als auch MBCS im Programm aktivieren](../text/internationalization-strategies.md)  
  
-   [Verwenden Sie MBCS, um ein internationales Programm zu erstellen.](../text/mbcs-programming-tips.md)  
  
-   [Anzeigen einer Zusammenfassung zur MBCS-Programmierung](../text/mbcs-programming-tips.md)  
  
-   [Erfahren Sie mehr über Zuordnungen für generischen Text für Byte-breiter Portabilität](../text/generic-text-mappings-in-tchar-h.md)  
  
## <a name="see-also"></a>Siehe auch  
 [Text und Zeichenfolgen](../text/text-and-strings-in-visual-cpp.md)   
 [MBCS-Unterstützung in Visual C++](../text/mbcs-support-in-visual-cpp.md)