---
title: 'Concurrency:: Graphics-Namespace Funktionen | Microsoft Docs'
ms.custom: ''
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- amp_graphics/Concurrency::fast_math::copy_async
- amp_graphics/Concurrency::fast_math::copy
dev_langs:
- C++
ms.assetid: ace01cd5-29d3-4356-930e-c81a61c5f934
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: 8fc00f1754358eca0d6e90d484153b79c0a67130
ms.sourcegitcommit: 7019081488f68abdd5b2935a3b36e2a5e8c571f8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/07/2018
---
# <a name="concurrencygraphics-namespace-functions"></a>Concurrency:: Graphics-Namespace-Funktionen
|||  
|-|-|  
|[copy](#copy)|[copy_async](#copy_async)|  
  
##  <a name="copy"></a>  Copy-Funktion (Concurrency:: Graphics-Namespace)  
 Kopiert eine Quelltextur in einen Zielpuffer oder kopiert einen Quellpuffer in einen Zielpuffer. Das allgemeine Format dieser Funktion ist `copy(src, dest)`.  
  
```  
template <
    typename _Src_type,  
    typename = typename std::enable_if<details::texture_traits<_Src_type>::is_texture, void>::type>  
>  
void copy (
    const _Src_type& _Src,  
    _Out_ void* _Dst,  
    unsigned int _Dst_byte_size);

 
template <
    typename _Src_type,  
    typename = typename std::enable_if<details::texture_traits<_Src_type>::is_texture, void>::type  
>  
void copy(
    const _Src_type& _Src,  
    const index<_Src_type::rank>& _Src_offset,  
    const extent<_Src_type::rank>& _Copy_extent,  
    _Out_ void* _Dst,  
    unsigned int _Dst_byte_size);

 
template <
    typename _Dst_type,  
    typename = typename std::enable_if<details::texture_traits<_Dst_type>::is_texture, void>::type  
>  
void copy(
    const void* _Src,  
    unsigned int _Src_byte_size, _Dst_type& _Dst);

 
template <
    typename _Dst_type,  
    typename = typename std::enable_if<details::texture_traits<_Dst_type>::is_texture, void>::type  
>  
void copy(
    const void* _Src,  
    unsigned int _Src_byte_size,  
    _Dst_type& _Dst,  
    const index<_Dst_type::rank>& _Dst_offset,  
    const extent<_Dst_type::rank>& _Copy_extent);

 
template <
    typename InputIterator,  
    typename _Dst_type,  
    typename = typename std::enable_if<details::texture_traits<_Dst_type>::is_texture, void>::type  
>  
void copy(InputIterator first, InputIterator last, _Dst_type& _Dst);

 
template <
    typename InputIterator,  
    typename _Dst_type,  
    typename = typename std::enable_if<details::texture_traits<_Dst_type>::is_texture, void>::type  
>void copy(InputIterator first, InputIterator last, _Dst_type& _Dst,  
    const index<_Dst_type::rank>& _Dst_offset,  
    const extent<_Dst_type::rank>& _Copy_extent);

 
template <
    typename _Src_type,  
    typename OutputIterator,  
    typename = typename std::enable_if<details::texture_traits<_Src_type>::is_texture&& !details::texture_traits<OutputIterator>::is_texture, void>::type  
>  
void copy(
    const _Src_type& _Src, OutputIterator _Dst);

 
template <
    typename _Src_type,  
    typename OutputIterator,  
    typename = typename std::enable_if<details::texture_traits<_Src_type>::is_texture&& !details::texture_traits<OutputIterator>::is_texture, void>::type  
>  
void copy (
    const _Src_type& _Src,  
    const index<_Src_type::rank>& _Src_offset,  
    const extent<_Src_type::rank>& _Copy_extent, OutputIterator _Dst);

 
template <
    typename _Src_type,  
    typename _Dst_type,  
    typename = typename std::enable_if<details::texture_traits<_Src_type>::is_texture&& details::texture_traits<_Dst_type>::is_texture, void>::type  
>  
void copy (
    const _Src_type& _Src, _Dst_type& _Dst);

 
template <
    typename _Src_type,  
    typename _Dst_type,  
    typename = typename std::enable_if<details::texture_traits<_Src_type>::is_texture&& details::texture_traits<_Dst_type>::is_texture,  
    void>::type 
>  
void copy (
    const _Src_type& _Src,  
    const index<_Src_type::rank>& _Src_offset, _Dst_type& _Dst,  
    const index<_Dst_type::rank>& _Dst_offset,  
    const extent<_Src_type::rank>& _Copy_extent);
```  
  
### <a name="parameters"></a>Parameter  
 `_Copy_extent`  
 Der Umfang des zu kopierenden Texturabschnitts.  
  
 `_Dst`  
 Das Objekt, in das kopiert werden soll.  
  
 `_Dst_byte_size`  
 Die Anzahl von Bytes im Ziel.  
  
 `_Dst_type`  
 Der Typ des Zielobjekts.  
  
 `_Dst_offset`  
 Der Offset in das Ziel, an dem der Kopiervorgang beginnen soll.  
  
 `InputIterator`  
 Der Typ des Eingabeiterators.  
  
 `OutputIterator`  
 Der Typ des Ausgabeiterators.  
  
 `_Src`  
 Das zu kopierende Objekt.  
  
 `_Src_byte_size`  
 Die Anzahl von Bytes in der Quelle.  
  
 `_Src_type`  
 Der Typ des Quellobjekts.  
  
 `_Src_offset`  
 Der Offset in der Quelle, an der der Kopiervorgang beginnen soll.  
  
 `first`  
 Ein Anfangsiterator in den Quellcontainer.  
  
 `last`  
 Ein Endeiterator in den Quellcontainer.  
  
##  <a name="copy_async"></a>  Copy_async-Funktion (Concurrency:: Graphics-Namespace)  
 Kopiert asynchron eine Quelltextur in einen Zielpuffer oder kopiert einen Quellpuffer in einen Zielpuffer und gibt eine [Completion_future](completion-future-class.md) -Objekt, das auf das gewartet werden kann. Es können keine Daten kopiert werden, wenn auf einer Zugriffstaste Code ausgeführt wird. Das allgemeine Format dieser Funktion ist `copy(src, dest)`.  
  
```  
template<
    typename _Src_type,  
    typename = typename std::enable_if<details::texture_traits<_Src_type>::is_texture, void>::type  
>  
concurrency::completion_future copy_async(
    const _Src_type& _Src,  
    _Out_ void* _Dst,  
    unsigned int _Dst_byte_size);

 
template<
    typename _Src_type,  
    typename = typename std::enable_if<details::texture_traits<_Src_type>::is_texture, void>::type  
>  
concurrency::completion_future copy_async(
    const _Src_type& _Src,  
    const index<_Src_type::rank>& _Src_offset,  
    const extent<_Src_type::rank>& _Copy_extent,  
    _Out_ void* _Dst,  
    unsigned int _Dst_byte_size);

 
template <
    typename _Dst_type,  
    typename = typename std::enable_if<details::texture_traits<_Dst_type>::is_texture, void>::type  
>  
concurrency::completion_future copy_async(
    const void* _Src,  
    unsigned int _Src_byte_size, _Dst_type& _Dst);

 
template <
    typename _Dst_type,  
    typename = typename std::enable_if<details::texture_traits<_Dst_type>::is_texture, void>::type  
>  
concurrency::completion_future copy_async(
    const void* _Src,  
    unsigned int _Src_byte_size, _Dst_type& _Dst,  
    const index<_Dst_type::rank>& _Dst_offset,  
    const extent<_Dst_type::rank>& _Copy_extent);

 
template <
    typename InputIterator,  
    typename _Dst_type,  
    typename = typename std::enable_if<details::texture_traits<_Dst_type>::is_texture, void>::type  
>  
concurrency::completion_future copy_async(InputIterator first, InputIterator last, _Dst_type& _Dst);

 
template <
    typename InputIterator,  
    typename _Dst_type,  
    typename = typename std::enable_if<details::texture_traits<_Dst_type>::is_texture, void>::type  
>  
concurrency::completion_future copy_async(InputIterator first, InputIterator last, _Dst_type& _Dst,  
    const index<_Dst_type::rank>& _Dst_offset,  
    const extent<_Dst_type::rank>& _Copy_extent);

 
template <
    typename _Src_type,  
    typename OutputIterator,  
    typename = typename std::enable_if<details::texture_traits<_Src_type>::is_texture&& !details::texture_traits<OutputIterator>::is_texture, void>::type  
>  
concurrency::completion_future copy_async(_Src_type& _Src, OutputIterator _Dst);

 
template <
    typename _Src_type,  
    typename OutputIterator,  
    typename = typename std::enable_if<details::texture_traits<_Src_type>::is_texture&& !details::texture_traits<OutputIterator>::is_texture, void>::type  
>  
concurrency::completion_future copy_async(_Src_type& _Src,  
    const index<_Src_type::rank>& _Src_offset,  
    const extent<_Src_type::rank>& _Copy_extent,  
    OutputIterator _Dst);

 
template <
    typename _Src_type,  
    typename _Dst_type,  
    typename = typename std::enable_if<details::texture_traits<_Src_type>::is_texture&& details::texture_traits<_Dst_type>::is_texture, void>::type  
>  
concurrency::completion_future copy_async(_Src_type& _Src, _Dst_type& _Dst);

 
template <
    typename _Src_type,  
    typename _Dst_type,  
    typename = typename std::enable_if<details::texture_traits<_Src_type>::is_texture&& details::texture_traits<_Dst_type>::is_texture, void>::type  
>  
concurrency::completion_future copy_async(_Src_type& _Src,  
    const index<_Src_type::rank>& _Src_offset, _Dst_type &_Dst,  
    const index<_Dst_type::rank>& _Dst_offset,  
    const extent<_Src_type::rank>& _Copy_extent);
```  
  
### <a name="parameters"></a>Parameter  
 `_Copy_extent`  
 Der Umfang des zu kopierenden Texturabschnitts.  
  
 `_Dst`  
 Das Objekt, in das kopiert werden soll.  
  
 `_Dst_byte_size`  
 Die Anzahl von Bytes im Ziel.  
  
 `_Dst_type`  
 Der Typ des Zielobjekts.  
  
 `_Dst_offset`  
 Der Offset in das Ziel, an dem der Kopiervorgang beginnen soll.  
  
 `InputIterator`  
 Der Typ des Eingabeiterators.  
  
 `OutputIterator`  
 Der Typ des Ausgabeiterators.  
  
 `_Src`  
 Das zu kopierende Objekt.  
  
 `_Src_byte_size`  
 Die Anzahl von Bytes in der Quelle.  
  
 `_Src_type`  
 Der Typ des Quellobjekts.  
  
 `_Src_offset`  
 Der Offset in der Quelle, an der der Kopiervorgang beginnen soll.  
  
 `first`  
 Ein Anfangsiterator in den Quellcontainer.  
  
 `last`  
 Ein Endeiterator in den Quellcontainer.  

## <a name="requirements"></a>Anforderungen  
 **Header:** amp_graphics.h  
  
 **Namespace:** Concurrency:: Graphics 

## <a name="see-also"></a>Siehe auch  
 [Concurrency::graphics Namespace](concurrency-graphics-namespace.md)
