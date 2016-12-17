---
title: "Compiler Error C3278"
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
  - "C3278"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "C3278"
ms.assetid: 56f818f5-85a6-4792-843b-54fe16327658
caps.latest.revision: 9
caps.handback.revision: "9"
ms.author: "corob"
manager: "ghogen"
---
# Compiler Error C3278
[!INCLUDE[vs2017banner](../../assembler/inline/includes/vs2017banner.md)]

Direkter Aufruf der Schnittstellenmethode oder reinen Methode 'Methode' wird zur Laufzeit fehlschlagen.  
  
 Es erfolgte ein Aufruf für eine Schnittstellenmethode oder eine reine Methode, was nicht zulässig ist.  
  
 Im folgenden Beispiel wird C3278 generiert:  
  
```  
// C3278_2.cpp  
// compile with: /clr  
using namespace System;  
interface class I  
{  
   void vmf();  
};  
  
public ref class C: public I  
{  
public:  
   void vmf()  
   {  
      Console::WriteLine( "In C::vmf()" );  
      I::vmf(); // C3278  
   }  
  
};  
  
int main()  
{  
   C^ pC = gcnew C;  
   pC->vmf();  
}  
```