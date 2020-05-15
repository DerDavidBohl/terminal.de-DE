---
title: Windows Terminal-Tastenzuordnungen
description: Erfahren Sie, wie Sie benutzerdefinierte Tastenzuordnungen für Windows Terminal erstellen können.
author: cinnamon-msft
ms.author: cinnamon
ms.date: 05/19/2020
ms.topic: how-to
ms.service: terminal
ms.localizationpriority: high
ms.openlocfilehash: 76bf91f8d7c2b49c2dc6bcf0c83640b57b2acd01
ms.sourcegitcommit: bb5b7fd7db4b81e0d44e060989dc16b6775c802a
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/15/2020
ms.locfileid: "83415965"
---
# <a name="custom-key-bindings-in-windows-terminal"></a>Benutzerdefinierte Tastenzuordnungen in Windows Terminal

Sie können benutzerdefinierte Tastenzuordnungen (Tastenkombinationen) in Windows Terminals erstellen, die Ihnen die Kontrolle darüber geben, wie Sie über Ihre Tastatur mit dem Terminal interagieren.

## <a name="key-binding-formats"></a>Formate für Tastenzuordnungen

Tastenzuordnungen können in den folgenden Formaten strukturiert werden:

### <a name="commands-without-arguments"></a>Befehle ohne Argumente

```json
{ "command": "commandName", "keys": "modifiers+key" }
```

Diese Standardeinstellung verwendet z. B. die Tastenzuordnung <kbd>ALT+F4</kbd>, um das Terminalfenster zu schließen:

```json
{ "command": "closeWindow", "keys": "alt+f4" }
```

### <a name="commands-with-arguments"></a>Befehle mit Argumenten

```json
{ "command": { "action": "commandName", "argument": "value" }, "keys": "modifiers+key" }
```

Bei dieser Standardeinstellung wird z. B. die Tastenzuordnung <kbd>STRG+UMSCHALT+1</kbd> verwendet, um eine neue Registerkarte im Terminal zu öffnen, je nachdem, welches Profil in Ihrem Dropdownmenü zuerst aufgeführt ist (in der Regel wird dadurch das PowerShell-Profil geöffnet):

```json
{ "command": { "action": "newTab", "index": 0 }, "keys": "ctrl+shift+1" }
```

<br />

___

## <a name="key-binding-properties"></a>Eigenschaften für Tastenzuordnungen

Tastenzuordnungen können unter Verwendung der folgenden Eigenschaften konstruiert werden.

### <a name="command"></a>Befehl

Dies ist der Befehl, der ausgeführt wird, wenn die zugehörigen Tasten gedrückt werden.

**Eigenschaftenname:** `command`

**Erfordernis:** Erforderlich

**Akzeptiert:** Zeichenfolge

### <a name="keys"></a>Tasten

Hiermit werden die Tastenkombinationen definiert, mit denen der Befehl aufgerufen wird. Tasten können eine beliebige Anzahl von Zusatztasten mit einer Taste aufweisen. Akzeptierte Zusatztasten und Tasten sind [unten](#accepted-modifiers-and-keys) aufgelistet.

**Eigenschaftenname:** `keys`

**Erfordernis:** Erforderlich

**Akzeptiert:** Zeichenfolge oder Array [Zeichenfolge]

### <a name="action"></a>Action

Hiermit werden bestimmten Befehlen zusätzliche Funktionen hinzugefügt.

**Eigenschaftenname:** `action`

**Erfordernis:** Optional

**Akzeptiert:** Zeichenfolge

<br />

___

## <a name="accepted-modifiers-and-keys"></a>Akzeptierte Zusatztasten und Tasten

### <a name="modifiers"></a>Zusatztasten

`ctrl+`, `shift+`, `alt+`

### <a name="modifier-keys"></a>Zusatztasten

| Type | Tasten |
| ---- | ---- |
| Funktions- und alphanumerische Tasten | `f1-f24`, `a-z`, `0-9` |
| Sonderzeichen | ``` ` ```, `-`, `=`, `[`, `]`, `\`, `;`, `'`, `,`, `.`, `/` |
| Pfeiltasten | `down`, `left`, `right`, `up`, `pagedown`, `pageup`, `pgdn`, `pgup`, `end`, `home`, `plus` |
| Aktionstasten | `tab`, `enter`, `esc`, `escape`, `space`, `backspace`, `delete`, `insert` |
| Tasten des Ziffernblocks | `numpad_0-numpad_9`, `numpad0-numpad9`, `numpad_add`, `numpad_plus`, `numpad_decimal`, `numpad_period`, `numpad_divide`, `numpad_minus`, `numpad_subtract`, `numpad_multiply` |

<br />

___

## <a name="application-level-commands"></a>Befehle auf Anwendungsebene

### <a name="close-window"></a>Fenster schließen

:::row:::
:::column span="":::
Hiermit werden das aktuelle Fenster und alle darin enthaltenen Registerkarten geschlossen. Wenn `confirmCloseAllTabs` auf `true` festgelegt ist, wird ein Dialogfenster zur Bestätigung angezeigt, um sicherzustellen, dass Sie alle Registerkarten schließen möchten. Weitere Informationen zu dieser Einstellung finden Sie auf der Seite [Globale Einstellungen](./global-settings.md#hide-close-all-tabs-popup).

**Befehlsname:** `closeWindow`

**Standardzuordnung:**

```json
{ "command": "closeWindow", "keys": "alt+f4" }
```

:::column-end:::
:::column span="":::
![Windows Terminal: Bestätigung zum Schließen aller Registerkarten](./../images/confirm-close-all-tabs.png)

:::column-end:::
:::row-end:::

### <a name="find"></a>Suchen

Hiermit wird das Suchdialogfeld geöffnet. Weitere Informationen zur Suche finden Sie auf der Seite [Suchen](./../search.md).

**Befehlsname:** `find`

**Standardzuordnung:**

```json
{ "command": "find", "keys": "ctrl+shift+f" }
```

### <a name="open-the-dropdown"></a>Dropdownmenü öffnen

Hiermit wird das Dropdownmenü geöffnet.

**Befehlsname:** `openNewTabDropdown`

**Standardzuordnung:**

```json
{ "command": "openNewTabDropdown", "keys": "ctrl+shift+space" }
```

### <a name="open-settings-file"></a>Einstellungsdatei öffnen

Hiermit wird die Einstellungsdatei geöffnet.

**Befehlsname:** `openSettings`

**Standardzuordnung:**

```json
{ "command": "openSettings", "keys": "ctrl+," }
```

### <a name="toggle-full-screen"></a>Vollbildmodus ein-/ausschalten

Dies ermöglicht es Ihnen, zwischen dem Vollbildmodus und den Standardfenstergrößen zu wechseln.

**Befehlsname:** `toggleFullscreen`

**Standardzuordnungen:**

```json
{ "command": "toggleFullscreen", "keys": "alt+enter" },
{ "command": "toggleFullscreen", "keys": "f11" }
```

<br />

___

## <a name="tab-management-commands"></a>Befehle zur Registerkartenverwaltung

### <a name="close-tab"></a>Registerkarte schließen

Hiermit wird die aktuelle Registerkarte geschlossen.

**Befehlsname:** `closeTab`

### <a name="duplicate-tab"></a>Registerkarte duplizieren

Hiermit wird eine Kopie der aktuellen Registerkarte erstellt und geöffnet.

**Befehlsname:** `duplicateTab`

**Standardzuordnung:**

```json
{ "command": "duplicateTab", "keys": "ctrl+shift+d" }
```

### <a name="new-tab"></a>Neue Registerkarte

Hiermit wird eine neue Registerkarte erstellt. Ohne Argumente wird das Standardprofil in einer neuen Registerkarte geöffnet. Wenn keine Aktion angegeben ist, wird die entsprechende Einstellung des Standardprofils verwendet.

**Befehlsname:** `newTab`

**Standardzuordnungen:**

```json
{ "command": "newTab", "keys": "ctrl+shift+t" },
{ "command": { "action": "newTab", "index": 0 }, "keys": "ctrl+shift+1" },
{ "command": { "action": "newTab", "index": 1 }, "keys": "ctrl+shift+2" },
{ "command": { "action": "newTab", "index": 2 }, "keys": "ctrl+shift+3" },
{ "command": { "action": "newTab", "index": 3 }, "keys": "ctrl+shift+4" },
{ "command": { "action": "newTab", "index": 4 }, "keys": "ctrl+shift+5" },
{ "command": { "action": "newTab", "index": 5 }, "keys": "ctrl+shift+6" },
{ "command": { "action": "newTab", "index": 6 }, "keys": "ctrl+shift+7" },
{ "command": { "action": "newTab", "index": 7 }, "keys": "ctrl+shift+8" },
{ "command": { "action": "newTab", "index": 8 }, "keys": "ctrl+shift+9" }
```

#### <a name="actions"></a>Aktionen

| Name | Erfordernis | Akzeptierter Typ | Beschreibung |
| ---- | --------- | ------- | ----------- |
| `commandLine` | Optional | Name der ausführbaren Datei als Zeichenfolge | Ausführbare Datei wird auf der Registerkarte ausgeführt. |
| `startingDirectory` | Optional | Speicherort des Ordners als Zeichenfolge | Das Verzeichnis, in dem die Registerkarte geöffnet wird. |
| `tabTitle` | Optional | Zeichenfolge | Der Titel der neuen Registerkarte. |
| `index` | Optional | Ganze Zahl | Profil, das auf der Grundlage seiner Position im Dropdownmenü geöffnet wird (beginnend bei 0). |
| `profile` | Optional | Name oder GUID des Profils als Zeichenfolge | Profil, das auf der Grundlage seiner GUID oder seines Namens geöffnet wird. |

### <a name="open-next-tab"></a>Nächste Registerkarte öffnen

Hiermit wird die Registerkarte rechts von der aktuellen geöffnet.

**Befehlsname:** `nextTab`

**Standardzuordnung:**

```json
{ "command": "nextTab", "keys": "ctrl+tab" }
```

### <a name="open-previous-tab"></a>Vorherige Registerkarte öffnen

Hiermit wird die Registerkarte links von der aktuellen geöffnet.

**Befehlsname:** `prevTab`

**Standardzuordnung:**

```json
{ "command": "prevTab", "keys": "ctrl+shift+tab" }
```

### <a name="open-a-specific-tab"></a>Bestimmte Registerkarte öffnen

Hiermit wird abhängig vom Index eine bestimmte Registerkarte geöffnet.

**Befehlsname:** `switchToTab`

**Standardzuordnungen:**

```json
{ "command": { "action": "switchToTab", "index": 0 }, "keys": "ctrl+alt+1" },
{ "command": { "action": "switchToTab", "index": 1 }, "keys": "ctrl+alt+2" },
{ "command": { "action": "switchToTab", "index": 2 }, "keys": "ctrl+alt+3" },
{ "command": { "action": "switchToTab", "index": 3 }, "keys": "ctrl+alt+4" },
{ "command": { "action": "switchToTab", "index": 4 }, "keys": "ctrl+alt+5" },
{ "command": { "action": "switchToTab", "index": 5 }, "keys": "ctrl+alt+6" },
{ "command": { "action": "switchToTab", "index": 6 }, "keys": "ctrl+alt+7" },
{ "command": { "action": "switchToTab", "index": 7 }, "keys": "ctrl+alt+8" },
{ "command": { "action": "switchToTab", "index": 8 }, "keys": "ctrl+alt+9" }
```

#### <a name="actions"></a>Aktionen

| Name | Erfordernis | Akzeptierter Typ | Beschreibung |
| ---- | --------- | ------- | ----------- |
| `index` | Erforderlich | Ganze Zahl | Registerkarte, die auf der Grundlage ihrer Position in der Registerkartenleiste geöffnet wird (beginnend bei 0). |

<br />

___

## <a name="pane-management-commands"></a>Befehle zur Bereichsverwaltung

### <a name="close-pane"></a>Bereich schließen

Hiermit wird der aktive Bereich geschlossen. Wenn keine geteilten Bereiche vorhanden sind, wird die aktuelle Registerkarte geschlossen. Wenn nur eine Registerkarte geöffnet ist, wird das Fenster geschlossen.

**Befehlsname:** `closePane`

**Standardzuordnung:**

```json
{ "command": "closePane", "keys": "ctrl+shift+w" }
```

### <a name="move-pane-focus"></a>Fokusbereich verschieben

Hiermit wird der Fokus in Abhängigkeit von der Richtung auf einen anderen Bereich verschoben.

**Befehlsname:** `moveFocus`

**Standardzuordnungen:**

```json
{ "command": { "action": "moveFocus", "direction": "down" }, "keys": "alt+down" },
{ "command": { "action": "moveFocus", "direction": "left" }, "keys": "alt+left" },
{ "command": { "action": "moveFocus", "direction": "right" }, "keys": "alt+right" },
{ "command": { "action": "moveFocus", "direction": "up" }, "keys": "alt+up" }
```

#### <a name="actions"></a>Aktionen

| Name | Erfordernis | Akzeptierter Typ | Beschreibung |
| ---- | --------- | ------- | ----------- |
| `direction` | Erforderlich | `"left"`, `"right"`, `"up"`, `"down"` | Die Richtung, in die der Fokus verschoben wird. |

### <a name="resize-a-pane"></a>Größe eines Bereichs ändern

Hiermit wird die Größe des aktiven Bereichs geändert.

**Befehlsname:** `resizePane`

**Standardzuordnungen:**

```json
{ "command": { "action": "resizePane", "direction": "down" }, "keys": "alt+shift+down" },
{ "command": { "action": "resizePane", "direction": "left" }, "keys": "alt+shift+left" },
{ "command": { "action": "resizePane", "direction": "right" }, "keys": "alt+shift+right" },
{ "command": { "action": "resizePane", "direction": "up" }, "keys": "alt+shift+up" }
```

#### <a name="actions"></a>Aktionen

| Name | Erfordernis | Akzeptierter Typ | Beschreibung |
| ---- | --------- | ------- | ----------- |
| `direction` | Erforderlich | `"left"`, `"right"`, `"up"`, `"down"` | Die Richtung, in der die Größe des Bereichs geändert wird. |

### <a name="split-a-pane"></a>Bereich teilen

Hiermit wird die Größe des aktiven Bereichs halbiert und ein weiterer geöffnet. Ohne Argumente wird das Standardprofil in einem neuen Bereich geöffnet. Wenn keine Aktion angegeben ist, wird die entsprechende Einstellung des Standardprofils verwendet.

**Befehlsname:** `splitPane`

**Standardzuordnungen:**

```json
// In settings.json
{ "command": { "action": "splitPane", "split": "auto", "splitMode": "duplicate" }, "keys": "alt+shift+d" },

// In defaults.json
{ "command": { "action": "splitPane", "split": "horizontal"}, "keys": "alt+shift+-" },
{ "command": { "action": "splitPane", "split": "vertical"}, "keys": "alt+shift+plus" }
```

#### <a name="actions"></a>Aktionen

| Name | Erfordernis | Akzeptierter Typ | Beschreibung |
| ---- | --------- | ------- | ----------- |
| `split` | Erforderlich | `"vertical"`, `"horizontal"`, `"auto"` | Gibt an, wie der Bereich unterteilt wird. `"auto"` unterteilt den Bereich in der Richtung, die die größte Oberfläche bereitstellt. |
| `commandLine` | Optional | Name der ausführbaren Datei als Zeichenfolge | Ausführbare Datei wird im Bereich ausgeführt. |
| `startingDirectory` | Optional | Speicherort des Ordners als Zeichenfolge | Das Verzeichnis, in dem der Bereich geöffnet wird. |
| `tabTitle` | Optional | Zeichenfolge | Titel der Registerkarte, wenn der neue Bereich den Fokus erhält. |
| `index` | Optional | Ganze Zahl | Profil, das auf der Grundlage seiner Position im Dropdownmenü geöffnet wird (beginnend bei 0). |
| `profile` | Optional | Name oder GUID des Profils als Zeichenfolge | Profil, das auf der Grundlage seiner GUID oder seines Namens geöffnet wird. |
| `splitMode` | Optional | `"duplicate"` | Hiermit wird gesteuert, wie der Bereich unterteilt wird. Akzeptiert nur `"duplicate"`, wodurch das Profil des Fokusbereichs in einem neuen Bereich dupliziert wird. |

<br />

___

## <a name="clipboard-integration-commands"></a>Befehle zur Integration der Zwischenablage

### <a name="copy"></a>Kopieren

Hiermit wird der ausgewählte Terminalinhalt in die Zwischenablage kopiert.

**Befehlsname:** `copy`

**Standardzuordnungen:**

```json
// In settings.json
{ "command": { "action": "copy", "singleLine": false }, "keys": "ctrl+c" },

// In defaults.json
{ "command": { "action": "copy", "singleLine": false }, "keys": "ctrl+shift+c" },
{ "command": { "action": "copy", "singleLine": false }, "keys": "ctrl+insert" }
```

#### <a name="clipboard-actions"></a>Zwischenablageaktionen

| Name | Erfordernis | Akzeptierter Typ | Beschreibung |
| ---- | --------- | ------- | ----------- |
| `singleLine` | Optional | `true`, `false` | Bei `true` wird der kopierte Inhalt als einzelne Zeile kopiert. Bei `false` werden Zeilenvorschübe aus dem ausgewählten Text beibehalten. |

### <a name="paste"></a>Einfügen

Hiermit wird der Inhalt eingefügt, der in die Zwischenablage kopiert wurde.

**Befehlsname:** `paste`

**Standardzuordnungen:**

```json
// In settings.json
{ "command": "paste", "keys": "ctrl+v" },

// In defaults.json
{ "command": "paste", "keys": "ctrl+shift+v" },
{ "command": "paste", "keys": "shift+insert" }
```

<br />

___

## <a name="scrollback-commands"></a>Befehle zum Scrollen

### <a name="scroll-up"></a>Nach oben scrollen

Hiermit wird auf dem Bildschirm nach oben gescrollt.

**Befehlsname:** `scrollUp`

**Standardzuordnung:**

```json
{ "command": "scrollUp", "keys": "ctrl+shift+up" }
```

### <a name="scroll-down"></a>Nach unten scrollen

Hiermit wird auf dem Bildschirm nach unten gescrollt.

**Befehlsname:** `scrollDown`

**Standardzuordnung:**

```json
{ "command": "scrollDown", "keys": "ctrl+shift+down" }
```

### <a name="scroll-up-a-whole-page"></a>Ganze Seite nach oben scrollen

Hiermit wird der Bildschirm um eine ganze Seite nach oben gescrollt, was der Höhe des Fensters entspricht.

**Befehlsname:** `scrollUpPage`

**Standardzuordnung:**

```json
{ "command": "scrollUpPage", "keys": "ctrl+shift+pgup" }
```

### <a name="scroll-down-a-whole-page"></a>Ganze Seite nach unten scrollen

Hiermit wird der Bildschirm um eine ganze Seite nach unten gescrollt, was der Höhe des Fensters entspricht.

**Befehlsname:** `scrollDownPage`

**Standardzuordnung:**

```json
{ "command": "scrollDownPage", "keys": "ctrl+shift+pgdn" }
```

<br />

___

## <a name="visual-adjustment-commands"></a>Befehle zur visuellen Anpassung

### <a name="adjust-font-size"></a>Schriftgrad anpassen

Hiermit wird die Textgröße um eine angegebene Punktanzahl geändert.

**Befehlsname:** `adjustFontSize`

**Standardzuordnungen:**

```json
{ "command": { "action": "adjustFontSize", "delta": 1 }, "keys": "ctrl+=" },
{ "command": { "action": "adjustFontSize", "delta": -1 }, "keys": "ctrl+-" }
```

#### <a name="actions"></a>Aktionen

| Name | Erfordernis | Akzeptierter Typ | Beschreibung |
| ---- | --------- | ------- | ----------- |
| `delta` | Erforderlich | Ganze Zahl | Umfang der Größenänderung pro Befehlsaufruf. |

### <a name="reset-font-size"></a>Schriftgrad zurücksetzen

Hiermit wird die Textgröße auf den Standardwert zurückgesetzt.

**Befehlsname:** `resetFontSize`

**Standardzuordnung:**

```json
{ "command": "resetFontSize", "keys": "ctrl+0" }
```

<br />

___

## <a name="unbind-keys"></a>Tastenzuordnung aufheben

Hiermit wird die Zuordnung der zu einem beliebigen Befehl zugewiesenen Tasten aufgehoben.

**Befehlsname:** `unbound`
