---
title: Binary_search (STL/CLR) | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-cli
ms.topic: reference
f1_keywords:
- cliext::binary_search
dev_langs:
- C++
helpviewer_keywords:
- binary_search function [STL/CLR]
ms.assetid: 520869cc-7cd3-4c81-b439-05f042474416
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- dotnet
ms.openlocfilehash: 467efdb6c17dd6f3d9dcf8b7aa8b3495367a92f4
ms.sourcegitcommit: 76b7653ae443a2b8eb1186b789f8503609d6453e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/04/2018
---
# <a name="binarysearch-stlclr"></a>binary_search (STL/CLR)
Testet, ob ein Element in einem sortierten Bereich einem angegebenen Wert entspricht oder ihm auf eine von einem binären Prädikat angegebene Weise gleicht.  
  
## <a name="syntax"></a>Syntax  
  
```  
template<class _FwdIt, class _Ty> inline  
    bool binary_search(_FwdIt _First, _FwdIt _Last, const _Ty% _Val);  
template<class _FwdIt, class _Ty, class _Pr> inline  
    bool binary_search(_FwdIt _First, _FwdIt _Last,  
        const _Ty% _Val, _Pr _Pred);  
```  
  
## <a name="remarks"></a>Hinweise  
 Diese Funktion verhält sich wie die C++-Standardbibliothek Funktion `binary_search`. Weitere Informationen finden Sie unter [Binary_search](../standard-library/algorithm-functions.md#binary_search).  
  
## <a name="requirements"></a>Anforderungen  
 **Header:** \<Cliext-Algorithmus >  
  
 **Namespace:** Cliext  
  
## <a name="see-also"></a>Siehe auch  
 [algorithm (STL/CLR)](../dotnet/algorithm-stl-clr.md)