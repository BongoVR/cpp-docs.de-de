---
title: 'Aufrufbeispiel: Funktionsprototyp und Aufruf-Funktion | Microsoft Docs'
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-language
ms.topic: language-reference
dev_langs:
- C++
helpviewer_keywords:
- calling conventions, examples [C++]
- examples [C++], calling conventions
ms.assetid: e4275d1f-df2e-4bfc-a162-eb43ec69554a
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: 2fcfda308ed3a5723b32729e7986a7063e9928fd
ms.sourcegitcommit: be2a7679c2bd80968204dee03d13ca961eaa31ff
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/03/2018
---
# <a name="calling-example-function-prototype-and-call"></a>Aufrufbeispiel:Funktionsprototyp und Aufruf
## <a name="microsoft-specific"></a>Microsoft-spezifisch  
 Das folgende Beispiel zeigt die Ergebnisse eines Funktionsaufrufs mit unterschiedlichen Aufrufkonventionen.  
  
 Dieses Beispiel basiert auf dem folgenden Funktionsskelett. Ersetzen Sie `calltype` durch die entsprechende Aufrufkonvention.  
  
```  
void    calltype MyFunc( char c, short s, int i, double f );  
.  
.  
.  
void    MyFunc( char c, short s, int i, double f )  
    {  
    .  
    .  
    .  
    }  
.  
.  
.  
MyFunc ('x', 12, 8192, 2.7183);  
```  
  
 Weitere Informationen finden Sie unter [Ergebnisse aufrufen Beispiel](../cpp/results-of-calling-example.md).  
  
**Ende Microsoft-spezifisch**  
  
## <a name="see-also"></a>Siehe auch  
 [Aufrufkonventionen](../cpp/calling-conventions.md)