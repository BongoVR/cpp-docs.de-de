---
title: Iid_is | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-windows
ms.topic: reference
f1_keywords:
- vc-attr.iid_is
dev_langs:
- C++
helpviewer_keywords:
- iid_is attribute
ms.assetid: 2f9b42a9-7130-4b08-9b1e-0d5d360e10ff
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- uwp
ms.openlocfilehash: f9ef3a14211e223b9902dc9843639d217ceaf1b3
ms.sourcegitcommit: d55ac596ba8f908f5d91d228dc070dad31cb8360
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/08/2018
---
# <a name="iidis"></a>iid_is
Gibt die IID der COM-Schnittstelle, die einen Schnittstellenzeiger verweist.  
  
## <a name="syntax"></a>Syntax  
  
```  
  
      [ iid_is(  
   "expression"  
) ]  
```  
  
#### <a name="parameters"></a>Parameter  
 *Ausdruck*  
 Ein Ausdruck der C#-Sprache, der eine IID einer COM-Schnittstelle angibt, auf einen Schnittstellenzeiger verweist.  
  
## <a name="remarks"></a>Hinweise  
 Die **Iid_is** C++-Attribut hat die gleiche Funktionalität wie die [Iid_is](http://msdn.microsoft.com/library/windows/desktop/aa367044) MIDL-Attribut.  
  
## <a name="example"></a>Beispiel  
 Der folgende Code zeigt die Verwendung von **Iid_is**:  
  
```  
// cpp_attr_ref_iid_is.cpp  
// compile with: /LD  
#include "wtypes.h"  
#include "unknwn.h"  
[dispinterface, uuid("00000000-0000-0000-0000-000000000001")]  
__interface IFireTabCtrl : IDispatch  
{  
   [id(1)] HRESULT CreateInstance([in] REFIID riid,[out, iid_is("riid")]   
   IUnknown ** ppvObject);  
};  
  
[module(name="ATLFIRELib")];  
```  
  
## <a name="requirements"></a>Anforderungen  
  
### <a name="attribute-context"></a>Attributkontext  
  
|||  
|-|-|  
|**Betrifft**|Schnittstellenparameter,-Datenmember|  
|**Wiederholbar**|Nein|  
|**Erforderliche Attribute**|Keiner|  
|**Ungültige Attribute**|Keiner|  
  
 Weitere Informationen finden Sie unter [Attributkontexte](../windows/attribute-contexts.md).  
  
## <a name="see-also"></a>Siehe auch  
 [IDL-Attribute](../windows/idl-attributes.md)   
 [Parameterattribute](../windows/parameter-attributes.md)   
