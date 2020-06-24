---
title: 'Windows Terminal: Farbschemas'
description: Erfahren Sie, wie Sie Farbschemas für Windows Terminal erstellen können.
author: cinnamon-msft
ms.author: cinnamon
ms.date: 05/19/2020
ms.topic: how-to
ms.service: terminal
ms.localizationpriority: high
ms.openlocfilehash: 9f7e6133a08a21c3b77689cd8dce32dacbf80351
ms.sourcegitcommit: d8e23557224bc50a82a36dc80ac68b9d11dfdde9
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2020
ms.locfileid: "84720136"
---
# <a name="color-schemes-in-windows-terminal"></a><span data-ttu-id="73d1d-103">Farbschemas in Windows Terminal</span><span class="sxs-lookup"><span data-stu-id="73d1d-103">Color schemes in Windows Terminal</span></span>

## <a name="creating-your-own-color-scheme"></a><span data-ttu-id="73d1d-104">Erstellen eines eigenen Farbschemas</span><span class="sxs-lookup"><span data-stu-id="73d1d-104">Creating your own color scheme</span></span>

<span data-ttu-id="73d1d-105">Farbschemata können im `schemes`-Array Ihrer Datei „settings.json“ definiert werden.</span><span class="sxs-lookup"><span data-stu-id="73d1d-105">Color schemes can be defined in the `schemes` array of your settings.json file.</span></span> <span data-ttu-id="73d1d-106">Sie werden im folgenden Format geschrieben:</span><span class="sxs-lookup"><span data-stu-id="73d1d-106">They are written in the following format:</span></span>

```json
{
    "name" : "Campbell",

    "cursorColor": "#FFFFFF",
    "selectionBackground": "#FFFFFF",

    "background" : "#0C0C0C",
    "foreground" : "#CCCCCC",

    "black" : "#0C0C0C",
    "blue" : "#0037DA",
    "cyan" : "#3A96DD",
    "green" : "#13A10E",
    "purple" : "#881798",
    "red" : "#C50F1F",
    "white" : "#CCCCCC",
    "yellow" : "#C19C00",
    "brightBlack" : "#767676",
    "brightBlue" : "#3B78FF",
    "brightCyan" : "#61D6D6",
    "brightGreen" : "#16C60C",
    "brightPurple" : "#B4009E",
    "brightRed" : "#E74856",
    "brightWhite" : "#F2F2F2",
    "brightYellow" : "#F9F1A5"
},
```

<span data-ttu-id="73d1d-107">Jede Einstellung, mit Ausnahme von `name`, akzeptiert eine Farbe als Zeichenfolge im Hexadezimalformat: `"#rgb"` oder `"#rrggbb"`.</span><span class="sxs-lookup"><span data-stu-id="73d1d-107">Every setting, aside from `name`, accepts a color as a string in hex format: `"#rgb"` or `"#rrggbb"`.</span></span> <span data-ttu-id="73d1d-108">Die Einstellungen `cursorColor` und `selectionBackground` sind optional.</span><span class="sxs-lookup"><span data-stu-id="73d1d-108">The `cursorColor` and `selectionBackground` settings are optional.</span></span>

<br />

___

## <a name="included-color-schemes"></a><span data-ttu-id="73d1d-109">Enthaltene Farbschemas</span><span class="sxs-lookup"><span data-stu-id="73d1d-109">Included color schemes</span></span>

<span data-ttu-id="73d1d-110">Windows Terminal enthält diese Farbschemas in der Datei „defaults.json“, auf die Sie zugreifen können, indem Sie <kbd>ALT</kbd> gedrückt halten und die Schaltfläche „Einstellungen“ auswählen.</span><span class="sxs-lookup"><span data-stu-id="73d1d-110">Windows Terminal includes these color schemes inside the defaults.json file, which can be accessed by holding <kbd>alt</kbd> and selecting the settings button.</span></span> <span data-ttu-id="73d1d-111">Wenn Sie ein Farbschema innerhalb eines Ihrer Befehlszeilenprofile einrichten möchten, fügen Sie die Eigenschaft `colorScheme` mit dem Wert `name` des Farbschemas hinzu.</span><span class="sxs-lookup"><span data-stu-id="73d1d-111">If you would like to set up a color scheme inside one of your command-line profiles, add the `colorScheme` property with the color scheme's `name` as the value.</span></span>

```json
"colorScheme": "COLOR SCHEME NAME"
```

### <a name="campbell"></a><span data-ttu-id="73d1d-112">Campbell</span><span class="sxs-lookup"><span data-stu-id="73d1d-112">Campbell</span></span>

![Windows Terminal: Campbell-Farbschema](./../images/campbell-color-scheme.png)

### <a name="campbell-powershell"></a><span data-ttu-id="73d1d-114">Campbell PowerShell</span><span class="sxs-lookup"><span data-stu-id="73d1d-114">Campbell Powershell</span></span>

![Windows Terminal: Campbell-PowerShell-Farbschema](./../images/campbell-powershell-color-scheme.png)

### <a name="vintage"></a><span data-ttu-id="73d1d-116">Vintage</span><span class="sxs-lookup"><span data-stu-id="73d1d-116">Vintage</span></span>

![Windows Terminal: Vintage-Farbschema](./../images/vintage-color-scheme.png)

### <a name="one-half-dark"></a><span data-ttu-id="73d1d-118">One Half Dark</span><span class="sxs-lookup"><span data-stu-id="73d1d-118">One Half Dark</span></span>

![Windows Terminal: One Half Dark-Farbschema](./../images/one-half-dark-color-scheme.png)

### <a name="one-half-light"></a><span data-ttu-id="73d1d-120">One Half Light</span><span class="sxs-lookup"><span data-stu-id="73d1d-120">One Half Light</span></span>

![Windows Terminal: One Half Light-Farbschema](./../images/one-half-light-color-scheme.png)

### <a name="solarized-dark"></a><span data-ttu-id="73d1d-122">Solarized Dark</span><span class="sxs-lookup"><span data-stu-id="73d1d-122">Solarized Dark</span></span>

![Windows Terminal: Solarized Dark-Farbschema](./../images/solarized-dark-color-scheme.png)

### <a name="solarized-light"></a><span data-ttu-id="73d1d-124">Solarized Light</span><span class="sxs-lookup"><span data-stu-id="73d1d-124">Solarized Light</span></span>

![Windows Terminal: Solarized Light-Farbschema](./../images/solarized-light-color-scheme.png)

### <a name="tango-dark"></a><span data-ttu-id="73d1d-126">Tango Dark</span><span class="sxs-lookup"><span data-stu-id="73d1d-126">Tango Dark</span></span>

![Windows Terminal: Tango Dark-Farbschema](./../images/tango-dark-color-scheme.png)

### <a name="tango-light"></a><span data-ttu-id="73d1d-128">Tango Light</span><span class="sxs-lookup"><span data-stu-id="73d1d-128">Tango Light</span></span>

![Windows Terminal: Tango Light-Farbschema](./../images/tango-light-color-scheme.png)
