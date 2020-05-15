---
title: Konfiguration des Windows-endfrosted Glass-Designs
description: Dies ist eine Beispielkonfiguration für ein satiniertem Glass-Design.
author: cinnamon-msft
ms.author: cinnamon
ms.date: 05/19/2020
ms.topic: sample
ms.service: terminal
ms.openlocfilehash: c6fa0ef042e48a151f0a29b557997f2bbed90495
ms.sourcegitcommit: bb5b7fd7db4b81e0d44e060989dc16b6775c802a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/15/2020
ms.locfileid: "83416535"
---
# <a name="frosted-glass-theme-in-windows-terminal"></a><span data-ttu-id="ae585-103">Gefrosterte Glasdesign im Windows-Terminal</span><span class="sxs-lookup"><span data-stu-id="ae585-103">Frosted Glass Theme in Windows Terminal</span></span>

<span data-ttu-id="ae585-104">Die Eingabeaufforderung wird mithilfe von Powerline formatiert und verwendet die `Cascadia Code PL` Schriftart, die von der [GitHub-Seite "Cascadia Code GitHub](https://github.com/microsoft/cascadia-code/releases)" heruntergeladen werden kann.</span><span class="sxs-lookup"><span data-stu-id="ae585-104">The prompt is styled using Powerline and is using the `Cascadia Code PL` font, which can be downloaded from the [Cascadia Code GitHub releases page](https://github.com/microsoft/cascadia-code/releases).</span></span>

> [!div class="nextstepaction"]
> [<span data-ttu-id="ae585-105">Informationen zum Einrichten von Powerline</span><span class="sxs-lookup"><span data-stu-id="ae585-105">Learn how to set up Powerline</span></span>](./../tutorials/powerline-setup.md)

![Design des Windows-endfrosted Glases](./../images/frosted-glass-theme.png)

```json
    {
        "theme": "light",
        "profiles": [
            {
                "name" : "PowerShell",
                "source" : "Windows.Terminal.PowershellCore",
                "acrylicOpacity": 0.7,
                "colorScheme" : "Frost",
                "cursorColor" : "#000000",
                "fontFace" : "Cascadia Code PL",
                "useAcrylic": true
            }
        ],
        "schemes": [
            {
                "name" : "Frost",
                "background" : "#FFFFFF",
                "black" : "#3C5712",
                "blue" : "#17b2ff",
                "brightBlack" : "#749B36",
                "brightBlue" : "#27B2F6",
                "brightCyan" : "#13A8C0",
                "brightGreen" : "#89AF50",
                "brightPurple" : "#F2A20A",
                "brightRed" : "#F49B36",
                "brightWhite" : "#741274",
                "brightYellow" : "#991070",
                "cyan" : "#3C96A6",
                "foreground" : "#000000",
                "green" : "#6AAE08",
                "purple" : "#991070",
                "red" : "#8D0C0C",
                "white" : "#6E386E",
                "yellow" : "#991070"
            }
        ]
    }
```
