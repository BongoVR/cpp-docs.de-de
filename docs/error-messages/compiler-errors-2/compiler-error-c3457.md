---
title: Compilerfehler C3457 | Microsoft Docs
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- cpp-tools
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- C3457
dev_langs:
- C++
helpviewer_keywords:
- C3457
ms.assetid: 5c1e366a-fa75-4cca-b9a3-86d4ebe4090e
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
ms.openlocfilehash: 0ba6aa69cdf82dc0ee87ff96b0dfa48fddc2e2ab
ms.contentlocale: de-de
ms.lasthandoff: 04/12/2017

---
# <a name="compiler-error-c3457"></a>Compilerfehler C3457
'attribut': Das Attribut unterstützt keine unbenannten Argumente.  
  
 Quellanmerkungsattribute unterstützen im Gegensatz zu benutzerdefinierten CLR-Attributen oder Compilerattributen nur benannte Argumente.  
  
## <a name="example"></a>Beispiel  
 Im folgenden Beispiel wird C3457 generiert:  
  
```  
#include "SourceAnnotations.h"  
[vc_attributes::Post( 1 )] int f();   // C3457  
[vc_attributes::Post( Valid=vc_attributes::Yes )] int f2();   // OK  
```
