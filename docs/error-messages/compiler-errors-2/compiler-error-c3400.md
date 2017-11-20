---
title: Compilerfehler C3400 | Microsoft Docs
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-tools
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords: C3400
dev_langs: C++
helpviewer_keywords: C3400
ms.assetid: d44169a8-73b6-4766-b406-b3a6c93f2a4d
caps.latest.revision: "3"
author: corob-msft
ms.author: corob
manager: ghogen
ms.openlocfilehash: 5eb0815c218fc018120f7502a4d1c081e98d6642
ms.sourcegitcommit: ebec1d449f2bd98aa851667c2bfeb7e27ce657b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/24/2017
---
# <a name="compiler-error-c3400"></a>Compilerfehler C3400
Zirkuläre Einschränkungsabhängigkeit mit „constraint_1“ und „constraint_2“  
  
 Der Compiler hat zirkuläre Einschränkungen erkannt.  
  
 Weitere Informationen finden Sie unter [Einschränkungen für generische Typparameter (C + c++ / CLI)](../../windows/constraints-on-generic-type-parameters-cpp-cli.md).  
  
## <a name="example"></a>Beispiel  
 Im folgenden Beispiel wird C3400 generiert:  
  
```  
// C3400.cpp  
// compile with: /clr /c  
generic<class T, class U>  
where T : U  
where U : T   // C3400  
public ref struct R {};  
```