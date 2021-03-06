---
title: C-Zuweisungsoperatoren | Microsoft-Dokumentation
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-language
ms.topic: language-reference
dev_langs:
- C++
helpviewer_keywords:
- remainder assignment operator (%=)
- '&= operator'
- bitwise-AND assignment operator
- operators [C], assignment
- operators [C], shift
- ^= operator, assignment operators
- += operator
- '>>= operator'
- '|= operator'
- division assignment operator
- subtraction operator
- right shift operators
- subtraction operator, C assignment operators
- = operator, assignment operators
- '*= operator'
- '>> operator'
- '%= operator'
- assignment operators, C
- = operator
- assignment operators
- assignment conversions
- -= operator
- multiplication assignment operator (*=)
- shift operators, right
- /= operator
- operator >>=, C assignment operators
- <<= operator
ms.assetid: 11688dcb-c941-44e7-a636-3fc98e7dac40
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: 9a13f3b36ae4f5bbd11f170d78d735427882d2ff
ms.sourcegitcommit: be2a7679c2bd80968204dee03d13ca961eaa31ff
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/03/2018
---
# <a name="c-assignment-operators"></a>C-Zuweisungsoperatoren
Eine Zuweisungsvorgang weist den Wert des rechten Operanden dem Speicherort zu, der vom linken Operanden benannt wird. Deshalb muss der linke Operand eines Zuweisungsvorgangs ein änderbarer l-Wert sein. Nach der Zuweisung hat ein Zuweisungsausdruck den Wert des linken Operanden, ist jedoch kein L-Wert.  
  
 **Syntax**  
  
 *assignment-expression*:  
 *conditional-expression*  
  
 *unary-expression assignment-operator assignment-expression*  
  
 *assignment-operator*: eines der folgenden Zeichen:  
 **= \*=** `/=` `%=` `+=` **-= <\<= >>= &=** `^=` `|=`  
  
 Die Zuweisungsoperatoren in C können Werte in einem einzelnen Vorgang transformieren und zuweisen. C stellt die folgenden Zuweisungsoperatoren bereit:  
  
|Operator|Vorgang ausgeführt|  
|--------------|-------------------------|  
|**=**|Einfache Zuweisung|  
|**\*=**|Multiplikationszuweisung|  
|`/=`|Divisionszuweisung|  
|`%=`|Restzuweisung|  
|`+=`|Additionszuweisung|  
|**-=**|Subtraktionszuweisung|  
|**<\<=**|Linksschiebezuweisung|  
|**>>=**|Rechtsschiebezuweisung|  
|**&=**|Bitweise AND-Zuweisung|  
|`^=`|Bitweise exklusive OR-Zuweisung|  
|`&#124;=`|Bitweise inklusive OR-Zuweisung|  
  
 In der Zuweisung wird der Typ des rechten Werts in den Typ des linken Werts konvertiert, und der Wert wird im linken Operanden gespeichert, nachdem die Zuweisung stattgefunden hat. Der linke Operand darf kein Array, keine Funktion und keine Konstante sein. Der bestimmte Konvertierungspfad, der von den beiden Typen abhängt, wird ausführlich in [Typkonvertierungen](../c-language/type-conversions-c.md) erläutert.  
  
## <a name="see-also"></a>Siehe auch  
 [Zuweisungsoperatoren](../cpp/assignment-operators.md)