---
title: "CDataSource::GetProperty | Microsoft Docs"
ms.custom: ""
ms.date: "11/04/2016"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-cpp"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "ATL::CDataSource::GetProperty"
  - "ATL.CDataSource.GetProperty"
  - "CDataSource.GetProperty"
  - "CDataSource::GetProperty"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "GetProperty-Methode"
ms.assetid: 6531147c-b164-4ab5-a4a7-509634b85b4d
caps.latest.revision: 8
author: "mikeblome"
ms.author: "mblome"
manager: "ghogen"
caps.handback.revision: 8
---
# CDataSource::GetProperty
[!INCLUDE[vs2017banner](../../assembler/inline/includes/vs2017banner.md)]

Gibt den Wert einer angegebenen Eigenschaft für das verbundene Datenquellenobjekt zurück.  
  
## Syntax  
  
```  
  
      HRESULT GetProperty(   
   const GUID& guid,   
   DBPROPID propid,   
   VARIANT* pVariant    
) const throw( );  
```  
  
#### Parameter  
 `guid`  
 \[in\] Eine GUID, die dem Eigenschaftensatz angegeben, dass der Eigenschaft zurückgibt.  
  
 `propid`  
 \[in\] Eigenschafts\-ID, damit die Eigenschaft zurückgegeben wird.  
  
 *pVariant*  
 \[out\] Ein Zeiger an eine Variante, in der **GetProperty** der Wert der Eigenschaft zurückgibt.  
  
## Rückgabewert  
 Standard\- `HRESULT`.  
  
## Hinweise  
 Um mehrere Eigenschaften abzurufen, verwenden Sie [GetProperties](../../data/oledb/cdatasource-getproperties.md).  
  
## Anforderungen  
 **Header:** atldbcli.h  
  
## Siehe auch  
 [CDataSource\-Klasse](../../data/oledb/cdatasource-class.md)