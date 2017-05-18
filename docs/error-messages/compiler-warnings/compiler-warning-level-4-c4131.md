---
title: Compilerwarnung (Stufe 4) C4131 | Microsoft Docs
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- cpp-tools
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- C4131
dev_langs:
- C++
helpviewer_keywords:
- C4131
ms.assetid: 7903b3e1-454f-4be2-aa9b-230992f96a2d
caps.latest.revision: 6
author: corob-msft
ms.author: corob
manager: ghogen
translation.priority.ht:
- de-de
- es-es
- fr-fr
- it-it
- ja-jp
- ko-kr
- ru-ru
- zh-cn
- zh-tw
translation.priority.mt:
- cs-cz
- pl-pl
- pt-br
- tr-tr
ms.translationtype: Machine Translation
ms.sourcegitcommit: 0d9cbb01d1ad0f2ea65d59334cb88140ef18fce0
ms.openlocfilehash: abe0127ba906fc52adf66b32e8530d60c9a08b2b
ms.contentlocale: de-de
ms.lasthandoff: 04/12/2017

---
# <a name="compiler-warning-level-4-c4131"></a>Compilerwarnung (Stufe 4) C4131
"function": Verwendet Deklarator für altes Format  
  
 Die angegebene Funktionsdeklaration weist keine Prototypform auf.  
  
 Funktionsdeklarationen im alten Format sollten in die Prototypform konvertiert werden.  
  
 Im folgenden Beispiel wird eine Funktionsdeklaration im alten Stil veranschaulicht:  
  
```  
// C4131.c  
// compile with: /W4 /c  
void addrec( name, id ) // C4131 expected  
char *name;  
int id;  
{ }  
```  
  
 Im folgenden Beispiel wird eine Prototypform veranschaulicht:  
  
```  
void addrec( char *name, int id )  
{ }  
```
