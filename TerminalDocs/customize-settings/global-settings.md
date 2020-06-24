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
# <a name="global-settings-in-windows-terminal"></a><span data-ttu-id="dd8df-103">Globale Einstellungen in Windows Terminal</span><span class="sxs-lookup"><span data-stu-id="dd8df-103">Global settings in Windows Terminal</span></span>

<span data-ttu-id="dd8df-104">Die unten aufgeführten Eigenschaften betreffen das gesamte Terminalfenster, unabhängig von den Profileinstellungen.</span><span class="sxs-lookup"><span data-stu-id="dd8df-104">The properties listed below affect the entire terminal window, regardless of the profile settings.</span></span> <span data-ttu-id="dd8df-105">Diese sollten im Stammbereich Ihrer settings.json-Datei stehen.</span><span class="sxs-lookup"><span data-stu-id="dd8df-105">These should be placed at the root of your settings.json file.</span></span>

## <a name="default-profile"></a><span data-ttu-id="dd8df-106">Standardprofil</span><span class="sxs-lookup"><span data-stu-id="dd8df-106">Default profile</span></span>

<span data-ttu-id="dd8df-107">Legen Sie das Standardprofil fest, das geöffnet wird, indem Sie <kbd>STRG+UMSCHALT+T</kbd> eingeben, die `newTab` zugewiesene Tastenzuordnung drücken, `wt new-tab` ohne Angabe eines Profils ausführen oder auf das Symbol „+“ klicken.</span><span class="sxs-lookup"><span data-stu-id="dd8df-107">Set the default profile that opens by typing <kbd>ctrl+shift+t</kbd>, typing the key binding assigned to `newTab`, running `wt new-tab` without specifying a profile, or clicking the '+' icon.</span></span>

<span data-ttu-id="dd8df-108">**Eigenschaftenname:** `defaultProfile`</span><span class="sxs-lookup"><span data-stu-id="dd8df-108">**Property name:** `defaultProfile`</span></span>

<span data-ttu-id="dd8df-109">**Erfordernis:** Erforderlich</span><span class="sxs-lookup"><span data-stu-id="dd8df-109">**Necessity:** Required</span></span>

<span data-ttu-id="dd8df-110">**Akzeptiert:** GUID- oder Profilname als Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="dd8df-110">**Accepts:** GUID or profile name as a string</span></span>

<span data-ttu-id="dd8df-111">**Standardwert:** PowerShell-GUID</span><span class="sxs-lookup"><span data-stu-id="dd8df-111">**Default value:** PowerShell's GUID</span></span>

> [!IMPORTANT]
> <span data-ttu-id="dd8df-112">Die Verwendung des Profilnamens für `defaultProfile` ist nur in der [Windows Terminal-Vorschau](https://aka.ms/terminal-preview/) möglich.</span><span class="sxs-lookup"><span data-stu-id="dd8df-112">Using the profile name for `defaultProfile` is only available in [Windows Terminal Preview](https://aka.ms/terminal-preview/).</span></span>

<br />

___

## <a name="disable-dynamic-profiles"></a><span data-ttu-id="dd8df-113">Dynamische Profile deaktivieren</span><span class="sxs-lookup"><span data-stu-id="dd8df-113">Disable dynamic profiles</span></span>

<span data-ttu-id="dd8df-114">Hiermit wird festgelegt, welche dynamischen Profilgeneratoren deaktiviert werden, sodass sie ihre Profile beim Start nicht zur Liste der Profile hinzufügen können.</span><span class="sxs-lookup"><span data-stu-id="dd8df-114">This sets which dynamic profile generators are disabled, preventing them from adding their profiles to the list of profiles on startup.</span></span> <span data-ttu-id="dd8df-115">Informationen zu dynamischen Profilen finden Sie auf der Seite [Dynamische Profile](./../dynamic-profiles.md).</span><span class="sxs-lookup"><span data-stu-id="dd8df-115">For information on dynamic profiles, visit the [Dynamic profiles page](./../dynamic-profiles.md).</span></span>

<span data-ttu-id="dd8df-116">**Eigenschaftenname:** `disabledProfileSources`</span><span class="sxs-lookup"><span data-stu-id="dd8df-116">**Property name:** `disabledProfileSources`</span></span>

<span data-ttu-id="dd8df-117">**Erfordernis:** Optional</span><span class="sxs-lookup"><span data-stu-id="dd8df-117">**Necessity:** Optional</span></span>

<span data-ttu-id="dd8df-118">**Akzeptiert:** `"Windows.Terminal.Wsl"`, `"Windows.Terminal.Azure"` und/oder `"Windows.Terminal.PowershellCore"` innerhalb eines Arrays</span><span class="sxs-lookup"><span data-stu-id="dd8df-118">**Accepts:** `"Windows.Terminal.Wsl"`, `"Windows.Terminal.Azure"`, and/or `"Windows.Terminal.PowershellCore"` inside an array</span></span>

<span data-ttu-id="dd8df-119">**Standardwert:** `[]`</span><span class="sxs-lookup"><span data-stu-id="dd8df-119">**Default value:** `[]`</span></span>

<br />

___

## <a name="darklight-theme"></a><span data-ttu-id="dd8df-120">Dunkles/Helles Design</span><span class="sxs-lookup"><span data-stu-id="dd8df-120">Dark/Light theme</span></span>

:::row:::
:::column span="":::
<span data-ttu-id="dd8df-121">Hiermit wird das Design der Anwendung festgelegt.</span><span class="sxs-lookup"><span data-stu-id="dd8df-121">This sets the theme of the application.</span></span> <span data-ttu-id="dd8df-122">`"system"` verwendet dasselbe Design wie Windows.</span><span class="sxs-lookup"><span data-stu-id="dd8df-122">`"system"` will use the same theme as Windows.</span></span>

<span data-ttu-id="dd8df-123">**Eigenschaftenname:** `theme`</span><span class="sxs-lookup"><span data-stu-id="dd8df-123">**Property name:** `theme`</span></span>

<span data-ttu-id="dd8df-124">**Erfordernis:** Optional</span><span class="sxs-lookup"><span data-stu-id="dd8df-124">**Necessity:** Optional</span></span>

<span data-ttu-id="dd8df-125">**Akzeptiert:** `"system"`, `"dark"`, `"light"`</span><span class="sxs-lookup"><span data-stu-id="dd8df-125">**Accepts:** `"system"`, `"dark"`, `"light"`</span></span>

<span data-ttu-id="dd8df-126">**Standardwert:** `"system"`</span><span class="sxs-lookup"><span data-stu-id="dd8df-126">**Default value:** `"system"`</span></span>

:::column-end:::
:::column span="":::
<span data-ttu-id="dd8df-127">![Windows Terminal: Dunkles Design](./../images/requested-themes.gif)
_Konfiguration: [Powerline in PowerShell](./../custom-terminal-gallery/powerline-in-powershell.md)_</span><span class="sxs-lookup"><span data-stu-id="dd8df-127">![Windows Terminal dark theme](./../images/requested-themes.gif)
_Configuration: [Powerline in PowerShell](./../custom-terminal-gallery/powerline-in-powershell.md)_</span></span>

:::column-end:::
:::row-end:::

<br />

___

## <a name="tab-settings"></a><span data-ttu-id="dd8df-128">Registerkarteneinstellungen</span><span class="sxs-lookup"><span data-stu-id="dd8df-128">Tab settings</span></span>

### <a name="always-show-tabs"></a><span data-ttu-id="dd8df-129">Registerkarten immer anzeigen</span><span class="sxs-lookup"><span data-stu-id="dd8df-129">Always show tabs</span></span>

:::row:::
:::column span="":::
<span data-ttu-id="dd8df-130">Wenn diese Einstellung auf `true` festgelegt ist, werden Registerkarten immer angezeigt.</span><span class="sxs-lookup"><span data-stu-id="dd8df-130">When this is set to `true`, tabs are always displayed.</span></span> <span data-ttu-id="dd8df-131">Wenn sie auf `false` und `showTabsInTitlebar` auf `true` festgelegt ist, werden Registerkarten immer unterhalb der Titelleiste angezeigt.</span><span class="sxs-lookup"><span data-stu-id="dd8df-131">When it's set to `false` and `showTabsInTitlebar` is set to `true`, tabs are always displayed underneath the title bar.</span></span> <span data-ttu-id="dd8df-132">Wenn diese Einstellung auf `false` und `showTabsInTitlebar` auf `false` festgelegt ist, werden Registerkarten erst angezeigt, wenn mehr als eine Registerkarte vorhanden ist, indem Sie <kbd>STRG+UMSCHALT+T</kbd> oder die zu `newTab` zugewiesene Tastenzuordnung eingeben.</span><span class="sxs-lookup"><span data-stu-id="dd8df-132">When this is set to `false` and `showTabsInTitlebar` is set to `false`, tabs only appear after more than one tab exists by typing <kbd>ctrl+shift+t</kbd> or by typing the key binding assigned to `newTab`.</span></span> <span data-ttu-id="dd8df-133">Beachten Sie, dass das Ändern dieser Einstellung das Starten einer neuen Terminalinstanz erfordert.</span><span class="sxs-lookup"><span data-stu-id="dd8df-133">Note that changing this setting will require starting a new terminal instance.</span></span>

<span data-ttu-id="dd8df-134">**Eigenschaftenname:** `alwaysShowTabs`</span><span class="sxs-lookup"><span data-stu-id="dd8df-134">**Property name:** `alwaysShowTabs`</span></span>

<span data-ttu-id="dd8df-135">**Erfordernis:** Optional</span><span class="sxs-lookup"><span data-stu-id="dd8df-135">**Necessity:** Optional</span></span>

<span data-ttu-id="dd8df-136">**Akzeptiert:** `true`, `false`</span><span class="sxs-lookup"><span data-stu-id="dd8df-136">**Accepts:** `true`, `false`</span></span>

<span data-ttu-id="dd8df-137">**Standardwert:** `true`</span><span class="sxs-lookup"><span data-stu-id="dd8df-137">**Default value:** `true`</span></span>

:::column-end:::
:::column span="":::
![Windows Terminal zeigt Registerkarten immer an](./../images/always-show-tabs.gif)

:::column-end:::
:::row-end:::

### <a name="tab-width-mode"></a><span data-ttu-id="dd8df-139">Modus für Registerkartenbreite</span><span class="sxs-lookup"><span data-stu-id="dd8df-139">Tab width mode</span></span>

:::row:::
:::column span="":::
<span data-ttu-id="dd8df-140">Hiermit wird die Breite der Registerkarten festgelegt.</span><span class="sxs-lookup"><span data-stu-id="dd8df-140">This sets the width of the tabs.</span></span> <span data-ttu-id="dd8df-141">`"equal"` bewirkt, dass jede Registerkarte dieselbe Breite erhält.</span><span class="sxs-lookup"><span data-stu-id="dd8df-141">`"equal"` makes each tab the same width.</span></span> <span data-ttu-id="dd8df-142">`"titleLength"` passt die Größe der einzelnen Registerkarten auf die Länge des Titels an.</span><span class="sxs-lookup"><span data-stu-id="dd8df-142">`"titleLength"` sizes each tab to the length of its title.</span></span> <span data-ttu-id="dd8df-143">`"compact"` verkleinert jede inaktive Registerkarte auf die Breite des Symbols, wodurch für die aktive Registerkarte mehr Platz zum Anzeigen des vollständigen Titels verbleibt.</span><span class="sxs-lookup"><span data-stu-id="dd8df-143">`"compact"` will shrink every inactive tab to the width of the icon, leaving the active tab more space to display its full title.</span></span>

<span data-ttu-id="dd8df-144">**Eigenschaftenname:** `tabWidthMode`</span><span class="sxs-lookup"><span data-stu-id="dd8df-144">**Property name:** `tabWidthMode`</span></span>

<span data-ttu-id="dd8df-145">**Erfordernis:** Optional</span><span class="sxs-lookup"><span data-stu-id="dd8df-145">**Necessity:** Optional</span></span>

<span data-ttu-id="dd8df-146">**Akzeptiert:** `"equal"`, `"titleLength"`, `"compact"`</span><span class="sxs-lookup"><span data-stu-id="dd8df-146">**Accepts:** `"equal"`, `"titleLength"`, `"compact"`</span></span>

<span data-ttu-id="dd8df-147">**Standardwert:** `"equal"`</span><span class="sxs-lookup"><span data-stu-id="dd8df-147">**Default value:** `"equal"`</span></span>

:::column-end:::
:::column span="":::
![Windows Terminal: Modus für Registerkartenbreite](./../images/tab-width-mode.gif)

:::column-end:::
:::row-end:::

> [!IMPORTANT]
> <span data-ttu-id="dd8df-149">Die `"compact"`-Einstellung steht nur in der [Windows Terminal-Vorschau](https://aka.ms/terminal-preview/) zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="dd8df-149">The `"compact"` setting is only available in [Windows Terminal Preview](https://aka.ms/terminal-preview/).</span></span>

### <a name="hide-close-all-tabs-popup"></a><span data-ttu-id="dd8df-150">Popupfenster „Alle Registerkarten schließen“ ausblenden</span><span class="sxs-lookup"><span data-stu-id="dd8df-150">Hide close all tabs popup</span></span>

:::row:::
:::column span="":::
<span data-ttu-id="dd8df-151">Wenn diese Einstellung auf `true` festgelegt ist, _erfordert_ das Schließen eines Fensters mit mehreren geöffneten Registerkarten eine Bestätigung.</span><span class="sxs-lookup"><span data-stu-id="dd8df-151">When this is set to `true`, closing a window with multiple tabs open _will_ require confirmation.</span></span> <span data-ttu-id="dd8df-152">Wenn diese Einstellung auf `false` festgelegt ist, erfordert das Schließen eines Fensters mit mehreren geöffneten Registerkarten _keine_ Bestätigung.</span><span class="sxs-lookup"><span data-stu-id="dd8df-152">When it's set to `false`, closing a window with multiple tabs open _will not_ require confirmation.</span></span>

<span data-ttu-id="dd8df-153">**Eigenschaftenname:** `confirmCloseAllTabs`</span><span class="sxs-lookup"><span data-stu-id="dd8df-153">**Property name:** `confirmCloseAllTabs`</span></span>

<span data-ttu-id="dd8df-154">**Erfordernis:** Optional</span><span class="sxs-lookup"><span data-stu-id="dd8df-154">**Necessity:** Optional</span></span>

<span data-ttu-id="dd8df-155">**Akzeptiert:** `true`, `false`</span><span class="sxs-lookup"><span data-stu-id="dd8df-155">**Accepts:** `true`, `false`</span></span>

<span data-ttu-id="dd8df-156">**Standardwert:** `true`</span><span class="sxs-lookup"><span data-stu-id="dd8df-156">**Default value:** `true`</span></span>

:::column-end:::
:::column span="":::
![Windows Terminal: Bestätigung zum Schließen aller Registerkarten](./../images/confirm-close-all-tabs.png)

:::column-end:::
:::row-end:::

<br />

___

## <a name="launch-settings"></a><span data-ttu-id="dd8df-158">Starteinstellungen</span><span class="sxs-lookup"><span data-stu-id="dd8df-158">Launch settings</span></span>

### <a name="launch-on-startup-preview"></a><span data-ttu-id="dd8df-159">Beim Start öffnen ([Vorschau](https://aka.ms/terminal-preview/))</span><span class="sxs-lookup"><span data-stu-id="dd8df-159">Launch on startup ([Preview](https://aka.ms/terminal-preview/))</span></span>

<span data-ttu-id="dd8df-160">Wenn diese Einstellung auf `true` festgelegt ist, ist das Öffnen von Windows Terminal beim Systemstart aktiviert.</span><span class="sxs-lookup"><span data-stu-id="dd8df-160">When set to `true`, this enables the launch of Windows Terminal at startup.</span></span> <span data-ttu-id="dd8df-161">Das Festlegen der Einstellung auf `false` deaktiviert den Eintrag der Systemstartaufgabe.</span><span class="sxs-lookup"><span data-stu-id="dd8df-161">Setting this to `false` will disable the startup task entry.</span></span> <span data-ttu-id="dd8df-162">Hinweis: Wenn der Eintrag der Systemstartaufgabe von Windows Terminal entweder durch eine Organisationsrichtlinie oder durch eine Benutzeraktion deaktiviert ist, hat diese Einstellung keine Wirkung.</span><span class="sxs-lookup"><span data-stu-id="dd8df-162">Note: if the Windows Terminal startup task entry is disabled either by org policy or by user action this setting will have no effect.</span></span>

<span data-ttu-id="dd8df-163">**Eigenschaftenname:** `startOnUserLogin`</span><span class="sxs-lookup"><span data-stu-id="dd8df-163">**Property name:** `startOnUserLogin`</span></span>

<span data-ttu-id="dd8df-164">**Erfordernis:** Optional</span><span class="sxs-lookup"><span data-stu-id="dd8df-164">**Necessity:** Optional</span></span>

<span data-ttu-id="dd8df-165">**Akzeptiert:** `true`, `false`</span><span class="sxs-lookup"><span data-stu-id="dd8df-165">**Accepts:** `true`, `false`</span></span>

<span data-ttu-id="dd8df-166">**Standardwert:** `false`</span><span class="sxs-lookup"><span data-stu-id="dd8df-166">**Default value:** `false`</span></span>

> [!IMPORTANT]
> <span data-ttu-id="dd8df-167">Diese Funktion steht nur in der [Windows Terminal-Vorschau](https://aka.ms/terminal-preview/) zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="dd8df-167">This feature is only available in [Windows Terminal Preview](https://aka.ms/terminal-preview/).</span></span>

### <a name="launch-size"></a><span data-ttu-id="dd8df-168">Startgröße</span><span class="sxs-lookup"><span data-stu-id="dd8df-168">Launch size</span></span>

<span data-ttu-id="dd8df-169">Hiermit wird definiert, ob das Terminal maximiert, im Vollbildmodus oder in einem Fenster gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="dd8df-169">This defines whether the terminal will launch as maximized, fullscreen, or in a window.</span></span>

<span data-ttu-id="dd8df-170">**Eigenschaftenname:** `launchMode`</span><span class="sxs-lookup"><span data-stu-id="dd8df-170">**Property name:** `launchMode`</span></span>

<span data-ttu-id="dd8df-171">**Erfordernis:** Optional</span><span class="sxs-lookup"><span data-stu-id="dd8df-171">**Necessity:** Optional</span></span>

<span data-ttu-id="dd8df-172">**Akzeptiert:** `"default"`, `"maximized"`, `"fullscreen"`</span><span class="sxs-lookup"><span data-stu-id="dd8df-172">**Accepts:** `"default"`, `"maximized"`, `"fullscreen"`</span></span>

<span data-ttu-id="dd8df-173">**Standardwert:** `"default"`</span><span class="sxs-lookup"><span data-stu-id="dd8df-173">**Default value:** `"default"`</span></span>

> [!IMPORTANT]
> <span data-ttu-id="dd8df-174">Die `"fullscreen"`-Einstellung steht nur in der [Windows Terminal-Vorschau](https://aka.ms/terminal-preview/) zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="dd8df-174">The `"fullscreen"` setting is only available in [Windows Terminal Preview](https://aka.ms/terminal-preview/).</span></span>

### <a name="launch-position"></a><span data-ttu-id="dd8df-175">Startposition</span><span class="sxs-lookup"><span data-stu-id="dd8df-175">Launch position</span></span>

<span data-ttu-id="dd8df-176">Hiermit wird die Pixelposition der oberen linken Ecke des Fensters beim ersten Laden festgelegt.</span><span class="sxs-lookup"><span data-stu-id="dd8df-176">This sets the pixel position of the top left corner of the window upon first load.</span></span> <span data-ttu-id="dd8df-177">Bei einem System mit mehreren Bildschirmen sind diese Koordinaten relativ zur oberen linken Ecke des primären Bildschirms.</span><span class="sxs-lookup"><span data-stu-id="dd8df-177">On a system with multiple displays, these coordinates are relative to the top left of the primary display.</span></span> <span data-ttu-id="dd8df-178">Wenn keine X-oder Y-Koordinate bereitgestellt wird, verwendet das Terminal die Standardeinstellung des Systems für diesen Wert.</span><span class="sxs-lookup"><span data-stu-id="dd8df-178">If an X or Y coordinate is not provided, the terminal will use the system default for that value.</span></span> <span data-ttu-id="dd8df-179">Wenn `launchMode` auf `"maximized"` festgelegt ist, wird das Fenster auf dem Monitor maximiert, der durch diese Koordinaten angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="dd8df-179">If `launchMode` is set to `"maximized"`, the window will be maximized on the monitor specified by those coordinates.</span></span>

<span data-ttu-id="dd8df-180">**Eigenschaftenname:** `initialPosition`</span><span class="sxs-lookup"><span data-stu-id="dd8df-180">**Property name:** `initialPosition`</span></span>

<span data-ttu-id="dd8df-181">**Erfordernis:** Optional</span><span class="sxs-lookup"><span data-stu-id="dd8df-181">**Necessity:** Optional</span></span>

<span data-ttu-id="dd8df-182">**Akzeptiert:** Koordinaten als Zeichenfolge in den folgenden Formaten: `","`, `"#,#"`, `"#,"`, `",#"`</span><span class="sxs-lookup"><span data-stu-id="dd8df-182">**Accepts:** Coordinates as a string in the following formats: `","`, `"#,#"`, `"#,"`, `",#"`</span></span>

<span data-ttu-id="dd8df-183">**Standardwert:** `","`</span><span class="sxs-lookup"><span data-stu-id="dd8df-183">**Default value:** `","`</span></span>

### <a name="columns-on-first-launch"></a><span data-ttu-id="dd8df-184">Spalten beim ersten Start</span><span class="sxs-lookup"><span data-stu-id="dd8df-184">Columns on first launch</span></span>

<span data-ttu-id="dd8df-185">Dies ist die Anzahl der Zeichenspalten, die beim ersten Laden im Fenster angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="dd8df-185">This is the number of character columns displayed in the window upon first load.</span></span> <span data-ttu-id="dd8df-186">Wenn `launchMode` auf `"maximized"` festgelegt ist, wird diese Eigenschaft ignoriert.</span><span class="sxs-lookup"><span data-stu-id="dd8df-186">If `launchMode` is set to `"maximized"`, this property is ignored.</span></span>

<span data-ttu-id="dd8df-187">**Eigenschaftenname:** `initialCols`</span><span class="sxs-lookup"><span data-stu-id="dd8df-187">**Property name:** `initialCols`</span></span>

<span data-ttu-id="dd8df-188">**Erfordernis:** Optional</span><span class="sxs-lookup"><span data-stu-id="dd8df-188">**Necessity:** Optional</span></span>

<span data-ttu-id="dd8df-189">**Akzeptiert:** Ganze Zahl</span><span class="sxs-lookup"><span data-stu-id="dd8df-189">**Accepts:** Integer</span></span>

<span data-ttu-id="dd8df-190">**Standardwert:** `120`</span><span class="sxs-lookup"><span data-stu-id="dd8df-190">**Default value:** `120`</span></span>

### <a name="rows-on-first-launch"></a><span data-ttu-id="dd8df-191">Zeilen beim ersten Start</span><span class="sxs-lookup"><span data-stu-id="dd8df-191">Rows on first launch</span></span>

<span data-ttu-id="dd8df-192">Dies ist die Anzahl der Zeilen, die beim ersten Laden im Fenster angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="dd8df-192">This is the number of rows displayed in the window upon first load.</span></span> <span data-ttu-id="dd8df-193">Wenn `launchMode` auf `"maximized"` festgelegt ist, wird diese Eigenschaft ignoriert.</span><span class="sxs-lookup"><span data-stu-id="dd8df-193">If `launchMode` is set to `"maximized"`, this property is ignored.</span></span>

<span data-ttu-id="dd8df-194">**Eigenschaftenname:** `initialRows`</span><span class="sxs-lookup"><span data-stu-id="dd8df-194">**Property name:** `initialRows`</span></span>

<span data-ttu-id="dd8df-195">**Erfordernis:** Optional</span><span class="sxs-lookup"><span data-stu-id="dd8df-195">**Necessity:** Optional</span></span>

<span data-ttu-id="dd8df-196">**Akzeptiert:** Ganze Zahl</span><span class="sxs-lookup"><span data-stu-id="dd8df-196">**Accepts:** Integer</span></span>

<span data-ttu-id="dd8df-197">**Standardwert:** `30`</span><span class="sxs-lookup"><span data-stu-id="dd8df-197">**Default value:** `30`</span></span>

<br />

___

## <a name="title-bar-settings"></a><span data-ttu-id="dd8df-198">Titelleisteneinstellungen</span><span class="sxs-lookup"><span data-stu-id="dd8df-198">Title bar settings</span></span>

### <a name="showhide-the-title-bar"></a><span data-ttu-id="dd8df-199">Titelleiste anzeigen/ausblenden</span><span class="sxs-lookup"><span data-stu-id="dd8df-199">Show/Hide the title bar</span></span>

:::row:::
:::column span="":::
<span data-ttu-id="dd8df-200">Wenn diese Einstellung auf `true` festgelegt ist, werden die Registerkarten in die Titelleiste verschoben, und die Titelleiste wird ausgeblendet.</span><span class="sxs-lookup"><span data-stu-id="dd8df-200">When this is set to `true`, the tabs are moved into the title bar and the title bar disappears.</span></span> <span data-ttu-id="dd8df-201">Wenn sie auf `false` festgelegt ist, befindet sich die Titelleiste oberhalb der Registerkarten.</span><span class="sxs-lookup"><span data-stu-id="dd8df-201">When it's set to `false`, the title bar sits above the tabs.</span></span> <span data-ttu-id="dd8df-202">Beachten Sie, dass das Ändern dieser Einstellung das Starten einer neuen Terminalinstanz erfordert.</span><span class="sxs-lookup"><span data-stu-id="dd8df-202">Note that changing this setting will require starting a new terminal instance.</span></span>

<span data-ttu-id="dd8df-203">**Eigenschaftenname:** `showTabsInTitlebar`</span><span class="sxs-lookup"><span data-stu-id="dd8df-203">**Property name:** `showTabsInTitlebar`</span></span>

<span data-ttu-id="dd8df-204">**Erfordernis:** Optional</span><span class="sxs-lookup"><span data-stu-id="dd8df-204">**Necessity:** Optional</span></span>

<span data-ttu-id="dd8df-205">**Akzeptiert:** `true`, `false`</span><span class="sxs-lookup"><span data-stu-id="dd8df-205">**Accepts:** `true`, `false`</span></span>

<span data-ttu-id="dd8df-206">**Standardwert:** `true`</span><span class="sxs-lookup"><span data-stu-id="dd8df-206">**Default value:** `true`</span></span>

:::column-end:::
:::column span="":::
![Windows Terminal zeigt Registerkarten in der Titelleiste an](./../images/show-tabs-in-title-bar.gif)

:::column-end:::
:::row-end:::

### <a name="set-the-text-in-the-title-bar"></a><span data-ttu-id="dd8df-208">Text in der Titelleiste festlegen</span><span class="sxs-lookup"><span data-stu-id="dd8df-208">Set the text in the title bar</span></span>

<span data-ttu-id="dd8df-209">Wenn diese Einstellung auf `true` festgelegt ist, wird in der Titelleiste der Titel der ausgewählten Registerkarte angezeigt. Wenn sie auf `false` festgelegt ist, wird in der Titelleiste „Windows Terminal“ angezeigt.</span><span class="sxs-lookup"><span data-stu-id="dd8df-209">When this is set to `true`, the title bar displays the title of the selected tab. When it's set to `false`, title bar displays "Windows Terminal".</span></span> <span data-ttu-id="dd8df-210">Beachten Sie, dass das Ändern dieser Einstellung das Starten einer neuen Terminalinstanz erfordert.</span><span class="sxs-lookup"><span data-stu-id="dd8df-210">Note that changing this setting will require starting a new terminal instance.</span></span>

<span data-ttu-id="dd8df-211">**Eigenschaftenname:** `showTerminalTitleInTitlebar`</span><span class="sxs-lookup"><span data-stu-id="dd8df-211">**Property name:** `showTerminalTitleInTitlebar`</span></span>

<span data-ttu-id="dd8df-212">**Erfordernis:** Optional</span><span class="sxs-lookup"><span data-stu-id="dd8df-212">**Necessity:** Optional</span></span>

<span data-ttu-id="dd8df-213">**Akzeptiert:** `true`, `false`</span><span class="sxs-lookup"><span data-stu-id="dd8df-213">**Accepts:** `true`, `false`</span></span>

<span data-ttu-id="dd8df-214">**Standardwert:** `true`</span><span class="sxs-lookup"><span data-stu-id="dd8df-214">**Default value:** `true`</span></span>

<br />

___

## <a name="selection-settings"></a><span data-ttu-id="dd8df-215">Auswahleinstellungen</span><span class="sxs-lookup"><span data-stu-id="dd8df-215">Selection settings</span></span>

### <a name="copy-after-selection-is-made"></a><span data-ttu-id="dd8df-216">Nach Auswahl kopieren</span><span class="sxs-lookup"><span data-stu-id="dd8df-216">Copy after selection is made</span></span>

<span data-ttu-id="dd8df-217">Wenn diese Einstellung auf `true` festgelegt ist, wird eine Auswahl sofort bei der Erstellung in die Zwischenablage kopiert.</span><span class="sxs-lookup"><span data-stu-id="dd8df-217">When this is set to `true`, a selection is immediately copied to your clipboard upon creation.</span></span> <span data-ttu-id="dd8df-218">Beim Klicken mit der rechten Maustaste erfolgt in dieser Fall immer ein Einfügevorgang.</span><span class="sxs-lookup"><span data-stu-id="dd8df-218">The right-click on your mouse will always paste in this case.</span></span> <span data-ttu-id="dd8df-219">Wenn sie auf `false` festgelegt ist, bleibt die Auswahl bestehen und wartet auf weitere Maßnahmen.</span><span class="sxs-lookup"><span data-stu-id="dd8df-219">When it's set to `false`, the selection persists and awaits further action.</span></span> <span data-ttu-id="dd8df-220">Wenn Sie mit der rechten Maustaste klicken, wird die Auswahl kopiert.</span><span class="sxs-lookup"><span data-stu-id="dd8df-220">Using your mouse to right-click will copy the selection.</span></span>

<span data-ttu-id="dd8df-221">**Eigenschaftenname:** `copyOnSelect`</span><span class="sxs-lookup"><span data-stu-id="dd8df-221">**Property name:** `copyOnSelect`</span></span>

<span data-ttu-id="dd8df-222">**Erfordernis:** Optional</span><span class="sxs-lookup"><span data-stu-id="dd8df-222">**Necessity:** Optional</span></span>

<span data-ttu-id="dd8df-223">**Akzeptiert:** `true`, `false`</span><span class="sxs-lookup"><span data-stu-id="dd8df-223">**Accepts:** `true`, `false`</span></span>

<span data-ttu-id="dd8df-224">**Standardwert:** `false`</span><span class="sxs-lookup"><span data-stu-id="dd8df-224">**Default value:** `false`</span></span>

### <a name="copy-formatting"></a><span data-ttu-id="dd8df-225">Formatierung kopieren</span><span class="sxs-lookup"><span data-stu-id="dd8df-225">Copy formatting</span></span>

<span data-ttu-id="dd8df-226">Wenn diese Einstellung auf `true` festgelegt ist, werden Farb- und Schriftformatierung des ausgewählten Textes ebenfalls in die Zwischenablage kopiert.</span><span class="sxs-lookup"><span data-stu-id="dd8df-226">When this is set to `true`, the color and font formatting of selected text is also copied to your clipboard.</span></span> <span data-ttu-id="dd8df-227">Wenn sie auf `false` festgelegt ist, wird Nur-Text in die Zwischenablage kopiert.</span><span class="sxs-lookup"><span data-stu-id="dd8df-227">When it's set to `false`, only plain text is copied to your clipboard.</span></span>

<span data-ttu-id="dd8df-228">**Eigenschaftenname:** `copyFormatting`</span><span class="sxs-lookup"><span data-stu-id="dd8df-228">**Property name:** `copyFormatting`</span></span>

<span data-ttu-id="dd8df-229">**Erfordernis:** Optional</span><span class="sxs-lookup"><span data-stu-id="dd8df-229">**Necessity:** Optional</span></span>

<span data-ttu-id="dd8df-230">**Akzeptiert:** `true`, `false`</span><span class="sxs-lookup"><span data-stu-id="dd8df-230">**Accepts:** `true`, `false`</span></span>

<span data-ttu-id="dd8df-231">**Standardwert:** `false`</span><span class="sxs-lookup"><span data-stu-id="dd8df-231">**Default value:** `false`</span></span>

### <a name="word-delimiters"></a><span data-ttu-id="dd8df-232">Worttrennzeichen</span><span class="sxs-lookup"><span data-stu-id="dd8df-232">Word delimiters</span></span>

<span data-ttu-id="dd8df-233">Hiermit werden die in einer durch Doppelklick ausgelösten Auswahl verwendeten Worttrennzeichen festgelegt.</span><span class="sxs-lookup"><span data-stu-id="dd8df-233">This determines the word delimiters used in a double-click selection.</span></span> <span data-ttu-id="dd8df-234">Worttrennzeichen sind Zeichen, die angeben, wo die Grenze zwischen zwei Wörtern liegt.</span><span class="sxs-lookup"><span data-stu-id="dd8df-234">Word delimiters are characters that specify where the boundary is between two words.</span></span> <span data-ttu-id="dd8df-235">Die häufigsten Beispiele sind Leerzeichen, Semikolons, Kommas und Punkte.</span><span class="sxs-lookup"><span data-stu-id="dd8df-235">The most common examples are spaces, semicolons, commas, and periods.</span></span>

<span data-ttu-id="dd8df-236">**Eigenschaftenname:** `wordDelimiters`</span><span class="sxs-lookup"><span data-stu-id="dd8df-236">**Property name:** `wordDelimiters`</span></span>

<span data-ttu-id="dd8df-237">**Erfordernis:** Optional</span><span class="sxs-lookup"><span data-stu-id="dd8df-237">**Necessity:** Optional</span></span>

<span data-ttu-id="dd8df-238">**Akzeptiert:** Zeichen als Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="dd8df-238">**Accepts:** Characters as a string</span></span>

<span data-ttu-id="dd8df-239">**Standardwert:** <code>&nbsp;&#x2f;&#x5c;&#x28;&#x29;&#x22;&#x27;&#x2d;&#x3a;&#x2c;&#x2e;&#x3b;&#x3c;&#x3e;&#x7e;&#x21;&#x40;&#x23;&#x24;&#x25;&#x5e;&#x26;&#x2a;&#x7c;&#x2b;&#x3d;&#x5b;&#x5d;&#x7b;&#x7d;&#x7e;&#x3f;│</code></span><span class="sxs-lookup"><span data-stu-id="dd8df-239">**Default value:** <code>&nbsp;&#x2f;&#x5c;&#x28;&#x29;&#x22;&#x27;&#x2d;&#x3a;&#x2c;&#x2e;&#x3b;&#x3c;&#x3e;&#x7e;&#x21;&#x40;&#x23;&#x24;&#x25;&#x5e;&#x26;&#x2a;&#x7c;&#x2b;&#x3d;&#x5b;&#x5d;&#x7b;&#x7d;&#x7e;&#x3f;│</code></span></span><br><span data-ttu-id="dd8df-240">_(`│` ist `U+2502 BOX DRAWINGS LIGHT VERTICAL`)_</span><span class="sxs-lookup"><span data-stu-id="dd8df-240">_(`│` is `U+2502 BOX DRAWINGS LIGHT VERTICAL`)_</span></span>

<br />

___

## <a name="scroll-speed"></a><span data-ttu-id="dd8df-241">Scrollgeschwindigkeit</span><span class="sxs-lookup"><span data-stu-id="dd8df-241">Scroll speed</span></span>

<span data-ttu-id="dd8df-242">Dies ist die Anzahl der Zeilen, die gleichzeitig mit dem Mausrad gescrollt werden können.</span><span class="sxs-lookup"><span data-stu-id="dd8df-242">This is the number of rows to scroll at a time with the mouse wheel.</span></span> <span data-ttu-id="dd8df-243">Dadurch wird die Systemeinstellung außer Kraft gesetzt, wenn der Wert nicht null (0) oder `"system"` ist.</span><span class="sxs-lookup"><span data-stu-id="dd8df-243">This will override the system setting if the value is not zero or `"system"`.</span></span>

<span data-ttu-id="dd8df-244">**Eigenschaftenname:** `rowsToScroll`</span><span class="sxs-lookup"><span data-stu-id="dd8df-244">**Property name:** `rowsToScroll`</span></span>

<span data-ttu-id="dd8df-245">**Erfordernis:** Optional</span><span class="sxs-lookup"><span data-stu-id="dd8df-245">**Necessity:** Optional</span></span>

<span data-ttu-id="dd8df-246">**Akzeptiert:** Ganze Zahl</span><span class="sxs-lookup"><span data-stu-id="dd8df-246">**Accepts:** Integer</span></span>

<span data-ttu-id="dd8df-247">**Standardwert:** `"system"`</span><span class="sxs-lookup"><span data-stu-id="dd8df-247">**Default value:** `"system"`</span></span>

<br />

___

## <a name="window-resize-behavior"></a><span data-ttu-id="dd8df-248">Verhalten bei der Größenänderung von Fenstern</span><span class="sxs-lookup"><span data-stu-id="dd8df-248">Window resize behavior</span></span>

:::row:::
:::column span="":::
<span data-ttu-id="dd8df-249">Wenn diese Einstellung auf `true` festgelegt ist, wird das Fenster bei einer Größenänderung an der nächstgelegenen Zeichengrenze ausgerichtet.</span><span class="sxs-lookup"><span data-stu-id="dd8df-249">When this is set to `true`, the window will snap to the nearest character boundary on resize.</span></span> <span data-ttu-id="dd8df-250">Wenn sie auf `false` festgelegt ist, wird die Größe des Fensters „reibungslos“ angepasst.</span><span class="sxs-lookup"><span data-stu-id="dd8df-250">When it's set to `false`, the window will resize "smoothly".</span></span>

<span data-ttu-id="dd8df-251">**Eigenschaftenname:** `snapToGridOnResize`</span><span class="sxs-lookup"><span data-stu-id="dd8df-251">**Property name:** `snapToGridOnResize`</span></span>

<span data-ttu-id="dd8df-252">**Erfordernis:** Optional</span><span class="sxs-lookup"><span data-stu-id="dd8df-252">**Necessity:** Optional</span></span>

<span data-ttu-id="dd8df-253">**Akzeptiert:** `true`, `false`</span><span class="sxs-lookup"><span data-stu-id="dd8df-253">**Accepts:** `true`, `false`</span></span>

<span data-ttu-id="dd8df-254">**Standardwert:** `true`</span><span class="sxs-lookup"><span data-stu-id="dd8df-254">**Default value:** `true`</span></span>

:::column-end:::
:::column span="":::
![Windows Terminal: „Am Raster ausrichten“ beim Ändern der Größe](./../images/snap-to-grid-on-resize.gif)

:::column-end:::
:::row-end:::

<br />

___

## <a name="rendering-settings"></a><span data-ttu-id="dd8df-256">Renderingeinstellungen</span><span class="sxs-lookup"><span data-stu-id="dd8df-256">Rendering settings</span></span>

<span data-ttu-id="dd8df-257">Wenn Sie die Renderingeinstellungen ändern möchten, finden Sie weitere Informationen zu Ihrer Unterstützung auf der [Seite zur Problembehandlung](./../troubleshooting.md#the-text-is-blurry).</span><span class="sxs-lookup"><span data-stu-id="dd8df-257">If you are thinking about changing the rendering settings, additional information is provided on the [Troubleshooting page](./../troubleshooting.md#the-text-is-blurry) to help guide you.</span></span>

### <a name="screen-redrawing"></a><span data-ttu-id="dd8df-258">Neuzeichnen des Bildschirms</span><span class="sxs-lookup"><span data-stu-id="dd8df-258">Screen redrawing</span></span>

<span data-ttu-id="dd8df-259">Wenn diese Einstellung auf `true` festgelegt wird, zeichnet das Terminal für jedes Einzelbild den gesamten Bildschirm neu.</span><span class="sxs-lookup"><span data-stu-id="dd8df-259">When this set to `true`, the terminal will redraw the entire screen each frame.</span></span> <span data-ttu-id="dd8df-260">Bei Einstellung auf `false` werden nur die Updates am Bildschirm zwischen den Einzelbildern gerendert.</span><span class="sxs-lookup"><span data-stu-id="dd8df-260">When set to `false`, it will render only the updates to the screen between frames.</span></span>

<span data-ttu-id="dd8df-261">**Eigenschaftenname:** `experimental.rendering.forceFullRepaint`</span><span class="sxs-lookup"><span data-stu-id="dd8df-261">**Property name:** `experimental.rendering.forceFullRepaint`</span></span>

<span data-ttu-id="dd8df-262">**Erfordernis:** Optional</span><span class="sxs-lookup"><span data-stu-id="dd8df-262">**Necessity:** Optional</span></span>

<span data-ttu-id="dd8df-263">**Akzeptiert:** `true`, `false`</span><span class="sxs-lookup"><span data-stu-id="dd8df-263">**Accepts:** `true`, `false`</span></span>

<span data-ttu-id="dd8df-264">**Standardwert:** `false`</span><span class="sxs-lookup"><span data-stu-id="dd8df-264">**Default value:** `false`</span></span>

### <a name="software-rendering"></a><span data-ttu-id="dd8df-265">Softwarerendering</span><span class="sxs-lookup"><span data-stu-id="dd8df-265">Software rendering</span></span>

<span data-ttu-id="dd8df-266">Wenn diese Einstellung auf `true` festgelegt ist, verwendet das Terminal den Softwarerenderer (auch als</span><span class="sxs-lookup"><span data-stu-id="dd8df-266">When this is set to `true`, the terminal will use the software renderer (a.k.a.</span></span> <span data-ttu-id="dd8df-267">WARP bezeichnet) anstelle des Hardwarerenderers.</span><span class="sxs-lookup"><span data-stu-id="dd8df-267">WARP) instead of the hardware one.</span></span>

<span data-ttu-id="dd8df-268">**Eigenschaftenname:** `experimental.rendering.software`</span><span class="sxs-lookup"><span data-stu-id="dd8df-268">**Property name:** `experimental.rendering.software`</span></span>

<span data-ttu-id="dd8df-269">**Erfordernis:** Optional</span><span class="sxs-lookup"><span data-stu-id="dd8df-269">**Necessity:** Optional</span></span>

<span data-ttu-id="dd8df-270">**Akzeptiert:** `true`, `false`</span><span class="sxs-lookup"><span data-stu-id="dd8df-270">**Accepts:** `true`, `false`</span></span>

<span data-ttu-id="dd8df-271">**Standardwert:** `false`</span><span class="sxs-lookup"><span data-stu-id="dd8df-271">**Default value:** `false`</span></span>
