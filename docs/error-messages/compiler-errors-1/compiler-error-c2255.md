---
title: Compilerfehler C2255 | Microsoft Docs
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-tools
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords: C2255
dev_langs: C++
helpviewer_keywords: C2255
ms.assetid: 67dc4cb0-de6b-4405-bd64-d47736367a93
caps.latest.revision: "8"
author: corob-msft
ms.author: corob
manager: ghogen
ms.workload: cplusplus
ms.openlocfilehash: 6ca5f2a33b07ff0b78f12c20f528f1d9b6c3c20d
ms.sourcegitcommit: 8fa8fdf0fbb4f57950f1e8f4f9b81b4d39ec7d7a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/21/2017
---
# <a name="compiler-error-c2255"></a>Compilerfehler C2255
"Element": außerhalb einer Klassendefinition nicht zulässig.  
  
 Beispielsweise wird eine Funktion, die keine Memberfunktion ist, als `friend`deklariert.  
  
 Im folgenden Beispiel wird C2255 generiert:  
  
```  
// C2255.cpp  
// compile with: /c  
class A {  
private:  
   void func1();  
   friend void func2();  
};  
  
friend void func1() {}   // C2255  
void func2(){}  
```