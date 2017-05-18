---
title: strncmp, wcsncmp, _mbsncmp, _mbsncmp_l | Microsoft-Dokumentation
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- cpp-standard-libraries
ms.tgt_pltfrm: 
ms.topic: article
apiname:
- strncmp
- _mbsncmp
- wcsncmp
- _mbsncmp_l
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
- ntdll.dll
- ucrtbase.dll
- api-ms-win-crt-multibyte-l1-1-0.dll
- api-ms-win-crt-string-l1-1-0.dll
apitype: DLLExport
f1_keywords:
- _ftcsnccmp
- _ftcsncmp
- _tcsncmp
- _tcsnccmp
- strncmp
- _mbsncmp
- wcsncmp
dev_langs:
- C++
helpviewer_keywords:
- _tcsnccmp function
- ftcsncmp function
- wcsncmp function
- _ftcsncmp function
- _mbsncmp function
- tcsncmp function
- mbsncmp function
- _mbsncmp_l function
- mbsncmp_l function
- strncmp function
- strings [C++], comparing characters of
- string comparison [C++], strncmp function
- _tcsncmp function
- tcsnccmp function
- ftcsnccmp function
- characters [C++], comparing
- _ftcsnccmp function
ms.assetid: 2fdbf4e6-77da-4b59-9086-488f6066b8af
caps.latest.revision: 28
author: corob-msft
ms.author: corob
manager: ghogen
translation.priority.ht:
- cs-cz
- de-de
- es-es
- fr-fr
- it-it
- ja-jp
- ko-kr
- pl-pl
- pt-br
- ru-ru
- tr-tr
- zh-cn
- zh-tw
ms.translationtype: Machine Translation
ms.sourcegitcommit: e257f037a05c45f5b98e64ea55bd125af443b0be
ms.openlocfilehash: 4a66ac6c57b2e4ae25c7496152b4e113f3bbf751
ms.contentlocale: de-de
ms.lasthandoff: 03/29/2017

---
# <a name="strncmp-wcsncmp-mbsncmp-mbsncmpl"></a>strncmp, wcsncmp, _mbsncmp, _mbsncmp_l
Vergleicht die angegebene Anzahl von Zeichen zweier Zeichenfolgen.  
  
> [!IMPORTANT]
>  `_mbsncmp` und `_mbsncmp_l` können nicht in Anwendungen verwendet werden, die in Windows-Runtime ausgeführt werden. Weitere Informationen finden Sie unter [In /ZW nicht unterstützte CRT-Funktionen](http://msdn.microsoft.com/library/windows/apps/jj606124.aspx).  
  
## <a name="syntax"></a>Syntax  
  
```  
int strncmp(  
   const char *string1,  
   const char *string2,  
   size_t count   
);  
int wcsncmp(  
   const wchar_t *string1,  
   const wchar_t *string2,  
   size_t count   
);  
int _mbsncmp(  
   const unsigned char *string1,  
   const unsigned char *string2,  
   size_t count   
);  
int _mbsncmp_l(  
   const unsigned char *string1,  
   const unsigned char *string2,  
   size_t count,   
   _locale_t locale  
);int _mbsnbcmp(  
   const unsigned char *string1,  
   const unsigned char *string2,  
   size_t count   
);  
```  
  
#### <a name="parameters"></a>Parameter  
 `string1, string2`  
 Zu vergleichende Zeichenfolgen.  
  
 `count`  
 Anzahl der zu vergleichenden Zeichen.  
  
 `locale`  
 Zu verwendendes Gebietsschema.  
  
## <a name="return-value"></a>Rückgabewert  
 Der Rückgabewert zeigt der Beziehung der untergeordneten Zeichenfolgen von `string1` und `string2` wie folgt an.  
  
|Rückgabewert|Beschreibung|  
|------------------|-----------------|  
|< 0|Die untergeordnete Zeichenfolge `string1` ist kleiner als die untergeordnete Zeichenfolge `string2`.|  
|0|Die untergeordnete Zeichenfolge `string1` ist mit der untergeordneten Zeichenfolge `string2` identisch.|  
|> 0|Die untergeordnete Zeichenfolge `string1` ist größer als die untergeordnete Zeichenfolge `string2`.|  
  
 Bei einem Parameterüberprüfungsfehler geben `_mbsncmp` und `_mbsncmp_l` `_NLSCMPERROR` zurück (definiert in \<string.h> und \<mbstring.h>).  
  
## <a name="remarks"></a>Hinweise  
 Die `strncmp`-Funktion führt einen Ordinalvergleich der (höchstens) ersten `count`-Zeichen in `string1` und `string2` und gibt einen Wert zurück, der die Beziehung zwischen den untergeordneten Zeichenfolgen angibt. `strncmp` ist eine Version von `_strnicmp`, bei der die Groß-/Kleinschreibung zu beachten ist. `wcsncmp`und `_mbsncmp` sind Versionen von `_wcsnicmp` und `_mbsnicmp`, bei denen ebenfalls die Groß-/Kleinschreibung zu beachten ist.  
  
 `wcsncmp` und `_mbsncmp` sind Breitzeichen- und Multibytezeichenversionen von `strncmp`. Die Argumente von `wcsncmp` sind Breitzeichen-Zeichenfolgen, die von `_mbsncmp` sind Multibyte-Zeichenfolgen. `_mbsncmp` erkennt Multibyte-Zeichenfolge entsprechend einer Multibyte-Codepage und gibt im Falle eines Fehlers `_NLSCMPERROR` zurück.  
  
 Darüber hinaus überprüfen `_mbsncmp` `_mbsncmp_l` auch Parameter. Wenn `string1` oder `string2` ein NULL-Zeiger ist, wird der Handler für ungültige Parameter, wie in [Parameter Validation (Parameterüberprüfung)](../../c-runtime-library/parameter-validation.md) beschrieben, aufgerufen. Wenn die weitere Ausführung zugelassen wird, geben `_mbsncmp` und `_mbsncmp_l` den Wert `_NLSCMPERROR` zurück und setzen `errno` auf `EINVAL`. `strncmp` und `wcsncmp` überprüfen ihre Parameter nicht. Anderenfalls verhalten sich diese Funktionen identisch.  
  
 Das Vergleichsverhalten von `_mbsncmp` und `_mbsncmp_l` wird durch die Einstellung der `LC_CTYPE`-Kategorieeinstellung des Gebietsschemas beeinflusst. Hierdurch wird die Erkennung von vorangestellten und nachfolgenden Bytes von Multibytezeichen gesteuert. Weitere Informationen finden Sie unter [setlocale](../../c-runtime-library/reference/setlocale-wsetlocale.md). Die `_mbsncmp`-Funktion verwendet das aktuelle Gebietsschema für dieses gebietsschemaabhängige Verhalten. Die `_mbsncmp_l`-Funktion ist identisch, abgesehen davon, dass sie stattdessen den `locale`-Parameter verwendet. Weitere Informationen finden Sie unter [Locale](../../c-runtime-library/locale.md). Wenn das Gebietsschema ein Einzelbyte-Gebietsschema ist, ist das Verhalten dieser Funktionen identisch mit `strncmp`.  
  
### <a name="generic-text-routine-mappings"></a>Zuordnung generischer Textroutinen  
  
|TCHAR.H-Routine|_UNICODE und _MBCS nicht definiert.|_MBCS definiert|_UNICODE definiert|  
|---------------------|------------------------------------|--------------------|-----------------------|  
|`_tcsnccmp`|`strncmp`|`_mbsncmp`|`wcsncmp`|  
|`_tcsncmp`|`strncmp`|`_mbsnbcmp`|`wcsncmp`|  
|`_tccmp`|Führt eine Zuordnung zum Makro oder zur Inlinefunktion aus|`_mbsncmp`|Führt eine Zuordnung zum Makro oder zur Inlinefunktion aus|  
|**Nicht zutreffend**|**Nicht zutreffend**|`_mbsncmp_l`|**Nicht zutreffend**|  
  
## <a name="requirements"></a>Anforderungen  
  
|Routine|Erforderlicher Header|  
|-------------|---------------------|  
|`strncmp`|\<string.h>|  
|`wcsncmp`|\<string.h> oder \<wchar.h>|  
|`_mbsncmp`, `_mbsncmp_l`|\<mbstring.h>|  
  
 Weitere Informationen zur Kompatibilität finden Sie unter [Kompatibilität](../../c-runtime-library/compatibility.md).  
  
## <a name="example"></a>Beispiel  
  
```  
// crt_strncmp.c  
#include <string.h>  
#include <stdio.h>  
  
char string1[] = "The quick brown dog jumps over the lazy fox";  
char string2[] = "The QUICK brown fox jumps over the lazy dog";  
  
int main( void )  
{  
   char tmp[20];  
   int result;  
   printf( "Compare strings:\n      %s\n      %s\n\n",  
           string1, string2 );  
   printf( "Function:   strncmp (first 10 characters only)\n" );  
   result = strncmp( string1, string2 , 10 );  
   if( result > 0 )  
      strcpy_s( tmp, sizeof(tmp), "greater than" );  
   else if( result < 0 )  
      strcpy_s( tmp, sizeof(tmp), "less than" );  
   else  
      strcpy_s( tmp, sizeof(tmp), "equal to" );  
   printf( "Result:      String 1 is %s string 2\n\n", tmp );  
   printf( "Function:   strnicmp _strnicmp (first 10 characters only)\n" );  
   result = _strnicmp( string1, string2, 10 );  
   if( result > 0 )  
      strcpy_s( tmp, sizeof(tmp), "greater than" );  
   else if( result < 0 )  
      strcpy_s( tmp, sizeof(tmp), "less than" );  
   else  
      strcpy_s( tmp, sizeof(tmp), "equal to" );  
   printf( "Result:      String 1 is %s string 2\n", tmp );  
}  
```  
  
```Output  
Compare strings:  
      The quick brown dog jumps over the lazy fox  
      The QUICK brown fox jumps over the lazy dog  
  
Function:   strncmp (first 10 characters only)  
Result:      String 1 is greater than string 2  
  
Function:   strnicmp _strnicmp (first 10 characters only)  
Result:      String 1 is equal to string 2  
```  
  
## <a name="see-also"></a>Siehe auch  
 [Zeichenfolgenbearbeitung](../../c-runtime-library/string-manipulation-crt.md)   
 [Locale](../../c-runtime-library/locale.md)   
 [Interpretation von Multibyte-Zeichensequenzen](../../c-runtime-library/interpretation-of-multibyte-character-sequences.md)   
 [_mbsnbcmp, _mbsnbcmp_l](../../c-runtime-library/reference/mbsnbcmp-mbsnbcmp-l.md)   
 [_mbsnbicmp, _mbsnbicmp_l](../../c-runtime-library/reference/mbsnbicmp-mbsnbicmp-l.md)   
 [strcmp, wcscmp, _mbscmp](../../c-runtime-library/reference/strcmp-wcscmp-mbscmp.md)   
 [strcoll-Funktionen](../../c-runtime-library/strcoll-functions.md)   
 [_strnicmp, _wcsnicmp, _mbsnicmp, _strnicmp_l, _wcsnicmp_l, _mbsnicmp_l](../../c-runtime-library/reference/strnicmp-wcsnicmp-mbsnicmp-strnicmp-l-wcsnicmp-l-mbsnicmp-l.md)   
 [strrchr, wcsrchr, _mbsrchr, _mbsrchr_l](../../c-runtime-library/reference/strrchr-wcsrchr-mbsrchr-mbsrchr-l.md)   
 [_strset, _strset_l, _wcsset, _wcsset_l, _mbsset, _mbsset_l](../../c-runtime-library/reference/strset-strset-l-wcsset-wcsset-l-mbsset-mbsset-l.md)   
 [strspn, wcsspn, _mbsspn, _mbsspn_l](../../c-runtime-library/reference/strspn-wcsspn-mbsspn-mbsspn-l.md)
