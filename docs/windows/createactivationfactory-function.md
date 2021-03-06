---
title: CreateActivationFactory-Funktion | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-windows
ms.topic: reference
f1_keywords:
- module/Microsoft::WRL::Details::CreateActivationFactory
dev_langs:
- C++
helpviewer_keywords:
- CreateActivationFactory function
ms.assetid: a1a53e04-6757-4faf-a4c8-ecf06e43b959
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- uwp
ms.openlocfilehash: e842a13461757e26dd1aed663c590df4c1ba6c74
ms.sourcegitcommit: d55ac596ba8f908f5d91d228dc070dad31cb8360
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/08/2018
---
# <a name="createactivationfactory-function"></a>CreateActivationFactory-Funktion
Erstellt eine Instanzen der angegebenen Klasse erstellende Factory, die durch die Windows-Runtime aktiviert werden kann.  
  
## <a name="syntax"></a>Syntax  
  
```cpp  
template<typename Factory>  
   inline HRESULT STDMETHODCALLTYPE CreateActivationFactory(  
      _In_ unsigned int *flags,        _In_ const CreatorMap* entry,   
      REFIID riid,   
     _Outptr_ IUnknown **ppFactory) throw();  
  
```  
  
#### <a name="parameters"></a>Parameter  
 `flags`  
 Eine Kombination aus einem oder mehreren [RuntimeClassType](../windows/runtimeclasstype-enumeration.md) Enumerationswerte.  
  
 `entry`  
 Zeiger auf eine [CreatorMap](../windows/creatormap-structure.md) , Initialisierung und Registrierung Informationen über Parameter enthält `riid`.  
  
 `riid`  
 Verweis auf eine Schnittstellen-ID.  
  
 `ppFactory`  
 Wenn dieser Vorgang erfolgreich, einen Zeiger auf eine aktivierungsfactory ausgeführt wird.  
  
## <a name="return-value"></a>Rückgabewert  
 S_OK, wenn erfolgreich; andernfalls ein HRESULT, das den Fehler angibt.  
  
## <a name="remarks"></a>Hinweise  
 Ein Assert-Fehler wird ausgegeben, wenn Vorlagenparameter `Factory` nicht IActivationFactory-Schnittstelle abgeleitet.  
  
## <a name="requirements"></a>Anforderungen  
 **Header:** module.h  
  
 **Namespace:** Microsoft::WRL  
  
## <a name="see-also"></a>Siehe auch  
 [Microsoft::WRL::Wrappers::Details-Namespace](../windows/microsoft-wrl-wrappers-details-namespace.md)