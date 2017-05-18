---
title: Compilerfehler C2075 | Microsoft Docs
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- cpp-tools
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- C2075
dev_langs:
- C++
helpviewer_keywords:
- C2075
ms.assetid: 8b1865d2-540b-4117-b982-e7a58a0b6cf7
caps.latest.revision: 7
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
ms.openlocfilehash: 515dc4e2c72df372a684076809e57bc6d164798a
ms.contentlocale: de-de
ms.lasthandoff: 04/12/2017

---
# <a name="compiler-error-c2075"></a>Compilerfehler C2075
"Bezeichner": für die Initialisierung eines Arrays sind geschweifte Klammern erforderlich  
  
 Der angegebene Arrayinitialisierer war nicht in geschweifte Klammern eingeschlossen.  
  
 Im folgenden Beispiel wird C2075 generiert:  
  
```  
// C2075.c  
int main() {  
   int i[] = 1, 2, 3 };   // C2075  
}  
```  
  
 Mögliche Lösung:  
  
```  
// C2075b.c  
int main() {  
   int j[] = { 1, 2, 3 };  
}  
```
