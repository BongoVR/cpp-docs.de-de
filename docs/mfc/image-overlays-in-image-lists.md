---
title: Bild überlagert in Bildlisten | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-mfc
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- overlays [MFC]
- image lists [MFC], image overlays in
- CImageList class [MFC], image overlays in
ms.assetid: aaf4e1c4-cd12-42c8-9af4-1bb458889b4e
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: 55a55a6e015a2f8c1613a85717c030737712c4da
ms.sourcegitcommit: 76b7653ae443a2b8eb1186b789f8503609d6453e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/04/2018
---
# <a name="image-overlays-in-image-lists"></a>Overlaymasken in Bildlisten
Jede Bildliste ([CImageList](../mfc/reference/cimagelist-class.md)) enthält eine Liste von Bildern für die Verwendung als Overlaymasken. Eine Overlaymaske"" ist ein Bild transparent über ein anderes Bild gezeichnet. Bilder kann als eine Overlaymaske verwendet werden. Sie können bis zu vier Overlaymasken pro Bildliste angeben.  
  
 Den Index eines Bilds wird zur Liste der Overlaymasken hinzufügen, mit der [SetOverlayImage](../mfc/reference/cimagelist-class.md#setoverlayimage) Memberfunktion, den Index eines Bilds und den Index des eine Overlaymaske. Beachten Sie, dass die Indizes für die Overlaymasken einsbasierte anstatt nullbasiert sind.  
  
 Sie zeichnen eine Overlaymaske auf ein Bild mit einem einzigen Aufruf **zeichnen**. Die Parameter umfassen den Index des zu zeichnenden Bilds und den Index ein Overlay-Maske. Verwenden Sie die [INDEXTOOVERLAYMASK](http://msdn.microsoft.com/library/windows/desktop/bb761408) Makro, das den Index der Overlaymaske angeben. Sie können auch ein Overlaybild angeben, beim Aufrufen der [DrawIndirect](../mfc/reference/cimagelist-class.md#drawindirect) Memberfunktion.  
  
## <a name="see-also"></a>Siehe auch  
 [Verwenden von CImageList](../mfc/using-cimagelist.md)   
 [Steuerelemente](../mfc/controls-mfc.md)

