---
title: CProviderTypes, CProviderInfo | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-data
ms.topic: reference
f1_keywords:
- m_bIsLong
- m_szLocalTypeName
- m_guidType
- m_bCaseSensitive
- m_szVersion
- m_szCreateParams
- IS_NULLABLE
- m_bAutoUniqueValue
- LITERAL_SUFFIX
- COLUMN_SIZE
- CProviderTypes
- LOCAL_TYPE_NAME
- MINIMUM_SCALE
- m_nMinScale
- m_nColumnSize
- m_szLiteralSuffix
- m_bFixedPrecScale
- m_szLiteralPrefix
- m_nMaxScale
- m_szTypeLib
- m_nDataType
- m_bUnsignedAttribute
- m_nSearchable
- m_bBestMatch
- m_szTypeName
- DATA_TYPE
- MAXIMUM_SCALE
- CProviderInfo
- FIXED_PREC_SCALE
- m_bIsNullable
- IS_LONG
dev_langs:
- C++
helpviewer_keywords:
- DATA_TYPE
- MAXIMUM_SCALE
- m_nMinScale
- m_guidType
- LOCAL_TYPE_NAME
- m_bAutoUniqueValue
- m_bBestMatch
- m_bIsLong
- m_bUnsignedAttribute
- CProviderInfo parameter class
- FIXED_PREC_SCALE
- m_nColumnSize
- m_szVersion
- CProviderTypes typedef class
- m_szCreateParams
- IS_NULLABLE
- m_bIsNullable
- m_szTypeLib
- m_szLiteralPrefix
- m_nMaxScale
- m_nDataType
- m_bCaseSensitive
- m_bFixedPrecScale
- m_nSearchable
- MINIMUM_SCALE
- m_szTypeName
- m_szLocalTypeName
- IS_LONG
- LITERAL_SUFFIX
- COLUMN_SIZE
- m_szLiteralSuffix
ms.assetid: 6f1620ff-c2f0-4f5b-931c-27b0cd2a580d
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- data-storage
ms.openlocfilehash: 5937d45a49cce84f8c9db55bd6a1b18a51b60ee6
ms.sourcegitcommit: 76b7653ae443a2b8eb1186b789f8503609d6453e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/04/2018
---
# <a name="cprovidertypes-cproviderinfo"></a>CProviderTypes, CProviderInfo
Rufen Sie die-typedefklasse **CProviderTypes** zum Implementieren der Parameterklasse **CProviderInfo**.  
  
## <a name="remarks"></a>Hinweise  
 Finden Sie unter [Schemarowset-Klassen und TypeDef-Klassen](../../data/oledb/schema-rowset-classes-and-typedef-classes.md) für Weitere Informationen zur Verwendung von typedef-Klassen.  
  
 Diese Klasse gibt die vom Datenanbieter unterstützten (Basis-) Datentypen.  
  
 Die folgende Tabelle enthält die Datenmember der Klasse und ihre entsprechenden OLE DB-Spalten. Finden Sie unter [PROVIDER_TYPES-Rowset](https://msdn.microsoft.com/en-us/library/ms709785.aspx) in der *OLE DB Programmer's Reference* für Weitere Informationen über das Schema und die Spalten.  
  
|Datenmember|OLE DB-Spalten|  
|------------------|--------------------|  
|m_szTypeName|TYPE_NAME|  
|m_nDataType|DATA_TYPE|  
|m_nColumnSize|COLUMN_SIZE|  
|m_szLiteralPrefix|LITERAL_PREFIX-ZEICHEN|  
|m_szLiteralSuffix|LITERAL_SUFFIX|  
|m_szCreateParams|CREATE_PARAMS|  
|m_bIsNullable|IS_NULLABLE|  
|m_bCaseSensitive|CASE_SENSITIVE|  
|m_nSearchable|DURCHSUCHBARE|  
|m_bUnsignedAttribute|UNSIGNED_ATTRIBUTE|  
|m_bFixedPrecScale|FIXED_PREC_SCALE|  
|m_bAutoUniqueValue|AUTO_UNIQUE_VALUE|  
|m_szLocalTypeName|LOCAL_TYPE_NAME|  
|m_nMinScale|MINIMUM_SCALE|  
|m_nMaxScale|MAXIMUM_SCALE|  
|m_guidType|GUID|  
|m_szTypeLib|TYPELIB|  
|m_szVersion|VERSION|  
|m_bIsLong|IS_LONG|  
|m_bBestMatch|BEST_MATCH|  
  
## <a name="requirements"></a>Anforderungen  
 **Header:** "atldbsch.h" Einfügen  
  
## <a name="see-also"></a>Siehe auch  
 [CRestrictions-Klasse](../../data/oledb/crestrictions-class.md)