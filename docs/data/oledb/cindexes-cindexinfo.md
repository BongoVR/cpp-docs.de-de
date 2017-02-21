---
title: "CIndexes, CIndexInfo | Microsoft Docs"
ms.custom: ""
ms.date: "11/04/2016"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-cpp"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "INITIAL_SIZE"
  - "NULL_COLLATION"
  - "m_szFilterCondition"
  - "m_bPrimaryKey"
  - "m_szTableSchema"
  - "m_bSortBookmarks"
  - "m_szIndexSchema"
  - "m_nColumnPropID"
  - "ORDINAL_POSITION"
  - "INDEX_CATALOG"
  - "m_nOrdinalPosition"
  - "COLUMN_GUID"
  - "m_bAutoUpdate"
  - "m_nNullCollation"
  - "CLUSTERED"
  - "NULLS"
  - "m_szColumnName"
  - "m_nFillFactor"
  - "m_nPages"
  - "INDEX_NAME"
  - "m_szTableCatalog"
  - "m_szIndexName"
  - "m_szIndexCatalog"
  - "m_nCardinality"
  - "m_nInitialSize"
  - "m_bUnique"
  - "COLUMN_PROPID"
  - "m_guidColumn"
  - "m_nNulls"
  - "m_szTableName"
  - "FILL_FACTOR"
  - "m_nType"
  - "m_bClustered"
  - "COLLATION"
  - "FILTER_CONDITION"
  - "m_nCollation"
  - "CIndexes"
  - "INDEX_SCHEMA"
  - "CIndexInfo"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "CIndexes-Typedefklasse"
  - "CIndexInfo-Parameterklasse"
  - "CLUSTERED"
  - "COLUMN_GUID"
  - "COLUMN_NAME"
  - "COLUMN_PROPID"
  - "FILL_FACTOR"
  - "FILTER_CONDITION"
  - "INDEX_CATALOG"
  - "INDEX_NAME"
  - "INDEX_SCHEMA"
  - "INITIAL_SIZE"
  - "m_bAutoUpdate"
  - "m_bClustered"
  - "m_bPrimaryKey"
  - "m_bSortBookmarks"
  - "m_bUnique"
  - "m_guidColumn"
  - "m_nCardinality"
  - "m_nCollation"
  - "m_nColumnPropID"
  - "m_nFillFactor"
  - "m_nInitialSize"
  - "m_nNullCollation"
  - "m_nNulls"
  - "m_nOrdinalPosition"
  - "m_nPages"
  - "m_nType"
  - "m_szColumnName"
  - "m_szFilterCondition"
  - "m_szIndexCatalog"
  - "m_szIndexName"
  - "m_szIndexSchema"
  - "m_szTableCatalog"
  - "m_szTableName"
  - "m_szTableSchema"
  - "NULL_COLLATION"
  - "NULLS"
  - "ORDINAL_POSITION"
  - "TABLE_CATALOG"
  - "TABLE_NAME"
  - "TABLE_SCHEMA"
ms.assetid: 592fa773-fd23-4332-8d47-d76101f9ddd7
caps.latest.revision: 6
author: "mikeblome"
ms.author: "mblome"
manager: "ghogen"
caps.handback.revision: 6
---
# CIndexes, CIndexInfo
[!INCLUDE[vs2017banner](../../assembler/inline/includes/vs2017banner.md)]

Rufen Sie die typedef\-Klasse **CIndexes** auf, um dessen Parameterklasse **CIndexInfo** zu implementieren.  
  
## Hinweise  
 Siehe [Schemarowset\-Klassen und typedef\-Klassen](../../data/oledb/schema-rowset-classes-and-typedef-classes.md) weitere Informationen zur Verwendung von Informationen.  
  
 Diese Klasse identifiziert die Indizes, definiert im Katalog, die von einem bestimmten Benutzers befindlichen.  
  
 Die folgende Tabelle zeigt die Klassendatenmember und ihre entsprechenden OLE DB Spalten auf.  Siehe [INDIZES Rowset](https://msdn.microsoft.com/en-us/library/ms709712.aspx) in *der OLE DB\-Programmierreferenz* weitere Informationen über das Schema und Spalten.  
  
|Datenmember|OLE DB\-Spalten|  
|-----------------|---------------------|  
|m\_szTableCatalog|TABLE\_CATALOG|  
|m\_szTableSchema|TABLE\_SCHEMA|  
|m\_szTableName|TABLE\_NAME|  
|m\_szIndexCatalog|INDEX\_CATALOG|  
|m\_szIndexSchema|INDEX\_SCHEMA|  
|m\_szIndexName|INDEX\_NAME|  
|m\_bPrimaryKey|PRIMARY\_KEY|  
|m\_bUnique|UNIQUE|  
|m\_bClustered|CLUSTERED|  
|m\_nType|TYPE|  
|m\_nFillFactor|FILL\_FACTOR|  
|m\_nInitialSize|INITIAL\_SIZE|  
|m\_nNulls|NULLS|  
|m\_bSortBookmarks|SORT\_BOOKMARKS|  
|m\_bAutoUpdate|AUTO\_UPDATE|  
|m\_nNullCollation|NULL\_COLLATION|  
|m\_nOrdinalPosition|ORDINAL\_POSITION|  
|m\_szColumnName|COLUMN\_NAME|  
|m\_guidColumn|COLUMN\_GUID|  
|m\_nColumnPropID|COLUMN\_PROPID|  
|m\_nCollation|COLLATION|  
|m\_nCardinality|CARDINALITY|  
|m\_nPages|PAGES|  
|m\_szFilterCondition|FILTER\_CONDITION|  
  
## Voraussetzungen  
 **Header:**  atldbsch.h  
  
## Siehe auch  
 [CRestrictions\-Klasse](../../data/oledb/crestrictions-class.md)