---
title: "Compilerfehler C3622 | Microsoft Docs"
ms.custom: ""
ms.date: "11/04/2016"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-cpp"
ms.tgt_pltfrm: ""
ms.topic: "error-reference"
f1_keywords: 
  - "C3622"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "C3622"
ms.assetid: 02836f78-0cf2-4947-b87e-710187d81014
caps.latest.revision: 11
author: "corob-msft"
ms.author: "corob"
manager: "ghogen"
caps.handback.revision: 11
---
# Compilerfehler C3622
[!INCLUDE[vs2017banner](../../assembler/inline/includes/vs2017banner.md)]

'Klasse' : Eine Klasse, die als 'keyword' deklariert wurde, kann nicht instanziiert werden  
  
 Es wurde versucht, eine als [abstract](../../windows/abstract-cpp-component-extensions.md) \(or [\_\_abstract](../../misc/abstract.md)\) gekennzeichnete Klasse zu instanziieren.  Eine als **abstract** gekennzeichnete Klasse kann zwar eine Basisklasse sein, aber nicht instanziiert werden.  
  
## Beispiel  
 Im folgenden Beispiel wird C3622 generiert.  
  
```  
// C3622.cpp  
// compile with: /clr  
ref class a abstract {};  
  
int main() {  
   a aa;   // C3622  
}  
```  
  
## Beispiel  
 Im folgenden Beispiel wird C3622 generiert.  
  
```  
// C3622_b.cpp  
// compile with: /clr:oldSyntax  
__abstract class a {  
};  
int main() {  
   a aa;   // C3622  
}  
```