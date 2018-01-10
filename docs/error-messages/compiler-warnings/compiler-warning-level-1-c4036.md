---
title: "编译器警告 （等级 1） C4036 |Microsoft 文档"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- cpp-tools
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- C4036
dev_langs:
- C++
helpviewer_keywords:
- C4036
ms.assetid: f0b15359-4d62-48ec-8cb1-a7b36587a47f
caps.latest.revision: 10
author: corob-msft
ms.author: corob
manager: ghogen
ms.translationtype: MT
ms.sourcegitcommit: 35b46e23aeb5f4dbfd2a0dd44b906389dd5bfc88
ms.openlocfilehash: 6392ba12c14ca3ef89f992e358bf019d1d92e5db
ms.contentlocale: zh-cn
ms.lasthandoff: 10/10/2017

---
# <a name="compiler-warning-level-1-c4036"></a>编译器警告（等级 1）C4036
未命名的“type”作为实际参数  
  
 未向用作实际参数的结构、联合、枚举或类提供任何类型名称。 如果使用 [/Zg](../../build/reference/zg-generate-function-prototypes.md) 来生成函数原型，编译器会发出此警告，并注释掉所生成原型中的形式参数。  
  
 指定类型名称，以解决此警告。  
  
## <a name="example"></a>示例  
 以下示例生成 C4036。  
  
```  
// C4036.c  
// compile with: /Zg /W1  
// D9035 expected  
typedef struct { int i; } T;  
void f(T* t) {}   // C4036  
  
// OK  
typedef struct MyStruct { int i; } T2;  
void f2(T2 * t) {}  
```