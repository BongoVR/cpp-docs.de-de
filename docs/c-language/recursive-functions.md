---
title: Rekursive Funktionen | Microsoft-Dokumentation
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-language
ms.topic: language-reference
dev_langs:
- C++
helpviewer_keywords:
- functions [C], recursive
- function calls, recursive
- functions [C], calling recursively
- recursive function calls
ms.assetid: 59739040-3081-4006-abbc-9d8423992bce
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: 90a6334ae0c00378f5162274dab499f3cb10bc3e
ms.sourcegitcommit: be2a7679c2bd80968204dee03d13ca961eaa31ff
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/03/2018
---
# <a name="recursive-functions"></a>Rekursive Funktionen
Jede Funktion in einem C-Programm kann rekursiv aufgerufen werden, d. h. sie kann sich selbst aufrufen. Die Anzahl von rekursiven Aufrufen ist auf die Größe des Stapels beschränkt. Weitere Informationen zu Linkeroptionen, die die Stapelgröße festlegen, erhalten Sie unter [/STACK (Stapelreservierungen)](../build/reference/stack-stack-allocations.md). Jedes Mal, wenn die Funktion aufgerufen wird, wird neuer Speicherplatz für die Parameter und für die Variablen **auto** und **register** zugeordnet, sodass die Werte in den vorangegangenen, unfertigen Aufrufen nicht überschrieben werden. Auf Parameter kann nur direkt durch die Instanz der Funktion zugegriffen werden, in der sie erstellt werden. Auf vorherige Parameter kann nicht direkt durch nachfolgende Instanzen der Funktion zugegriffen werden.  
  
 Beachten Sie, dass die Variablen, die mit **static**-Speicher deklariert werden, keinen neuen Speicher mit jedem rekursiven Aufruf erfordern. Der Speicher bleibt so lange erhalten wie das Programm besteht. Jeder Verweis auf eine solche Variable greift auf denselben Speicherbereich zu.  
  
## <a name="example"></a>Beispiel  
 In diesem Beispiel werden rekursive Aufrufe veranschaulicht:  
  
```  
int factorial( int num );      /* Function prototype */  
  
int main()  
{  
    int result, number;  
    .  
    .  
    .  
    result = factorial( number );  
}  
  
int factorial( int num )      /* Function definition */  
{  
    .  
    .  
    .  
    if ( ( num > 0 ) || ( num <= 10 ) )  
        return( num * factorial( num - 1 ) );  
}  
  
```  
  
## <a name="see-also"></a>Siehe auch  
 [Funktionsaufrufe](../c-language/function-calls.md)