---
title: Search_n (STL/CLR) | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-cli
ms.topic: reference
f1_keywords:
- cliext::search_n
dev_langs:
- C++
helpviewer_keywords:
- search_n function [STL/CLR]
ms.assetid: 34d9fd07-b160-4b1e-a632-303200740dfc
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- dotnet
ms.openlocfilehash: 8ece98fe14ac9d94585ed24f846d676bfe8c2bd9
ms.sourcegitcommit: 76b7653ae443a2b8eb1186b789f8503609d6453e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/04/2018
---
# <a name="searchn-stlclr"></a>search_n (STL/CLR)
Sucht nach der ersten Untersequenz in einem Bereich, der aus einer angegebenen Anzahl von Elementen besteht, die einen bestimmten Wert oder eine Beziehung zu diesem durch ein binäres Prädikat angegebenen Wert haben.  
  
## <a name="syntax"></a>Syntax  
  
```  
template<class _FwdIt1, class _Diff2, class _Ty> inline  
    _FwdIt1 search_n(_FwdIt1 _First1, _FwdIt1 _Last1,  
        _Diff2 _Count, const _Ty& _Val);  
template<class _FwdIt1, class _Diff2, class _Ty, class _Pr> inline  
    _FwdIt1 search_n(_FwdIt1 _First1, _FwdIt1 _Last1,  
        _Diff2 _Count, const _Ty& _Val, _Pr _Pred);  
```  
  
## <a name="remarks"></a>Hinweise  
 Diese Funktion verhält sich wie die C++-Standardbibliothek Funktion `search_n`. Weitere Informationen finden Sie unter [Search_n](../standard-library/algorithm-functions.md#search_n).  
  
## <a name="requirements"></a>Anforderungen  
 **Header:** \<Cliext-Algorithmus >  
  
 **Namespace:** Cliext  
  
## <a name="see-also"></a>Siehe auch  
 [algorithm (STL/CLR)](../dotnet/algorithm-stl-clr.md)