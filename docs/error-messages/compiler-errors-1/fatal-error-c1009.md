---
title: Schwerwiegender Fehler C1009 | Microsoft Docs
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- cpp-tools
ms.tgt_pltfrm: 
ms.topic: error-reference
f1_keywords:
- C1009
dev_langs:
- C++
helpviewer_keywords:
- C1009
ms.assetid: dcc8383c-3362-4c47-9c26-25d2451ebd53
caps.latest.revision: 
author: corob-msft
ms.author: corob
manager: ghogen
ms.workload:
- cplusplus
ms.openlocfilehash: 92d91240ea092ff75387246952ce5b7207527173
ms.sourcegitcommit: 8fa8fdf0fbb4f57950f1e8f4f9b81b4d39ec7d7a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/21/2017
---
# <a name="fatal-error-c1009"></a>Schwerwiegender Fehler C1009
Compilerlimit: zu tiefe Schachtelung von Makros  
  
 Der Compiler hat versucht, zu viele Makros gleichzeitig zu erweitern. Der Compiler hat einen Grenzwert von 256 Ebenen der Schachtelung von Makros. Teilen Sie geschachtelte Makros in einfachere Makros.