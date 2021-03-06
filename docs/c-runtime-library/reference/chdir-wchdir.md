---
title: _chdir, _wchdir | Microsoft-Dokumentation
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-standard-libraries
ms.topic: reference
apiname:
- _wchdir
- _chdir
apilocation:
- msvcrt.dll
- msvcr80.dll
- msvcr90.dll
- msvcr100.dll
- msvcr100_clr0400.dll
- msvcr110.dll
- msvcr110_clr0400.dll
- msvcr120.dll
- msvcr120_clr0400.dll
- ucrtbase.dll
- api-ms-win-crt-filesystem-l1-1-0.dll
apitype: DLLExport
f1_keywords:
- tchdir
- _chdir
- _wchdir
- _tchdir
- wchdir
dev_langs:
- C++
helpviewer_keywords:
- _tchdir function
- _chdir function
- _wchdir function
- tchdir function
- wchdir function
- chdir function
- directories [C++], changing
ms.assetid: 85e9393b-62ac-45d5-ab2a-fa2217f6152e
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 92becad93e1d0375f3ecf1ec587daa877a4c8485
ms.sourcegitcommit: be2a7679c2bd80968204dee03d13ca961eaa31ff
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/03/2018
---
# <a name="chdir-wchdir"></a>_chdir, _wchdir

Ändert das aktuelle Arbeitsverzeichnis.

## <a name="syntax"></a>Syntax

```C
int _chdir(
   const char *dirname
);
int _wchdir(
   const wchar_t *dirname
);
```

### <a name="parameters"></a>Parameter

*Verwendung*<br/>
Pfad des neuen Arbeitsverzeichnisses.

## <a name="return-value"></a>Rückgabewert

Diese Funktionen geben bei Erfolg den Wert 0 zurück. Ein Rückgabewert "-1" gibt einen Fehler. Wenn der angegebene Pfad nicht gefunden werden kann, **Errno** festgelegt ist, um **ENOENT**. Wenn *Dirname* NULL ist, den Handler für ungültige Parameter aufgerufen, wie in beschrieben [Parametervalidierung](../../c-runtime-library/parameter-validation.md). Wenn die weitere Ausführung zugelassen wird, um den Vorgang fortzusetzen, **Errno** festgelegt ist, um **EINVAL** und die Funktion gibt-1 zurück.

## <a name="remarks"></a>Hinweise

Die **_chdir** -Funktion ändert das aktuelle Arbeitsverzeichnis auf das Verzeichnis, das vom angegebenen *Dirname*. Die *Dirname* -Parameter muss auf ein vorhandenes Verzeichnis verweisen. Diese Funktion kann das aktuelle Arbeitsverzeichnis auf jedem beliebigen Laufwerk ändern. Wenn ein neuer Laufwerkbuchstabe in angegebenen *Dirname*, wird der Standardlaufwerkbuchstabe ebenfalls geändert. Wenn z. B. A der Standardlaufwerkbuchstabe und \BIN das aktuelle Arbeitsverzeichnis ist, ändert der folgende Aufruf das aktuelle Arbeitsverzeichnis in C und legt C als neues Standardlaufwerk fest:

```C
_chdir("c:\temp");
```

Bei Verwendung von den optionalen umgekehrten Schrägstrich (**&#92;**) in Pfadangaben verwenden, müssen Sie zwei umgekehrte Schrägstriche platzieren (**&#92;&#92;**) in einem C-Zeichenfolgenliteral dargestellt einen einzelnen umgekehrten Schrägstrich ( **&#92;**).

**_wchdir** ist eine Breitzeichen-Version von **_chdir**; das *Dirname* Argument **_wchdir** ist eine Breitzeichen-Zeichenfolge. **_wchdir** und **_chdir** Verhalten sich andernfalls identisch.

### <a name="generic-text-routine-mapping"></a>Zuordnung generischer Textroutinen:

|Tchar.h-Routine|_UNICODE und _MBCS nicht definiert|_MBCS definiert|_UNICODE definiert|
|---------------------|--------------------------------------|--------------------|-----------------------|
|**_tchdir**|**_chdir**|**_chdir**|**_wchdir**|

## <a name="requirements"></a>Anforderungen

|Routine|Erforderlicher Header|Optionaler Header|
|-------------|---------------------|---------------------|
|**_chdir**|\<direct.h>|\<errno.h>|
|**_wchdir**|\<direct.h> oder \<wchar.h>|\<errno.h>|

Weitere Informationen zur Kompatibilität finden Sie unter [Kompatibilität](../../c-runtime-library/compatibility.md).

## <a name="example"></a>Beispiel

```C
// crt_chdir.c
// arguments: C:\WINDOWS

/* This program uses the _chdir function to verify
   that a given directory exists. */

#include <direct.h>
#include <stdio.h>
#include <stdlib.h>
#include <errno.h>

int main( int argc, char *argv[] )
{

   if(_chdir( argv[1] ) )
   {
      switch (errno)
      {
      case ENOENT:
         printf( "Unable to locate the directory: %s\n", argv[1] );
         break;
      case EINVAL:
         printf( "Invalid buffer.\n");
         break;
      default:
         printf( "Unknown error.\n");
      }
   }
   else
      system( "dir *.exe");
}
```

```Output
 Volume in drive C has no label.
 Volume Serial Number is 2018-08A1

 Directory of c:\windows

08/29/2002  04:00 AM         1,004,032 explorer.exe
12/17/2002  04:43 PM            10,752 hh.exe
03/03/2003  09:24 AM            33,792 ieuninst.exe
10/29/1998  04:45 PM           306,688 IsUninst.exe
08/29/2002  04:00 AM            66,048 NOTEPAD.EXE
03/03/2003  09:24 AM            33,792 Q330994.exe
08/29/2002  04:00 AM           134,144 regedit.exe
02/28/2003  06:26 PM            46,352 setdebug.exe
08/29/2002  04:00 AM            15,360 TASKMAN.EXE
08/29/2002  04:00 AM            49,680 twunk_16.exe
08/29/2002  04:00 AM            25,600 twunk_32.exe
08/29/2002  04:00 AM           256,192 winhelp.exe
08/29/2002  04:00 AM           266,752 winhlp32.exe
              13 File(s)      2,249,184 bytes
               0 Dir(s)  67,326,029,824 bytes free
```

## <a name="see-also"></a>Siehe auch

[Verzeichnissteuerung](../../c-runtime-library/directory-control.md)<br/>
[_mkdir, _wmkdir](mkdir-wmkdir.md)<br/>
[_rmdir, _wrmdir](rmdir-wrmdir.md)<br/>
[system, _wsystem](system-wsystem.md)<br/>
