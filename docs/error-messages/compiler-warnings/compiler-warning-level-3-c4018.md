---
title: "Compilerwarnung (Stufe 3) C4018"
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
  - "C4018"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "C4018"
ms.assetid: 6e8cbb04-d914-4319-b431-cbc2fbe40eb1
caps.latest.revision: 7
caps.handback.revision: "7"
ms.author: "corob"
manager: "ghogen"
---
# Compilerwarnung (Stufe 3) C4018
[!INCLUDE[vs2017banner](../../assembler/inline/includes/vs2017banner.md)]

'Ausdruck': Konflikt zwischen signed und unsigned  
  
 Beim Vergleich von zwei Zahlen mit bzw. ohne Vorzeichen musste der Wert mit Vorzeichen vom Compiler in einen vorzeichenlosen Wert umgewandelt werden.  
  
 Diese Warnung wird nicht mehr angezeigt, wenn Sie einen der zwei Typen beim Testen von Typen mit und ohne Vorzeichen umwandeln.  
  
 Im folgenden Beispiel wird C4018 generiert:  
  
```  
// C4018.cpp  
// compile with: /W3  
int main() {  
   unsigned int uc = 0;  
   int c = 0;  
   unsigned int c2 = 0;  
  
   if (uc < c) uc = 0;   // C4018  
  
   // OK  
   if (uc == c2) uc = 0;  
}  
```