---
title: Compilerfehler C3347 | Microsoft Docs
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- devlang-cpp
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- C3347
dev_langs:
- C++
helpviewer_keywords:
- C3347
ms.assetid: e939ad29-0b78-4681-9618-9bdae5675cee
caps.latest.revision: 8
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
ms.sourcegitcommit: 0d9cbb01d1ad0f2ea65d59334cb88140ef18fce0
ms.openlocfilehash: d20934732a3b04bcd49485c3e0ba5b3562b147c5
ms.lasthandoff: 04/12/2017

---
# <a name="compiler-error-c3347"></a>Compilerfehler C3347
'Arg': Das erforderliche Argument ist nicht im Attribut 'idl_modules' festgelegt.  
  
 Ein erforderliches Argument wurde nicht übergeben, um die [Idl_module](../../windows/idl-module.md) Attribut.  
  
 Im folgenden Beispiel wird C3347 generiert:  
  
```  
// C3347.cpp  
// compile with: /c  
[module(name="xx")];  
  
[idl_module(dllname="x")];    // C3347  
// try the following line instead  
// [idl_module(name="test", dllname="x")];  
```
