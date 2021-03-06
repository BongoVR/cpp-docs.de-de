---
title: ATL-Modulklassen | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-atl
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- CComModule class, what's changed
- ATL, module classes
- module classes
ms.assetid: fd75382d-c955-46ba-a38e-37728b7fa00f
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: 777d81fbe1de48289863fda00591a5328b40cf4c
ms.sourcegitcommit: be2a7679c2bd80968204dee03d13ca961eaa31ff
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/03/2018
---
# <a name="atl-module-classes"></a>ATL-Modulklassen
Dieses Thema erläutert die Modulklassen, die neu in ATL 7.0 waren.  
  
## <a name="ccommodule-replacement-classes"></a>CComModule Ersatz-Klassen  
 Frühere Versionen von ATL verwendet `CComModule`. In ATL 7.0 `CComModule` Funktionalität wird von mehreren Klassen ersetzt:  
  
-   [CAtlBaseModule](../atl/reference/catlbasemodule-class.md) enthält Informationen, die von den meisten Anwendungen, die ATL verwenden erforderlich Enthält die HINSTANCE des Moduls und die Ressourceninstanz.  
  
-   [CAtlComModule](../atl/reference/catlcommodule-class.md) enthält Informationen, die COM-Klassen in ATL erforderlich  
  
-   [CAtlWinModule](../atl/reference/catlwinmodule-class.md) enthält Informationen, die erforderlich sind, durch die Windowing-Klassen in ATL  
  
-   [CAtlDebugInterfacesModule](../atl/reference/catldebuginterfacesmodule-class.md) enthält Unterstützung für das Debuggen.  
  
-   [Von CAtlModule](../atl/reference/catlmodule-class.md) Folgendes `CAtlModule`-abgeleitete Klassen werden angepasst, um in einen bestimmten Anwendungstyp erforderlichen Informationen enthalten. Die meisten Elemente in diesen Klassen können überschrieben werden:  
  
    -   [CAtlDllModuleT](../atl/reference/catldllmodulet-class.md) in DLL-Anwendungen verwendet. Stellt den Code für die standard-Exporte bereit.  
  
    -   [CAtlExeModuleT](../atl/reference/catlexemodulet-class.md) in EXE-Anwendungen verwendet. Enthält Code, die in einer EXE-Datei erforderlich.  
  
    -   [CAtlServiceModuleT](../atl/reference/catlservicemodulet-class.md) bietet Unterstützung zum Erstellen von Windows NT und Windows 2000-Dienste.  
  
 `CComModule` ist für die Abwärtskompatibilität weiterhin verfügbar.  
  
## <a name="reasons-for-distributing-ccommodule-functionality"></a>Gründe für das Verteilen von CComModule-Funktion  
 Die Funktionalität des `CComModule` mehrere neue Klassen verteilt wurde, den folgenden Gründen:  
  
-   Stellen Sie die Funktionalität in `CComModule` präzise.  
  
     Unterstützung für COM, Windowing, Debuggen und anwendungsspezifische (DLL oder EXE)-Funktionen ist nun in separaten Klassen.  
  
-   Deklarieren Sie automatisch die globale Instanz jedes dieser Module.  
  
     Eine globale Instanz von der erforderlichen Modulklassen wird in das Projekt verknüpft.  
  
-   Entfernen Sie die Notwendigkeit des Init "und" Begriff Methoden aufrufen.  
  
     Init "und" Begriff Methoden wurden in den Konstruktoren und Destruktoren für die Modulklassen verschoben; Es ist nicht mehr erforderlich Init "und" Begriff aufrufen.  
  
## <a name="see-also"></a>Siehe auch  
 [Konzepte](../atl/active-template-library-atl-concepts.md)   
 [Klassenübersicht](../atl/atl-class-overview.md)

