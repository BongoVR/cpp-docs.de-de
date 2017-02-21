---
title: "_unlock | Microsoft Docs"
ms.custom: ""
ms.date: "11/04/2016"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-cpp"
ms.tgt_pltfrm: ""
ms.topic: "article"
apiname: 
  - "_unlock"
apilocation: 
  - "msvcrt.dll"
  - "msvcr100.dll"
  - "msvcr110_clr0400.dll"
  - "msvcr110.dll"
  - "msvcr80.dll"
  - "msvcr120.dll"
  - "msvcr90.dll"
  - "msvcr120_clr0400.dll"
apitype: "DLLExport"
f1_keywords: 
  - "unlock"
  - "_unlock"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "unlock-Funktion"
  - "_unlock-Funktion"
ms.assetid: 2eda2507-a134-4997-aa12-f2f8cb319e14
caps.latest.revision: 5
author: "corob-msft"
ms.author: "corob"
manager: "ghogen"
caps.handback.revision: 5
---
# _unlock
[!INCLUDE[vs2017banner](../assembler/inline/includes/vs2017banner.md)]

Gibt eine Multi\-Thread\-Sperre frei.  
  
> [!IMPORTANT]
>  Diese Funktion ist veraltet. Von Visual Studio 2015 an ist sie nicht in der CRT verfügbar.  
  
## Syntax  
  
```  
void __cdecl _unlock(  
   int locknum  
);  
```  
  
#### Parameter  
 \[in\] `locknum`  
 Der Bezeichner der freizugebenden Sperre.  
  
## Anforderungen  
 **Quelle:** mlock.c  
  
## Siehe auch  
 [Alphabetische Funktionsreferenz](../c-runtime-library/reference/crt-alphabetical-function-reference.md)   
 [\_lock](../c-runtime-library/lock.md)