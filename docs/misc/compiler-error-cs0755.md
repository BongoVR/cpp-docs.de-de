---
title: "Compilerfehler CS0755"
ms.custom: na
ms.date: "11/17/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: na
ms.suite: na
ms.technology: 
  - "devlang-csharp"
ms.tgt_pltfrm: na
ms.topic: "article"
f1_keywords: 
  - "CS0755"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS0755"
ms.assetid: 80613029-a009-4bdf-b1c2-1eec1e60c7b4
caps.latest.revision: 7
caps.handback.revision: "7"
ms.author: "wiwagn"
manager: "wpickett"
---
# Compilerfehler CS0755
Beide partiellen Methodendeklarationen müssen Erweiterungsmethoden sein, oder keine von beiden darf eine Erweiterungsmethode sein.  
  
 Eine partielle Methode besteht aus einer definierenden Deklaration \(Signatur\) und einer optionalen implementierenden Deklaration \(Text\). Wenn die definierende Deklaration eine Erweiterungsmethode ist, muss die implementierende Deklaration, sofern definiert, auch eine Erweiterungsmethode sein. Und wenn die definierende Methode keine Erweiterungsmethode ist, darf auch die implementierende Methode keine Erweiterungsmethode sein.  
  
### So beheben Sie diesen Fehler  
  
1.  Entfernen Sie den `this`\-Modifizierer aus einer Methode, oder fügen Sie ihn der anderen hinzu.  
  
## Beispiel  
 Im folgenden Beispiel wird der Fehler CS0755 generiert:  
  
```  
// cs0755.cs public static partial class Ext { static partial void Part(this C c); //Extension method // Typically the implementing declaration is in a separate file. static partial void Part(C c) //CS0755 { } } public partial class C { public static int Main() { return 1; } }  
```  
  
## Siehe auch  
 [Erweiterungsmethoden](../Topic/Extension%20Methods%20\(C%23%20Programming%20Guide\).md)