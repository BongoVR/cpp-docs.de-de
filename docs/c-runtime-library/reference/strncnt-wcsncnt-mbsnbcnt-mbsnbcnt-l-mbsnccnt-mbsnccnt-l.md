---
title: _strncnt, _wcsncnt, _mbsnbcnt, _mbsnbcnt_l, _mbsnccnt, _mbsnccnt_l | Microsoft-Dokumentation
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-standard-libraries
ms.topic: reference
apiname:
- _mbsnbcnt_l
- _mbsnccnt
- _wcsncnt
- _strncnt
- _mbsnccnt_l
- _mbsnbcnt
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
- api-ms-win-crt-multibyte-l1-1-0.dll
apitype: DLLExport
f1_keywords:
- _mbsnbcnt
- wcsncnt
- _tcsnbcnt
- _mbsnccnt
- _ftcsnbcnt
- mbsnbcnt
- strncnt
- mbsnbcnt_l
- mbsnccnt_l
- mbsnccnt
- _strncnt
- _wcsncnt
dev_langs:
- C++
helpviewer_keywords:
- _strncnt function
- _mbsnbcnt function
- _mbsnbcnt_l function
- _mbsnccnt_l function
- mbsnbcnt_l function
- mbsnbcnt function
- tcsnbcnt function
- mbsnccnt_l function
- strncnt function
- _tcsnbcnt function
- mbsnccnt function
- wcsncnt function
- _mbsnccnt function
- _wcsncnt function
ms.assetid: 2a022e9e-a307-4acb-a66b-e56e5357f848
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: cf9bebda262bde4dd3bb2484a95b7b57a6960d99
ms.sourcegitcommit: be2a7679c2bd80968204dee03d13ca961eaa31ff
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/03/2018
---
# <a name="strncnt-wcsncnt-mbsnbcnt-mbsnbcntl-mbsnccnt-mbsnccntl"></a>_strncnt, _wcsncnt, _mbsnbcnt, _mbsnbcnt_l, _mbsnccnt, _mbsnccnt_l

Gibt die Anzahl von Bytes oder Zeichen innerhalb einer angegebenen Zählers zurück.

> [!IMPORTANT]
> **_mbsnbcnt**, **_mbsnbcnt_l**, **_mbsnccnt**, und **_mbsnccnt_l** kann nicht in Anwendungen, die in der Windows-Runtime ausgeführt verwendet werden. Weitere Informationen finden Sie im Artikel [CRT functions not supported in Universal Windows Platform apps (In Apps für die universelle Windows-Plattform nicht unterstützte CRT-Funktionen)](../../cppcx/crt-functions-not-supported-in-universal-windows-platform-apps.md).

## <a name="syntax"></a>Syntax

```C
size_t _strncnt(
   const char *str,
   size_t count
);
size_t _wcsncnt(
   const wchar_t *str,
   size_t count
);
size_t _mbsnbcnt(
   const unsigned char *str,
   size_t count
);
size_t _mbsnbcnt_l(
   const unsigned char *str,
   size_t count,
   _locale_t locale
);
size_t _mbsnccnt(
   const unsigned char *str,
   size_t count
);
size_t _mbsnccnt_l(
   const unsigned char *str,
   size_t count,
   _locale_t locale
);

```

### <a name="parameters"></a>Parameter

*str*<br/>
Zu untersuchende Zeichenfolge.

*count*<br/>
Anzahl von Zeichen oder Bytes, die überprüft werden *str*.

*locale*<br/>
Zu verwendendes Gebietsschema.

## <a name="return-value"></a>Rückgabewert

**_mbsnbcnt** und **_mbsnbcnt_l** Zurückgeben der Anzahl der Bytes, die gefunden in der ersten *Anzahl* eines multibytezeichens von *str*. **_mbsnccnt** und **_mbsnccnt_l** Zurückgeben der Anzahl der Zeichen in der ersten *Anzahl* der Bytes der *str*. Wenn ein NULL-Zeichen, bevor die Überprüfung von gefunden wird *str* wurde abgeschlossen, die Anzahl von Bytes oder Zeichen gefunden wird, bevor das NULL-Zeichen zurück. Wenn *str* besteht aus weniger als *Anzahl* sie die Anzahl der Zeichen oder Bytes Zeichen oder Bytes in der Zeichenfolge zurück. Wenn *Anzahl* ist kleiner als 0 (null), geben sie 0 zurück. In früheren Versionen hatten diese Funktionen einen Rückgabewert vom Typ **Int** statt **Size_t**.

**_strncnt** gibt die Anzahl der Zeichen in der ersten *Anzahl* Bytes der einzelbytezeichenfolge *str*. **_wcsncnt** gibt die Anzahl der Zeichen in der ersten *Anzahl* Breitzeichen der Breitzeichenfolge *str*.

## <a name="remarks"></a>Hinweise

**_mbsnbcnt** und **_mbsnbcnt_l** zählen die Anzahl von Bytes, die gefunden in der ersten *Anzahl* eines multibytezeichens von *str*. **_mbsnbcnt** und **_mbsnbcnt_l** ersetzen **Mtob** und sollte verwendet werden, anstelle von **Mtob**.

**_mbsnccnt** und **_mbsnccnt_l** zählen die Anzahl von Zeichen in der ersten *Anzahl* der Bytes der *str*. Wenn **_mbsnccnt** und **_mbsnccnt_l** eine NULL in das zweite Byte Double-Byte-Zeichen, das erste Byte wird auch als NULL betrachtet und ist nicht im zurückgegebenen Zählwert enthalten. **_mbsnccnt** und **_mbsnccnt_l** ersetzen **Btom** und sollte verwendet werden, anstelle von **Btom**.

Wenn *str* ist ein null-Zeiger oder *Anzahl* gleich 0 ist, rufen diese Funktionen den Handler für ungültige Parameter aus, wie in beschrieben [Parametervalidierung](../../c-runtime-library/parameter-validation.md), **Errno** festgelegt ist, um **EINVAL**, und die Funktion gibt 0 zurück.

Der Ausgabewert wird von der Einstellung der beeinflusst die **LC_CTYPE** -kategorieneinstellung des Gebietsschemas; Siehe [Setlocale](setlocale-wsetlocale.md) für Weitere Informationen. Die Versionen dieser Funktionen ohne das **_l**-Suffix verwenden das aktuelle Gebietsschema für dieses vom Gebietsschema abhängige Verhalten; die Versionen mit dem **_l**-Suffix sind beinahe identisch, verwenden jedoch stattdessen den ihnen übergebenen Gebietsschemaparameter. Weitere Informationen finden Sie unter [Locale](../../c-runtime-library/locale.md).

### <a name="generic-text-routine-mappings"></a>Zuordnung generischer Textroutinen

|Routine|_UNICODE und _MBCS nicht definiert|_MBCS definiert|_UNICODE definiert|
|-------------|--------------------------------------|--------------------|-----------------------|
|**_tcsnbcnt**|**_strncnt**|**_mbsnbcnt**|**_wcsncnt**|
|**_tcsnccnt**|**_strncnt**|**_mbsnbcnt**|n/v|
|**_wcsncnt**|n/v|n/v|**_mbsnbcnt**|
|**_wcsncnt**|n/v|n/v|**_mbsnccnt**|
|n/v|n/v|**_mbsnbcnt_l**|**_mbsnccnt_l**|

## <a name="requirements"></a>Anforderungen

|Routine|Erforderlicher Header|
|-------------|---------------------|
|**_mbsnbcnt**|\<mbstring.h>|
|**_mbsnbcnt_l**|\<mbstring.h>|
|**_mbsnccnt**|\<mbstring.h>|
|**_mbsnccnt_l**|\<mbstring.h>|
|**_strncnt**|\<tchar.h>|
|**_wcsncnt**|\<tchar.h>|

Weitere Informationen zur Kompatibilität finden Sie unter [Kompatibilität](../../c-runtime-library/compatibility.md).

## <a name="example"></a>Beispiel

```C
// crt_mbsnbcnt.c

#include  <mbstring.h>
#include  <stdio.h>

int main( void )
{
   unsigned char str[] = "This is a multibyte-character string.";
   unsigned int char_count, byte_count;
   char_count = _mbsnccnt( str, 10 );
   byte_count = _mbsnbcnt( str, 10 );
   if ( byte_count - char_count )
      printf( "The first 10 characters contain %d multibyte characters\n", char_count );
   else
      printf( "The first 10 characters are single-byte.\n");
}
```

### <a name="output"></a>Ausgabe

```Output
The first 10 characters are single-byte.
```

## <a name="see-also"></a>Siehe auch

[Zeichenfolgenbearbeitung](../../c-runtime-library/string-manipulation-crt.md)<br/>
[Locale](../../c-runtime-library/locale.md)<br/>
[Interpretation von Multibyte-Zeichensequenzen](../../c-runtime-library/interpretation-of-multibyte-character-sequences.md)<br/>
[_mbsnbcat, _mbsnbcat_l](mbsnbcat-mbsnbcat-l.md)<br/>
