---
title: Schwerwiegender Fehler C1022 | Microsoft Docs
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- cpp-tools
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- C1022
dev_langs:
- C++
helpviewer_keywords:
- C1022
ms.assetid: edada720-dc73-49bc-bd93-a7945a316312
caps.latest.revision: 9
author: corob-msft
ms.author: corob
manager: ghogen
ms.translationtype: MT
ms.sourcegitcommit: 35b46e23aeb5f4dbfd2a0dd44b906389dd5bfc88
ms.openlocfilehash: 8215a0a505503c9a4040439629aea59926baf27e
ms.contentlocale: de-de
ms.lasthandoff: 10/09/2017

---
# <a name="fatal-error-c1022"></a>Schwerwiegender Fehler C1022
#endif erwartet  
  
 Eine `#if`-, `#ifdef`- oder `#ifndef` -Direktive weist keine übereinstimmende `#endif` -Direktive auf. Stellen Sie sicher, dass jedes `#if`, `#ifdef`oder `#ifndef` über ein übereinstimmendes `#endif`verfügt.  
  
 Im folgenden Beispiel wird C1022 generiert:  
  
```  
// C1022.cpp  
#define true 1  
  
#if (true)  
#else   
#else    // C1022  
```  
  
 Mögliche Lösung:  
  
```  
// C1022b.cpp  
// compile with: /c  
#define true 1  
  
#if (true)  
#else   
#endif  
```
