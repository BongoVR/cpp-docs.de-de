---
title: "Problembehandlung bei Ausnahmen: System.Threading.SynchronizationLockException"
ms.custom: na
ms.date: "10/29/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: na
ms.suite: na
ms.technology: 
  - "devlang-csharp"
ms.tgt_pltfrm: na
ms.topic: "article"
helpviewer_keywords: 
  - "SynchronizationLockException-Ausnahme"
  - "System.Threading.SynchronizationLockException-Ausnahme"
ms.assetid: 82d80643-fc5c-40ae-a579-46869772d25c
caps.latest.revision: 4
caps.handback.revision: "4"
ms.author: "mblome"
manager: "douge"
---
# Problembehandlung bei Ausnahmen: System.Threading.SynchronizationLockException
Diese Ausnahme wird ausgelöst, wenn eine Methode, für die der Aufrufer die Sperre für einen bestimmten `Monitor` besitzen muss, von einem Aufrufer aufgerufen wird, der diese Sperre nicht besitzt.  
  
## Hinweise  
 Eine <xref:System.Threading.SynchronizationLockException> wird ausgelöst, wenn in einem nicht synchronisierten Codeblock eine der folgenden Methoden der <xref:System.Threading.Monitor.Exit*>\-Klasse aufgerufen wird: <xref:System.Threading.Monitor.Pulse*>, <xref:System.Threading.Monitor.PulseAll*>, <xref:System.Threading.Monitor.Wait*> oder `Monitor`.  
  
## Siehe auch  
 <xref:System.Threading.SynchronizationLockException>   
 [Use the Exception Assistant](../Topic/How%20to:%20Use%20the%20Exception%20Assistant.md)