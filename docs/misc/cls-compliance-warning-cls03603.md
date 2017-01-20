---
title: "CLS-Kompatibilit&#228;t: Warnung CLS03603"
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
  - "CLS03603"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "CLS03603"
ms.assetid: 8bd74395-6b44-427d-8fe0-648dd946e6d2
caps.latest.revision: 8
caps.handback.revision: "8"
ms.author: "corob"
manager: "douge"
---
# CLS-Kompatibilit&#228;t: Warnung CLS03603
Globale static\-Felder sind nicht CLS\-kompatibel.  
  
 Globale static\-Felder und Methoden sind nicht CLS\-kompatibel.  
  
 Weitere Informationen zur Überprüfung der CLS\-Kompatibilität \(Common Language Subset\) finden Sie unter [CLS\-kompatible Assemblys](assetId:///3320b57e-ea55-4697-a17d-f509a36a3c93).  
  
 Im folgenden Beispiel wird CLS03603 generiert:  
  
```  
// CLS03603.cpp // compile with: /clr /LD // CLS03603 expected using namespace System; using namespace System::Reflection; [assembly:CLSCompliant (true)]; [assembly:AssemblyKeyFile("clscompliance.snk")]; int i;   // CLS03603 public ref class MyClass { public: int i;   // OK };  
```