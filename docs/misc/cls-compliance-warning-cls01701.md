---
title: "CLS-Kompatibilit&#228;t: Warnung CLS01701"
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
  - "CLS01701"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "CLS01701"
ms.assetid: 6ccbe156-9017-44ea-bd4e-a838af2ec2e7
caps.latest.revision: 8
caps.handback.revision: "8"
ms.author: "corob"
manager: "douge"
---
# CLS-Kompatibilit&#228;t: Warnung CLS01701
Nicht verwaltete Zeigertypen sind nicht CLS\-kompatibel.  
  
 Ein CLS\-kompatibler Konstruktor darf keine systemeigene Zeigerdeklaration enthalten.  
  
 Weitere Informationen zur CLS\-Kompatibilitätsprüfung finden Sie unter [CLS\-kompatible Assemblys](assetId:///3320b57e-ea55-4697-a17d-f509a36a3c93).  
  
 Im folgenden Beispiel wird CLS01701 generiert:  
  
```  
// CLS01701.cpp // compile with: /clr /LD // CLS01701 expected using namespace System; using namespace System::Reflection; [assembly:CLSCompliant (true)]; [assembly:AssemblyKeyFile("clscompliance.snk")]; public ref class One { public: One(int* Parameter) {}   // CLS01701 };  
```