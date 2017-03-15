---
title: "Compilerfehler C3100 | Microsoft Docs"
ms.custom: ""
ms.date: "11/04/2016"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-cpp"
ms.tgt_pltfrm: ""
ms.topic: "error-reference"
f1_keywords: 
  - "C3100"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "C3100"
ms.assetid: 7a9c9eaf-08ef-442d-94a0-e457beee8549
caps.latest.revision: 5
author: "corob-msft"
ms.author: "corob"
manager: "ghogen"
caps.handback.revision: 5
---
# Compilerfehler C3100
[!INCLUDE[vs2017banner](../../assembler/inline/includes/vs2017banner.md)]

'Ziel': Unbekannter Attributqualifizierer  
  
 Es wurde ein ungültiges Attributziel angegeben.  
  
 Weitere Informationen finden Sie unter [User\-Defined Attributes](../../windows/user-defined-attributes-cpp-component-extensions.md).  
  
## Beispiel  
 Im folgenden Beispiel wird C3100 generiert.  
  
```  
// C3100.cpp  
// compile with: /clr /c  
using namespace System;  
[AttributeUsage(AttributeTargets::All)]  
public ref class Attr : public Attribute {  
public:  
   Attr(int t) : m_t(t) {}  
   int m_t;  
};  
  
[invalid_target:Attr(10)];   // C3100  
[assembly:Attr(10)];   // OK  
```