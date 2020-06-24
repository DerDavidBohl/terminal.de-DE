---
title: 'Windows Terminal: Powerline-Setup'
description: In diesem Tutorial erfahren Sie, wie Sie Powerline in Windows Terminal einrichten.
author: cinnamon-msft
ms.author: cinnamon
ms.date: 05/19/2020
ms.topic: tutorial
ms.service: terminal
ms.openlocfilehash: 2896ede288e0e466f68323a87e5a4b07bd509d3c
ms.sourcegitcommit: bae07a8dd2010a95de4d53b1465abe226e4ad18e
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/26/2020
ms.locfileid: "83856348"
---
# <a name="tutorial-set-up-powerline-in-windows-terminal"></a><span data-ttu-id="09182-103">Tutorial: Einrichten von Powerline in Windows Terminal</span><span class="sxs-lookup"><span data-stu-id="09182-103">Tutorial: Set up Powerline in Windows Terminal</span></span>

<span data-ttu-id="09182-104">Powerline bietet eine angepasste Erfahrung für die Eingabeaufforderung, die Farbcodierungen und Aufforderungen für den Git-Status bietet.</span><span class="sxs-lookup"><span data-stu-id="09182-104">Powerline provides a customized command prompt experience providing Git status color-coding and prompts.</span></span>

![Windows Terminal: Powerline in PowerShell](./../images/powerline-powershell.png)

<span data-ttu-id="09182-106">In diesem Tutorial erfahren Sie, wie Sie die folgenden Aufgaben durchführen:</span><span class="sxs-lookup"><span data-stu-id="09182-106">In this tutorial, you learn how to:</span></span>

> [!div class="checklist"]
>
> * <span data-ttu-id="09182-107">Einrichten von Powerline in PowerShell</span><span class="sxs-lookup"><span data-stu-id="09182-107">Set up Powerline in PowerShell</span></span>
> * <span data-ttu-id="09182-108">Einrichten von Powerline in Ubuntu/WSL</span><span class="sxs-lookup"><span data-stu-id="09182-108">Set up Powerline in Ubuntu/WSL</span></span>
> * <span data-ttu-id="09182-109">Hinzufügen fehlender Powerline-Glyphen</span><span class="sxs-lookup"><span data-stu-id="09182-109">Add missing Powerline glyphs</span></span>

## <a name="prerequisites"></a><span data-ttu-id="09182-110">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="09182-110">Prerequisites</span></span>

### <a name="install-a-powerline-font"></a><span data-ttu-id="09182-111">Installieren einer Powerline-Schriftart</span><span class="sxs-lookup"><span data-stu-id="09182-111">Install a Powerline font</span></span>

<span data-ttu-id="09182-112">Powerline verwendet Glyphen, um die Eingabeaufforderung zu formatieren.</span><span class="sxs-lookup"><span data-stu-id="09182-112">Powerline uses glyphs in order to style the prompt.</span></span> <span data-ttu-id="09182-113">Wenn Ihre Schriftart keine Powerline-Glyphen enthält, werden an der Eingabeaufforderung möglicherweise mehrere Unicode-Ersetzungszeichen „&#x25AF;“ angezeigt.</span><span class="sxs-lookup"><span data-stu-id="09182-113">If your font does not include Powerline glyphs, you may see several Unicode replacement characters '&#x25AF;' throughout your prompt.</span></span> <span data-ttu-id="09182-114">Obwohl [Cascadia Mono](./../cascadia-code.md) keine Powerline-Glyphen enthält, können Sie Cascadia Code PL oder Cascadia Mono PL installieren, die die Powerline-Glyphen enthalten.</span><span class="sxs-lookup"><span data-stu-id="09182-114">Though [Cascadia Mono](./../cascadia-code.md) does not include Powerline glyphs, you can install Cascadia Code PL or Cascadia Mono PL, which have the Powerline glyphs included.</span></span> <span data-ttu-id="09182-115">Diese Schriftarten können auf der GitHub-Seite mit [Cascadia Code-Versionen](https://github.com/microsoft/cascadia-code/releases) installiert werden.</span><span class="sxs-lookup"><span data-stu-id="09182-115">These fonts can be installed from the [Cascadia Code GitHub releases page](https://github.com/microsoft/cascadia-code/releases).</span></span>

## <a name="set-up-powerline-in-powershell"></a><span data-ttu-id="09182-116">Einrichten von Powerline in PowerShell</span><span class="sxs-lookup"><span data-stu-id="09182-116">Set up Powerline in PowerShell</span></span>

### <a name="powershell-prerequisites"></a><span data-ttu-id="09182-117">PowerShell-Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="09182-117">PowerShell prerequisites</span></span>

<span data-ttu-id="09182-118">Wenn Sie dies nicht bereits erledigt haben, [installieren Sie Git für Windows](https://git-scm.com/downloads).</span><span class="sxs-lookup"><span data-stu-id="09182-118">If you don't already have it, [install Git for Windows](https://git-scm.com/downloads).</span></span>

<span data-ttu-id="09182-119">Installieren Sie mit PowerShell Posh-Git und Oh-My-Posh:</span><span class="sxs-lookup"><span data-stu-id="09182-119">Using PowerShell, install Posh-Git and Oh-My-Posh:</span></span>

```powershell
Install-Module posh-git -Scope CurrentUser
Install-Module oh-my-posh -Scope CurrentUser
```

> [!TIP]
> <span data-ttu-id="09182-120">Möglicherweise müssen Sie NuGet installieren, wenn es auf Ihrem System noch nicht vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="09182-120">You may need to install NuGet if you don't already have it.</span></span> <span data-ttu-id="09182-121">Wenn dies der Fall ist, werden Sie in der PowerShell-Befehlszeile gefragt, ob Sie NuGet installieren möchten.</span><span class="sxs-lookup"><span data-stu-id="09182-121">Your PowerShell command line will ask if you want to install NuGet if this is the case.</span></span> <span data-ttu-id="09182-122">Wählen Sie [Y] (Ja) aus.</span><span class="sxs-lookup"><span data-stu-id="09182-122">Select [Y] Yes.</span></span> <span data-ttu-id="09182-123">Möglicherweise müssen Sie auch genehmigen, dass Module aus [PSGallery](https://docs.microsoft.com/powershell/scripting/gallery/getting-started?view=powershell-7), einem „nicht vertrauenswürdigen Repository“, installiert werden.</span><span class="sxs-lookup"><span data-stu-id="09182-123">You may also need to approve that you are installing modules from [PSGallery](https://docs.microsoft.com/powershell/scripting/gallery/getting-started?view=powershell-7), an 'untrusted repository'.</span></span> <span data-ttu-id="09182-124">Wählen Sie [Y] (Ja) aus.</span><span class="sxs-lookup"><span data-stu-id="09182-124">Select [Y] Yes.</span></span>

<span data-ttu-id="09182-125">[Posh-Git](https://github.com/dahlbyk/posh-git) fügt Git-Statusinformationen zu Ihrer Eingabeaufforderung sowie die Befehlszeilenergänzung für Git-Befehle, Parameter, Remotes und Branchnamen hinzu.</span><span class="sxs-lookup"><span data-stu-id="09182-125">[Posh-Git](https://github.com/dahlbyk/posh-git) adds Git status information to your prompt as well as tab-completion for Git commands, parameters, remotes, and branch names.</span></span> <span data-ttu-id="09182-126">[Oh-My-Posh](https://github.com/JanDeDobbeleer/oh-my-posh) bietet Designfunktionen für Ihre PowerShell-Eingabeaufforderung.</span><span class="sxs-lookup"><span data-stu-id="09182-126">[Oh-My-Posh](https://github.com/JanDeDobbeleer/oh-my-posh) provides theme capabilities for your PowerShell prompt.</span></span>

<span data-ttu-id="09182-127">Wenn Sie PowerShell Core verwenden, installieren Sie PSReadline:</span><span class="sxs-lookup"><span data-stu-id="09182-127">If you are using PowerShell Core, install PSReadline:</span></span>

```powershell
Install-Module -Name PSReadLine -Scope CurrentUser -Force -SkipPublisherCheck
```

<span data-ttu-id="09182-128">Mit [PSReadline](https://docs.microsoft.com/powershell/module/psreadline/?view=powershell-6) können Sie die Bearbeitungsumgebung für die Befehlszeile in PowerShell anpassen.</span><span class="sxs-lookup"><span data-stu-id="09182-128">[PSReadline](https://docs.microsoft.com/powershell/module/psreadline/?view=powershell-6) lets you customize the command line editing environment in PowerShell.</span></span>

### <a name="customize-your-powershell-prompt"></a><span data-ttu-id="09182-129">Anpassen der PowerShell-Eingabeaufforderung</span><span class="sxs-lookup"><span data-stu-id="09182-129">Customize your PowerShell prompt</span></span>

<span data-ttu-id="09182-130">Öffnen Sie Ihr PowerShell-Profil mit `notepad $PROFILE` oder dem Texteditor Ihrer Wahl.</span><span class="sxs-lookup"><span data-stu-id="09182-130">Open your PowerShell profile with `notepad $PROFILE` or the text editor of your choice.</span></span> <span data-ttu-id="09182-131">Dabei handelt es sich nicht um Ihr Windows Terminal-Profil.</span><span class="sxs-lookup"><span data-stu-id="09182-131">This is not your Windows Terminal profile.</span></span> <span data-ttu-id="09182-132">Ihr PowerShell-Profil ist ein Skript, das bei jedem Start von PowerShell ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="09182-132">Your PowerShell profile is a script that runs every time PowerShell starts.</span></span> <span data-ttu-id="09182-133">[Weitere Informationen zu PowerShell-Profilen](https://docs.microsoft.com/powershell/module/microsoft.powershell.core/about/about_profiles?view=powershell-7).</span><span class="sxs-lookup"><span data-stu-id="09182-133">[Learn more about PowerShell profiles](https://docs.microsoft.com/powershell/module/microsoft.powershell.core/about/about_profiles?view=powershell-7).</span></span>

<span data-ttu-id="09182-134">Fügen Sie in Ihrem PowerShell-Profil am Ende der Datei Folgendes hinzu:</span><span class="sxs-lookup"><span data-stu-id="09182-134">In your PowerShell profile, add the following to the end of the file:</span></span>

```powershell
Import-Module posh-git
Import-Module oh-my-posh
Set-Theme Paradox
```

<span data-ttu-id="09182-135">Nun beginnt jede neue Instanz mit dem Import von Posh-Git und Oh-My-Posh und legt dann das Paradox-Design von Oh-My-Posh fest.</span><span class="sxs-lookup"><span data-stu-id="09182-135">Now, each new instance starts by importing Posh-Git and Oh-My-Posh, then setting the Paradox theme from Oh-My-Posh.</span></span> <span data-ttu-id="09182-136">Oh-My-Posh verfügt über mehrere [integrierte Designs](https://github.com/JanDeDobbeleer/oh-my-posh#themes).</span><span class="sxs-lookup"><span data-stu-id="09182-136">Oh-My-Posh comes with several [built-in themes](https://github.com/JanDeDobbeleer/oh-my-posh#themes).</span></span>

### <a name="set-cascadia-code-pl-as-fontface-in-settings"></a><span data-ttu-id="09182-137">Festlegen von Cascadia Code PL als Schriftart in den Einstellungen</span><span class="sxs-lookup"><span data-stu-id="09182-137">Set Cascadia Code PL as fontFace in settings</span></span>

<span data-ttu-id="09182-138">Um die Schriftart Cascadia Code PL für die Nutzung in Powerline festzulegen (nach dem Herunterladen, Entzippen und Installieren auf dem System), müssen Sie Ihre [Profileinstellungen](../customize-settings/profile-settings.md) in Ihrer settings.json-Datei öffnen, indem Sie im Dropdownmenü von Windows Terminal **Einstellungen** (STRG+,) auswählen.</span><span class="sxs-lookup"><span data-stu-id="09182-138">To set the Cascadia Code PL font for use with PowerLine (after downloading, unzipping, and installing on your system), you will need to open your [profile settings](../customize-settings/profile-settings.md) in your settings.json file by selecting **Settings** (Ctrl+,) from your Windows Terminal drop-down menu.</span></span>

<span data-ttu-id="09182-139">Suchen Sie in der geöffneten settings.json-Datei das Windows PowerShell-Profil, und fügen Sie `"fontFace": "Cascadia Code PL"` hinzu, um Cascadia Code PL als Schriftart anzugeben.</span><span class="sxs-lookup"><span data-stu-id="09182-139">Once your settings.json file opens, find the Windows PowerShell profile and add: `"fontFace": "Cascadia Code PL"` to designate Cascadia Code PL as the font.</span></span> <span data-ttu-id="09182-140">Dadurch werden diese hübschen Cascadia Code Powerline-Glyphen bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="09182-140">This will provide those nice Cascadia Code Powerline glyphs.</span></span> <span data-ttu-id="09182-141">Die Änderung sollte in Ihrem Terminal sichtbar werden, sobald Sie im Editor **Speichern** auswählen.</span><span class="sxs-lookup"><span data-stu-id="09182-141">You should notice the change in your terminal as soon as you select **Save** in your editor.</span></span>

<span data-ttu-id="09182-142">Die settings.json-Datei mit Ihren Windows PowerShell-Profileinstellungen sollte jetzt wie folgt aussehen:</span><span class="sxs-lookup"><span data-stu-id="09182-142">Your Windows PowerShell profile settings.json file should now look like this:</span></span>

```json
{
    // Make changes here to the powershell.exe profile.
    "guid": "{61c54bbd-c2c6-5271-96e7-009a87ff44bf}",
    "name": "Windows PowerShell",
    "commandline": "powershell.exe",
    "fontFace": "Cascadia Code PL",
    "hidden": false
},
```

## <a name="set-up-powerline-in-wsl-ubuntu"></a><span data-ttu-id="09182-143">Einrichten von Powerline in WSL Ubuntu</span><span class="sxs-lookup"><span data-stu-id="09182-143">Set up Powerline in WSL Ubuntu</span></span>

### <a name="wsl-ubuntu-prerequisites"></a><span data-ttu-id="09182-144">Voraussetzungen für WSL Ubuntu</span><span class="sxs-lookup"><span data-stu-id="09182-144">WSL Ubuntu prerequisites</span></span>

<span data-ttu-id="09182-145">Ubuntu verfügt über mehrere Powerline-Optionen für die Installation.</span><span class="sxs-lookup"><span data-stu-id="09182-145">Ubuntu has several Powerline options to install from.</span></span> <span data-ttu-id="09182-146">In diesem Tutorial werden Go und Powerline-Go verwendet:</span><span class="sxs-lookup"><span data-stu-id="09182-146">This tutorial will be using Go and Powerline-Go:</span></span>

```bash
sudo apt install golang-go
go get -u github.com/justjanne/powerline-go
```

### <a name="customize-your-ubuntu-prompt"></a><span data-ttu-id="09182-147">Anpassen der Ubuntu-Eingabeaufforderung</span><span class="sxs-lookup"><span data-stu-id="09182-147">Customize your Ubuntu prompt</span></span>

<span data-ttu-id="09182-148">Öffnen Sie die `~/.bashrc`-Datei mit `nano ~/.bashrc` oder dem Text-Editor Ihrer Wahl.</span><span class="sxs-lookup"><span data-stu-id="09182-148">Open your `~/.bashrc` file with `nano ~/.bashrc` or the text editor of your choice.</span></span> <span data-ttu-id="09182-149">Dies ist ein Bash-Skript, das bei jedem Start von bash ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="09182-149">This is a bash script that runs every time bash starts.</span></span> <span data-ttu-id="09182-150">Fügen Sie Folgendes hinzu, aber beachten Sie, dass GOPATH möglicherweise bereits vorhanden ist:</span><span class="sxs-lookup"><span data-stu-id="09182-150">Add the following, though beware that GOPATH may already exist:</span></span>

```bash
GOPATH=$HOME/go
function _update_ps1() {
    PS1="$($GOPATH/bin/powerline-go -error $?)"
}
if [ "$TERM" != "linux" ] && [ -f "$GOPATH/bin/powerline-go" ]; then
    PROMPT_COMMAND="_update_ps1; $PROMPT_COMMAND"
fi
```

## <a name="additional-resources"></a><span data-ttu-id="09182-151">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="09182-151">Additional resources</span></span>

* [<span data-ttu-id="09182-152">Scott Hanselman „How to Make a Pretty prompt in Windows Terminal“ (Erstellen einer ansprechenden Eingabeaufforderung in Windows Terminal)</span><span class="sxs-lookup"><span data-stu-id="09182-152">Scott Hanselman's "How to make a pretty prompt in Windows Terminal"</span></span>](https://www.hanselman.com/blog/HowToMakeAPrettyPromptInWindowsTerminalWithPowerlineNerdFontsCascadiaCodeWSLAndOhmyposh.aspx)

* [<span data-ttu-id="09182-153">Ändern/Einrichten einer benutzerdefinierten bash-Eingabeaufforderung (PS1) unter Linux</span><span class="sxs-lookup"><span data-stu-id="09182-153">How to change/set up bash custom prompt (PS1) in Linux</span></span>](https://www.cyberciti.biz/tips/howto-linux-unix-bash-shell-setup-prompt.html)
