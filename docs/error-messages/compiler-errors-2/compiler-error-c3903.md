---
title: "Compilerfehler C3903"
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
  - "C3903"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "C3903"
ms.assetid: cf47d7ad-a3bd-4f75-a253-71586e7a3be6
caps.latest.revision: 9
caps.handback.revision: "9"
ms.author: "corob"
manager: "ghogen"
---
# Compilerfehler C3903
[!INCLUDE[vs2017banner](../../assembler/inline/includes/vs2017banner.md)]

'Eigenschaft': hat keine set\-Methode oder get\-Methode  
  
 Eine Eigenschaft muss mindestens über eine `get`\-Methode oder eine `set`\-Methode verfügen.  Weitere Informationen finden Sie unter [Eigenschaft](../../windows/property-cpp-component-extensions.md).  
  
 Im folgenden Beispiel wird C3903 generiert:  
  
```  
// C3903.cpp  
// compile with: /clr  
ref class X {  
   property int P {  
      void f(int){}  
      // Add one or both of the following lines.  
      // void set(int){}  
      // int get(){return 0;}  
   };   // C3903  
  
   property double Q[,,,,] {  
      void f(){}  
      // Add one or both of the following lines.  
      // void set(int, char, int, char, double, double){}  
      // double get(int, char, int, char, double){return 1.1;}  
   }   // C3903  
};  
```