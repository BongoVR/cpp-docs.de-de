---
title: _com_ptr_t::QueryInterface | Microsoft Docs
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- cpp-language
ms.tgt_pltfrm: 
ms.topic: language-reference
f1_keywords:
- _com_ptr_t::QueryInterface
- _com_ptr_t.QueryInterface
dev_langs:
- C++
helpviewer_keywords:
- QueryInterface method [C++]
ms.assetid: d03292f1-6b02-40db-9756-8b0837a97319
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
ms.openlocfilehash: 6b5c8fb9ca1d628b178c19b677b90f17cc992373
ms.contentlocale: de-de
ms.lasthandoff: 09/25/2017

---
# <a name="comptrtqueryinterface"></a>_com_ptr_t::QueryInterface
**Microsoft-spezifisch**  
  
 Ruft die `QueryInterface` Memberfunktion von **IUnknown** für den gekapselten Schnittstellenzeiger auf.  
  
## <a name="syntax"></a>Syntax  
  
```  
  
      template<typename _InterfaceType> HRESULT QueryInterface (  
   const IID& iid,  
   _InterfaceType*& p   
) throw ( );  
template<typename _InterfaceType> HRESULT QueryInterface (  
   const IID& iid,  
   _InterfaceType** p  
) throw( );  
```  
  
#### <a name="parameters"></a>Parameter  
 `iid`  
 **IID** eines Schnittstellenzeigers.  
  
 `p`  
 Nicht formatierter Schnittstellenzeiger.  
  
## <a name="remarks"></a>Hinweise  
 Aufrufe **IUnknown:: QueryInterface** für den gekapselten Schnittstellenzeiger mit dem angegebenen **IID** und gibt den resultierenden unformatierten Schnittstellenzeiger in `p`. Diese Routine gibt `HRESULT` zurück, um einen Erfolg oder Fehler anzuzeigen.  
  
 **Ende Microsoft-spezifisch**  
  
## <a name="see-also"></a>Siehe auch  
 [_com_ptr_t-Klasse](../cpp/com-ptr-t-class.md)
