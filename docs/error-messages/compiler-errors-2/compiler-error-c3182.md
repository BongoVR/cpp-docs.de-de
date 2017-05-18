---
title: Compiler-Fehler C3182 generiert | Microsoft-Dokumentation
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- cpp-tools
ms.tgt_pltfrm: 
ms.topic: error-reference
f1_keywords:
- C3182
dev_langs:
- C++
helpviewer_keywords:
- C3182
ms.assetid: f3681266-308e-4990-a979-8eef8920e186
caps.latest.revision: 11
author: corob-msft
ms.author: corob
manager: ghogen
translation.priority.ht:
- cs-cz
- de-de
- es-es
- fr-fr
- it-it
- ja-jp
- ko-kr
- pl-pl
- pt-br
- ru-ru
- tr-tr
- zh-cn
- zh-tw
ms.translationtype: Machine Translation
ms.sourcegitcommit: c243063a9770542f137d5950e8a269f771960f74
ms.openlocfilehash: 3dfd76788c55e74625172dedf2ceb5b8bdfaa061
ms.contentlocale: de-de
ms.lasthandoff: 02/24/2017

---
# <a name="compiler-error-c3182"></a>Compiler-Fehler C3182 generiert
'Klasse': eine Memberdeklaration using-Deklaration oder der Zugriff ist nicht zulässig, innerhalb einer verwalteten oder WinRTtype  
  
 Ein [mit](../../cpp/using-declaration.md) -Deklaration ist in sämtlichen verwalteten Klassen unzulässig.  
  
 Im folgenden Beispiel wird C3182 generiert und gezeigt, wie Sie diesen Fehler beheben:  
  
```  
// C3182a.cpp  
// compile with: /clr /c  
ref struct B {  
   void mf(int) {  
   }  
};  
  
ref struct D : B {  
   using B::mf;   // C3182, delete to resolve  
   void mf(char) {  
   }  
};  
```  

