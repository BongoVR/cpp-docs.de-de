---
title: Ausdrücke mit Unäroperatoren | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-language
ms.topic: language-reference
dev_langs:
- C++
helpviewer_keywords:
- expressions [C++], unary operators
- unary operators [C++], expressions with
- expressions [C++], operators
ms.assetid: 1217685b-b85d-4b48-9ff4-d90f56a26c1b
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: 0e1b8db2e02e6ab3e2a70d94ba5f6fe3516e464e
ms.sourcegitcommit: be2a7679c2bd80968204dee03d13ca961eaa31ff
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/03/2018
---
# <a name="expressions-with-unary-operators"></a>Ausdrücke mit unären Operatoren
Unäre Operatoren werden nur auf einen Operanden in einem Ausdruck angewendet. Die unären Operatoren lauten wie folgt:  
  
-   [Der Dereferenzierungsoperator (*)](../cpp/indirection-operator-star.md)  
  
-   [Address-of-Operator (&)](../cpp/address-of-operator-amp.md)  
  
-   [Unärer plus -Operator (+)](../cpp/unary-plus-and-negation-operators-plus-and.md)  
  
-   [Unärer Negationsoperator (-)](../cpp/unary-plus-and-negation-operators-plus-and.md)  
  
-   [Logischer Negationsoperator (!)](../cpp/logical-negation-operator-exclpt.md)  
  
-   [Einerkomplementoperator (~)](../cpp/one-s-complement-operator-tilde.md)  
  
-   [Präfixinkrement-Operator (++)](../cpp/prefix-increment-and-decrement-operators-increment-and-decrement.md)  
  
-   [Präfixdekrement-Operator (-)](../cpp/prefix-increment-and-decrement-operators-increment-and-decrement.md)  
  
-   [Umwandlungsoperator)](../cpp/cast-operator-parens.md)  
  
-   [Sizeof-operator](../cpp/sizeof-operator.md)  
  
-   [__uuidof-operator](../cpp/uuidof-operator.md)  
  
-   [__alignof-operator](../cpp/alignof-operator.md)  
  
-   [New-operator](../cpp/new-operator-cpp.md)  
  
-   [Delete-operator](../cpp/delete-operator-cpp.md)  
  
 Diese Operatoren weisen eine Assoziativität von rechts nach links auf. Unäre Ausdrücke umfassen im Allgemeinen Syntax, die einem Postfix oder primären Ausdruck vorausgeht.  
  
 Folgende Formen von unären Ausdrücken sind möglich:  
  
-   *postfix-expression*  
  
-   `++` *Unary-expression*  
  
-   `--` *Unary-expression*  
  
-   *unärer Operator* *Umwandlungsausdruck*  
  
-   `sizeof` *Unary-expression*  
  
-   `sizeof(` *Typname* `)`  
  
-   `decltype(` *Ausdruck* `)`  
  
-   *Zuweisungsausdruck*  
  
-   *Aufhebung der Zuordnung-Ausdruck*  
  
 Alle *Postfix-Expression* gilt eine *Unary-Expression*, und da jeder primärer Ausdruck ist ein *Postfix-Expression*, ist primäre Ausdrücke berücksichtigt eine *Unary-Expression* auch. Weitere Informationen finden Sie unter [Postfixausdrücke](../cpp/postfix-expressions.md) und [Primärausdrücke](../cpp/primary-expressions.md).  
  
 Ein *unäroperator* besteht aus mindestens einer der folgenden Symbole: `* & + - ! ~`  
  
 Die *Umwandlungsausdruck* ist ein unärer Ausdruck mit einer optionalen Umwandlung so ändern Sie den Typ. Weitere Informationen finden Sie unter [Umwandlungsoperator: ()](../cpp/cast-operator-parens.md).  
  
 Ein *Ausdruck* kann ein beliebiger Ausdruck sein. Weitere Informationen finden Sie unter [Ausdrücke](../cpp/expressions-cpp.md).  
  
 Die *Zuweisungsausdruck* bezieht sich auf die `new` Operator. Die *Aufhebung Ausdruck* bezieht sich auf die `delete` Operator. Weitere Informationen finden Sie unter den Links weiter oben in diesem Thema.  
  
## <a name="see-also"></a>Siehe auch  
 [Ausdruckstypen](../cpp/types-of-expressions.md)