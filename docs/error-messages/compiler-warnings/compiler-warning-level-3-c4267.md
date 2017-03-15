---
title: "Compilerwarnung (Stufe 3) C4267 | Microsoft Docs"
ms.custom: ""
ms.date: "11/04/2016"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-cpp"
ms.tgt_pltfrm: ""
ms.topic: "error-reference"
f1_keywords: 
  - "C4267"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "C4267"
ms.assetid: 2fa2f13f-fa4f-47bb-ad8f-6cb19cfc91e6
caps.latest.revision: 15
author: "corob-msft"
ms.author: "corob"
manager: "ghogen"
caps.handback.revision: 15
---
# Compilerwarnung (Stufe 3) C4267
[!INCLUDE[vs2017banner](../../assembler/inline/includes/vs2017banner.md)]

'var': Konvertierung von 'size\_t' nach 'type', Datenverlust möglich  
  
 Der Compiler hat eine Konvertierung von `size_t` zu einem kleineren Typ ermittelt.  
  
 Verwenden Sie zum Beheben dieser Warnung `size_t` anstelle von `type`.  Verwenden Sie alternativ einen integralen Typ, der mindestens so groß wie `size_t` ist.  
  
## Beispiel  
 Im folgenden Beispiel wird der Fehler C4267 generiert:  
  
```  
// C4267.cpp  
// compile by using: cl /W4 C4267.cpp  
void Func1(short) {}  
void Func2(int) {}  
void Func3(long) {}  
void Func4(size_t) {}  
  
int main() {  
   size_t bufferSize = 10;  
   Func1(bufferSize);   // C4267 for all platforms  
   Func2(bufferSize);   // C4267 only for 64-bit platforms  
   Func3(bufferSize);   // C4267 only for 64-bit platforms  
   Func4(bufferSize);   // OK for all platforms  
}  
```