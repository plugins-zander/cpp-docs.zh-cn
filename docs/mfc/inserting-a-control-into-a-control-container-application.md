---
title: ActiveX 控件容器：将控件插入控件容器应用程序
ms.date: 11/04/2016
helpviewer_keywords:
- ActiveX control containers [MFC], inserting controls
- ActiveX controls [MFC], adding to projects
ms.assetid: bbb617ff-872f-43d8-b4d6-c49adb16b148
ms.openlocfilehash: e8426fd7a420ef06650930e547d06c78cc094975
ms.sourcegitcommit: a1676bf6caae05ecd698f26ed80c08828722b237
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/29/2020
ms.locfileid: "91503096"
---
# <a name="activex-control-containers-inserting-a-control-into-a-control-container-application"></a>ActiveX 控件容器：将控件插入控件容器应用程序

在从 ActiveX 控件容器应用程序访问 ActiveX 控件之前，必须使用 " [插入 Activex 控件](../windows/adding-editing-or-deleting-controls.md) " 对话框将 activex 控件添加到容器应用程序。

若要向 ActiveX 控件容器项目添加 ActiveX 控件，请参阅 [查看 Activex 控件并将其添加到对话框](../windows/adding-editing-or-deleting-controls.md)。

添加控件后，需要将 ActiveX 控件类型 () 的成员变量添加到对话框类。 有关此过程的详细信息，请参阅 [添加成员变量](../ide/adding-a-member-variable-visual-cpp.md)。

添加成员变量后，将自动生成一个称为包装类的类，并将其添加到你的项目中。 此类用作控件容器和嵌入控件之间的接口。

## <a name="see-also"></a>请参阅

[ActiveX 控件容器](activex-control-containers.md)
