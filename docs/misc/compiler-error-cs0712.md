---
title: "Compilerfehler CS0712"
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
  - "CS0712"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS0712"
ms.assetid: cde64c0c-3953-4563-8c24-8b646230bbb8
caps.latest.revision: 7
caps.handback.revision: "7"
ms.author: "wiwagn"
manager: "wpickett"
---
# Compilerfehler CS0712
Es kann keine Instanz der statischen "statistische Klasse"\-Klasse erstellt werden.  
  
 Es ist nicht möglich,  Instanzen von statischen Klassen zu erstellen. Statische Klassen sind für statische Felder und Methoden vorgesehen, können aber nicht instanziiert werden.  
  
## Beispiel  
 Im folgenden Beispiel wird CS0712 generiert:  
  
```  
// CS0712.cs public static class SC { } public class CMain { public static void Main() { SC sc = new SC();  // CS0712 } }  
```