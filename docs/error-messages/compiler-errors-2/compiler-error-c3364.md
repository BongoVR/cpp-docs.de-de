---
title: "Compilerfehler C3364 | Microsoft Docs"
ms.custom: ""
ms.date: "11/04/2016"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-cpp"
ms.tgt_pltfrm: ""
ms.topic: "error-reference"
f1_keywords: 
  - "C3364"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "C3364"
ms.assetid: 98654741-60fe-4472-a6af-e580f8c0a6e1
caps.latest.revision: 8
author: "corob-msft"
ms.author: "corob"
manager: "ghogen"
caps.handback.revision: 8
---
# Compilerfehler C3364
[!INCLUDE[vs2017banner](../../assembler/inline/includes/vs2017banner.md)]

'Delegat': Delegatkonstruktor: Argument muss ein Zeiger auf eine Memberfunktion einer verwalteten Klasse oder globalen Funktion sein  
  
 Der zweite Parameter des Delegatkonstruktors akzeptiert entweder die Adresse einer Memberfunktion oder die Adresse einer statischen Memberfunktion einer beliebigen Klasse.  Beide werden als einfache Adressen behandelt.  
  
 Im folgenden Beispiel wird C3364 generiert:  
  
```  
// C3364_2.cpp  
// compile with: /clr  
  
delegate int D( int, int );  
  
ref class C {  
public:  
   int mf( int, int ) {  
      return 1;  
   }  
};  
  
int main() {  
   C^ pC = gcnew C;  
   System::Delegate^ pD = gcnew D( pC,pC->mf( 1, 2 ) ); // C3364  
  
   // try the following line instead  
   // System::Delegate^ pD = gcnew D(pC, &C::mf);  
}  
```  
  
 Im folgenden Beispiel wird C3364 generiert:  
  
```  
// C3364.cpp  
// compile with: /clr:oldSyntax  
#using <mscorlib.dll>  
  
__delegate int D(int, int);  
  
__gc class C {  
public:  
   int mf(int, int) {  
      return 1;  
   }  
};  
  
int main() {  
   C *pC = new C;  
   System::Delegate *pD = new D(pC, pC->mf(1, 2));   // C3364  
   // try the following line instead  
   // System::Delegate *pD = new D(pC, &C::mf);  
}  
```