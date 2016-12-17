---
title: "_free_locale"
ms.custom: na
ms.date: "12/03/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: na
ms.suite: na
ms.technology: 
  - "devlang-cpp"
ms.tgt_pltfrm: na
ms.topic: "article"
apiname: 
  - "_free_locale"
apilocation: 
  - "msvcrt.dll"
  - "msvcr80.dll"
  - "msvcr90.dll"
  - "msvcr100.dll"
  - "msvcr100_clr0400.dll"
  - "msvcr110.dll"
  - "msvcr110_clr0400.dll"
  - "msvcr120.dll"
  - "msvcr120_clr0400.dll"
  - "ucrtbase.dll"
  - "api-ms-win-crt-locale-l1-1-0.dll"
apitype: "DLLExport"
f1_keywords: 
  - "__free_locale"
  - "free_locale"
  - "_free_locale"
dev_langs: 
  - "C++"
  - "C"
helpviewer_keywords: 
  - "__free_locale-Funktion"
  - "_free_locale-Funktion"
  - "free_locale-Funktion"
  - "Gebietsschemas, Freigeben"
ms.assetid: 1f08d348-ab32-4028-a145-6cbd51b49af9
caps.latest.revision: 12
caps.handback.revision: "12"
ms.author: "corob"
manager: "ghogen"
---
# _free_locale
[!INCLUDE[vs2017banner](../../assembler/inline/includes/vs2017banner.md)]

Gibt einen Gebietsschemaobjekt frei.  
  
## Syntax  
  
```  
void _free_locale(  
   _locale_t locale  
);  
```  
  
#### Parameter  
 `locale`  
 Gebietsschemaobjekt zum freizugeben.  
  
## Hinweise  
 Die Funktion `_free_locale` wird verwendet, um dem Gebietsschemaobjekt freizugeben, die von einem Aufruf von `_get_current_locale` oder `_create_locale` aufgerufen wird.  
  
 Der vorherige Name dieser Funktion, `__free_locale` \(mit zwei führenden Unterstrichen\) ist veraltet.  
  
## Anforderungen  
  
|`Routine`|Erforderlicher Header|  
|---------------|---------------------------|  
|`_free_locale`|\<locale.h\>|  
  
 Weitere Informationen zur Kompatibilität finden Sie unter [Kompatibilität](../../c-runtime-library/compatibility.md) in der Einführung.  
  
## .NET Framework-Entsprechung  
 Keine Entsprechung.  
  
## Siehe auch  
 [\_get\_current\_locale](../../c-runtime-library/reference/get-current-locale.md)   
 [\_create\_locale, \_wcreate\_locale](../../c-runtime-library/reference/create-locale-wcreate-locale.md)