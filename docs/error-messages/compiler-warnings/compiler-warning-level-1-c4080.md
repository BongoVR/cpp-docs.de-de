---
title: "Compilerwarnung (Stufe 1) C4080 | Microsoft Docs"
ms.custom: ""
ms.date: "11/04/2016"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-csharp"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "C4080"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "C4080"
ms.assetid: 964fb3f4-b9fd-450b-aa23-35cece126172
caps.latest.revision: 7
author: "corob-msft"
ms.author: "corob"
manager: "ghogen"
caps.handback.revision: 7
---
# Compilerwarnung (Stufe 1) C4080
[!INCLUDE[vs2017banner](../../assembler/inline/includes/vs2017banner.md)]

Bezeichner für Segmentnamen erwartet; "Symbol" gefunden  
  
 Der Name des Segments in [\#pragma alloc\_text](../../preprocessor/alloc-text.md) muss eine Zeichenfolge oder ein Bezeichner sein. Der Compiler ignoriert das Pragma, wenn kein gültiger Bezeichner gefunden wurde.  
  
 Im folgenden Beispiel wird C4080 generiert:  
  
```  
// C4080.cpp // compile with: /W1 extern "C" void func(void); #pragma alloc_text()   // C4080 // try this line to resolve the warning // #pragma alloc_text("mysection", func) int main() { } void func(void) { }  
```