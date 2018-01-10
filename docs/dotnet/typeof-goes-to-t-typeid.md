---
title: 'Typeof wird zu t:: typeid | Microsoft Docs'
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-windows
ms.tgt_pltfrm: 
ms.topic: article
dev_langs: C++
helpviewer_keywords:
- typeid operator
- __typeof keyword
- typeid keyword [C++]
ms.assetid: 6a0d35a7-7a1a-4070-b187-cff37cfdc205
caps.latest.revision: "8"
author: mikeblome
ms.author: mblome
manager: ghogen
ms.workload:
- cplusplus
- dotnet
ms.openlocfilehash: 09ec4aef4c8bc68f8a808193b30d86b8519ba881
ms.sourcegitcommit: 8fa8fdf0fbb4f57950f1e8f4f9b81b4d39ec7d7a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/21/2017
---
# <a name="typeof-goes-to-ttypeid"></a>typeof wird zu T::typeid
Die `typeof` Operator wird in Managed Extensions für C++ durch Ersetzen der `typeid` -Schlüsselwort in Visual C++.  
  
 In Managed Extensions die `__typeof()` Operator gibt das zugeordnete `Type*` Objekt, wenn der Name eines verwalteten Typs übergeben. Zum Beispiel:  
  
```  
// Creates and initializes a new Array instance.  
Array* myIntArray =   
   Array::CreateInstance( __typeof(Int32), 5 );  
```  
  
 In der neuen Syntax `__typeof` wurde ersetzt durch eine weitere Form der `typeid` zurückgegeben, die eine `Type^` Wenn ein verwalteter Typ angegeben wird.  
  
```  
// Creates and initializes a new Array instance.  
Array^ myIntArray =   
   Array::CreateInstance( Int32::typeid, 5 );  
```  
  
## <a name="see-also"></a>Siehe auch  
 [Allgemeine Sprachänderungen (C + c++ / CLI)](../dotnet/general-language-changes-cpp-cli.md)   
 [typeid](../windows/typeid-cpp-component-extensions.md)