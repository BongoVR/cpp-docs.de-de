---
title: Compilerfehler C3291 | Microsoft Docs
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- cpp-tools
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- C3291
dev_langs:
- C++
helpviewer_keywords:
- C3291
ms.assetid: ed2e9f89-8dbc-4387-bc26-cc955e840858
caps.latest.revision: 5
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
ms.translationtype: Machine Translation
ms.sourcegitcommit: 0d9cbb01d1ad0f2ea65d59334cb88140ef18fce0
ms.openlocfilehash: 231ccf64776c608131878caf9bdbe7e463903f6b
ms.contentlocale: de-de
ms.lasthandoff: 04/12/2017

---
# <a name="compiler-error-c3291"></a>Compilerfehler C3291
"default": Kann nicht der Name einer trivial-Eigenschaft sein.  
  
 Eine trivial-Eigenschaft kann nicht als `default`benannt werden. Finden Sie unter [Eigenschaft](../../windows/property-cpp-component-extensions.md) für Weitere Informationen.  
  
## <a name="example"></a>Beispiel  
 Im folgenden Beispiel wird C3291 generiert:  
  
```  
// C3291.cpp  
// compile with: /clr /c  
ref struct C {  
   property System::String ^ default;   // C3291  
   property System::String ^ Default;   // OK  
};  
```
