---
title: "MSBuild Error MSB1013"
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
  - "MSBuild.RepeatedResponseFileError"
helpviewer_keywords: 
  - "MSB1013"
ms.assetid: 3e85c710-99e6-4141-b058-63a144a06454
caps.latest.revision: 11
caps.handback.revision: "11"
ms.author: "mblome"
manager: "douge"
---
# MSBuild Error MSB1013
**Die Antwortdatei wurde zweimal angegeben.  Eine Antwortdatei kann nur einmal angegeben werden.**  
  
 Die Befehlszeile enthält Verweise auf mehrere Antwortdateien.  Beispielsweise `msbuild @response.rsp @response.rsp`.  
  
 Dieser Fehler kann auch dann auftreten, wenn die angegebene Antwortdatei einen Verweis auf eine andere Antwortdatei enthält, die ihrerseits einen Verweis auf die Originalantwortdatei enthält.  Eine Antwortdatei kann in einer Kompilierung nur einmal angegeben werden.  
  
### So beheben Sie diesen Fehler  
  
-   Entfernen Sie den doppelten Verweis auf die Antwortdatei.  Verwenden Sie beispielsweise `msbuild @response.rsp` anstelle von `msbuild @response.rsp @response.rsp`.  
  
-   Entfernen Sie den Verweis auf die ursprüngliche Antwortdatei aus der Antwortdatei, auf die sie verweist.  
  
## Siehe auch  
 [Command\-Line Reference](../Topic/MSBuild%20Command-Line%20Reference.md)