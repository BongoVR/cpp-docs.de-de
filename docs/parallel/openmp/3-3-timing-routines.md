---
title: 3.3 Routinen zur zeitlichen Steuerung | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-parallel
ms.topic: conceptual
dev_langs:
- C++
ms.assetid: 21060d64-cbe8-4e38-8718-3a68d6a57be3
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: b3b8fc16e34124419362d5989131c2cf66df30b6
ms.sourcegitcommit: 7019081488f68abdd5b2935a3b36e2a5e8c571f8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/07/2018
---
# <a name="33-timing-routines"></a>3.3 Routinen zur zeitlichen Steuerung
Die in diesem Abschnitt beschriebenen Funktionen unterstützen einen portable Realzeit Timer:  
  
-   Die `omp_get_wtime` Funktion gibt die verstrichene wanduhrzeit zurück.  
  
-   Die `omp_get_wtick` Funktion gibt Sekunden zwischen aufeinander folgenden Zeiteinheiten zurück.