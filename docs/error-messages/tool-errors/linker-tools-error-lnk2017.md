---
title: Linkertoolfehler Lnk2017 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- LNK2017
dev_langs:
- C++
helpviewer_keywords:
- LNK2017
ms.assetid: f7c21733-b0fb-4888-a295-9b453ba6ee77
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 095423b5f2d86cef309ed4316ff72d195b11eb26
ms.sourcegitcommit: 76b7653ae443a2b8eb1186b789f8503609d6453e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/04/2018
---
# <a name="linker-tools-error-lnk2017"></a>Linkertoolfehler LNK2017
'Symbol' Verschiebung "Segment" ohne/LARGEADDRESSAWARE: No ungültig.  
  
 Sie versuchen, ein 64-Bit-Abbild mit 32-Bit-Adressen erstellen. Zu diesem Zweck müssen Sie folgende Aktionen ausführen:  
  
-   Verwenden Sie eine feste Adresse an.  
  
-   Beschränken Sie das Image auf 3 GB.  
  
-   Geben Sie [/LARGEADDRESSAWARE: No](../../build/reference/largeaddressaware-handle-large-addresses.md).