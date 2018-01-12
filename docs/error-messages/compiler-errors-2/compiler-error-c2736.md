---
title: Compiler-Fehler C2736 generiert | Microsoft Docs
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-tools
ms.tgt_pltfrm: 
ms.topic: error-reference
f1_keywords: C2736
dev_langs: C++
helpviewer_keywords: C2736
ms.assetid: 95a6bc28-c0cb-49dc-87e6-e993dbbba881
caps.latest.revision: "7"
author: corob-msft
ms.author: corob
manager: ghogen
ms.workload: cplusplus
ms.openlocfilehash: 6356e6de30222c46b2831830e108ed3cc084c905
ms.sourcegitcommit: 8fa8fdf0fbb4f57950f1e8f4f9b81b4d39ec7d7a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/21/2017
---
# <a name="compiler-error-c2736"></a>Compiler-Fehler C2736 generiert
' Schlüsselwort ' ist in Typumwandlung nicht zulässig.  
  
 Das Schlüsselwort ist in einer Typumwandlung ungültig.  
  
 Im folgende Beispiel wird C2736 generiert:  
  
```  
// C2736.cpp  
int main() {  
   return (virtual) 0;   // C2736  
   // try the following line instead  
   // return 0;  
}  
```