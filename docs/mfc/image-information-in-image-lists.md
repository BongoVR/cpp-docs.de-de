---
title: Bild der Informationen in Bildlisten | Microsoft Docs
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-windows
ms.tgt_pltfrm: 
ms.topic: article
dev_langs: C++
helpviewer_keywords:
- CImageList class [MFC], image information in
- image lists [MFC], image information in
ms.assetid: 73c41543-fa91-405d-b15b-0feffa6a72c1
caps.latest.revision: "10"
author: mikeblome
ms.author: mblome
manager: ghogen
ms.openlocfilehash: 80e897ec79314abb2e77864e53d470e72f275a94
ms.sourcegitcommit: ebec1d449f2bd98aa851667c2bfeb7e27ce657b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/24/2017
---
# <a name="image-information-in-image-lists"></a>Bildinformationen in Bildlisten
[CImageList](../mfc/reference/cimagelist-class.md) umfasst eine Reihe von Funktionen, die Informationen aus einer Bildliste abrufen. Die [GetImageInfo](../mfc/reference/cimagelist-class.md#getimageinfo) Member-Funktion füllt eine `IMAGEINFO` Struktur mit Informationen über ein einzelnes Bild, einschließlich der Ziehpunkte des Bitmaps Bild und die Maske, die Anzahl von Farbebenen und Bits pro Pixel und das umschließende Rechteck des Bilds in der Image-Bitmap. Diese Informationen können Sie um die Bitmaps für das Bild direkt zu bearbeiten.  
  
 Die [GetImageCount](../mfc/reference/cimagelist-class.md#getimagecount) Memberfunktion Ruft die Anzahl von Bildern in einer Bildliste ab.  
  
 Sie können ein Symbol basierend auf einem Bild und die Maske in einer Bildliste mit Erstellen der [ExtractIcon](../mfc/reference/cimagelist-class.md#extracticon) Memberfunktion. Die Funktion gibt das Handle für das Symbol "Neu".  
  
## <a name="see-also"></a>Siehe auch  
 [Verwenden von CImageList](../mfc/using-cimagelist.md)   
 [Steuerelemente](../mfc/controls-mfc.md)
