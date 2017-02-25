---
title: "Compilerfehler C2645 | Microsoft Docs"
ms.custom: ""
ms.date: "11/04/2016"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-cpp"
ms.tgt_pltfrm: ""
ms.topic: "error-reference"
f1_keywords: 
  - "C2645"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "C2645"
ms.assetid: 6609c2fa-c3b2-4a6b-8e8d-58fb52f67175
caps.latest.revision: 8
author: "corob-msft"
ms.author: "corob"
manager: "ghogen"
caps.handback.revision: 8
---
# Compilerfehler C2645
[!INCLUDE[vs2017banner](../../assembler/inline/includes/vs2017banner.md)]

Kein vollständiger Name für Memberzeiger \("::\*" gefunden\)  
  
 In der Deklaration eines Memberzeigers wurde keine Klasse angegeben.  
  
 Im folgenden Beispiel wird C2645 generiert:  
  
```  
// C2645.cpp  
class A {};  
int main() {  
   int B::* bp;   // C2645 B not defined  
   int A::* ap;   // OK  
}  
```