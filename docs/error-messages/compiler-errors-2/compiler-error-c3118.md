---
title: "Compilerfehler C3118"
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
  - "C3118"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "C3118"
ms.assetid: 40fbe681-8868-4cb2-a2b2-4db4449319a7
caps.latest.revision: 6
caps.handback.revision: "6"
ms.author: "corob"
manager: "ghogen"
---
# Compilerfehler C3118
[!INCLUDE[vs2017banner](../../assembler/inline/includes/vs2017banner.md)]

'Schnittstelle': Schnittstellen unterstützen keine virtuelle Vererbung  
  
 Sie haben versucht, virtuell von einer Schnittstelle zu erben.  Beispiel:  
  
```  
// C3118.cpp  
__interface I1 {  
};  
  
__interface I2 : virtual I1 {   // C3118  
};  
```  
  
 erzeugt diesen Fehler.