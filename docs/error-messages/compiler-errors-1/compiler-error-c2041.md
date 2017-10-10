---
title: Compilerfehler Fehler C2041 | Microsoft Docs
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- cpp-tools
ms.tgt_pltfrm: 
ms.topic: error-reference
f1_keywords:
- C2041
dev_langs:
- C++
helpviewer_keywords:
- C2041
ms.assetid: c9a33bb1-f9cf-47d6-bd21-7d867a8c37d5
caps.latest.revision: 7
author: corob-msft
ms.author: corob
manager: ghogen
ms.translationtype: MT
ms.sourcegitcommit: 35b46e23aeb5f4dbfd2a0dd44b906389dd5bfc88
ms.openlocfilehash: 4102f95b5a48860cba2e9ec79d2d5c22cd1413cf
ms.contentlocale: de-de
ms.lasthandoff: 10/09/2017

---
# <a name="compiler-error-c2041"></a>Compilerfehler Fehler C2041
Unzulässige Ziffer "Character" für Basis 'Zahl'  
  
 Das angegebene Zeichen ist keine gültige Ziffer für Basis (z. B. oktale oder hexadezimale).  
  
 Im folgende Beispiel wird C2041 generiert:  
  
```  
// C2041.cpp  
int i = 081;   // C2041  8 is not a base 8 digit  
```  
  
 Mögliche Lösung:  
  
```  
// C2041b.cpp  
// compile with: /c  
int j = 071;  
```
