---
title: _com_error::HRESULTToWCode | Microsoft Docs
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- cpp-language
ms.tgt_pltfrm: 
ms.topic: language-reference
f1_keywords:
- _com_error::HRESULTToWCode
dev_langs:
- C++
helpviewer_keywords:
- HRESULTToWCode method [C++]
ms.assetid: ff3789f5-1047-41a0-b7e3-86dd8f638dba
caps.latest.revision: 6
author: mikeblome
ms.author: mblome
manager: ghogen
translation.priority.ht:
- cs-cz
- de-de
- es-es
- fr-fr
- it-it
- ja-jp
- ko-kr
- pl-pl
- pt-br
- ru-ru
- tr-tr
- zh-cn
- zh-tw
ms.translationtype: HT
ms.sourcegitcommit: 6ffef5f51e57cf36d5984bfc43d023abc8bc5c62
ms.openlocfilehash: 296c6f43c1bc840ae13bdf4ad355d7f41e2cc3fd
ms.contentlocale: de-de
ms.lasthandoff: 09/25/2017

---
# <a name="comerrorhresulttowcode"></a>_com_error::HRESULTToWCode
**Microsoft-spezifisch**  
  
 Ordnet 32-Bit-`HRESULT` dem 16-Bit-`wCode` zu.  
  
## <a name="syntax"></a>Syntax  
  
```  
  
      static WORD HRESULTToWCode(  
   HRESULT hr   
) throw( );  
```  
  
#### <a name="parameters"></a>Parameter  
 `hr`  
 Die 32-Bit- `HRESULT` 16-Bit zugeordnet werden `wCode`.  
  
## <a name="return-value"></a>Rückgabewert  
 16-Bit- `wCode` zugeordnet, die von der 32-Bit- `HRESULT`.  
  
## <a name="remarks"></a>Hinweise  
 Finden Sie unter [_com_error:: wcode](../cpp/com-error-wcode.md) für Weitere Informationen.  
  
 **Ende Microsoft-spezifisch**  
  
## <a name="see-also"></a>Siehe auch  
 [_com_error:: wcode](../cpp/com-error-wcode.md)   
 [_com_error::WCodeToHRESULT](../cpp/com-error-wcodetohresult.md)   
 [_com_error-Klasse](../cpp/com-error-class.md)
