---
title: Binäre Operatoren | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-language
ms.topic: language-reference
dev_langs:
- C++
helpviewer_keywords:
- member-selection operators [C++]
- operators [C++], binary
- binary operators [C++]
ms.assetid: c0e7fbff-bc87-4708-8333-504ac09ee83e
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: 3b930c548ea411beb03255d694f2423903053288
ms.sourcegitcommit: be2a7679c2bd80968204dee03d13ca961eaa31ff
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/03/2018
---
# <a name="binary-operators"></a>Binäre Operatoren
Die folgende Tabelle zeigt eine Liste von Operatoren, die überladen werden können.  
  
### <a name="redefinable-binary-operators"></a>Neu definierbare binäre Operatoren  
  
|Operator|name|  
|--------------|----------|  
|**,**|Komma|  
|`!=`|Ungleichheit|  
|`%`|Modulooperator|  
|`%=`|Modulo/Zuweisung|  
|**&**|Bitweises AND|  
|**&&**|Logisches AND|  
|**&=**|Bitweises AND/Zuweisung|  
|**\***|Multiplikation|  
|**\*=**|Multiplikation/Zuweisung|  
|**+**|Addition|  
|`+=`|Addition/Zuweisung|  
|**-**|Subtraktion|  
|**-=**|Subtraktion/Zuweisung|  
|**->**|Memberauswahl|  
|**->\***|Pointer-to-member-Auswahl|  
|**/**|Division|  
|`/=`|Division/Zuweisung|  
|**<**|Kleiner als|  
|**<<**|Nach links verschieben|  
|**<<=**|Nach links verschieben/Zuweisung|  
|**<=**|Kleiner oder gleich|  
|**=**|Zuweisung|  
|`==`|Gleichheit|  
|**>**|Größer als|  
|**>=**|Größer oder gleich|  
|**>>**|Nach rechts verschieben|  
|**>>=**|Nach rechts verschieben/Zuweisung|  
|**^**|Exklusives OR|  
|`^=`|Exklusives OR/Zuweisung|  
|**&#124;**|Bitweises inklusives OR|  
|`&#124;=`|Bitweises inklusives OR/Zuweisung|  
|`&#124;&#124;`|Logisches OR|  
  
 Um eine binäre Operatorfunktion als nicht statischen Member zu deklarieren, muss sie im folgenden Format deklariert werden:  
  
 *ret-Type* **Operator**`op`**(** `arg` **)**  
  
 wobei *ret-Type* ist der Rückgabetyp `op` ist einer der in der obigen Tabelle aufgelisteten Operatoren und `arg` ist ein Argument eines beliebigen Typs.  
  
 Um eine binäre Operatorfunktion als globale Funktion zu deklarieren, muss sie im folgenden Format deklariert werden:  
  
 *ret-Type* **Operator**`op`**(** `arg1` **,** `arg2` **)**  
  
 auf dem *ret-Type* und `op` sind für Member-Operator-Funktionen erläutert und `arg1` und `arg2` sind Argumente. Mindestens eines der Argumente muss ein Klassentyp sein.  
  
> [!NOTE]
>  Es gibt keine Einschränkung für die Rückgabetypen der binären Operatoren. Die meisten benutzerdefinierten binären Operatoren geben jedoch entweder einen Klassentyp oder einen Verweis auf einen Klassentyp zurück.  
  
## <a name="see-also"></a>Siehe auch  
 [Operatorüberladung](../cpp/operator-overloading.md)