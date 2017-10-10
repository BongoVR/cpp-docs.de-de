---
title: Compiler-Fehler C2724 generiert | Microsoft Docs
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- cpp-tools
ms.tgt_pltfrm: 
ms.topic: error-reference
f1_keywords:
- C2724
dev_langs:
- C++
helpviewer_keywords:
- C2724
ms.assetid: 4e4664bc-8c96-4156-b79f-03436f532ea8
caps.latest.revision: 6
author: corob-msft
ms.author: corob
manager: ghogen
ms.translationtype: MT
ms.sourcegitcommit: 35b46e23aeb5f4dbfd2a0dd44b906389dd5bfc88
ms.openlocfilehash: 13c582f081d78e415b4c98bf300b18004fcc33bc
ms.contentlocale: de-de
ms.lasthandoff: 10/10/2017

---
# <a name="compiler-error-c2724"></a>Compiler-Fehler C2724 generiert
'Bezeichner':'static' sollte nicht für Memberfunktionen, die im Dateibereich definiert verwendet werden  
  
 Statische Memberfunktionen sollten mit externer Bindung deklariert werden.  
  
 Im folgende Beispiel wird C2724 generiert:  
  
```  
// C2724.cpp  
class C {  
   static void func();  
};  
  
static void C::func(){};   // C2724  
// try the following line instead  
// void C::func(){};  
```
