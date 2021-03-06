---
title: Zuweisung | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-language
ms.topic: language-reference
dev_langs:
- C++
helpviewer_keywords:
- operators [C++], assignment
- assignment operators [C++], overloaded
ms.assetid: d87e4f89-f8f5-42c1-9d3c-184bca9d0e15
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: 66fd08215c3849bf487578b28b1824afbec14c52
ms.sourcegitcommit: be2a7679c2bd80968204dee03d13ca961eaa31ff
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/03/2018
---
# <a name="assignment"></a>Zuweisung
Der Zuweisungsoperator (**=**) ist strenggenommen ein binärer Operator. Seine Deklaration ist mit jedem anderen binären Operator identisch, mit den folgenden Ausnahmen:  
  
-   Es muss eine nicht statische Memberfunktion sein. Kein `operator=` kann als Nichtmemberfunktion deklariert werden.  
  
-   Es wird nicht von abgeleiteten Klassen geerbt.  
  
-   Eine `operator=`-Standardfunktion kann vom Compiler für Klassentypen generiert werden, falls nicht vorhanden. (Weitere Informationen zu `operator=` -Funktionen finden Sie unter [Memberwise Assignment and Initialization](http://msdn.microsoft.com/en-us/94048213-8b49-4416-8069-b1b7a6f271f9).)  
  
 Das folgende Beispiel veranschaulicht, wie Sie einen Zuweisungsoperator deklarieren:  
  
```  
// assignment.cpp  
class Point  
{  
public:  
   Point &operator=( Point & );  // Right side is the argument.  
   int _x, _y;  
};  
  
// Define assignment operator.  
Point &Point::operator=( Point &ptRHS )  
{  
   _x = ptRHS._x;  
   _y = ptRHS._y;  
  
   return *this;  // Assignment operator returns left side.  
}  
  
int main()  
{  
}  
```  
  
 Beachten Sie, dass das angegebene Argument die rechte Seite des Ausdrucks ist. Der Operator gibt das Objekt zurück, um das Verhalten des Zuweisungsoperators beizubehalten, der den Wert des linken Rands zurückgibt, nachdem die Zuweisung abgeschlossen ist. So können Anweisungen geschrieben werden wie:  
  
```  
pt1 = pt2 = pt3;  
```  
  
## <a name="see-also"></a>Siehe auch  
 [Operatorüberladung](../cpp/operator-overloading.md)