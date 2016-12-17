---
title: "Compilerfehler C2574"
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
  - "C2574"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "C2574"
ms.assetid: 3e1c5c18-ee8b-4dbb-bfc0-d3b8991af71b
caps.latest.revision: 9
caps.handback.revision: "9"
ms.author: "corob"
manager: "ghogen"
---
# Compilerfehler C2574
[!INCLUDE[vs2017banner](../../assembler/inline/includes/vs2017banner.md)]

'Destruktor': kann nicht statisch deklariert werden  
  
 Weder Destruktoren noch Konstruktoren können als `static` deklariert werden.  
  
 Im folgenden Beispiel wird C2574 generiert:  
  
```  
// C2574.cpp  
// compile with: /c  
class A {  
   virtual static ~A();   // C2574  
   //  try the following line instead  
   // virtual ~A();  
};  
```