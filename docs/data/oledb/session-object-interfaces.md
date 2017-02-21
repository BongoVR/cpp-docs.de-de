---
title: "Sitzungsobjekt-Schnittstellen | Microsoft Docs"
ms.custom: ""
ms.date: "11/04/2016"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-cpp"
ms.tgt_pltfrm: ""
ms.topic: "article"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "Schnittstellen, Liste"
  - "Schnittstellen, Sitzungsobjekt"
  - "OLE DB-Anbietervorlagen, Objektschnittstelle"
  - "Sitzungsobjekte [OLE DB]"
  - "Sitzungsobjekte [OLE DB], Schnittstellen"
ms.assetid: ac01a958-6dde-4bd7-8b63-94459e488335
caps.latest.revision: 7
author: "mikeblome"
ms.author: "mblome"
manager: "ghogen"
caps.handback.revision: 7
---
# Sitzungsobjekt-Schnittstellen
[!INCLUDE[vs2017banner](../../assembler/inline/includes/vs2017banner.md)]

In der folgenden Tabelle sind die erforderlichen und optionalen Schnittstellen aufgeführt, die in OLE DB für Sitzungsobjekte definiert sind.  
  
|Schnittstelle|Erforderlich?|Durch OLE DB\-Vorlagen implementiert?|  
|-------------------|-------------------|-------------------------------------------|  
|[\<caps:sentence id\="tgt5" sentenceid\="84bd345ed51e4b9228da4eebd9ca3bd6" class\="tgtSentence"\>IGetDataSource\<\/caps:sentence\>](https://msdn.microsoft.com/en-us/library/ms709721.aspx)|Erforderlich|ja|  
|[\<caps:sentence id\="tgt8" sentenceid\="1857d9ee3f90b714f7d456a2712c0041" class\="tgtSentence"\>IOpenRowset\<\/caps:sentence\>](https://msdn.microsoft.com/en-us/library/ms716946.aspx)|Erforderlich|ja|  
|[\<caps:sentence id\="tgt11" sentenceid\="5a404cb65e2c2338db2e80978a9e67a2" class\="tgtSentence"\>ISessionProperties\<\/caps:sentence\>](https://msdn.microsoft.com/en-us/library/ms713721.aspx)|Erforderlich|ja|  
|[\<caps:sentence id\="tgt14" sentenceid\="713bcc50c078a14a6fb0a671b416510b" class\="tgtSentence"\>IAlterIndex\<\/caps:sentence\>](https://msdn.microsoft.com/en-us/library/ms714943.aspx)|Optional|nein|  
|[\<caps:sentence id\="tgt17" sentenceid\="24fbee76531423a4d09802565cd11362" class\="tgtSentence"\>IAlterTable\<\/caps:sentence\>](https://msdn.microsoft.com/en-us/library/ms719764.aspx)|Optional|nein|  
|[\<caps:sentence id\="tgt20" sentenceid\="b692103b1e1bfc19e7c5b54e42ba6f33" class\="tgtSentence"\>IBindResource\<\/caps:sentence\>](https://msdn.microsoft.com/en-us/library/ms714936.aspx)|Optional|nein|  
|[\<caps:sentence id\="tgt23" sentenceid\="437b598116cf64157b7c6f6d0ebe8095" class\="tgtSentence"\>ICreateRow\<\/caps:sentence\>](https://msdn.microsoft.com/en-us/library/ms716832.aspx)|Optional|nein|  
|[\<caps:sentence id\="tgt26" sentenceid\="336cdaf38e70da667eae9ab8a6d3c9ff" class\="tgtSentence"\>IDBCreateCommand\<\/caps:sentence\>](https://msdn.microsoft.com/en-us/library/ms711625.aspx)|Optional|ja|  
|[\<caps:sentence id\="tgt29" sentenceid\="7cffd2da39279c8fb46f585db4ebcc91" class\="tgtSentence"\>IDBSchemaRowset\<\/caps:sentence\>](https://msdn.microsoft.com/en-us/library/ms713686.aspx)|Optional|ja|  
|[\<caps:sentence id\="tgt32" sentenceid\="b8d3ac9198a7bc6dca13799dec75e132" class\="tgtSentence"\>IIndexDefinition\<\/caps:sentence\>](https://msdn.microsoft.com/en-us/library/ms711593.aspx)|Optional|nein|  
|[\<caps:sentence id\="tgt35" sentenceid\="130702210bcc45e1afd88b1f2aae1a0b" class\="tgtSentence"\>ISupportErrorInfo\<\/caps:sentence\>](https://msdn.microsoft.com/en-us/library/ms715816.aspx)|Optional|ja|  
|[\<caps:sentence id\="tgt38" sentenceid\="9335c6109fea1ca1e5e74ee87ff58c45" class\="tgtSentence"\>ITableCreation\<\/caps:sentence\>](https://msdn.microsoft.com/en-us/library/ms713639.aspx)|Optional|nein|  
|[\<caps:sentence id\="tgt41" sentenceid\="568789fddb5a6849d3b1f59b42254292" class\="tgtSentence"\>ITableDefinition\<\/caps:sentence\>](https://msdn.microsoft.com/en-us/library/ms714277.aspx)|Optional|nein|  
|[\<caps:sentence id\="tgt44" sentenceid\="9a9807a7d8d31a6c0de805a5f28111d4" class\="tgtSentence"\>ITableDefinitionWithConstraints\<\/caps:sentence\>](https://msdn.microsoft.com/en-us/library/ms720947.aspx)|Optional|nein|  
|[\<caps:sentence id\="tgt47" sentenceid\="f5097e646bb93cceb560c38e13953a89" class\="tgtSentence"\>ITransaction\<\/caps:sentence\>](https://msdn.microsoft.com/en-us/library/ms723053.aspx)|Optional|nein|  
|[\<caps:sentence id\="tgt50" sentenceid\="160d543e4608ffb947e7e98bc94d2dd6" class\="tgtSentence"\>ITransactionJoin\<\/caps:sentence\>](https://msdn.microsoft.com/en-us/library/ms718071.aspx)|Optional|nein|  
|[\<caps:sentence id\="tgt53" sentenceid\="06c2b3c9bbd28371734b84bf68130381" class\="tgtSentence"\>ITransactionLocal\<\/caps:sentence\>](https://msdn.microsoft.com/en-us/library/ms714893.aspx)|Optional|nein|  
|[\<caps:sentence id\="tgt56" sentenceid\="3cf0b0ed75f511b15ab0f34f30e50a04" class\="tgtSentence"\>ITransactionObject\<\/caps:sentence\>](https://msdn.microsoft.com/en-us/library/ms713659.aspx)|Optional|nein|  
  
 Durch das Sitzungsobjekt wird ein Rowsetobjekt erstellt.  Wenn der Anbieter Befehle unterstützt, wird durch die Sitzung auch ein Befehlsobjekt \(`CCommand` zur Implementierung von OLE DB\-**TCommand**\) erstellt.  Das Befehlsobjekt implementiert die `ICommand`\-Schnittstelle und verwendet die `ICommand::Execute`\-Methode, um Befehle für das Rowset auszuführen, wie in der folgenden Abbildung dargestellt.  
  
 ![Konzeptionelles Diagramm zu Anbietern](../../data/oledb/media/vc4u551.png "vc4U551")  
  
## Siehe auch  
 [Architektur von OLE DB\-Anbietervorlagen](../../data/oledb/ole-db-provider-template-architecture.md)