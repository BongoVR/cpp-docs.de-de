---
title: return-Anweisung (C++) | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-language
ms.topic: language-reference
f1_keywords:
- return_cpp
dev_langs:
- C++
helpviewer_keywords:
- return keyword [C++], syntax
- return keyword [C++]
ms.assetid: a498903a-056a-4df0-a6cf-72f633a62210
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: 1252e6833dae0f04e1cb148c5703d04d42cee353
ms.sourcegitcommit: be2a7679c2bd80968204dee03d13ca961eaa31ff
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/03/2018
---
# <a name="return-statement-c"></a>return-Anweisung (C++)
Beendet die Ausführung einer Funktion und gibt die Steuerung an die aufrufende Funktion zurück (oder an das Betriebssystem, wenn Sie die Steuerung von der `main`-Funktion übertragen). Die Ausführung wird in der aufrufenden Funktion an dem Punkt fortgesetzt, der dem Aufruf unmittelbar folgt.  
  
## <a name="syntax"></a>Syntax  
  
```  
return [expression];  
```  
  
## <a name="remarks"></a>Hinweise  
 Die Klausel `expression` wird, sofern vorhanden, in den Typ konvertiert, der in der Funktionsdeklaration angegeben wird, als ob eine Initialisierung durchgeführt würde. Eine Konvertierung vom Typ des Ausdrucks in den `return`-Typ der Funktion kann temporäre Objekte erstellen. Weitere Informationen dazu, wie und wann temporäre Objekte erstellt werden, finden Sie unter [temporäre Objekte](../cpp/temporary-objects.md).  
  
 Der Wert der `expression`-Klausel wird an die aufrufende Funktion zurückgegeben. Wenn der Ausdruck ausgelassen wird, wird der Rückgabewert der Funktion nicht definiert. Konstruktoren und Destruktoren und Funktionen des Typs `void`, geben Sie einen Ausdruck in kann nicht der `return` Anweisung. Funktionen aller anderen Typen müssen einen Ausdruck in der `return`-Anweisung angeben.  
  
 Wenn die Ablaufsteuerung den Block verlässt, der die Funktionsdefinition einschließt, ist das Ergebnis das gleiche wie beim Ausführen der `return`-Anweisung ohne einen Ausdruck. Dies ist ungültig bei Funktionen, die mit Rückgabewert deklariert werden.  
  
 Eine Funktion kann eine beliebige Anzahl von `return`-Anweisungen aufweisen.  
  
 Im folgenden Beispiel wird ein Ausdruck mit einer `return`-Anweisung verwendet, um die größte von zwei ganzen Zahlen zu erhalten.  
  
## <a name="example"></a>Beispiel  
  
```  
// return_statement2.cpp  
#include <stdio.h>  
  
int max ( int a, int b )  
{  
   return ( a > b ? a : b );  
}  
  
int main()  
{  
    int nOne = 5;  
    int nTwo = 7;  
  
    printf_s("\n%d is bigger\n", max( nOne, nTwo ));  
}  
```  
  
## <a name="see-also"></a>Siehe auch  
 [Sprunganweisungen](../cpp/jump-statements-cpp.md)   
 [Schlüsselwörter](../cpp/keywords-cpp.md)