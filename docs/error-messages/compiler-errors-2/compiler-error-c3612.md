---
title: "Compilerfehler C3612"
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
  - "C3612"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "C3612"
ms.assetid: aa6e3a2b-4afa-481c-98c1-1b6d1f82f869
caps.latest.revision: 11
caps.handback.revision: "11"
ms.author: "corob"
manager: "ghogen"
---
# Compilerfehler C3612
[!INCLUDE[vs2017banner](../../assembler/inline/includes/vs2017banner.md)]

'Typ': Eine versiegelte Klasse kann nicht abstrakt sein  
  
 Mit `value` \(oder [\_\_value](../../misc/value.md) definierte Typen sind standardmäßig versiegelt, und eine Klasse ist abstrakt, sofern sie nicht alle Methoden ihrer Basisklasse implementiert.  Eine versiegelte abstrakte Klasse kann weder eine Basisklasse sein noch instanziiert werden.  
  
 Weitere Informationen finden Sie unter [Classes and Structs](../../windows/classes-and-structs-cpp-component-extensions.md).  
  
 Im folgenden Beispiel wird C3612 generiert:  
  
```  
// C3612.cpp  
// compile with: /clr /c  
value struct V: public System::ICloneable {};   // C3612  
  
// OK  
value struct V2: public System::ICloneable {  
   Object^ Clone();  
};  
```