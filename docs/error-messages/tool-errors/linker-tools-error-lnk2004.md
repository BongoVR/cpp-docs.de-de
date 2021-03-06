---
title: Linkertoolfehler Lnk2004 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- LNK2004
dev_langs:
- C++
helpviewer_keywords:
- LNK2004
ms.assetid: 07645371-e67b-4a2c-b0e0-dde24c94ef7e
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 2619ebc3fcf997574628354a951619cd18a81b46
ms.sourcegitcommit: 76b7653ae443a2b8eb1186b789f8503609d6453e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/04/2018
---
# <a name="linker-tools-error-lnk2004"></a>Linkertoolfehler LNK2004
Gp relativer Fixup-Überlauf zu 'Ziel'; kurzer Abschnitt "Abschnitt" ist zu groß ist oder außerhalb des gültigen Bereichs.  
  
 Der Abschnitt war zu groß.  
  
 Um diesen Fehler zu beheben, verringern Sie die Größe des short-Abschnitts, indem Sie explizit Einfügen von Daten in den long-Abschnitten mit #pragma Section (".sectionname", read, Write, Long) und `__declspec(allocate(".sectionname"))` -Definitionen und Deklarationen.  Ein auf ein Objekt angewendeter  
  
```  
#pragma section(".data$mylong", read, write, long)  
__declspec(allocate(".data$mylong"))  
char    rg0[1] = { 1 };  
char    rg1[2] = { 1 };  
char    rg2[4] = { 1 };  
char    rg3[8] = { 1 };  
char    rg4[16] = { 1 };  
char    rg5[32] = { 1 };  
```  
  
 Sie können auch logisch gruppierte Daten in ihre eigene Struktur verschieben, die eine Auflistung von Daten, die größer als 8 Bytes festgelegt, werden die der Compiler in einem Abschnitt long-Daten zuordnet.  Ein auf ein Objekt angewendeter  
  
```  
// from this...  
int     w1  = 23;  
int     w2 = 46;  
int     w3 = 23*3;  
int     w4 = 23*4;  
  
// to this...  
struct X {  
    int     w1;  
    int     w2;  
    int     w3;  
    int     w4;  
} x  = { 23, 23*2, 23*3, 23*4 };  
  
```  
  
 Diesem Fehler folgt der schwerwiegende Fehler `LNK1165`.