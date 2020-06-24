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
# <a name="color-schemes-in-windows-terminal"></a>Farbschemas in Windows Terminal

## <a name="creating-your-own-color-scheme"></a>Erstellen eines eigenen Farbschemas

Farbschemata können im `schemes`-Array Ihrer Datei „settings.json“ definiert werden. Sie werden im folgenden Format geschrieben:

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

Jede Einstellung, mit Ausnahme von `name`, akzeptiert eine Farbe als Zeichenfolge im Hexadezimalformat: `"#rgb"` oder `"#rrggbb"`. Die Einstellungen `cursorColor` und `selectionBackground` sind optional.

<br />

___

## <a name="included-color-schemes"></a>Enthaltene Farbschemas

Windows Terminal enthält diese Farbschemas in der Datei „defaults.json“, auf die Sie zugreifen können, indem Sie <kbd>ALT</kbd> gedrückt halten und die Schaltfläche „Einstellungen“ auswählen. Wenn Sie ein Farbschema innerhalb eines Ihrer Befehlszeilenprofile einrichten möchten, fügen Sie die Eigenschaft `colorScheme` mit dem Wert `name` des Farbschemas hinzu.

```json
"colorScheme": "COLOR SCHEME NAME"
```

### <a name="campbell"></a>Campbell

![Windows Terminal: Campbell-Farbschema](./../images/campbell-color-scheme.png)

### <a name="campbell-powershell"></a>Campbell PowerShell

![Windows Terminal: Campbell-PowerShell-Farbschema](./../images/campbell-powershell-color-scheme.png)

### <a name="vintage"></a>Vintage

![Windows Terminal: Vintage-Farbschema](./../images/vintage-color-scheme.png)

### <a name="one-half-dark"></a>One Half Dark

![Windows Terminal: One Half Dark-Farbschema](./../images/one-half-dark-color-scheme.png)

### <a name="one-half-light"></a>One Half Light

![Windows Terminal: One Half Light-Farbschema](./../images/one-half-light-color-scheme.png)

### <a name="solarized-dark"></a>Solarized Dark

![Windows Terminal: Solarized Dark-Farbschema](./../images/solarized-dark-color-scheme.png)

### <a name="solarized-light"></a>Solarized Light

![Windows Terminal: Solarized Light-Farbschema](./../images/solarized-light-color-scheme.png)

### <a name="tango-dark"></a>Tango Dark

![Windows Terminal: Tango Dark-Farbschema](./../images/tango-dark-color-scheme.png)

### <a name="tango-light"></a>Tango Light

![Windows Terminal: Tango Light-Farbschema](./../images/tango-light-color-scheme.png)
