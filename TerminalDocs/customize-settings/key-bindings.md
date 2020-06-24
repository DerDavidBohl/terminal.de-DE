---
title: Windows Terminal-Tastenzuordnungen
description: Erfahren Sie, wie Sie benutzerdefinierte Tastenzuordnungen für Windows Terminal erstellen können.
author: cinnamon-msft
ms.author: cinnamon
ms.date: 06/18/2020
ms.topic: how-to
ms.service: terminal
ms.localizationpriority: high
ms.openlocfilehash: 2716e3bfbbc290eb3f2bdce58d0de5c12ee3225d
ms.sourcegitcommit: 91a802863cd0730d2e364377ffe44f819a66ff2a
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/18/2020
ms.locfileid: "84994290"
---
# <a name="custom-key-bindings-in-windows-terminal"></a><span data-ttu-id="e0fe2-103">Benutzerdefinierte Tastenzuordnungen in Windows Terminal</span><span class="sxs-lookup"><span data-stu-id="e0fe2-103">Custom key bindings in Windows Terminal</span></span>

<span data-ttu-id="e0fe2-104">Sie können benutzerdefinierte Tastenzuordnungen (Tastenkombinationen) in Windows Terminals erstellen, die Ihnen die Kontrolle darüber geben, wie Sie über Ihre Tastatur mit dem Terminal interagieren.</span><span class="sxs-lookup"><span data-stu-id="e0fe2-104">You can create custom key bindings (keyboard shortcuts) inside Windows Terminal that give you control of how you interact with the terminal using your keyboard.</span></span>

## <a name="key-binding-formats"></a><span data-ttu-id="e0fe2-105">Formate für Tastenzuordnungen</span><span class="sxs-lookup"><span data-stu-id="e0fe2-105">Key binding formats</span></span>

<span data-ttu-id="e0fe2-106">Tastenzuordnungen können in den folgenden Formaten strukturiert werden:</span><span class="sxs-lookup"><span data-stu-id="e0fe2-106">Key bindings can be structured in the following formats:</span></span>

### <a name="commands-without-arguments"></a><span data-ttu-id="e0fe2-107">Befehle ohne Argumente</span><span class="sxs-lookup"><span data-stu-id="e0fe2-107">Commands without arguments</span></span>

```json
{ "command": "commandName", "keys": "modifiers+key" }
```

<span data-ttu-id="e0fe2-108">Diese Standardeinstellung verwendet z. B. die Tastenzuordnung <kbd>ALT+F4</kbd>, um das Terminalfenster zu schließen:</span><span class="sxs-lookup"><span data-stu-id="e0fe2-108">For example, this default setting uses the shortcut key <kbd>alt+f4</kbd> to close the terminal window:</span></span>

```json
{ "command": "closeWindow", "keys": "alt+f4" }
```

### <a name="commands-with-arguments"></a><span data-ttu-id="e0fe2-109">Befehle mit Argumenten</span><span class="sxs-lookup"><span data-stu-id="e0fe2-109">Commands with arguments</span></span>

```json
{ "command": { "action": "commandName", "argument": "value" }, "keys": "modifiers+key" }
```

<span data-ttu-id="e0fe2-110">Bei dieser Standardeinstellung wird z. B. die Tastenzuordnung <kbd>STRG+UMSCHALT+1</kbd> verwendet, um eine neue Registerkarte im Terminal zu öffnen, je nachdem, welches Profil in Ihrem Dropdownmenü zuerst aufgeführt ist (in der Regel wird dadurch das PowerShell-Profil geöffnet):</span><span class="sxs-lookup"><span data-stu-id="e0fe2-110">For example, this default setting uses the shortcut key <kbd>ctrl+shift+1</kbd> to open a new tab in the terminal based on whichever profile is listed first in your dropdown menu (typically this will open the PowerShell profile):</span></span>

```json
{ "command": { "action": "newTab", "index": 0 }, "keys": "ctrl+shift+1" }
```

<br />

___

## <a name="key-binding-properties"></a><span data-ttu-id="e0fe2-111">Eigenschaften für Tastenzuordnungen</span><span class="sxs-lookup"><span data-stu-id="e0fe2-111">Key binding properties</span></span>

<span data-ttu-id="e0fe2-112">Tastenzuordnungen können unter Verwendung der folgenden Eigenschaften konstruiert werden.</span><span class="sxs-lookup"><span data-stu-id="e0fe2-112">Key bindings can be constructed using the following properties.</span></span>

### <a name="command"></a><span data-ttu-id="e0fe2-113">Befehl</span><span class="sxs-lookup"><span data-stu-id="e0fe2-113">Command</span></span>

<span data-ttu-id="e0fe2-114">Dies ist der Befehl, der ausgeführt wird, wenn die zugehörigen Tasten gedrückt werden.</span><span class="sxs-lookup"><span data-stu-id="e0fe2-114">This is the command executed when the associated keys are pressed.</span></span>

<span data-ttu-id="e0fe2-115">**Eigenschaftenname:** `command`</span><span class="sxs-lookup"><span data-stu-id="e0fe2-115">**Property name:** `command`</span></span>

<span data-ttu-id="e0fe2-116">**Erfordernis:** Erforderlich</span><span class="sxs-lookup"><span data-stu-id="e0fe2-116">**Necessity:** Required</span></span>

<span data-ttu-id="e0fe2-117">**Akzeptiert:** Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="e0fe2-117">**Accepts:** String</span></span>

### <a name="keys"></a><span data-ttu-id="e0fe2-118">Tasten</span><span class="sxs-lookup"><span data-stu-id="e0fe2-118">Keys</span></span>

<span data-ttu-id="e0fe2-119">Hiermit werden die Tastenkombinationen definiert, mit denen der Befehl aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="e0fe2-119">This defines the key combinations used to call the command.</span></span> <span data-ttu-id="e0fe2-120">Tasten können eine beliebige Anzahl von Zusatztasten mit einer Taste aufweisen.</span><span class="sxs-lookup"><span data-stu-id="e0fe2-120">Keys can have any number of modifiers with one key.</span></span> <span data-ttu-id="e0fe2-121">Akzeptierte Zusatztasten und Tasten sind [unten](#accepted-modifiers-and-keys) aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="e0fe2-121">Accepted modifiers and keys are listed [below](#accepted-modifiers-and-keys).</span></span>

<span data-ttu-id="e0fe2-122">**Eigenschaftenname:** `keys`</span><span class="sxs-lookup"><span data-stu-id="e0fe2-122">**Property name:** `keys`</span></span>

<span data-ttu-id="e0fe2-123">**Erfordernis:** Erforderlich</span><span class="sxs-lookup"><span data-stu-id="e0fe2-123">**Necessity:** Required</span></span>

<span data-ttu-id="e0fe2-124">**Akzeptiert:** Zeichenfolge oder Array [Zeichenfolge]</span><span class="sxs-lookup"><span data-stu-id="e0fe2-124">**Accepts:** String or array[string]</span></span>

### <a name="action"></a><span data-ttu-id="e0fe2-125">Action</span><span class="sxs-lookup"><span data-stu-id="e0fe2-125">Action</span></span>

<span data-ttu-id="e0fe2-126">Hiermit werden bestimmten Befehlen zusätzliche Funktionen hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="e0fe2-126">This adds additional functionality to certain commands.</span></span>

<span data-ttu-id="e0fe2-127">**Eigenschaftenname:** `action`</span><span class="sxs-lookup"><span data-stu-id="e0fe2-127">**Property name:** `action`</span></span>

<span data-ttu-id="e0fe2-128">**Erfordernis:** Optional</span><span class="sxs-lookup"><span data-stu-id="e0fe2-128">**Necessity:** Optional</span></span>

<span data-ttu-id="e0fe2-129">**Akzeptiert:** Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="e0fe2-129">**Accepts:** String</span></span>

<br />

___

## <a name="accepted-modifiers-and-keys"></a><span data-ttu-id="e0fe2-130">Akzeptierte Zusatztasten und Tasten</span><span class="sxs-lookup"><span data-stu-id="e0fe2-130">Accepted modifiers and keys</span></span>

### <a name="modifiers"></a><span data-ttu-id="e0fe2-131">Zusatztasten</span><span class="sxs-lookup"><span data-stu-id="e0fe2-131">Modifiers</span></span>

<span data-ttu-id="e0fe2-132">`ctrl+`, `shift+`, `alt+`</span><span class="sxs-lookup"><span data-stu-id="e0fe2-132">`ctrl+`, `shift+`, `alt+`</span></span>

### <a name="modifier-keys"></a><span data-ttu-id="e0fe2-133">Zusatztasten</span><span class="sxs-lookup"><span data-stu-id="e0fe2-133">Modifier keys</span></span>

| <span data-ttu-id="e0fe2-134">Type</span><span class="sxs-lookup"><span data-stu-id="e0fe2-134">Type</span></span> | <span data-ttu-id="e0fe2-135">Tasten</span><span class="sxs-lookup"><span data-stu-id="e0fe2-135">Keys</span></span> |
| ---- | ---- |
| <span data-ttu-id="e0fe2-136">Funktions- und alphanumerische Tasten</span><span class="sxs-lookup"><span data-stu-id="e0fe2-136">Function and alphanumeric keys</span></span> | <span data-ttu-id="e0fe2-137">`f1-f24`, `a-z`, `0-9`</span><span class="sxs-lookup"><span data-stu-id="e0fe2-137">`f1-f24`, `a-z`, `0-9`</span></span> |
| <span data-ttu-id="e0fe2-138">Sonderzeichen</span><span class="sxs-lookup"><span data-stu-id="e0fe2-138">Symbols</span></span> | <span data-ttu-id="e0fe2-139">``` ` ```, `-`, `=`, `[`, `]`, `\`, `;`, `'`, `,`, `.`, `/`</span><span class="sxs-lookup"><span data-stu-id="e0fe2-139">``` ` ```, `-`, `=`, `[`, `]`, `\`, `;`, `'`, `,`, `.`, `/`</span></span> |
| <span data-ttu-id="e0fe2-140">Pfeiltasten</span><span class="sxs-lookup"><span data-stu-id="e0fe2-140">Arrow keys</span></span> | <span data-ttu-id="e0fe2-141">`down`, `left`, `right`, `up`, `pagedown`, `pageup`, `pgdn`, `pgup`, `end`, `home`, `plus`</span><span class="sxs-lookup"><span data-stu-id="e0fe2-141">`down`, `left`, `right`, `up`, `pagedown`, `pageup`, `pgdn`, `pgup`, `end`, `home`, `plus`</span></span> |
| <span data-ttu-id="e0fe2-142">Aktionstasten</span><span class="sxs-lookup"><span data-stu-id="e0fe2-142">Action keys</span></span> | <span data-ttu-id="e0fe2-143">`tab`, `enter`, `esc`, `escape`, `space`, `backspace`, `delete`, `insert`</span><span class="sxs-lookup"><span data-stu-id="e0fe2-143">`tab`, `enter`, `esc`, `escape`, `space`, `backspace`, `delete`, `insert`</span></span> |
| <span data-ttu-id="e0fe2-144">Tasten des Ziffernblocks</span><span class="sxs-lookup"><span data-stu-id="e0fe2-144">Numpad keys</span></span> | <span data-ttu-id="e0fe2-145">`numpad_0-numpad_9`, `numpad0-numpad9`, `numpad_add`, `numpad_plus`, `numpad_decimal`, `numpad_period`, `numpad_divide`, `numpad_minus`, `numpad_subtract`, `numpad_multiply`</span><span class="sxs-lookup"><span data-stu-id="e0fe2-145">`numpad_0-numpad_9`, `numpad0-numpad9`, `numpad_add`, `numpad_plus`, `numpad_decimal`, `numpad_period`, `numpad_divide`, `numpad_minus`, `numpad_subtract`, `numpad_multiply`</span></span> |

<br />

___

## <a name="application-level-commands"></a><span data-ttu-id="e0fe2-146">Befehle auf Anwendungsebene</span><span class="sxs-lookup"><span data-stu-id="e0fe2-146">Application-level commands</span></span>

### <a name="close-window"></a><span data-ttu-id="e0fe2-147">Fenster schließen</span><span class="sxs-lookup"><span data-stu-id="e0fe2-147">Close window</span></span>

:::row:::
:::column span="":::
<span data-ttu-id="e0fe2-148">Hiermit werden das aktuelle Fenster und alle darin enthaltenen Registerkarten geschlossen.</span><span class="sxs-lookup"><span data-stu-id="e0fe2-148">This closes the current window and all tabs within it.</span></span> <span data-ttu-id="e0fe2-149">Wenn `confirmCloseAllTabs` auf `true` festgelegt ist, wird ein Dialogfenster zur Bestätigung angezeigt, um sicherzustellen, dass Sie alle Registerkarten schließen möchten.</span><span class="sxs-lookup"><span data-stu-id="e0fe2-149">If `confirmCloseAllTabs` is set to `true`, a confirmation dialog will appear to ensure you'd like to close all your tabs.</span></span> <span data-ttu-id="e0fe2-150">Weitere Informationen zu dieser Einstellung finden Sie auf der Seite [Globale Einstellungen](./global-settings.md#hide-close-all-tabs-popup).</span><span class="sxs-lookup"><span data-stu-id="e0fe2-150">More information on this setting can be found on the [Global settings page](./global-settings.md#hide-close-all-tabs-popup).</span></span>

<span data-ttu-id="e0fe2-151">**Befehlsname:** `closeWindow`</span><span class="sxs-lookup"><span data-stu-id="e0fe2-151">**Command name:** `closeWindow`</span></span>

<span data-ttu-id="e0fe2-152">**Standardzuordnung:**</span><span class="sxs-lookup"><span data-stu-id="e0fe2-152">**Default binding:**</span></span>

```json
{ "command": "closeWindow", "keys": "alt+f4" }
```

:::column-end:::
:::column span="":::
![Windows Terminal: Bestätigung zum Schließen aller Registerkarten](./../images/confirm-close-all-tabs.png)

:::column-end:::
:::row-end:::

### <a name="find"></a><span data-ttu-id="e0fe2-154">Suchen</span><span class="sxs-lookup"><span data-stu-id="e0fe2-154">Find</span></span>

<span data-ttu-id="e0fe2-155">Hiermit wird das Suchdialogfeld geöffnet.</span><span class="sxs-lookup"><span data-stu-id="e0fe2-155">This opens the search dialog box.</span></span> <span data-ttu-id="e0fe2-156">Weitere Informationen zur Suche finden Sie auf der Seite [Suchen](./../search.md).</span><span class="sxs-lookup"><span data-stu-id="e0fe2-156">More information on search can be found on the [Search page](./../search.md).</span></span>

<span data-ttu-id="e0fe2-157">**Befehlsname:** `find`</span><span class="sxs-lookup"><span data-stu-id="e0fe2-157">**Command name:** `find`</span></span>

<span data-ttu-id="e0fe2-158">**Standardzuordnung:**</span><span class="sxs-lookup"><span data-stu-id="e0fe2-158">**Default binding:**</span></span>

```json
{ "command": "find", "keys": "ctrl+shift+f" }
```

### <a name="open-the-dropdown"></a><span data-ttu-id="e0fe2-159">Dropdownmenü öffnen</span><span class="sxs-lookup"><span data-stu-id="e0fe2-159">Open the dropdown</span></span>

<span data-ttu-id="e0fe2-160">Hiermit wird das Dropdownmenü geöffnet.</span><span class="sxs-lookup"><span data-stu-id="e0fe2-160">This opens the dropdown menu.</span></span>

<span data-ttu-id="e0fe2-161">**Befehlsname:** `openNewTabDropdown`</span><span class="sxs-lookup"><span data-stu-id="e0fe2-161">**Command name:** `openNewTabDropdown`</span></span>

<span data-ttu-id="e0fe2-162">**Standardzuordnung:**</span><span class="sxs-lookup"><span data-stu-id="e0fe2-162">**Default binding:**</span></span>

```json
{ "command": "openNewTabDropdown", "keys": "ctrl+shift+space" }
```

### <a name="open-settings-files"></a><span data-ttu-id="e0fe2-163">Einstellungsdateien öffnen</span><span class="sxs-lookup"><span data-stu-id="e0fe2-163">Open settings files</span></span>

<span data-ttu-id="e0fe2-164">Hiermit werden entweder die standardmäßigen oder die benutzerdefinierten Einstellungsdateien geöffnet.</span><span class="sxs-lookup"><span data-stu-id="e0fe2-164">This opens either the default or custom settings files.</span></span> <span data-ttu-id="e0fe2-165">Ohne das Feld `target` wird die settings.json-Datei geöffnet.</span><span class="sxs-lookup"><span data-stu-id="e0fe2-165">Without the `target` field, this will open the settings.json file.</span></span>

<span data-ttu-id="e0fe2-166">**Befehlsname:** `openSettings`</span><span class="sxs-lookup"><span data-stu-id="e0fe2-166">**Command name:** `openSettings`</span></span>

<span data-ttu-id="e0fe2-167">**Standardzuordnung:**</span><span class="sxs-lookup"><span data-stu-id="e0fe2-167">**Default binding:**</span></span>

```json
{ "command": "openSettings", "keys": "ctrl+," },
{ "command": { "action": "openSettings", "target": "defaultsFile" }, "keys": "ctrl+alt+," },
```

#### <a name="actions"></a><span data-ttu-id="e0fe2-168">Aktionen</span><span class="sxs-lookup"><span data-stu-id="e0fe2-168">Actions</span></span>

| <span data-ttu-id="e0fe2-169">Name</span><span class="sxs-lookup"><span data-stu-id="e0fe2-169">Name</span></span> | <span data-ttu-id="e0fe2-170">Erfordernis</span><span class="sxs-lookup"><span data-stu-id="e0fe2-170">Necessity</span></span> | <span data-ttu-id="e0fe2-171">Akzeptierter Typ</span><span class="sxs-lookup"><span data-stu-id="e0fe2-171">Accepts</span></span> | <span data-ttu-id="e0fe2-172">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e0fe2-172">Description</span></span> |
| ---- | --------- | ------- | ----------- |
| `target` | <span data-ttu-id="e0fe2-173">Optional</span><span class="sxs-lookup"><span data-stu-id="e0fe2-173">Optional</span></span> | <span data-ttu-id="e0fe2-174">`"settingsFile"`, `"defaultsFile"`, `"allFiles"`</span><span class="sxs-lookup"><span data-stu-id="e0fe2-174">`"settingsFile"`, `"defaultsFile"`, `"allFiles"`</span></span> | <span data-ttu-id="e0fe2-175">Die zu öffnende Einstellungsdatei.</span><span class="sxs-lookup"><span data-stu-id="e0fe2-175">The settings file to open.</span></span> |

> [!IMPORTANT]
> <span data-ttu-id="e0fe2-176">Das Feld `target` steht nur in der [Windows Terminal-Vorschau](https://aka.ms/terminal-preview/) zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="e0fe2-176">The `target` field is only available in [Windows Terminal Preview](https://aka.ms/terminal-preview/).</span></span>

### <a name="toggle-full-screen"></a><span data-ttu-id="e0fe2-177">Vollbildmodus ein-/ausschalten</span><span class="sxs-lookup"><span data-stu-id="e0fe2-177">Toggle full screen</span></span>

<span data-ttu-id="e0fe2-178">Dies ermöglicht es Ihnen, zwischen dem Vollbildmodus und den Standardfenstergrößen zu wechseln.</span><span class="sxs-lookup"><span data-stu-id="e0fe2-178">This allows you to switch between full screen and default window sizes.</span></span>

<span data-ttu-id="e0fe2-179">**Befehlsname:** `toggleFullscreen`</span><span class="sxs-lookup"><span data-stu-id="e0fe2-179">**Command name:** `toggleFullscreen`</span></span>

<span data-ttu-id="e0fe2-180">**Standardzuordnungen:**</span><span class="sxs-lookup"><span data-stu-id="e0fe2-180">**Default bindings:**</span></span>

```json
{ "command": "toggleFullscreen", "keys": "alt+enter" },
{ "command": "toggleFullscreen", "keys": "f11" }
```

<br />

___

## <a name="tab-management-commands"></a><span data-ttu-id="e0fe2-181">Befehle zur Registerkartenverwaltung</span><span class="sxs-lookup"><span data-stu-id="e0fe2-181">Tab management commands</span></span>

### <a name="close-tab"></a><span data-ttu-id="e0fe2-182">Registerkarte schließen</span><span class="sxs-lookup"><span data-stu-id="e0fe2-182">Close tab</span></span>

<span data-ttu-id="e0fe2-183">Hiermit wird die aktuelle Registerkarte geschlossen.</span><span class="sxs-lookup"><span data-stu-id="e0fe2-183">This closes the current tab.</span></span>

<span data-ttu-id="e0fe2-184">**Befehlsname:** `closeTab`</span><span class="sxs-lookup"><span data-stu-id="e0fe2-184">**Command name:** `closeTab`</span></span>

### <a name="duplicate-tab"></a><span data-ttu-id="e0fe2-185">Registerkarte duplizieren</span><span class="sxs-lookup"><span data-stu-id="e0fe2-185">Duplicate tab</span></span>

<span data-ttu-id="e0fe2-186">Hiermit wird eine Kopie der aktuellen Registerkarte erstellt und geöffnet.</span><span class="sxs-lookup"><span data-stu-id="e0fe2-186">This makes a copy of the current tab and opens it.</span></span>

<span data-ttu-id="e0fe2-187">**Befehlsname:** `duplicateTab`</span><span class="sxs-lookup"><span data-stu-id="e0fe2-187">**Command name:** `duplicateTab`</span></span>

<span data-ttu-id="e0fe2-188">**Standardzuordnung:**</span><span class="sxs-lookup"><span data-stu-id="e0fe2-188">**Default binding:**</span></span>

```json
{ "command": "duplicateTab", "keys": "ctrl+shift+d" }
```

### <a name="new-tab"></a><span data-ttu-id="e0fe2-189">Neue Registerkarte</span><span class="sxs-lookup"><span data-stu-id="e0fe2-189">New tab</span></span>

<span data-ttu-id="e0fe2-190">Hiermit wird eine neue Registerkarte erstellt. Ohne Argumente wird das Standardprofil in einer neuen Registerkarte geöffnet. Wenn keine Aktion angegeben ist, wird die entsprechende Einstellung des Standardprofils verwendet.</span><span class="sxs-lookup"><span data-stu-id="e0fe2-190">This creates a new tab. Without any arguments, this will open the default profile in a new tab. If an action is not specified, the default profile's equivalent setting will be used.</span></span>

<span data-ttu-id="e0fe2-191">**Befehlsname:** `newTab`</span><span class="sxs-lookup"><span data-stu-id="e0fe2-191">**Command name:** `newTab`</span></span>

<span data-ttu-id="e0fe2-192">**Standardzuordnungen:**</span><span class="sxs-lookup"><span data-stu-id="e0fe2-192">**Default bindings:**</span></span>

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

#### <a name="actions"></a><span data-ttu-id="e0fe2-193">Aktionen</span><span class="sxs-lookup"><span data-stu-id="e0fe2-193">Actions</span></span>

| <span data-ttu-id="e0fe2-194">Name</span><span class="sxs-lookup"><span data-stu-id="e0fe2-194">Name</span></span> | <span data-ttu-id="e0fe2-195">Erfordernis</span><span class="sxs-lookup"><span data-stu-id="e0fe2-195">Necessity</span></span> | <span data-ttu-id="e0fe2-196">Akzeptierter Typ</span><span class="sxs-lookup"><span data-stu-id="e0fe2-196">Accepts</span></span> | <span data-ttu-id="e0fe2-197">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e0fe2-197">Description</span></span> |
| ---- | --------- | ------- | ----------- |
| `commandLine` | <span data-ttu-id="e0fe2-198">Optional</span><span class="sxs-lookup"><span data-stu-id="e0fe2-198">Optional</span></span> | <span data-ttu-id="e0fe2-199">Name der ausführbaren Datei als Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="e0fe2-199">Executable file name as a string</span></span> | <span data-ttu-id="e0fe2-200">Ausführbare Datei wird auf der Registerkarte ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e0fe2-200">Executable run within the tab.</span></span> |
| `startingDirectory` | <span data-ttu-id="e0fe2-201">Optional</span><span class="sxs-lookup"><span data-stu-id="e0fe2-201">Optional</span></span> | <span data-ttu-id="e0fe2-202">Speicherort des Ordners als Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="e0fe2-202">Folder location as a string</span></span> | <span data-ttu-id="e0fe2-203">Das Verzeichnis, in dem die Registerkarte geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="e0fe2-203">Directory in which the tab will open.</span></span> |
| `tabTitle` | <span data-ttu-id="e0fe2-204">Optional</span><span class="sxs-lookup"><span data-stu-id="e0fe2-204">Optional</span></span> | <span data-ttu-id="e0fe2-205">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="e0fe2-205">String</span></span> | <span data-ttu-id="e0fe2-206">Der Titel der neuen Registerkarte.</span><span class="sxs-lookup"><span data-stu-id="e0fe2-206">Title of the new tab.</span></span> |
| `index` | <span data-ttu-id="e0fe2-207">Optional</span><span class="sxs-lookup"><span data-stu-id="e0fe2-207">Optional</span></span> | <span data-ttu-id="e0fe2-208">Ganze Zahl</span><span class="sxs-lookup"><span data-stu-id="e0fe2-208">Integer</span></span> | <span data-ttu-id="e0fe2-209">Profil, das auf der Grundlage seiner Position im Dropdownmenü geöffnet wird (beginnend bei 0).</span><span class="sxs-lookup"><span data-stu-id="e0fe2-209">Profile that will open based on its position in the dropdown (starting at 0).</span></span> |
| `profile` | <span data-ttu-id="e0fe2-210">Optional</span><span class="sxs-lookup"><span data-stu-id="e0fe2-210">Optional</span></span> | <span data-ttu-id="e0fe2-211">Name oder GUID des Profils als Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="e0fe2-211">Profile's name or GUID as a string</span></span> | <span data-ttu-id="e0fe2-212">Profil, das auf der Grundlage seiner GUID oder seines Namens geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="e0fe2-212">Profile that will open based on its GUID or name.</span></span> |

### <a name="open-next-tab"></a><span data-ttu-id="e0fe2-213">Nächste Registerkarte öffnen</span><span class="sxs-lookup"><span data-stu-id="e0fe2-213">Open next tab</span></span>

<span data-ttu-id="e0fe2-214">Hiermit wird die Registerkarte rechts von der aktuellen geöffnet.</span><span class="sxs-lookup"><span data-stu-id="e0fe2-214">This opens the tab to the right of the current one.</span></span>

<span data-ttu-id="e0fe2-215">**Befehlsname:** `nextTab`</span><span class="sxs-lookup"><span data-stu-id="e0fe2-215">**Command name:** `nextTab`</span></span>

<span data-ttu-id="e0fe2-216">**Standardzuordnung:**</span><span class="sxs-lookup"><span data-stu-id="e0fe2-216">**Default binding:**</span></span>

```json
{ "command": "nextTab", "keys": "ctrl+tab" }
```

### <a name="open-previous-tab"></a><span data-ttu-id="e0fe2-217">Vorherige Registerkarte öffnen</span><span class="sxs-lookup"><span data-stu-id="e0fe2-217">Open previous tab</span></span>

<span data-ttu-id="e0fe2-218">Hiermit wird die Registerkarte links von der aktuellen geöffnet.</span><span class="sxs-lookup"><span data-stu-id="e0fe2-218">This opens the tab to the left of the current one.</span></span>

<span data-ttu-id="e0fe2-219">**Befehlsname:** `prevTab`</span><span class="sxs-lookup"><span data-stu-id="e0fe2-219">**Command name:** `prevTab`</span></span>

<span data-ttu-id="e0fe2-220">**Standardzuordnung:**</span><span class="sxs-lookup"><span data-stu-id="e0fe2-220">**Default binding:**</span></span>

```json
{ "command": "prevTab", "keys": "ctrl+shift+tab" }
```

### <a name="open-a-specific-tab"></a><span data-ttu-id="e0fe2-221">Bestimmte Registerkarte öffnen</span><span class="sxs-lookup"><span data-stu-id="e0fe2-221">Open a specific tab</span></span>

<span data-ttu-id="e0fe2-222">Hiermit wird abhängig vom Index eine bestimmte Registerkarte geöffnet.</span><span class="sxs-lookup"><span data-stu-id="e0fe2-222">This opens a specific tab depending on the index.</span></span>

<span data-ttu-id="e0fe2-223">**Befehlsname:** `switchToTab`</span><span class="sxs-lookup"><span data-stu-id="e0fe2-223">**Command name:** `switchToTab`</span></span>

<span data-ttu-id="e0fe2-224">**Standardzuordnungen:**</span><span class="sxs-lookup"><span data-stu-id="e0fe2-224">**Default bindings:**</span></span>

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

#### <a name="actions"></a><span data-ttu-id="e0fe2-225">Aktionen</span><span class="sxs-lookup"><span data-stu-id="e0fe2-225">Actions</span></span>

| <span data-ttu-id="e0fe2-226">Name</span><span class="sxs-lookup"><span data-stu-id="e0fe2-226">Name</span></span> | <span data-ttu-id="e0fe2-227">Erfordernis</span><span class="sxs-lookup"><span data-stu-id="e0fe2-227">Necessity</span></span> | <span data-ttu-id="e0fe2-228">Akzeptierter Typ</span><span class="sxs-lookup"><span data-stu-id="e0fe2-228">Accepts</span></span> | <span data-ttu-id="e0fe2-229">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e0fe2-229">Description</span></span> |
| ---- | --------- | ------- | ----------- |
| `index` | <span data-ttu-id="e0fe2-230">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="e0fe2-230">Required</span></span> | <span data-ttu-id="e0fe2-231">Ganze Zahl</span><span class="sxs-lookup"><span data-stu-id="e0fe2-231">Integer</span></span> | <span data-ttu-id="e0fe2-232">Registerkarte, die auf der Grundlage ihrer Position in der Registerkartenleiste geöffnet wird (beginnend bei 0).</span><span class="sxs-lookup"><span data-stu-id="e0fe2-232">Tab that will open based on its position in the tab bar (starting at 0).</span></span> |

<br />

___

## <a name="pane-management-commands"></a><span data-ttu-id="e0fe2-233">Befehle zur Bereichsverwaltung</span><span class="sxs-lookup"><span data-stu-id="e0fe2-233">Pane management commands</span></span>

### <a name="close-pane"></a><span data-ttu-id="e0fe2-234">Bereich schließen</span><span class="sxs-lookup"><span data-stu-id="e0fe2-234">Close pane</span></span>

<span data-ttu-id="e0fe2-235">Hiermit wird der aktive Bereich geschlossen.</span><span class="sxs-lookup"><span data-stu-id="e0fe2-235">This closes the active pane.</span></span> <span data-ttu-id="e0fe2-236">Wenn keine geteilten Bereiche vorhanden sind, wird die aktuelle Registerkarte geschlossen. Wenn nur eine Registerkarte geöffnet ist, wird das Fenster geschlossen.</span><span class="sxs-lookup"><span data-stu-id="e0fe2-236">If there aren't any split panes, this will close the current tab. If there is only one tab open, this will close the window.</span></span>

<span data-ttu-id="e0fe2-237">**Befehlsname:** `closePane`</span><span class="sxs-lookup"><span data-stu-id="e0fe2-237">**Command name:** `closePane`</span></span>

<span data-ttu-id="e0fe2-238">**Standardzuordnung:**</span><span class="sxs-lookup"><span data-stu-id="e0fe2-238">**Default binding:**</span></span>

```json
{ "command": "closePane", "keys": "ctrl+shift+w" }
```

### <a name="move-pane-focus"></a><span data-ttu-id="e0fe2-239">Fokusbereich verschieben</span><span class="sxs-lookup"><span data-stu-id="e0fe2-239">Move pane focus</span></span>

<span data-ttu-id="e0fe2-240">Hiermit wird der Fokus in Abhängigkeit von der Richtung auf einen anderen Bereich verschoben.</span><span class="sxs-lookup"><span data-stu-id="e0fe2-240">This changes focus to a different pane depending on the direction.</span></span>

<span data-ttu-id="e0fe2-241">**Befehlsname:** `moveFocus`</span><span class="sxs-lookup"><span data-stu-id="e0fe2-241">**Command name:** `moveFocus`</span></span>

<span data-ttu-id="e0fe2-242">**Standardzuordnungen:**</span><span class="sxs-lookup"><span data-stu-id="e0fe2-242">**Default bindings:**</span></span>

```json
{ "command": { "action": "moveFocus", "direction": "down" }, "keys": "alt+down" },
{ "command": { "action": "moveFocus", "direction": "left" }, "keys": "alt+left" },
{ "command": { "action": "moveFocus", "direction": "right" }, "keys": "alt+right" },
{ "command": { "action": "moveFocus", "direction": "up" }, "keys": "alt+up" }
```

#### <a name="actions"></a><span data-ttu-id="e0fe2-243">Aktionen</span><span class="sxs-lookup"><span data-stu-id="e0fe2-243">Actions</span></span>

| <span data-ttu-id="e0fe2-244">Name</span><span class="sxs-lookup"><span data-stu-id="e0fe2-244">Name</span></span> | <span data-ttu-id="e0fe2-245">Erfordernis</span><span class="sxs-lookup"><span data-stu-id="e0fe2-245">Necessity</span></span> | <span data-ttu-id="e0fe2-246">Akzeptierter Typ</span><span class="sxs-lookup"><span data-stu-id="e0fe2-246">Accepts</span></span> | <span data-ttu-id="e0fe2-247">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e0fe2-247">Description</span></span> |
| ---- | --------- | ------- | ----------- |
| `direction` | <span data-ttu-id="e0fe2-248">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="e0fe2-248">Required</span></span> | <span data-ttu-id="e0fe2-249">`"left"`, `"right"`, `"up"`, `"down"`</span><span class="sxs-lookup"><span data-stu-id="e0fe2-249">`"left"`, `"right"`, `"up"`, `"down"`</span></span> | <span data-ttu-id="e0fe2-250">Die Richtung, in die der Fokus verschoben wird.</span><span class="sxs-lookup"><span data-stu-id="e0fe2-250">Direction in which the focus will move.</span></span> |

### <a name="resize-a-pane"></a><span data-ttu-id="e0fe2-251">Größe eines Bereichs ändern</span><span class="sxs-lookup"><span data-stu-id="e0fe2-251">Resize a pane</span></span>

<span data-ttu-id="e0fe2-252">Hiermit wird die Größe des aktiven Bereichs geändert.</span><span class="sxs-lookup"><span data-stu-id="e0fe2-252">This changes the size of the active pane.</span></span>

<span data-ttu-id="e0fe2-253">**Befehlsname:** `resizePane`</span><span class="sxs-lookup"><span data-stu-id="e0fe2-253">**Command name:** `resizePane`</span></span>

<span data-ttu-id="e0fe2-254">**Standardzuordnungen:**</span><span class="sxs-lookup"><span data-stu-id="e0fe2-254">**Default bindings:**</span></span>

```json
{ "command": { "action": "resizePane", "direction": "down" }, "keys": "alt+shift+down" },
{ "command": { "action": "resizePane", "direction": "left" }, "keys": "alt+shift+left" },
{ "command": { "action": "resizePane", "direction": "right" }, "keys": "alt+shift+right" },
{ "command": { "action": "resizePane", "direction": "up" }, "keys": "alt+shift+up" }
```

#### <a name="actions"></a><span data-ttu-id="e0fe2-255">Aktionen</span><span class="sxs-lookup"><span data-stu-id="e0fe2-255">Actions</span></span>

| <span data-ttu-id="e0fe2-256">Name</span><span class="sxs-lookup"><span data-stu-id="e0fe2-256">Name</span></span> | <span data-ttu-id="e0fe2-257">Erfordernis</span><span class="sxs-lookup"><span data-stu-id="e0fe2-257">Necessity</span></span> | <span data-ttu-id="e0fe2-258">Akzeptierter Typ</span><span class="sxs-lookup"><span data-stu-id="e0fe2-258">Accepts</span></span> | <span data-ttu-id="e0fe2-259">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e0fe2-259">Description</span></span> |
| ---- | --------- | ------- | ----------- |
| `direction` | <span data-ttu-id="e0fe2-260">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="e0fe2-260">Required</span></span> | <span data-ttu-id="e0fe2-261">`"left"`, `"right"`, `"up"`, `"down"`</span><span class="sxs-lookup"><span data-stu-id="e0fe2-261">`"left"`, `"right"`, `"up"`, `"down"`</span></span> | <span data-ttu-id="e0fe2-262">Die Richtung, in der die Größe des Bereichs geändert wird.</span><span class="sxs-lookup"><span data-stu-id="e0fe2-262">Direction in which the pane will be resized.</span></span> |

### <a name="split-a-pane"></a><span data-ttu-id="e0fe2-263">Bereich teilen</span><span class="sxs-lookup"><span data-stu-id="e0fe2-263">Split a pane</span></span>

<span data-ttu-id="e0fe2-264">Hiermit wird die Größe des aktiven Bereichs halbiert und ein weiterer geöffnet.</span><span class="sxs-lookup"><span data-stu-id="e0fe2-264">This halves the size of the active pane and opens another.</span></span> <span data-ttu-id="e0fe2-265">Ohne Argumente wird das Standardprofil in einem neuen Bereich geöffnet.</span><span class="sxs-lookup"><span data-stu-id="e0fe2-265">Without any arguments, this will open the default profile in the new pane.</span></span> <span data-ttu-id="e0fe2-266">Wenn keine Aktion angegeben ist, wird die entsprechende Einstellung des Standardprofils verwendet.</span><span class="sxs-lookup"><span data-stu-id="e0fe2-266">If an action is not specified, the default profile's equivalent setting will be used.</span></span>

<span data-ttu-id="e0fe2-267">**Befehlsname:** `splitPane`</span><span class="sxs-lookup"><span data-stu-id="e0fe2-267">**Command name:** `splitPane`</span></span>

<span data-ttu-id="e0fe2-268">**Standardzuordnungen:**</span><span class="sxs-lookup"><span data-stu-id="e0fe2-268">**Default bindings:**</span></span>

```json
// In settings.json
{ "command": { "action": "splitPane", "split": "auto", "splitMode": "duplicate" }, "keys": "alt+shift+d" },

// In defaults.json
{ "command": { "action": "splitPane", "split": "horizontal"}, "keys": "alt+shift+-" },
{ "command": { "action": "splitPane", "split": "vertical"}, "keys": "alt+shift+plus" }
```

#### <a name="actions"></a><span data-ttu-id="e0fe2-269">Aktionen</span><span class="sxs-lookup"><span data-stu-id="e0fe2-269">Actions</span></span>

| <span data-ttu-id="e0fe2-270">Name</span><span class="sxs-lookup"><span data-stu-id="e0fe2-270">Name</span></span> | <span data-ttu-id="e0fe2-271">Erfordernis</span><span class="sxs-lookup"><span data-stu-id="e0fe2-271">Necessity</span></span> | <span data-ttu-id="e0fe2-272">Akzeptierter Typ</span><span class="sxs-lookup"><span data-stu-id="e0fe2-272">Accepts</span></span> | <span data-ttu-id="e0fe2-273">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e0fe2-273">Description</span></span> |
| ---- | --------- | ------- | ----------- |
| `split` | <span data-ttu-id="e0fe2-274">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="e0fe2-274">Required</span></span> | <span data-ttu-id="e0fe2-275">`"vertical"`, `"horizontal"`, `"auto"`</span><span class="sxs-lookup"><span data-stu-id="e0fe2-275">`"vertical"`, `"horizontal"`, `"auto"`</span></span> | <span data-ttu-id="e0fe2-276">Gibt an, wie der Bereich unterteilt wird.</span><span class="sxs-lookup"><span data-stu-id="e0fe2-276">How the pane will split.</span></span> <span data-ttu-id="e0fe2-277">`"auto"` unterteilt den Bereich in der Richtung, die die größte Oberfläche bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="e0fe2-277">`"auto"` will split in the direction that provides the most surface area.</span></span> |
| `commandLine` | <span data-ttu-id="e0fe2-278">Optional</span><span class="sxs-lookup"><span data-stu-id="e0fe2-278">Optional</span></span> | <span data-ttu-id="e0fe2-279">Name der ausführbaren Datei als Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="e0fe2-279">Executable file name as a string</span></span> | <span data-ttu-id="e0fe2-280">Ausführbare Datei wird im Bereich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e0fe2-280">Executable run within the pane.</span></span> |
| `startingDirectory` | <span data-ttu-id="e0fe2-281">Optional</span><span class="sxs-lookup"><span data-stu-id="e0fe2-281">Optional</span></span> | <span data-ttu-id="e0fe2-282">Speicherort des Ordners als Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="e0fe2-282">Folder location as a string</span></span> | <span data-ttu-id="e0fe2-283">Das Verzeichnis, in dem der Bereich geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="e0fe2-283">Directory in which the pane will open.</span></span> |
| `tabTitle` | <span data-ttu-id="e0fe2-284">Optional</span><span class="sxs-lookup"><span data-stu-id="e0fe2-284">Optional</span></span> | <span data-ttu-id="e0fe2-285">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="e0fe2-285">String</span></span> | <span data-ttu-id="e0fe2-286">Titel der Registerkarte, wenn der neue Bereich den Fokus erhält.</span><span class="sxs-lookup"><span data-stu-id="e0fe2-286">Title of the tab when the new pane is focused.</span></span> |
| `index` | <span data-ttu-id="e0fe2-287">Optional</span><span class="sxs-lookup"><span data-stu-id="e0fe2-287">Optional</span></span> | <span data-ttu-id="e0fe2-288">Ganze Zahl</span><span class="sxs-lookup"><span data-stu-id="e0fe2-288">Integer</span></span> | <span data-ttu-id="e0fe2-289">Profil, das auf der Grundlage seiner Position im Dropdownmenü geöffnet wird (beginnend bei 0).</span><span class="sxs-lookup"><span data-stu-id="e0fe2-289">Profile that will open based on its position in the dropdown (starting at 0).</span></span> |
| `profile` | <span data-ttu-id="e0fe2-290">Optional</span><span class="sxs-lookup"><span data-stu-id="e0fe2-290">Optional</span></span> | <span data-ttu-id="e0fe2-291">Name oder GUID des Profils als Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="e0fe2-291">Profile's name or GUID as a string</span></span> | <span data-ttu-id="e0fe2-292">Profil, das auf der Grundlage seiner GUID oder seines Namens geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="e0fe2-292">Profile that will open based on its GUID or name.</span></span> |
| `splitMode` | <span data-ttu-id="e0fe2-293">Optional</span><span class="sxs-lookup"><span data-stu-id="e0fe2-293">Optional</span></span> | `"duplicate"` | <span data-ttu-id="e0fe2-294">Hiermit wird gesteuert, wie der Bereich unterteilt wird.</span><span class="sxs-lookup"><span data-stu-id="e0fe2-294">Controls how the pane splits.</span></span> <span data-ttu-id="e0fe2-295">Akzeptiert nur `"duplicate"`, wodurch das Profil des Fokusbereichs in einem neuen Bereich dupliziert wird.</span><span class="sxs-lookup"><span data-stu-id="e0fe2-295">Only accepts `"duplicate"`, which will duplicate the focused pane's profile into a new pane.</span></span> |

<br />

___

## <a name="clipboard-integration-commands"></a><span data-ttu-id="e0fe2-296">Befehle zur Integration der Zwischenablage</span><span class="sxs-lookup"><span data-stu-id="e0fe2-296">Clipboard integration commands</span></span>

### <a name="copy"></a><span data-ttu-id="e0fe2-297">Kopieren</span><span class="sxs-lookup"><span data-stu-id="e0fe2-297">Copy</span></span>

<span data-ttu-id="e0fe2-298">Hiermit wird der ausgewählte Terminalinhalt in die Zwischenablage kopiert.</span><span class="sxs-lookup"><span data-stu-id="e0fe2-298">This copies the selected terminal content to your clipboard.</span></span>

<span data-ttu-id="e0fe2-299">**Befehlsname:** `copy`</span><span class="sxs-lookup"><span data-stu-id="e0fe2-299">**Command name:** `copy`</span></span>

<span data-ttu-id="e0fe2-300">**Standardzuordnungen:**</span><span class="sxs-lookup"><span data-stu-id="e0fe2-300">**Default bindings:**</span></span>

```json
// In settings.json
{ "command": { "action": "copy", "singleLine": false }, "keys": "ctrl+c" },

// In defaults.json
{ "command": { "action": "copy", "singleLine": false }, "keys": "ctrl+shift+c" },
{ "command": { "action": "copy", "singleLine": false }, "keys": "ctrl+insert" }
```

#### <a name="clipboard-actions"></a><span data-ttu-id="e0fe2-301">Zwischenablageaktionen</span><span class="sxs-lookup"><span data-stu-id="e0fe2-301">Clipboard Actions</span></span>

| <span data-ttu-id="e0fe2-302">Name</span><span class="sxs-lookup"><span data-stu-id="e0fe2-302">Name</span></span> | <span data-ttu-id="e0fe2-303">Erfordernis</span><span class="sxs-lookup"><span data-stu-id="e0fe2-303">Necessity</span></span> | <span data-ttu-id="e0fe2-304">Akzeptierter Typ</span><span class="sxs-lookup"><span data-stu-id="e0fe2-304">Accepts</span></span> | <span data-ttu-id="e0fe2-305">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e0fe2-305">Description</span></span> |
| ---- | --------- | ------- | ----------- |
| `singleLine` | <span data-ttu-id="e0fe2-306">Optional</span><span class="sxs-lookup"><span data-stu-id="e0fe2-306">Optional</span></span> | <span data-ttu-id="e0fe2-307">`true`, `false`</span><span class="sxs-lookup"><span data-stu-id="e0fe2-307">`true`, `false`</span></span> | <span data-ttu-id="e0fe2-308">Bei `true` wird der kopierte Inhalt als einzelne Zeile kopiert.</span><span class="sxs-lookup"><span data-stu-id="e0fe2-308">When `true`, the copied content will be copied as a single line.</span></span> <span data-ttu-id="e0fe2-309">Bei `false` werden Zeilenvorschübe aus dem ausgewählten Text beibehalten.</span><span class="sxs-lookup"><span data-stu-id="e0fe2-309">When `false`, newlines persist from the selected text.</span></span> |

### <a name="paste"></a><span data-ttu-id="e0fe2-310">Einfügen</span><span class="sxs-lookup"><span data-stu-id="e0fe2-310">Paste</span></span>

<span data-ttu-id="e0fe2-311">Hiermit wird der Inhalt eingefügt, der in die Zwischenablage kopiert wurde.</span><span class="sxs-lookup"><span data-stu-id="e0fe2-311">This inserts the content that was copied onto the clipboard.</span></span>

<span data-ttu-id="e0fe2-312">**Befehlsname:** `paste`</span><span class="sxs-lookup"><span data-stu-id="e0fe2-312">**Command name:** `paste`</span></span>

<span data-ttu-id="e0fe2-313">**Standardzuordnungen:**</span><span class="sxs-lookup"><span data-stu-id="e0fe2-313">**Default bindings:**</span></span>

```json
// In settings.json
{ "command": "paste", "keys": "ctrl+v" },

// In defaults.json
{ "command": "paste", "keys": "ctrl+shift+v" },
{ "command": "paste", "keys": "shift+insert" }
```

<br />

___

## <a name="scrollback-commands"></a><span data-ttu-id="e0fe2-314">Befehle zum Scrollen</span><span class="sxs-lookup"><span data-stu-id="e0fe2-314">Scrollback commands</span></span>

### <a name="scroll-up"></a><span data-ttu-id="e0fe2-315">Nach oben scrollen</span><span class="sxs-lookup"><span data-stu-id="e0fe2-315">Scroll up</span></span>

<span data-ttu-id="e0fe2-316">Hiermit wird auf dem Bildschirm nach oben gescrollt.</span><span class="sxs-lookup"><span data-stu-id="e0fe2-316">This scrolls the screen up.</span></span>

<span data-ttu-id="e0fe2-317">**Befehlsname:** `scrollUp`</span><span class="sxs-lookup"><span data-stu-id="e0fe2-317">**Command name:** `scrollUp`</span></span>

<span data-ttu-id="e0fe2-318">**Standardzuordnung:**</span><span class="sxs-lookup"><span data-stu-id="e0fe2-318">**Default binding:**</span></span>

```json
{ "command": "scrollUp", "keys": "ctrl+shift+up" }
```

### <a name="scroll-down"></a><span data-ttu-id="e0fe2-319">Nach unten scrollen</span><span class="sxs-lookup"><span data-stu-id="e0fe2-319">Scroll down</span></span>

<span data-ttu-id="e0fe2-320">Hiermit wird auf dem Bildschirm nach unten gescrollt.</span><span class="sxs-lookup"><span data-stu-id="e0fe2-320">This scrolls the screen down.</span></span>

<span data-ttu-id="e0fe2-321">**Befehlsname:** `scrollDown`</span><span class="sxs-lookup"><span data-stu-id="e0fe2-321">**Command name:** `scrollDown`</span></span>

<span data-ttu-id="e0fe2-322">**Standardzuordnung:**</span><span class="sxs-lookup"><span data-stu-id="e0fe2-322">**Default binding:**</span></span>

```json
{ "command": "scrollDown", "keys": "ctrl+shift+down" }
```

### <a name="scroll-up-a-whole-page"></a><span data-ttu-id="e0fe2-323">Ganze Seite nach oben scrollen</span><span class="sxs-lookup"><span data-stu-id="e0fe2-323">Scroll up a whole page</span></span>

<span data-ttu-id="e0fe2-324">Hiermit wird der Bildschirm um eine ganze Seite nach oben gescrollt, was der Höhe des Fensters entspricht.</span><span class="sxs-lookup"><span data-stu-id="e0fe2-324">This scrolls the screen up by a whole page, which is the height of the window.</span></span>

<span data-ttu-id="e0fe2-325">**Befehlsname:** `scrollUpPage`</span><span class="sxs-lookup"><span data-stu-id="e0fe2-325">**Command name:** `scrollUpPage`</span></span>

<span data-ttu-id="e0fe2-326">**Standardzuordnung:**</span><span class="sxs-lookup"><span data-stu-id="e0fe2-326">**Default binding:**</span></span>

```json
{ "command": "scrollUpPage", "keys": "ctrl+shift+pgup" }
```

### <a name="scroll-down-a-whole-page"></a><span data-ttu-id="e0fe2-327">Ganze Seite nach unten scrollen</span><span class="sxs-lookup"><span data-stu-id="e0fe2-327">Scroll down a whole page</span></span>

<span data-ttu-id="e0fe2-328">Hiermit wird der Bildschirm um eine ganze Seite nach unten gescrollt, was der Höhe des Fensters entspricht.</span><span class="sxs-lookup"><span data-stu-id="e0fe2-328">This scrolls the screen down by a whole page, which is the height of the window.</span></span>

<span data-ttu-id="e0fe2-329">**Befehlsname:** `scrollDownPage`</span><span class="sxs-lookup"><span data-stu-id="e0fe2-329">**Command name:** `scrollDownPage`</span></span>

<span data-ttu-id="e0fe2-330">**Standardzuordnung:**</span><span class="sxs-lookup"><span data-stu-id="e0fe2-330">**Default binding:**</span></span>

```json
{ "command": "scrollDownPage", "keys": "ctrl+shift+pgdn" }
```

<br />

___

## <a name="visual-adjustment-commands"></a><span data-ttu-id="e0fe2-331">Befehle zur visuellen Anpassung</span><span class="sxs-lookup"><span data-stu-id="e0fe2-331">Visual adjustment commands</span></span>

### <a name="adjust-font-size"></a><span data-ttu-id="e0fe2-332">Schriftgrad anpassen</span><span class="sxs-lookup"><span data-stu-id="e0fe2-332">Adjust font size</span></span>

<span data-ttu-id="e0fe2-333">Hiermit wird die Textgröße um eine angegebene Punktanzahl geändert.</span><span class="sxs-lookup"><span data-stu-id="e0fe2-333">This changes the text size by a specified point amount.</span></span>

<span data-ttu-id="e0fe2-334">**Befehlsname:** `adjustFontSize`</span><span class="sxs-lookup"><span data-stu-id="e0fe2-334">**Command name:** `adjustFontSize`</span></span>

<span data-ttu-id="e0fe2-335">**Standardzuordnungen:**</span><span class="sxs-lookup"><span data-stu-id="e0fe2-335">**Default bindings:**</span></span>

```json
{ "command": { "action": "adjustFontSize", "delta": 1 }, "keys": "ctrl+=" },
{ "command": { "action": "adjustFontSize", "delta": -1 }, "keys": "ctrl+-" }
```

#### <a name="actions"></a><span data-ttu-id="e0fe2-336">Aktionen</span><span class="sxs-lookup"><span data-stu-id="e0fe2-336">Actions</span></span>

| <span data-ttu-id="e0fe2-337">Name</span><span class="sxs-lookup"><span data-stu-id="e0fe2-337">Name</span></span> | <span data-ttu-id="e0fe2-338">Erfordernis</span><span class="sxs-lookup"><span data-stu-id="e0fe2-338">Necessity</span></span> | <span data-ttu-id="e0fe2-339">Akzeptierter Typ</span><span class="sxs-lookup"><span data-stu-id="e0fe2-339">Accepts</span></span> | <span data-ttu-id="e0fe2-340">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e0fe2-340">Description</span></span> |
| ---- | --------- | ------- | ----------- |
| `delta` | <span data-ttu-id="e0fe2-341">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="e0fe2-341">Required</span></span> | <span data-ttu-id="e0fe2-342">Ganze Zahl</span><span class="sxs-lookup"><span data-stu-id="e0fe2-342">Integer</span></span> | <span data-ttu-id="e0fe2-343">Umfang der Größenänderung pro Befehlsaufruf.</span><span class="sxs-lookup"><span data-stu-id="e0fe2-343">Amount of size change per command invocation.</span></span> |

### <a name="reset-font-size"></a><span data-ttu-id="e0fe2-344">Schriftgrad zurücksetzen</span><span class="sxs-lookup"><span data-stu-id="e0fe2-344">Reset font size</span></span>

<span data-ttu-id="e0fe2-345">Hiermit wird die Textgröße auf den Standardwert zurückgesetzt.</span><span class="sxs-lookup"><span data-stu-id="e0fe2-345">This resets the text size to the default value.</span></span>

<span data-ttu-id="e0fe2-346">**Befehlsname:** `resetFontSize`</span><span class="sxs-lookup"><span data-stu-id="e0fe2-346">**Command name:** `resetFontSize`</span></span>

<span data-ttu-id="e0fe2-347">**Standardzuordnung:**</span><span class="sxs-lookup"><span data-stu-id="e0fe2-347">**Default binding:**</span></span>

```json
{ "command": "resetFontSize", "keys": "ctrl+0" }
```

<br />

___

## <a name="unbind-keys"></a><span data-ttu-id="e0fe2-348">Tastenzuordnung aufheben</span><span class="sxs-lookup"><span data-stu-id="e0fe2-348">Unbind keys</span></span>

<span data-ttu-id="e0fe2-349">Hiermit wird die Zuordnung der zu einem beliebigen Befehl zugewiesenen Tasten aufgehoben.</span><span class="sxs-lookup"><span data-stu-id="e0fe2-349">This unbinds the associated keys from any command.</span></span>

<span data-ttu-id="e0fe2-350">**Befehlsname:** `unbound`</span><span class="sxs-lookup"><span data-stu-id="e0fe2-350">**Command name:** `unbound`</span></span>
