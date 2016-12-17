---
title: "Compilerfehler CS0611"
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
  - "CS0611"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS0611"
ms.assetid: bbd857a0-9454-4438-a21c-fef5bc7eee06
caps.latest.revision: 6
caps.handback.revision: "6"
ms.author: "wiwagn"
manager: "wpickett"
---
# Compilerfehler CS0611
Arrayelemente können nicht vom Typ 'Typ' sein.  
  
 Es gibt einige Typen, die nicht als Typ eines Arrays verwendet werden können. Zu diesen Typen gehören **System.TypedReference** und **System.ArgIterator**.  
  
 Im folgenden Beispiel wird CS0611 generiert, weil **System.TypedReference** als Arrayelement verwendet wurde:  
  
```  
// CS0611.cs public class a { public static void Main() { System.TypedReference[] ao = new System.TypedReference [10];   // CS0611 // try the following line instead // int[] ao = new int[10]; } }  
```