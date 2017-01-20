---
title: "Compilerfehler C3277"
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
  - "C3277"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "C3277"
ms.assetid: 8ac5f476-e30c-4879-92c6-f03cdbd74045
caps.latest.revision: 7
caps.handback.revision: "7"
ms.author: "corob"
manager: "ghogen"
---
# Compilerfehler C3277
[!INCLUDE[vs2017banner](../../assembler/inline/includes/vs2017banner.md)]

Eine nicht verwaltete Enumeration 'Enumeration' kann nicht innerhalb eines verwalteten 'Typs' definiert werden  
  
 Eine Enumeration wurde innerhalb eines verwalteten Typs falsch definiert.  
  
 Im folgenden Beispiel wird C3277 generiert:  
  
```  
// C3277a.cpp  
// compile with: /clr  
ref class A  
{  
   enum E {e1,e2};   // C3277  
   // try the following line instead  
   // enum class E {e1,e2};  
};  
  
int main()  
{  
}  
```  
  
 Im folgenden Beispiel wird C3277 generiert:  
  
```  
// C3277b.cpp  
// compile with: /clr:oldSyntax  
#using <mscorlib.dll>  
__gc class A  
{  
   enum E {e1,e2};   // C3277  
   // try the following line instead  
   // __value enum E {e1,e2};  
};  
  
int main()  
{  
}  
```