---
title: _getdcwd, _wgetdcwd | Microsoft-Dokumentation
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-standard-libraries
ms.topic: reference
apiname:
- _getdcwd
- _wgetdcwd
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
- api-ms-win-crt-stdio-l1-1-0.dll
apitype: DLLExport
f1_keywords:
- wgetdcwd
- getdcwd
- _getdcwd
- tgetdcwd
- _wgetdcwd
- _tgetdcwd
dev_langs:
- C++
helpviewer_keywords:
- wgetdcwd function
- working directory
- getdcwd function
- _getdcwd function
- _wgetdcwd function
- current working directory
- directories [C++], current working
ms.assetid: 184152f5-c7b0-495b-918d-f9a6adc178bd
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: b0ccc526b196982402ca3b795276df8c790ad35a
ms.sourcegitcommit: be2a7679c2bd80968204dee03d13ca961eaa31ff
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/03/2018
---
# <a name="getdcwd-wgetdcwd"></a>_getdcwd, _wgetdcwd

Ruft den vollständigen Pfad des aktuellen Arbeitsverzeichnisses auf dem angegebenen Laufwerk ab.

## <a name="syntax"></a>Syntax

```C
char *_getdcwd(
   int drive,
   char *buffer,
   int maxlen
);
wchar_t *_wgetdcwd(
   int drive,
   wchar_t *buffer,
   int maxlen
);
```

### <a name="parameters"></a>Parameter

*Laufwerk*<br/>
Eine nicht negative ganze Zahl, die das Laufwerk angibt (0 = Standardlaufwerk, 1 = A, 2 = B usw.).

Wenn das angegebene Laufwerk nicht verfügbar ist oder die Art des Laufwerks (z. B. Wechseldatenträger, festes Laufwerk, CD-ROM-Laufwerk, RAM-Datenträger oder Netzlaufwerk) nicht bestimmt werden kann, wird der Handler für ungültige Parameter aufgerufen, wie in [Parameter Validation](../../c-runtime-library/parameter-validation.md)beschrieben.

*buffer*<br/>
Speicherort für den Pfad, oder **NULL**.

Wenn **NULL** angegeben ist, wird diese Funktion weist einen Puffer von mindestens *Maxlen* mit Größe **"malloc"**, und der Rückgabewert der **_getdcwd**ist ein Zeiger auf den zugeordneten Puffer. Der Puffer kann freigegeben werden, durch den Aufruf **freien** und der Zeiger übergeben wird.

*maxlen*<br/>
Eine positive ganze Zahl ungleich NULL, der angibt, die maximale Länge des Pfads in Zeichen: **Char** für **_getdcwd** und **Wchar_t** für **_wgetdcwd**.

Wenn *Maxlen* ist nicht größer als 0 (null), wird der Handler für ungültige Parameter, dies wird im beschrieben [Parametervalidierung](../../c-runtime-library/parameter-validation.md), aufgerufen wird.

## <a name="return-value"></a>Rückgabewert

Zeiger auf eine Zeichenfolge, die den vollständigen Pfad des aktuellen Arbeitsverzeichnisses auf dem angegebenen Laufwerk darstellt oder **NULL**, wodurch ein Fehler.

Wenn *Puffer* angegeben ist, als **NULL** und es ist nicht genügend Arbeitsspeicher zum Zuordnen *Maxlen* Zeichen, die ein Fehler auftritt und **Errno** ist Legen Sie auf **ENOMEM**. Überschreitet die Länge des Pfads, der das abschließende Nullzeichen enthält, *Maxlen*, ein Fehler auftritt und **Errno** festgelegt ist, um **ERANGE**. Weitere Informationen zu diesen Fehlercodes finden Sie unter [errno, _doserrno, _sys_errlist und _sys_nerr](../../c-runtime-library/errno-doserrno-sys-errlist-and-sys-nerr.md).

## <a name="remarks"></a>Hinweise

Die **_getdcwd** Funktion ruft den vollständigen Pfad des aktuellen Arbeitsverzeichnisses auf dem angegebenen Laufwerk ab und speichert ihn unter *Puffer*. Wenn das aktuelle Arbeitsverzeichnis auf das Stammverzeichnis festgelegt ist, endet die Zeichenfolge mit einem umgekehrten Schrägstrich (\\). Wenn das aktuelle Arbeitsverzeichnis nicht auf das Stammverzeichnis festgelegt ist, endet die Zeichenfolge mit dem Namen des Verzeichnisses und nicht mit einem umgekehrten Schrägstrich.

**_wgetdcwd** ist eine Breitzeichen-Version von **_getdcwd**, und die zugehörige *Puffer* Parameter und der Rückgabewert sind Breitzeichen Zeichenfolgen. Andernfalls **_wgetdcwd** und **_getdcwd** Verhalten sich identisch.

Diese Funktion ist threadsicher, obwohl sie von der Funktion **GetFullPathName**abhängig ist, die selbst nicht threadsicher ist. Es kann jedoch zu einer Verletzung der Threadsicherheit kommen, wenn die Multithreadanwendung sowohl diese Funktion als auch **GetFullPathName**aufruft. Weitere Informationen finden Sie in der [MSDN Library](http://go.microsoft.com/fwlink/p/?linkid=150542) . Suchen Sie dort nach **GetFullPathName**.

Die Version von dieser Funktion mit dem **_nolock** Suffix verhält sich ebenso wie dieser Funktion identisch, allerdings nicht threadsicher ist und nicht vor Störungen durch andere Threads geschützt. Weitere Informationen finden Sie unter [_getdcwd_nolock, _wgetdcwd_nolock](getdcwd-nolock-wgetdcwd-nolock.md).

Wenn **_DEBUG** und **_CRTDBG_MAP_ALLOC** definiert sind, werden Aufrufe von **_getdcwd** und **_wgetdcwd** werden durch Aufrufe von ersetzt **_getdcwd_dbg** und **_wgetdcwd_dbg** , sodass Sie speicherbelegungen Debuggen können. Weitere Informationen finden Sie unter[_getdcwd_dbg, _wgetdcwd_dbg](getdcwd-dbg-wgetdcwd-dbg.md).

### <a name="generic-text-routine-mappings"></a>Zuordnung generischer Textroutinen

|Tchar.h-Routine|_UNICODE und _MBCS nicht definiert|_MBCS definiert|_UNICODE definiert|
|---------------------|--------------------------------------|--------------------|-----------------------|
|**_tgetdcwd**|**_getdcwd**|**_getdcwd**|**_wgetdcwd**|

## <a name="requirements"></a>Anforderungen

|Routine|Erforderlicher Header|
|-------------|---------------------|
|**_getdcwd**|\<direct.h>|
|**_wgetdcwd**|\<direct.h> oder \<wchar.h>|

Weitere Informationen zur Kompatibilität finden Sie unter [Kompatibilität](../../c-runtime-library/compatibility.md).

## <a name="example"></a>Beispiel

Siehe das Beispiel in [_getdrive](getdrive.md).

## <a name="see-also"></a>Siehe auch

[Verzeichnissteuerung](../../c-runtime-library/directory-control.md)<br/>
[_chdir, _wchdir](chdir-wchdir.md)<br/>
[_getcwd, _wgetcwd](getcwd-wgetcwd.md)<br/>
[_getdrive](getdrive.md)<br/>
[_mkdir, _wmkdir](mkdir-wmkdir.md)<br/>
[_rmdir, _wrmdir](rmdir-wrmdir.md)<br/>
