---
title: "Compilerfehler C3891 | Microsoft Docs"
ms.custom: ""
ms.date: "11/04/2016"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-cpp"
ms.tgt_pltfrm: ""
ms.topic: "error-reference"
f1_keywords: 
  - "C3891"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "C3891"
ms.assetid: 6e1a9458-97f5-4580-bc0f-aa97a1bfd20d
caps.latest.revision: 9
author: "corob-msft"
ms.author: "corob"
manager: "ghogen"
caps.handback.revision: 9
---
# Compilerfehler C3891
[!INCLUDE[vs2017banner](../../assembler/inline/includes/vs2017banner.md)]

'var': Ein literal\-Datenmember kann nicht als L\-Wert verwendet werden  
  
 Eine [literal](../../windows/literal-cpp-component-extensions.md)\-Variable ist eine Konstante, deren Wert nicht nach der Initialisierung in der Deklaration geändert werden kann.  
  
 Im folgenden Beispiel wird C3891 generiert:  
  
```  
// C3891.cpp  
// compile with: /clr  
ref struct Y1 {  
   literal int staticConst = 9;  
};  
  
int main() {  
   Y1::staticConst = 0;   // C3891  
}  
```