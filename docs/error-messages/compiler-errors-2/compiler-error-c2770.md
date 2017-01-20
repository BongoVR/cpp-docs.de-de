---
title: "Compilerfehler C2770"
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
  - "C2770"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "C2770"
ms.assetid: 100001b5-80b0-4971-8ff6-9023f443c926
caps.latest.revision: 8
caps.handback.revision: "8"
ms.author: "corob"
manager: "ghogen"
---
# Compilerfehler C2770
[!INCLUDE[vs2017banner](../../assembler/inline/includes/vs2017banner.md)]

Ungültige explizite template\_or\_generic\-Argumente für 'Vorlage'  
  
 Potenzielle Funktionsvorlagen mit expliziten generischen oder Vorlagenargumenten ergaben nicht zulässige Funktionstypen.  
  
 Im folgenden Beispiel wird C2770 generiert:  
  
```  
// C2770.cpp  
#include <stdio.h>  
template <class T>  
int f(typename T::B*);   // expects type with member B  
  
struct Err {};  
  
int main() {  
   f<int>(0);   // C2770 int has no B  
   // try the following line instead  
   f<OK>(0);  
}  
```