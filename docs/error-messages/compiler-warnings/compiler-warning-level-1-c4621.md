---
title: "Compilerwarnung (Stufe 1) C4621 | Microsoft Docs"
ms.custom: ""
ms.date: "11/04/2016"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-cpp"
ms.tgt_pltfrm: ""
ms.topic: "error-reference"
f1_keywords: 
  - "C4621"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "C4621"
ms.assetid: 40931bd9-cb89-497e-86f0-cec9f016c63c
caps.latest.revision: 6
author: "corob-msft"
ms.author: "corob"
manager: "ghogen"
caps.handback.revision: 6
---
# Compilerwarnung (Stufe 1) C4621
[!INCLUDE[vs2017banner](../../assembler/inline/includes/vs2017banner.md)]

Keine Postfix\-Form für 'Operator \-\-' für den Typ 'Typ' gefunden, Präfix\-Form wird verwendet  
  
 Für den angegebenen Typ wurde kein Postfix\-Dekrementoperator definiert.  Der Compiler hat stattdessen den überladenen Operator Präfix verwendet.  
  
 Diese Warnung kann durch die Definition eines Operators Postfix `--` vermieden werden.  Erstellen Sie eine aus zwei Argumenten bestehende Version des Operators `--`, wie im Folgenden dargestellt:  
  
```  
// C4621.cpp  
// compile with: /W1  
class A  
{  
public:  
   A(int nData) : m_nData(nData)  
   {  
   }  
  
   A operator--()  
   {  
      m_nData -= 1;  
      return *this;  
   }  
  
   // A operator--(int)  
   // {  
   //    A tmp = *this;  
   //    m_nData -= 1;  
   //    return tmp;  
   // }  
  
private:  
   int m_nData;  
};  
  
int main()  
{  
   A a(10);  
   --a;  
   a--;   // C4621  
}  
```