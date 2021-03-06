---
title: Linkertoolfehler Lnk1112 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- LNK1112
dev_langs:
- C++
helpviewer_keywords:
- LNK1112
ms.assetid: 425793d8-37e6-4072-9b6e-c3d4e9c12562
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: fd4af160607d75f036d25d21f5a95e753bddb3be
ms.sourcegitcommit: 76b7653ae443a2b8eb1186b789f8503609d6453e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/04/2018
---
# <a name="linker-tools-error-lnk1112"></a>Linkertoolfehler LNK1112
Modul-Computertyp „Typ1“ steht in Konflikt mit dem Zielcomputertyp „Typ2“.  
  
 Die als Eingabe festgelegten Objektdateien wurden für unterschiedliche Computertypen kompiliert.  
  
 Wenn Sie z. B. versuchen, eine mit **/clr** und eine mit **/clr:pure** kompilierte Objektdatei (Computertyp CEE) zu verknüpfen, generiert der Linker den Fehler LNK1112.  
  
 Wenn Sie ein Modul mit dem [!INCLUDE[vcprx64](../../assembler/inline/includes/vcprx64_md.md)] -Compiler und ein anderes Modul mit dem x86-Compiler erstellen und dann versuchen, diese zu verknüpfen, wird vom Linker gleichsam der Fehler LNK1112 generiert.  
  
 Eine mögliche Ursache für diesen Fehler ist, dass Sie eine 64-Bit-Anwendung entwickeln, aber keiner der 64-Bit-Compiler von Visual C++ installiert ist. In diesem Fall stehen die 64-Bit-Konfigurationen nicht zur Verfügung. Um dieses Problem zu beheben, führen Sie das Installationsprogramm für Visual Studio aus und installieren die fehlenden Komponenten von C++.  
  
 Dieser Fehler kann auch auftreten, wenn Sie die **aktive Projektmappenkonfiguration** im **Konfigurations-Manager** ändern und anschließend versuchen, das Projekt zu erstellen, bevor Sie die Zwischenprojektdateien gelöscht haben. Wählen Sie zum Beheben dieses Fehlers **Projektmappe neu erstellen** aus dem Menü **Erstellen** aus. Sie können auch **Projektmappe bereinigen** aus dem Menü **Erstellen** auswählen und die Projektmappe anschließend erstellen.  
  
## <a name="see-also"></a>Siehe auch  
 [Fehler und Warnungen der Linkertools](../../error-messages/tool-errors/linker-tools-errors-and-warnings.md)