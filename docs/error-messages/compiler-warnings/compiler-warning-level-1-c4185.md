---
title: Compilerwarnung (Stufe 1) C4185 | Microsoft Docs
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- devlang-cpp
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- C4185
dev_langs:
- C++
helpviewer_keywords:
- C4185
ms.assetid: 37e7063a-35b1-4e05-ae31-e811dced02b9
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
translationtype: Machine Translation
ms.sourcegitcommit: 0d9cbb01d1ad0f2ea65d59334cb88140ef18fce0
ms.openlocfilehash: 5d7447b13f9e70f8ce91c463f96d2c18815f3080
ms.lasthandoff: 04/12/2017

---
# <a name="compiler-warning-level-1-c4185"></a>Compilerwarnung (Stufe 1) C4185
Das unbekannte #import-Attribut "Attribut" wird ignoriert  
  
 Das Attribut ist kein gültiges `#import`-Attribut. Wird ignoriert.  
  
## <a name="example"></a>Beispiel  
  
```  
// C4185.cpp  
// compile with: /W1 /c  
#import "stdole2.tlb" no_such_attribute   // C4185  
```
