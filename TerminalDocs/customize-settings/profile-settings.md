---
title: Windows Terminal-Profileinstellungen
description: Erfahren Sie, wie die einzelnen Profile in Windows Terminal angepasst werden.
author: cinnamon-msft
ms.author: cinnamon
ms.date: 05/19/2020
ms.topic: how-to
ms.service: terminal
ms.localizationpriority: high
ms.openlocfilehash: 309fb40736718df7d1670a7376806b70ef0e35fe
ms.sourcegitcommit: bb5b7fd7db4b81e0d44e060989dc16b6775c802a
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/15/2020
ms.locfileid: "83416085"
---
# <a name="profile-settings-in-the-windows-terminal"></a>Profileinstellungen in Windows Terminal

Die unten aufgeführten Einstellungen sind spezifisch für die einzelnen eindeutigen Profile. Wenn Sie möchten, dass eine Einstellung auf alle Profile angewendet wird, können Sie sie dem Abschnitt `defaults` über der Profilliste in der Datei „settings.json“ hinzufügen.

```json
"defaults":
{
    // SETTINGS TO APPLY TO ALL PROFILES
},
"list":
[
    // PROFILE OBJECTS
]
```

## <a name="unique-identifier"></a>Eindeutiger Bezeichner

Profile können eine GUID als eindeutigen Bezeichner verwenden. Damit ein Profil zu Ihrem Standardprofil wird, benötigt es eine GUID für die globale Einstellung `defaultProfile`.

**Eigenschaftenname:** `guid`

**Erfordernis:** Erforderlich

**Akzeptiert:** GUID als Zeichenfolge im Registrierungsformat: `"{00000000-0000-0000-0000-000000000000}"`

<br />

___

## <a name="executable-settings"></a>Ausführbare Einstellungen

### <a name="command-line"></a>Befehlszeile

Dies ist die ausführbare Datei, die im Profil verwendet wird.

**Eigenschaftenname:** `commandline`

**Erfordernis:** Optional

**Akzeptiert:** Name der ausführbaren Datei als Zeichenfolge

**Standardwert:** `"cmd.exe"`

### <a name="source"></a>Quelle

Hiermit wird der Name des Profilgenerators gespeichert, von dem das Profil stammt. _Es sind keine erkennbaren Werte für dieses Feld vorhanden._ Weitere Informationen zu dynamischen Profilen finden Sie auf der Seite [Dynamische Profile](./../dynamic-profiles.md).

**Eigenschaftenname:** `source`

**Erfordernis:** Optional

**Akzeptiert:** Zeichenfolge

### <a name="starting-directory"></a>Startverzeichnis

Dies ist das Verzeichnis, in dem die Shell beim Laden gestartet wird.

**Eigenschaftenname:** `startingDirectory`

**Erfordernis:** Optional

**Akzeptiert:** Speicherort des Ordners als Zeichenfolge

**Standardwert:** `"%USERPROFILE%"`

<br />

___

## <a name="dropdown-settings"></a>Dropdowneinstellungen

![Windows Terminal-Dropdownmenü](./../images/dropdown.png)
_Konfiguration: [Raspberry Ubuntu](./../custom-terminal-gallery/raspberry-ubuntu.md)_

### <a name="name"></a>Name

Dies ist der Name des Profils, der im Dropdownmenü angezeigt wird. Dieser Wert wird auch als „Titel“ verwendet, der beim Start an die Shell übergeben wird. Einige Shells (z. B. `bash`) können diesen Anfangswert möglicherweise ignorieren, während andere (`Command Prompt`, `PowerShell`) diesen Wert während der Lebensdauer der Anwendung verwenden. Dieses Verhalten von „Titel“ kann durch `tabTitle` außer Kraft gesetzt werden.

**Eigenschaftenname:** `name`

**Erfordernis:** Erforderlich

**Akzeptiert:** Zeichenfolge

### <a name="icon"></a>Symbol

Hiermit wird das Symbol festgelegt, das auf der Registerkarte und im Dropdownmenü angezeigt wird.

**Eigenschaftenname:** `icon`

**Erfordernis:** Optional

**Akzeptiert:** Speicherort der Datei als Zeichenfolge

### <a name="hide-a-profile-from-the-dropdown"></a>Ein Profil aus dem Dropdownmenü ausblenden

Wenn `hidden` auf `true` festgelegt ist, wird das Profil nicht in der Liste der Profile angezeigt. Dies kann verwendet werden, um Standardprofile und dynamisch generierte Profile auszublenden, während sie in der Einstellungsdatei beibehalten werden. Weitere Informationen zu dynamischen Profilen finden Sie auf der Seite [Dynamische Profile](./../dynamic-profiles.md).

**Eigenschaftenname:** `hidden`

**Erfordernis:** Optional

**Akzeptiert:** `true`, `false`

**Standardwert:** `false`

<br />

___

## <a name="tab-title-settings"></a>Einstellungen für Registerkartentitel

### <a name="custom-tab-title"></a>Benutzerdefinierter Registerkartentitel

Wenn diese Einstellung festgelegt ist, ersetzt sie `name` als Titel, der beim Start an die Shell übergeben wird. Einige Shells (z. B. `bash`) können diesen Anfangswert möglicherweise ignorieren, während andere (`Command Prompt`, `PowerShell`) diesen Wert während der Lebensdauer der Anwendung verwenden. Wenn Sie erfahren möchten, wie Sie Ihren Titel von der Shell festlegen lassen können, besuchen Sie das [Tutorial zu Registerkartentiteln](./../tutorials/tab-title.md).

**Eigenschaftenname:** `tabTitle`

**Erfordernis:** Optional

**Akzeptiert:** Zeichenfolge

### <a name="suppress-title-changes-from-the-shell"></a>Titeländerungen von der Shell unterdrücken

Wenn dieser Wert auf `true` festgelegt ist, setzt `tabTitle` den Standardtitel der Registerkarte außer Kraft und alle Nachrichten von der Anwendung zur Titeländerung werden unterdrückt. Wenn `tabTitle` nicht festgelegt ist, wird stattdessen `name` verwendet. Wenn dies auf `false` festgelegt ist, verhält sich `tabTitle` normal.

**Eigenschaftenname:** `suppressApplicationTitle`

**Erfordernis:** Optional

**Akzeptiert:** `true`, `false`

<br />

___

## <a name="text-settings"></a>Texteinstellungen

### <a name="font-face"></a>Schriftart

Dies ist der Name der Schriftart, die im Profil verwendet wird. Das Terminal versucht, alternativ Consolas zu verwenden, wenn diese Schriftart nicht gefunden werden kann oder ungültig ist. Informationen zu den anderen Varianten der Standardschriftart, Cascadia Mono, finden Sie auf der [Cascadia Code-Seite](./../cascadia-code.md).

**Eigenschaftenname:** `fontFace`

**Erfordernis:** Optional

**Akzeptiert:** Schriftartname als Zeichenfolge

**Standardwert:** `"Cascadia Mono"`

### <a name="font-size"></a>Schriftgrad

Hiermit wird der Schriftgrad des Profils in Punkt festgelegt.

**Eigenschaftenname:** `fontSize`

**Erfordernis:** Optional

**Akzeptiert:** Ganze Zahl

**Standardwert:** `12`

### <a name="padding"></a>Abstand

:::row:::
:::column span="":::
Hiermit wird der Abstand um den Text im Fenster festgelegt. Dabei werden drei verschiedene Formate akzeptiert: `"#"` legt denselben Abstand für alle Seiten fest, `"#, #"` legt denselben Abstand für links-rechts und oben-unten fest, und `"#, #, #, #"` legt den Abstand individuell für links, oben, rechts und unten fest.

**Eigenschaftenname:** `padding`

**Erfordernis:** Optional

**Akzeptiert:** Werte als Zeichenfolge in den folgenden Formaten: `"#"`, `"#, #"`, `"#, #, #, #"`

**Standardwert:** `"8, 8, 8, 8"`

:::column-end:::
:::column span="":::
![Windows Terminal-Abstand](./../images/padding.gif)

:::column-end:::
:::row-end:::

### <a name="antialiasing-text"></a>Antialiasing bei Text

Hiermit wird gesteuert, wie das Antialiasing bei Text im Renderer erfolgt. Beachten Sie, dass das Ändern dieser Einstellung das Starten einer neuen Terminalinstanz erfordert.

![Windows Terminal: Antialiasing bei Text](./../images/antialiasing-mode.gif)

**Eigenschaftenname:** `antialiasingMode`

**Erfordernis:** Optional

**Akzeptiert:** `"grayscale"`, `"cleartype"`, `"aliased"`

**Standardwert:** `"grayscale"`

<br />

___

## <a name="cursor-settings"></a>Cursoreinstellungen

### <a name="cursor-shape"></a>Cursorform

Hiermit wird die Cursorform für das Profil festgelegt. Mögliche Cursor: `"bar"` (&#x2503;), `"vintage"` (&#x2583;), `"underscore"` (&#x2581;), `"filledBox"` (&#x2588;), `"emptyBox"` (&#x25AF;)

**Eigenschaftenname:** `cursorShape`

**Erfordernis:** Optional

**Akzeptiert:** `"bar"`, `"vintage"`, `"underscore"`, `"filledBox"`, `"emptyBox"`

**Standardwert:** `"bar"`

### <a name="cursor-color"></a>Cursorfarbe

Hiermit wird die Cursorfarbe für das Profil festgelegt. Hiermit wird das im Farbschema festgelegte `cursorColor` außer Kraft gesetzt, wenn `colorScheme` festgelegt ist.

**Eigenschaftenname:** `cursorColor`

**Erfordernis:** Optional

**Akzeptiert:** Farbe als Zeichenfolge im Hexadezimalformat: `"#rgb"` oder `"#rrggbb"`

### <a name="cursor-height"></a>Cursorhöhe

Hiermit wird die prozentuale Höhe des Cursors ab dem unteren Rand festgelegt. Dies funktioniert nur, wenn `cursorShape` auf `"vintage"` festgelegt ist.

**Eigenschaftenname:** `cursorHeight`

**Erfordernis:** Optional

**Akzeptiert:** Ganzzahl zwischen 25 und 100

<br />

___

## <a name="color-settings"></a>Farbeinstellungen

### <a name="color-scheme"></a>Farbschema

Dies ist der Name des Farbschemas, das im Profil verwendet wird. Farbschemas werden im `schemes`-Objekt definiert. Ausführlichere Informationen finden Sie auf der Seite [Farbschemas](./color-schemes.md).

**Eigenschaftenname:** `colorScheme`

**Erfordernis:** Optional

**Akzeptiert:** Name des Farbschemas als Zeichenfolge

**Standardwert:** `"Campbell"`

### <a name="foreground-color"></a>Vordergrundfarbe

Hiermit wird die Vordergrundfarbe des Profils geändert. Hiermit wird das im Farbschema festgelegte `foreground` außer Kraft gesetzt, wenn `colorScheme` festgelegt ist.

**Eigenschaftenname:** `foreground`

**Erfordernis:** Optional

**Akzeptiert:** Farbe als Zeichenfolge im Hexadezimalformat: `"#rgb"` oder `"#rrggbb"`

### <a name="background-color"></a>Hintergrundfarbe

Hiermit wird die Hintergrundfarbe des Profils mit dieser Einstellung geändert. Hiermit wird das im Farbschema festgelegte `background` außer Kraft gesetzt, wenn `colorScheme` festgelegt ist.

**Eigenschaftenname:** `background`

**Erfordernis:** Optional

**Akzeptiert:** Farbe als Zeichenfolge im Hexadezimalformat: `"#rgb"` oder `"#rrggbb"`

### <a name="selection-background-color"></a>Auswahlhintergrundfarbe

Hiermit wird die Hintergrundfarbe einer Auswahl im Profil festgelegt. Hiermit wird das im Farbschema festgelegte `selectionBackground` außer Kraft gesetzt, wenn `colorScheme` festgelegt ist.

**Eigenschaftenname:** `selectionBackground`

**Erfordernis:** Optional

**Akzeptiert:** Farbe als Zeichenfolge im Hexadezimalformat: `"#rgb"` oder `"#rrggbb"`

<br />

___

## <a name="acrylic-settings"></a>Acryleinstellungen

### <a name="enable-acrylic"></a>Acryl aktivieren

:::row:::
:::column span="":::
Wenn dies auf `true` festgelegt ist, hat das Fenster einen Acrylhintergrund. Wenn es auf `false` festgelegt ist, hat das Fenster einen einfachen, Hintergrund ohne Textur. Die Transparenz gilt aufgrund von Betriebssystemeinschränkungen nur für Fenster mit Fokus.

**Eigenschaftenname:** `useAcrylic`

**Erfordernis:** Optional

**Akzeptiert:** `true`, `false`

**Standardwert:** `false`

:::column-end:::
:::column span="":::
![Windows Terminal: Acryl](./../images/acrylic.gif)

:::column-end:::
:::row-end:::

### <a name="acrylic-opacity"></a>Acryldeckkraft

:::row:::
:::column span="":::
Wenn `useAcrylic` auf `true` festgelegt ist, wird die Transparenz des Fensters für das Profil festgelegt. Hierbei werden Gleitkommazahlen zwischen 0 und 1 akzeptiert.

**Eigenschaftenname:** `acrylicOpacity`

**Erfordernis:** Optional

**Akzeptiert:** Zahl als Gleitkommawert zwischen 0 und 1

**Standardwert:** `0.5`

:::column-end:::
:::column span="":::
![Windows Terminal: Acryldeckkraft](./../images/acrylic-opacity.gif)

:::column-end:::
:::row-end:::

<br />

___

## <a name="background-image-settings"></a>Hintergrundbildeinstellungen

### <a name="setting-the-background-image"></a>Hintergrundbild festlegen

Hiermit wird der Dateispeicherort des Bilds festgelegt, das über den Fensterhintergrund gezeichnet werden soll. Bei dem Hintergrundbild kann es sich um eine JPG-, PNG- oder GIF-Datei handeln.

**Eigenschaftenname:** `backgroundImage`

**Erfordernis:** Optional

**Akzeptiert:** Speicherort der Datei als Zeichenfolge

### <a name="background-image-stretch-mode"></a>Streckmodus für Hintergrundbild

:::row:::
:::column span="":::
Hiermit wird festgelegt, wie die Größe des Hintergrundbilds geändert wird, um das Fenster auszufüllen.

**Eigenschaftenname:** `backgroundImageStretchMode`

**Erfordernis:** Optional

**Akzeptiert:** `"none"`, `"fill"`, `"uniform"`, `"uniformToFill"`

**Standardwert:** `"uniformToFill"`

:::column-end:::
:::column span="":::
![Windows Terminal: Streckmodus für Hintergrundbild](./../images/background-image-stretch-mode.gif)
 _[Hintergrundbildquelle](https://wallpaperhub.app/wallpapers/6287)_

:::column-end:::
:::row-end:::

### <a name="background-image-alignment"></a>Hintergrundbildausrichtung

:::row:::
:::column span="":::
Hiermit wird festgelegt, wie das Hintergrundbild an den Fensterbegrenzungen ausgerichtet wird.

**Eigenschaftenname:** `backgroundImageAlignment`

**Erfordernis:** Optional

**Akzeptiert:** `"center"`, `"left"`, `"top"`, `"right"`, `"bottom"`, `"topLeft"`, `"topRight"`, `"bottomLeft"`, `"bottomRight"`

**Standardwert:** `"center"`

:::column-end:::
:::column span="":::
![Windows Terminal: Hintergrundbildausrichtung](./../images/background-image-alignment.gif)
 _[Hintergrundbildquelle](https://design.ubuntu.com/brand/ubuntu-logo/)_

:::column-end:::
:::row-end:::

### <a name="background-image-opacity"></a>Hintergrundbilddeckkraft

:::row:::
:::column span="":::
Hiermit wird die Transparenz des Hintergrundbilds festgelegt.

:::column-end:::
:::row-end:::

**Eigenschaftenname:** `backgroundImageOpacity`

**Erfordernis:** Optional

**Akzeptiert:** Zahl als Gleitkommawert zwischen 0 und 1

**Standardwert:** `1.0`

<br />

___

## <a name="scroll-settings"></a>Scrolleinstellungen

### <a name="scrollbar-visibility"></a>Sichtbarkeit der Scrollleiste

Hiermit wird die Sichtbarkeit der Scrollleiste festgelegt.

**Eigenschaftenname:** `scrollbarState`

**Erfordernis:** Optional

**Akzeptiert:** `"visible"`, `"hidden"`

### <a name="scroll-to-input-line-when-typing"></a>Beim Eingeben zur Eingabezeile scrollen

Wenn dies auf `true` festgelegt ist, scrollt das Fenster bei der Eingabe zur Befehlseingabezeile. Wenn es auf `false` festgelegt ist, scrollt das Fenster bei der Eingabe nicht.

**Eigenschaftenname:** `snapOnInput`

**Erfordernis:** Optional

**Akzeptiert:** `true`, `false`

**Standardwert:** `true`

### <a name="history-size"></a>Verlaufsgröße

Hiermit wird die Anzahl der Zeilen über den Zeilen festgelegt, die in dem Fenster angezeigt werden, zu dem Sie zurückscrollen können.

**Eigenschaftenname:** `historySize`

**Erfordernis:** Optional

**Akzeptiert:** Ganze Zahl

**Standardwert:** `9001`

<br />

___

## <a name="how-the-profile-closes-when-exiting"></a>Wie das Profil beim Verlassen geschlossen wird

Hiermit wird festgelegt, wie das Profil auf einen Abbruch oder einen fehlerhaften Start reagiert. `"graceful"` schließt das Profil, wenn `exit` eingegeben oder der Prozess normal beendet wird. `"always"` schließt das Profil immer und `"never"` schließt das Profil nie. `true` und `false` werden als Synonyme für `"graceful"` bzw. `"never"` akzeptiert.

**Eigenschaftenname:** `closeOnExit`

**Erfordernis:** Optional

**Akzeptiert:** `"graceful"`, `"always"`, `"never"`, `true`, `false`

**Standardwert:** `"graceful"`

<br />

___

## <a name="retro-terminal-effects"></a>Terminaleffekte im Retrostil

:::row:::
:::column span="":::
Wenn dieser Wert auf `true` festgelegt ist, emuliert das Terminal einen klassischen CRT-Bildschirm mit Scan-Linien und unscharfen Textkanten. Hierbei handelt es sich um ein experimentelles Feature, dessen Weiterbestehen nicht garantiert ist.

**Eigenschaftenname:** `experimental.retroTerminalEffect`

**Erfordernis:** Optional

**Akzeptiert:** `true`, `false`

**Standardwert:** `false`

:::column-end:::
:::column span="":::
![Windows Terminal: Experimenteller Terminaleffekt im Retrostil](./../images/experimental-retro-terminal-effect.gif)
_Konfiguration: [Eingabeaufforderung im Retrostil](./../custom-terminal-gallery/retro-command-prompt.md)_

:::column-end:::
:::row-end:::
