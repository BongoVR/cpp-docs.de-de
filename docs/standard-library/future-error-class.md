---
title: future_error-Klasse | Microsoft-Dokumentation
ms.custom: ''
ms.date: 11/04/2016
ms.reviewer: ''
ms.suite: ''
ms.technology:
- cpp-standard-libraries
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- future/std::future_error
dev_langs:
- C++
ms.assetid: 6071c545-ac2a-49ef-9967-07b0125da861
caps.latest.revision: 13
author: corob-msft
ms.author: corob
manager: ghogen
ms.workload:
- cplusplus
ms.openlocfilehash: 8bb570a7f3a880795add320371a8472f4816a0f3
ms.sourcegitcommit: dd1a509526fa8bb18e97ab7bc7b91cbdb3ec7059
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2018
---
# <a name="futureerror-class"></a>future_error-Klasse

Beschreibt ein Ausnahmeobjekt, das von Methoden der Typen ausgelöst werden kann, die [future](../standard-library/future-class.md)-Objekte verwalten.

## <a name="syntax"></a>Syntax

```cpp
class future_error : public logic_error {
public:
    future_error(error_code code);

const error_code& code() const throw();

const char *what() const throw();

};
```

## <a name="requirements"></a>Anforderungen

**Header:** \<zukünftige >

**Namespace:** std

## <a name="see-also"></a>Siehe auch

[Headerdateienreferenz](../standard-library/cpp-standard-library-header-files.md)<br/>
[logic_error-Klasse](../standard-library/logic-error-class.md)<br/>
[error_code-Klasse](../standard-library/error-code-class.md)<br/>
