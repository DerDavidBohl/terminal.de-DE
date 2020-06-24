---
title: Windows Terminal-Profileinstellungen
description: Erfahren Sie, wie die einzelnen Profile in Windows Terminal angepasst werden.
author: cinnamon-msft
ms.author: cinnamon
ms.date: 06/18/2020
ms.topic: how-to
ms.service: terminal
ms.localizationpriority: high
ms.openlocfilehash: ad7121f9cd6583562c03bf0e35d2928f46fe5d91
ms.sourcegitcommit: 91a802863cd0730d2e364377ffe44f819a66ff2a
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/18/2020
ms.locfileid: "84994393"
---
# <a name="profile-settings-in-windows-terminal"></a><span data-ttu-id="73963-103">Profileinstellungen in Windows Terminal</span><span class="sxs-lookup"><span data-stu-id="73963-103">Profile settings in Windows Terminal</span></span>

<span data-ttu-id="73963-104">Die unten aufgeführten Einstellungen sind spezifisch für die einzelnen eindeutigen Profile.</span><span class="sxs-lookup"><span data-stu-id="73963-104">The settings listed below are specific to each unique profile.</span></span> <span data-ttu-id="73963-105">Wenn Sie möchten, dass eine Einstellung auf alle Profile angewendet wird, können Sie sie dem Abschnitt `defaults` über der Profilliste in der Datei „settings.json“ hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="73963-105">If you'd like a setting to apply to all of your profiles, you can add it to the `defaults` section above the list of profiles in your settings.json file.</span></span>

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

## <a name="unique-identifier"></a><span data-ttu-id="73963-106">Eindeutiger Bezeichner</span><span class="sxs-lookup"><span data-stu-id="73963-106">Unique identifier</span></span>

<span data-ttu-id="73963-107">Profile können eine GUID als eindeutigen Bezeichner verwenden.</span><span class="sxs-lookup"><span data-stu-id="73963-107">Profiles can use a GUID as a unique identifier.</span></span> <span data-ttu-id="73963-108">Damit ein Profil zu Ihrem Standardprofil wird, benötigt es eine GUID für die globale Einstellung `defaultProfile`.</span><span class="sxs-lookup"><span data-stu-id="73963-108">To make a profile your default profile, it needs a GUID for the `defaultProfile` global setting.</span></span>

<span data-ttu-id="73963-109">**Eigenschaftenname:** `guid`</span><span class="sxs-lookup"><span data-stu-id="73963-109">**Property name:** `guid`</span></span>

<span data-ttu-id="73963-110">**Erfordernis:** Erforderlich</span><span class="sxs-lookup"><span data-stu-id="73963-110">**Necessity:** Required</span></span>

<span data-ttu-id="73963-111">**Akzeptiert:** GUID als Zeichenfolge im Registrierungsformat: `"{00000000-0000-0000-0000-000000000000}"`</span><span class="sxs-lookup"><span data-stu-id="73963-111">**Accepts:** GUID as a string in registry format: `"{00000000-0000-0000-0000-000000000000}"`</span></span>

<br />

___

## <a name="executable-settings"></a><span data-ttu-id="73963-112">Ausführbare Einstellungen</span><span class="sxs-lookup"><span data-stu-id="73963-112">Executable settings</span></span>

### <a name="command-line"></a><span data-ttu-id="73963-113">Befehlszeile</span><span class="sxs-lookup"><span data-stu-id="73963-113">Command line</span></span>

<span data-ttu-id="73963-114">Dies ist die ausführbare Datei, die im Profil verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="73963-114">This is the executable used in the profile.</span></span>

<span data-ttu-id="73963-115">**Eigenschaftenname:** `commandline`</span><span class="sxs-lookup"><span data-stu-id="73963-115">**Property name:** `commandline`</span></span>

<span data-ttu-id="73963-116">**Erfordernis:** Optional</span><span class="sxs-lookup"><span data-stu-id="73963-116">**Necessity:** Optional</span></span>

<span data-ttu-id="73963-117">**Akzeptiert:** Name der ausführbaren Datei als Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="73963-117">**Accepts:** Executable file name as a string</span></span>

<span data-ttu-id="73963-118">**Standardwert:** `"cmd.exe"`</span><span class="sxs-lookup"><span data-stu-id="73963-118">**Default value:** `"cmd.exe"`</span></span>

### <a name="source"></a><span data-ttu-id="73963-119">Quelle</span><span class="sxs-lookup"><span data-stu-id="73963-119">Source</span></span>

<span data-ttu-id="73963-120">Hiermit wird der Name des Profilgenerators gespeichert, von dem das Profil stammt.</span><span class="sxs-lookup"><span data-stu-id="73963-120">This stores the name of the profile generator that originated the profile.</span></span> <span data-ttu-id="73963-121">_Es sind keine erkennbaren Werte für dieses Feld vorhanden._</span><span class="sxs-lookup"><span data-stu-id="73963-121">_There are no discoverable values for this field._</span></span> <span data-ttu-id="73963-122">Weitere Informationen zu dynamischen Profilen finden Sie auf der Seite [Dynamische Profile](./../dynamic-profiles.md).</span><span class="sxs-lookup"><span data-stu-id="73963-122">For additional information on dynamic profiles, visit the [Dynamic profiles page](./../dynamic-profiles.md).</span></span>

<span data-ttu-id="73963-123">**Eigenschaftenname:** `source`</span><span class="sxs-lookup"><span data-stu-id="73963-123">**Property name:** `source`</span></span>

<span data-ttu-id="73963-124">**Erfordernis:** Optional</span><span class="sxs-lookup"><span data-stu-id="73963-124">**Necessity:** Optional</span></span>

<span data-ttu-id="73963-125">**Akzeptiert:** Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="73963-125">**Accepts:** String</span></span>

### <a name="starting-directory"></a><span data-ttu-id="73963-126">Startverzeichnis</span><span class="sxs-lookup"><span data-stu-id="73963-126">Starting directory</span></span>

<span data-ttu-id="73963-127">Dies ist das Verzeichnis, in dem die Shell beim Laden gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="73963-127">This is the directory the shell starts in when it is loaded.</span></span>

<span data-ttu-id="73963-128">**Eigenschaftenname:** `startingDirectory`</span><span class="sxs-lookup"><span data-stu-id="73963-128">**Property name:** `startingDirectory`</span></span>

<span data-ttu-id="73963-129">**Erfordernis:** Optional</span><span class="sxs-lookup"><span data-stu-id="73963-129">**Necessity:** Optional</span></span>

<span data-ttu-id="73963-130">**Akzeptiert:** Speicherort des Ordners als Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="73963-130">**Accepts:** Folder location as a string</span></span>

<span data-ttu-id="73963-131">**Standardwert:** `"%USERPROFILE%"`</span><span class="sxs-lookup"><span data-stu-id="73963-131">**Default value:** `"%USERPROFILE%"`</span></span>

<br />

> [!NOTE]
> <span data-ttu-id="73963-132">Wenn Sie das Startverzeichnis festlegen, in dem die installierten WSL-Distributionen geöffnet werden, sollten Sie folgendes Format verwenden: „startingdirectory“: „//WSL$/<distro name>“, wobei Sie den Namen Ihrer Distribution einsetzen.</span><span class="sxs-lookup"><span data-stu-id="73963-132">When setting the starting directory that your installed WSL distributions open to, you should use this format: "startingDirectory": "//wsl$/<distro name>", replacing with the name of your distribution.</span></span> <span data-ttu-id="73963-133">Beispielsweise „startingDirectory“: „//wsl$/Ubuntu-20.04“.</span><span class="sxs-lookup"><span data-stu-id="73963-133">For example, "startingDirectory": "//wsl$/Ubuntu-20.04".</span></span>

___

## <a name="dropdown-settings"></a><span data-ttu-id="73963-134">Dropdowneinstellungen</span><span class="sxs-lookup"><span data-stu-id="73963-134">Dropdown settings</span></span>

<span data-ttu-id="73963-135">![Windows Terminal-Dropdownmenü](./../images/dropdown.png)
_Konfiguration: [Raspberry Ubuntu](./../custom-terminal-gallery/raspberry-ubuntu.md)_</span><span class="sxs-lookup"><span data-stu-id="73963-135">![Windows Terminal dropdown](./../images/dropdown.png)
_Configuration: [Raspberry Ubuntu](./../custom-terminal-gallery/raspberry-ubuntu.md)_</span></span>

### <a name="name"></a><span data-ttu-id="73963-136">Name</span><span class="sxs-lookup"><span data-stu-id="73963-136">Name</span></span>

<span data-ttu-id="73963-137">Dies ist der Name des Profils, der im Dropdownmenü angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="73963-137">This is the name of the profile that will be displayed in the dropdown menu.</span></span> <span data-ttu-id="73963-138">Dieser Wert wird auch als „Titel“ verwendet, der beim Start an die Shell übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="73963-138">This value is also used as the "title" to pass to the shell on startup.</span></span> <span data-ttu-id="73963-139">Einige Shells (z. B. `bash`) können diesen Anfangswert möglicherweise ignorieren, während andere (`Command Prompt`, `PowerShell`) diesen Wert während der Lebensdauer der Anwendung verwenden.</span><span class="sxs-lookup"><span data-stu-id="73963-139">Some shells (like `bash`) may choose to ignore this initial value, while others (`Command Prompt`, `PowerShell`) may use this value over the lifetime of the application.</span></span> <span data-ttu-id="73963-140">Dieses Verhalten von „Titel“ kann durch `tabTitle` außer Kraft gesetzt werden.</span><span class="sxs-lookup"><span data-stu-id="73963-140">This "title" behavior can be overridden by using `tabTitle`.</span></span>

<span data-ttu-id="73963-141">**Eigenschaftenname:** `name`</span><span class="sxs-lookup"><span data-stu-id="73963-141">**Property name:** `name`</span></span>

<span data-ttu-id="73963-142">**Erfordernis:** Erforderlich</span><span class="sxs-lookup"><span data-stu-id="73963-142">**Necessity:** Required</span></span>

<span data-ttu-id="73963-143">**Akzeptiert:** Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="73963-143">**Accepts:** String</span></span>

### <a name="icon"></a><span data-ttu-id="73963-144">Symbol</span><span class="sxs-lookup"><span data-stu-id="73963-144">Icon</span></span>

<span data-ttu-id="73963-145">Hiermit wird das Symbol festgelegt, das auf der Registerkarte und im Dropdownmenü angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="73963-145">This sets the icon that displays within the tab and the dropdown menu.</span></span>

<span data-ttu-id="73963-146">**Eigenschaftenname:** `icon`</span><span class="sxs-lookup"><span data-stu-id="73963-146">**Property name:** `icon`</span></span>

<span data-ttu-id="73963-147">**Erfordernis:** Optional</span><span class="sxs-lookup"><span data-stu-id="73963-147">**Necessity:** Optional</span></span>

<span data-ttu-id="73963-148">**Akzeptiert:** Speicherort der Datei als Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="73963-148">**Accepts:** File location as a string</span></span>

### <a name="hide-a-profile-from-the-dropdown"></a><span data-ttu-id="73963-149">Ein Profil aus dem Dropdownmenü ausblenden</span><span class="sxs-lookup"><span data-stu-id="73963-149">Hide a profile from the dropdown</span></span>

<span data-ttu-id="73963-150">Wenn `hidden` auf `true` festgelegt ist, wird das Profil nicht in der Liste der Profile angezeigt.</span><span class="sxs-lookup"><span data-stu-id="73963-150">If `hidden` is set to `true`, the profile will not appear in the list of profiles.</span></span> <span data-ttu-id="73963-151">Dies kann verwendet werden, um Standardprofile und dynamisch generierte Profile auszublenden, während sie in der Einstellungsdatei beibehalten werden.</span><span class="sxs-lookup"><span data-stu-id="73963-151">This can be used to hide default profiles and dynamically generated profiles, while leaving them in your settings file.</span></span> <span data-ttu-id="73963-152">Weitere Informationen zu dynamischen Profilen finden Sie auf der Seite [Dynamische Profile](./../dynamic-profiles.md).</span><span class="sxs-lookup"><span data-stu-id="73963-152">To learn more about dynamic profiles, visit the [Dynamic profiles page](./../dynamic-profiles.md).</span></span>

<span data-ttu-id="73963-153">**Eigenschaftenname:** `hidden`</span><span class="sxs-lookup"><span data-stu-id="73963-153">**Property name:** `hidden`</span></span>

<span data-ttu-id="73963-154">**Erfordernis:** Optional</span><span class="sxs-lookup"><span data-stu-id="73963-154">**Necessity:** Optional</span></span>

<span data-ttu-id="73963-155">**Akzeptiert:** `true`, `false`</span><span class="sxs-lookup"><span data-stu-id="73963-155">**Accepts:** `true`, `false`</span></span>

<span data-ttu-id="73963-156">**Standardwert:** `false`</span><span class="sxs-lookup"><span data-stu-id="73963-156">**Default value:** `false`</span></span>

<br />

___

## <a name="tab-title-settings"></a><span data-ttu-id="73963-157">Einstellungen für Registerkartentitel</span><span class="sxs-lookup"><span data-stu-id="73963-157">Tab title settings</span></span>

### <a name="custom-tab-title"></a><span data-ttu-id="73963-158">Benutzerdefinierter Registerkartentitel</span><span class="sxs-lookup"><span data-stu-id="73963-158">Custom tab title</span></span>

<span data-ttu-id="73963-159">Wenn diese Einstellung festgelegt ist, ersetzt sie `name` als Titel, der beim Start an die Shell übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="73963-159">If set, this will replace the `name` as the title to pass to the shell on startup.</span></span> <span data-ttu-id="73963-160">Einige Shells (z. B. `bash`) können diesen Anfangswert möglicherweise ignorieren, während andere (`Command Prompt`, `PowerShell`) diesen Wert während der Lebensdauer der Anwendung verwenden.</span><span class="sxs-lookup"><span data-stu-id="73963-160">Some shells (like `bash`) may choose to ignore this initial value, while others (`Command Prompt`, `PowerShell`) may use this value over the lifetime of the application.</span></span> <span data-ttu-id="73963-161">Wenn Sie erfahren möchten, wie Sie Ihren Titel von der Shell festlegen lassen können, besuchen Sie das [Tutorial zu Registerkartentiteln](./../tutorials/tab-title.md).</span><span class="sxs-lookup"><span data-stu-id="73963-161">If you'd like to learn how to have the shell set your title, visit the [tab title tutorial](./../tutorials/tab-title.md).</span></span>

<span data-ttu-id="73963-162">**Eigenschaftenname:** `tabTitle`</span><span class="sxs-lookup"><span data-stu-id="73963-162">**Property name:** `tabTitle`</span></span>

<span data-ttu-id="73963-163">**Erfordernis:** Optional</span><span class="sxs-lookup"><span data-stu-id="73963-163">**Necessity:** Optional</span></span>

<span data-ttu-id="73963-164">**Akzeptiert:** Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="73963-164">**Accepts:** String</span></span>

### <a name="suppress-title-changes-from-the-shell"></a><span data-ttu-id="73963-165">Titeländerungen von der Shell unterdrücken</span><span class="sxs-lookup"><span data-stu-id="73963-165">Suppress title changes from the shell</span></span>

<span data-ttu-id="73963-166">Wenn dieser Wert auf `true` festgelegt ist, setzt `tabTitle` den Standardtitel der Registerkarte außer Kraft und alle Nachrichten von der Anwendung zur Titeländerung werden unterdrückt.</span><span class="sxs-lookup"><span data-stu-id="73963-166">When this is set to `true`, `tabTitle` overrides the default title of the tab and any title change messages from the application will be suppressed.</span></span> <span data-ttu-id="73963-167">Wenn `tabTitle` nicht festgelegt ist, wird stattdessen `name` verwendet.</span><span class="sxs-lookup"><span data-stu-id="73963-167">If `tabTitle` isn't set, `name` will be used instead.</span></span> <span data-ttu-id="73963-168">Wenn dies auf `false` festgelegt ist, verhält sich `tabTitle` normal.</span><span class="sxs-lookup"><span data-stu-id="73963-168">When this is set to `false`, `tabTitle` behaves as normal.</span></span>

<span data-ttu-id="73963-169">**Eigenschaftenname:** `suppressApplicationTitle`</span><span class="sxs-lookup"><span data-stu-id="73963-169">**Property name:** `suppressApplicationTitle`</span></span>

<span data-ttu-id="73963-170">**Erfordernis:** Optional</span><span class="sxs-lookup"><span data-stu-id="73963-170">**Necessity:** Optional</span></span>

<span data-ttu-id="73963-171">**Akzeptiert:** `true`, `false`</span><span class="sxs-lookup"><span data-stu-id="73963-171">**Accepts:** `true`, `false`</span></span>

<br />

___

## <a name="text-settings"></a><span data-ttu-id="73963-172">Texteinstellungen</span><span class="sxs-lookup"><span data-stu-id="73963-172">Text settings</span></span>

### <a name="font-face"></a><span data-ttu-id="73963-173">Schriftart</span><span class="sxs-lookup"><span data-stu-id="73963-173">Font face</span></span>

<span data-ttu-id="73963-174">Dies ist der Name der Schriftart, die im Profil verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="73963-174">This is the name of the font face used in the profile.</span></span> <span data-ttu-id="73963-175">Das Terminal versucht, alternativ Consolas zu verwenden, wenn diese Schriftart nicht gefunden werden kann oder ungültig ist.</span><span class="sxs-lookup"><span data-stu-id="73963-175">The terminal will try to fallback to Consolas if this can't be found or is invalid.</span></span> <span data-ttu-id="73963-176">Informationen zu den anderen Varianten der Standardschriftart, Cascadia Mono, finden Sie auf der [Cascadia Code-Seite](./../cascadia-code.md).</span><span class="sxs-lookup"><span data-stu-id="73963-176">To learn about the other variants of the default font, Cascadia Mono, visit the [Cascadia Code page](./../cascadia-code.md).</span></span>

<span data-ttu-id="73963-177">**Eigenschaftenname:** `fontFace`</span><span class="sxs-lookup"><span data-stu-id="73963-177">**Property name:** `fontFace`</span></span>

<span data-ttu-id="73963-178">**Erfordernis:** Optional</span><span class="sxs-lookup"><span data-stu-id="73963-178">**Necessity:** Optional</span></span>

<span data-ttu-id="73963-179">**Akzeptiert:** Schriftartname als Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="73963-179">**Accepts:** Font name as a string</span></span>

<span data-ttu-id="73963-180">**Standardwert:** `"Cascadia Mono"`</span><span class="sxs-lookup"><span data-stu-id="73963-180">**Default value:** `"Cascadia Mono"`</span></span>

### <a name="font-size"></a><span data-ttu-id="73963-181">Schriftgrad</span><span class="sxs-lookup"><span data-stu-id="73963-181">Font size</span></span>

<span data-ttu-id="73963-182">Hiermit wird der Schriftgrad des Profils in Punkt festgelegt.</span><span class="sxs-lookup"><span data-stu-id="73963-182">This sets the profile's font size in points.</span></span>

<span data-ttu-id="73963-183">**Eigenschaftenname:** `fontSize`</span><span class="sxs-lookup"><span data-stu-id="73963-183">**Property name:** `fontSize`</span></span>

<span data-ttu-id="73963-184">**Erfordernis:** Optional</span><span class="sxs-lookup"><span data-stu-id="73963-184">**Necessity:** Optional</span></span>

<span data-ttu-id="73963-185">**Akzeptiert:** Ganze Zahl</span><span class="sxs-lookup"><span data-stu-id="73963-185">**Accepts:** Integer</span></span>

<span data-ttu-id="73963-186">**Standardwert:** `12`</span><span class="sxs-lookup"><span data-stu-id="73963-186">**Default value:** `12`</span></span>

### <a name="font-weight-preview"></a><span data-ttu-id="73963-187">Schriftbreite ([Vorschau](https://aka.ms/terminal-preview/))</span><span class="sxs-lookup"><span data-stu-id="73963-187">Font weight ([Preview](https://aka.ms/terminal-preview/))</span></span>

<span data-ttu-id="73963-188">Dadurch wird die Breite (Dünne oder Dicke der Striche) für die Schriftart des Profils festgelegt.</span><span class="sxs-lookup"><span data-stu-id="73963-188">This sets the weight (lightness or heaviness of the strokes) for the profile's font.</span></span>

<span data-ttu-id="73963-189">**Eigenschaftenname:** `fontWeight`</span><span class="sxs-lookup"><span data-stu-id="73963-189">**Property name:** `fontWeight`</span></span>

<span data-ttu-id="73963-190">**Erfordernis:** Optional</span><span class="sxs-lookup"><span data-stu-id="73963-190">**Necessity:** Optional</span></span>

<span data-ttu-id="73963-191">**Akzeptiert:** `"normal"`, `"thin"`, `"extra-light"`, `"light"`, `"semi-light"`, `"medium"`, `"semi-bold"`, `"bold"`, `"extra-bold"`, `"black"`, `"extra-black"` oder eine Ganzzahl, die der numerischen Darstellung der OpenType-Schriftbreite entspricht</span><span class="sxs-lookup"><span data-stu-id="73963-191">**Accepts:** `"normal"`, `"thin"`, `"extra-light"`, `"light"`, `"semi-light"`, `"medium"`, `"semi-bold"`, `"bold"`, `"extra-bold"`, `"black"`, `"extra-black"`, or an integer corresponding to the numeric representation of the OpenType font weight</span></span>

<span data-ttu-id="73963-192">**Standardwert:** `"normal"`</span><span class="sxs-lookup"><span data-stu-id="73963-192">**Default value:** `"normal"`</span></span>

> [!IMPORTANT]
> <span data-ttu-id="73963-193">Diese Funktion steht nur in der [Windows Terminal-Vorschau](https://aka.ms/terminal-preview/) zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="73963-193">This feature is only available in [Windows Terminal Preview](https://aka.ms/terminal-preview/).</span></span>

### <a name="padding"></a><span data-ttu-id="73963-194">Abstand</span><span class="sxs-lookup"><span data-stu-id="73963-194">Padding</span></span>

:::row:::
:::column span="":::
<span data-ttu-id="73963-195">Hiermit wird der Abstand um den Text im Fenster festgelegt.</span><span class="sxs-lookup"><span data-stu-id="73963-195">This sets the padding around the text within the window.</span></span> <span data-ttu-id="73963-196">Dabei werden drei verschiedene Formate akzeptiert: `"#"` legt denselben Abstand für alle Seiten fest, `"#, #"` legt denselben Abstand für links-rechts und oben-unten fest, und `"#, #, #, #"` legt den Abstand individuell für links, oben, rechts und unten fest.</span><span class="sxs-lookup"><span data-stu-id="73963-196">This will accept three different formats: `"#"` sets the same padding for all sides, `"#, #"` sets the same padding for left-right and top-bottom, and `"#, #, #, #"` sets the padding individually for left, top, right, and bottom.</span></span>

<span data-ttu-id="73963-197">**Eigenschaftenname:** `padding`</span><span class="sxs-lookup"><span data-stu-id="73963-197">**Property name:** `padding`</span></span>

<span data-ttu-id="73963-198">**Erfordernis:** Optional</span><span class="sxs-lookup"><span data-stu-id="73963-198">**Necessity:** Optional</span></span>

<span data-ttu-id="73963-199">**Akzeptiert:** Werte als Zeichenfolge in den folgenden Formaten: `"#"`, `"#, #"`, `"#, #, #, #"`</span><span class="sxs-lookup"><span data-stu-id="73963-199">**Accepts:** Values as a string in the following formats: `"#"`, `"#, #"`, `"#, #, #, #"`</span></span>

<span data-ttu-id="73963-200">**Standardwert:** `"8, 8, 8, 8"`</span><span class="sxs-lookup"><span data-stu-id="73963-200">**Default value:** `"8, 8, 8, 8"`</span></span>

:::column-end:::
:::column span="":::
![Windows Terminal-Abstand](./../images/padding.gif)

:::column-end:::
:::row-end:::

### <a name="antialiasing-text"></a><span data-ttu-id="73963-202">Antialiasing bei Text</span><span class="sxs-lookup"><span data-stu-id="73963-202">Antialiasing text</span></span>

<span data-ttu-id="73963-203">Hiermit wird gesteuert, wie das Antialiasing bei Text im Renderer erfolgt.</span><span class="sxs-lookup"><span data-stu-id="73963-203">This controls how text is antialiased in the renderer.</span></span> <span data-ttu-id="73963-204">Beachten Sie, dass das Ändern dieser Einstellung das Starten einer neuen Terminalinstanz erfordert.</span><span class="sxs-lookup"><span data-stu-id="73963-204">Note that changing this setting will require starting a new terminal instance.</span></span>

![Windows Terminal: Antialiasing bei Text](./../images/antialiasing-mode.gif)

<span data-ttu-id="73963-206">**Eigenschaftenname:** `antialiasingMode`</span><span class="sxs-lookup"><span data-stu-id="73963-206">**Property name:** `antialiasingMode`</span></span>

<span data-ttu-id="73963-207">**Erfordernis:** Optional</span><span class="sxs-lookup"><span data-stu-id="73963-207">**Necessity:** Optional</span></span>

<span data-ttu-id="73963-208">**Akzeptiert:** `"grayscale"`, `"cleartype"`, `"aliased"`</span><span class="sxs-lookup"><span data-stu-id="73963-208">**Accepts:** `"grayscale"`, `"cleartype"`, `"aliased"`</span></span>

<span data-ttu-id="73963-209">**Standardwert:** `"grayscale"`</span><span class="sxs-lookup"><span data-stu-id="73963-209">**Default value:** `"grayscale"`</span></span>

<br />

___

## <a name="cursor-settings"></a><span data-ttu-id="73963-210">Cursoreinstellungen</span><span class="sxs-lookup"><span data-stu-id="73963-210">Cursor settings</span></span>

### <a name="cursor-shape"></a><span data-ttu-id="73963-211">Cursorform</span><span class="sxs-lookup"><span data-stu-id="73963-211">Cursor shape</span></span>

<span data-ttu-id="73963-212">Hiermit wird die Cursorform für das Profil festgelegt.</span><span class="sxs-lookup"><span data-stu-id="73963-212">This sets the cursor shape for the profile.</span></span> <span data-ttu-id="73963-213">Mögliche Cursor: `"bar"` (&#x2503;), `"vintage"` (&#x2583;), `"underscore"` (&#x2581;), `"filledBox"` (&#x2588;), `"emptyBox"` (&#x25AF;)</span><span class="sxs-lookup"><span data-stu-id="73963-213">The possible cursors are as follows: `"bar"` ( &#x2503; ), `"vintage"` ( &#x2583; ), `"underscore"` ( &#x2581; ), `"filledBox"` ( &#x2588; ), `"emptyBox"` ( &#x25AF; )</span></span>

<span data-ttu-id="73963-214">**Eigenschaftenname:** `cursorShape`</span><span class="sxs-lookup"><span data-stu-id="73963-214">**Property name:** `cursorShape`</span></span>

<span data-ttu-id="73963-215">**Erfordernis:** Optional</span><span class="sxs-lookup"><span data-stu-id="73963-215">**Necessity:** Optional</span></span>

<span data-ttu-id="73963-216">**Akzeptiert:** `"bar"`, `"vintage"`, `"underscore"`, `"filledBox"`, `"emptyBox"`</span><span class="sxs-lookup"><span data-stu-id="73963-216">**Accepts:** `"bar"`, `"vintage"`, `"underscore"`, `"filledBox"`, `"emptyBox"`</span></span>

<span data-ttu-id="73963-217">**Standardwert:** `"bar"`</span><span class="sxs-lookup"><span data-stu-id="73963-217">**Default value:** `"bar"`</span></span>

### <a name="cursor-color"></a><span data-ttu-id="73963-218">Cursorfarbe</span><span class="sxs-lookup"><span data-stu-id="73963-218">Cursor color</span></span>

<span data-ttu-id="73963-219">Hiermit wird die Cursorfarbe für das Profil festgelegt.</span><span class="sxs-lookup"><span data-stu-id="73963-219">This sets the cursor color of the profile.</span></span> <span data-ttu-id="73963-220">Hiermit wird das im Farbschema festgelegte `cursorColor` außer Kraft gesetzt, wenn `colorScheme` festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="73963-220">This will override the `cursorColor` set in the color scheme if `colorScheme` is set.</span></span>

<span data-ttu-id="73963-221">**Eigenschaftenname:** `cursorColor`</span><span class="sxs-lookup"><span data-stu-id="73963-221">**Property name:** `cursorColor`</span></span>

<span data-ttu-id="73963-222">**Erfordernis:** Optional</span><span class="sxs-lookup"><span data-stu-id="73963-222">**Necessity:** Optional</span></span>

<span data-ttu-id="73963-223">**Akzeptiert:** Farbe als Zeichenfolge im Hexadezimalformat: `"#rgb"` oder `"#rrggbb"`</span><span class="sxs-lookup"><span data-stu-id="73963-223">**Accepts:** Color as a string in hex format: `"#rgb"` or `"#rrggbb"`</span></span>

### <a name="cursor-height"></a><span data-ttu-id="73963-224">Cursorhöhe</span><span class="sxs-lookup"><span data-stu-id="73963-224">Cursor height</span></span>

<span data-ttu-id="73963-225">Hiermit wird die prozentuale Höhe des Cursors ab dem unteren Rand festgelegt.</span><span class="sxs-lookup"><span data-stu-id="73963-225">This sets the percentage height of the cursor starting from the bottom.</span></span> <span data-ttu-id="73963-226">Dies funktioniert nur, wenn `cursorShape` auf `"vintage"` festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="73963-226">This will only work when `cursorShape` is set to `"vintage"`.</span></span>

<span data-ttu-id="73963-227">**Eigenschaftenname:** `cursorHeight`</span><span class="sxs-lookup"><span data-stu-id="73963-227">**Property name:** `cursorHeight`</span></span>

<span data-ttu-id="73963-228">**Erfordernis:** Optional</span><span class="sxs-lookup"><span data-stu-id="73963-228">**Necessity:** Optional</span></span>

<span data-ttu-id="73963-229">**Akzeptiert:** Ganzzahl zwischen 25 und 100</span><span class="sxs-lookup"><span data-stu-id="73963-229">**Accepts:** Integer from 25-100</span></span>

<br />

___

## <a name="keyboard-settings"></a><span data-ttu-id="73963-230">Tastatureinstellungen</span><span class="sxs-lookup"><span data-stu-id="73963-230">Keyboard settings</span></span>

### <a name="altgr-aliasing-preview"></a><span data-ttu-id="73963-231">AltGr-Aliasing ([Vorschau](https://aka.ms/terminal-preview/))</span><span class="sxs-lookup"><span data-stu-id="73963-231">AltGr aliasing ([Preview](https://aka.ms/terminal-preview/))</span></span>

<span data-ttu-id="73963-232">Hiermit können Sie steuern, ob Windows Terminal <kbd>STRG+ALT</kbd> als Alias für <kbd>ALTGR</kbd> behandelt.</span><span class="sxs-lookup"><span data-stu-id="73963-232">This allows you to control if Windows Terminal will treat <kbd>ctrl+alt</kbd> as an alias for <kbd>AltGr</kbd>.</span></span>

<span data-ttu-id="73963-233">**Eigenschaftenname:** `altGrAliasing`</span><span class="sxs-lookup"><span data-stu-id="73963-233">**Property name:** `altGrAliasing`</span></span>

<span data-ttu-id="73963-234">**Erfordernis:** Optional</span><span class="sxs-lookup"><span data-stu-id="73963-234">**Necessity:** Optional</span></span>

<span data-ttu-id="73963-235">**Akzeptiert:** `true`, `false`</span><span class="sxs-lookup"><span data-stu-id="73963-235">**Accepts:** `true`, `false`</span></span>

<span data-ttu-id="73963-236">**Standardwert:** `true`</span><span class="sxs-lookup"><span data-stu-id="73963-236">**Default value:** `true`</span></span>

> [!IMPORTANT]
> <span data-ttu-id="73963-237">Diese Funktion steht nur in der [Windows Terminal-Vorschau](https://aka.ms/terminal-preview/) zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="73963-237">This feature is only available in [Windows Terminal Preview](https://aka.ms/terminal-preview/).</span></span>

<br />

___

## <a name="color-settings"></a><span data-ttu-id="73963-238">Farbeinstellungen</span><span class="sxs-lookup"><span data-stu-id="73963-238">Color settings</span></span>

### <a name="color-scheme"></a><span data-ttu-id="73963-239">Farbschema</span><span class="sxs-lookup"><span data-stu-id="73963-239">Color scheme</span></span>

<span data-ttu-id="73963-240">Dies ist der Name des Farbschemas, das im Profil verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="73963-240">This is the name of the color scheme used in the profile.</span></span> <span data-ttu-id="73963-241">Farbschemas werden im `schemes`-Objekt definiert.</span><span class="sxs-lookup"><span data-stu-id="73963-241">Color schemes are defined in the `schemes` object.</span></span> <span data-ttu-id="73963-242">Ausführlichere Informationen finden Sie auf der Seite [Farbschemas](./color-schemes.md).</span><span class="sxs-lookup"><span data-stu-id="73963-242">More detailed information can be found on the [Color schemes page](./color-schemes.md).</span></span>

<span data-ttu-id="73963-243">**Eigenschaftenname:** `colorScheme`</span><span class="sxs-lookup"><span data-stu-id="73963-243">**Property name:** `colorScheme`</span></span>

<span data-ttu-id="73963-244">**Erfordernis:** Optional</span><span class="sxs-lookup"><span data-stu-id="73963-244">**Necessity:** Optional</span></span>

<span data-ttu-id="73963-245">**Akzeptiert:** Name des Farbschemas als Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="73963-245">**Accepts:** Name of color scheme as a string</span></span>

<span data-ttu-id="73963-246">**Standardwert:** `"Campbell"`</span><span class="sxs-lookup"><span data-stu-id="73963-246">**Default value:** `"Campbell"`</span></span>

### <a name="foreground-color"></a><span data-ttu-id="73963-247">Vordergrundfarbe</span><span class="sxs-lookup"><span data-stu-id="73963-247">Foreground color</span></span>

<span data-ttu-id="73963-248">Hiermit wird die Vordergrundfarbe des Profils geändert.</span><span class="sxs-lookup"><span data-stu-id="73963-248">This changes the foreground color of the profile.</span></span> <span data-ttu-id="73963-249">Hiermit wird das im Farbschema festgelegte `foreground` außer Kraft gesetzt, wenn `colorScheme` festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="73963-249">This overrides `foreground` set in the color scheme if `colorScheme` is set.</span></span>

<span data-ttu-id="73963-250">**Eigenschaftenname:** `foreground`</span><span class="sxs-lookup"><span data-stu-id="73963-250">**Property name:** `foreground`</span></span>

<span data-ttu-id="73963-251">**Erfordernis:** Optional</span><span class="sxs-lookup"><span data-stu-id="73963-251">**Necessity:** Optional</span></span>

<span data-ttu-id="73963-252">**Akzeptiert:** Farbe als Zeichenfolge im Hexadezimalformat: `"#rgb"` oder `"#rrggbb"`</span><span class="sxs-lookup"><span data-stu-id="73963-252">**Accepts:** Color as a string in hex format: `"#rgb"` or `"#rrggbb"`</span></span>

### <a name="background-color"></a><span data-ttu-id="73963-253">Hintergrundfarbe</span><span class="sxs-lookup"><span data-stu-id="73963-253">Background color</span></span>

<span data-ttu-id="73963-254">Hiermit wird die Hintergrundfarbe des Profils mit dieser Einstellung geändert.</span><span class="sxs-lookup"><span data-stu-id="73963-254">This changes the background color of the profile with this setting.</span></span> <span data-ttu-id="73963-255">Hiermit wird das im Farbschema festgelegte `background` außer Kraft gesetzt, wenn `colorScheme` festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="73963-255">This overrides `background` set in the color scheme if `colorScheme` is set.</span></span>

<span data-ttu-id="73963-256">**Eigenschaftenname:** `background`</span><span class="sxs-lookup"><span data-stu-id="73963-256">**Property name:** `background`</span></span>

<span data-ttu-id="73963-257">**Erfordernis:** Optional</span><span class="sxs-lookup"><span data-stu-id="73963-257">**Necessity:** Optional</span></span>

<span data-ttu-id="73963-258">**Akzeptiert:** Farbe als Zeichenfolge im Hexadezimalformat: `"#rgb"` oder `"#rrggbb"`</span><span class="sxs-lookup"><span data-stu-id="73963-258">**Accepts:** Color as a string in hex format: `"#rgb"` or `"#rrggbb"`</span></span>

### <a name="selection-background-color"></a><span data-ttu-id="73963-259">Auswahlhintergrundfarbe</span><span class="sxs-lookup"><span data-stu-id="73963-259">Selection background color</span></span>

<span data-ttu-id="73963-260">Hiermit wird die Hintergrundfarbe einer Auswahl im Profil festgelegt.</span><span class="sxs-lookup"><span data-stu-id="73963-260">This sets the background color of a selection within the profile.</span></span> <span data-ttu-id="73963-261">Hiermit wird das im Farbschema festgelegte `selectionBackground` außer Kraft gesetzt, wenn `colorScheme` festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="73963-261">This will override the `selectionBackground` set in the color scheme if `colorScheme` is set.</span></span>

<span data-ttu-id="73963-262">**Eigenschaftenname:** `selectionBackground`</span><span class="sxs-lookup"><span data-stu-id="73963-262">**Property name:** `selectionBackground`</span></span>

<span data-ttu-id="73963-263">**Erfordernis:** Optional</span><span class="sxs-lookup"><span data-stu-id="73963-263">**Necessity:** Optional</span></span>

<span data-ttu-id="73963-264">**Akzeptiert:** Farbe als Zeichenfolge im Hexadezimalformat: `"#rgb"` oder `"#rrggbb"`</span><span class="sxs-lookup"><span data-stu-id="73963-264">**Accepts:** Color as a string in hex format: `"#rgb"` or `"#rrggbb"`</span></span>

<br />

___

## <a name="acrylic-settings"></a><span data-ttu-id="73963-265">Acryleinstellungen</span><span class="sxs-lookup"><span data-stu-id="73963-265">Acrylic settings</span></span>

### <a name="enable-acrylic"></a><span data-ttu-id="73963-266">Acryl aktivieren</span><span class="sxs-lookup"><span data-stu-id="73963-266">Enable acrylic</span></span>

:::row:::
:::column span="":::
<span data-ttu-id="73963-267">Wenn dies auf `true` festgelegt ist, hat das Fenster einen Acrylhintergrund.</span><span class="sxs-lookup"><span data-stu-id="73963-267">When this is set to `true`, the window will have an acrylic background.</span></span> <span data-ttu-id="73963-268">Wenn es auf `false` festgelegt ist, hat das Fenster einen einfachen, Hintergrund ohne Textur.</span><span class="sxs-lookup"><span data-stu-id="73963-268">When it's set to `false`, the window will have a plain, untextured background.</span></span> <span data-ttu-id="73963-269">Die Transparenz gilt aufgrund von Betriebssystemeinschränkungen nur für Fenster mit Fokus.</span><span class="sxs-lookup"><span data-stu-id="73963-269">The transparency only applies to focused windows due to OS limitations.</span></span>

<span data-ttu-id="73963-270">**Eigenschaftenname:** `useAcrylic`</span><span class="sxs-lookup"><span data-stu-id="73963-270">**Property name:** `useAcrylic`</span></span>

<span data-ttu-id="73963-271">**Erfordernis:** Optional</span><span class="sxs-lookup"><span data-stu-id="73963-271">**Necessity:** Optional</span></span>

<span data-ttu-id="73963-272">**Akzeptiert:** `true`, `false`</span><span class="sxs-lookup"><span data-stu-id="73963-272">**Accepts:** `true`, `false`</span></span>

<span data-ttu-id="73963-273">**Standardwert:** `false`</span><span class="sxs-lookup"><span data-stu-id="73963-273">**Default value:** `false`</span></span>

:::column-end:::
:::column span="":::
![Windows Terminal: Acryl](./../images/acrylic.gif)

:::column-end:::
:::row-end:::

### <a name="acrylic-opacity"></a><span data-ttu-id="73963-275">Acryldeckkraft</span><span class="sxs-lookup"><span data-stu-id="73963-275">Acrylic opacity</span></span>

:::row:::
:::column span="":::
<span data-ttu-id="73963-276">Wenn `useAcrylic` auf `true` festgelegt ist, wird die Transparenz des Fensters für das Profil festgelegt.</span><span class="sxs-lookup"><span data-stu-id="73963-276">When `useAcrylic` is set to `true`, this sets the transparency of the window for the profile.</span></span> <span data-ttu-id="73963-277">Hierbei werden Gleitkommazahlen zwischen 0 und 1 akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="73963-277">This accepts floating point values from 0-1.</span></span>

<span data-ttu-id="73963-278">**Eigenschaftenname:** `acrylicOpacity`</span><span class="sxs-lookup"><span data-stu-id="73963-278">**Property name:** `acrylicOpacity`</span></span>

<span data-ttu-id="73963-279">**Erfordernis:** Optional</span><span class="sxs-lookup"><span data-stu-id="73963-279">**Necessity:** Optional</span></span>

<span data-ttu-id="73963-280">**Akzeptiert:** Zahl als Gleitkommawert zwischen 0 und 1</span><span class="sxs-lookup"><span data-stu-id="73963-280">**Accepts:** Number as a floating point value from 0-1</span></span>

<span data-ttu-id="73963-281">**Standardwert:** `0.5`</span><span class="sxs-lookup"><span data-stu-id="73963-281">**Default value:** `0.5`</span></span>

:::column-end:::
:::column span="":::
![Windows Terminal: Acryldeckkraft](./../images/acrylic-opacity.gif)

:::column-end:::
:::row-end:::

<br />

___

## <a name="background-image-settings"></a><span data-ttu-id="73963-283">Hintergrundbildeinstellungen</span><span class="sxs-lookup"><span data-stu-id="73963-283">Background image settings</span></span>

### <a name="setting-the-background-image"></a><span data-ttu-id="73963-284">Hintergrundbild festlegen</span><span class="sxs-lookup"><span data-stu-id="73963-284">Setting the background image</span></span>

<span data-ttu-id="73963-285">Hiermit wird der Dateispeicherort des Bilds festgelegt, das über den Fensterhintergrund gezeichnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="73963-285">This sets the file location of the image to draw over the window background.</span></span> <span data-ttu-id="73963-286">Bei dem Hintergrundbild kann es sich um eine JPG-, PNG- oder GIF-Datei handeln.</span><span class="sxs-lookup"><span data-stu-id="73963-286">The background image can be a .jpg, .png, or .gif file.</span></span>

<span data-ttu-id="73963-287">**Eigenschaftenname:** `backgroundImage`</span><span class="sxs-lookup"><span data-stu-id="73963-287">**Property name:** `backgroundImage`</span></span>

<span data-ttu-id="73963-288">**Erfordernis:** Optional</span><span class="sxs-lookup"><span data-stu-id="73963-288">**Necessity:** Optional</span></span>

<span data-ttu-id="73963-289">**Akzeptiert:** Speicherort der Datei als Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="73963-289">**Accepts:** File location as a string</span></span>

### <a name="background-image-stretch-mode"></a><span data-ttu-id="73963-290">Streckmodus für Hintergrundbild</span><span class="sxs-lookup"><span data-stu-id="73963-290">Background image stretch mode</span></span>

:::row:::
:::column span="":::
<span data-ttu-id="73963-291">Hiermit wird festgelegt, wie die Größe des Hintergrundbilds geändert wird, um das Fenster auszufüllen.</span><span class="sxs-lookup"><span data-stu-id="73963-291">This sets how the background image is resized to fill the window.</span></span>

<span data-ttu-id="73963-292">**Eigenschaftenname:** `backgroundImageStretchMode`</span><span class="sxs-lookup"><span data-stu-id="73963-292">**Property name:** `backgroundImageStretchMode`</span></span>

<span data-ttu-id="73963-293">**Erfordernis:** Optional</span><span class="sxs-lookup"><span data-stu-id="73963-293">**Necessity:** Optional</span></span>

<span data-ttu-id="73963-294">**Akzeptiert:** `"none"`, `"fill"`, `"uniform"`, `"uniformToFill"`</span><span class="sxs-lookup"><span data-stu-id="73963-294">**Accepts:** `"none"`, `"fill"`, `"uniform"`, `"uniformToFill"`</span></span>

<span data-ttu-id="73963-295">**Standardwert:** `"uniformToFill"`</span><span class="sxs-lookup"><span data-stu-id="73963-295">**Default value:** `"uniformToFill"`</span></span>

:::column-end:::
:::column span="":::
<span data-ttu-id="73963-296">![Windows Terminal: Streckmodus für Hintergrundbild](./../images/background-image-stretch-mode.gif)
 _[Hintergrundbildquelle](https://wallpaperhub.app/wallpapers/6287)_</span><span class="sxs-lookup"><span data-stu-id="73963-296">![Windows Terminal background image stretch mode](./../images/background-image-stretch-mode.gif)
_[Background image source](https://wallpaperhub.app/wallpapers/6287)_</span></span>

:::column-end:::
:::row-end:::

### <a name="background-image-alignment"></a><span data-ttu-id="73963-297">Hintergrundbildausrichtung</span><span class="sxs-lookup"><span data-stu-id="73963-297">Background image alignment</span></span>

:::row:::
:::column span="":::
<span data-ttu-id="73963-298">Hiermit wird festgelegt, wie das Hintergrundbild an den Fensterbegrenzungen ausgerichtet wird.</span><span class="sxs-lookup"><span data-stu-id="73963-298">This sets how the background image aligns to the boundaries of the window.</span></span>

<span data-ttu-id="73963-299">**Eigenschaftenname:** `backgroundImageAlignment`</span><span class="sxs-lookup"><span data-stu-id="73963-299">**Property name:** `backgroundImageAlignment`</span></span>

<span data-ttu-id="73963-300">**Erfordernis:** Optional</span><span class="sxs-lookup"><span data-stu-id="73963-300">**Necessity:** Optional</span></span>

<span data-ttu-id="73963-301">**Akzeptiert:** `"center"`, `"left"`, `"top"`, `"right"`, `"bottom"`, `"topLeft"`, `"topRight"`, `"bottomLeft"`, `"bottomRight"`</span><span class="sxs-lookup"><span data-stu-id="73963-301">**Accepts:** `"center"`, `"left"`, `"top"`, `"right"`, `"bottom"`, `"topLeft"`, `"topRight"`, `"bottomLeft"`, `"bottomRight"`</span></span>

<span data-ttu-id="73963-302">**Standardwert:** `"center"`</span><span class="sxs-lookup"><span data-stu-id="73963-302">**Default value:** `"center"`</span></span>

:::column-end:::
:::column span="":::
<span data-ttu-id="73963-303">![Windows Terminal: Hintergrundbildausrichtung](./../images/background-image-alignment.gif)
 _[Hintergrundbildquelle](https://design.ubuntu.com/brand/ubuntu-logo/)_</span><span class="sxs-lookup"><span data-stu-id="73963-303">![Windows Terminal background image alignment](./../images/background-image-alignment.gif)
_[Background image source](https://design.ubuntu.com/brand/ubuntu-logo/)_</span></span>

:::column-end:::
:::row-end:::

### <a name="background-image-opacity"></a><span data-ttu-id="73963-304">Hintergrundbilddeckkraft</span><span class="sxs-lookup"><span data-stu-id="73963-304">Background image opacity</span></span>

:::row:::
:::column span="":::
<span data-ttu-id="73963-305">Hiermit wird die Transparenz des Hintergrundbilds festgelegt.</span><span class="sxs-lookup"><span data-stu-id="73963-305">This sets the transparency of the background image.</span></span>

:::column-end:::
:::row-end:::

<span data-ttu-id="73963-306">**Eigenschaftenname:** `backgroundImageOpacity`</span><span class="sxs-lookup"><span data-stu-id="73963-306">**Property name:** `backgroundImageOpacity`</span></span>

<span data-ttu-id="73963-307">**Erfordernis:** Optional</span><span class="sxs-lookup"><span data-stu-id="73963-307">**Necessity:** Optional</span></span>

<span data-ttu-id="73963-308">**Akzeptiert:** Zahl als Gleitkommawert zwischen 0 und 1</span><span class="sxs-lookup"><span data-stu-id="73963-308">**Accepts:** Number as a floating point value from 0-1</span></span>

<span data-ttu-id="73963-309">**Standardwert:** `1.0`</span><span class="sxs-lookup"><span data-stu-id="73963-309">**Default value:** `1.0`</span></span>

<br />

___

## <a name="scroll-settings"></a><span data-ttu-id="73963-310">Scrolleinstellungen</span><span class="sxs-lookup"><span data-stu-id="73963-310">Scroll settings</span></span>

### <a name="scrollbar-visibility"></a><span data-ttu-id="73963-311">Sichtbarkeit der Scrollleiste</span><span class="sxs-lookup"><span data-stu-id="73963-311">Scrollbar visibility</span></span>

<span data-ttu-id="73963-312">Hiermit wird die Sichtbarkeit der Scrollleiste festgelegt.</span><span class="sxs-lookup"><span data-stu-id="73963-312">This sets the visibility of the scrollbar.</span></span>

<span data-ttu-id="73963-313">**Eigenschaftenname:** `scrollbarState`</span><span class="sxs-lookup"><span data-stu-id="73963-313">**Property name:** `scrollbarState`</span></span>

<span data-ttu-id="73963-314">**Erfordernis:** Optional</span><span class="sxs-lookup"><span data-stu-id="73963-314">**Necessity:** Optional</span></span>

<span data-ttu-id="73963-315">**Akzeptiert:** `"visible"`, `"hidden"`</span><span class="sxs-lookup"><span data-stu-id="73963-315">**Accepts:** `"visible"`, `"hidden"`</span></span>

### <a name="scroll-to-input-line-when-typing"></a><span data-ttu-id="73963-316">Beim Eingeben zur Eingabezeile scrollen</span><span class="sxs-lookup"><span data-stu-id="73963-316">Scroll to input line when typing</span></span>

<span data-ttu-id="73963-317">Wenn dies auf `true` festgelegt ist, scrollt das Fenster bei der Eingabe zur Befehlseingabezeile.</span><span class="sxs-lookup"><span data-stu-id="73963-317">When this is set to `true`, the window will scroll to the command input line when typing.</span></span> <span data-ttu-id="73963-318">Wenn es auf `false` festgelegt ist, scrollt das Fenster bei der Eingabe nicht.</span><span class="sxs-lookup"><span data-stu-id="73963-318">When it's set to `false`, the window will not scroll when you start typing.</span></span>

<span data-ttu-id="73963-319">**Eigenschaftenname:** `snapOnInput`</span><span class="sxs-lookup"><span data-stu-id="73963-319">**Property name:** `snapOnInput`</span></span>

<span data-ttu-id="73963-320">**Erfordernis:** Optional</span><span class="sxs-lookup"><span data-stu-id="73963-320">**Necessity:** Optional</span></span>

<span data-ttu-id="73963-321">**Akzeptiert:** `true`, `false`</span><span class="sxs-lookup"><span data-stu-id="73963-321">**Accepts:** `true`, `false`</span></span>

<span data-ttu-id="73963-322">**Standardwert:** `true`</span><span class="sxs-lookup"><span data-stu-id="73963-322">**Default value:** `true`</span></span>

### <a name="history-size"></a><span data-ttu-id="73963-323">Verlaufsgröße</span><span class="sxs-lookup"><span data-stu-id="73963-323">History size</span></span>

<span data-ttu-id="73963-324">Hiermit wird die Anzahl der Zeilen über den Zeilen festgelegt, die in dem Fenster angezeigt werden, zu dem Sie zurückscrollen können.</span><span class="sxs-lookup"><span data-stu-id="73963-324">This sets the number of lines above the ones displayed in the window you can scroll back to.</span></span>

<span data-ttu-id="73963-325">**Eigenschaftenname:** `historySize`</span><span class="sxs-lookup"><span data-stu-id="73963-325">**Property name:** `historySize`</span></span>

<span data-ttu-id="73963-326">**Erfordernis:** Optional</span><span class="sxs-lookup"><span data-stu-id="73963-326">**Necessity:** Optional</span></span>

<span data-ttu-id="73963-327">**Akzeptiert:** Ganze Zahl</span><span class="sxs-lookup"><span data-stu-id="73963-327">**Accepts:** Integer</span></span>

<span data-ttu-id="73963-328">**Standardwert:** `9001`</span><span class="sxs-lookup"><span data-stu-id="73963-328">**Default value:** `9001`</span></span>

<br />

___

## <a name="how-the-profile-closes-when-exiting"></a><span data-ttu-id="73963-329">Wie das Profil beim Verlassen geschlossen wird</span><span class="sxs-lookup"><span data-stu-id="73963-329">How the profile closes when exiting</span></span>

<span data-ttu-id="73963-330">Hiermit wird festgelegt, wie das Profil auf einen Abbruch oder einen fehlerhaften Start reagiert.</span><span class="sxs-lookup"><span data-stu-id="73963-330">This sets how the profile reacts to termination or failure to launch.</span></span> <span data-ttu-id="73963-331">`"graceful"` schließt das Profil, wenn `exit` eingegeben oder der Prozess normal beendet wird.</span><span class="sxs-lookup"><span data-stu-id="73963-331">`"graceful"` will close the profile when `exit` is typed or when the process exits normally.</span></span> <span data-ttu-id="73963-332">`"always"` schließt das Profil immer und `"never"` schließt das Profil nie.</span><span class="sxs-lookup"><span data-stu-id="73963-332">`"always"` will always close the profile and `"never"` will never close the profile.</span></span> <span data-ttu-id="73963-333">`true` und `false` werden als Synonyme für `"graceful"` bzw. `"never"` akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="73963-333">`true` and `false` are accepted as synonyms for `"graceful"` and `"never"`, respectively.</span></span>

<span data-ttu-id="73963-334">**Eigenschaftenname:** `closeOnExit`</span><span class="sxs-lookup"><span data-stu-id="73963-334">**Property name:** `closeOnExit`</span></span>

<span data-ttu-id="73963-335">**Erfordernis:** Optional</span><span class="sxs-lookup"><span data-stu-id="73963-335">**Necessity:** Optional</span></span>

<span data-ttu-id="73963-336">**Akzeptiert:** `"graceful"`, `"always"`, `"never"`, `true`, `false`</span><span class="sxs-lookup"><span data-stu-id="73963-336">**Accepts:** `"graceful"`, `"always"`, `"never"`, `true`, `false`</span></span>

<span data-ttu-id="73963-337">**Standardwert:** `"graceful"`</span><span class="sxs-lookup"><span data-stu-id="73963-337">**Default value:** `"graceful"`</span></span>

<br />

___

## <a name="retro-terminal-effects"></a><span data-ttu-id="73963-338">Terminaleffekte im Retrostil</span><span class="sxs-lookup"><span data-stu-id="73963-338">Retro terminal effects</span></span>

:::row:::
:::column span="":::
<span data-ttu-id="73963-339">Wenn dieser Wert auf `true` festgelegt ist, emuliert das Terminal einen klassischen CRT-Bildschirm mit Scan-Linien und unscharfen Textkanten.</span><span class="sxs-lookup"><span data-stu-id="73963-339">When this is set to `true`, the terminal will emulate a classic CRT display with scan lines and blurry text edges.</span></span> <span data-ttu-id="73963-340">Hierbei handelt es sich um ein experimentelles Feature, dessen Weiterbestehen nicht garantiert ist.</span><span class="sxs-lookup"><span data-stu-id="73963-340">This is an experimental feature and its continued existence is not guaranteed.</span></span>

<span data-ttu-id="73963-341">**Eigenschaftenname:** `experimental.retroTerminalEffect`</span><span class="sxs-lookup"><span data-stu-id="73963-341">**Property name:** `experimental.retroTerminalEffect`</span></span>

<span data-ttu-id="73963-342">**Erfordernis:** Optional</span><span class="sxs-lookup"><span data-stu-id="73963-342">**Necessity:** Optional</span></span>

<span data-ttu-id="73963-343">**Akzeptiert:** `true`, `false`</span><span class="sxs-lookup"><span data-stu-id="73963-343">**Accepts:** `true`, `false`</span></span>

<span data-ttu-id="73963-344">**Standardwert:** `false`</span><span class="sxs-lookup"><span data-stu-id="73963-344">**Default value:** `false`</span></span>

:::column-end:::
:::column span="":::
<span data-ttu-id="73963-345">![Windows Terminal: Experimenteller Terminaleffekt im Retrostil](./../images/experimental-retro-terminal-effect.gif)
_Konfiguration: [Eingabeaufforderung im Retrostil](./../custom-terminal-gallery/retro-command-prompt.md)_</span><span class="sxs-lookup"><span data-stu-id="73963-345">![Windows Terminal experimental retro terminal effect](./../images/experimental-retro-terminal-effect.gif)
_Configuration: [Retro Command Prompt](./../custom-terminal-gallery/retro-command-prompt.md)_</span></span>

:::column-end:::
:::row-end:::
