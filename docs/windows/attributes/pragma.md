---
title: 'pragma (c + + COM 特性) '
ms.date: 10/02/2018
f1_keywords:
- vc-attr.pragma
helpviewer_keywords:
- pragma attribute
ms.assetid: 3f90d023-b8b5-4007-8311-008bb72cbea1
ms.openlocfilehash: e5683a6f52eccf9eae7c29010849a148e506b286
ms.sourcegitcommit: ec6dd97ef3d10b44e0fedaa8e53f41696f49ac7b
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/25/2020
ms.locfileid: "88836164"
---
# <a name="pragma"></a>pragma

向生成的 .idl 文件发出指定的字符串，且不使用引号。

## <a name="syntax"></a>语法

```cpp
[ pragma(pragma_statement) ];
```

### <a name="parameters"></a>参数

*pragma_statement*<br/>
要进入生成的 .idl 文件的杂注。

## <a name="remarks"></a>注解

**Pragma** c + + 属性与[杂注](/windows/win32/Midl/pragma)MIDL 特性具有相同的功能。

## <a name="example"></a>示例

```cpp
// cpp_attr_ref_pragma.cpp
// compile with: /LD
#include "unknwn.h"
[module(name="MyLib")];
[pragma(pack(4))];

[dispinterface, uuid("00000000-0000-0000-0000-000000000001")]
__interface A
{
   [id(1)] HRESULT MyMethod ([in, satype("BSTR")] SAFEARRAY **p);
};
```

## <a name="requirements"></a>要求

| 特性上下文 | 值 |
|-|-|
|**适用于**|任何位置|
|**且**|否|
|**必需属性**|无|
|**无效的特性**|无|

有关特性上下文的详细信息，请参见 [特性上下文](cpp-attributes-com-net.md#contexts)。

## <a name="see-also"></a>另请参阅

[IDL 特性](idl-attributes.md)<br/>
[独立属性](stand-alone-attributes.md)<br/>
[pack](../../preprocessor/pack.md)
