---
title: Compilerfehler C2117 | Microsoft Docs
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- cpp-tools
ms.tgt_pltfrm: 
ms.topic: error-reference
f1_keywords:
- C2117
dev_langs:
- C++
helpviewer_keywords:
- C2117
ms.assetid: b947379d-5861-42fc-ac26-170318579cbd
caps.latest.revision: 
author: corob-msft
ms.author: corob
manager: ghogen
ms.workload:
- cplusplus
ms.openlocfilehash: f5f214109a6e7838ad0964f912feea78c6e5e9c5
ms.sourcegitcommit: 8fa8fdf0fbb4f57950f1e8f4f9b81b4d39ec7d7a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/21/2017
---
# <a name="compiler-error-c2117"></a>Compilerfehler C2117
"Bezeichner": Arraygrenze überschritten  
  
 Ein Array hat zu viele Initialisierungen:  
  
-   Arrayelemente und Initialisierungen stimmen in Größe und Anzahl nicht überein.  
  
-   Kein Speicherplatz für das Nullabschlusszeichen in einer Zeichenfolge.  
  
 Im folgende Beispiel wird C2117 generiert:  
  
```  
// C2117.cpp  
int main() {  
   char abc[4] = "abcd";   // C2117  
   char def[4] = "abd";   // OK  
}  
```