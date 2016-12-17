---
title: "Compilerwarnung (Stufe 4) C4210"
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
  - "C4210"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "C4210"
ms.assetid: f8600adf-dfe2-4022-a37a-3d4997641dfd
caps.latest.revision: 7
caps.handback.revision: "7"
ms.author: "corob"
manager: "ghogen"
---
# Compilerwarnung (Stufe 4) C4210
[!INCLUDE[vs2017banner](../../assembler/inline/includes/vs2017banner.md)]

Nicht dem Standard entsprechende Erweiterung: Funktion gehört zum Gültigkeitsbereich der Datei  
  
 Bei Verwendung der Microsoft\-Standarderweiterungen \([\/Ze](../../build/reference/za-ze-disable-language-extensions.md)\) befinden sich Funktionsdeklarationen innerhalb des Dateigültigkeitsbereichs.  
  
```  
// C4210.c  
// compile with: /W4 /c  
void func1()  
{  
   extern int func2( double );   // C4210 expected  
}  
  
int main()  
{  
   func2( 4 );   //  /Ze passes 4 as type double  
}                //  /Za passes 4 as type int  
```  
  
 Durch diese Erweiterung kann verhindert werden, dass der Code auf andere Compiler portierbar ist.