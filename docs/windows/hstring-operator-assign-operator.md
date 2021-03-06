---
title: 'Hstring:: Operator = | Microsoft Docs'
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-windows
ms.topic: reference
f1_keywords:
- corewrappers/Microsoft::WRL::Wrappers::HString::operator=
dev_langs:
- C++
ms.assetid: 8e68c1ff-bc57-4526-810e-af3c284b4e30
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- uwp
ms.openlocfilehash: 6fd1082beb6d84c5dded008e20683f7292cbc1e0
ms.sourcegitcommit: d55ac596ba8f908f5d91d228dc070dad31cb8360
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/08/2018
---
# <a name="hstringoperator-operator"></a>HString::Operator=-Operator
Verschiebt den Wert eines anderen HString-Objekts zum aktuellen HString-Objekt.  
  
## <a name="syntax"></a>Syntax  
  
```cpp  
HString& operator=(HString&& other) throw()  
```  
  
#### <a name="parameters"></a>Parameter  
 `other`  
 Ein vorhandenes HString-Objekt.  
  
## <a name="remarks"></a>Hinweise  
 Der Wert des vorhandenen `other` Objekt kopiert wird, mit dem aktuellen HString-Objekt, und klicken Sie dann die `other` -Objekt zerstört wird.  
  
## <a name="requirements"></a>Anforderungen  
 **Header:** corewrappers.h  
  
 **Namespace:** Microsoft::WRL::Wrappers  
  
## <a name="see-also"></a>Siehe auch  
 [HString-Klasse](../windows/hstring-class.md)