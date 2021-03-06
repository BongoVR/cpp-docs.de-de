---
title: --Konstruktoren Kommentar | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-mfc
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- constructors comment
- declarations, constructors
- MFC source files, Constructors comment
- declaring constructors, code comments
- comments, MFC
- comments, constructors comment
- constructors [MFC], declaring
- instance constructors, code comments
ms.assetid: f400774e-ba85-49ed-85b7-70ef2f7dcb2b
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: 71b78e74b4b8d974fceaf5f854c9890cd7cdd1a1
ms.sourcegitcommit: 76b7653ae443a2b8eb1186b789f8503609d6453e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/04/2018
---
# <a name="-constructors-comment"></a>// Constructors-Kommentar
Die `// Constructors` Teil einer MFC-Klassendeklaration deklariert, Konstruktoren (in dem Sinne C++) sowie Initialisierungsfunktionen erforderlich, um das Objekt tatsächlich verwenden. Beispielsweise `CWnd::Create` wird im Abschnitt Konstruktoren, da vor der Verwendung der `CWnd` Objekt ist, wird er erstellt werden muss"vollständig" durch den ersten Aufruf des C++-Konstruktors und dem anschließenden Aufrufen der **erstellen** Funktion. In der Regel sind diese Member öffentlich.  
  
 Beispielsweise `CStdioFile` verfügt über drei Konstruktoren, von denen, in der Liste unter angezeigt wird [ein Beispiel für die Kommentare](../mfc/an-example-of-the-comments.md).  
  
## <a name="see-also"></a>Siehe auch  
 [Verwenden der MFC-Quelldateien](../mfc/using-the-mfc-source-files.md)   
 [/ / Implementierungskommentar](../mfc/decrement-implementation-comment.md)   
 [Attributekommentar](../mfc/decrement-attributes-comment.md)   
 [Vorgänge-Kommentar](../mfc/decrement-operations-comment.md)   
 [Overridables-Kommentar](../mfc/decrement-overridables-comment.md)

