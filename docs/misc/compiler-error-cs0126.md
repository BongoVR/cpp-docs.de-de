---
title: "Compilerfehler CS0126"
ms.custom: na
ms.date: "11/16/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: na
ms.suite: na
ms.technology: 
  - "devlang-csharp"
ms.tgt_pltfrm: na
ms.topic: "article"
f1_keywords: 
  - "CS0126"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS0126"
ms.assetid: 15fb0f38-ac9d-4c09-a69f-398a4903d790
caps.latest.revision: 8
caps.handback.revision: "8"
ms.author: "wiwagn"
manager: "wpickett"
---
# Compilerfehler CS0126
Ein Objekt oder Typ ist erforderlich, der in "Typ" konvertiert werden kann.  
  
 Es ist eine return\-Anweisung vorhanden, aber die Anweisung gibt keinen Wert zurück, der den erwarteten Typ hat. Weitere Informationen finden Sie unter [Eigenschaften](../Topic/Properties%20\(C%23%20Programming%20Guide\).md).  
  
 Im folgenden Beispiel wird CS0126 generiert:  
  
```  
// CS0126.cs public class a { public int i { set { } get { return;   // CS0126, specify a value to return } } }  
```