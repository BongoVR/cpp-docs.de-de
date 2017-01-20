---
title: "Compilerwarnung (Stufe 1) CS1709"
ms.custom: na
ms.date: "10/29/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: na
ms.suite: na
ms.technology: 
  - "devlang-csharp"
ms.tgt_pltfrm: na
ms.topic: "article"
f1_keywords: 
  - "CS1709"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS1709"
ms.assetid: e2bb1d30-4f30-4e10-82da-df1d3418454c
caps.latest.revision: 8
caps.handback.revision: "8"
ms.author: "wiwagn"
manager: "wpickett"
---
# Compilerwarnung (Stufe 1) CS1709
Der für die Präprozessordirektive angegebene Dateiname ist leer.  
  
 Sie haben eine Präprozessordirektive angegeben, die einen Dateinamen enthält, die Datei ist jedoch leer. Um diese Warnung zu beheben, fügen Sie den erforderlichen Inhalt in die Datei ein.  
  
## Beispiel  
 Im folgenden Beispiel wird CS1709 generiert:  
  
```  
// CS1709.cs class Test { static void Main() { #pragma checksum "" "{406EA660-64CF-4C82-B6F0-42D48172A799}" ""  // CS1709 } }  
```