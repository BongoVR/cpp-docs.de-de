---
title: Compilerfehler C3394 | Microsoft Docs
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- cpp-tools
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- C3394
dev_langs:
- C++
helpviewer_keywords:
- C3394
ms.assetid: 4e025d79-27ba-43c8-b0d9-839ecef98126
caps.latest.revision: 
author: corob-msft
ms.author: corob
manager: ghogen
ms.workload:
- cplusplus
ms.openlocfilehash: 051b4704034e23c24dc10b75b40d97ef27e99203
ms.sourcegitcommit: 8fa8fdf0fbb4f57950f1e8f4f9b81b4d39ec7d7a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/21/2017
---
# <a name="compiler-error-c3394"></a>Compilerfehler C3394
Syntaxfehler in Einschränkungsklausel: „identifier“ wurde gefunden, es wurde jedoch ein Typ erwartet.  
  
 Eine Einschränkung wurde nicht ordnungsgemäß formatiert.  Weitere Informationen finden Sie unter [Einschränkungen für generische Typparameter (C + c++ / CLI)](../../windows/constraints-on-generic-type-parameters-cpp-cli.md).  
  
## <a name="example"></a>Beispiel  
 Im folgenden Beispiel wird C3394 generiert:  
  
```  
// C3394.cpp  
// compile with: /clr /c  
ref class MyClass {};  
ref class R {  
   generic<typename T>  
   where T : static   // C3394  
   // try the following line instead  
   // where T : MyClass  
   void f() {}  
};  
```