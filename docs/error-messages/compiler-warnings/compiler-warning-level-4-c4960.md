---
title: "编译器警告 （等级 4） C4960 |Microsoft 文档"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- cpp-tools
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- C4960
dev_langs:
- C++
helpviewer_keywords:
- C4960
ms.assetid: 3b4ed286-9e8d-46f1-af0c-00ba669693a9
caps.latest.revision: 8
author: corob-msft
ms.author: corob
manager: ghogen
translation.priority.ht:
- de-de
- es-es
- fr-fr
- it-it
- ja-jp
- ko-kr
- ru-ru
- zh-cn
- zh-tw
translation.priority.mt:
- cs-cz
- pl-pl
- pt-br
- tr-tr
ms.translationtype: Machine Translation
ms.sourcegitcommit: 0d9cbb01d1ad0f2ea65d59334cb88140ef18fce0
ms.openlocfilehash: c61350cebf8601d706e7efec9273c967008bd6fd
ms.contentlocale: zh-cn
ms.lasthandoff: 04/12/2017

---
# <a name="compiler-warning-level-4-c4960"></a>编译器警告（等级 4）C4960
“function”太大，无法配置  
  
 使用时[/ltcg: pgoptimize](../../build/reference/ltcg-link-time-code-generation.md)，编译器检测到某个输入的模块具有的指令超过 65,535 的函数。 如此大的函数不可用于按配置进行的优化。  
  
 若要解决此警告，请减小该函数的大小。