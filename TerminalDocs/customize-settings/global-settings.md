---
title: 'Windows Terminal: Globale Einstellungen'
description: Erfahren Sie, wie Sie die globalen Einstellungen in Windows Terminals anpassen.
author: cinnamon-msft
ms.author: cinnamon
ms.date: 06/18/2020
ms.topic: how-to
ms.service: terminal
ms.localizationpriority: high
ms.openlocfilehash: ba3197bb8b9466d37c01432b60314a7a00227898
ms.sourcegitcommit: 91a802863cd0730d2e364377ffe44f819a66ff2a
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/18/2020
ms.locfileid: "84994308"
---
# <a name="global-settings-in-windows-terminal"></a>Globale Einstellungen in Windows Terminal

Die unten aufgeführten Eigenschaften betreffen das gesamte Terminalfenster, unabhängig von den Profileinstellungen. Diese sollten im Stammbereich Ihrer settings.json-Datei stehen.

## <a name="default-profile"></a>Standardprofil

Legen Sie das Standardprofil fest, das geöffnet wird, indem Sie <kbd>STRG+UMSCHALT+T</kbd> eingeben, die `newTab` zugewiesene Tastenzuordnung drücken, `wt new-tab` ohne Angabe eines Profils ausführen oder auf das Symbol „+“ klicken.

**Eigenschaftenname:** `defaultProfile`

**Erfordernis:** Erforderlich

**Akzeptiert:** GUID- oder Profilname als Zeichenfolge

**Standardwert:** PowerShell-GUID

> [!IMPORTANT]
> Die Verwendung des Profilnamens für `defaultProfile` ist nur in der [Windows Terminal-Vorschau](https://aka.ms/terminal-preview/) möglich.

<br />

___

## <a name="disable-dynamic-profiles"></a>Dynamische Profile deaktivieren

Hiermit wird festgelegt, welche dynamischen Profilgeneratoren deaktiviert werden, sodass sie ihre Profile beim Start nicht zur Liste der Profile hinzufügen können. Informationen zu dynamischen Profilen finden Sie auf der Seite [Dynamische Profile](./../dynamic-profiles.md).

**Eigenschaftenname:** `disabledProfileSources`

**Erfordernis:** Optional

**Akzeptiert:** `"Windows.Terminal.Wsl"`, `"Windows.Terminal.Azure"` und/oder `"Windows.Terminal.PowershellCore"` innerhalb eines Arrays

**Standardwert:** `[]`

<br />

___

## <a name="darklight-theme"></a>Dunkles/Helles Design

:::row:::
:::column span="":::
Hiermit wird das Design der Anwendung festgelegt. `"system"` verwendet dasselbe Design wie Windows.

**Eigenschaftenname:** `theme`

**Erfordernis:** Optional

**Akzeptiert:** `"system"`, `"dark"`, `"light"`

**Standardwert:** `"system"`

:::column-end:::
:::column span="":::
![Windows Terminal: Dunkles Design](./../images/requested-themes.gif)
_Konfiguration: [Powerline in PowerShell](./../custom-terminal-gallery/powerline-in-powershell.md)_

:::column-end:::
:::row-end:::

<br />

___

## <a name="tab-settings"></a>Registerkarteneinstellungen

### <a name="always-show-tabs"></a>Registerkarten immer anzeigen

:::row:::
:::column span="":::
Wenn diese Einstellung auf `true` festgelegt ist, werden Registerkarten immer angezeigt. Wenn sie auf `false` und `showTabsInTitlebar` auf `true` festgelegt ist, werden Registerkarten immer unterhalb der Titelleiste angezeigt. Wenn diese Einstellung auf `false` und `showTabsInTitlebar` auf `false` festgelegt ist, werden Registerkarten erst angezeigt, wenn mehr als eine Registerkarte vorhanden ist, indem Sie <kbd>STRG+UMSCHALT+T</kbd> oder die zu `newTab` zugewiesene Tastenzuordnung eingeben. Beachten Sie, dass das Ändern dieser Einstellung das Starten einer neuen Terminalinstanz erfordert.

**Eigenschaftenname:** `alwaysShowTabs`

**Erfordernis:** Optional

**Akzeptiert:** `true`, `false`

**Standardwert:** `true`

:::column-end:::
:::column span="":::
![Windows Terminal zeigt Registerkarten immer an](./../images/always-show-tabs.gif)

:::column-end:::
:::row-end:::

### <a name="tab-width-mode"></a>Modus für Registerkartenbreite

:::row:::
:::column span="":::
Hiermit wird die Breite der Registerkarten festgelegt. `"equal"` bewirkt, dass jede Registerkarte dieselbe Breite erhält. `"titleLength"` passt die Größe der einzelnen Registerkarten auf die Länge des Titels an. `"compact"` verkleinert jede inaktive Registerkarte auf die Breite des Symbols, wodurch für die aktive Registerkarte mehr Platz zum Anzeigen des vollständigen Titels verbleibt.

**Eigenschaftenname:** `tabWidthMode`

**Erfordernis:** Optional

**Akzeptiert:** `"equal"`, `"titleLength"`, `"compact"`

**Standardwert:** `"equal"`

:::column-end:::
:::column span="":::
![Windows Terminal: Modus für Registerkartenbreite](./../images/tab-width-mode.gif)

:::column-end:::
:::row-end:::

> [!IMPORTANT]
> Die `"compact"`-Einstellung steht nur in der [Windows Terminal-Vorschau](https://aka.ms/terminal-preview/) zur Verfügung.

### <a name="hide-close-all-tabs-popup"></a>Popupfenster „Alle Registerkarten schließen“ ausblenden

:::row:::
:::column span="":::
Wenn diese Einstellung auf `true` festgelegt ist, _erfordert_ das Schließen eines Fensters mit mehreren geöffneten Registerkarten eine Bestätigung. Wenn diese Einstellung auf `false` festgelegt ist, erfordert das Schließen eines Fensters mit mehreren geöffneten Registerkarten _keine_ Bestätigung.

**Eigenschaftenname:** `confirmCloseAllTabs`

**Erfordernis:** Optional

**Akzeptiert:** `true`, `false`

**Standardwert:** `true`

:::column-end:::
:::column span="":::
![Windows Terminal: Bestätigung zum Schließen aller Registerkarten](./../images/confirm-close-all-tabs.png)

:::column-end:::
:::row-end:::

<br />

___

## <a name="launch-settings"></a>Starteinstellungen

### <a name="launch-on-startup-preview"></a>Beim Start öffnen ([Vorschau](https://aka.ms/terminal-preview/))

Wenn diese Einstellung auf `true` festgelegt ist, ist das Öffnen von Windows Terminal beim Systemstart aktiviert. Das Festlegen der Einstellung auf `false` deaktiviert den Eintrag der Systemstartaufgabe. Hinweis: Wenn der Eintrag der Systemstartaufgabe von Windows Terminal entweder durch eine Organisationsrichtlinie oder durch eine Benutzeraktion deaktiviert ist, hat diese Einstellung keine Wirkung.

**Eigenschaftenname:** `startOnUserLogin`

**Erfordernis:** Optional

**Akzeptiert:** `true`, `false`

**Standardwert:** `false`

> [!IMPORTANT]
> Diese Funktion steht nur in der [Windows Terminal-Vorschau](https://aka.ms/terminal-preview/) zur Verfügung.

### <a name="launch-size"></a>Startgröße

Hiermit wird definiert, ob das Terminal maximiert, im Vollbildmodus oder in einem Fenster gestartet wird.

**Eigenschaftenname:** `launchMode`

**Erfordernis:** Optional

**Akzeptiert:** `"default"`, `"maximized"`, `"fullscreen"`

**Standardwert:** `"default"`

> [!IMPORTANT]
> Die `"fullscreen"`-Einstellung steht nur in der [Windows Terminal-Vorschau](https://aka.ms/terminal-preview/) zur Verfügung.

### <a name="launch-position"></a>Startposition

Hiermit wird die Pixelposition der oberen linken Ecke des Fensters beim ersten Laden festgelegt. Bei einem System mit mehreren Bildschirmen sind diese Koordinaten relativ zur oberen linken Ecke des primären Bildschirms. Wenn keine X-oder Y-Koordinate bereitgestellt wird, verwendet das Terminal die Standardeinstellung des Systems für diesen Wert. Wenn `launchMode` auf `"maximized"` festgelegt ist, wird das Fenster auf dem Monitor maximiert, der durch diese Koordinaten angegeben wird.

**Eigenschaftenname:** `initialPosition`

**Erfordernis:** Optional

**Akzeptiert:** Koordinaten als Zeichenfolge in den folgenden Formaten: `","`, `"#,#"`, `"#,"`, `",#"`

**Standardwert:** `","`

### <a name="columns-on-first-launch"></a>Spalten beim ersten Start

Dies ist die Anzahl der Zeichenspalten, die beim ersten Laden im Fenster angezeigt werden. Wenn `launchMode` auf `"maximized"` festgelegt ist, wird diese Eigenschaft ignoriert.

**Eigenschaftenname:** `initialCols`

**Erfordernis:** Optional

**Akzeptiert:** Ganze Zahl

**Standardwert:** `120`

### <a name="rows-on-first-launch"></a>Zeilen beim ersten Start

Dies ist die Anzahl der Zeilen, die beim ersten Laden im Fenster angezeigt werden. Wenn `launchMode` auf `"maximized"` festgelegt ist, wird diese Eigenschaft ignoriert.

**Eigenschaftenname:** `initialRows`

**Erfordernis:** Optional

**Akzeptiert:** Ganze Zahl

**Standardwert:** `30`

<br />

___

## <a name="title-bar-settings"></a>Titelleisteneinstellungen

### <a name="showhide-the-title-bar"></a>Titelleiste anzeigen/ausblenden

:::row:::
:::column span="":::
Wenn diese Einstellung auf `true` festgelegt ist, werden die Registerkarten in die Titelleiste verschoben, und die Titelleiste wird ausgeblendet. Wenn sie auf `false` festgelegt ist, befindet sich die Titelleiste oberhalb der Registerkarten. Beachten Sie, dass das Ändern dieser Einstellung das Starten einer neuen Terminalinstanz erfordert.

**Eigenschaftenname:** `showTabsInTitlebar`

**Erfordernis:** Optional

**Akzeptiert:** `true`, `false`

**Standardwert:** `true`

:::column-end:::
:::column span="":::
![Windows Terminal zeigt Registerkarten in der Titelleiste an](./../images/show-tabs-in-title-bar.gif)

:::column-end:::
:::row-end:::

### <a name="set-the-text-in-the-title-bar"></a>Text in der Titelleiste festlegen

Wenn diese Einstellung auf `true` festgelegt ist, wird in der Titelleiste der Titel der ausgewählten Registerkarte angezeigt. Wenn sie auf `false` festgelegt ist, wird in der Titelleiste „Windows Terminal“ angezeigt. Beachten Sie, dass das Ändern dieser Einstellung das Starten einer neuen Terminalinstanz erfordert.

**Eigenschaftenname:** `showTerminalTitleInTitlebar`

**Erfordernis:** Optional

**Akzeptiert:** `true`, `false`

**Standardwert:** `true`

<br />

___

## <a name="selection-settings"></a>Auswahleinstellungen

### <a name="copy-after-selection-is-made"></a>Nach Auswahl kopieren

Wenn diese Einstellung auf `true` festgelegt ist, wird eine Auswahl sofort bei der Erstellung in die Zwischenablage kopiert. Beim Klicken mit der rechten Maustaste erfolgt in dieser Fall immer ein Einfügevorgang. Wenn sie auf `false` festgelegt ist, bleibt die Auswahl bestehen und wartet auf weitere Maßnahmen. Wenn Sie mit der rechten Maustaste klicken, wird die Auswahl kopiert.

**Eigenschaftenname:** `copyOnSelect`

**Erfordernis:** Optional

**Akzeptiert:** `true`, `false`

**Standardwert:** `false`

### <a name="copy-formatting"></a>Formatierung kopieren

Wenn diese Einstellung auf `true` festgelegt ist, werden Farb- und Schriftformatierung des ausgewählten Textes ebenfalls in die Zwischenablage kopiert. Wenn sie auf `false` festgelegt ist, wird Nur-Text in die Zwischenablage kopiert.

**Eigenschaftenname:** `copyFormatting`

**Erfordernis:** Optional

**Akzeptiert:** `true`, `false`

**Standardwert:** `false`

### <a name="word-delimiters"></a>Worttrennzeichen

Hiermit werden die in einer durch Doppelklick ausgelösten Auswahl verwendeten Worttrennzeichen festgelegt. Worttrennzeichen sind Zeichen, die angeben, wo die Grenze zwischen zwei Wörtern liegt. Die häufigsten Beispiele sind Leerzeichen, Semikolons, Kommas und Punkte.

**Eigenschaftenname:** `wordDelimiters`

**Erfordernis:** Optional

**Akzeptiert:** Zeichen als Zeichenfolge

**Standardwert:** <code>&nbsp;&#x2f;&#x5c;&#x28;&#x29;&#x22;&#x27;&#x2d;&#x3a;&#x2c;&#x2e;&#x3b;&#x3c;&#x3e;&#x7e;&#x21;&#x40;&#x23;&#x24;&#x25;&#x5e;&#x26;&#x2a;&#x7c;&#x2b;&#x3d;&#x5b;&#x5d;&#x7b;&#x7d;&#x7e;&#x3f;│</code><br>_(`│` ist `U+2502 BOX DRAWINGS LIGHT VERTICAL`)_

<br />

___

## <a name="scroll-speed"></a>Scrollgeschwindigkeit

Dies ist die Anzahl der Zeilen, die gleichzeitig mit dem Mausrad gescrollt werden können. Dadurch wird die Systemeinstellung außer Kraft gesetzt, wenn der Wert nicht null (0) oder `"system"` ist.

**Eigenschaftenname:** `rowsToScroll`

**Erfordernis:** Optional

**Akzeptiert:** Ganze Zahl

**Standardwert:** `"system"`

<br />

___

## <a name="window-resize-behavior"></a>Verhalten bei der Größenänderung von Fenstern

:::row:::
:::column span="":::
Wenn diese Einstellung auf `true` festgelegt ist, wird das Fenster bei einer Größenänderung an der nächstgelegenen Zeichengrenze ausgerichtet. Wenn sie auf `false` festgelegt ist, wird die Größe des Fensters „reibungslos“ angepasst.

**Eigenschaftenname:** `snapToGridOnResize`

**Erfordernis:** Optional

**Akzeptiert:** `true`, `false`

**Standardwert:** `true`

:::column-end:::
:::column span="":::
![Windows Terminal: „Am Raster ausrichten“ beim Ändern der Größe](./../images/snap-to-grid-on-resize.gif)

:::column-end:::
:::row-end:::

<br />

___

## <a name="rendering-settings"></a>Renderingeinstellungen

Wenn Sie die Renderingeinstellungen ändern möchten, finden Sie weitere Informationen zu Ihrer Unterstützung auf der [Seite zur Problembehandlung](./../troubleshooting.md#the-text-is-blurry).

### <a name="screen-redrawing"></a>Neuzeichnen des Bildschirms

Wenn diese Einstellung auf `true` festgelegt wird, zeichnet das Terminal für jedes Einzelbild den gesamten Bildschirm neu. Bei Einstellung auf `false` werden nur die Updates am Bildschirm zwischen den Einzelbildern gerendert.

**Eigenschaftenname:** `experimental.rendering.forceFullRepaint`

**Erfordernis:** Optional

**Akzeptiert:** `true`, `false`

**Standardwert:** `false`

### <a name="software-rendering"></a>Softwarerendering

Wenn diese Einstellung auf `true` festgelegt ist, verwendet das Terminal den Softwarerenderer (auch als WARP bezeichnet) anstelle des Hardwarerenderers.

**Eigenschaftenname:** `experimental.rendering.software`

**Erfordernis:** Optional

**Akzeptiert:** `true`, `false`

**Standardwert:** `false`
