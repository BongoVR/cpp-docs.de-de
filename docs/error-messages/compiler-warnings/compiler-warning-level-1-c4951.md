---
title: Compilerwarnung (Stufe 1) C4951 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C4951
dev_langs:
- C++
helpviewer_keywords:
- C4951
ms.assetid: 669d8bb7-5efa-4ba9-99db-4e65addbf054
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: c3ebf012338bdf6b90cc943e754056335c6751a4
ms.sourcegitcommit: 76b7653ae443a2b8eb1186b789f8503609d6453e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/04/2018
---
# <a name="compiler-warning-level-1-c4951"></a>Compilerwarnung (Stufe 1) C4951
"Funktion" wurde bearbeitet, seit die Profildaten erfasst wurden. Die Funktionsprofildaten werden nicht verwendet.  
  
 Eine Funktion wurde in einem Eingabemodul für [/LTCG:PGUPDATE](../../build/reference/ltcg-link-time-code-generation.md)bearbeitet, sodass die Profildaten jetzt ungültig sind. Das Eingabemodul wurde nach **/LTCG:PGINSTRUMENT** neu kompiliert und verfügt über eine Funktion (***Funktion***) mit einer anderen Ablaufsteuerung als der, die zum Zeitpunkt des **/LTCG:PGINSTRUMENT** -Vorgangs im Modul enthalten war.  
  
 Diese Warnung dient nur zu Informationszwecken. Um diese Warnung zu beheben, führen Sie **/LTCG:PGINSTRUMENT**aus, wiederholen alle Testläufe und führen **/LTCG:PGOPTIMIZE**aus.  
  
 Bei Verwendung von **/LTCG:PGOPTIMIZE** würde diese Warnung durch einen Fehler ersetzt.