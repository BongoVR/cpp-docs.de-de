---
title: Operatoren für den Memberzugriff:. "und" -&gt; | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-language
ms.topic: language-reference
f1_keywords:
- .
- ->
dev_langs:
- C++
helpviewer_keywords:
- member access, expressions
- operators [C++], member access
- dot operator (.)
- -> operator
- member access, operators
- postfix operators [C++]
- . operator
- member access
ms.assetid: f8fc3df9-d728-40c5-b384-276927f5f1b3
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: 2958291551d081b4284c6683d62f6dd5de06f70d
ms.sourcegitcommit: be2a7679c2bd80968204dee03d13ca961eaa31ff
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/03/2018
---
# <a name="member-access-operators--and--gt"></a>Operatoren für den Memberzugriff:. "und" -&gt;
## <a name="syntax"></a>Syntax  
  
```  
postfix-expression . name  
postfix-expression -> name  
```  
  
## <a name="remarks"></a>Hinweise  
 Die Operatoren für den Memberzugriff **.** und **->** werden verwendet, um auf Member von Strukturen, Unions und Klassen verweisen. Memberzugriffsausdrücke haben den Wert und Typ des ausgewählten Members.  
  
 Es gibt zwei Arten von Memberzugriffsausdrücken:  
  
1.  In der ersten Form stellt *postfixausdruck* stellt einen Wert von der Struktur, Klasse oder union-Typ und *Namen* Namen eines Members der angegebenen Struktur, Union oder Klasse. Der Wert des Vorgangs ist der *Namen* und ist ein l-Wert, wenn *postfixausdruck* ist ein l-Wert.  
  
2.  In der zweiten Form *postfixausdruck* stellt einen Zeiger auf eine Struktur, Union oder Klasse, und *Namen* Namen eines Members der angegebenen Struktur, Union oder Klasse. Der Wert ist der *Namen* und ist ein l-Wert. Die **->** Operator dereferenziert den Zeiger. Daher sind die Begriffe * e ***->** `member` und **(\****e***)**.`member` (, in denen *e* stellt einen Zeiger) identische Ergebnisse ergeben (Ausnahme: Wenn die Operatoren **->** oder **\*** überladen werden).  
  
## <a name="example"></a>Beispiel  
 Im folgenden Beispiel werden beide Formen des Memberzugriffsoperators dargestellt.  
  
```  
// expre_Selection_Operator.cpp  
// compile with: /EHsc  
#include <iostream>  
using namespace std;  
  
struct Date {  
   Date(int i, int j, int k) : day(i), month(j), year(k){}  
   int month;  
   int day;  
   int year;  
};  
  
int main() {  
   Date mydate(1,1,1900);  
   mydate.month = 2;     
   cout  << mydate.month << "/" << mydate.day  
         << "/" << mydate.year << endl;  
  
   Date *mydate2 = new Date(1,1,2000);  
   mydate2->month = 2;  
   cout  << mydate2->month << "/" << mydate2->day  
         << "/" << mydate2->year << endl;  
   delete mydate2;  
}  
```  
  
```Output  
2/1/1900  
2/1/2000  
```  
  
## <a name="see-also"></a>Siehe auch  
 [Postfixausdrücke](../cpp/postfix-expressions.md)   
 [Integrierte C++-Operatoren, Rangfolge und Assoziativität](../cpp/cpp-built-in-operators-precedence-and-associativity.md)   
 [Klassen und Strukturen](../cpp/classes-and-structs-cpp.md)   
 [Struktur- und Unionmember](../c-language/structure-and-union-members.md)