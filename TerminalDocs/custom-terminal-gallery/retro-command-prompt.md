---
title: Konfiguration der Windows-Terminal-Eingabeaufforderung
description: Dies ist die Konfiguration für eine Retro-Eingabeaufforderung im Windows-Terminal.
author: cinnamon-msft
ms.author: cinnamon
ms.date: 05/19/2020
ms.topic: sample
ms.service: terminal
ms.openlocfilehash: 4eb110034784a9d48c5419826081c8d7c937efee
ms.sourcegitcommit: a489b75e14e2c123bf6b4ac2a15ff85b515564be
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/18/2020
ms.locfileid: "83553142"
---
# <a name="retro-command-prompt-in-windows-terminal"></a><span data-ttu-id="c2f40-103">Retro-Eingabeaufforderung im Windows-Terminal</span><span class="sxs-lookup"><span data-stu-id="c2f40-103">Retro Command Prompt in Windows Terminal</span></span>

<span data-ttu-id="c2f40-104">Die Eingabeaufforderung verwendet die `PxPlus IBM VGA8` Schriftart, die nicht im Windows-Terminal enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="c2f40-104">The prompt is using the `PxPlus IBM VGA8` font, which is not included in Windows Terminal.</span></span>

![Windows-Terminal Eingabe Eingabeaufforderung](./../images/retro-command-prompt.png)

```json
    {
        "theme": "dark",
        "profiles": [
            {
                "name": "Command Prompt",
                "commandline": "cmd.exe",
                "closeOnExit" : true,
                "colorScheme" : "Retro",
                "cursorColor" : "#FFFFFF",
                "cursorShape": "filledBox",
                "fontSize" : 16,
                "padding" : "5, 5, 5, 5",
                "tabTitle" : "Command Prompt",
                "fontFace": "PxPlus IBM VGA8",
                "experimental.retroTerminalEffect": true
            }
        ],
        "schemes": [
            {
                "name": "Retro",
                "background": "#000000",
                "black": "#00ff00",
                "blue": "#00ff00",
                "brightBlack": "#00ff00",
                "brightBlue": "#00ff00",
                "brightCyan": "#00ff00",
                "brightGreen": "#00ff00",
                "brightPurple": "#00ff00",
                "brightRed": "#00ff00",
                "brightWhite": "#00ff00",
                "brightYellow": "#00ff00",
                "cyan": "#00ff00",
                "foreground": "#00ff00",
                "green": "#00ff00",
                "purple": "#00ff00",
                "red": "#00ff00",
                "white": "#00ff00",
                "yellow": "#00ff00"
            }
        ]
    }
```
