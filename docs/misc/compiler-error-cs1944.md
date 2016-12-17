---
title: "Compilerfehler CS1944"
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
  - "CS1944"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS1944"
ms.assetid: e5e2c018-9a7e-48ee-8dd3-98e3553777c1
caps.latest.revision: 8
caps.handback.revision: "8"
ms.author: "wiwagn"
manager: "wpickett"
---
# Compilerfehler CS1944
Eine Ausdrucksbaumstruktur darf keinen unsicheren Zeigervorgang enthalten.  
  
 Ausdrucksbaumstrukturen unterstützen keine Zeigertypen, da die <xref:System.Linq.Expressions.Expression`1.Compile*?displayProperty=fullName>\-Methode nur zum Erzeugen von überprüfbarem Code zulässig ist. Weitere Informationen finden Sie in den Kommentaren.  
  
### So beheben Sie diesen Fehler  
  
1.  Verwenden Sie keine Zeigertypen, wenn Sie versuchen, eine Ausdrucksbaumstruktur zu erstellen.  
  
## Beispiel  
 Im folgenden Beispiel wird der Fehler CS1944 generiert:  
  
<CodeContentPlaceHolder>0</CodeContentPlaceHolder>  
 In einigen Situationen ist es angemessen, Zeiger in Ausdrucksbaumstrukturen zu verwenden. Beachten Sie z. B. folgenden Code:  
  
 `Expression<Func\<int*[], int*[]>) e = (int*[] i)=>i;`  
  
 Dieser Code stellt eine gültige Ausdrucksbaumstruktur dar, da keine Typargumente Zeigertypen sind. Sie sind Zeigerarrays und Arrays sind keine Zeigertypen. Der Text der Ausdrucksbaumstruktur führt auch keine gefährlichen Aktionen mit einem Zeiger aus.  
  
## Siehe auch  
 [Unsicher](../Topic/unsafe%20\(C%23%20Reference\).md)