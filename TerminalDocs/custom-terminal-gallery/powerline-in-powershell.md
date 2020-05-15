---
title: Windows-Terminal-Powerline in der PowerShell-Konfiguration
description: Dies ist die Konfiguration und das Design für Powerline in PowerShell.
author: cinnamon-msft
ms.author: cinnamon
ms.date: 05/19/2020
ms.topic: sample
ms.service: terminal
ms.openlocfilehash: 2e8e19647df456ab69347f923e75601ddfcc2e2f
ms.sourcegitcommit: bb5b7fd7db4b81e0d44e060989dc16b6775c802a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/15/2020
ms.locfileid: "83416545"
---
# <a name="powerline-in-powershell-theme-for-windows-terminal"></a><span data-ttu-id="11dd5-103">PowerShell-Design für Windows-Terminal</span><span class="sxs-lookup"><span data-stu-id="11dd5-103">Powerline in PowerShell theme for Windows Terminal</span></span>

<span data-ttu-id="11dd5-104">Die Eingabeaufforderung wird mithilfe von Powerline formatiert und verwendet die `Cascadia Code PL` Schriftart, die von der [GitHub-Seite "Cascadia Code GitHub](https://github.com/microsoft/cascadia-code/releases)" heruntergeladen werden kann.</span><span class="sxs-lookup"><span data-stu-id="11dd5-104">The prompt is styled using Powerline and is using the `Cascadia Code PL` font, which can be downloaded from the [Cascadia Code GitHub releases page](https://github.com/microsoft/cascadia-code/releases).</span></span>

> [!div class="nextstepaction"]
> [<span data-ttu-id="11dd5-105">Informationen zum Einrichten von Powerline</span><span class="sxs-lookup"><span data-stu-id="11dd5-105">Learn how to set up Powerline</span></span>](./../tutorials/powerline-setup.md)

![PowerShell für Windows-Terminal PowerShell](./../images/powerline-powershell.png)

```json
    {
        "theme": "dark",
        "profiles": [
            {
                "name" : "Powershell",
                "source" : "Windows.Terminal.PowershellCore",
                "acrylicOpacity" : 0.7,
                "colorScheme" : "Campbell",
                "cursorColor" : "#FFFFFD",
                "fontFace" : "Cascadia Code PL",
                "useAcrylic" : true
            }
        ]
    }
```
