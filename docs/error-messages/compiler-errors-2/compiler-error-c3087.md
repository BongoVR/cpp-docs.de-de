---
title: Compilerfehler C3087 | Microsoft Docs
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- cpp-tools
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- C3087
dev_langs:
- C++
helpviewer_keywords:
- C3087
ms.assetid: 4f5bdd52-a853-4f02-b160-6868e9190b9d
caps.latest.revision: 5
author: corob-msft
ms.author: corob
manager: ghogen
ms.translationtype: MT
ms.sourcegitcommit: 35b46e23aeb5f4dbfd2a0dd44b906389dd5bfc88
ms.openlocfilehash: d786cb3f8c04e5d8ff32aebe30915d4aca3cfb2f
ms.contentlocale: de-de
ms.lasthandoff: 10/10/2017

---
# <a name="compiler-error-c3087"></a>Compilerfehler C3087
„named_argument“: Durch den Aufruf von „attribute“ wird dieser Member bereits initialisiert.  
  
 Ein benanntes Argument wurde im selben Attributblock festgelegt wie ein unbenanntes Argument für den gleichen Wert. Geben Sie nur ein benanntes oder unbenanntes Argument an.  
  
## <a name="example"></a>Beispiel  
 Im folgenden Beispiel wird C3087 generiert.  
  
```  
// C3087.cpp  
// compile with: /c  
[idl_quote("quote1", text="quote2")];   // C3087  
[idl_quote(text="quote3")];   // OK  
[idl_quote("quote4")];   // OK  
```
