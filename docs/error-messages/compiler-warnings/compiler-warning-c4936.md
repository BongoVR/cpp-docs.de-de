---
title: Compiler-Warnung C4936 | Microsoft-Dokumentation
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- devlang-csharp
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- C4936
dev_langs:
- C++
helpviewer_keywords:
- C4936
ms.assetid: 6676de35-bf1b-4d0b-a70f-b5734130336c
caps.latest.revision: 12
author: corob-msft
ms.author: corob
manager: ghogen
translation.priority.ht:
- de-de
- es-es
- fr-fr
- it-it
- ja-jp
- ko-kr
- ru-ru
- zh-cn
- zh-tw
translation.priority.mt:
- cs-cz
- pl-pl
- pt-br
- tr-tr
translationtype: Machine Translation
ms.sourcegitcommit: cc82b83860786ffc3f0aee73ede18ecadef16a7a
ms.openlocfilehash: 58d702067c186eeeea94768a03836b64577961ca
ms.lasthandoff: 02/24/2017

---
# <a name="compiler-warning-c4936"></a>Compilerwarnung C4936
__declspec wird nur bei einer Kompilierung mit /clr oder /clr:pure unterstützt.  
  
 Die **/CLR: pure** -Compileroption in Visual Studio 2015 veraltet ist.  
  
 Ein `__declspec` -Modifizierer wurde verwendet, die aber `__declspec` Modifizierer ist nur gültig, wenn Sie mit einem kompiliert die [/CLR](../../build/reference/clr-common-language-runtime-compilation.md) Optionen.  
  
 Weitere Informationen finden Sie unter [Appdomain](../../cpp/appdomain.md) und [Prozess](../../cpp/process.md).  
  
 C4936 wird immer als Fehler ausgegeben.  Sie können mit C4936 Deaktivieren der [Warnung](../../preprocessor/warning.md) Pragma.  
  
 Im folgenden Beispiel wird C4936 generiert:  
  
```  
// C4936.cpp  
// compile with: /c  
// #pragma warning (disable : 4936)  
__declspec(process) int i;   // C4936  
__declspec(appdomain) int j;   // C4936  
```
