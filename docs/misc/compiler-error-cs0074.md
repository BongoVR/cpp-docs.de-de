---
title: "Compilerfehler CS0074"
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
  - "CS0074"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS0074"
ms.assetid: 9395c532-3934-4553-8e41-042bfe3399ce
caps.latest.revision: 8
caps.handback.revision: "8"
ms.author: "wiwagn"
manager: "wpickett"
---
# Compilerfehler CS0074
'ereignis': Ein abstraktes Ereignis kann keinen Initialisierer haben.  
  
 Wenn ein [Ereignis](../Topic/event%20\(C%23%20Reference\).md) als **abstrakt** markiert ist, kann es nicht initialisiert werden. Weitere Informationen finden Sie unter [Ereignisse](../Topic/Events%20\(C%23%20Programming%20Guide\).md).  
  
 Im folgenden Beispiel wird CS0074 generiert:  
  
```  
// CS0074.cs delegate void D(); abstract class Test { public abstract event D e = null;   // CS0074 // try the following line instead // public abstract event D e; public static void Main() { } }  
```