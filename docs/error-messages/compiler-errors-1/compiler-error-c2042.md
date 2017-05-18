---
title: Compilerfehler C2042 | Microsoft Docs
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- cpp-tools
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- C2042
dev_langs:
- C++
helpviewer_keywords:
- C2042
ms.assetid: e111788f-41ce-405a-9824-a4c1c26059e6
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
ms.openlocfilehash: 6d8666d0ede87237ab890d36767c6581ca9a0a35
ms.contentlocale: de-de
ms.lasthandoff: 04/12/2017

---
# <a name="compiler-error-c2042"></a>Compilerfehler C2042
Die Schlüsselwörter "signed/unsigned" schließen sich gegenseitig aus  
  
 Die Schlüsselwörter `signed` und `unsigned` werden innerhalb der gleichen Deklaration verwendet.  
  
 Im folgenden Beispiel wird C2042 generiert:  
  
```  
// C2042.cpp  
unsigned signed int i;   // C2042  
```  
  
 Mögliche Lösung:  
  
```  
// C2042b.cpp  
// compile with: /c  
unsigned int i;  
signed int ii;  
```
