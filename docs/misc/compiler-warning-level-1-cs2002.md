---
title: "Compilerwarnung (Stufe 1) CS2002"
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
  - "CS2002"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS2002"
ms.assetid: 4acd054e-d3fe-4be6-a660-53a0a5e8c6a4
caps.latest.revision: 7
caps.handback.revision: "7"
ms.author: "wiwagn"
manager: "wpickett"
---
# Compilerwarnung (Stufe 1) CS2002
Die Quelldatei „file“ wurde mehrere Male angegeben.  
  
 Der Name einer Quelldatei wurde mehrmals an den Compiler übergeben. Sie können eine Datei nur einmal an den Compiler übergeben, um eine Ausgabedatei zu erstellen.  
  
 Diese Warnung kann nicht durch die [\/nowarn](../Topic/-nowarn%20\(C%23%20Compiler%20Options\).md)\-Option unterdrückt werden.  
  
 Im folgenden Beispiel wird CS2002 generiert:  
  
```  
// CS2002.cs // compile with: CS2002.cs public class A { public static void Main(){} }  
```  
  
 Kompilieren Sie das Beispiel mit der Befehlszeile, um den Fehler zu generieren:  
  
```  
csc CS2002.cs CS2002.cs  
```