---
title: Zusammenfassung der Anweisungen | Microsoft-Dokumentation
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-language
ms.topic: language-reference
dev_langs:
- C++
ms.assetid: ce45d2fe-ec0e-459f-afb1-80ab6a7f0239
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: 4b2d3b27149344151f891e23c39bbecb8e4c1102
ms.sourcegitcommit: be2a7679c2bd80968204dee03d13ca961eaa31ff
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/03/2018
---
# <a name="summary-of-statements"></a>Zusammenfassung der Anweisungen
*statement*:  
 *labeled-statement*  
  
 *compound-statement*  
  
 *expression-statement*  
  
 *selection-statement*  
  
 *iteration-statement*  
  
 *jump-statement*  
  
 *try-except-statement* /* Microsoft-spezifisch \*/  
  
 *try-finally-statement* /* Microsoft-spezifisch \*/  
  
 *jump-statement*:  
 **goto**  *identifier*  **;**  
  
 **continue ;**  
  
 **break ;**  
  
 **return**  *expression*opt **;**  
  
 *compound-statement*:  
 **{**  *declaration-list*opt*statement-list*opt **}**  
  
 *declaration-list*:  
 *declaration*  
  
 *declaration-list-Deklaration*  
  
 *statement-list*:  
 *statement*  
  
 *statement-list-Anweisung*  
  
 *expression-statement*:  
 *expression*opt **;**  
  
 *iteration-statement*:  
 **while (**  *expression*  **)**  *statement*  
  
 **do**  *statement*  **while (**  *expression*  **) ;**  
  
 **for (**  *expression*opt **;** *expression*opt **;** *expression*opt **)** *statement*  
  
 *selection-statement*:  
 **if (**  *expression*  **)**  *statement*  
  
 **if (**  *expression*  **)**  *statement*  **else**  *statement*  
  
 **switch (**  *expression*  **)**  *statement*  
  
 *labeled-statement*:  
 *identifier*  **:**  *statement*  
  
 **case** *constant-expression* **:** *statement*  
  
 **default :** *statement*  
  
 *try-except-statement*:   /\* Microsoft-spezifisch \*/  
 **__try** *compound-statement*  
  
 **__except (** *expression* **)** *compound-statement*  
  
 *try-finally-statement*:   /\* Microsoft-spezifisch \*/  
 **__try** *compound-statement*  
  
 **__finally**  *compound-statement*  
  
## <a name="see-also"></a>Siehe auch  
 [Phrasenstrukturgrammatik](../c-language/phrase-structure-grammar.md)