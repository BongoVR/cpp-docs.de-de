---
title: "Compilerfehler C3732 | Microsoft Docs"
ms.custom: ""
ms.date: "11/04/2016"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-cpp"
ms.tgt_pltfrm: ""
ms.topic: "error-reference"
f1_keywords: 
  - "C3732"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "C3732"
ms.assetid: 2d55a7e1-9c39-4379-a093-2f7beb27e2ca
caps.latest.revision: 7
author: "corob-msft"
ms.author: "corob"
manager: "ghogen"
caps.handback.revision: 7
---
# Compilerfehler C3732
[!INCLUDE[vs2017banner](../../assembler/inline/includes/vs2017banner.md)]

'Schnittstelle': Eine benutzerdefinierte Schnittstelle, die COM\-Ereignisse auslöst, kann nicht von IDispatch erben  
  
 Eine Schnittstelle, die COM\-Ereignisse unterstützt, kann nicht von `IDispatch` erben.  Weitere Informationen finden Sie unter [Ereignisbehandlung in COM](../../cpp/event-handling-in-com.md).  
  
 Im folgenden Beispiel wird C3732 generiert:  
  
```  
// C3732.cpp  
#define _ATL_ATTRIBUTES 1  
#include "atlbase.h"  
#include "atlcom.h"  
  
[module(name="test")];  
  
// to resolve this C3732, use dual instead of object  
// or inherit from IUnknown  
[ object ]  
__interface I : IDispatch  
{  
};  
  
[ event_source(com), coclass ]  
struct A  
{  
   __event __interface I;   // C3732  
};  
  
int main()  
{  
}  
```