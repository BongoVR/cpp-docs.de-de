---
title: SAL-Anmerkungen | Microsoft-Dokumentation
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-standard-libraries
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- __z annotation
- ref annotation
- _opt annotation
- __checkreturn annotatioin
- __deref_opt annotation
- deref_opt annotation
- __deref annotation
- __in annotation
- annotations [C++]
- z annotation
- _inout annotation
- __ref annotation
- full annotation
- _in annotation
- _ref annotation
- __out annotation
- _ecount annotation
- SAL annotations
- __opt annotation
- inout annotation
- in annotation
- _CA_SHOULD_CHECK_RETURN
- __bcount annotation
- _full annotation
- _bcount annotation
- deref annotation
- part annotation
- _out annotation
- __nz annotation
- __part annotation
- opt annotation
- __full annotation
- _nz annotation
- _z annotation
- out annotation
- __ecount annotation
- __inout annotation
- SAL annotations, _CA_SHOULD_CHECK_RETURN
- _deref_opt annotation
- _deref annotation
- nz annotation
- _part annotation
- ecount annotation
- bcount annotation
ms.assetid: 81893638-010c-41a0-9cb3-666fe360f3e0
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 2eb935285c8c90c238baf59cd11a1232fa33d895
ms.sourcegitcommit: be2a7679c2bd80968204dee03d13ca961eaa31ff
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/03/2018
---
# <a name="sal-annotations"></a>SAL-Anmerkungen
Wenn Sie die Headerdateien der Bibliothek untersuchen, fallen Ihnen unter Umständen einige ungewöhnliche Anmerkungen auf, z. B. `_In_z` und `_Out_z_cap_(_Size)`. Dies sind Beispiele für die Microsoft-Quellcodeanmerkungssprache (Source-Code Annotation Language, SAL). Mit den darin verfügbaren Anmerkungen kann beschrieben werden, wie eine Funktion ihre Parameter verwendet, z. B. die getroffenen Annahmen und die Garantien für den Abschluss. In der Headerdatei \<sal.h> sind die Anmerkungen definiert.  
  
 Weitere Informationen zur Verwendung von SAL-Anmerkungen in Visual Studio finden Sie unter [Verwenden von SAL-Anmerkungen zum Reduzieren von C/C++-Codefehlern](/visualstudio/code-quality/using-sal-annotations-to-reduce-c-cpp-code-defects).  
  
## <a name="see-also"></a>Siehe auch  
 [CRT-Bibliotheksfunktionen](../c-runtime-library/crt-library-features.md)