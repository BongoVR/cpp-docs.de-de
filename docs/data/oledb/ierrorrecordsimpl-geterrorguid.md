---
title: 'IErrorRecordsImpl:: Geterrorguid | Microsoft Docs'
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-windows
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- GetErrorGUID
- IErrorRecordsImpl.GetErrorGUID
- IErrorRecordsImpl::GetErrorGUID
dev_langs: C++
helpviewer_keywords: GetErrorGUID method
ms.assetid: 42c00755-50e5-401a-8246-adef9de5ced2
caps.latest.revision: "9"
author: mikeblome
ms.author: mblome
manager: ghogen
ms.workload:
- cplusplus
- data-storage
ms.openlocfilehash: 00709f0b796fedd050c0836d013b10b7216f7ee3
ms.sourcegitcommit: 8fa8fdf0fbb4f57950f1e8f4f9b81b4d39ec7d7a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/21/2017
---
# <a name="ierrorrecordsimplgeterrorguid"></a>IErrorRecordsImpl::GetErrorGUID
Ruft den Fehler GUID aus einer Error-Datensatzes ab.  
  
## <a name="syntax"></a>Syntax  
  
```  
  
      REFGUID GetErrorGUID(  
   ERRORINFO& rCurError   
);  
```  
  
#### <a name="parameters"></a>Parameter  
 `rCurError`  
 Ein `ERRORINFO` Datensatz in einer **IErrorInfo** Schnittstelle.  
  
## <a name="return-value"></a>Rückgabewert  
 Ein Verweis auf eine GUID für den Fehler.  
  
## <a name="requirements"></a>Anforderungen  
 **Header:** „atldb.h“  
  
## <a name="see-also"></a>Siehe auch  
 [IErrorRecordsImpl-Klasse](../../data/oledb/ierrorrecordsimpl-class.md)