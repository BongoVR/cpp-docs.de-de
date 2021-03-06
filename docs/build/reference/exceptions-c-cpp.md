---
title: Ausnahmen (C/C++) | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-tools
ms.topic: reference
f1_keywords:
- ERROR_MOD_NOT_FOUND
- vcppException
- ERROR_SEVERITY_ERROR
dev_langs:
- C++
helpviewer_keywords:
- vcppException
- C++ exception handling, delayed loading of DLLs
- delayed loading of DLLs, exceptions
- ERROR_SEVERITY_ERROR exception
- ERROR_MOD_NOT_FOUND exception
ms.assetid: c03be05d-1c39-4f35-84cf-00c9af3bae9a
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 819f9424b2439cc49517afe54d62a8ed4f06d22d
ms.sourcegitcommit: be2a7679c2bd80968204dee03d13ca961eaa31ff
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/03/2018
---
# <a name="exceptions-cc"></a>Ausnahmen (C/C++)
Zwei Ausnahmecodes können ausgelöst werden, wenn Fehler auftreten:  
  
-   Für eine **LoadLibrary** Fehler  
  
-   Für eine **GetProcAddress** Fehler  
  
 Hier sind die Ausnahmeinformationen:  
  
```  
//  
// Exception information  
//  
#define FACILITY_VISUALCPP  ((LONG)0x6d)  
#define VcppException(sev,err)  ((sev) | (FACILITY_VISUALCPP<<16) | err)  
```  
  
 Ausnahmecodes, die ausgelöst werden, die Standardwerte VcppException (ERROR_SEVERITY_ERROR, ERROR_MOD_NOT_FOUND) und VcppException (ERROR_SEVERITY_ERROR, ERROR_PROC_NOT_FOUND)-Werte. Die Ausnahme übergibt einen Zeiger auf eine **DelayLoadInfo** Struktur in der LPDWORD-Wert, der abgerufen werden kann **GetExceptionInformation** in der [EXCEPTION_RECORD](http://msdn.microsoft.com/library/windows/desktop/aa363082) -Struktur, ExceptionInformation [0]-Feld.  
  
 Darüber hinaus die falschen Bits im GrAttrs-Feld festgelegt sind, wird die Ausnahme zusätzlich ausgelöst. Diese Ausnahme ausgelöst wird, zum Verteilungsvorgang, schwerwiegender.  
  
 Finden Sie unter [Struktur- und Konstantendefinitionen](../../build/reference/structure-and-constant-definitions.md) für Weitere Informationen.  
  
## <a name="see-also"></a>Siehe auch  
 [Fehlerbehandlung und Benachrichtigung](../../build/reference/error-handling-and-notification.md)