---
title: 'Activationfactory:: Release-Methode | Microsoft Docs'
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-windows
ms.topic: reference
f1_keywords:
- module/Microsoft::WRL::ActivationFactory::Release
dev_langs:
- C++
helpviewer_keywords:
- Release method
ms.assetid: 5bc25ff0-ee3c-4a2d-a9b6-2d8f158033ad
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- uwp
ms.openlocfilehash: f2617df132f31d63379a3bd27a49409b1599a090
ms.sourcegitcommit: d55ac596ba8f908f5d91d228dc070dad31cb8360
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/08/2018
---
# <a name="activationfactoryrelease-method"></a>ActivationFactory::Release-Methode
Dekrementiert den Verweiszähler des aktuellen ActivationFactory-Objekts.  
  
## <a name="syntax"></a>Syntax  
  
```  
STDMETHOD_(  
   ULONG,  
   Release  
)();  
```  
  
## <a name="return-value"></a>Rückgabewert  
 „S_OK“ im Erfolgsfall, andernfalls ein HRESULT, das den Fehler beschreibt.  
  
## <a name="requirements"></a>Anforderungen  
 **Header:** module.h  
  
 **Namespace:** Microsoft::WRL  
  
## <a name="see-also"></a>Siehe auch  
 [ActivationFactory-Klasse](../windows/activationfactory-class.md)