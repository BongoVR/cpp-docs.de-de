---
title: Compilerfehler C2161 | Microsoft Docs
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- cpp-tools
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- C2161
dev_langs:
- C++
helpviewer_keywords:
- C2161
ms.assetid: d6798821-13bb-4e60-924f-85f7bf955387
caps.latest.revision: 8
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
ms.openlocfilehash: 06b21ad039a8ec8eab076f3bfaaa7aa6ee1df3b7
ms.contentlocale: de-de
ms.lasthandoff: 04/12/2017

---
# <a name="compiler-error-c2161"></a>Compilerfehler C2161
"##" kann nicht am Ende einer Makrodefinition stehen  
  
 Eine Makrodefinition endete mit einem tokeneinfügenden Operator (##).  
  
 Im folgenden Beispiel wird C2161 generiert:  
  
```  
// C2161.cpp  
// compile with: /c  
#define mac(a,b) a   // OK  
#define mac(a,b) a##   // C2161  
```
