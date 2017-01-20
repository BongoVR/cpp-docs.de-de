---
title: "CLS-Kompatibilit&#228;t: Warnung CLS01706"
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
  - "CLS01706"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "CLS01706"
ms.assetid: b89ccbf1-7256-4842-a0af-44a803f28340
caps.latest.revision: 8
caps.handback.revision: "8"
ms.author: "corob"
manager: "douge"
---
# CLS-Kompatibilit&#228;t: Warnung CLS01706
Nicht verwaltete Zeigertypen sind nicht CLS\-kompatibel.  
  
 Eine CLS\-kompatible Funktionssignatur darf keinen nicht verwalteten Zeigertyp enthalten.  
  
 Weitere Informationen zur Überprüfung der CLS\-Kompatibilität \(Common Language Subset\) finden Sie unter [CLS\-kompatible Assemblys](assetId:///3320b57e-ea55-4697-a17d-f509a36a3c93).  
  
 Im folgenden Beispiel wird CLS01706 generiert:  
  
```  
// CLS01706.cpp // compile with: /clr /LD // CLS01706 expected [assembly:System::CLSCompliant (true)]; [assembly:System::Reflection::AssemblyKeyFile("clscompliance.snk")]; public ref class One { public: void Method1(int* parameter) {}   // CLS01706 void Method1(One ^ parameter) {}   // OK };  
```