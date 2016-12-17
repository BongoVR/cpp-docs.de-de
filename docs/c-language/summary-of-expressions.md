---
title: "Zusammenfassung der Ausdr&#252;cke"
ms.custom: na
ms.date: "12/03/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: na
ms.suite: na
ms.technology: 
  - "devlang-cpp"
ms.tgt_pltfrm: na
ms.topic: "article"
dev_langs: 
  - "C++"
  - "C"
ms.assetid: ed448953-687a-4b57-a1cb-12967bd770ea
caps.latest.revision: 8
caps.handback.revision: "8"
ms.author: "mblome"
manager: "ghogen"
---
# Zusammenfassung der Ausdr&#252;cke
[!INCLUDE[vs2017banner](../assembler/inline/includes/vs2017banner.md)]

*primary\-expression*:  
 *identifier*  
  
 *constant*  
  
 *string\-literal*  
  
 **\(**  *expression*  **\)**  
  
 *expression*:  
 *assignment\-expression*  
  
 *expression*  **,**  *assignment\-expression*  
  
 *constant\-expression*:  
 *conditional\-expression*  
  
 *Bedingter Ausdruck*:  
 *Ausdruck für 'logisches OR'*  
  
 *logical\-OR\-expression*  **?**  *expression*  **:**  *conditional\-expression*  
  
 *assignment\-expression*:  
 *conditional\-expression*  
  
 *unary\-expression assignment\-operator assignment\-expression*  
  
 *postfix\-expression*:  
 *primary\-expression*  
  
 *postfix\-expression*  **\[**  *expression*  **\]**  
  
 *postfix\-expression*  **\(**  *argument\-expression\-list*  opt **\)**  
  
 *postfix\-expression*  **.**  *identifier*  
  
 *postfix\-expression*  **–\>**  *identifier*  
  
 *postfix\-expression*  **\+\+**  
  
 *postfix\-expression*  **––**  
  
 *argument\-expression\-list*:  
 *assignment\-expression*  
  
 *argument\-expression\-list*  **,**  *assignment\-expression*  
  
 *unary\-expression*:  
 *postfix\-expression*  
  
 **\+\+**  *unary\-expression*  
  
 **––**  *unary\-expression*  
  
 *unary\-operator*  
  
 *cast\-expression*  
  
 **sizeof**  *unary\-expression*  
  
 **sizeof \(**  *type\-name*  **\)**  
  
 *unary\-operator*: einer von:  
 **& \* \+ – ~ \!**  
  
 *Umwandlungsausdruck*:  
 *unary\-expression*  
  
 **\(**  *type\-name*  **\)**  *cast\-expression*  
  
 *multiplicative\-expression*:  
 *cast\-expression*  
  
 *multiplicative\-expression*  **\***  *cast\-expression*  
  
 *multiplicative\-expression*  **\/**  *cast\-expression*  
  
 *multiplicative\-expression*  **%**  *cast\-expression*  
  
 *additive\-expression*:  
 *multiplicative\-expression*  
  
 *additive\-expression*  **\+**  *multiplicative\-expression*  
  
 *additive\-expression*  **–**  *multiplicative\-expression*  
  
 *shift\-expression*:  
 *additive\-expression*  
  
 *shift\-expression*  **\<\<**  *additive\-expression*  
  
 *shift\-expression*  **\>\>**  *additive\-expression*  
  
 *relational\-expression*:  
 *shift\-expression*  
  
 *relational\-expression*  **\<**  *shift\-expression*  
  
 *relational\-expression*  **\>**  *shift\-expression relational\-expression*  **\<\=**  *shift\-expression*  
  
 *relational\-expression*  **\>\=**  *shift\-expression*  
  
 *equality\-expression*:  
 *relational\-expression*  
  
 *equality\-expression*  **\=\=**  *relational\-expression*  
  
 *equality\-expression*  **\!\=**  *relational\-expression*  
  
 *AND\-expression*:  
 *equality\-expression*  
  
 *AND\-expression*  **&**  *equality\-expression*  
  
 *exclusive\-OR\-expression*:  
 *AND\-expression*  
  
 *exclusive\-OR\-expression*  **^**  *AND\-expression*  
  
 *inclusive\-OR\-expression*:  
 *exclusive\-OR\-expression*  
  
 *inclusive\-OR\-expression*  **&#124;**   *exclusive\-OR\-expression*  
  
 *logical\-AND\-expression*:  
 *inclusive\-OR\-expression*  
  
 *logical\-AND\-expression*  **&&**  *inclusive\-OR\-expression*  
  
 *logical\-OR\-expression*:  
 *logical\-AND\-expression*  
  
 *logical\-OR\-expression*  **&#124;&#124;**  *logical\-AND\-expression*  
  
## Siehe auch  
 [Phrasenstrukturgrammatik](../c-language/phrase-structure-grammar.md)