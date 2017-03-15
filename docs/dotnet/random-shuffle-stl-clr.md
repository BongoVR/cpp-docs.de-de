---
title: "random_shuffle (STL/CLR) | Microsoft Docs"
ms.custom: ""
ms.date: "11/04/2016"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-cpp"
ms.tgt_pltfrm: ""
ms.topic: "reference"
f1_keywords: 
  - "cliext::random_shuffle"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "random_shuffle-Funktion [STL/CLR]"
ms.assetid: 0f9d93e2-f50f-40e6-bbe4-2ca3231a895e
caps.latest.revision: 4
author: "mikeblome"
ms.author: "mblome"
manager: "ghogen"
caps.handback.revision: 4
---
# random_shuffle (STL/CLR)
[!INCLUDE[vs2017banner](../assembler/inline/includes/vs2017banner.md)]

Ordnet eine Sequenz von `N`\-Elementen in einem Bereich in einen von `N` neu an\! beliebige Anordnungen zufällig ausgewählt.  
  
## Syntax  
  
```  
template<class _RanIt> inline  
    void random_shuffle(_RanIt _First, _RanIt _Last);  
template<class _RanIt, class _Fn1> inline  
    void random_shuffle(_RanIt _First, _RanIt _Last, _Fn1% _Func);  
```  
  
## Hinweise  
 Diese Funktion verhält sich genauso wie die STL\-Funktion `random_shuffle`.  Weitere Informationen finden Sie unter [random\_shuffle](../Topic/random_shuffle.md).  
  
## Anforderungen  
 **Header:** \<cliext\/Algorithmus\>  
  
 **Namespace:** cliext  
  
## Siehe auch  
 [algorithm](../dotnet/algorithm-stl-clr.md)