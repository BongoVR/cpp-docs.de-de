---
title: "Compilerfehler C2891 | Microsoft Docs"
ms.custom: ""
ms.date: "11/04/2016"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-cpp"
ms.tgt_pltfrm: ""
ms.topic: "error-reference"
f1_keywords: 
  - "C2891"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "C2891"
ms.assetid: e12cfb2d-df45-4b0d-b155-c51d17e812fa
caps.latest.revision: 7
author: "corob-msft"
ms.author: "corob"
manager: "ghogen"
caps.handback.revision: 7
---
# Compilerfehler C2891
[!INCLUDE[vs2017banner](../../assembler/inline/includes/vs2017banner.md)]

'Parameter': die Adresse eines Vorlagenparameters kann nicht verwendet werden  
  
 Verwenden Sie anstelle von:  
  
```  
template <int i> int* f() { return &i; }  
```  
  
 den folgenden Code:  
  
```  
template <int i> int* f() { return i; }  
```