---
title: "Compilerfehler C2738 | Microsoft Docs"
ms.custom: ""
ms.date: "11/04/2016"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-cpp"
ms.tgt_pltfrm: ""
ms.topic: "error-reference"
f1_keywords: 
  - "C2738"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "C2738"
ms.assetid: 896b4640-1ee0-4cd8-9910-de3efa30006a
caps.latest.revision: 7
author: "corob-msft"
ms.author: "corob"
manager: "ghogen"
caps.handback.revision: 7
---
# Compilerfehler C2738
[!INCLUDE[vs2017banner](../../assembler/inline/includes/vs2017banner.md)]

'Deklaration': Ist mehrdeutig oder kein Member von 'Typ'  
  
 Eine Funktion wurde falsch deklariert.  
  
 Im folgenden Beispiel wird C2738 generiert:  
  
```  
// C2738.cpp  
struct A {  
   template <class T> operator T*();  
   // template <class T> operator T();  
};  
  
template <>  
A::operator int() {   // C2738  
  
// try the following line instead  
// A::operator int*() {  
  
// or use the commented member declaration  
  
   return 0;  
}  
```