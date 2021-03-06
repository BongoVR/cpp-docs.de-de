---
title: Unicode und MBCS | Microsoft Docs
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
- MBCS [C++], Unicode
- MFC [C++], character sets
- character sets [C++], multibyte
- run-time libraries [C++], language portability
- character sets [C++], Unicode
- Unicode [C++], MFC and C run-time functions
- multibyte characters [C++]
- runtime [C++], language portability
ms.assetid: 677baec6-71b4-4579-94df-64f18bc117c4
author: ghogen
ms.author: ghogen
ms.workload:
- cplusplus
ms.openlocfilehash: 2e10c07e11cbe940b5f7cfee460ddd33f6f5ff1f
ms.sourcegitcommit: d55ac596ba8f908f5d91d228dc070dad31cb8360
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/08/2018
---
# <a name="unicode-and-mbcs"></a>Unicode und MBCS
Die MFC-Bibliothek (Microsoft Foundation Classes), die C-Laufzeitbibliothek für Visual C++ und die Visual C++-Entwicklungsumgebung unterstützen Sie bei der internationalen Programmierung. Sie bieten:  
  
-   Unterstützung für den Unicode-Standard unter Windows. Unicode ist der aktuelle Standard und sollte möglichst verwendet werden.  
  
     Unicode ist ein 16-Bit-Verfahren für die Zeichencodierung, in dem die Zeichensätze aller Sprachen codiert werden können. Alle ASCII-Zeichen sind in Unicode als erweiterte Zeichen enthalten.  
  
-   Unterstützung für den Doppelbyte-Zeichensatz (Double-Byte Character Set, DBCS), einer Variante des Mehrbyte-Zeichensatzes (MBCS) auf allen Plattformen  
  
     DBCS-Zeichen bestehen aus einem oder zwei Bytes. Bestimmte Bytebereiche sind zur Verwendung als führende Bytes reserviert. Ein führendes Byte zeigt an, dass es selbst und das nächste Byte (das nachfolgende Byte) ein einziges, aus zwei Bytes bestehendes Zeichen darstellen. Es ist wichtig, stets zu wissen, bei welchen Bytes es sich um führende Bytes handelt. In einem bestimmten Mehrbyte-Zeichensatz liegen die führenden Bytes ebenso wie die nachfolgenden Bytes innerhalb eines bestimmten Bereichs. Wenn sich diese Bereiche überschneiden, muss unter Umständen anhand des Kontexts ermittelt werden, ob ein bestimmtes Byte als führendes oder als nachfolgendes Byte verwendet wird.  
  
-   Unterstützung für Tools, die die MBCS-Programmierung von Anwendungen für internationale Märkte vereinfachen  
  
     Bei der Ausführung unter einer MBCS-aktivierten Version des Betriebssystems Windows 2000 ist das Visual C++-Entwicklungssystem, einschließlich des integrierten Quellcode-Editors, Debuggers und der Befehlszeilentools, vollständig MBCS-aktiviert. Weitere Informationen finden Sie unter [MBCS-Unterstützung in Visual C++](../text/mbcs-support-in-visual-cpp.md).  
  
> [!NOTE]
>  In der vorliegenden Dokumentation umschreibt der Begriff MBCS jede Nicht-Unicode-Unterstützung für Mehrbytezeichen. In Visual C++ ist MBCS gleichbedeutend mit DBCS. Zeichensätze, die "breiter" als zwei Byte sind, werden nicht unterstützt.  
  
 Der ASCII-Zeichensatz ist definitionsgemäß eine Teilmenge jedes Mehrbyte-Zeichensatzes. In vielen Multibyte-Zeichensätzen sind die Zeichen im Bereich von 0x00 bis 0x7F mit den gleichwertigen Zeichen des ASCII-Zeichensatzes identisch. Z. B. in ASCII- und MBCS-Zeichenfolgen, das 1-Byte- **NULL** Zeichen ('\0') wurde der Wert 0 x 00 und gibt an, das abschließende Nullzeichen.  
  
## <a name="see-also"></a>Siehe auch  
 [Text und Zeichenfolgen](../text/text-and-strings-in-visual-cpp.md)   
 [Aktivierung der Internationalen Programmierung](../text/international-enabling.md)