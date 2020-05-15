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
# <a name="custom-key-bindings-in-windows-terminal"></a><span data-ttu-id="525f8-103">Benutzerdefinierte Tastenzuordnungen in Windows Terminal</span><span class="sxs-lookup"><span data-stu-id="525f8-103">Custom key bindings in Windows Terminal</span></span>

<span data-ttu-id="525f8-104">Sie können benutzerdefinierte Tastenzuordnungen (Tastenkombinationen) in Windows Terminals erstellen, die Ihnen die Kontrolle darüber geben, wie Sie über Ihre Tastatur mit dem Terminal interagieren.</span><span class="sxs-lookup"><span data-stu-id="525f8-104">You can create custom key bindings (keyboard shortcuts) inside the Windows Terminal that give you control of how you interact with the terminal using your keyboard.</span></span>

## <a name="key-binding-formats"></a><span data-ttu-id="525f8-105">Formate für Tastenzuordnungen</span><span class="sxs-lookup"><span data-stu-id="525f8-105">Key binding formats</span></span>

<span data-ttu-id="525f8-106">Tastenzuordnungen können in den folgenden Formaten strukturiert werden:</span><span class="sxs-lookup"><span data-stu-id="525f8-106">Key bindings can be structured in the following formats:</span></span>

### <a name="commands-without-arguments"></a><span data-ttu-id="525f8-107">Befehle ohne Argumente</span><span class="sxs-lookup"><span data-stu-id="525f8-107">Commands without arguments</span></span>

```json
{ "command": "commandName", "keys": "modifiers+key" }
```

<span data-ttu-id="525f8-108">Diese Standardeinstellung verwendet z. B. die Tastenzuordnung <kbd>ALT+F4</kbd>, um das Terminalfenster zu schließen:</span><span class="sxs-lookup"><span data-stu-id="525f8-108">For example, this default setting uses the shortcut key <kbd>alt+f4</kbd> to close the terminal window:</span></span>

```json
{ "command": "closeWindow", "keys": "alt+f4" }
```

### <a name="commands-with-arguments"></a><span data-ttu-id="525f8-109">Befehle mit Argumenten</span><span class="sxs-lookup"><span data-stu-id="525f8-109">Commands with arguments</span></span>

```json
{ "command": { "action": "commandName", "argument": "value" }, "keys": "modifiers+key" }
```

<span data-ttu-id="525f8-110">Bei dieser Standardeinstellung wird z. B. die Tastenzuordnung <kbd>STRG+UMSCHALT+1</kbd> verwendet, um eine neue Registerkarte im Terminal zu öffnen, je nachdem, welches Profil in Ihrem Dropdownmenü zuerst aufgeführt ist (in der Regel wird dadurch das PowerShell-Profil geöffnet):</span><span class="sxs-lookup"><span data-stu-id="525f8-110">For example, this default setting uses the shortcut key <kbd>ctrl+shift+1</kbd> to open a new tab in the terminal based on whichever profile is listed first in your dropdown menu (typically this will open the PowerShell profile):</span></span>

```json
{ "command": { "action": "newTab", "index": 0 }, "keys": "ctrl+shift+1" }
```

<br />

___

## <a name="key-binding-properties"></a><span data-ttu-id="525f8-111">Eigenschaften für Tastenzuordnungen</span><span class="sxs-lookup"><span data-stu-id="525f8-111">Key binding properties</span></span>

<span data-ttu-id="525f8-112">Tastenzuordnungen können unter Verwendung der folgenden Eigenschaften konstruiert werden.</span><span class="sxs-lookup"><span data-stu-id="525f8-112">Key bindings can be constructed using the following properties.</span></span>

### <a name="command"></a><span data-ttu-id="525f8-113">Befehl</span><span class="sxs-lookup"><span data-stu-id="525f8-113">Command</span></span>

<span data-ttu-id="525f8-114">Dies ist der Befehl, der ausgeführt wird, wenn die zugehörigen Tasten gedrückt werden.</span><span class="sxs-lookup"><span data-stu-id="525f8-114">This is the command executed when the associated keys are pressed.</span></span>

<span data-ttu-id="525f8-115">**Eigenschaftenname:** `command`</span><span class="sxs-lookup"><span data-stu-id="525f8-115">**Property name:** `command`</span></span>

<span data-ttu-id="525f8-116">**Erfordernis:** Erforderlich</span><span class="sxs-lookup"><span data-stu-id="525f8-116">**Necessity:** Required</span></span>

<span data-ttu-id="525f8-117">**Akzeptiert:** Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="525f8-117">**Accepts:** String</span></span>

### <a name="keys"></a><span data-ttu-id="525f8-118">Tasten</span><span class="sxs-lookup"><span data-stu-id="525f8-118">Keys</span></span>

<span data-ttu-id="525f8-119">Hiermit werden die Tastenkombinationen definiert, mit denen der Befehl aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="525f8-119">This defines the key combinations used to call the command.</span></span> <span data-ttu-id="525f8-120">Tasten können eine beliebige Anzahl von Zusatztasten mit einer Taste aufweisen.</span><span class="sxs-lookup"><span data-stu-id="525f8-120">Keys can have any number of modifiers with one key.</span></span> <span data-ttu-id="525f8-121">Akzeptierte Zusatztasten und Tasten sind [unten](#accepted-modifiers-and-keys) aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="525f8-121">Accepted modifiers and keys are listed [below](#accepted-modifiers-and-keys).</span></span>

<span data-ttu-id="525f8-122">**Eigenschaftenname:** `keys`</span><span class="sxs-lookup"><span data-stu-id="525f8-122">**Property name:** `keys`</span></span>

<span data-ttu-id="525f8-123">**Erfordernis:** Erforderlich</span><span class="sxs-lookup"><span data-stu-id="525f8-123">**Necessity:** Required</span></span>

<span data-ttu-id="525f8-124">**Akzeptiert:** Zeichenfolge oder Array [Zeichenfolge]</span><span class="sxs-lookup"><span data-stu-id="525f8-124">**Accepts:** String or array[string]</span></span>

### <a name="action"></a><span data-ttu-id="525f8-125">Action</span><span class="sxs-lookup"><span data-stu-id="525f8-125">Action</span></span>

<span data-ttu-id="525f8-126">Hiermit werden bestimmten Befehlen zusätzliche Funktionen hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="525f8-126">This adds additional functionality to certain commands.</span></span>

<span data-ttu-id="525f8-127">**Eigenschaftenname:** `action`</span><span class="sxs-lookup"><span data-stu-id="525f8-127">**Property name:** `action`</span></span>

<span data-ttu-id="525f8-128">**Erfordernis:** Optional</span><span class="sxs-lookup"><span data-stu-id="525f8-128">**Necessity:** Optional</span></span>

<span data-ttu-id="525f8-129">**Akzeptiert:** Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="525f8-129">**Accepts:** String</span></span>

<br />

___

## <a name="accepted-modifiers-and-keys"></a><span data-ttu-id="525f8-130">Akzeptierte Zusatztasten und Tasten</span><span class="sxs-lookup"><span data-stu-id="525f8-130">Accepted modifiers and keys</span></span>

### <a name="modifiers"></a><span data-ttu-id="525f8-131">Zusatztasten</span><span class="sxs-lookup"><span data-stu-id="525f8-131">Modifiers</span></span>

<span data-ttu-id="525f8-132">`ctrl+`, `shift+`, `alt+`</span><span class="sxs-lookup"><span data-stu-id="525f8-132">`ctrl+`, `shift+`, `alt+`</span></span>

### <a name="modifier-keys"></a><span data-ttu-id="525f8-133">Zusatztasten</span><span class="sxs-lookup"><span data-stu-id="525f8-133">Modifier keys</span></span>

| <span data-ttu-id="525f8-134">Type</span><span class="sxs-lookup"><span data-stu-id="525f8-134">Type</span></span> | <span data-ttu-id="525f8-135">Tasten</span><span class="sxs-lookup"><span data-stu-id="525f8-135">Keys</span></span> |
| ---- | ---- |
| <span data-ttu-id="525f8-136">Funktions- und alphanumerische Tasten</span><span class="sxs-lookup"><span data-stu-id="525f8-136">Function and alphanumeric keys</span></span> | <span data-ttu-id="525f8-137">`f1-f24`, `a-z`, `0-9`</span><span class="sxs-lookup"><span data-stu-id="525f8-137">`f1-f24`, `a-z`, `0-9`</span></span> |
| <span data-ttu-id="525f8-138">Sonderzeichen</span><span class="sxs-lookup"><span data-stu-id="525f8-138">Symbols</span></span> | <span data-ttu-id="525f8-139">``` ` ```, `-`, `=`, `[`, `]`, `\`, `;`, `'`, `,`, `.`, `/`</span><span class="sxs-lookup"><span data-stu-id="525f8-139">``` ` ```, `-`, `=`, `[`, `]`, `\`, `;`, `'`, `,`, `.`, `/`</span></span> |
| <span data-ttu-id="525f8-140">Pfeiltasten</span><span class="sxs-lookup"><span data-stu-id="525f8-140">Arrow keys</span></span> | <span data-ttu-id="525f8-141">`down`, `left`, `right`, `up`, `pagedown`, `pageup`, `pgdn`, `pgup`, `end`, `home`, `plus`</span><span class="sxs-lookup"><span data-stu-id="525f8-141">`down`, `left`, `right`, `up`, `pagedown`, `pageup`, `pgdn`, `pgup`, `end`, `home`, `plus`</span></span> |
| <span data-ttu-id="525f8-142">Aktionstasten</span><span class="sxs-lookup"><span data-stu-id="525f8-142">Action keys</span></span> | <span data-ttu-id="525f8-143">`tab`, `enter`, `esc`, `escape`, `space`, `backspace`, `delete`, `insert`</span><span class="sxs-lookup"><span data-stu-id="525f8-143">`tab`, `enter`, `esc`, `escape`, `space`, `backspace`, `delete`, `insert`</span></span> |
| <span data-ttu-id="525f8-144">Tasten des Ziffernblocks</span><span class="sxs-lookup"><span data-stu-id="525f8-144">Numpad keys</span></span> | <span data-ttu-id="525f8-145">`numpad_0-numpad_9`, `numpad0-numpad9`, `numpad_add`, `numpad_plus`, `numpad_decimal`, `numpad_period`, `numpad_divide`, `numpad_minus`, `numpad_subtract`, `numpad_multiply`</span><span class="sxs-lookup"><span data-stu-id="525f8-145">`numpad_0-numpad_9`, `numpad0-numpad9`, `numpad_add`, `numpad_plus`, `numpad_decimal`, `numpad_period`, `numpad_divide`, `numpad_minus`, `numpad_subtract`, `numpad_multiply`</span></span> |

<br />

___

## <a name="application-level-commands"></a><span data-ttu-id="525f8-146">Befehle auf Anwendungsebene</span><span class="sxs-lookup"><span data-stu-id="525f8-146">Application-level commands</span></span>

### <a name="close-window"></a><span data-ttu-id="525f8-147">Fenster schließen</span><span class="sxs-lookup"><span data-stu-id="525f8-147">Close window</span></span>

:::row:::
:::column span="":::
<span data-ttu-id="525f8-148">Hiermit werden das aktuelle Fenster und alle darin enthaltenen Registerkarten geschlossen.</span><span class="sxs-lookup"><span data-stu-id="525f8-148">This closes the current window and all tabs within it.</span></span> <span data-ttu-id="525f8-149">Wenn `confirmCloseAllTabs` auf `true` festgelegt ist, wird ein Dialogfenster zur Bestätigung angezeigt, um sicherzustellen, dass Sie alle Registerkarten schließen möchten.</span><span class="sxs-lookup"><span data-stu-id="525f8-149">If `confirmCloseAllTabs` is set to `true`, a confirmation dialog will appear to ensure you'd like to close all your tabs.</span></span> <span data-ttu-id="525f8-150">Weitere Informationen zu dieser Einstellung finden Sie auf der Seite [Globale Einstellungen](./global-settings.md#hide-close-all-tabs-popup).</span><span class="sxs-lookup"><span data-stu-id="525f8-150">More information on this setting can be found on the [Global settings page](./global-settings.md#hide-close-all-tabs-popup).</span></span>

<span data-ttu-id="525f8-151">**Befehlsname:** `closeWindow`</span><span class="sxs-lookup"><span data-stu-id="525f8-151">**Command name:** `closeWindow`</span></span>

<span data-ttu-id="525f8-152">**Standardzuordnung:**</span><span class="sxs-lookup"><span data-stu-id="525f8-152">**Default binding:**</span></span>

```json
{ "command": "closeWindow", "keys": "alt+f4" }
```

:::column-end:::
:::column span="":::
![Windows Terminal: Bestätigung zum Schließen aller Registerkarten](./../images/confirm-close-all-tabs.png)

:::column-end:::
:::row-end:::

### <a name="find"></a><span data-ttu-id="525f8-154">Suchen</span><span class="sxs-lookup"><span data-stu-id="525f8-154">Find</span></span>

<span data-ttu-id="525f8-155">Hiermit wird das Suchdialogfeld geöffnet.</span><span class="sxs-lookup"><span data-stu-id="525f8-155">This opens the search dialog box.</span></span> <span data-ttu-id="525f8-156">Weitere Informationen zur Suche finden Sie auf der Seite [Suchen](./../search.md).</span><span class="sxs-lookup"><span data-stu-id="525f8-156">More information on search can be found on the [Search page](./../search.md).</span></span>

<span data-ttu-id="525f8-157">**Befehlsname:** `find`</span><span class="sxs-lookup"><span data-stu-id="525f8-157">**Command name:** `find`</span></span>

<span data-ttu-id="525f8-158">**Standardzuordnung:**</span><span class="sxs-lookup"><span data-stu-id="525f8-158">**Default binding:**</span></span>

```json
{ "command": "find", "keys": "ctrl+shift+f" }
```

### <a name="open-the-dropdown"></a><span data-ttu-id="525f8-159">Dropdownmenü öffnen</span><span class="sxs-lookup"><span data-stu-id="525f8-159">Open the dropdown</span></span>

<span data-ttu-id="525f8-160">Hiermit wird das Dropdownmenü geöffnet.</span><span class="sxs-lookup"><span data-stu-id="525f8-160">This opens the dropdown menu.</span></span>

<span data-ttu-id="525f8-161">**Befehlsname:** `openNewTabDropdown`</span><span class="sxs-lookup"><span data-stu-id="525f8-161">**Command name:** `openNewTabDropdown`</span></span>

<span data-ttu-id="525f8-162">**Standardzuordnung:**</span><span class="sxs-lookup"><span data-stu-id="525f8-162">**Default binding:**</span></span>

```json
{ "command": "openNewTabDropdown", "keys": "ctrl+shift+space" }
```

### <a name="open-settings-file"></a><span data-ttu-id="525f8-163">Einstellungsdatei öffnen</span><span class="sxs-lookup"><span data-stu-id="525f8-163">Open settings file</span></span>

<span data-ttu-id="525f8-164">Hiermit wird die Einstellungsdatei geöffnet.</span><span class="sxs-lookup"><span data-stu-id="525f8-164">This opens the settings file.</span></span>

<span data-ttu-id="525f8-165">**Befehlsname:** `openSettings`</span><span class="sxs-lookup"><span data-stu-id="525f8-165">**Command name:** `openSettings`</span></span>

<span data-ttu-id="525f8-166">**Standardzuordnung:**</span><span class="sxs-lookup"><span data-stu-id="525f8-166">**Default binding:**</span></span>

```json
{ "command": "openSettings", "keys": "ctrl+," }
```

### <a name="toggle-full-screen"></a><span data-ttu-id="525f8-167">Vollbildmodus ein-/ausschalten</span><span class="sxs-lookup"><span data-stu-id="525f8-167">Toggle full screen</span></span>

<span data-ttu-id="525f8-168">Dies ermöglicht es Ihnen, zwischen dem Vollbildmodus und den Standardfenstergrößen zu wechseln.</span><span class="sxs-lookup"><span data-stu-id="525f8-168">This allows you to switch between full screen and default window sizes.</span></span>

<span data-ttu-id="525f8-169">**Befehlsname:** `toggleFullscreen`</span><span class="sxs-lookup"><span data-stu-id="525f8-169">**Command name:** `toggleFullscreen`</span></span>

<span data-ttu-id="525f8-170">**Standardzuordnungen:**</span><span class="sxs-lookup"><span data-stu-id="525f8-170">**Default bindings:**</span></span>

```json
{ "command": "toggleFullscreen", "keys": "alt+enter" },
{ "command": "toggleFullscreen", "keys": "f11" }
```

<br />

___

## <a name="tab-management-commands"></a><span data-ttu-id="525f8-171">Befehle zur Registerkartenverwaltung</span><span class="sxs-lookup"><span data-stu-id="525f8-171">Tab management commands</span></span>

### <a name="close-tab"></a><span data-ttu-id="525f8-172">Registerkarte schließen</span><span class="sxs-lookup"><span data-stu-id="525f8-172">Close tab</span></span>

<span data-ttu-id="525f8-173">Hiermit wird die aktuelle Registerkarte geschlossen.</span><span class="sxs-lookup"><span data-stu-id="525f8-173">This closes the current tab.</span></span>

<span data-ttu-id="525f8-174">**Befehlsname:** `closeTab`</span><span class="sxs-lookup"><span data-stu-id="525f8-174">**Command name:** `closeTab`</span></span>

### <a name="duplicate-tab"></a><span data-ttu-id="525f8-175">Registerkarte duplizieren</span><span class="sxs-lookup"><span data-stu-id="525f8-175">Duplicate tab</span></span>

<span data-ttu-id="525f8-176">Hiermit wird eine Kopie der aktuellen Registerkarte erstellt und geöffnet.</span><span class="sxs-lookup"><span data-stu-id="525f8-176">This makes a copy of the current tab and opens it.</span></span>

<span data-ttu-id="525f8-177">**Befehlsname:** `duplicateTab`</span><span class="sxs-lookup"><span data-stu-id="525f8-177">**Command name:** `duplicateTab`</span></span>

<span data-ttu-id="525f8-178">**Standardzuordnung:**</span><span class="sxs-lookup"><span data-stu-id="525f8-178">**Default binding:**</span></span>

```json
{ "command": "duplicateTab", "keys": "ctrl+shift+d" }
```

### <a name="new-tab"></a><span data-ttu-id="525f8-179">Neue Registerkarte</span><span class="sxs-lookup"><span data-stu-id="525f8-179">New tab</span></span>

<span data-ttu-id="525f8-180">Hiermit wird eine neue Registerkarte erstellt. Ohne Argumente wird das Standardprofil in einer neuen Registerkarte geöffnet. Wenn keine Aktion angegeben ist, wird die entsprechende Einstellung des Standardprofils verwendet.</span><span class="sxs-lookup"><span data-stu-id="525f8-180">This creates a new tab. Without any arguments, this will open the default profile in a new tab. If an action is not specified, the default profile's equivalent setting will be used.</span></span>

<span data-ttu-id="525f8-181">**Befehlsname:** `newTab`</span><span class="sxs-lookup"><span data-stu-id="525f8-181">**Command name:** `newTab`</span></span>

<span data-ttu-id="525f8-182">**Standardzuordnungen:**</span><span class="sxs-lookup"><span data-stu-id="525f8-182">**Default bindings:**</span></span>

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

#### <a name="actions"></a><span data-ttu-id="525f8-183">Aktionen</span><span class="sxs-lookup"><span data-stu-id="525f8-183">Actions</span></span>

| <span data-ttu-id="525f8-184">Name</span><span class="sxs-lookup"><span data-stu-id="525f8-184">Name</span></span> | <span data-ttu-id="525f8-185">Erfordernis</span><span class="sxs-lookup"><span data-stu-id="525f8-185">Necessity</span></span> | <span data-ttu-id="525f8-186">Akzeptierter Typ</span><span class="sxs-lookup"><span data-stu-id="525f8-186">Accepts</span></span> | <span data-ttu-id="525f8-187">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="525f8-187">Description</span></span> |
| ---- | --------- | ------- | ----------- |
| `commandLine` | <span data-ttu-id="525f8-188">Optional</span><span class="sxs-lookup"><span data-stu-id="525f8-188">Optional</span></span> | <span data-ttu-id="525f8-189">Name der ausführbaren Datei als Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="525f8-189">Executable file name as a string</span></span> | <span data-ttu-id="525f8-190">Ausführbare Datei wird auf der Registerkarte ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="525f8-190">Executable run within the tab.</span></span> |
| `startingDirectory` | <span data-ttu-id="525f8-191">Optional</span><span class="sxs-lookup"><span data-stu-id="525f8-191">Optional</span></span> | <span data-ttu-id="525f8-192">Speicherort des Ordners als Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="525f8-192">Folder location as a string</span></span> | <span data-ttu-id="525f8-193">Das Verzeichnis, in dem die Registerkarte geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="525f8-193">Directory in which the tab will open.</span></span> |
| `tabTitle` | <span data-ttu-id="525f8-194">Optional</span><span class="sxs-lookup"><span data-stu-id="525f8-194">Optional</span></span> | <span data-ttu-id="525f8-195">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="525f8-195">String</span></span> | <span data-ttu-id="525f8-196">Der Titel der neuen Registerkarte.</span><span class="sxs-lookup"><span data-stu-id="525f8-196">Title of the new tab.</span></span> |
| `index` | <span data-ttu-id="525f8-197">Optional</span><span class="sxs-lookup"><span data-stu-id="525f8-197">Optional</span></span> | <span data-ttu-id="525f8-198">Ganze Zahl</span><span class="sxs-lookup"><span data-stu-id="525f8-198">Integer</span></span> | <span data-ttu-id="525f8-199">Profil, das auf der Grundlage seiner Position im Dropdownmenü geöffnet wird (beginnend bei 0).</span><span class="sxs-lookup"><span data-stu-id="525f8-199">Profile that will open based on its position in the dropdown (starting at 0).</span></span> |
| `profile` | <span data-ttu-id="525f8-200">Optional</span><span class="sxs-lookup"><span data-stu-id="525f8-200">Optional</span></span> | <span data-ttu-id="525f8-201">Name oder GUID des Profils als Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="525f8-201">Profile's name or GUID as a string</span></span> | <span data-ttu-id="525f8-202">Profil, das auf der Grundlage seiner GUID oder seines Namens geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="525f8-202">Profile that will open based on its GUID or name.</span></span> |

### <a name="open-next-tab"></a><span data-ttu-id="525f8-203">Nächste Registerkarte öffnen</span><span class="sxs-lookup"><span data-stu-id="525f8-203">Open next tab</span></span>

<span data-ttu-id="525f8-204">Hiermit wird die Registerkarte rechts von der aktuellen geöffnet.</span><span class="sxs-lookup"><span data-stu-id="525f8-204">This opens the tab to the right of the current one.</span></span>

<span data-ttu-id="525f8-205">**Befehlsname:** `nextTab`</span><span class="sxs-lookup"><span data-stu-id="525f8-205">**Command name:** `nextTab`</span></span>

<span data-ttu-id="525f8-206">**Standardzuordnung:**</span><span class="sxs-lookup"><span data-stu-id="525f8-206">**Default binding:**</span></span>

```json
{ "command": "nextTab", "keys": "ctrl+tab" }
```

### <a name="open-previous-tab"></a><span data-ttu-id="525f8-207">Vorherige Registerkarte öffnen</span><span class="sxs-lookup"><span data-stu-id="525f8-207">Open previous tab</span></span>

<span data-ttu-id="525f8-208">Hiermit wird die Registerkarte links von der aktuellen geöffnet.</span><span class="sxs-lookup"><span data-stu-id="525f8-208">This opens the tab to the left of the current one.</span></span>

<span data-ttu-id="525f8-209">**Befehlsname:** `prevTab`</span><span class="sxs-lookup"><span data-stu-id="525f8-209">**Command name:** `prevTab`</span></span>

<span data-ttu-id="525f8-210">**Standardzuordnung:**</span><span class="sxs-lookup"><span data-stu-id="525f8-210">**Default binding:**</span></span>

```json
{ "command": "prevTab", "keys": "ctrl+shift+tab" }
```

### <a name="open-a-specific-tab"></a><span data-ttu-id="525f8-211">Bestimmte Registerkarte öffnen</span><span class="sxs-lookup"><span data-stu-id="525f8-211">Open a specific tab</span></span>

<span data-ttu-id="525f8-212">Hiermit wird abhängig vom Index eine bestimmte Registerkarte geöffnet.</span><span class="sxs-lookup"><span data-stu-id="525f8-212">This opens a specific tab depending on the index.</span></span>

<span data-ttu-id="525f8-213">**Befehlsname:** `switchToTab`</span><span class="sxs-lookup"><span data-stu-id="525f8-213">**Command name:** `switchToTab`</span></span>

<span data-ttu-id="525f8-214">**Standardzuordnungen:**</span><span class="sxs-lookup"><span data-stu-id="525f8-214">**Default bindings:**</span></span>

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

#### <a name="actions"></a><span data-ttu-id="525f8-215">Aktionen</span><span class="sxs-lookup"><span data-stu-id="525f8-215">Actions</span></span>

| <span data-ttu-id="525f8-216">Name</span><span class="sxs-lookup"><span data-stu-id="525f8-216">Name</span></span> | <span data-ttu-id="525f8-217">Erfordernis</span><span class="sxs-lookup"><span data-stu-id="525f8-217">Necessity</span></span> | <span data-ttu-id="525f8-218">Akzeptierter Typ</span><span class="sxs-lookup"><span data-stu-id="525f8-218">Accepts</span></span> | <span data-ttu-id="525f8-219">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="525f8-219">Description</span></span> |
| ---- | --------- | ------- | ----------- |
| `index` | <span data-ttu-id="525f8-220">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="525f8-220">Required</span></span> | <span data-ttu-id="525f8-221">Ganze Zahl</span><span class="sxs-lookup"><span data-stu-id="525f8-221">Integer</span></span> | <span data-ttu-id="525f8-222">Registerkarte, die auf der Grundlage ihrer Position in der Registerkartenleiste geöffnet wird (beginnend bei 0).</span><span class="sxs-lookup"><span data-stu-id="525f8-222">Tab that will open based on its position in the tab bar (starting at 0).</span></span> |

<br />

___

## <a name="pane-management-commands"></a><span data-ttu-id="525f8-223">Befehle zur Bereichsverwaltung</span><span class="sxs-lookup"><span data-stu-id="525f8-223">Pane management commands</span></span>

### <a name="close-pane"></a><span data-ttu-id="525f8-224">Bereich schließen</span><span class="sxs-lookup"><span data-stu-id="525f8-224">Close pane</span></span>

<span data-ttu-id="525f8-225">Hiermit wird der aktive Bereich geschlossen.</span><span class="sxs-lookup"><span data-stu-id="525f8-225">This closes the active pane.</span></span> <span data-ttu-id="525f8-226">Wenn keine geteilten Bereiche vorhanden sind, wird die aktuelle Registerkarte geschlossen. Wenn nur eine Registerkarte geöffnet ist, wird das Fenster geschlossen.</span><span class="sxs-lookup"><span data-stu-id="525f8-226">If there aren't any split panes, this will close the current tab. If there is only one tab open, this will close the window.</span></span>

<span data-ttu-id="525f8-227">**Befehlsname:** `closePane`</span><span class="sxs-lookup"><span data-stu-id="525f8-227">**Command name:** `closePane`</span></span>

<span data-ttu-id="525f8-228">**Standardzuordnung:**</span><span class="sxs-lookup"><span data-stu-id="525f8-228">**Default binding:**</span></span>

```json
{ "command": "closePane", "keys": "ctrl+shift+w" }
```

### <a name="move-pane-focus"></a><span data-ttu-id="525f8-229">Fokusbereich verschieben</span><span class="sxs-lookup"><span data-stu-id="525f8-229">Move pane focus</span></span>

<span data-ttu-id="525f8-230">Hiermit wird der Fokus in Abhängigkeit von der Richtung auf einen anderen Bereich verschoben.</span><span class="sxs-lookup"><span data-stu-id="525f8-230">This changes focus to a different pane depending on the direction.</span></span>

<span data-ttu-id="525f8-231">**Befehlsname:** `moveFocus`</span><span class="sxs-lookup"><span data-stu-id="525f8-231">**Command name:** `moveFocus`</span></span>

<span data-ttu-id="525f8-232">**Standardzuordnungen:**</span><span class="sxs-lookup"><span data-stu-id="525f8-232">**Default bindings:**</span></span>

```json
{ "command": { "action": "moveFocus", "direction": "down" }, "keys": "alt+down" },
{ "command": { "action": "moveFocus", "direction": "left" }, "keys": "alt+left" },
{ "command": { "action": "moveFocus", "direction": "right" }, "keys": "alt+right" },
{ "command": { "action": "moveFocus", "direction": "up" }, "keys": "alt+up" }
```

#### <a name="actions"></a><span data-ttu-id="525f8-233">Aktionen</span><span class="sxs-lookup"><span data-stu-id="525f8-233">Actions</span></span>

| <span data-ttu-id="525f8-234">Name</span><span class="sxs-lookup"><span data-stu-id="525f8-234">Name</span></span> | <span data-ttu-id="525f8-235">Erfordernis</span><span class="sxs-lookup"><span data-stu-id="525f8-235">Necessity</span></span> | <span data-ttu-id="525f8-236">Akzeptierter Typ</span><span class="sxs-lookup"><span data-stu-id="525f8-236">Accepts</span></span> | <span data-ttu-id="525f8-237">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="525f8-237">Description</span></span> |
| ---- | --------- | ------- | ----------- |
| `direction` | <span data-ttu-id="525f8-238">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="525f8-238">Required</span></span> | <span data-ttu-id="525f8-239">`"left"`, `"right"`, `"up"`, `"down"`</span><span class="sxs-lookup"><span data-stu-id="525f8-239">`"left"`, `"right"`, `"up"`, `"down"`</span></span> | <span data-ttu-id="525f8-240">Die Richtung, in die der Fokus verschoben wird.</span><span class="sxs-lookup"><span data-stu-id="525f8-240">Direction in which the focus will move.</span></span> |

### <a name="resize-a-pane"></a><span data-ttu-id="525f8-241">Größe eines Bereichs ändern</span><span class="sxs-lookup"><span data-stu-id="525f8-241">Resize a pane</span></span>

<span data-ttu-id="525f8-242">Hiermit wird die Größe des aktiven Bereichs geändert.</span><span class="sxs-lookup"><span data-stu-id="525f8-242">This changes the size of the active pane.</span></span>

<span data-ttu-id="525f8-243">**Befehlsname:** `resizePane`</span><span class="sxs-lookup"><span data-stu-id="525f8-243">**Command name:** `resizePane`</span></span>

<span data-ttu-id="525f8-244">**Standardzuordnungen:**</span><span class="sxs-lookup"><span data-stu-id="525f8-244">**Default bindings:**</span></span>

```json
{ "command": { "action": "resizePane", "direction": "down" }, "keys": "alt+shift+down" },
{ "command": { "action": "resizePane", "direction": "left" }, "keys": "alt+shift+left" },
{ "command": { "action": "resizePane", "direction": "right" }, "keys": "alt+shift+right" },
{ "command": { "action": "resizePane", "direction": "up" }, "keys": "alt+shift+up" }
```

#### <a name="actions"></a><span data-ttu-id="525f8-245">Aktionen</span><span class="sxs-lookup"><span data-stu-id="525f8-245">Actions</span></span>

| <span data-ttu-id="525f8-246">Name</span><span class="sxs-lookup"><span data-stu-id="525f8-246">Name</span></span> | <span data-ttu-id="525f8-247">Erfordernis</span><span class="sxs-lookup"><span data-stu-id="525f8-247">Necessity</span></span> | <span data-ttu-id="525f8-248">Akzeptierter Typ</span><span class="sxs-lookup"><span data-stu-id="525f8-248">Accepts</span></span> | <span data-ttu-id="525f8-249">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="525f8-249">Description</span></span> |
| ---- | --------- | ------- | ----------- |
| `direction` | <span data-ttu-id="525f8-250">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="525f8-250">Required</span></span> | <span data-ttu-id="525f8-251">`"left"`, `"right"`, `"up"`, `"down"`</span><span class="sxs-lookup"><span data-stu-id="525f8-251">`"left"`, `"right"`, `"up"`, `"down"`</span></span> | <span data-ttu-id="525f8-252">Die Richtung, in der die Größe des Bereichs geändert wird.</span><span class="sxs-lookup"><span data-stu-id="525f8-252">Direction in which the pane will be resized.</span></span> |

### <a name="split-a-pane"></a><span data-ttu-id="525f8-253">Bereich teilen</span><span class="sxs-lookup"><span data-stu-id="525f8-253">Split a pane</span></span>

<span data-ttu-id="525f8-254">Hiermit wird die Größe des aktiven Bereichs halbiert und ein weiterer geöffnet.</span><span class="sxs-lookup"><span data-stu-id="525f8-254">This halves the size of the active pane and opens another.</span></span> <span data-ttu-id="525f8-255">Ohne Argumente wird das Standardprofil in einem neuen Bereich geöffnet.</span><span class="sxs-lookup"><span data-stu-id="525f8-255">Without any arguments, this will open the default profile in the new pane.</span></span> <span data-ttu-id="525f8-256">Wenn keine Aktion angegeben ist, wird die entsprechende Einstellung des Standardprofils verwendet.</span><span class="sxs-lookup"><span data-stu-id="525f8-256">If an action is not specified, the default profile's equivalent setting will be used.</span></span>

<span data-ttu-id="525f8-257">**Befehlsname:** `splitPane`</span><span class="sxs-lookup"><span data-stu-id="525f8-257">**Command name:** `splitPane`</span></span>

<span data-ttu-id="525f8-258">**Standardzuordnungen:**</span><span class="sxs-lookup"><span data-stu-id="525f8-258">**Default bindings:**</span></span>

```json
// In settings.json
{ "command": { "action": "splitPane", "split": "auto", "splitMode": "duplicate" }, "keys": "alt+shift+d" },

// In defaults.json
{ "command": { "action": "splitPane", "split": "horizontal"}, "keys": "alt+shift+-" },
{ "command": { "action": "splitPane", "split": "vertical"}, "keys": "alt+shift+plus" }
```

#### <a name="actions"></a><span data-ttu-id="525f8-259">Aktionen</span><span class="sxs-lookup"><span data-stu-id="525f8-259">Actions</span></span>

| <span data-ttu-id="525f8-260">Name</span><span class="sxs-lookup"><span data-stu-id="525f8-260">Name</span></span> | <span data-ttu-id="525f8-261">Erfordernis</span><span class="sxs-lookup"><span data-stu-id="525f8-261">Necessity</span></span> | <span data-ttu-id="525f8-262">Akzeptierter Typ</span><span class="sxs-lookup"><span data-stu-id="525f8-262">Accepts</span></span> | <span data-ttu-id="525f8-263">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="525f8-263">Description</span></span> |
| ---- | --------- | ------- | ----------- |
| `split` | <span data-ttu-id="525f8-264">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="525f8-264">Required</span></span> | <span data-ttu-id="525f8-265">`"vertical"`, `"horizontal"`, `"auto"`</span><span class="sxs-lookup"><span data-stu-id="525f8-265">`"vertical"`, `"horizontal"`, `"auto"`</span></span> | <span data-ttu-id="525f8-266">Gibt an, wie der Bereich unterteilt wird.</span><span class="sxs-lookup"><span data-stu-id="525f8-266">How the pane will split.</span></span> <span data-ttu-id="525f8-267">`"auto"` unterteilt den Bereich in der Richtung, die die größte Oberfläche bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="525f8-267">`"auto"` will split in the direction that provides the most surface area.</span></span> |
| `commandLine` | <span data-ttu-id="525f8-268">Optional</span><span class="sxs-lookup"><span data-stu-id="525f8-268">Optional</span></span> | <span data-ttu-id="525f8-269">Name der ausführbaren Datei als Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="525f8-269">Executable file name as a string</span></span> | <span data-ttu-id="525f8-270">Ausführbare Datei wird im Bereich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="525f8-270">Executable run within the pane.</span></span> |
| `startingDirectory` | <span data-ttu-id="525f8-271">Optional</span><span class="sxs-lookup"><span data-stu-id="525f8-271">Optional</span></span> | <span data-ttu-id="525f8-272">Speicherort des Ordners als Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="525f8-272">Folder location as a string</span></span> | <span data-ttu-id="525f8-273">Das Verzeichnis, in dem der Bereich geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="525f8-273">Directory in which the pane will open.</span></span> |
| `tabTitle` | <span data-ttu-id="525f8-274">Optional</span><span class="sxs-lookup"><span data-stu-id="525f8-274">Optional</span></span> | <span data-ttu-id="525f8-275">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="525f8-275">String</span></span> | <span data-ttu-id="525f8-276">Titel der Registerkarte, wenn der neue Bereich den Fokus erhält.</span><span class="sxs-lookup"><span data-stu-id="525f8-276">Title of the tab when the new pane is focused.</span></span> |
| `index` | <span data-ttu-id="525f8-277">Optional</span><span class="sxs-lookup"><span data-stu-id="525f8-277">Optional</span></span> | <span data-ttu-id="525f8-278">Ganze Zahl</span><span class="sxs-lookup"><span data-stu-id="525f8-278">Integer</span></span> | <span data-ttu-id="525f8-279">Profil, das auf der Grundlage seiner Position im Dropdownmenü geöffnet wird (beginnend bei 0).</span><span class="sxs-lookup"><span data-stu-id="525f8-279">Profile that will open based on its position in the dropdown (starting at 0).</span></span> |
| `profile` | <span data-ttu-id="525f8-280">Optional</span><span class="sxs-lookup"><span data-stu-id="525f8-280">Optional</span></span> | <span data-ttu-id="525f8-281">Name oder GUID des Profils als Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="525f8-281">Profile's name or GUID as a string</span></span> | <span data-ttu-id="525f8-282">Profil, das auf der Grundlage seiner GUID oder seines Namens geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="525f8-282">Profile that will open based on its GUID or name.</span></span> |
| `splitMode` | <span data-ttu-id="525f8-283">Optional</span><span class="sxs-lookup"><span data-stu-id="525f8-283">Optional</span></span> | `"duplicate"` | <span data-ttu-id="525f8-284">Hiermit wird gesteuert, wie der Bereich unterteilt wird.</span><span class="sxs-lookup"><span data-stu-id="525f8-284">Controls how the pane splits.</span></span> <span data-ttu-id="525f8-285">Akzeptiert nur `"duplicate"`, wodurch das Profil des Fokusbereichs in einem neuen Bereich dupliziert wird.</span><span class="sxs-lookup"><span data-stu-id="525f8-285">Only accepts `"duplicate"`, which will duplicate the focused pane's profile into a new pane.</span></span> |

<br />

___

## <a name="clipboard-integration-commands"></a><span data-ttu-id="525f8-286">Befehle zur Integration der Zwischenablage</span><span class="sxs-lookup"><span data-stu-id="525f8-286">Clipboard integration commands</span></span>

### <a name="copy"></a><span data-ttu-id="525f8-287">Kopieren</span><span class="sxs-lookup"><span data-stu-id="525f8-287">Copy</span></span>

<span data-ttu-id="525f8-288">Hiermit wird der ausgewählte Terminalinhalt in die Zwischenablage kopiert.</span><span class="sxs-lookup"><span data-stu-id="525f8-288">This copies the selected terminal content to your clipboard.</span></span>

<span data-ttu-id="525f8-289">**Befehlsname:** `copy`</span><span class="sxs-lookup"><span data-stu-id="525f8-289">**Command name:** `copy`</span></span>

<span data-ttu-id="525f8-290">**Standardzuordnungen:**</span><span class="sxs-lookup"><span data-stu-id="525f8-290">**Default bindings:**</span></span>

```json
// In settings.json
{ "command": { "action": "copy", "singleLine": false }, "keys": "ctrl+c" },

// In defaults.json
{ "command": { "action": "copy", "singleLine": false }, "keys": "ctrl+shift+c" },
{ "command": { "action": "copy", "singleLine": false }, "keys": "ctrl+insert" }
```

#### <a name="clipboard-actions"></a><span data-ttu-id="525f8-291">Zwischenablageaktionen</span><span class="sxs-lookup"><span data-stu-id="525f8-291">Clipboard Actions</span></span>

| <span data-ttu-id="525f8-292">Name</span><span class="sxs-lookup"><span data-stu-id="525f8-292">Name</span></span> | <span data-ttu-id="525f8-293">Erfordernis</span><span class="sxs-lookup"><span data-stu-id="525f8-293">Necessity</span></span> | <span data-ttu-id="525f8-294">Akzeptierter Typ</span><span class="sxs-lookup"><span data-stu-id="525f8-294">Accepts</span></span> | <span data-ttu-id="525f8-295">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="525f8-295">Description</span></span> |
| ---- | --------- | ------- | ----------- |
| `singleLine` | <span data-ttu-id="525f8-296">Optional</span><span class="sxs-lookup"><span data-stu-id="525f8-296">Optional</span></span> | <span data-ttu-id="525f8-297">`true`, `false`</span><span class="sxs-lookup"><span data-stu-id="525f8-297">`true`, `false`</span></span> | <span data-ttu-id="525f8-298">Bei `true` wird der kopierte Inhalt als einzelne Zeile kopiert.</span><span class="sxs-lookup"><span data-stu-id="525f8-298">When `true`, the copied content will be copied as a single line.</span></span> <span data-ttu-id="525f8-299">Bei `false` werden Zeilenvorschübe aus dem ausgewählten Text beibehalten.</span><span class="sxs-lookup"><span data-stu-id="525f8-299">When `false`, newlines persist from the selected text.</span></span> |

### <a name="paste"></a><span data-ttu-id="525f8-300">Einfügen</span><span class="sxs-lookup"><span data-stu-id="525f8-300">Paste</span></span>

<span data-ttu-id="525f8-301">Hiermit wird der Inhalt eingefügt, der in die Zwischenablage kopiert wurde.</span><span class="sxs-lookup"><span data-stu-id="525f8-301">This inserts the content that was copied onto the clipboard.</span></span>

<span data-ttu-id="525f8-302">**Befehlsname:** `paste`</span><span class="sxs-lookup"><span data-stu-id="525f8-302">**Command name:** `paste`</span></span>

<span data-ttu-id="525f8-303">**Standardzuordnungen:**</span><span class="sxs-lookup"><span data-stu-id="525f8-303">**Default bindings:**</span></span>

```json
// In settings.json
{ "command": "paste", "keys": "ctrl+v" },

// In defaults.json
{ "command": "paste", "keys": "ctrl+shift+v" },
{ "command": "paste", "keys": "shift+insert" }
```

<br />

___

## <a name="scrollback-commands"></a><span data-ttu-id="525f8-304">Befehle zum Scrollen</span><span class="sxs-lookup"><span data-stu-id="525f8-304">Scrollback commands</span></span>

### <a name="scroll-up"></a><span data-ttu-id="525f8-305">Nach oben scrollen</span><span class="sxs-lookup"><span data-stu-id="525f8-305">Scroll up</span></span>

<span data-ttu-id="525f8-306">Hiermit wird auf dem Bildschirm nach oben gescrollt.</span><span class="sxs-lookup"><span data-stu-id="525f8-306">This scrolls the screen up.</span></span>

<span data-ttu-id="525f8-307">**Befehlsname:** `scrollUp`</span><span class="sxs-lookup"><span data-stu-id="525f8-307">**Command name:** `scrollUp`</span></span>

<span data-ttu-id="525f8-308">**Standardzuordnung:**</span><span class="sxs-lookup"><span data-stu-id="525f8-308">**Default binding:**</span></span>

```json
{ "command": "scrollUp", "keys": "ctrl+shift+up" }
```

### <a name="scroll-down"></a><span data-ttu-id="525f8-309">Nach unten scrollen</span><span class="sxs-lookup"><span data-stu-id="525f8-309">Scroll down</span></span>

<span data-ttu-id="525f8-310">Hiermit wird auf dem Bildschirm nach unten gescrollt.</span><span class="sxs-lookup"><span data-stu-id="525f8-310">This scrolls the screen down.</span></span>

<span data-ttu-id="525f8-311">**Befehlsname:** `scrollDown`</span><span class="sxs-lookup"><span data-stu-id="525f8-311">**Command name:** `scrollDown`</span></span>

<span data-ttu-id="525f8-312">**Standardzuordnung:**</span><span class="sxs-lookup"><span data-stu-id="525f8-312">**Default binding:**</span></span>

```json
{ "command": "scrollDown", "keys": "ctrl+shift+down" }
```

### <a name="scroll-up-a-whole-page"></a><span data-ttu-id="525f8-313">Ganze Seite nach oben scrollen</span><span class="sxs-lookup"><span data-stu-id="525f8-313">Scroll up a whole page</span></span>

<span data-ttu-id="525f8-314">Hiermit wird der Bildschirm um eine ganze Seite nach oben gescrollt, was der Höhe des Fensters entspricht.</span><span class="sxs-lookup"><span data-stu-id="525f8-314">This scrolls the screen up by a whole page, which is the height of the window.</span></span>

<span data-ttu-id="525f8-315">**Befehlsname:** `scrollUpPage`</span><span class="sxs-lookup"><span data-stu-id="525f8-315">**Command name:** `scrollUpPage`</span></span>

<span data-ttu-id="525f8-316">**Standardzuordnung:**</span><span class="sxs-lookup"><span data-stu-id="525f8-316">**Default binding:**</span></span>

```json
{ "command": "scrollUpPage", "keys": "ctrl+shift+pgup" }
```

### <a name="scroll-down-a-whole-page"></a><span data-ttu-id="525f8-317">Ganze Seite nach unten scrollen</span><span class="sxs-lookup"><span data-stu-id="525f8-317">Scroll down a whole page</span></span>

<span data-ttu-id="525f8-318">Hiermit wird der Bildschirm um eine ganze Seite nach unten gescrollt, was der Höhe des Fensters entspricht.</span><span class="sxs-lookup"><span data-stu-id="525f8-318">This scrolls the screen down by a whole page, which is the height of the window.</span></span>

<span data-ttu-id="525f8-319">**Befehlsname:** `scrollDownPage`</span><span class="sxs-lookup"><span data-stu-id="525f8-319">**Command name:** `scrollDownPage`</span></span>

<span data-ttu-id="525f8-320">**Standardzuordnung:**</span><span class="sxs-lookup"><span data-stu-id="525f8-320">**Default binding:**</span></span>

```json
{ "command": "scrollDownPage", "keys": "ctrl+shift+pgdn" }
```

<br />

___

## <a name="visual-adjustment-commands"></a><span data-ttu-id="525f8-321">Befehle zur visuellen Anpassung</span><span class="sxs-lookup"><span data-stu-id="525f8-321">Visual adjustment commands</span></span>

### <a name="adjust-font-size"></a><span data-ttu-id="525f8-322">Schriftgrad anpassen</span><span class="sxs-lookup"><span data-stu-id="525f8-322">Adjust font size</span></span>

<span data-ttu-id="525f8-323">Hiermit wird die Textgröße um eine angegebene Punktanzahl geändert.</span><span class="sxs-lookup"><span data-stu-id="525f8-323">This changes the text size by a specified point amount.</span></span>

<span data-ttu-id="525f8-324">**Befehlsname:** `adjustFontSize`</span><span class="sxs-lookup"><span data-stu-id="525f8-324">**Command name:** `adjustFontSize`</span></span>

<span data-ttu-id="525f8-325">**Standardzuordnungen:**</span><span class="sxs-lookup"><span data-stu-id="525f8-325">**Default bindings:**</span></span>

```json
{ "command": { "action": "adjustFontSize", "delta": 1 }, "keys": "ctrl+=" },
{ "command": { "action": "adjustFontSize", "delta": -1 }, "keys": "ctrl+-" }
```

#### <a name="actions"></a><span data-ttu-id="525f8-326">Aktionen</span><span class="sxs-lookup"><span data-stu-id="525f8-326">Actions</span></span>

| <span data-ttu-id="525f8-327">Name</span><span class="sxs-lookup"><span data-stu-id="525f8-327">Name</span></span> | <span data-ttu-id="525f8-328">Erfordernis</span><span class="sxs-lookup"><span data-stu-id="525f8-328">Necessity</span></span> | <span data-ttu-id="525f8-329">Akzeptierter Typ</span><span class="sxs-lookup"><span data-stu-id="525f8-329">Accepts</span></span> | <span data-ttu-id="525f8-330">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="525f8-330">Description</span></span> |
| ---- | --------- | ------- | ----------- |
| `delta` | <span data-ttu-id="525f8-331">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="525f8-331">Required</span></span> | <span data-ttu-id="525f8-332">Ganze Zahl</span><span class="sxs-lookup"><span data-stu-id="525f8-332">Integer</span></span> | <span data-ttu-id="525f8-333">Umfang der Größenänderung pro Befehlsaufruf.</span><span class="sxs-lookup"><span data-stu-id="525f8-333">Amount of size change per command invocation.</span></span> |

### <a name="reset-font-size"></a><span data-ttu-id="525f8-334">Schriftgrad zurücksetzen</span><span class="sxs-lookup"><span data-stu-id="525f8-334">Reset font size</span></span>

<span data-ttu-id="525f8-335">Hiermit wird die Textgröße auf den Standardwert zurückgesetzt.</span><span class="sxs-lookup"><span data-stu-id="525f8-335">This resets the text size to the default value.</span></span>

<span data-ttu-id="525f8-336">**Befehlsname:** `resetFontSize`</span><span class="sxs-lookup"><span data-stu-id="525f8-336">**Command name:** `resetFontSize`</span></span>

<span data-ttu-id="525f8-337">**Standardzuordnung:**</span><span class="sxs-lookup"><span data-stu-id="525f8-337">**Default binding:**</span></span>

```json
{ "command": "resetFontSize", "keys": "ctrl+0" }
```

<br />

___

## <a name="unbind-keys"></a><span data-ttu-id="525f8-338">Tastenzuordnung aufheben</span><span class="sxs-lookup"><span data-stu-id="525f8-338">Unbind keys</span></span>

<span data-ttu-id="525f8-339">Hiermit wird die Zuordnung der zu einem beliebigen Befehl zugewiesenen Tasten aufgehoben.</span><span class="sxs-lookup"><span data-stu-id="525f8-339">This unbinds the associated keys from any command.</span></span>

<span data-ttu-id="525f8-340">**Befehlsname:** `unbound`</span><span class="sxs-lookup"><span data-stu-id="525f8-340">**Command name:** `unbound`</span></span>
