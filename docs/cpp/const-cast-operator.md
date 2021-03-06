---
title: Const_cast-Operator | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-language
ms.topic: language-reference
f1_keywords:
- const_cast_cpp
dev_langs:
- C++
helpviewer_keywords:
- const_cast keyword [C++]
ms.assetid: 4d8bb203-ef33-4a10-9f9f-c64d4fbc1687
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: ed5daf503024b2c3f843faeeaedbd9ec9bf64b7c
ms.sourcegitcommit: be2a7679c2bd80968204dee03d13ca961eaa31ff
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/03/2018
---
# <a name="constcast-operator"></a>const_cast-Operator
Entfernt die **const**, `volatile`, und **__unaligned** -Attribute aus einer Klasse.  
  
## <a name="syntax"></a>Syntax  
  
```  
  
const_cast <   
type-id  
 > (   
expression  
 )  
  
```  
  
## <a name="remarks"></a>Hinweise  
 Ein Zeiger auf einen beliebigen Objekttyp oder ein Zeiger auf einen Datenmember explizit in einen Typ, der identisch ist konvertiert werden kann die **const**, `volatile`, und **__unaligned** Qualifizierer. Für Zeiger und Verweise verweist das Ergebnis auf das ursprüngliche Objekt. Für Zeiger auf Datenmember, verweist das Ergebnis auf denselben Member wie der ursprüngliche (uncast) Zeiger auf Datenmember. Je nach Typ des verweisenden Objekts, führt ein Schreibvorgang durch den resultierenden Zeiger, Verweis oder Zeiger auf Datenmember möglicherweise zu nicht definiertem Verhalten.  
  
 Sie können den Operator `const_cast` nicht verwenden, um den konstanten Status einer konstanten Variable direkt zu überschreiben.  
  
 Der `const_cast`-Operator konvertiert einen NULL-Zeigerwert in den NULL-Zeigerwert des Zieltyps.  
  
## <a name="example"></a>Beispiel  
  
```  
// expre_const_cast_Operator.cpp  
// compile with: /EHsc  
#include <iostream>  
  
using namespace std;  
class CCTest {  
public:  
   void setNumber( int );  
   void printNumber() const;  
private:  
   int number;  
};  
  
void CCTest::setNumber( int num ) { number = num; }  
  
void CCTest::printNumber() const {  
   cout << "\nBefore: " << number;  
   const_cast< CCTest * >( this )->number--;  
   cout << "\nAfter: " << number;  
}  
  
int main() {  
   CCTest X;  
   X.setNumber( 8 );  
   X.printNumber();  
}  
```  
  
 In der Zeile, die `const_cast` enthält, lautet der Datentyp des `this` Zeigers `const CCTest *`. Der Operator `const_cast` ändert den Datentyp des `this`-Zeigers in `CCTest *` und ermöglicht die Änderung des Members `number`. Die Umwandlung erfolgt nur für den Rest der Anweisung, in der er angezeigt wird.  
  
## <a name="see-also"></a>Siehe auch  
 [Umwandlungsoperatoren](../cpp/casting-operators.md)   
 [Schlüsselwörter](../cpp/keywords-cpp.md)