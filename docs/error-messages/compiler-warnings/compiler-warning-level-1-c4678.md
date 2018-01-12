---
title: Compilerwarnung (Stufe 1) C4678 | Microsoft Docs
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-tools
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords: C4678
dev_langs: C++
helpviewer_keywords: C4678
ms.assetid: 0c588f34-595d-4e5c-9470-8723fca2cc06
caps.latest.revision: "10"
author: corob-msft
ms.author: corob
manager: ghogen
ms.workload: cplusplus
ms.openlocfilehash: 7648101a0862aa2006feff73a5ebe32bd0f424a1
ms.sourcegitcommit: 8fa8fdf0fbb4f57950f1e8f4f9b81b4d39ec7d7a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/21/2017
---
# <a name="compiler-warning-level-1-c4678"></a>Compilerwarnung (Stufe 1) C4678
Basisklasse "base_type" hat eine stärkere Zugriffsbeschränkung als "derived_type"  
  
Ein öffentlicher Typ wurde von einem privaten Typ abgeleitet. Wenn der öffentliche Typ in einer referenzierten Assembly instanziiert wird, sind die Member des privaten Basistyps nicht zugänglich.  
  
C4678 ist nur über die veraltete Compileroption erreichbar **/CLR: oldSyntax**. Es ist ein Fehler auf, wenn mit **"/ CLR"**, damit eine Basisklasse, die weniger zugegriffen werden kann, die abgeleitete Klasse.  
