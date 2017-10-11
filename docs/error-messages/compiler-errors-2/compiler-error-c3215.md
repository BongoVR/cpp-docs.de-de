---
title: Compilerfehler C3215 | Microsoft Docs
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- cpp-tools
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- C3215
dev_langs:
- C++
helpviewer_keywords:
- C3215
ms.assetid: d0d16007-8885-42e0-b086-2d3a61f348c5
caps.latest.revision: 9
author: corob-msft
ms.author: corob
manager: ghogen
ms.translationtype: MT
ms.sourcegitcommit: 35b46e23aeb5f4dbfd2a0dd44b906389dd5bfc88
ms.openlocfilehash: e4a649c01762b8a113e928bb63ffe293f86d21c3
ms.contentlocale: de-de
ms.lasthandoff: 10/10/2017

---
# <a name="compiler-error-c3215"></a>Compilerfehler C3215
"Typ1": Der generische Typparameter wird bereits von "Typ2" eingeschränkt.  
  
 Eine Einschränkung wurde mehrmals angegeben.  
  
 Weitere Informationen zu Generika finden Sie unter [Generics](../../windows/generics-cpp-component-extensions.md).  
  
 Im folgenden Beispiel wird C3215 generiert:  
  
```  
// C3215.cpp  
// compile with: /clr  
interface struct A {};  
  
generic <class T>  
where T : A,A  
ref class C {};   // C3215  
```  
  
 Mögliche Lösung:  
  
```  
// C3215b.cpp  
// compile with: /clr /c  
interface struct A {};  
  
generic <class T>  
where T : A  
ref class C {};  
```
