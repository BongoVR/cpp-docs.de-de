---
title: Initialisieren von Klassen und Strukturen ohne Konstruktoren (C++) | Microsoft Docs
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-language
ms.tgt_pltfrm: 
ms.topic: language-reference
dev_langs: C++
ms.assetid: 3e55c3d6-1c6b-4084-b9e5-221b151402f4
caps.latest.revision: "3"
author: mikeblome
ms.author: mblome
manager: ghogen
ms.openlocfilehash: 6a93b6b8f182407109465d1397a063b23a408df9
ms.sourcegitcommit: ebec1d449f2bd98aa851667c2bfeb7e27ce657b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/24/2017
---
# <a name="initializing-classes-and-structs-without-constructors-c"></a>Initialisieren von Klassen und Strukturen ohne Konstruktoren (C++)
Es ist nicht immer erforderlich, einen Konstruktor für eine Klasse zu definieren, insbesondere bei einfachen. Benutzer können Objekte einer Klasse oder Struktur mithilfe einer einheitlichen Initialisierung initialisieren, wie dies aus dem folgenden Beispiel hervorgeht:  
  
```  
#include "stdafx.h"  
#include <Windows.h>  
  
// No constructor  
struct TempData  
{  
    int StationId;  
    time_t time;  
    double current;  
    double maxTemp;  
    double minTemp;  
};  
  
// Has a constructor  
struct TempData2  
{  
    TempData2(double minimum, double maximum, double cur, int id, time_t t) :  
       minTemp(minimum), maxTemp(maximum), current(cur), stationId(id), time(t) {}  
    int stationId;  
    time_t time;  
    double current;  
    double maxTemp;  
    double minTemp;  
};  
  
int main()  
{  
    // Member initialization (in order of declaration):  
    TempData td{ 45978, GetCurrentTime(), 28.9, 37.0, 16.7 };  
  
    // Default initialization = {0,0,0,0,0}  
    TempData td_default{};  
  
    //Error C4700 uninitialized local variable  
    TempData td_noInit;  
  
    // Member declaration (in order of ctor parameters)  
    TempData2 td2{ 16.7, 37.0, 28.9, 45978, GetCurrentTime() };  
  
    return 0;  
}  
  
```  
  
 Beachten Sie, dass wenn eine Klasse oder Struktur keinen Konstruktor verfügt, Sie die Listenelemente in der Reihenfolge, dass die Elemente in der Klasse deklariert werden. Wenn die Klasse einen Konstruktor verfügt, geben Sie die Elemente in der Reihenfolge der Parameter ein.  
  
## <a name="see-also"></a>Siehe auch  
 [Klassen und Strukturen](../cpp/classes-and-structs-cpp.md)   
 [Konstruktoren](../cpp/constructors-cpp.md)