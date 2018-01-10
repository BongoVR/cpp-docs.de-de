---
title: Compiler-Fehler C2792 generiert | Microsoft Docs
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-tools
ms.tgt_pltfrm: 
ms.topic: error-reference
f1_keywords: C2792
dev_langs: C++
helpviewer_keywords: C2792
ms.assetid: 392cf748-4f5e-4e62-a364-3118d5658408
caps.latest.revision: "8"
author: corob-msft
ms.author: corob
manager: ghogen
ms.workload: cplusplus
ms.openlocfilehash: 2b0e2436cda7763ab0256082b42a3a46fa010737
ms.sourcegitcommit: 8fa8fdf0fbb4f57950f1e8f4f9b81b4d39ec7d7a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/21/2017
---
# <a name="compiler-error-c2792"></a>Compiler-Fehler C2792 generiert
'Superuser": Dieses Schlüsselwort muss darauf folgen '::'  
  
 Das einzige Token, das befolgen kann, dass Sie das Schlüsselwort `__super` ist `::`.  
  
 Im folgende Beispiel wird C2792 generiert:  
  
```  
// C2792.cpp  
struct B {  
   void mf();  
};  
  
struct D : B {  
   void mf() {  
      __super.();   // C2792  
  
      // try the following line instead  
      // __super::mf();  
   }  
};  
```