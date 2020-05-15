---
title: 'Windows Terminal: Globale Einstellungen'
description: Erfahren Sie, wie Sie die globalen Einstellungen in Windows Terminals anpassen.
author: cinnamon-msft
ms.author: cinnamon
ms.date: 05/19/2020
ms.topic: how-to
ms.service: terminal
ms.localizationpriority: high
ms.openlocfilehash: 3cbe4b2b99f8115ff4eeaab5f525de393d7e5eb1
ms.sourcegitcommit: bb5b7fd7db4b81e0d44e060989dc16b6775c802a
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/15/2020
ms.locfileid: "83415955"
---
# <a name="global-settings-in-the-windows-terminal"></a><span data-ttu-id="74a72-103">Globale Einstellungen in Windows Terminal</span><span class="sxs-lookup"><span data-stu-id="74a72-103">Global settings in the Windows Terminal</span></span>

<span data-ttu-id="74a72-104">Die unten aufgeführten Eigenschaften betreffen das gesamte Terminalfenster, unabhängig von den Profileinstellungen.</span><span class="sxs-lookup"><span data-stu-id="74a72-104">The properties listed below affect the entire terminal window, regardless of the profile settings.</span></span> <span data-ttu-id="74a72-105">Diese sollten im Stammbereich Ihrer settings.json-Datei stehen.</span><span class="sxs-lookup"><span data-stu-id="74a72-105">These should be placed at the root of your settings.json file.</span></span>

## <a name="default-profile"></a><span data-ttu-id="74a72-106">Standardprofil</span><span class="sxs-lookup"><span data-stu-id="74a72-106">Default profile</span></span>

<span data-ttu-id="74a72-107">Legen Sie das Standardprofil fest, das geöffnet wird, indem Sie <kbd>STRG+UMSCHALT+T</kbd> eingeben, die `newTab` zugewiesene Tastenzuordnung drücken, `wt new-tab` ohne Angabe eines Profils ausführen oder auf das Symbol „+“ klicken.</span><span class="sxs-lookup"><span data-stu-id="74a72-107">Set the default profile that opens by typing <kbd>ctrl+shift+t</kbd>, typing the key binding assigned to `newTab`, running `wt new-tab` without specifying a profile, or clicking the '+' icon.</span></span>

<span data-ttu-id="74a72-108">**Eigenschaftenname:** `defaultProfile`</span><span class="sxs-lookup"><span data-stu-id="74a72-108">**Property name:** `defaultProfile`</span></span>

<span data-ttu-id="74a72-109">**Erfordernis:** Erforderlich</span><span class="sxs-lookup"><span data-stu-id="74a72-109">**Necessity:** Required</span></span>

<span data-ttu-id="74a72-110">**Akzeptiert:** GUID als Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="74a72-110">**Accepts:** GUID as a string</span></span>

<span data-ttu-id="74a72-111">**Standardwert:** PowerShell-GUID</span><span class="sxs-lookup"><span data-stu-id="74a72-111">**Default value:** PowerShell's GUID</span></span>

<br />

___

## <a name="disable-dynamic-profiles"></a><span data-ttu-id="74a72-112">Dynamische Profile deaktivieren</span><span class="sxs-lookup"><span data-stu-id="74a72-112">Disable dynamic profiles</span></span>

<span data-ttu-id="74a72-113">Hiermit wird festgelegt, welche dynamischen Profilgeneratoren deaktiviert werden, sodass sie ihre Profile beim Start nicht zur Liste der Profile hinzufügen können.</span><span class="sxs-lookup"><span data-stu-id="74a72-113">This sets which dynamic profile generators are disabled, preventing them from adding their profiles to the list of profiles on startup.</span></span> <span data-ttu-id="74a72-114">Informationen zu dynamischen Profilen finden Sie auf der Seite [Dynamische Profile](./../dynamic-profiles.md).</span><span class="sxs-lookup"><span data-stu-id="74a72-114">For information on dynamic profiles, visit the [Dynamic profiles page](./../dynamic-profiles.md).</span></span>

<span data-ttu-id="74a72-115">**Eigenschaftenname:** `disabledProfileSources`</span><span class="sxs-lookup"><span data-stu-id="74a72-115">**Property name:** `disabledProfileSources`</span></span>

<span data-ttu-id="74a72-116">**Erfordernis:** Optional</span><span class="sxs-lookup"><span data-stu-id="74a72-116">**Necessity:** Optional</span></span>

<span data-ttu-id="74a72-117">**Akzeptiert:** `"Windows.Terminal.Wsl"`, `"Windows.Terminal.Azure"` und/oder `"Windows.Terminal.PowershellCore"` innerhalb eines Arrays</span><span class="sxs-lookup"><span data-stu-id="74a72-117">**Accepts:** `"Windows.Terminal.Wsl"`, `"Windows.Terminal.Azure"`, and/or `"Windows.Terminal.PowershellCore"` inside an array</span></span>

<span data-ttu-id="74a72-118">**Standardwert:** `[]`</span><span class="sxs-lookup"><span data-stu-id="74a72-118">**Default value:** `[]`</span></span>

<br />

___

## <a name="darklight-theme"></a><span data-ttu-id="74a72-119">Dunkles/Helles Design</span><span class="sxs-lookup"><span data-stu-id="74a72-119">Dark/Light theme</span></span>

:::row:::
:::column span="":::
<span data-ttu-id="74a72-120">Hiermit wird das Design der Anwendung festgelegt.</span><span class="sxs-lookup"><span data-stu-id="74a72-120">This sets the theme of the application.</span></span> <span data-ttu-id="74a72-121">`"system"` verwendet dasselbe Design wie Windows.</span><span class="sxs-lookup"><span data-stu-id="74a72-121">`"system"` will use the same theme as Windows.</span></span>

<span data-ttu-id="74a72-122">**Eigenschaftenname:** `theme`</span><span class="sxs-lookup"><span data-stu-id="74a72-122">**Property name:** `theme`</span></span>

<span data-ttu-id="74a72-123">**Erfordernis:** Optional</span><span class="sxs-lookup"><span data-stu-id="74a72-123">**Necessity:** Optional</span></span>

<span data-ttu-id="74a72-124">**Akzeptiert:** `"system"`, `"dark"`, `"light"`</span><span class="sxs-lookup"><span data-stu-id="74a72-124">**Accepts:** `"system"`, `"dark"`, `"light"`</span></span>

<span data-ttu-id="74a72-125">**Standardwert:** `"system"`</span><span class="sxs-lookup"><span data-stu-id="74a72-125">**Default value:** `"system"`</span></span>

:::column-end:::
:::column span="":::
<span data-ttu-id="74a72-126">![Windows Terminal: Dunkles Design](./../images/requested-themes.gif)
_Konfiguration: [Powerline in PowerShell](./../custom-terminal-gallery/powerline-in-powershell.md)_</span><span class="sxs-lookup"><span data-stu-id="74a72-126">![Windows Terminal dark theme](./../images/requested-themes.gif)
_Configuration: [Powerline in PowerShell](./../custom-terminal-gallery/powerline-in-powershell.md)_</span></span>

:::column-end:::
:::row-end:::

<br />

___

## <a name="tab-settings"></a><span data-ttu-id="74a72-127">Registerkarteneinstellungen</span><span class="sxs-lookup"><span data-stu-id="74a72-127">Tab settings</span></span>

### <a name="always-show-tabs"></a><span data-ttu-id="74a72-128">Registerkarten immer anzeigen</span><span class="sxs-lookup"><span data-stu-id="74a72-128">Always show tabs</span></span>

:::row:::
:::column span="":::
<span data-ttu-id="74a72-129">Wenn diese Einstellung auf `true` festgelegt ist, werden Registerkarten immer angezeigt.</span><span class="sxs-lookup"><span data-stu-id="74a72-129">When this is set to `true`, tabs are always displayed.</span></span> <span data-ttu-id="74a72-130">Wenn sie auf `false` und `showTabsInTitlebar` auf `true` festgelegt ist, werden Registerkarten immer unterhalb der Titelleiste angezeigt.</span><span class="sxs-lookup"><span data-stu-id="74a72-130">When it's set to `false` and `showTabsInTitlebar` is set to `true`, tabs are always displayed underneath the title bar.</span></span> <span data-ttu-id="74a72-131">Wenn diese Einstellung auf `false` und `showTabsInTitlebar` auf `false` festgelegt ist, werden Registerkarten erst angezeigt, wenn mehr als eine Registerkarte vorhanden ist, indem Sie <kbd>STRG+UMSCHALT+T</kbd> oder die zu `newTab` zugewiesene Tastenzuordnung eingeben.</span><span class="sxs-lookup"><span data-stu-id="74a72-131">When this is set to `false` and `showTabsInTitlebar` is set to `false`, tabs only appear after more than one tab exists by typing <kbd>ctrl+shift+t</kbd> or by typing the key binding assigned to `newTab`.</span></span> <span data-ttu-id="74a72-132">Beachten Sie, dass das Ändern dieser Einstellung das Starten einer neuen Terminalinstanz erfordert.</span><span class="sxs-lookup"><span data-stu-id="74a72-132">Note that changing this setting will require starting a new terminal instance.</span></span>

<span data-ttu-id="74a72-133">**Eigenschaftenname:** `alwaysShowTabs`</span><span class="sxs-lookup"><span data-stu-id="74a72-133">**Property name:** `alwaysShowTabs`</span></span>

<span data-ttu-id="74a72-134">**Erfordernis:** Optional</span><span class="sxs-lookup"><span data-stu-id="74a72-134">**Necessity:** Optional</span></span>

<span data-ttu-id="74a72-135">**Akzeptiert:** `true`, `false`</span><span class="sxs-lookup"><span data-stu-id="74a72-135">**Accepts:** `true`, `false`</span></span>

<span data-ttu-id="74a72-136">**Standardwert:** `true`</span><span class="sxs-lookup"><span data-stu-id="74a72-136">**Default value:** `true`</span></span>

:::column-end:::
:::column span="":::
![Windows Terminal zeigt Registerkarten immer an](./../images/always-show-tabs.gif)

:::column-end:::
:::row-end:::

### <a name="tab-width-mode"></a><span data-ttu-id="74a72-138">Modus für Registerkartenbreite</span><span class="sxs-lookup"><span data-stu-id="74a72-138">Tab width mode</span></span>

:::row:::
:::column span="":::
<span data-ttu-id="74a72-139">Hiermit wird die Breite der Registerkarten festgelegt.</span><span class="sxs-lookup"><span data-stu-id="74a72-139">This sets the width of the tabs.</span></span> <span data-ttu-id="74a72-140">`"equal"` bewirkt, dass jede Registerkarte dieselbe Breite erhält.</span><span class="sxs-lookup"><span data-stu-id="74a72-140">`"equal"` makes each tab the same width.</span></span> <span data-ttu-id="74a72-141">`"titleLength"` passt die Größe der einzelnen Registerkarten auf die Länge des Titels an.</span><span class="sxs-lookup"><span data-stu-id="74a72-141">`"titleLength"` sizes each tab to the length of its title.</span></span>

<span data-ttu-id="74a72-142">**Eigenschaftenname:** `tabWidthMode`</span><span class="sxs-lookup"><span data-stu-id="74a72-142">**Property name:** `tabWidthMode`</span></span>

<span data-ttu-id="74a72-143">**Erfordernis:** Optional</span><span class="sxs-lookup"><span data-stu-id="74a72-143">**Necessity:** Optional</span></span>

<span data-ttu-id="74a72-144">**Akzeptiert:** `"equal"`, `"titleLength"`</span><span class="sxs-lookup"><span data-stu-id="74a72-144">**Accepts:** `"equal"`, `"titleLength"`</span></span>

<span data-ttu-id="74a72-145">**Standardwert:** `"equal"`</span><span class="sxs-lookup"><span data-stu-id="74a72-145">**Default value:** `"equal"`</span></span>

:::column-end:::
:::column span="":::
![Windows Terminal: Modus für Registerkartenbreite](./../images/tab-width-mode.gif)

:::column-end:::
:::row-end:::

### <a name="hide-close-all-tabs-popup"></a><span data-ttu-id="74a72-147">Popupfenster „Alle Registerkarten schließen“ ausblenden</span><span class="sxs-lookup"><span data-stu-id="74a72-147">Hide close all tabs popup</span></span>

:::row:::
:::column span="":::
<span data-ttu-id="74a72-148">Wenn diese Einstellung auf `true` festgelegt ist, _erfordert_ das Schließen eines Fensters mit mehreren geöffneten Registerkarten eine Bestätigung.</span><span class="sxs-lookup"><span data-stu-id="74a72-148">When this is set to `true`, closing a window with multiple tabs open _will_ require confirmation.</span></span> <span data-ttu-id="74a72-149">Wenn diese Einstellung auf `false` festgelegt ist, erfordert das Schließen eines Fensters mit mehreren geöffneten Registerkarten _keine_ Bestätigung.</span><span class="sxs-lookup"><span data-stu-id="74a72-149">When it's set to `false`, closing a window with multiple tabs open _will not_ require confirmation.</span></span>

<span data-ttu-id="74a72-150">**Eigenschaftenname:** `confirmCloseAllTabs`</span><span class="sxs-lookup"><span data-stu-id="74a72-150">**Property name:** `confirmCloseAllTabs`</span></span>

<span data-ttu-id="74a72-151">**Erfordernis:** Optional</span><span class="sxs-lookup"><span data-stu-id="74a72-151">**Necessity:** Optional</span></span>

<span data-ttu-id="74a72-152">**Akzeptiert:** `true`, `false`</span><span class="sxs-lookup"><span data-stu-id="74a72-152">**Accepts:** `true`, `false`</span></span>

<span data-ttu-id="74a72-153">**Standardwert:** `true`</span><span class="sxs-lookup"><span data-stu-id="74a72-153">**Default value:** `true`</span></span>

:::column-end:::
:::column span="":::
![Windows Terminal: Bestätigung zum Schließen aller Registerkarten](./../images/confirm-close-all-tabs.png)

:::column-end:::
:::row-end:::

<br />

___

## <a name="launch-settings"></a><span data-ttu-id="74a72-155">Starteinstellungen</span><span class="sxs-lookup"><span data-stu-id="74a72-155">Launch settings</span></span>

### <a name="launch-maximized"></a><span data-ttu-id="74a72-156">Maximiert starten</span><span class="sxs-lookup"><span data-stu-id="74a72-156">Launch maximized</span></span>

<span data-ttu-id="74a72-157">Hiermit wird definiert, ob das Terminal maximiert gestartet wird, um den gesamten Bildschirm oder ein Fenster auszufüllen.</span><span class="sxs-lookup"><span data-stu-id="74a72-157">This defines whether the terminal will launch as maximized to fill the entire screen or in a window.</span></span>

<span data-ttu-id="74a72-158">**Eigenschaftenname:** `launchMode`</span><span class="sxs-lookup"><span data-stu-id="74a72-158">**Property name:** `launchMode`</span></span>

<span data-ttu-id="74a72-159">**Erfordernis:** Optional</span><span class="sxs-lookup"><span data-stu-id="74a72-159">**Necessity:** Optional</span></span>

<span data-ttu-id="74a72-160">**Akzeptiert:** `"default"`, `"maximized"`</span><span class="sxs-lookup"><span data-stu-id="74a72-160">**Accepts:** `"default"`, `"maximized"`</span></span>

<span data-ttu-id="74a72-161">**Standardwert:** `"default"`</span><span class="sxs-lookup"><span data-stu-id="74a72-161">**Default value:** `"default"`</span></span>

### <a name="launch-position"></a><span data-ttu-id="74a72-162">Startposition</span><span class="sxs-lookup"><span data-stu-id="74a72-162">Launch position</span></span>

<span data-ttu-id="74a72-163">Hiermit wird die Pixelposition der oberen linken Ecke des Fensters beim ersten Laden festgelegt.</span><span class="sxs-lookup"><span data-stu-id="74a72-163">This sets the pixel position of the top left corner of the window upon first load.</span></span> <span data-ttu-id="74a72-164">Bei einem System mit mehreren Bildschirmen sind diese Koordinaten relativ zur oberen linken Ecke des primären Bildschirms.</span><span class="sxs-lookup"><span data-stu-id="74a72-164">On a system with multiple displays, these coordinates are relative to the top left of the primary display.</span></span> <span data-ttu-id="74a72-165">Wenn keine X-oder Y-Koordinate bereitgestellt wird, verwendet das Terminal die Standardeinstellung des Systems für diesen Wert.</span><span class="sxs-lookup"><span data-stu-id="74a72-165">If an X or Y coordinate is not provided, the terminal will use the system default for that value.</span></span> <span data-ttu-id="74a72-166">Wenn `launchMode` auf `"maximized"` festgelegt ist, wird das Fenster auf dem Monitor maximiert, der durch diese Koordinaten angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="74a72-166">If `launchMode` is set to `"maximized"`, the window will be maximized on the monitor specified by those coordinates.</span></span>

<span data-ttu-id="74a72-167">**Eigenschaftenname:** `initialPosition`</span><span class="sxs-lookup"><span data-stu-id="74a72-167">**Property name:** `initialPosition`</span></span>

<span data-ttu-id="74a72-168">**Erfordernis:** Optional</span><span class="sxs-lookup"><span data-stu-id="74a72-168">**Necessity:** Optional</span></span>

<span data-ttu-id="74a72-169">**Akzeptiert:** Koordinaten als Zeichenfolge in den folgenden Formaten: `","`, `"#,#"`, `"#,"`, `",#"`</span><span class="sxs-lookup"><span data-stu-id="74a72-169">**Accepts:** Coordinates as a string in the following formats: `","`, `"#,#"`, `"#,"`, `",#"`</span></span>

<span data-ttu-id="74a72-170">**Standardwert:** `","`</span><span class="sxs-lookup"><span data-stu-id="74a72-170">**Default value:** `","`</span></span>

### <a name="columns-on-first-launch"></a><span data-ttu-id="74a72-171">Spalten beim ersten Start</span><span class="sxs-lookup"><span data-stu-id="74a72-171">Columns on first launch</span></span>

<span data-ttu-id="74a72-172">Dies ist die Anzahl der Zeichenspalten, die beim ersten Laden im Fenster angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="74a72-172">This is the number of character columns displayed in the window upon first load.</span></span> <span data-ttu-id="74a72-173">Wenn `launchMode` auf `"maximized"` festgelegt ist, wird diese Eigenschaft ignoriert.</span><span class="sxs-lookup"><span data-stu-id="74a72-173">If `launchMode` is set to `"maximized"`, this property is ignored.</span></span>

<span data-ttu-id="74a72-174">**Eigenschaftenname:** `initialCols`</span><span class="sxs-lookup"><span data-stu-id="74a72-174">**Property name:** `initialCols`</span></span>

<span data-ttu-id="74a72-175">**Erfordernis:** Optional</span><span class="sxs-lookup"><span data-stu-id="74a72-175">**Necessity:** Optional</span></span>

<span data-ttu-id="74a72-176">**Akzeptiert:** Ganze Zahl</span><span class="sxs-lookup"><span data-stu-id="74a72-176">**Accepts:** Integer</span></span>

<span data-ttu-id="74a72-177">**Standardwert:** `120`</span><span class="sxs-lookup"><span data-stu-id="74a72-177">**Default value:** `120`</span></span>

### <a name="rows-on-first-launch"></a><span data-ttu-id="74a72-178">Zeilen beim ersten Start</span><span class="sxs-lookup"><span data-stu-id="74a72-178">Rows on first launch</span></span>

<span data-ttu-id="74a72-179">Dies ist die Anzahl der Zeilen, die beim ersten Laden im Fenster angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="74a72-179">This is the number of rows displayed in the window upon first load.</span></span> <span data-ttu-id="74a72-180">Wenn `launchMode` auf `"maximized"` festgelegt ist, wird diese Eigenschaft ignoriert.</span><span class="sxs-lookup"><span data-stu-id="74a72-180">If `launchMode` is set to `"maximized"`, this property is ignored.</span></span>

<span data-ttu-id="74a72-181">**Eigenschaftenname:** `initialRows`</span><span class="sxs-lookup"><span data-stu-id="74a72-181">**Property name:** `initialRows`</span></span>

<span data-ttu-id="74a72-182">**Erfordernis:** Optional</span><span class="sxs-lookup"><span data-stu-id="74a72-182">**Necessity:** Optional</span></span>

<span data-ttu-id="74a72-183">**Akzeptiert:** Ganze Zahl</span><span class="sxs-lookup"><span data-stu-id="74a72-183">**Accepts:** Integer</span></span>

<span data-ttu-id="74a72-184">**Standardwert:** `30`</span><span class="sxs-lookup"><span data-stu-id="74a72-184">**Default value:** `30`</span></span>

<br />

___

## <a name="title-bar-settings"></a><span data-ttu-id="74a72-185">Titelleisteneinstellungen</span><span class="sxs-lookup"><span data-stu-id="74a72-185">Title bar settings</span></span>

### <a name="showhide-the-title-bar"></a><span data-ttu-id="74a72-186">Titelleiste anzeigen/ausblenden</span><span class="sxs-lookup"><span data-stu-id="74a72-186">Show/Hide the title bar</span></span>

:::row:::
:::column span="":::
<span data-ttu-id="74a72-187">Wenn diese Einstellung auf `true` festgelegt ist, werden die Registerkarten in die Titelleiste verschoben, und die Titelleiste wird ausgeblendet.</span><span class="sxs-lookup"><span data-stu-id="74a72-187">When this is set to `true`, the tabs are moved into the title bar and the title bar disappears.</span></span> <span data-ttu-id="74a72-188">Wenn sie auf `false` festgelegt ist, befindet sich die Titelleiste oberhalb der Registerkarten.</span><span class="sxs-lookup"><span data-stu-id="74a72-188">When it's set to `false`, the title bar sits above the tabs.</span></span> <span data-ttu-id="74a72-189">Beachten Sie, dass das Ändern dieser Einstellung das Starten einer neuen Terminalinstanz erfordert.</span><span class="sxs-lookup"><span data-stu-id="74a72-189">Note that changing this setting will require starting a new terminal instance.</span></span>

<span data-ttu-id="74a72-190">**Eigenschaftenname:** `showTabsInTitlebar`</span><span class="sxs-lookup"><span data-stu-id="74a72-190">**Property name:** `showTabsInTitlebar`</span></span>

<span data-ttu-id="74a72-191">**Erfordernis:** Optional</span><span class="sxs-lookup"><span data-stu-id="74a72-191">**Necessity:** Optional</span></span>

<span data-ttu-id="74a72-192">**Akzeptiert:** `true`, `false`</span><span class="sxs-lookup"><span data-stu-id="74a72-192">**Accepts:** `true`, `false`</span></span>

<span data-ttu-id="74a72-193">**Standardwert:** `true`</span><span class="sxs-lookup"><span data-stu-id="74a72-193">**Default value:** `true`</span></span>

:::column-end:::
:::column span="":::
![Windows Terminal zeigt Registerkarten in der Titelleiste an](./../images/show-tabs-in-title-bar.gif)

:::column-end:::
:::row-end:::

### <a name="set-the-text-in-the-title-bar"></a><span data-ttu-id="74a72-195">Text in der Titelleiste festlegen</span><span class="sxs-lookup"><span data-stu-id="74a72-195">Set the text in the title bar</span></span>

<span data-ttu-id="74a72-196">Wenn diese Einstellung auf `true` festgelegt ist, wird in der Titelleiste der Titel der ausgewählten Registerkarte angezeigt. Wenn sie auf `false` festgelegt ist, wird in der Titelleiste „Windows Terminal“ angezeigt.</span><span class="sxs-lookup"><span data-stu-id="74a72-196">When this is set to `true`, the title bar displays the title of the selected tab. When it's set to `false`, title bar displays "Windows Terminal".</span></span> <span data-ttu-id="74a72-197">Beachten Sie, dass das Ändern dieser Einstellung das Starten einer neuen Terminalinstanz erfordert.</span><span class="sxs-lookup"><span data-stu-id="74a72-197">Note that changing this setting will require starting a new terminal instance.</span></span>

<span data-ttu-id="74a72-198">**Eigenschaftenname:** `showTerminalTitleInTitlebar`</span><span class="sxs-lookup"><span data-stu-id="74a72-198">**Property name:** `showTerminalTitleInTitlebar`</span></span>

<span data-ttu-id="74a72-199">**Erfordernis:** Optional</span><span class="sxs-lookup"><span data-stu-id="74a72-199">**Necessity:** Optional</span></span>

<span data-ttu-id="74a72-200">**Akzeptiert:** `true`, `false`</span><span class="sxs-lookup"><span data-stu-id="74a72-200">**Accepts:** `true`, `false`</span></span>

<span data-ttu-id="74a72-201">**Standardwert:** `true`</span><span class="sxs-lookup"><span data-stu-id="74a72-201">**Default value:** `true`</span></span>

<br />

___

## <a name="selection-settings"></a><span data-ttu-id="74a72-202">Auswahleinstellungen</span><span class="sxs-lookup"><span data-stu-id="74a72-202">Selection settings</span></span>

### <a name="copy-after-selection-is-made"></a><span data-ttu-id="74a72-203">Nach Auswahl kopieren</span><span class="sxs-lookup"><span data-stu-id="74a72-203">Copy after selection is made</span></span>

<span data-ttu-id="74a72-204">Wenn diese Einstellung auf `true` festgelegt ist, wird eine Auswahl sofort bei der Erstellung in die Zwischenablage kopiert.</span><span class="sxs-lookup"><span data-stu-id="74a72-204">When this is set to `true`, a selection is immediately copied to your clipboard upon creation.</span></span> <span data-ttu-id="74a72-205">Beim Klicken mit der rechten Maustaste erfolgt in dieser Fall immer ein Einfügevorgang.</span><span class="sxs-lookup"><span data-stu-id="74a72-205">The right-click on your mouse will always paste in this case.</span></span> <span data-ttu-id="74a72-206">Wenn sie auf `false` festgelegt ist, bleibt die Auswahl bestehen und wartet auf weitere Maßnahmen.</span><span class="sxs-lookup"><span data-stu-id="74a72-206">When it's set to `false`, the selection persists and awaits further action.</span></span> <span data-ttu-id="74a72-207">Wenn Sie mit der rechten Maustaste klicken, wird die Auswahl kopiert.</span><span class="sxs-lookup"><span data-stu-id="74a72-207">Using your mouse to right-click will copy the selection.</span></span>

<span data-ttu-id="74a72-208">**Eigenschaftenname:** `copyOnSelect`</span><span class="sxs-lookup"><span data-stu-id="74a72-208">**Property name:** `copyOnSelect`</span></span>

<span data-ttu-id="74a72-209">**Erfordernis:** Optional</span><span class="sxs-lookup"><span data-stu-id="74a72-209">**Necessity:** Optional</span></span>

<span data-ttu-id="74a72-210">**Akzeptiert:** `true`, `false`</span><span class="sxs-lookup"><span data-stu-id="74a72-210">**Accepts:** `true`, `false`</span></span>

<span data-ttu-id="74a72-211">**Standardwert:** `false`</span><span class="sxs-lookup"><span data-stu-id="74a72-211">**Default value:** `false`</span></span>

### <a name="copy-formatting"></a><span data-ttu-id="74a72-212">Formatierung kopieren</span><span class="sxs-lookup"><span data-stu-id="74a72-212">Copy formatting</span></span>

<span data-ttu-id="74a72-213">Wenn diese Einstellung auf `true` festgelegt ist, werden Farb- und Schriftformatierung des ausgewählten Textes ebenfalls in die Zwischenablage kopiert.</span><span class="sxs-lookup"><span data-stu-id="74a72-213">When this is set to `true`, the color and font formatting of selected text is also copied to your clipboard.</span></span> <span data-ttu-id="74a72-214">Wenn sie auf `false` festgelegt ist, wird Nur-Text in die Zwischenablage kopiert.</span><span class="sxs-lookup"><span data-stu-id="74a72-214">When it's set to `false`, only plain text is copied to your clipboard.</span></span>

<span data-ttu-id="74a72-215">**Eigenschaftenname:** `copyFormatting`</span><span class="sxs-lookup"><span data-stu-id="74a72-215">**Property name:** `copyFormatting`</span></span>

<span data-ttu-id="74a72-216">**Erfordernis:** Optional</span><span class="sxs-lookup"><span data-stu-id="74a72-216">**Necessity:** Optional</span></span>

<span data-ttu-id="74a72-217">**Akzeptiert:** `true`, `false`</span><span class="sxs-lookup"><span data-stu-id="74a72-217">**Accepts:** `true`, `false`</span></span>

<span data-ttu-id="74a72-218">**Standardwert:** `false`</span><span class="sxs-lookup"><span data-stu-id="74a72-218">**Default value:** `false`</span></span>

### <a name="word-delimiters"></a><span data-ttu-id="74a72-219">Worttrennzeichen</span><span class="sxs-lookup"><span data-stu-id="74a72-219">Word delimiters</span></span>

<span data-ttu-id="74a72-220">Hiermit werden die in einer durch Doppelklick ausgelösten Auswahl verwendeten Worttrennzeichen festgelegt.</span><span class="sxs-lookup"><span data-stu-id="74a72-220">This determines the word delimiters used in a double-click selection.</span></span> <span data-ttu-id="74a72-221">Worttrennzeichen sind Zeichen, die angeben, wo die Grenze zwischen zwei Wörtern liegt.</span><span class="sxs-lookup"><span data-stu-id="74a72-221">Word delimiters are characters that specify where the boundary is between two words.</span></span> <span data-ttu-id="74a72-222">Die häufigsten Beispiele sind Leerzeichen, Semikolons, Kommas und Punkte.</span><span class="sxs-lookup"><span data-stu-id="74a72-222">The most common examples are spaces, semicolons, commas, and periods.</span></span>

<span data-ttu-id="74a72-223">**Eigenschaftenname:** `wordDelimiters`</span><span class="sxs-lookup"><span data-stu-id="74a72-223">**Property name:** `wordDelimiters`</span></span>

<span data-ttu-id="74a72-224">**Erfordernis:** Optional</span><span class="sxs-lookup"><span data-stu-id="74a72-224">**Necessity:** Optional</span></span>

<span data-ttu-id="74a72-225">**Akzeptiert:** Zeichen als Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="74a72-225">**Accepts:** Characters as a string</span></span>

<span data-ttu-id="74a72-226">**Standardwert:** <code>&nbsp;&#x2f;&#x5c;&#x28;&#x29;&#x22;&#x27;&#x2d;&#x3a;&#x2c;&#x2e;&#x3b;&#x3c;&#x3e;&#x7e;&#x21;&#x40;&#x23;&#x24;&#x25;&#x5e;&#x26;&#x2a;&#x7c;&#x2b;&#x3d;&#x5b;&#x5d;&#x7b;&#x7d;&#x7e;&#x3f;│</code></span><span class="sxs-lookup"><span data-stu-id="74a72-226">**Default value:** <code>&nbsp;&#x2f;&#x5c;&#x28;&#x29;&#x22;&#x27;&#x2d;&#x3a;&#x2c;&#x2e;&#x3b;&#x3c;&#x3e;&#x7e;&#x21;&#x40;&#x23;&#x24;&#x25;&#x5e;&#x26;&#x2a;&#x7c;&#x2b;&#x3d;&#x5b;&#x5d;&#x7b;&#x7d;&#x7e;&#x3f;│</code></span></span><br><span data-ttu-id="74a72-227">_(`│` ist `U+2502 BOX DRAWINGS LIGHT VERTICAL`)_</span><span class="sxs-lookup"><span data-stu-id="74a72-227">_(`│` is `U+2502 BOX DRAWINGS LIGHT VERTICAL`)_</span></span>

<br />

___

## <a name="scroll-speed"></a><span data-ttu-id="74a72-228">Scrollgeschwindigkeit</span><span class="sxs-lookup"><span data-stu-id="74a72-228">Scroll speed</span></span>

<span data-ttu-id="74a72-229">Dies ist die Anzahl der Zeilen, die gleichzeitig mit dem Mausrad gescrollt werden können.</span><span class="sxs-lookup"><span data-stu-id="74a72-229">This is the number of rows to scroll at a time with the mouse wheel.</span></span> <span data-ttu-id="74a72-230">Dadurch wird die Systemeinstellung außer Kraft gesetzt, wenn der Wert nicht null (0) oder `"system"` ist.</span><span class="sxs-lookup"><span data-stu-id="74a72-230">This will override the system setting if the value is not zero or `"system"`.</span></span>

<span data-ttu-id="74a72-231">**Eigenschaftenname:** `rowsToScroll`</span><span class="sxs-lookup"><span data-stu-id="74a72-231">**Property name:** `rowsToScroll`</span></span>

<span data-ttu-id="74a72-232">**Erfordernis:** Optional</span><span class="sxs-lookup"><span data-stu-id="74a72-232">**Necessity:** Optional</span></span>

<span data-ttu-id="74a72-233">**Akzeptiert:** Ganze Zahl</span><span class="sxs-lookup"><span data-stu-id="74a72-233">**Accepts:** Integer</span></span>

<span data-ttu-id="74a72-234">**Standardwert:** `"system"`</span><span class="sxs-lookup"><span data-stu-id="74a72-234">**Default value:** `"system"`</span></span>

<br />

___

## <a name="window-resize-behavior"></a><span data-ttu-id="74a72-235">Verhalten bei der Größenänderung von Fenstern</span><span class="sxs-lookup"><span data-stu-id="74a72-235">Window resize behavior</span></span>

:::row:::
:::column span="":::
<span data-ttu-id="74a72-236">Wenn diese Einstellung auf `true` festgelegt ist, wird das Fenster bei einer Größenänderung an der nächstgelegenen Zeichengrenze ausgerichtet.</span><span class="sxs-lookup"><span data-stu-id="74a72-236">When this is set to `true`, the window will snap to the nearest character boundary on resize.</span></span> <span data-ttu-id="74a72-237">Wenn sie auf `false` festgelegt ist, wird die Größe des Fensters „reibungslos“ angepasst.</span><span class="sxs-lookup"><span data-stu-id="74a72-237">When it's set to `false`, the window will resize "smoothly".</span></span>

<span data-ttu-id="74a72-238">**Eigenschaftenname:** `snapToGridOnResize`</span><span class="sxs-lookup"><span data-stu-id="74a72-238">**Property name:** `snapToGridOnResize`</span></span>

<span data-ttu-id="74a72-239">**Erfordernis:** Optional</span><span class="sxs-lookup"><span data-stu-id="74a72-239">**Necessity:** Optional</span></span>

<span data-ttu-id="74a72-240">**Akzeptiert:** `true`, `false`</span><span class="sxs-lookup"><span data-stu-id="74a72-240">**Accepts:** `true`, `false`</span></span>

<span data-ttu-id="74a72-241">**Standardwert:** `true`</span><span class="sxs-lookup"><span data-stu-id="74a72-241">**Default value:** `true`</span></span>

:::column-end:::
:::column span="":::
![Windows Terminal: „Am Raster ausrichten“ beim Ändern der Größe](./../images/snap-to-grid-on-resize.gif)

:::column-end:::
:::row-end:::
