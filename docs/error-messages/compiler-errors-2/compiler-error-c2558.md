---
title: Compilerfehler C2558 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2558
dev_langs:
- C++
helpviewer_keywords:
- C2558
ms.assetid: 822b701e-dcae-423a-b21f-47f36aff9c90
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: d7db417edebf0a1fff6ef87bf8ae407889a0e0af
ms.sourcegitcommit: 76b7653ae443a2b8eb1186b789f8503609d6453e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/04/2018
---
# <a name="compiler-error-c2558"></a>Compilerfehler C2558
'Bezeichner': Kein Kopierkonstruktor verfügbar, oder der Kopierkonstruktor ist als 'explicit' deklariert  
  
 Durch einen Kopierkonstruktor wird ein Objekt von einem anderen Objekt desselben Typs initialisiert. (Es wird eine Kopie des Objekts angelegt.) Der Compiler generiert einen Standardkopierkonstruktor, wenn keine Konstruktoren definiert wurden.  
  
### <a name="to-fix-this-error"></a>So beheben Sie diesen Fehler  
  
1.  Das Problem kann auftreten bei dem Versuch, eine Klasse zu kopieren, deren Kopierkonstruktor als `private` deklariert ist. In den meisten Fällen sollte eine Klasse mit einem als `private` deklarierten Kopierkonstruktor nicht kopiert werden. Mithilfe allgemeiner Programmierpraktiken wurde ein Kopierkonstruktor als `private` deklariert, um die direkte Verwendung einer Klasse zu verhindern. Die Klasse ist möglicherweise nutzlos oder benötigt eine andere Klasse, um ordnungsgemäß zu funktionieren.  
  
     Wenn es Ihnen sicher erscheint, eine Klasse mit einem `private`-Kopierkonstruktor zu verwenden, leiten Sie von der Klasse eine neue Klasse mit einem `private`-Konstruktor ab und stellen Sie in der neuen Klasse einen `public`-Kopierkonstruktor oder einen `protected`-Kopierkonstruktor bereit. Verwenden Sie die abgeleitete Klasse anstelle des Originals.  
  
2.  Das Problem kann auftreten bei dem Versuch, eine Klasse zu kopieren, deren Kopierkonstruktor explizit ist. Das Deklarieren eines Kopierkonstruktors als `explicit` verhindert die Übergabe/Rückgabe von Objekten einer Klasse an/von Funktionen. Weitere Informationen über explizite Konstruktoren finden Sie unter [benutzerdefinierte Typkonvertierungen](../../cpp/user-defined-type-conversions-cpp.md).  
  
3.  Das Problem kann auftreten bei dem Versuch, eine Klasseninstanz zu kopieren, die als `const` deklariert ist, und ein Kopierkonstruktor verwendet wird, der keinen `const` Verweisparameter akzeptiert. Deklarieren Sie den Kopierkonstruktor mit einem Verweis vom Typ `const` und nicht mit einem nicht konstanten Verweis.