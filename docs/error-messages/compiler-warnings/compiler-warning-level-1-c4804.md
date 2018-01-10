---
title: Compilerwarnung (Stufe 1) C4804 | Microsoft Docs
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-tools
ms.tgt_pltfrm: 
ms.topic: error-reference
f1_keywords: C4804
dev_langs: C++
helpviewer_keywords: C4804
ms.assetid: 069e8f44-3ef6-43bb-8524-4116fc6eea83
caps.latest.revision: "7"
author: corob-msft
ms.author: corob
manager: ghogen
ms.workload: cplusplus
ms.openlocfilehash: 08ca44f1d272207f287cca2d1e9bb147b0591fe1
ms.sourcegitcommit: 8fa8fdf0fbb4f57950f1e8f4f9b81b4d39ec7d7a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/21/2017
---
# <a name="compiler-warning-level-1-c4804"></a>Compilerwarnung (Stufe 1) C4804
'Operation': unsichere Verwendung des Typs "Bool", Vorgang  
  
 Diese Warnung gilt für bei der Verwendung einer `bool` Variable oder ein Wert in der erwarteten Weise. C4804 wird beispielsweise generiert, wenn Sie Operatoren wie z. B. der negativen unäre Operator verwenden (**-**) oder dem Komplementoperator (`~`). Der Compiler wertet den Ausdruck.  
  
## <a name="example"></a>Beispiel  
 Im folgenden Beispiel wird C4804 generiert:  
  
```  
// C4804.cpp  
// compile with: /W1  
  
int main()  
{  
   bool i = true;  
   if (-i)   // C4804, remove the '-' to resolve  
   {  
      i = false;  
   }  
}  
```