---
title: Rückrufelemente und Rückrufmaske | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-mfc
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- callback items in CListCtrl class [MFC]
- CListCtrl class [MFC], callback item and callback mask
ms.assetid: 67c1f76f-6144-453e-9376-6712f89430ae
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: 95c896308970ffc6a2040657927dc127eee278ba
ms.sourcegitcommit: 76b7653ae443a2b8eb1186b789f8503609d6453e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/04/2018
---
# <a name="callback-items-and-the-callback-mask"></a>Rückrufelemente und die Rückrufmaske
Für die einzelnen Elemente einem Listenansicht-Steuerelement in der Regel speichert den Bezeichnungstext, den Bildindex Liste von Symbolen für das Element, und ein Satz von Bit flags für der Zustand des Elements. Sie können einzelne Elemente als Rückrufelemente definieren, die sind nützlich, wenn die Anwendung bereits einige der Informationen für ein Element gespeichert.  
  
 Ein Element wird als ein Rückrufelement definiert, durch Angeben der entsprechenden Werte für die `pszText` und `iImage` Mitglied der **LV_ITEM** Struktur (finden Sie unter [CListCtrl:: GetItem](../mfc/reference/clistctrl-class.md#getitem)). Wenn die Anwendung die des Elements oder Unterelements Text verwaltet, geben Sie die **LPSTR_TEXTCALLBACK** Wert für die `pszText` Member. Wenn die Anwendung das Symbol für das Element der nachverfolgt, geben Sie die **I_IMAGECALLBACK** Wert für die `iImage` Member.  
  
 Zusätzlich zum Definieren von Rückrufelemente, können Sie auch das Steuerelement Rückrufmaske ändern. Diese Maske ist ein Satz von Bitflags, die die Element-Zustände angeben, für die das Steuerelement, statt die Anwendung die aktuellen Daten speichert. Die Rückrufmaske gilt für alle Elemente des Steuerelements im Gegensatz zu Rückrufelement, die für ein bestimmtes Element angewendet wird. Die Rückrufmaske ist 0 (null), wird standardmäßig, was bedeutet, dass das Steuerelement alle-Element-Zustände verfolgt. Um dieses Standardverhalten zu ändern, initialisieren Sie die Maske, die eine beliebige Kombination der folgenden Werte:  
  
-   `LVIS_CUT` Das Element ist für einen Ausschneide- und Einfügevorgang markiert.  
  
-   `LVIS_DROPHILITED` Das Element wird als Drag-and-Drop-Ziel hervorgehoben.  
  
-   `LVIS_FOCUSED` Das Element besitzt den Fokus.  
  
-   `LVIS_SELECTED` Das Element ausgewählt ist.  
  
-   **LVIS_OVERLAYMASK** die Anwendung speichert die Liste Abbildindex des aktuellen Overlay-Images für jedes Element.  
  
-   **LVIS_STATEIMAGEMASK** die Anwendung speichert die Liste Abbildindex des aktuellen statusbilds für jedes Element.  
  
 Weitere Informationen abrufen und diese Maske festlegen, finden Sie unter [CListCtrl:: GetCallbackMask](../mfc/reference/clistctrl-class.md#getcallbackmask) und [CListCtrl::SetCallbackMask](../mfc/reference/clistctrl-class.md#setcallbackmask).  
  
## <a name="see-also"></a>Siehe auch  
 [Verwenden von CListCtrl](../mfc/using-clistctrl.md)   
 [Steuerelemente](../mfc/controls-mfc.md)

