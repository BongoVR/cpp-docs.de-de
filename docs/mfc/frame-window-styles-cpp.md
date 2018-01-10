---
title: Rahmenfensterstile (C++) | Microsoft Docs
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-windows
ms.tgt_pltfrm: 
ms.topic: article
dev_langs: C++
helpviewer_keywords:
- window styles [MFC]
- PreCreateWindow method, setting window styles
- windows [MFC], MFC
- frame windows [MFC], styles
- MFC, frame windows
- styles [MFC], windows
ms.assetid: fc5058c1-eec8-48d8-9f76-3fc01cfa53f7
caps.latest.revision: "8"
author: mikeblome
ms.author: mblome
manager: ghogen
ms.workload: cplusplus
ms.openlocfilehash: a5bdc0204c538f476c791657d8b29a28b7baedd4
ms.sourcegitcommit: 8fa8fdf0fbb4f57950f1e8f4f9b81b4d39ec7d7a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/21/2017
---
# <a name="frame-window-styles-c"></a>Rahmenfensterstile (C++)
Das Rahmenfenster, Sie mit dem Framework erhalten, eignen sich für die meisten Programme erhalten Sie zusätzliche Flexibilität, mit den erweiterten Funktionen jedoch [PreCreateWindow](../mfc/reference/cwnd-class.md#precreatewindow) und der globalen MFC-Funktion [AfxRegisterWndClass ](../mfc/reference/application-information-and-management.md#afxregisterwndclass). `PreCreateWindow`ist eine Memberfunktion der `CWnd`.  
  
 Wenden Sie die **WS_HSCROLL** und **WS_VSCROLL** Stile an das Hauptrahmenfenster, werden sie stattdessen angewendet die **MDICLIENT** -Fenster, sodass Benutzer die gescrolltwerdenkönnen**MDICLIENT** Bereich.  
  
 Wenn des Fensters **FWS_ADDTOTITLE** Formatbit (die sie in der Standardeinstellung) festgelegt ist, wird die Sicht weist dem Rahmenfenster Titel, der in der Titelleiste des Fensters, die basierend auf den Namen der Sicht Dokument anzuzeigen.  
  
## <a name="what-do-you-want-to-know-more-about"></a>Was möchten Sie mehr erfahren  
  
-   [Verwalten von untergeordneten MDI-Fenster (MDICLIENT)](../mfc/managing-mdi-child-windows.md), das Fenster innerhalb einer MDI-Frame, untergeordnete MDI-Fenster enthält,  
  
-   [Ändern der Stile eines mit MFC erstellten Fensters](../mfc/changing-the-styles-of-a-window-created-by-mfc.md)  
  
-   [Fensterstile](../mfc/reference/styles-used-by-mfc.md#window-styles)  
  
## <a name="see-also"></a>Siehe auch  
 [Rahmenfenster](../mfc/frame-windows.md)
