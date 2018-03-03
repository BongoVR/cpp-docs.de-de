---
title: _acmdln, _tcmdln, _wcmdln | Microsoft-Dokumentation
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- cpp-standard-libraries
ms.tgt_pltfrm: 
ms.topic: article
apiname:
- _wcmdln
- _acmdln
apilocation:
- msvcrt.dll
apitype: DLLExport
f1_keywords:
- _acmdln
- acmdln
- _wcmdln
- wcmdln
- _tcmdln
- tcmdln
dev_langs:
- C++
helpviewer_keywords:
- _wcmdln global variable
- wcmdln global variable
- _acmdln global variable
- _tcmdln global variable
- tcmdln global variable
- acmdln global variable
ms.assetid: 4fc0a6a0-3f93-420a-a19f-5276061ba539
caps.latest.revision: 
author: corob-msft
ms.author: corob
manager: ghogen
ms.workload:
- cplusplus
ms.openlocfilehash: 8250822adb801365fca826f33899a7ae3d1d06a4
ms.sourcegitcommit: 8fa8fdf0fbb4f57950f1e8f4f9b81b4d39ec7d7a
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/21/2017
---
# <a name="acmdln-tcmdln-wcmdln"></a>_acmdln, _tcmdln, _wcmdln
Interne globale CRT-Variable. Die Befehlszeile.  
  
## <a name="syntax"></a>Syntax  
  
```  
char * _acmdln;  
wchar_t * _wcmdln;  
  
#ifdef WPRFLAG  
   #define _tcmdln _wcmdln  
#else  
   #define _tcmdln _acmdln  
```  
  
## <a name="remarks"></a>Hinweise  
 Diese internen CRT-Variablen speichern die vollständige Befehlszeile. Sie sind in den exportierten Symbolen für die CRT verfügbar, aber nicht zur Verwendung in Ihrem Code vorgesehen. `_acmdln` speichert die Daten als Zeichenfolge. `_wcmdln` speichert die Daten als Breitzeichen-Zeichenfolge. `_tcmdln` kann als `_acmdln` oder `_wcmdln` definiert werden, abhängig davon, was angemessen ist.  
  
## <a name="see-also"></a>Siehe auch  
 [Globale Variablen](../c-runtime-library/global-variables.md)