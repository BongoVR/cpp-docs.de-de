---
title: Compilerfehler C3385 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C3385
dev_langs:
- C++
helpviewer_keywords:
- C3385
ms.assetid: 5f1838c1-986e-47db-8dbc-e06976b83cf3
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 1949e2836c6677f6aec2597743142b6f7e87cf5f
ms.sourcegitcommit: 76b7653ae443a2b8eb1186b789f8503609d6453e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/04/2018
---
# <a name="compiler-error-c3385"></a>Compilerfehler C3385
'Klasse::Funktion': Eine Funktion, die ein benutzerdefiniertes DllImport-Attribut hat, kann keine Instanz einer Klasse zurückgeben.  
  
 Eine Funktion, die als Teil einer DLL-Datei definiert wird, die mit dem `DllImport` -Attribut angegeben wurde, kann keine Instanz einer Klasse zurückgeben.  
  
 Im folgenden Beispiel wird C3385 generiert:  
  
```  
// C3385.cpp  
// compile with: /clr /c  
using namespace System;  
using namespace System::Runtime::InteropServices;  
  
struct SomeStruct1 {};  
  
public ref struct Wrap {  
   [ DllImport("somedll.dll", CharSet=CharSet::Unicode) ]  
   static SomeStruct1 f1([In, Out] SomeStruct1 *pS);   // C3385  
};  
```  
