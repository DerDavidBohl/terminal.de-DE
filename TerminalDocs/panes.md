---
title: Windows Terminal-Bereiche
description: Erfahren Sie, wie Sie Bereiche in Windows Terminal unterteilen.
author: cinnamon-msft
ms.author: cinnamon
ms.date: 05/19/2020
ms.topic: how-to
ms.service: terminal
ms.openlocfilehash: 5d13d48d8e9317c229720937f916f57769da7261
ms.sourcegitcommit: bb5b7fd7db4b81e0d44e060989dc16b6775c802a
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/15/2020
ms.locfileid: "83416305"
---
# <a name="panes-in-windows-terminal"></a>Bereiche in Windows Terminal

Bereiche bieten Ihnen die Möglichkeit, mehrere Befehlszeilenanwendungen nebeneinander auf derselben Registerkarte auszuführen. Dadurch ist es nicht mehr erforderlich, zwischen Registerkarten zu wechseln, und Sie können mehrere Eingabeaufforderungen gleichzeitig anzeigen.

## <a name="creating-a-new-pane"></a>Erstellen eines neuen Bereichs

Sie können entweder einen neuen vertikalen oder horizontalen Bereich in Windows Terminal erstellen. Bei vertikaler Teilung wird ein neuer Bereich rechts von dem Bereich geöffnet, der den Fokus enthält. Bei horizontaler Teilung wird ein neuer Bereich unterhalb des Bereichs geöffnet, der den Fokus enthält. Wenn Sie einen neuen vertikalen Bereich für Ihr Standardprofil erstellen möchten, können Sie <kbd>ALT+UMSCHALT+PLUS</kbd> (+) eingeben. Wenn Sie einen horizontalen Bereich für Ihr Standardprofil erstellen möchten, können Sie <kbd>ALT+UMSCHALT+MINUS</kbd> (-) eingeben.

![Windows Terminal: Bereich erstellen](./images/open-panes.gif)
_Konfiguration: [Raspberry Ubuntu](./custom-terminal-gallery/raspberry-ubuntu.md)_

Wenn Sie diese Tastenzuordnungen ändern möchten, können Sie neue erstellen, indem Sie die Aktion `splitPane` und die Werte `vertical` oder `horizontal` für die Eigenschaft `split` in Ihrer Datei „profiles.json“ verwenden. Wenn Sie nur einen Bereich mit der maximal möglichen Oberfläche wünschen, können Sie `split` auf `auto` festlegen. Weitere Informationen zu Tastenzuordnungen finden Sie auf der Seite [Tastenzuordnungen](./customize-settings/key-bindings.md).

```json
{ "command": { "action": "splitPane", "split": "vertical" }, "keys": "alt+shift+plus" },
{ "command": { "action": "splitPane", "split": "horizontal" }, "keys": "alt+shift+-" },
{ "command": { "action": "splitPane", "split": "auto" }, "keys": "alt+shift+|" }
```

## <a name="switching-between-panes"></a>Wechseln zwischen Bereichen

Das Terminal ermöglicht mithilfe der Tastatur die Navigation zwischen Bereichen. Wenn Sie die <kbd>ALT</kbd>-TASTE gedrückt halten, können Sie die Pfeiltasten verwenden, um den Fokus zwischen den Bereichen zu verschieben. Sie können erkennen, welcher Bereich den Fokus hat, indem Sie den ihn umgebenden Akzentfarbenrahmen betrachten. Beachten Sie, dass diese Akzentfarbe in den Windows-Farbeinstellungen festgelegt ist.

![Windows Terminal: Zwischen Bereichen wechseln](./images/navigate-panes.gif)

Sie können dies anpassen, indem Sie Tastenzuordnungen für den Befehl `moveFocus` hinzufügen und `direction` auf `down`, `left`, `right` oder `up` festlegen.

```json
{ "command": { "action": "moveFocus", "direction": "down" }, "keys": "alt+down" },
{ "command": { "action": "moveFocus", "direction": "left" }, "keys": "alt+left" },
{ "command": { "action": "moveFocus", "direction": "right" }, "keys": "alt+right" },
{ "command": { "action": "moveFocus", "direction": "up" }, "keys": "alt+up" }
```

## <a name="resizing-a-pane"></a>Ändern der Bereichsgröße

Sie können die Größe Ihrer Bereiche anpassen, indem Sie <kbd>ALT+UMSCHALT</kbd> gedrückt halten und mithilfe der Pfeiltasten die Größe des Bereichs ändern, der den Fokus enthält.

![Windows Terminal: Bereich erstellen](./images/resize-panes.gif)

Wenn Sie diese Tastenzuordnung anpassen möchten, können Sie neue hinzufügen, indem Sie die Aktion `resizePane` verwenden und `direction` auf `down`, `left`, `right` oder `up` festlegen.

```json
{ "command": { "action": "resizePane", "direction": "down" }, "keys": "alt+shift+down" },
{ "command": { "action": "resizePane", "direction": "left" }, "keys": "alt+shift+left" },
{ "command": { "action": "resizePane", "direction": "right" }, "keys": "alt+shift+right" },
{ "command": { "action": "resizePane", "direction": "up" }, "keys": "alt+shift+up" }
```

## <a name="closing-a-pane"></a>Schließen eines Bereichs

Sie können den Fokusbereich schließen, indem Sie <kbd>STRG+UMSCHALT+W</kbd> eingeben. Wenn Sie nur über einen Bereich verfügen, schließt <kbd>STRG+UMSCHALT+W</kbd> die Registerkarte. Wie immer wird das Fenster durch Schließen der letzten Registerkarte geschlossen.

![Windows Terminal: Bereiche schließen](./images/close-panes.gif)

Sie können ändern, welche Tasten den Bereich schließen, indem Sie eine Tastenzuordnung hinzufügen, die den Befehl `closePane` verwendet.

```json
{ "command": "closePane", "keys": "ctrl+shift+w" }
```

## <a name="customizing-panes-using-key-bindings"></a>Anpassen von Bereichen mithilfe von Tastenzuordnungen

Abhängig von den benutzerdefinierten Tastenzuordnungen können Sie anpassen, was in einem neuen Bereich geöffnet wird.

### <a name="duplicating-a-pane"></a>Duplizieren eines Bereichs

Das Terminal ermöglicht es Ihnen, das Profil des Fokusbereichs in einem anderen Bereich zu duplizieren.

![Windows Terminal: Bereiche duplizieren](./images/duplicate-panes.gif)

Dies kann durch Hinzufügen der Eigenschaft `splitMode` mit `duplicate` als Wert zu einer `splitPane`-Tastenzuordnung erfolgen.

```json
{ "command": { "action": "splitPane", "split": "auto", "splitMode": "duplicate" }, "keys": "alt+shift+d" }
```

### <a name="new-terminal-arguments"></a>Neue Terminalargumente

[!INCLUDE [new-terminal-arguments](./new-terminal-arguments.md)]
