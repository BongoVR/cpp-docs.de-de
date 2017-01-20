---
title: "Compilerfehler C3858"
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
  - "C3858"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "C3858"
ms.assetid: 46e178d5-a55f-4ac6-a9dc-561fbcba5c1f
caps.latest.revision: 6
caps.handback.revision: "6"
ms.author: "corob"
manager: "ghogen"
---
# Compilerfehler C3858
[!INCLUDE[vs2017banner](../../assembler/inline/includes/vs2017banner.md)]

'Typ': Kann im aktuellen Bereich nicht erneut deklariert werden  
  
 Der Typ kann im selben Gültigkeitsbereich nicht zweimal deklariert werden.  
  
 Im folgenden Beispiel wird C3858 generiert:  
  
```  
// C3858.cpp  
// compile with: /LD  
template <class T>  
struct Outer  
{  
   struct Inner;  
};  
  
template <class T>  
struct Outer<T>::Inner;   // C3858  
// try the following line instead  
// struct Outer<T>::Inner{};  
```