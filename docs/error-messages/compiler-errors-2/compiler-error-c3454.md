---
title: Compilerfehler C3454 | Microsoft Docs
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- cpp-tools
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- C3454
dev_langs:
- C++
helpviewer_keywords:
- C3454
ms.assetid: dc4e6d57-5b4d-4114-8d6f-22f9ae62925b
caps.latest.revision: 6
author: corob-msft
ms.author: corob
manager: ghogen
ms.translationtype: MT
ms.sourcegitcommit: 35b46e23aeb5f4dbfd2a0dd44b906389dd5bfc88
ms.openlocfilehash: 026b77ca4f9488c1178a2815ffb0a9c7c71bdf54
ms.contentlocale: de-de
ms.lasthandoff: 10/10/2017

---
# <a name="compiler-error-c3454"></a>Compilerfehler C3454
[attribut] ist in der Klassendeklaration nicht zulässig  
  
 Es muss eine Klasse für es definiert werden, damit es ein Attribut sein kann.  
  
 Weitere Informationen finden Sie unter [attribute](../../windows/attribute.md).  
  
## <a name="example"></a>Beispiel  
 Im folgenden Beispiel wird C3454 generiert:  
  
```  
// C3454.cpp  
// compile with: /clr /c  
using namespace System;  
  
[attribute]   // C3454  
ref class Attr1;  
  
[attribute]   // OK  
ref class Attr2 {};  
```
