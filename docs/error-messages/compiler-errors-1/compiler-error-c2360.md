---
title: "Compilerfehler C2360 | Microsoft Docs"
ms.custom: ""
ms.date: "11/04/2016"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-cpp"
ms.tgt_pltfrm: ""
ms.topic: "error-reference"
f1_keywords: 
  - "C2360"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "C2360"
ms.assetid: 51bfd2ee-8108-4777-aa93-148b9cebfa83
caps.latest.revision: 8
author: "corob-msft"
ms.author: "corob"
manager: "ghogen"
caps.handback.revision: 8
---
# Compilerfehler C2360
[!INCLUDE[vs2017banner](../../assembler/inline/includes/vs2017banner.md)]

Initialisierung von 'Bezeichner' wird durch 'case'\-Markierung übersprungen  
  
 Die Initialisierung von `identifier` kann in einer `switch`\-Anweisung übersprungen werden.  Sprünge hinter eine Deklaration sind bei einer Initialisierung nicht zulässig, es sein denn, sie befindet sich innerhalb eines Blockes. \(Sofern die Variable nicht innerhalb eines Blockes definiert ist, befindet sie sich bis zum Ende der `switch`\-Anweisung innerhalb des Gültigkeitsbereichs.\)  
  
 Im folgenden Beispiel wird C2360 generiert:  
  
```  
// C2360.cpp  
int main() {  
   int x = 0;  
   switch ( x ) {  
   case 0 :  
      int i = 1;  
      { int j = 1; }  
   case 1 :   // C2360  
      int k = 1;  
   }  
}  
```  
  
 Mögliche Lösung:  
  
```  
// C2360b.cpp  
int main() {  
   int x = 0;  
   switch ( x ) {  
   case 0 :  
      { int j = 1; int i = 1;}  
   case 1 :  
      int k = 1;  
   }  
}  
```