---
title: C++-Konstante Ausdrücke | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-language
ms.topic: language-reference
dev_langs:
- C++
helpviewer_keywords:
- constant expressions, syntax
- constant expressions
- expressions [C++], constant
ms.assetid: b07245a5-4c21-4589-b503-e6ffd631996f
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: d71427c7176d8448d861c6dd7602b6bc91941737
ms.sourcegitcommit: be2a7679c2bd80968204dee03d13ca961eaa31ff
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/03/2018
---
# <a name="c-constant-expressions"></a>C++-Ausdrücke (konstant)
Ein *konstant* Wert wird nicht verändert. C++ bietet zwei Schlüsselwörter, mit denen Sie den Zweck eines Objekts angeben können, der nicht dazu gedacht ist, geändert zu werden, und diese Absicht erzwingen soll.  
  
 C++ erfordert konstante Ausdrücke – Ausdrücke, die als Konstante ausgewertet werden – für Deklarationen von:  
  
-   Arraygrenzen  
  
-   Selektoren in case-Anweisungen  
  
-   Bitfeldlängenangabe  
  
-   Enumerationsinitialisierer  
  
 Die einzigen Operanden, die in konstanten Ausdrücken zulässig sind, lauten:  
  
-   Literale  
  
-   Enumerationskonstanten  
  
-   Werte, die als Konstanten deklariert sind und mit konstanten Ausdrücken initialisiert werden.  
  
-   `sizeof`-Ausdrücke  
  
 Konstanten, die keine Ganzzahlen sind, müssen (entweder explizit oder implizit) in ganzzahlige Typen konvertiert werden, um in einem konstanten Ausdruck zulässig zu sein. Daher ist der folgende Code gültig:  
  
```  
const double Size = 11.0;  
char chArray[(int)Size];  
```  
  
 Explizite Konvertierungen in ganzzahlige Typen sind in konstanten Ausdrücken zulässig; alle anderen Typen und abgeleiteten Typen sind nicht zulässig, sofern sie nicht als Operanden für den `sizeof`-Operator verwendet werden.  
  
 Der Kommaoperator sowie Zuweisungsoperatoren können nicht in konstanten Ausdrücken verwendet werden.  
  
## <a name="see-also"></a>Siehe auch  
 [Ausdruckstypen](../cpp/types-of-expressions.md)