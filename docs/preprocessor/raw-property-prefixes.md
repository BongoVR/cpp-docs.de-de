---
title: Raw_property_prefixes | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-tools
ms.topic: reference
f1_keywords:
- raw_property_prefixes
dev_langs:
- C++
helpviewer_keywords:
- raw_property_prefixes attribute
ms.assetid: 03a0f48c-c460-4175-a762-9f7f8d84b12f
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: c1f548c9513a086dd4741a9c61c51acebebb25db
ms.sourcegitcommit: d55ac596ba8f908f5d91d228dc070dad31cb8360
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/07/2018
---
# <a name="rawpropertyprefixes"></a>raw_property_prefixes
**C++-spezifisch**  
  
 Gibt alternative Präfixe für drei Eigenschaftenmethoden an.  
  
## <a name="syntax"></a>Syntax  
  
```  
raw_property_prefixes("GetPrefix","PutPrefix","PutRefPrefix")  
```  
  
#### <a name="parameters"></a>Parameter  
 `GetPrefix`  
 Präfix für die **Propget** Methoden.  
  
 `PutPrefix`  
 Präfix für die **Propput** Methoden.  
  
 `PutRefPrefix`  
 Präfix für die **Propputref** Methoden.  
  
## <a name="remarks"></a>Hinweise  
 Standardmäßig auf niedriger Ebene **Propget**, **Propput**, und **Propputref** Methoden sind Namen mit Präfixen von Memberfunktionen verfügbar **Get_**, **Put_**, und **Putref_** bzw. Diese Präfixe sind kompatibel mit den Namen, die in den Headerdateien verwendet werden, die von MIDL generiert werden.  
  
 **Ende C++-spezifisch**  
  
## <a name="see-also"></a>Siehe auch  
 [#import-Attribute](../preprocessor/hash-import-attributes-cpp.md)   
 [#import-Direktive](../preprocessor/hash-import-directive-cpp.md)