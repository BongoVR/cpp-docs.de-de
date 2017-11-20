---
title: Compilerwarnung (Stufe 4) C4513 | Microsoft Docs
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-tools
ms.tgt_pltfrm: 
ms.topic: error-reference
f1_keywords: C4513
dev_langs: C++
helpviewer_keywords: C4513
ms.assetid: 6877334a-f30a-4184-9483-dac3348737a4
caps.latest.revision: "6"
author: corob-msft
ms.author: corob
manager: ghogen
ms.openlocfilehash: 08365d28394afbbce40ee758002922dc9ca30395
ms.sourcegitcommit: ebec1d449f2bd98aa851667c2bfeb7e27ce657b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/24/2017
---
# <a name="compiler-warning-level-4-c4513"></a>Compilerwarnung (Stufe 4) C4513
'Klasse': Destruktor konnte nicht generiert werden  
  
 Der Compiler kann keinen Standarddestruktor für die angegebene Klasse generieren. Es wurde kein Destruktor erstellt. Der Destruktor wird in einer Basisklasse, die für die abgeleitete Klasse nicht zugänglich ist. Wenn die Basisklasse einen privaten Destruktor verfügt, stellen sie öffentliche oder geschützte.