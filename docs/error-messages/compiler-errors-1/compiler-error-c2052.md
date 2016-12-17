---
title: "Compilerfehler C2052"
ms.custom: na
ms.date: "12/03/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: na
ms.suite: na
ms.technology: 
  - "devlang-cpp"
ms.tgt_pltfrm: na
ms.topic: "error-reference"
f1_keywords: 
  - "C2052"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "C2052"
ms.assetid: 922ca43b-b64b-4ef7-9611-c7313be3fd79
caps.latest.revision: 8
caps.handback.revision: "8"
ms.author: "corob"
manager: "ghogen"
---
# Compilerfehler C2052
[!INCLUDE[vs2017banner](../../assembler/inline/includes/vs2017banner.md)]

'Typ': Unzulässiger Typ für case\-Ausdruck  
  
 **Case**\-Ausdrücke müssen ganzzahlige Konstanten sein.  
  
 Im folgenden Beispiel wird C2052 generiert:  
  
```  
// C2052.cpp  
int main() {  
   int index = 0;  
   switch (index) {  
      case 1:  
         return 24;  
      case 1.0:   // C2052  
      // try the following line instead  
      // case 2:  
         return 23;  
   }  
}  
```