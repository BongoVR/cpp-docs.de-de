---
title: NAME (C/C++) | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-tools
ms.topic: reference
f1_keywords:
- name
dev_langs:
- C++
helpviewer_keywords:
- NAME .def file statement
ms.assetid: 5c9b6bd8-9275-46a5-afba-f17a5936dc26
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: a94b82a65cf68d9802d7bf9620e4128ab6b35071
ms.sourcegitcommit: be2a7679c2bd80968204dee03d13ca961eaa31ff
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/03/2018
---
# <a name="name-cc"></a>NAME (C/C++)
Gibt einen Namen für die main-Ausgabedatei.  
  
```  
NAME [application][BASE=address]  
```  
  
## <a name="remarks"></a>Hinweise  
 Alternativ können Sie einen Ausgabedateinamen angeben ist, mit der [/OUT](../../build/reference/out-output-file-name.md) (Linkeroption) und eine entsprechende Methode zum Festlegen der Basisadresse wird mit der [/BASE](../../build/reference/base-base-address.md) (Linkeroption). Wenn beide angegeben sind, / OUT überschreibt **Namen**.  
  
 Wenn Sie eine DLL erstellen, wirkt sich der NAME nur den DLL-Namen.  
  
## <a name="see-also"></a>Siehe auch  
 [Regeln für Moduldefinitionsanweisungen](../../build/reference/rules-for-module-definition-statements.md)