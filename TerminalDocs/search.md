---
title: Windows Terminal-Suche
description: Erfahren Sie, wie Sie einen Suchvorgang in Windows Terminal ausführen.
author: cinnamon-msft
ms.author: cinnamon
ms.date: 05/19/2020
ms.topic: how-to
ms.service: terminal
ms.openlocfilehash: 94932d71e6543a83650e2e2a5febcb0206e22548
ms.sourcegitcommit: bb5b7fd7db4b81e0d44e060989dc16b6775c802a
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/15/2020
ms.locfileid: "83416335"
---
# <a name="how-to-search-in-windows-terminal"></a>Suchen in Windows Terminal

Windows Terminal enthält eine Suchfunktion, mit der Sie den Textpuffer nach einem bestimmten Schlüsselwort durchsuchen können. Dies ist bei der Suche nach einem Befehl hilfreich, den Sie vor einem oder für einen bestimmten Dateinamen ausgeführt haben.

## <a name="using-search"></a>Mithilfe der Suche

Standardmäßig können Sie das Suchdialogfeld durch Eingabe von <kbd>STRG+UMSCHALT+F</kbd> öffnen. Sobald es geöffnet ist, können Sie das gesuchte Schlüsselwort in das Textfeld eingeben und die <kbd>EINGABETASTE</kbd> drücken, um zu suchen.

![Screenshot der Windows Terminal-Suche](./images/search.png)
_Konfiguration: [Powerline in PowerShell](./custom-terminal-gallery/powerline-in-powershell.md)_

## <a name="directional-search"></a>Direktionale Suche

Das Terminal durchsucht den Textpuffer standardmäßig von unten nach oben. Sie können die Suchrichtung ändern, indem Sie einen der Pfeile im Suchdialogfeld auswählen.

![Screenshot der direktionalen Suche von Windows Terminal](./images/search-direction.gif)

## <a name="case-match-search"></a>Suche mit Übereinstimmung von Groß-/Kleinschreibung

Wenn Sie die Suchergebnisse eingrenzen möchten, können Sie die Übereinstimmung von Groß-/Kleinschreibung als Option zu Ihrer Suche hinzufügen. Sie können die Übereinstimmung von Groß-/Kleinschreibung umschalten, indem Sie die Schaltfläche für die Berücksichtigung der Groß-/Kleinschreibung auswählen, und die angezeigten Ergebnisse stimmen dann nur mit dem eingegebenen Suchbegriff mit seiner bestimmten Groß-/Kleinschreibung überein.

![Screenshot der Suche mit Berücksichtigung der Groß-/Kleinschreibung in Windows Terminal](./images/search-case-match.gif)

## <a name="searching-within-panes"></a>Suchen in Bereichen

Das Suchdialogfeld funktioniert auch mit [Bereichen](./panes.md). Wenn der Fokus in einem Bereich liegt, können Sie das Suchdialogfeld öffnen, das daraufhin in der oberen rechten Ecke des Bereichs angezeigt wird. Ein beliebiges von Ihnen eingegebenes Schlüsselwort zeigt nur die in diesem Bereich gefundenen Ergebnisse an.

![Screenshot der Suche in Windows Terminal-Bereichen](./images/search-panes.gif)

## <a name="customize-the-search-key-binding"></a>Anpassen der Suchtastenzuordnung

Sie können das Suchdialogfeld mit jeder beliebigen Tastenzuordnung (Tastenkombination) öffnen, die Sie bevorzugen. Öffnen Sie zum Ändern der Suchtastenzuordnung die Datei „settings.json“, und suchen Sie nach dem Befehl `find`. Standardmäßig ist dieser Befehl auf `ctrl+shift+f` festgelegt.

```json
// Press ctrl+shift+f to open the search box
        { "command": "find", "keys": "ctrl+shift+f" },
```

Sie können z. B. „STRG+UMSCHALT+F“ in „STRG+F“ ändern, sodass beim Eingeben von `ctrl+f` das Suchdialogfeld geöffnet wird.

Weitere Informationen zu Tastenzuordnungen finden Sie auf der Seite [Tastenzuordnungen](./customize-settings/key-bindings.md).
