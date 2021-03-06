---
title: CD2DBitmap-Klasse | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-mfc
ms.topic: reference
f1_keywords:
- CD2DBitmap
- AFXRENDERTARGET/CD2DBitmap
- AFXRENDERTARGET/CD2DBitmap::CD2DBitmap
- AFXRENDERTARGET/CD2DBitmap::Attach
- AFXRENDERTARGET/CD2DBitmap::CopyFromBitmap
- AFXRENDERTARGET/CD2DBitmap::CopyFromMemory
- AFXRENDERTARGET/CD2DBitmap::CopyFromRenderTarget
- AFXRENDERTARGET/CD2DBitmap::Create
- AFXRENDERTARGET/CD2DBitmap::Destroy
- AFXRENDERTARGET/CD2DBitmap::Detach
- AFXRENDERTARGET/CD2DBitmap::Get
- AFXRENDERTARGET/CD2DBitmap::GetDPI
- AFXRENDERTARGET/CD2DBitmap::GetPixelFormat
- AFXRENDERTARGET/CD2DBitmap::GetPixelSize
- AFXRENDERTARGET/CD2DBitmap::GetSize
- AFXRENDERTARGET/CD2DBitmap::IsValid
- AFXRENDERTARGET/CD2DBitmap::CommonInit
- AFXRENDERTARGET/CD2DBitmap::m_bAutoDestroyHBMP
- AFXRENDERTARGET/CD2DBitmap::m_hBmpSrc
- AFXRENDERTARGET/CD2DBitmap::m_lpszType
- AFXRENDERTARGET/CD2DBitmap::m_pBitmap
- AFXRENDERTARGET/CD2DBitmap::m_sizeDest
- AFXRENDERTARGET/CD2DBitmap::m_strPath
- AFXRENDERTARGET/CD2DBitmap::m_uiResID
dev_langs:
- C++
helpviewer_keywords:
- CD2DBitmap [MFC], CD2DBitmap
- CD2DBitmap [MFC], CD2DBitmap
- CD2DBitmap [MFC], Attach
- CD2DBitmap [MFC], CopyFromBitmap
- CD2DBitmap [MFC], CopyFromMemory
- CD2DBitmap [MFC], CopyFromRenderTarget
- CD2DBitmap [MFC], Create
- CD2DBitmap [MFC], Destroy
- CD2DBitmap [MFC], Detach
- CD2DBitmap [MFC], Get
- CD2DBitmap [MFC], GetDPI
- CD2DBitmap [MFC], GetPixelFormat
- CD2DBitmap [MFC], GetPixelSize
- CD2DBitmap [MFC], GetSize
- CD2DBitmap [MFC], IsValid
- CD2DBitmap [MFC], CommonInit
- CD2DBitmap [MFC], m_bAutoDestroyHBMP
- CD2DBitmap [MFC], m_hBmpSrc
- CD2DBitmap [MFC], m_lpszType
- CD2DBitmap [MFC], m_pBitmap
- CD2DBitmap [MFC], m_sizeDest
- CD2DBitmap [MFC], m_strPath
- CD2DBitmap [MFC], m_uiResID
ms.assetid: 2b3686f1-812c-462b-b449-9f0cb6949bf6
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: b92587d6cad3004c87ee6aee4716888d09c1270a
ms.sourcegitcommit: 76b7653ae443a2b8eb1186b789f8503609d6453e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/04/2018
---
# <a name="cd2dbitmap-class"></a>CD2DBitmap-Klasse
Ein Wrapper für ID2D1Bitmap.  
  
## <a name="syntax"></a>Syntax  
  
```  
class CD2DBitmap : public CD2DResource;  
```  
  
## <a name="members"></a>Member  
  
### <a name="public-constructors"></a>Öffentliche Konstruktoren  
  
|Name|Beschreibung|  
|----------|-----------------|  
|[CD2DBitmap::CD2DBitmap](#cd2dbitmap)|Überladen. Erstellt ein CD2DBitmap-Objekt aus HBITMAP.|  
|[CD2DBitmap:: ~ CD2DBitmap](#_dtorcd2dbitmap)|Der Destruktor. Wird aufgerufen, wenn ein D2D-Bitmap-Objekt zerstört wird.|  
  
### <a name="protected-constructors"></a>Geschützte Konstruktoren  
  
|Name|Beschreibung|  
|----------|-----------------|  
|[CD2DBitmap::CD2DBitmap](#cd2dbitmap)|Überladen. Erstellt ein CD2DBitmap-Objekt.|  
  
### <a name="public-methods"></a>Öffentliche Methoden  
  
|Name|Beschreibung|  
|----------|-----------------|  
|[CD2DBitmap::Attach](#attach)|Hängt die vorhandene Ressourcenschnittstelle, um das Objekt|  
|[CD2DBitmap::CopyFromBitmap](#copyfrombitmap)|Kopiert den angegebenen Bereich aus der angegebenen Bitmap in die aktuelle bitmap|  
|[CD2DBitmap::CopyFromMemory](#copyfrommemory)|Kopiert den angegebenen Bereich aus dem Arbeitsspeicher in die aktuelle bitmap|  
|[CD2DBitmap::CopyFromRenderTarget](#copyfromrendertarget)|Kopiert der angegebene Bereich aus dem angegebenen Renderziel in die aktuelle bitmap|  
|[CD2DBitmap::Create](#create)|Erstellt eine CD2DBitmap. (Überschreibt [CD2DResource:: Create](../../mfc/reference/cd2dresource-class.md#create).)|  
|[CD2DBitmap::Destroy](#destroy)|Zerstört ein CD2DBitmap-Objekt. (Überschreibt [CD2DResource:: Destroy](../../mfc/reference/cd2dresource-class.md#destroy).)|  
|[CD2DBitmap::Detach](#detach)|Trennt Ressourcenschnittstelle aus dem Objekt|  
|[CD2DBitmap::Get](#get)|Gibt die ID2D1Bitmap-Schnittstelle|  
|[CD2DBitmap::GetDPI](#getdpi)|Die Punkte pro Zoll (DPI) der Bitmap zurück|  
|[CD2DBitmap::GetPixelFormat](#getpixelformat)|Ruft das Pixelformat Format und Alpha der Bitmap ab|  
|[CD2DBitmap::GetPixelSize](#getpixelsize)|Gibt die Größe in geräteabhängige Einheiten (in Pixel), der bitmap|  
|[CD2DBitmap::GetSize](#getsize)|Gibt die Größe in geräteunabhängigen Pixeln (DIPs), der bitmap|  
|[CD2DBitmap::IsValid](#isvalid)|Überprüft die Gültigkeit der Ressource (Außerkraftsetzungen [CD2DResource::IsValid](../../mfc/reference/cd2dresource-class.md#isvalid).)|  
  
### <a name="protected-methods"></a>Geschützte Methoden  
  
|Name|Beschreibung|  
|----------|-----------------|  
|[CD2DBitmap::CommonInit](#commoninit)|Initialisiert das Objekt|  
  
### <a name="public-operators"></a>Öffentliche Operatoren  
  
|Name|Beschreibung|  
|----------|-----------------|  
|[CD2DBitmap::Operator ID2D1Bitmap *](#operator_id2d1bitmap_star)|Gibt die ID2D1Bitmap-Schnittstelle|  
  
### <a name="protected-data-members"></a>Geschützte Datenmember  
  
|name|Beschreibung|  
|----------|-----------------|  
|[CD2DBitmap::m_bAutoDestroyHBMP](#m_bautodestroyhbmp)|True, wenn M_hBmpSrc zerstört werden soll. andernfalls "false".|  
|[CD2DBitmap::m_hBmpSrc](#m_hbmpsrc)|Das Quellhandle mithilfe einer Bitmap.|  
|[CD2DBitmap::m_lpszType](#m_lpsztype)|Der Ressourcentyp.|  
|[CD2DBitmap::m_pBitmap](#m_pbitmap)|Speichert einen Zeiger auf ein ID2D1Bitmap-Objekt.|  
|[CD2DBitmap::m_sizeDest](#m_sizedest)|Bitmap Zielgröße.|  
|[CD2DBitmap::m_strPath](#m_strpath)|Botmap Dateipfad.|  
|[CD2DBitmap::m_uiResID](#m_uiresid)|Bitmap-Ressourcen-ID.|  
  
## <a name="inheritance-hierarchy"></a>Vererbungshierarchie  
 [CObject](../../mfc/reference/cobject-class.md)  
  
 [CD2DResource](../../mfc/reference/cd2dresource-class.md)  
  
 `CD2DBitmap`
  
## <a name="requirements"></a>Anforderungen  
 **Header:** afxrendertarget.h  
  
##  <a name="_dtorcd2dbitmap"></a>  CD2DBitmap:: ~ CD2DBitmap  
 Der Destruktor. Wird aufgerufen, wenn ein D2D-Bitmap-Objekt zerstört wird.  
  
```  
virtual ~CD2DBitmap();
```  
  
##  <a name="attach"></a>  CD2DBitmap::Attach  
 Hängt die vorhandene Ressourcenschnittstelle, um das Objekt  
  
```  
void Attach(ID2D1Bitmap* pResource);
```  
  
### <a name="parameters"></a>Parameter  
 `pResource`  
 Vorhandene Ressourcenschnittstelle. NULL darf nicht sein  
  
##  <a name="cd2dbitmap"></a>  CD2DBitmap::CD2DBitmap  
 Erstellt ein CD2DBitmap-Objekt aus der Ressource.  
  
```  
CD2DBitmap(
    CRenderTarget* pParentTarget,  
    UINT uiResID,  
    LPCTSTR lpszType = NULL,  
    CD2DSizeU sizeDest = CD2DSizeU(0, 0), 
    BOOL bAutoDestroy = TRUE);

 
CD2DBitmap(
    CRenderTarget* pParentTarget,  
    LPCTSTR lpszPath,  
    CD2DSizeU sizeDest = CD2DSizeU(0, 0), 
    BOOL bAutoDestroy = TRUE);

 
CD2DBitmap(
    CRenderTarget* pParentTarget,  
    HBITMAP hbmpSrc,  
    CD2DSizeU sizeDest = CD2DSizeU(0, 0), 
    BOOL bAutoDestroy = TRUE);

 
CD2DBitmap(
    CRenderTarget* pParentTarget,  
    BOOL bAutoDestroy = TRUE);
```  
  
### <a name="parameters"></a>Parameter  
 `pParentTarget`  
 Ein Zeiger auf das Renderziel.  
  
 `uiResID`  
 Die Ressourcen-ID-Nummer der Ressource.  
  
 `lpszType`  
 Ein Zeiger auf eine auf Null endende Zeichenfolge, die den Ressourcentyp enthält.  
  
 `sizeDest`  
 Die Zielgröße der Bitmap.  
  
 `bAutoDestroy`  
 Gibt an, dass das Objekt vom Besitzer (pParentTarget) zerstört wird.  
  
 `lpszPath`  
 Ein Zeiger auf eine auf Null endende Zeichenfolge, die den Namen der Datei enthält.  
  
 `hbmpSrc`  
 Handle für die Bitmap.  
  
##  <a name="commoninit"></a>  CD2DBitmap::CommonInit  
 Initialisiert das Objekt  
  
```  
void CommonInit();
```  
  
##  <a name="copyfrombitmap"></a>  CD2DBitmap::CopyFromBitmap  
 Kopiert den angegebenen Bereich aus der angegebenen Bitmap in die aktuelle bitmap  
  
```  
HRESULT CopyFromBitmap(
    const CD2DBitmap* pBitmap,  
    const CD2DPointU* destPoint = NULL,  
    const CD2DRectU* srcRect = NULL);
```  
  
### <a name="parameters"></a>Parameter  
 `pBitmap`  
 Die Bitmap aus kopieren  
  
 `destPoint`  
 In der aktuellen Bitmap wird der linken oberen Ecke des Bereichs, der der Bereich durch SrcRect angegebene, kopiert.  
  
 `srcRect`  
 Der Bereich der Bitmap kopieren  
  
### <a name="return-value"></a>Rückgabewert  
 Wenn die Methode erfolgreich ist, wird S_OK zurückgegeben. Andernfalls wird einen HRESULT-Fehlercode zurückgegeben.  
  
##  <a name="copyfrommemory"></a>  CD2DBitmap::CopyFromMemory  
 Kopiert den angegebenen Bereich aus dem Arbeitsspeicher in die aktuelle bitmap  
  
```  
HRESULT CopyFromMemory(
    const void* srcData,  
    UINT32 pitch,  
    const CD2DRectU* destRect = NULL);
```  
  
### <a name="parameters"></a>Parameter  
 `srcData`  
 Die zu kopierenden Daten  
  
 `pitch`  
 Der Stride oder Tonhöhe, der die Quellbitmap in SrcData gespeichert. Stride ist die Byteanzahl, die von einer Scanzeile (eine Zeile der Pixel im Arbeitsspeicher). Stride aus der folgenden Formel berechnet werden kann: Pixelbreite * Bytes pro Pixel + Auffüllung der Speicher  
  
 `destRect`  
 In der aktuellen Bitmap wird der linken oberen Ecke des Bereichs, der der Bereich durch SrcRect angegebene, kopiert.  
  
### <a name="return-value"></a>Rückgabewert  
 Wenn die Methode erfolgreich ist, wird S_OK zurückgegeben. Andernfalls wird einen HRESULT-Fehlercode zurückgegeben.  
  
##  <a name="copyfromrendertarget"></a>  CD2DBitmap::CopyFromRenderTarget  
 Kopiert der angegebene Bereich aus dem angegebenen Renderziel in die aktuelle bitmap  
  
```  
HRESULT CopyFromRenderTarget(
    const CRenderTarget* pRenderTarget,  
    const CD2DPointU* destPoint = NULL,  
    const CD2DRectU* srcRect = NULL);
```  
  
### <a name="parameters"></a>Parameter  
 `pRenderTarget`  
 Das Renderziel, das die zu kopierenden Bereich enthält  
  
 `destPoint`  
 In der aktuellen Bitmap wird der linken oberen Ecke des Bereichs, der der Bereich durch SrcRect angegebene, kopiert.  
  
 `srcRect`  
 Der Bereich der Renderziel kopieren  
  
### <a name="return-value"></a>Rückgabewert  
 Wenn die Methode erfolgreich ist, wird S_OK zurückgegeben. Andernfalls wird einen HRESULT-Fehlercode zurückgegeben.  
  
##  <a name="create"></a>  CD2DBitmap::Create  
 Erstellt eine CD2DBitmap.  
  
```  
virtual HRESULT Create(CRenderTarget* pRenderTarget);
```  
  
### <a name="parameters"></a>Parameter  
 `pRenderTarget`  
 Ein Zeiger auf das Renderziel.  
  
### <a name="return-value"></a>Rückgabewert  
 Wenn die Methode erfolgreich ist, wird S_OK zurückgegeben. Andernfalls wird einen HRESULT-Fehlercode zurückgegeben.  
  
##  <a name="destroy"></a>  CD2DBitmap::Destroy  
 Zerstört ein CD2DBitmap-Objekt.  
  
```  
virtual void Destroy();
```  
  
##  <a name="detach"></a>  CD2DBitmap::Detach  
 Trennt Ressourcenschnittstelle aus dem Objekt  
  
```  
ID2D1Bitmap* Detach();
```  
  
### <a name="return-value"></a>Rückgabewert  
 Zeiger auf getrennten Ressourcenschnittstelle.  
  
##  <a name="get"></a>  CD2DBitmap::Get  
 Gibt die ID2D1Bitmap-Schnittstelle  
  
```  
ID2D1Bitmap* Get();
```  
  
### <a name="return-value"></a>Rückgabewert  
 Ein Zeiger auf eine ID2D1Bitmap-Schnittstelle oder NULL, wenn das Objekt noch nicht initialisiert ist.  
  
##  <a name="getdpi"></a>  CD2DBitmap::GetDPI  
 Die Punkte pro Zoll (DPI) der Bitmap zurück  
  
```  
CD2DSizeF GetDPI() const;  
```  
  
### <a name="return-value"></a>Rückgabewert  
 Der horizontale und vertikale DPI der Bitmap.  
  
##  <a name="getpixelformat"></a>  CD2DBitmap::GetPixelFormat  
 Ruft das Pixelformat Format und Alpha der Bitmap ab  
  
```  
D2D1_PIXEL_FORMAT GetPixelFormat() const;  
```  
  
### <a name="return-value"></a>Rückgabewert  
 Die Pixel-Format und Alpha-Modus der Bitmap.  
  
##  <a name="getpixelsize"></a>  CD2DBitmap::GetPixelSize  
 Gibt die Größe in geräteabhängige Einheiten (in Pixel), der bitmap  
  
```  
CD2DSizeU GetPixelSize() const;  
```  
  
### <a name="return-value"></a>Rückgabewert  
 Die Größe in Pixel der Bitmap...  
  
##  <a name="getsize"></a>  CD2DBitmap::GetSize  
 Gibt die Größe in geräteunabhängigen Pixeln (DIPs), der bitmap  
  
```  
CD2DSizeF GetSize() const;  
```  
  
### <a name="return-value"></a>Rückgabewert  
 Die Größe in der Bitmap für die DIPs.  
  
##  <a name="isvalid"></a>  CD2DBitmap::IsValid  
 Die Ressource Gültigkeit überprüft  
  
```  
virtual BOOL IsValid() const;  
```  
  
### <a name="return-value"></a>Rückgabewert  
 True, wenn die Ressource gültig ist. andernfalls "false".  
  
##  <a name="m_bautodestroyhbmp"></a>  CD2DBitmap::m_bAutoDestroyHBMP  
 True, wenn M_hBmpSrc zerstört werden soll. andernfalls "false".  
  
```  
BOOL m_bAutoDestroyHBMP;  
```  
  
##  <a name="m_hbmpsrc"></a>  CD2DBitmap::m_hBmpSrc  
 Das Quellhandle mithilfe einer Bitmap.  
  
```  
HBITMAP m_hBmpSrc;  
```  
  
##  <a name="m_lpsztype"></a>  CD2DBitmap::m_lpszType  
 Der Ressourcentyp.  
  
```  
LPCTSTR m_lpszType;  
```  
  
##  <a name="m_pbitmap"></a>  CD2DBitmap::m_pBitmap  
 Speichert einen Zeiger auf ein ID2D1Bitmap-Objekt.  
  
```  
ID2D1Bitmap* m_pBitmap;  
```  
  
##  <a name="m_sizedest"></a>  CD2DBitmap::m_sizeDest  
 Bitmap Zielgröße.  
  
```  
CD2DSizeU m_sizeDest;  
```  
  
##  <a name="m_strpath"></a>  CD2DBitmap::m_strPath  
 Botmap Dateipfad.  
  
```  
CString m_strPath;  
```  
  
##  <a name="m_uiresid"></a>  CD2DBitmap::m_uiResID  
 Bitmap-Ressourcen-ID.  
  
```  
UINT m_uiResID;  
```  
  
##  <a name="operator_id2d1bitmap_star"></a>  CD2DBitmap::Operator ID2D1Bitmap *  
 Gibt die ID2D1Bitmap-Schnittstelle  
  
```  
operator ID2D1Bitmap*();
```   
  
### <a name="return-value"></a>Rückgabewert  
 Ein Zeiger auf eine ID2D1Bitmap-Schnittstelle oder NULL, wenn das Objekt noch nicht initialisiert ist.  
  
## <a name="see-also"></a>Siehe auch  
 [Klassen](../../mfc/reference/mfc-classes.md)
