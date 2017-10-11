---
title: Compilerfehler C3769 | Microsoft Docs
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- cpp-tools
ms.tgt_pltfrm: 
ms.topic: error-reference
f1_keywords:
- C3769
dev_langs:
- C++
helpviewer_keywords:
- C3769
ms.assetid: 341675e1-7428-4da6-8275-1b2f0a70dacc
caps.latest.revision: 6
author: corob-msft
ms.author: corob
manager: ghogen
ms.translationtype: MT
ms.sourcegitcommit: 35b46e23aeb5f4dbfd2a0dd44b906389dd5bfc88
ms.openlocfilehash: 097b12ca4cdca8f465fd5383e42609187b66d32e
ms.contentlocale: de-de
ms.lasthandoff: 10/10/2017

---
# <a name="compiler-error-c3769"></a>Compilerfehler C3769
'Typ': eine geschachtelte Klasse kann nicht den gleichen Namen wie dem unmittelbar einschließenden Klasse haben  
  
 Eine geschachtelte Klasse kann nicht den gleichen Namen wie dem unmittelbar einschließenden Klasse haben.  
  
## <a name="example"></a>Beispiel  
 Im folgende Beispiel wird C3769 generiert.  
  
```  
// C3769.cpp  
// compile with: /c  
class x {  
   class x {};   // C3769  
   class y {  
      class x{};   // OK  
   };  
};  
```
