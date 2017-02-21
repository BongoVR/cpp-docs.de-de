---
title: "Compilerfehler C3159 | Microsoft Docs"
ms.custom: ""
ms.date: "11/04/2016"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-cpp"
ms.tgt_pltfrm: ""
ms.topic: "error-reference"
f1_keywords: 
  - "C3159"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "C3159"
ms.assetid: e115cc76-0021-4568-95fd-61a324c41a85
caps.latest.revision: 10
author: "corob-msft"
ms.author: "corob"
manager: "ghogen"
caps.handback.revision: 10
---
# Compilerfehler C3159
[!INCLUDE[vs2017banner](../../assembler/inline/includes/vs2017banner.md)]

'Zeiger': Array von Zeigern zu einem Werttyp kann nicht deklariert werden  
  
 Ein Array von Zeigern auf einen Werttyp kann nicht deklariert werden.  
  
 C3159 ist nur über **\/clr:oldSyntax** erreichbar.  
  
 Im folgenden Beispiel wird C3159 generiert:  
  
```  
// C3159.cpp  
// compile with: /clr:oldSyntax  
#using <mscorlib.dll>  
  
__value struct B {  
};  
  
void f( B*[] );   // C3159  
  
int main() {  
}  
```