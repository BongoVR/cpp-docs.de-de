---
title: "IRowsetChangeImpl::DeleteRows | Microsoft Docs"
ms.custom: ""
ms.date: "11/04/2016"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-cpp"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "ATL.IRowsetChangeImpl.DeleteRows"
  - "ATL::IRowsetChangeImpl::DeleteRows"
  - "IRowsetChangeImpl.DeleteRows"
  - "DeleteRows"
  - "IRowsetChangeImpl::DeleteRows"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "DeleteRows-Methode"
ms.assetid: 462ad4f1-3b2a-4134-9733-be65708aa1d9
caps.latest.revision: 9
author: "mikeblome"
ms.author: "mblome"
manager: "ghogen"
caps.handback.revision: 9
---
# IRowsetChangeImpl::DeleteRows
[!INCLUDE[vs2017banner](../../assembler/inline/includes/vs2017banner.md)]

Zeilen löschen aus dem Rowset.  
  
## Syntax  
  
```  
  
      STDMETHOD ( DeleteRows )(  
   HCHAPTER /* hReserved */,  
   DBCOUNTITEM cRows,  
   const HROW rghRows[],  
   DBROWSTATUS rgRowStatus[]   
);  
```  
  
#### Parameter  
 Siehe [IRowsetChange::DeleteRows](https://msdn.microsoft.com/en-us/library/ms724362.aspx) in der *OLE* DB\-Programmierreferenz.  
  
## Anforderungen  
 **Header:** atldb.h  
  
## Siehe auch  
 [IRowsetChangeImpl\-Klasse](../../data/oledb/irowsetchangeimpl-class.md)