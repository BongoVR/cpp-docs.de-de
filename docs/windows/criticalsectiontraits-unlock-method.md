---
title: "CriticalSectionTraits::Unlock-Methode | Microsoft Docs"
ms.custom: ""
ms.date: "11/04/2016"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-cpp"
ms.tgt_pltfrm: ""
ms.topic: "reference"
f1_keywords: 
  - "corewrappers/Microsoft::WRL::Wrappers::HandleTraits::CriticalSectionTraits::Unlock"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "Unlock-Methode"
ms.assetid: 8fb382f5-6eda-407e-9673-71d77bda4962
caps.latest.revision: 3
author: "mikeblome"
ms.author: "mblome"
manager: "ghogen"
caps.handback.revision: 3
---
# CriticalSectionTraits::Unlock-Methode
[!INCLUDE[vs2017banner](../assembler/inline/includes/vs2017banner.md)]

Spezialisiert eine CriticalSections\-Vorlage, sodass sie das Freigeben des Besitzes des angegebenen Abschnittsobjekts kritischen unterstützt.  
  
## Syntax  
  
```  
inline static void Unlock(  
   _In_ Type cs  
);  
```  
  
#### Parameter  
 `cs`  
 Ein Zeiger zu einem kritischen Abschnittsobjekt.  
  
## Hinweise  
 Der *Type*\-Modifizierer wird als `typedef CRITICAL_SECTION* Type;` definiert.  
  
 Weitere Informationen finden Sie unter "LeaveCriticalSections\-Funktion" im "Synchronisierungs\-Funktions" Abschnitt der Windows\-API\-Dokumentation.  
  
## Anforderungen  
 **Header:** corewrappers.h  
  
 **Namespace:**  Microsoft::WRL::Wrappers::HandleTraits  
  
## Siehe auch  
 [CriticalSectionTraits\-Struktur](../windows/criticalsectiontraits-structure.md)