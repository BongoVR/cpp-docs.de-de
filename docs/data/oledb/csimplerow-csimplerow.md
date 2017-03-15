---
title: "CSimpleRow::CSimpleRow | Microsoft Docs"
ms.custom: ""
ms.date: "11/04/2016"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-cpp"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "CSimpleRow"
  - "ATL::CSimpleRow::CSimpleRow"
  - "CSimpleRow.CSimpleRow"
  - "ATL.CSimpleRow.CSimpleRow"
  - "CSimpleRow::CSimpleRow"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "CSimpleRow-Klasse, Konstruktor"
ms.assetid: 3968a36c-b8bb-48df-bd06-3956e64b0842
caps.latest.revision: 8
author: "mikeblome"
ms.author: "mblome"
manager: "ghogen"
caps.handback.revision: 8
---
# CSimpleRow::CSimpleRow
[!INCLUDE[vs2017banner](../../assembler/inline/includes/vs2017banner.md)]

Der \-Konstruktor.  
  
## Syntax  
  
```  
  
      CSimpleRow(  
   DBCOUNTITEM iRowsetCur   
);  
```  
  
#### Parameter  
 `iRowsetCur`  
 \[in\] Index dem aktuellen Rowset.  
  
## Hinweise  
 Legt [m\_iRowset](../../data/oledb/csimplerow-m-irowset.md) auf `iRowsetCur` fest.  
  
## Anforderungen  
 **Header:** atldb.h  
  
## Siehe auch  
 [CSimpleRow\-Klasse](../../data/oledb/csimplerow-class.md)