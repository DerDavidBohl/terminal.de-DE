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
# <a name="profile-settings-in-the-windows-terminal"></a><span data-ttu-id="1c58d-103">Profileinstellungen in Windows Terminal</span><span class="sxs-lookup"><span data-stu-id="1c58d-103">Profile settings in the Windows Terminal</span></span>

<span data-ttu-id="1c58d-104">Die unten aufgeführten Einstellungen sind spezifisch für die einzelnen eindeutigen Profile.</span><span class="sxs-lookup"><span data-stu-id="1c58d-104">The settings listed below are specific to each unique profile.</span></span> <span data-ttu-id="1c58d-105">Wenn Sie möchten, dass eine Einstellung auf alle Profile angewendet wird, können Sie sie dem Abschnitt `defaults` über der Profilliste in der Datei „settings.json“ hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="1c58d-105">If you'd like a setting to apply to all of your profiles, you can add it to the `defaults` section above the list of profiles in your settings.json file.</span></span>

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

## <a name="unique-identifier"></a><span data-ttu-id="1c58d-106">Eindeutiger Bezeichner</span><span class="sxs-lookup"><span data-stu-id="1c58d-106">Unique identifier</span></span>

<span data-ttu-id="1c58d-107">Profile können eine GUID als eindeutigen Bezeichner verwenden.</span><span class="sxs-lookup"><span data-stu-id="1c58d-107">Profiles can use a GUID as a unique identifier.</span></span> <span data-ttu-id="1c58d-108">Damit ein Profil zu Ihrem Standardprofil wird, benötigt es eine GUID für die globale Einstellung `defaultProfile`.</span><span class="sxs-lookup"><span data-stu-id="1c58d-108">To make a profile your default profile, it needs a GUID for the `defaultProfile` global setting.</span></span>

<span data-ttu-id="1c58d-109">**Eigenschaftenname:** `guid`</span><span class="sxs-lookup"><span data-stu-id="1c58d-109">**Property name:** `guid`</span></span>

<span data-ttu-id="1c58d-110">**Erfordernis:** Erforderlich</span><span class="sxs-lookup"><span data-stu-id="1c58d-110">**Necessity:** Required</span></span>

<span data-ttu-id="1c58d-111">**Akzeptiert:** GUID als Zeichenfolge im Registrierungsformat: `"{00000000-0000-0000-0000-000000000000}"`</span><span class="sxs-lookup"><span data-stu-id="1c58d-111">**Accepts:** GUID as a string in registry format: `"{00000000-0000-0000-0000-000000000000}"`</span></span>

<br />

___

## <a name="executable-settings"></a><span data-ttu-id="1c58d-112">Ausführbare Einstellungen</span><span class="sxs-lookup"><span data-stu-id="1c58d-112">Executable settings</span></span>

### <a name="command-line"></a><span data-ttu-id="1c58d-113">Befehlszeile</span><span class="sxs-lookup"><span data-stu-id="1c58d-113">Command line</span></span>

<span data-ttu-id="1c58d-114">Dies ist die ausführbare Datei, die im Profil verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="1c58d-114">This is the executable used in the profile.</span></span>

<span data-ttu-id="1c58d-115">**Eigenschaftenname:** `commandline`</span><span class="sxs-lookup"><span data-stu-id="1c58d-115">**Property name:** `commandline`</span></span>

<span data-ttu-id="1c58d-116">**Erfordernis:** Optional</span><span class="sxs-lookup"><span data-stu-id="1c58d-116">**Necessity:** Optional</span></span>

<span data-ttu-id="1c58d-117">**Akzeptiert:** Name der ausführbaren Datei als Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="1c58d-117">**Accepts:** Executable file name as a string</span></span>

<span data-ttu-id="1c58d-118">**Standardwert:** `"cmd.exe"`</span><span class="sxs-lookup"><span data-stu-id="1c58d-118">**Default value:** `"cmd.exe"`</span></span>

### <a name="source"></a><span data-ttu-id="1c58d-119">Quelle</span><span class="sxs-lookup"><span data-stu-id="1c58d-119">Source</span></span>

<span data-ttu-id="1c58d-120">Hiermit wird der Name des Profilgenerators gespeichert, von dem das Profil stammt.</span><span class="sxs-lookup"><span data-stu-id="1c58d-120">This stores the name of the profile generator that originated the profile.</span></span> <span data-ttu-id="1c58d-121">_Es sind keine erkennbaren Werte für dieses Feld vorhanden._</span><span class="sxs-lookup"><span data-stu-id="1c58d-121">_There are no discoverable values for this field._</span></span> <span data-ttu-id="1c58d-122">Weitere Informationen zu dynamischen Profilen finden Sie auf der Seite [Dynamische Profile](./../dynamic-profiles.md).</span><span class="sxs-lookup"><span data-stu-id="1c58d-122">For additional information on dynamic profiles, visit the [Dynamic profiles page](./../dynamic-profiles.md).</span></span>

<span data-ttu-id="1c58d-123">**Eigenschaftenname:** `source`</span><span class="sxs-lookup"><span data-stu-id="1c58d-123">**Property name:** `source`</span></span>

<span data-ttu-id="1c58d-124">**Erfordernis:** Optional</span><span class="sxs-lookup"><span data-stu-id="1c58d-124">**Necessity:** Optional</span></span>

<span data-ttu-id="1c58d-125">**Akzeptiert:** Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="1c58d-125">**Accepts:** String</span></span>

### <a name="starting-directory"></a><span data-ttu-id="1c58d-126">Startverzeichnis</span><span class="sxs-lookup"><span data-stu-id="1c58d-126">Starting directory</span></span>

<span data-ttu-id="1c58d-127">Dies ist das Verzeichnis, in dem die Shell beim Laden gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="1c58d-127">This is the directory the shell starts in when it is loaded.</span></span>

<span data-ttu-id="1c58d-128">**Eigenschaftenname:** `startingDirectory`</span><span class="sxs-lookup"><span data-stu-id="1c58d-128">**Property name:** `startingDirectory`</span></span>

<span data-ttu-id="1c58d-129">**Erfordernis:** Optional</span><span class="sxs-lookup"><span data-stu-id="1c58d-129">**Necessity:** Optional</span></span>

<span data-ttu-id="1c58d-130">**Akzeptiert:** Speicherort des Ordners als Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="1c58d-130">**Accepts:** Folder location as a string</span></span>

<span data-ttu-id="1c58d-131">**Standardwert:** `"%USERPROFILE%"`</span><span class="sxs-lookup"><span data-stu-id="1c58d-131">**Default value:** `"%USERPROFILE%"`</span></span>

<br />

___

## <a name="dropdown-settings"></a><span data-ttu-id="1c58d-132">Dropdowneinstellungen</span><span class="sxs-lookup"><span data-stu-id="1c58d-132">Dropdown settings</span></span>

<span data-ttu-id="1c58d-133">![Windows Terminal-Dropdownmenü](./../images/dropdown.png)
_Konfiguration: [Raspberry Ubuntu](./../custom-terminal-gallery/raspberry-ubuntu.md)_</span><span class="sxs-lookup"><span data-stu-id="1c58d-133">![Windows Terminal dropdown](./../images/dropdown.png)
_Configuration: [Raspberry Ubuntu](./../custom-terminal-gallery/raspberry-ubuntu.md)_</span></span>

### <a name="name"></a><span data-ttu-id="1c58d-134">Name</span><span class="sxs-lookup"><span data-stu-id="1c58d-134">Name</span></span>

<span data-ttu-id="1c58d-135">Dies ist der Name des Profils, der im Dropdownmenü angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="1c58d-135">This is the name of the profile that will be displayed in the dropdown menu.</span></span> <span data-ttu-id="1c58d-136">Dieser Wert wird auch als „Titel“ verwendet, der beim Start an die Shell übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="1c58d-136">This value is also used as the "title" to pass to the shell on startup.</span></span> <span data-ttu-id="1c58d-137">Einige Shells (z. B. `bash`) können diesen Anfangswert möglicherweise ignorieren, während andere (`Command Prompt`, `PowerShell`) diesen Wert während der Lebensdauer der Anwendung verwenden.</span><span class="sxs-lookup"><span data-stu-id="1c58d-137">Some shells (like `bash`) may choose to ignore this initial value, while others (`Command Prompt`, `PowerShell`) may use this value over the lifetime of the application.</span></span> <span data-ttu-id="1c58d-138">Dieses Verhalten von „Titel“ kann durch `tabTitle` außer Kraft gesetzt werden.</span><span class="sxs-lookup"><span data-stu-id="1c58d-138">This "title" behavior can be overridden by using `tabTitle`.</span></span>

<span data-ttu-id="1c58d-139">**Eigenschaftenname:** `name`</span><span class="sxs-lookup"><span data-stu-id="1c58d-139">**Property name:** `name`</span></span>

<span data-ttu-id="1c58d-140">**Erfordernis:** Erforderlich</span><span class="sxs-lookup"><span data-stu-id="1c58d-140">**Necessity:** Required</span></span>

<span data-ttu-id="1c58d-141">**Akzeptiert:** Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="1c58d-141">**Accepts:** String</span></span>

### <a name="icon"></a><span data-ttu-id="1c58d-142">Symbol</span><span class="sxs-lookup"><span data-stu-id="1c58d-142">Icon</span></span>

<span data-ttu-id="1c58d-143">Hiermit wird das Symbol festgelegt, das auf der Registerkarte und im Dropdownmenü angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="1c58d-143">This sets the icon that displays within the tab and the dropdown menu.</span></span>

<span data-ttu-id="1c58d-144">**Eigenschaftenname:** `icon`</span><span class="sxs-lookup"><span data-stu-id="1c58d-144">**Property name:** `icon`</span></span>

<span data-ttu-id="1c58d-145">**Erfordernis:** Optional</span><span class="sxs-lookup"><span data-stu-id="1c58d-145">**Necessity:** Optional</span></span>

<span data-ttu-id="1c58d-146">**Akzeptiert:** Speicherort der Datei als Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="1c58d-146">**Accepts:** File location as a string</span></span>

### <a name="hide-a-profile-from-the-dropdown"></a><span data-ttu-id="1c58d-147">Ein Profil aus dem Dropdownmenü ausblenden</span><span class="sxs-lookup"><span data-stu-id="1c58d-147">Hide a profile from the dropdown</span></span>

<span data-ttu-id="1c58d-148">Wenn `hidden` auf `true` festgelegt ist, wird das Profil nicht in der Liste der Profile angezeigt.</span><span class="sxs-lookup"><span data-stu-id="1c58d-148">If `hidden` is set to `true`, the profile will not appear in the list of profiles.</span></span> <span data-ttu-id="1c58d-149">Dies kann verwendet werden, um Standardprofile und dynamisch generierte Profile auszublenden, während sie in der Einstellungsdatei beibehalten werden.</span><span class="sxs-lookup"><span data-stu-id="1c58d-149">This can be used to hide default profiles and dynamically generated profiles, while leaving them in your settings file.</span></span> <span data-ttu-id="1c58d-150">Weitere Informationen zu dynamischen Profilen finden Sie auf der Seite [Dynamische Profile](./../dynamic-profiles.md).</span><span class="sxs-lookup"><span data-stu-id="1c58d-150">To learn more about dynamic profiles, visit the [Dynamic profiles page](./../dynamic-profiles.md).</span></span>

<span data-ttu-id="1c58d-151">**Eigenschaftenname:** `hidden`</span><span class="sxs-lookup"><span data-stu-id="1c58d-151">**Property name:** `hidden`</span></span>

<span data-ttu-id="1c58d-152">**Erfordernis:** Optional</span><span class="sxs-lookup"><span data-stu-id="1c58d-152">**Necessity:** Optional</span></span>

<span data-ttu-id="1c58d-153">**Akzeptiert:** `true`, `false`</span><span class="sxs-lookup"><span data-stu-id="1c58d-153">**Accepts:** `true`, `false`</span></span>

<span data-ttu-id="1c58d-154">**Standardwert:** `false`</span><span class="sxs-lookup"><span data-stu-id="1c58d-154">**Default value:** `false`</span></span>

<br />

___

## <a name="tab-title-settings"></a><span data-ttu-id="1c58d-155">Einstellungen für Registerkartentitel</span><span class="sxs-lookup"><span data-stu-id="1c58d-155">Tab title settings</span></span>

### <a name="custom-tab-title"></a><span data-ttu-id="1c58d-156">Benutzerdefinierter Registerkartentitel</span><span class="sxs-lookup"><span data-stu-id="1c58d-156">Custom tab title</span></span>

<span data-ttu-id="1c58d-157">Wenn diese Einstellung festgelegt ist, ersetzt sie `name` als Titel, der beim Start an die Shell übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="1c58d-157">If set, this will replace the `name` as the title to pass to the shell on startup.</span></span> <span data-ttu-id="1c58d-158">Einige Shells (z. B. `bash`) können diesen Anfangswert möglicherweise ignorieren, während andere (`Command Prompt`, `PowerShell`) diesen Wert während der Lebensdauer der Anwendung verwenden.</span><span class="sxs-lookup"><span data-stu-id="1c58d-158">Some shells (like `bash`) may choose to ignore this initial value, while others (`Command Prompt`, `PowerShell`) may use this value over the lifetime of the application.</span></span> <span data-ttu-id="1c58d-159">Wenn Sie erfahren möchten, wie Sie Ihren Titel von der Shell festlegen lassen können, besuchen Sie das [Tutorial zu Registerkartentiteln](./../tutorials/tab-title.md).</span><span class="sxs-lookup"><span data-stu-id="1c58d-159">If you'd like to learn how to have the shell set your title, visit the [tab title tutorial](./../tutorials/tab-title.md).</span></span>

<span data-ttu-id="1c58d-160">**Eigenschaftenname:** `tabTitle`</span><span class="sxs-lookup"><span data-stu-id="1c58d-160">**Property name:** `tabTitle`</span></span>

<span data-ttu-id="1c58d-161">**Erfordernis:** Optional</span><span class="sxs-lookup"><span data-stu-id="1c58d-161">**Necessity:** Optional</span></span>

<span data-ttu-id="1c58d-162">**Akzeptiert:** Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="1c58d-162">**Accepts:** String</span></span>

### <a name="suppress-title-changes-from-the-shell"></a><span data-ttu-id="1c58d-163">Titeländerungen von der Shell unterdrücken</span><span class="sxs-lookup"><span data-stu-id="1c58d-163">Suppress title changes from the shell</span></span>

<span data-ttu-id="1c58d-164">Wenn dieser Wert auf `true` festgelegt ist, setzt `tabTitle` den Standardtitel der Registerkarte außer Kraft und alle Nachrichten von der Anwendung zur Titeländerung werden unterdrückt.</span><span class="sxs-lookup"><span data-stu-id="1c58d-164">When this is set to `true`, `tabTitle` overrides the default title of the tab and any title change messages from the application will be suppressed.</span></span> <span data-ttu-id="1c58d-165">Wenn `tabTitle` nicht festgelegt ist, wird stattdessen `name` verwendet.</span><span class="sxs-lookup"><span data-stu-id="1c58d-165">If `tabTitle` isn't set, `name` will be used instead.</span></span> <span data-ttu-id="1c58d-166">Wenn dies auf `false` festgelegt ist, verhält sich `tabTitle` normal.</span><span class="sxs-lookup"><span data-stu-id="1c58d-166">When this is set to `false`, `tabTitle` behaves as normal.</span></span>

<span data-ttu-id="1c58d-167">**Eigenschaftenname:** `suppressApplicationTitle`</span><span class="sxs-lookup"><span data-stu-id="1c58d-167">**Property name:** `suppressApplicationTitle`</span></span>

<span data-ttu-id="1c58d-168">**Erfordernis:** Optional</span><span class="sxs-lookup"><span data-stu-id="1c58d-168">**Necessity:** Optional</span></span>

<span data-ttu-id="1c58d-169">**Akzeptiert:** `true`, `false`</span><span class="sxs-lookup"><span data-stu-id="1c58d-169">**Accepts:** `true`, `false`</span></span>

<br />

___

## <a name="text-settings"></a><span data-ttu-id="1c58d-170">Texteinstellungen</span><span class="sxs-lookup"><span data-stu-id="1c58d-170">Text settings</span></span>

### <a name="font-face"></a><span data-ttu-id="1c58d-171">Schriftart</span><span class="sxs-lookup"><span data-stu-id="1c58d-171">Font face</span></span>

<span data-ttu-id="1c58d-172">Dies ist der Name der Schriftart, die im Profil verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="1c58d-172">This is the name of the font face used in the profile.</span></span> <span data-ttu-id="1c58d-173">Das Terminal versucht, alternativ Consolas zu verwenden, wenn diese Schriftart nicht gefunden werden kann oder ungültig ist.</span><span class="sxs-lookup"><span data-stu-id="1c58d-173">The terminal will try to fallback to Consolas if this can't be found or is invalid.</span></span> <span data-ttu-id="1c58d-174">Informationen zu den anderen Varianten der Standardschriftart, Cascadia Mono, finden Sie auf der [Cascadia Code-Seite](./../cascadia-code.md).</span><span class="sxs-lookup"><span data-stu-id="1c58d-174">To learn about the other variants of the default font, Cascadia Mono, visit the [Cascadia Code page](./../cascadia-code.md).</span></span>

<span data-ttu-id="1c58d-175">**Eigenschaftenname:** `fontFace`</span><span class="sxs-lookup"><span data-stu-id="1c58d-175">**Property name:** `fontFace`</span></span>

<span data-ttu-id="1c58d-176">**Erfordernis:** Optional</span><span class="sxs-lookup"><span data-stu-id="1c58d-176">**Necessity:** Optional</span></span>

<span data-ttu-id="1c58d-177">**Akzeptiert:** Schriftartname als Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="1c58d-177">**Accepts:** Font name as a string</span></span>

<span data-ttu-id="1c58d-178">**Standardwert:** `"Cascadia Mono"`</span><span class="sxs-lookup"><span data-stu-id="1c58d-178">**Default value:** `"Cascadia Mono"`</span></span>

### <a name="font-size"></a><span data-ttu-id="1c58d-179">Schriftgrad</span><span class="sxs-lookup"><span data-stu-id="1c58d-179">Font size</span></span>

<span data-ttu-id="1c58d-180">Hiermit wird der Schriftgrad des Profils in Punkt festgelegt.</span><span class="sxs-lookup"><span data-stu-id="1c58d-180">This sets the profile's font size in points.</span></span>

<span data-ttu-id="1c58d-181">**Eigenschaftenname:** `fontSize`</span><span class="sxs-lookup"><span data-stu-id="1c58d-181">**Property name:** `fontSize`</span></span>

<span data-ttu-id="1c58d-182">**Erfordernis:** Optional</span><span class="sxs-lookup"><span data-stu-id="1c58d-182">**Necessity:** Optional</span></span>

<span data-ttu-id="1c58d-183">**Akzeptiert:** Ganze Zahl</span><span class="sxs-lookup"><span data-stu-id="1c58d-183">**Accepts:** Integer</span></span>

<span data-ttu-id="1c58d-184">**Standardwert:** `12`</span><span class="sxs-lookup"><span data-stu-id="1c58d-184">**Default value:** `12`</span></span>

### <a name="padding"></a><span data-ttu-id="1c58d-185">Abstand</span><span class="sxs-lookup"><span data-stu-id="1c58d-185">Padding</span></span>

:::row:::
:::column span="":::
<span data-ttu-id="1c58d-186">Hiermit wird der Abstand um den Text im Fenster festgelegt.</span><span class="sxs-lookup"><span data-stu-id="1c58d-186">This sets the padding around the text within the window.</span></span> <span data-ttu-id="1c58d-187">Dabei werden drei verschiedene Formate akzeptiert: `"#"` legt denselben Abstand für alle Seiten fest, `"#, #"` legt denselben Abstand für links-rechts und oben-unten fest, und `"#, #, #, #"` legt den Abstand individuell für links, oben, rechts und unten fest.</span><span class="sxs-lookup"><span data-stu-id="1c58d-187">This will accept three different formats: `"#"` sets the same padding for all sides, `"#, #"` sets the same padding for left-right and top-bottom, and `"#, #, #, #"` sets the padding individually for left, top, right, and bottom.</span></span>

<span data-ttu-id="1c58d-188">**Eigenschaftenname:** `padding`</span><span class="sxs-lookup"><span data-stu-id="1c58d-188">**Property name:** `padding`</span></span>

<span data-ttu-id="1c58d-189">**Erfordernis:** Optional</span><span class="sxs-lookup"><span data-stu-id="1c58d-189">**Necessity:** Optional</span></span>

<span data-ttu-id="1c58d-190">**Akzeptiert:** Werte als Zeichenfolge in den folgenden Formaten: `"#"`, `"#, #"`, `"#, #, #, #"`</span><span class="sxs-lookup"><span data-stu-id="1c58d-190">**Accepts:** Values as a string in the following formats: `"#"`, `"#, #"`, `"#, #, #, #"`</span></span>

<span data-ttu-id="1c58d-191">**Standardwert:** `"8, 8, 8, 8"`</span><span class="sxs-lookup"><span data-stu-id="1c58d-191">**Default value:** `"8, 8, 8, 8"`</span></span>

:::column-end:::
:::column span="":::
![Windows Terminal-Abstand](./../images/padding.gif)

:::column-end:::
:::row-end:::

### <a name="antialiasing-text"></a><span data-ttu-id="1c58d-193">Antialiasing bei Text</span><span class="sxs-lookup"><span data-stu-id="1c58d-193">Antialiasing text</span></span>

<span data-ttu-id="1c58d-194">Hiermit wird gesteuert, wie das Antialiasing bei Text im Renderer erfolgt.</span><span class="sxs-lookup"><span data-stu-id="1c58d-194">This controls how text is antialiased in the renderer.</span></span> <span data-ttu-id="1c58d-195">Beachten Sie, dass das Ändern dieser Einstellung das Starten einer neuen Terminalinstanz erfordert.</span><span class="sxs-lookup"><span data-stu-id="1c58d-195">Note that changing this setting will require starting a new terminal instance.</span></span>

![Windows Terminal: Antialiasing bei Text](./../images/antialiasing-mode.gif)

<span data-ttu-id="1c58d-197">**Eigenschaftenname:** `antialiasingMode`</span><span class="sxs-lookup"><span data-stu-id="1c58d-197">**Property name:** `antialiasingMode`</span></span>

<span data-ttu-id="1c58d-198">**Erfordernis:** Optional</span><span class="sxs-lookup"><span data-stu-id="1c58d-198">**Necessity:** Optional</span></span>

<span data-ttu-id="1c58d-199">**Akzeptiert:** `"grayscale"`, `"cleartype"`, `"aliased"`</span><span class="sxs-lookup"><span data-stu-id="1c58d-199">**Accepts:** `"grayscale"`, `"cleartype"`, `"aliased"`</span></span>

<span data-ttu-id="1c58d-200">**Standardwert:** `"grayscale"`</span><span class="sxs-lookup"><span data-stu-id="1c58d-200">**Default value:** `"grayscale"`</span></span>

<br />

___

## <a name="cursor-settings"></a><span data-ttu-id="1c58d-201">Cursoreinstellungen</span><span class="sxs-lookup"><span data-stu-id="1c58d-201">Cursor settings</span></span>

### <a name="cursor-shape"></a><span data-ttu-id="1c58d-202">Cursorform</span><span class="sxs-lookup"><span data-stu-id="1c58d-202">Cursor shape</span></span>

<span data-ttu-id="1c58d-203">Hiermit wird die Cursorform für das Profil festgelegt.</span><span class="sxs-lookup"><span data-stu-id="1c58d-203">This sets the cursor shape for the profile.</span></span> <span data-ttu-id="1c58d-204">Mögliche Cursor: `"bar"` (&#x2503;), `"vintage"` (&#x2583;), `"underscore"` (&#x2581;), `"filledBox"` (&#x2588;), `"emptyBox"` (&#x25AF;)</span><span class="sxs-lookup"><span data-stu-id="1c58d-204">The possible cursors are as follows: `"bar"` ( &#x2503; ), `"vintage"` ( &#x2583; ), `"underscore"` ( &#x2581; ), `"filledBox"` ( &#x2588; ), `"emptyBox"` ( &#x25AF; )</span></span>

<span data-ttu-id="1c58d-205">**Eigenschaftenname:** `cursorShape`</span><span class="sxs-lookup"><span data-stu-id="1c58d-205">**Property name:** `cursorShape`</span></span>

<span data-ttu-id="1c58d-206">**Erfordernis:** Optional</span><span class="sxs-lookup"><span data-stu-id="1c58d-206">**Necessity:** Optional</span></span>

<span data-ttu-id="1c58d-207">**Akzeptiert:** `"bar"`, `"vintage"`, `"underscore"`, `"filledBox"`, `"emptyBox"`</span><span class="sxs-lookup"><span data-stu-id="1c58d-207">**Accepts:** `"bar"`, `"vintage"`, `"underscore"`, `"filledBox"`, `"emptyBox"`</span></span>

<span data-ttu-id="1c58d-208">**Standardwert:** `"bar"`</span><span class="sxs-lookup"><span data-stu-id="1c58d-208">**Default value:** `"bar"`</span></span>

### <a name="cursor-color"></a><span data-ttu-id="1c58d-209">Cursorfarbe</span><span class="sxs-lookup"><span data-stu-id="1c58d-209">Cursor color</span></span>

<span data-ttu-id="1c58d-210">Hiermit wird die Cursorfarbe für das Profil festgelegt.</span><span class="sxs-lookup"><span data-stu-id="1c58d-210">This sets the cursor color of the profile.</span></span> <span data-ttu-id="1c58d-211">Hiermit wird das im Farbschema festgelegte `cursorColor` außer Kraft gesetzt, wenn `colorScheme` festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="1c58d-211">This will override the `cursorColor` set in the color scheme if `colorScheme` is set.</span></span>

<span data-ttu-id="1c58d-212">**Eigenschaftenname:** `cursorColor`</span><span class="sxs-lookup"><span data-stu-id="1c58d-212">**Property name:** `cursorColor`</span></span>

<span data-ttu-id="1c58d-213">**Erfordernis:** Optional</span><span class="sxs-lookup"><span data-stu-id="1c58d-213">**Necessity:** Optional</span></span>

<span data-ttu-id="1c58d-214">**Akzeptiert:** Farbe als Zeichenfolge im Hexadezimalformat: `"#rgb"` oder `"#rrggbb"`</span><span class="sxs-lookup"><span data-stu-id="1c58d-214">**Accepts:** Color as a string in hex format: `"#rgb"` or `"#rrggbb"`</span></span>

### <a name="cursor-height"></a><span data-ttu-id="1c58d-215">Cursorhöhe</span><span class="sxs-lookup"><span data-stu-id="1c58d-215">Cursor height</span></span>

<span data-ttu-id="1c58d-216">Hiermit wird die prozentuale Höhe des Cursors ab dem unteren Rand festgelegt.</span><span class="sxs-lookup"><span data-stu-id="1c58d-216">This sets the percentage height of the cursor starting from the bottom.</span></span> <span data-ttu-id="1c58d-217">Dies funktioniert nur, wenn `cursorShape` auf `"vintage"` festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="1c58d-217">This will only work when `cursorShape` is set to `"vintage"`.</span></span>

<span data-ttu-id="1c58d-218">**Eigenschaftenname:** `cursorHeight`</span><span class="sxs-lookup"><span data-stu-id="1c58d-218">**Property name:** `cursorHeight`</span></span>

<span data-ttu-id="1c58d-219">**Erfordernis:** Optional</span><span class="sxs-lookup"><span data-stu-id="1c58d-219">**Necessity:** Optional</span></span>

<span data-ttu-id="1c58d-220">**Akzeptiert:** Ganzzahl zwischen 25 und 100</span><span class="sxs-lookup"><span data-stu-id="1c58d-220">**Accepts:** Integer from 25-100</span></span>

<br />

___

## <a name="color-settings"></a><span data-ttu-id="1c58d-221">Farbeinstellungen</span><span class="sxs-lookup"><span data-stu-id="1c58d-221">Color settings</span></span>

### <a name="color-scheme"></a><span data-ttu-id="1c58d-222">Farbschema</span><span class="sxs-lookup"><span data-stu-id="1c58d-222">Color scheme</span></span>

<span data-ttu-id="1c58d-223">Dies ist der Name des Farbschemas, das im Profil verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="1c58d-223">This is the name of the color scheme used in the profile.</span></span> <span data-ttu-id="1c58d-224">Farbschemas werden im `schemes`-Objekt definiert.</span><span class="sxs-lookup"><span data-stu-id="1c58d-224">Color schemes are defined in the `schemes` object.</span></span> <span data-ttu-id="1c58d-225">Ausführlichere Informationen finden Sie auf der Seite [Farbschemas](./color-schemes.md).</span><span class="sxs-lookup"><span data-stu-id="1c58d-225">More detailed information can be found on the [Color schemes page](./color-schemes.md).</span></span>

<span data-ttu-id="1c58d-226">**Eigenschaftenname:** `colorScheme`</span><span class="sxs-lookup"><span data-stu-id="1c58d-226">**Property name:** `colorScheme`</span></span>

<span data-ttu-id="1c58d-227">**Erfordernis:** Optional</span><span class="sxs-lookup"><span data-stu-id="1c58d-227">**Necessity:** Optional</span></span>

<span data-ttu-id="1c58d-228">**Akzeptiert:** Name des Farbschemas als Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="1c58d-228">**Accepts:** Name of color scheme as a string</span></span>

<span data-ttu-id="1c58d-229">**Standardwert:** `"Campbell"`</span><span class="sxs-lookup"><span data-stu-id="1c58d-229">**Default value:** `"Campbell"`</span></span>

### <a name="foreground-color"></a><span data-ttu-id="1c58d-230">Vordergrundfarbe</span><span class="sxs-lookup"><span data-stu-id="1c58d-230">Foreground color</span></span>

<span data-ttu-id="1c58d-231">Hiermit wird die Vordergrundfarbe des Profils geändert.</span><span class="sxs-lookup"><span data-stu-id="1c58d-231">This changes the foreground color of the profile.</span></span> <span data-ttu-id="1c58d-232">Hiermit wird das im Farbschema festgelegte `foreground` außer Kraft gesetzt, wenn `colorScheme` festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="1c58d-232">This overrides `foreground` set in the color scheme if `colorScheme` is set.</span></span>

<span data-ttu-id="1c58d-233">**Eigenschaftenname:** `foreground`</span><span class="sxs-lookup"><span data-stu-id="1c58d-233">**Property name:** `foreground`</span></span>

<span data-ttu-id="1c58d-234">**Erfordernis:** Optional</span><span class="sxs-lookup"><span data-stu-id="1c58d-234">**Necessity:** Optional</span></span>

<span data-ttu-id="1c58d-235">**Akzeptiert:** Farbe als Zeichenfolge im Hexadezimalformat: `"#rgb"` oder `"#rrggbb"`</span><span class="sxs-lookup"><span data-stu-id="1c58d-235">**Accepts:** Color as a string in hex format: `"#rgb"` or `"#rrggbb"`</span></span>

### <a name="background-color"></a><span data-ttu-id="1c58d-236">Hintergrundfarbe</span><span class="sxs-lookup"><span data-stu-id="1c58d-236">Background color</span></span>

<span data-ttu-id="1c58d-237">Hiermit wird die Hintergrundfarbe des Profils mit dieser Einstellung geändert.</span><span class="sxs-lookup"><span data-stu-id="1c58d-237">This changes the background color of the profile with this setting.</span></span> <span data-ttu-id="1c58d-238">Hiermit wird das im Farbschema festgelegte `background` außer Kraft gesetzt, wenn `colorScheme` festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="1c58d-238">This overrides `background` set in the color scheme if `colorScheme` is set.</span></span>

<span data-ttu-id="1c58d-239">**Eigenschaftenname:** `background`</span><span class="sxs-lookup"><span data-stu-id="1c58d-239">**Property name:** `background`</span></span>

<span data-ttu-id="1c58d-240">**Erfordernis:** Optional</span><span class="sxs-lookup"><span data-stu-id="1c58d-240">**Necessity:** Optional</span></span>

<span data-ttu-id="1c58d-241">**Akzeptiert:** Farbe als Zeichenfolge im Hexadezimalformat: `"#rgb"` oder `"#rrggbb"`</span><span class="sxs-lookup"><span data-stu-id="1c58d-241">**Accepts:** Color as a string in hex format: `"#rgb"` or `"#rrggbb"`</span></span>

### <a name="selection-background-color"></a><span data-ttu-id="1c58d-242">Auswahlhintergrundfarbe</span><span class="sxs-lookup"><span data-stu-id="1c58d-242">Selection background color</span></span>

<span data-ttu-id="1c58d-243">Hiermit wird die Hintergrundfarbe einer Auswahl im Profil festgelegt.</span><span class="sxs-lookup"><span data-stu-id="1c58d-243">This sets the background color of a selection within the profile.</span></span> <span data-ttu-id="1c58d-244">Hiermit wird das im Farbschema festgelegte `selectionBackground` außer Kraft gesetzt, wenn `colorScheme` festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="1c58d-244">This will override the `selectionBackground` set in the color scheme if `colorScheme` is set.</span></span>

<span data-ttu-id="1c58d-245">**Eigenschaftenname:** `selectionBackground`</span><span class="sxs-lookup"><span data-stu-id="1c58d-245">**Property name:** `selectionBackground`</span></span>

<span data-ttu-id="1c58d-246">**Erfordernis:** Optional</span><span class="sxs-lookup"><span data-stu-id="1c58d-246">**Necessity:** Optional</span></span>

<span data-ttu-id="1c58d-247">**Akzeptiert:** Farbe als Zeichenfolge im Hexadezimalformat: `"#rgb"` oder `"#rrggbb"`</span><span class="sxs-lookup"><span data-stu-id="1c58d-247">**Accepts:** Color as a string in hex format: `"#rgb"` or `"#rrggbb"`</span></span>

<br />

___

## <a name="acrylic-settings"></a><span data-ttu-id="1c58d-248">Acryleinstellungen</span><span class="sxs-lookup"><span data-stu-id="1c58d-248">Acrylic settings</span></span>

### <a name="enable-acrylic"></a><span data-ttu-id="1c58d-249">Acryl aktivieren</span><span class="sxs-lookup"><span data-stu-id="1c58d-249">Enable acrylic</span></span>

:::row:::
:::column span="":::
<span data-ttu-id="1c58d-250">Wenn dies auf `true` festgelegt ist, hat das Fenster einen Acrylhintergrund.</span><span class="sxs-lookup"><span data-stu-id="1c58d-250">When this is set to `true`, the window will have an acrylic background.</span></span> <span data-ttu-id="1c58d-251">Wenn es auf `false` festgelegt ist, hat das Fenster einen einfachen, Hintergrund ohne Textur.</span><span class="sxs-lookup"><span data-stu-id="1c58d-251">When it's set to `false`, the window will have a plain, untextured background.</span></span> <span data-ttu-id="1c58d-252">Die Transparenz gilt aufgrund von Betriebssystemeinschränkungen nur für Fenster mit Fokus.</span><span class="sxs-lookup"><span data-stu-id="1c58d-252">The transparency only applies to focused windows due to OS limitations.</span></span>

<span data-ttu-id="1c58d-253">**Eigenschaftenname:** `useAcrylic`</span><span class="sxs-lookup"><span data-stu-id="1c58d-253">**Property name:** `useAcrylic`</span></span>

<span data-ttu-id="1c58d-254">**Erfordernis:** Optional</span><span class="sxs-lookup"><span data-stu-id="1c58d-254">**Necessity:** Optional</span></span>

<span data-ttu-id="1c58d-255">**Akzeptiert:** `true`, `false`</span><span class="sxs-lookup"><span data-stu-id="1c58d-255">**Accepts:** `true`, `false`</span></span>

<span data-ttu-id="1c58d-256">**Standardwert:** `false`</span><span class="sxs-lookup"><span data-stu-id="1c58d-256">**Default value:** `false`</span></span>

:::column-end:::
:::column span="":::
![Windows Terminal: Acryl](./../images/acrylic.gif)

:::column-end:::
:::row-end:::

### <a name="acrylic-opacity"></a><span data-ttu-id="1c58d-258">Acryldeckkraft</span><span class="sxs-lookup"><span data-stu-id="1c58d-258">Acrylic opacity</span></span>

:::row:::
:::column span="":::
<span data-ttu-id="1c58d-259">Wenn `useAcrylic` auf `true` festgelegt ist, wird die Transparenz des Fensters für das Profil festgelegt.</span><span class="sxs-lookup"><span data-stu-id="1c58d-259">When `useAcrylic` is set to `true`, this sets the transparency of the window for the profile.</span></span> <span data-ttu-id="1c58d-260">Hierbei werden Gleitkommazahlen zwischen 0 und 1 akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="1c58d-260">This accepts floating point values from 0-1.</span></span>

<span data-ttu-id="1c58d-261">**Eigenschaftenname:** `acrylicOpacity`</span><span class="sxs-lookup"><span data-stu-id="1c58d-261">**Property name:** `acrylicOpacity`</span></span>

<span data-ttu-id="1c58d-262">**Erfordernis:** Optional</span><span class="sxs-lookup"><span data-stu-id="1c58d-262">**Necessity:** Optional</span></span>

<span data-ttu-id="1c58d-263">**Akzeptiert:** Zahl als Gleitkommawert zwischen 0 und 1</span><span class="sxs-lookup"><span data-stu-id="1c58d-263">**Accepts:** Number as a floating point value from 0-1</span></span>

<span data-ttu-id="1c58d-264">**Standardwert:** `0.5`</span><span class="sxs-lookup"><span data-stu-id="1c58d-264">**Default value:** `0.5`</span></span>

:::column-end:::
:::column span="":::
![Windows Terminal: Acryldeckkraft](./../images/acrylic-opacity.gif)

:::column-end:::
:::row-end:::

<br />

___

## <a name="background-image-settings"></a><span data-ttu-id="1c58d-266">Hintergrundbildeinstellungen</span><span class="sxs-lookup"><span data-stu-id="1c58d-266">Background image settings</span></span>

### <a name="setting-the-background-image"></a><span data-ttu-id="1c58d-267">Hintergrundbild festlegen</span><span class="sxs-lookup"><span data-stu-id="1c58d-267">Setting the background image</span></span>

<span data-ttu-id="1c58d-268">Hiermit wird der Dateispeicherort des Bilds festgelegt, das über den Fensterhintergrund gezeichnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="1c58d-268">This sets the file location of the image to draw over the window background.</span></span> <span data-ttu-id="1c58d-269">Bei dem Hintergrundbild kann es sich um eine JPG-, PNG- oder GIF-Datei handeln.</span><span class="sxs-lookup"><span data-stu-id="1c58d-269">The background image can be a .jpg, .png, or .gif file.</span></span>

<span data-ttu-id="1c58d-270">**Eigenschaftenname:** `backgroundImage`</span><span class="sxs-lookup"><span data-stu-id="1c58d-270">**Property name:** `backgroundImage`</span></span>

<span data-ttu-id="1c58d-271">**Erfordernis:** Optional</span><span class="sxs-lookup"><span data-stu-id="1c58d-271">**Necessity:** Optional</span></span>

<span data-ttu-id="1c58d-272">**Akzeptiert:** Speicherort der Datei als Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="1c58d-272">**Accepts:** File location as a string</span></span>

### <a name="background-image-stretch-mode"></a><span data-ttu-id="1c58d-273">Streckmodus für Hintergrundbild</span><span class="sxs-lookup"><span data-stu-id="1c58d-273">Background image stretch mode</span></span>

:::row:::
:::column span="":::
<span data-ttu-id="1c58d-274">Hiermit wird festgelegt, wie die Größe des Hintergrundbilds geändert wird, um das Fenster auszufüllen.</span><span class="sxs-lookup"><span data-stu-id="1c58d-274">This sets how the background image is resized to fill the window.</span></span>

<span data-ttu-id="1c58d-275">**Eigenschaftenname:** `backgroundImageStretchMode`</span><span class="sxs-lookup"><span data-stu-id="1c58d-275">**Property name:** `backgroundImageStretchMode`</span></span>

<span data-ttu-id="1c58d-276">**Erfordernis:** Optional</span><span class="sxs-lookup"><span data-stu-id="1c58d-276">**Necessity:** Optional</span></span>

<span data-ttu-id="1c58d-277">**Akzeptiert:** `"none"`, `"fill"`, `"uniform"`, `"uniformToFill"`</span><span class="sxs-lookup"><span data-stu-id="1c58d-277">**Accepts:** `"none"`, `"fill"`, `"uniform"`, `"uniformToFill"`</span></span>

<span data-ttu-id="1c58d-278">**Standardwert:** `"uniformToFill"`</span><span class="sxs-lookup"><span data-stu-id="1c58d-278">**Default value:** `"uniformToFill"`</span></span>

:::column-end:::
:::column span="":::
<span data-ttu-id="1c58d-279">![Windows Terminal: Streckmodus für Hintergrundbild](./../images/background-image-stretch-mode.gif)
 _[Hintergrundbildquelle](https://wallpaperhub.app/wallpapers/6287)_</span><span class="sxs-lookup"><span data-stu-id="1c58d-279">![Windows Terminal background image stretch mode](./../images/background-image-stretch-mode.gif)
_[Background image source](https://wallpaperhub.app/wallpapers/6287)_</span></span>

:::column-end:::
:::row-end:::

### <a name="background-image-alignment"></a><span data-ttu-id="1c58d-280">Hintergrundbildausrichtung</span><span class="sxs-lookup"><span data-stu-id="1c58d-280">Background image alignment</span></span>

:::row:::
:::column span="":::
<span data-ttu-id="1c58d-281">Hiermit wird festgelegt, wie das Hintergrundbild an den Fensterbegrenzungen ausgerichtet wird.</span><span class="sxs-lookup"><span data-stu-id="1c58d-281">This sets how the background image aligns to the boundaries of the window.</span></span>

<span data-ttu-id="1c58d-282">**Eigenschaftenname:** `backgroundImageAlignment`</span><span class="sxs-lookup"><span data-stu-id="1c58d-282">**Property name:** `backgroundImageAlignment`</span></span>

<span data-ttu-id="1c58d-283">**Erfordernis:** Optional</span><span class="sxs-lookup"><span data-stu-id="1c58d-283">**Necessity:** Optional</span></span>

<span data-ttu-id="1c58d-284">**Akzeptiert:** `"center"`, `"left"`, `"top"`, `"right"`, `"bottom"`, `"topLeft"`, `"topRight"`, `"bottomLeft"`, `"bottomRight"`</span><span class="sxs-lookup"><span data-stu-id="1c58d-284">**Accepts:** `"center"`, `"left"`, `"top"`, `"right"`, `"bottom"`, `"topLeft"`, `"topRight"`, `"bottomLeft"`, `"bottomRight"`</span></span>

<span data-ttu-id="1c58d-285">**Standardwert:** `"center"`</span><span class="sxs-lookup"><span data-stu-id="1c58d-285">**Default value:** `"center"`</span></span>

:::column-end:::
:::column span="":::
<span data-ttu-id="1c58d-286">![Windows Terminal: Hintergrundbildausrichtung](./../images/background-image-alignment.gif)
 _[Hintergrundbildquelle](https://design.ubuntu.com/brand/ubuntu-logo/)_</span><span class="sxs-lookup"><span data-stu-id="1c58d-286">![Windows Terminal background image alignment](./../images/background-image-alignment.gif)
_[Background image source](https://design.ubuntu.com/brand/ubuntu-logo/)_</span></span>

:::column-end:::
:::row-end:::

### <a name="background-image-opacity"></a><span data-ttu-id="1c58d-287">Hintergrundbilddeckkraft</span><span class="sxs-lookup"><span data-stu-id="1c58d-287">Background image opacity</span></span>

:::row:::
:::column span="":::
<span data-ttu-id="1c58d-288">Hiermit wird die Transparenz des Hintergrundbilds festgelegt.</span><span class="sxs-lookup"><span data-stu-id="1c58d-288">This sets the transparency of the background image.</span></span>

:::column-end:::
:::row-end:::

<span data-ttu-id="1c58d-289">**Eigenschaftenname:** `backgroundImageOpacity`</span><span class="sxs-lookup"><span data-stu-id="1c58d-289">**Property name:** `backgroundImageOpacity`</span></span>

<span data-ttu-id="1c58d-290">**Erfordernis:** Optional</span><span class="sxs-lookup"><span data-stu-id="1c58d-290">**Necessity:** Optional</span></span>

<span data-ttu-id="1c58d-291">**Akzeptiert:** Zahl als Gleitkommawert zwischen 0 und 1</span><span class="sxs-lookup"><span data-stu-id="1c58d-291">**Accepts:** Number as a floating point value from 0-1</span></span>

<span data-ttu-id="1c58d-292">**Standardwert:** `1.0`</span><span class="sxs-lookup"><span data-stu-id="1c58d-292">**Default value:** `1.0`</span></span>

<br />

___

## <a name="scroll-settings"></a><span data-ttu-id="1c58d-293">Scrolleinstellungen</span><span class="sxs-lookup"><span data-stu-id="1c58d-293">Scroll settings</span></span>

### <a name="scrollbar-visibility"></a><span data-ttu-id="1c58d-294">Sichtbarkeit der Scrollleiste</span><span class="sxs-lookup"><span data-stu-id="1c58d-294">Scrollbar visibility</span></span>

<span data-ttu-id="1c58d-295">Hiermit wird die Sichtbarkeit der Scrollleiste festgelegt.</span><span class="sxs-lookup"><span data-stu-id="1c58d-295">This sets the visibility of the scrollbar.</span></span>

<span data-ttu-id="1c58d-296">**Eigenschaftenname:** `scrollbarState`</span><span class="sxs-lookup"><span data-stu-id="1c58d-296">**Property name:** `scrollbarState`</span></span>

<span data-ttu-id="1c58d-297">**Erfordernis:** Optional</span><span class="sxs-lookup"><span data-stu-id="1c58d-297">**Necessity:** Optional</span></span>

<span data-ttu-id="1c58d-298">**Akzeptiert:** `"visible"`, `"hidden"`</span><span class="sxs-lookup"><span data-stu-id="1c58d-298">**Accepts:** `"visible"`, `"hidden"`</span></span>

### <a name="scroll-to-input-line-when-typing"></a><span data-ttu-id="1c58d-299">Beim Eingeben zur Eingabezeile scrollen</span><span class="sxs-lookup"><span data-stu-id="1c58d-299">Scroll to input line when typing</span></span>

<span data-ttu-id="1c58d-300">Wenn dies auf `true` festgelegt ist, scrollt das Fenster bei der Eingabe zur Befehlseingabezeile.</span><span class="sxs-lookup"><span data-stu-id="1c58d-300">When this is set to `true`, the window will scroll to the command input line when typing.</span></span> <span data-ttu-id="1c58d-301">Wenn es auf `false` festgelegt ist, scrollt das Fenster bei der Eingabe nicht.</span><span class="sxs-lookup"><span data-stu-id="1c58d-301">When it's set to `false`, the window will not scroll when you start typing.</span></span>

<span data-ttu-id="1c58d-302">**Eigenschaftenname:** `snapOnInput`</span><span class="sxs-lookup"><span data-stu-id="1c58d-302">**Property name:** `snapOnInput`</span></span>

<span data-ttu-id="1c58d-303">**Erfordernis:** Optional</span><span class="sxs-lookup"><span data-stu-id="1c58d-303">**Necessity:** Optional</span></span>

<span data-ttu-id="1c58d-304">**Akzeptiert:** `true`, `false`</span><span class="sxs-lookup"><span data-stu-id="1c58d-304">**Accepts:** `true`, `false`</span></span>

<span data-ttu-id="1c58d-305">**Standardwert:** `true`</span><span class="sxs-lookup"><span data-stu-id="1c58d-305">**Default value:** `true`</span></span>

### <a name="history-size"></a><span data-ttu-id="1c58d-306">Verlaufsgröße</span><span class="sxs-lookup"><span data-stu-id="1c58d-306">History size</span></span>

<span data-ttu-id="1c58d-307">Hiermit wird die Anzahl der Zeilen über den Zeilen festgelegt, die in dem Fenster angezeigt werden, zu dem Sie zurückscrollen können.</span><span class="sxs-lookup"><span data-stu-id="1c58d-307">This sets the number of lines above the ones displayed in the window you can scroll back to.</span></span>

<span data-ttu-id="1c58d-308">**Eigenschaftenname:** `historySize`</span><span class="sxs-lookup"><span data-stu-id="1c58d-308">**Property name:** `historySize`</span></span>

<span data-ttu-id="1c58d-309">**Erfordernis:** Optional</span><span class="sxs-lookup"><span data-stu-id="1c58d-309">**Necessity:** Optional</span></span>

<span data-ttu-id="1c58d-310">**Akzeptiert:** Ganze Zahl</span><span class="sxs-lookup"><span data-stu-id="1c58d-310">**Accepts:** Integer</span></span>

<span data-ttu-id="1c58d-311">**Standardwert:** `9001`</span><span class="sxs-lookup"><span data-stu-id="1c58d-311">**Default value:** `9001`</span></span>

<br />

___

## <a name="how-the-profile-closes-when-exiting"></a><span data-ttu-id="1c58d-312">Wie das Profil beim Verlassen geschlossen wird</span><span class="sxs-lookup"><span data-stu-id="1c58d-312">How the profile closes when exiting</span></span>

<span data-ttu-id="1c58d-313">Hiermit wird festgelegt, wie das Profil auf einen Abbruch oder einen fehlerhaften Start reagiert.</span><span class="sxs-lookup"><span data-stu-id="1c58d-313">This sets how the profile reacts to termination or failure to launch.</span></span> <span data-ttu-id="1c58d-314">`"graceful"` schließt das Profil, wenn `exit` eingegeben oder der Prozess normal beendet wird.</span><span class="sxs-lookup"><span data-stu-id="1c58d-314">`"graceful"` will close the profile when `exit` is typed or when the process exits normally.</span></span> <span data-ttu-id="1c58d-315">`"always"` schließt das Profil immer und `"never"` schließt das Profil nie.</span><span class="sxs-lookup"><span data-stu-id="1c58d-315">`"always"` will always close the profile and `"never"` will never close the profile.</span></span> <span data-ttu-id="1c58d-316">`true` und `false` werden als Synonyme für `"graceful"` bzw. `"never"` akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="1c58d-316">`true` and `false` are accepted as synonyms for `"graceful"` and `"never"`, respectively.</span></span>

<span data-ttu-id="1c58d-317">**Eigenschaftenname:** `closeOnExit`</span><span class="sxs-lookup"><span data-stu-id="1c58d-317">**Property name:** `closeOnExit`</span></span>

<span data-ttu-id="1c58d-318">**Erfordernis:** Optional</span><span class="sxs-lookup"><span data-stu-id="1c58d-318">**Necessity:** Optional</span></span>

<span data-ttu-id="1c58d-319">**Akzeptiert:** `"graceful"`, `"always"`, `"never"`, `true`, `false`</span><span class="sxs-lookup"><span data-stu-id="1c58d-319">**Accepts:** `"graceful"`, `"always"`, `"never"`, `true`, `false`</span></span>

<span data-ttu-id="1c58d-320">**Standardwert:** `"graceful"`</span><span class="sxs-lookup"><span data-stu-id="1c58d-320">**Default value:** `"graceful"`</span></span>

<br />

___

## <a name="retro-terminal-effects"></a><span data-ttu-id="1c58d-321">Terminaleffekte im Retrostil</span><span class="sxs-lookup"><span data-stu-id="1c58d-321">Retro terminal effects</span></span>

:::row:::
:::column span="":::
<span data-ttu-id="1c58d-322">Wenn dieser Wert auf `true` festgelegt ist, emuliert das Terminal einen klassischen CRT-Bildschirm mit Scan-Linien und unscharfen Textkanten.</span><span class="sxs-lookup"><span data-stu-id="1c58d-322">When this is set to `true`, the terminal will emulate a classic CRT display with scan lines and blurry text edges.</span></span> <span data-ttu-id="1c58d-323">Hierbei handelt es sich um ein experimentelles Feature, dessen Weiterbestehen nicht garantiert ist.</span><span class="sxs-lookup"><span data-stu-id="1c58d-323">This is an experimental feature and its continued existence is not guaranteed.</span></span>

<span data-ttu-id="1c58d-324">**Eigenschaftenname:** `experimental.retroTerminalEffect`</span><span class="sxs-lookup"><span data-stu-id="1c58d-324">**Property name:** `experimental.retroTerminalEffect`</span></span>

<span data-ttu-id="1c58d-325">**Erfordernis:** Optional</span><span class="sxs-lookup"><span data-stu-id="1c58d-325">**Necessity:** Optional</span></span>

<span data-ttu-id="1c58d-326">**Akzeptiert:** `true`, `false`</span><span class="sxs-lookup"><span data-stu-id="1c58d-326">**Accepts:** `true`, `false`</span></span>

<span data-ttu-id="1c58d-327">**Standardwert:** `false`</span><span class="sxs-lookup"><span data-stu-id="1c58d-327">**Default value:** `false`</span></span>

:::column-end:::
:::column span="":::
<span data-ttu-id="1c58d-328">![Windows Terminal: Experimenteller Terminaleffekt im Retrostil](./../images/experimental-retro-terminal-effect.gif)
_Konfiguration: [Eingabeaufforderung im Retrostil](./../custom-terminal-gallery/retro-command-prompt.md)_</span><span class="sxs-lookup"><span data-stu-id="1c58d-328">![Windows Terminal experimental retro terminal effect](./../images/experimental-retro-terminal-effect.gif)
_Configuration: [Retro Command Prompt](./../custom-terminal-gallery/retro-command-prompt.md)_</span></span>

:::column-end:::
:::row-end:::
