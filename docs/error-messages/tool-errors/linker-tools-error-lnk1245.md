---
title: Linkertoolfehler Lnk1245 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- LNK1245
dev_langs:
- C++
helpviewer_keywords:
- LNK1245
ms.assetid: 179c8165-ffbb-44cd-9f24-5250f29577cc
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 47a1c2e5f7bf66946dcc5816d7a20fd485b59b45
ms.sourcegitcommit: 76b7653ae443a2b8eb1186b789f8503609d6453e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/04/2018
---
# <a name="linker-tools-error-lnk1245"></a>Linkertoolfehler LNK1245
Ungültiges Subsystem 'Subsystem' angegeben. / SUBSYSTEM muss WINDOWS, WINDOWSCE oder Konsole sein.  
  
 ["/ CLR"](../../build/reference/clr-common-language-runtime-compilation.md) wurde verwendet, um das Objekt zu kompilieren und eine der folgenden Bedingungen "true" war:  
  
-   Ein benutzerdefinierter Einstiegspunkt wurde definiert ([/Entry](../../build/reference/entry-entry-point-symbol.md)), sodass der Linker kein Subsystem ableiten kann.  
  
-   Ein Wert wurde zum Übergeben der [/Subsystem](../../build/reference/subsystem-specify-subsystem.md) Linkeroption, die nicht für Objekte mit "/ CLR" gültig ist.  
  
 Die Auflösung werden in beiden Fällen geben Sie einen gültigen Wert für die/Subsystem (Linkeroption).