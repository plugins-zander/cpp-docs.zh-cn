---
title: "编译器错误 C3883 |Microsoft 文档"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-tools
ms.tgt_pltfrm: 
ms.topic: error-reference
f1_keywords: C3883
dev_langs: C++
helpviewer_keywords: C3883
ms.assetid: cdd1c1f4-f268-4469-9c62-d52303114b0c
caps.latest.revision: "11"
author: corob-msft
ms.author: corob
manager: ghogen
ms.openlocfilehash: ef1203b3162aa08f1de9a5a4ee68277d2c3489cc
ms.sourcegitcommit: ebec1d449f2bd98aa851667c2bfeb7e27ce657b2
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/24/2017
---
# <a name="compiler-error-c3883"></a>编译器错误 C3883
var： 必须初始化 initonly 静态数据成员  
  
 变量标记为[initonly](../../dotnet/initonly-cpp-cli.md)未正确初始化。  
  
 下面的示例生成 C3883:  
  
```  
// C3883.cpp  
// compile with: /clr  
ref struct Y1 {  
   initonly  
   static int staticConst1;   // C3883  
};  
```  
  
 以下示例演示了可能的解决方法：  
  
```  
// C3883b.cpp  
// compile with: /clr /c  
ref struct Y1 {  
   initonly  
   static int staticConst2 = 0;  
};  
```  
  
 下面的示例演示如何在静态构造函数初始化：  
  
```  
// C3883c.cpp  
// compile with: /clr /LD  
ref struct Y1 {  
   initonly  
   static int staticConst1;  
  
   static Y1() {  
      staticConst1 = 0;  
   }  
};  
```