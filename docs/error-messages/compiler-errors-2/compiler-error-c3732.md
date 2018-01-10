---
title: Compilerfehler C3732 | Microsoft Docs
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-tools
ms.tgt_pltfrm: 
ms.topic: error-reference
f1_keywords: C3732
dev_langs: C++
helpviewer_keywords: C3732
ms.assetid: 2d55a7e1-9c39-4379-a093-2f7beb27e2ca
caps.latest.revision: "7"
author: corob-msft
ms.author: corob
manager: ghogen
ms.workload: cplusplus
ms.openlocfilehash: 5c6c0e4b2b5fc97bfabea0b059c89d2abff8b901
ms.sourcegitcommit: 8fa8fdf0fbb4f57950f1e8f4f9b81b4d39ec7d7a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/21/2017
---
# <a name="compiler-error-c3732"></a>Compilerfehler C3732
'Schnittstelle': eine benutzerdefinierte Schnittstelle, die COM-Ereignisse auslöst, kann nicht von IDispatch erben  
  
 Eine Schnittstelle, die COM-Ereignisse unterstützen kann nicht Vererben `IDispatch`. Weitere Informationen finden Sie unter [Ereignisbehandlung in COM](../../cpp/event-handling-in-com.md).  
  
 Der folgende Fehler wird C3732 generiert:  
  
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