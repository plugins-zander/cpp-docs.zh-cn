---
title: "编译器错误 C3368 |Microsoft 文档"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-tools
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords: C3368
dev_langs: C++
helpviewer_keywords: C3368
ms.assetid: 5bfd5be4-dfa9-4b33-9612-010561b40955
caps.latest.revision: "7"
author: corob-msft
ms.author: corob
manager: ghogen
ms.openlocfilehash: 86996ade6501ba83e1895f6ba9b30d62526ff442
ms.sourcegitcommit: ebec1d449f2bd98aa851667c2bfeb7e27ce657b2
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/24/2017
---
# <a name="compiler-error-c3368"></a>编译器错误 C3368
“function declaration”：IDL 的调用约定无效  
  
 你只能在 .idl 文件中使用 [__stdcall](../../cpp/stdcall.md) 或 [__cdecl](../../cpp/cdecl.md) 调用约定。  
  
 以下示例生成 C3368：  
  
```  
// C3368.cpp  
// processor: x86  
[idl_module(name="Name", dllname="Some.dll")];  
  
[idl_module(name="Name")]  
int __fastcall f1();   // C3368  
```