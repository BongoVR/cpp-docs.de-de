---
title: "Compilerwarnung (Stufe 1) C4926 | Microsoft Docs"
ms.custom: ""
ms.date: "11/04/2016"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-csharp"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "C4926"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "C4926"
ms.assetid: 5717fce0-146f-4ef2-bde0-e9a01c0922d1
caps.latest.revision: 6
author: "corob-msft"
ms.author: "corob"
manager: "ghogen"
caps.handback.revision: 6
---
# Compilerwarnung (Stufe 1) C4926
[!INCLUDE[vs2017banner](../../assembler/inline/includes/vs2017banner.md)]

"Bezeichner": Symbol ist bereits definiert: Attribute werden ignoriert  
  
 Es wurde eine Vorausdeklaration gefunden, aber ein attributiertes Konstrukt mit demselben Namen ist bereits vorhanden. Die Attribute für die Vorausdeklaration werden ignoriert.  
  
 Im folgenden Beispiel wird C4926 generiert.  
  
```  
// C4926.cpp // compile with: /W1 [module(name="MyLib")]; [coclass] struct a { }; [coclass] struct a;   // C4926 int main() { }  
```