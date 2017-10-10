---
title: Schwerwiegender Fehler C1103 | Microsoft Docs
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- cpp-tools
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- C1103
dev_langs:
- C++
helpviewer_keywords:
- C1103
ms.assetid: 9d276939-9c47-4235-9d20-76b8434f9731
caps.latest.revision: 6
author: corob-msft
ms.author: corob
manager: ghogen
ms.translationtype: MT
ms.sourcegitcommit: 35b46e23aeb5f4dbfd2a0dd44b906389dd5bfc88
ms.openlocfilehash: 41759b75db078d4f689b12cc71d502ec907b56a2
ms.contentlocale: de-de
ms.lasthandoff: 10/09/2017

---
# <a name="fatal-error-c1103"></a>Schwerwiegender Fehler C1103
Schwerwiegender Fehler beim Importieren der ProgID: "Meldung"  
  
 Der Compiler hat beim Importieren einer Typbibliothek ein Problem festgestellt.  Sie können beispielsweise keine Typbibliothek mit "progid" angeben und gleichzeitig `no_registry`festlegen.  
  
 Weitere Informationen finden Sie unter [#import-Direktive](../../preprocessor/hash-import-directive-cpp.md).  
  
 Im folgenden Beispiel wird C1103 generiert:  
  
```  
// C1103.cpp  
#import "progid:a.b.id.1.5" no_registry auto_search   // C1103  
```
