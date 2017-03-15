---
title: "Compilerfehler C3141 | Microsoft Docs"
ms.custom: ""
ms.date: "11/04/2016"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-cpp"
ms.tgt_pltfrm: ""
ms.topic: "error-reference"
f1_keywords: 
  - "C3141"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "C3141"
ms.assetid: b4fd65c3-50cc-46cd-8de0-6a6d24cb9cda
caps.latest.revision: 7
author: "corob-msft"
ms.author: "corob"
manager: "ghogen"
caps.handback.revision: 7
---
# Compilerfehler C3141
[!INCLUDE[vs2017banner](../../assembler/inline/includes/vs2017banner.md)]

'interface\_name': Schnittstellen unterstützen nur die öffentliche Vererbung  
  
 Schnittstellen, die mit dem Schlüsselwort [interface \(oder \_\_interface\)](../../cpp/interface.md) definiert wurden, unterstützen nur die öffentliche Vererbung.  
  
 Im folgenden Beispiel wird C3141 generiert:  
  
```  
// C3141.cpp  
__interface IBase {};  
__interface IDerived1 : protected IBase {};  // C3141  
__interface IDerived2 : private IBase {};    // C3141  
```