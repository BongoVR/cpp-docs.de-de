---
title: Mathematischer Fehler M6111 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- M6111
dev_langs:
- C++
helpviewer_keywords:
- M6111
ms.assetid: c0fc13f8-33c8-4e3f-a440-126cc623441b
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 3b03937ed442b169b960d573b44c0eb6ebca9660
ms.sourcegitcommit: 76b7653ae443a2b8eb1186b789f8503609d6453e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/04/2018
---
# <a name="math-error-m6111"></a>Mathematischer Fehler M6111
Stapelunterlauf  
  
 Ein Gleitkomma Vorgang verursachte einen Stapelunterlauf 8087/287/387-Coprozessor oder -Emulator.  
  
 Dieser Fehler wird häufig durch einen Aufruf verursacht eine `long double` Funktion, die keinen Wert zurückgibt. Die folgenden generiert z. B. diesen Fehler bei der Kompilierung und Ausführung:  
  
```  
long double ld() {};  
main ()  
{  
  ld();  
}  
```  
  
 Programm mit Exitcode 139 beendet wird.