---
title: 'Windows Terminal: Powerline-Setup'
description: In diesem Tutorial erfahren Sie, wie Sie Powerline in Windows Terminal einrichten.
author: cinnamon-msft
ms.author: cinnamon
ms.date: 05/19/2020
ms.topic: tutorial
ms.service: terminal
ms.openlocfilehash: f2004927097b13ba896b628bea0d7bd9f70d7266
ms.sourcegitcommit: bb5b7fd7db4b81e0d44e060989dc16b6775c802a
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/15/2020
ms.locfileid: "83416265"
---
# <a name="tutorial-set-up-powerline-in-windows-terminal"></a><span data-ttu-id="0c186-103">Tutorial: Einrichten von Powerline in Windows Terminal</span><span class="sxs-lookup"><span data-stu-id="0c186-103">Tutorial: Set up Powerline in Windows Terminal</span></span>

<span data-ttu-id="0c186-104">Powerline bietet eine angepasste Erfahrung für die Eingabeaufforderung, die Farbcodierungen und Aufforderungen für den Git-Status bietet.</span><span class="sxs-lookup"><span data-stu-id="0c186-104">Powerline provides a customized command prompt experience providing Git status color-coding and prompts.</span></span>

![Windows Terminal: Powerline in PowerShell](./../images/powerline-powershell.png)

<span data-ttu-id="0c186-106">In diesem Tutorial erfahren Sie, wie Sie die folgenden Aufgaben durchführen:</span><span class="sxs-lookup"><span data-stu-id="0c186-106">In this tutorial, you learn how to:</span></span>

> [!div class="checklist"]
> * <span data-ttu-id="0c186-107">Einrichten von Powerline in PowerShell</span><span class="sxs-lookup"><span data-stu-id="0c186-107">Set up Powerline in PowerShell</span></span>
> * <span data-ttu-id="0c186-108">Einrichten von Powerline in Ubuntu/WSL</span><span class="sxs-lookup"><span data-stu-id="0c186-108">Set up Powerline in Ubuntu/WSL</span></span>
> * <span data-ttu-id="0c186-109">Hinzufügen fehlender Powerline-Glyphen</span><span class="sxs-lookup"><span data-stu-id="0c186-109">Add missing Powerline glyphs</span></span>

## <a name="prerequisites"></a><span data-ttu-id="0c186-110">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="0c186-110">Prerequisites</span></span>

### <a name="install-a-powerline-font"></a><span data-ttu-id="0c186-111">Installieren einer Powerline-Schriftart</span><span class="sxs-lookup"><span data-stu-id="0c186-111">Install a Powerline font</span></span>

<span data-ttu-id="0c186-112">Powerline verwendet Glyphen, um die Eingabeaufforderung zu formatieren.</span><span class="sxs-lookup"><span data-stu-id="0c186-112">Powerline uses glyphs in order to style the prompt.</span></span> <span data-ttu-id="0c186-113">Wenn Ihre Schriftart keine Powerline-Glyphen enthält, werden an der Eingabeaufforderung möglicherweise mehrere Unicode-Ersetzungszeichen „“ angezeigt.</span><span class="sxs-lookup"><span data-stu-id="0c186-113">If your font does not include Powerline glyphs, you may see several Unicode replacement characters '' throughout your prompt.</span></span> <span data-ttu-id="0c186-114">Obwohl [Cascadia Mono](./../cascadia-code.md) keine Powerline-Glyphen enthält, können Sie Cascadia Code PL oder Cascadia Mono PL installieren, die die Powerline-Glyphen enthalten.</span><span class="sxs-lookup"><span data-stu-id="0c186-114">Though [Cascadia Mono](./../cascadia-code.md) does not include Powerline glyphs, you can install Cascadia Code PL or Cascadia Mono PL, which have the Powerline glyphs included.</span></span> <span data-ttu-id="0c186-115">Diese Schriftarten können auf der GitHub-Seite mit [Cascadia Code-Versionen](https://github.com/microsoft/cascadia-code/releases) installiert werden.</span><span class="sxs-lookup"><span data-stu-id="0c186-115">These fonts can be installed from the [Cascadia Code GitHub releases page](https://github.com/microsoft/cascadia-code/releases).</span></span>

## <a name="set-up-powerline-in-powershell"></a><span data-ttu-id="0c186-116">Einrichten von Powerline in PowerShell</span><span class="sxs-lookup"><span data-stu-id="0c186-116">Set up Powerline in PowerShell</span></span>

### <a name="powershell-prerequisites"></a><span data-ttu-id="0c186-117">PowerShell-Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="0c186-117">PowerShell prerequisites</span></span>

<span data-ttu-id="0c186-118">Wenn Sie dies nicht bereits erledigt haben, [installieren Sie Git für Windows](https://git-scm.com/downloads).</span><span class="sxs-lookup"><span data-stu-id="0c186-118">If you don't already have it, [install Git for Windows](https://git-scm.com/downloads).</span></span>

<span data-ttu-id="0c186-119">Installieren Sie mit PowerShell Posh-Git und Oh-My-Posh:</span><span class="sxs-lookup"><span data-stu-id="0c186-119">Using PowerShell, install Posh-Git and Oh-My-Posh:</span></span>

```powershell
Install-Module posh-git -Scope CurrentUser
Install-Module oh-my-posh -Scope CurrentUser
```

<span data-ttu-id="0c186-120">[Posh-Git](https://github.com/dahlbyk/posh-git) fügt Git-Statusinformationen zu Ihrer Eingabeaufforderung sowie die Befehlszeilenergänzung für Git-Befehle, Parameter, Remotes und Branchnamen hinzu.</span><span class="sxs-lookup"><span data-stu-id="0c186-120">[Posh-Git](https://github.com/dahlbyk/posh-git) adds Git status information to your prompt as well as tab-completion for Git commands, parameters, remotes, and branch names.</span></span> <span data-ttu-id="0c186-121">[Oh-My-Posh](https://github.com/JanDeDobbeleer/oh-my-posh) bietet Designfunktionen für Ihre PowerShell-Eingabeaufforderung.</span><span class="sxs-lookup"><span data-stu-id="0c186-121">[Oh-My-Posh](https://github.com/JanDeDobbeleer/oh-my-posh) provides theme capabilities for your PowerShell prompt.</span></span>

<span data-ttu-id="0c186-122">Wenn Sie PowerShell Core verwenden, installieren Sie PSReadline:</span><span class="sxs-lookup"><span data-stu-id="0c186-122">If you are using PowerShell Core, install PSReadline:</span></span>

```powershell
Install-Module -Name PSReadLine -AllowPrerelease -Scope CurrentUser -Force -SkipPublisherCheck
```

<span data-ttu-id="0c186-123">Mit [PSReadline](https://docs.microsoft.com/powershell/module/psreadline/?view=powershell-6) können Sie die Bearbeitungsumgebung für die Befehlszeile in PowerShell anpassen.</span><span class="sxs-lookup"><span data-stu-id="0c186-123">[PSReadline](https://docs.microsoft.com/powershell/module/psreadline/?view=powershell-6) lets you customize the command line editing environment in PowerShell.</span></span>

### <a name="customize-your-powershell-prompt"></a><span data-ttu-id="0c186-124">Anpassen der PowerShell-Eingabeaufforderung</span><span class="sxs-lookup"><span data-stu-id="0c186-124">Customize your PowerShell prompt</span></span>

<span data-ttu-id="0c186-125">Öffnen Sie Ihr PowerShell-Profil mit `notepad $PROFILE` oder dem Texteditor Ihrer Wahl.</span><span class="sxs-lookup"><span data-stu-id="0c186-125">Open your PowerShell profile with `notepad $PROFILE` or the text editor of your choice.</span></span> <span data-ttu-id="0c186-126">Dabei handelt es sich nicht um Ihr Windows Terminal-Profil.</span><span class="sxs-lookup"><span data-stu-id="0c186-126">This is not your Windows Terminal profile.</span></span> <span data-ttu-id="0c186-127">Ihr PowerShell-Profil ist ein Skript, das bei jedem Start von PowerShell ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0c186-127">Your PowerShell profile is a script that runs every time PowerShell starts.</span></span> <span data-ttu-id="0c186-128">[Weitere Informationen zu PowerShell-Profilen](https://docs.microsoft.com/powershell/module/microsoft.powershell.core/about/about_profiles?view=powershell-7).</span><span class="sxs-lookup"><span data-stu-id="0c186-128">[Learn more about PowerShell profiles](https://docs.microsoft.com/powershell/module/microsoft.powershell.core/about/about_profiles?view=powershell-7).</span></span>

<span data-ttu-id="0c186-129">Fügen Sie in Ihrem PowerShell-Profil am Ende der Datei Folgendes hinzu:</span><span class="sxs-lookup"><span data-stu-id="0c186-129">In your PowerShell profile, add the following to the end of the file:</span></span>

```powershell
Import-Module posh-git
Import-Module oh-my-posh
Set-Theme Paradox
```

<span data-ttu-id="0c186-130">Nun beginnt jede neue Instanz mit dem Import von Posh-Git und Oh-My-Posh und legt dann das Paradox-Design von Oh-My-Posh fest.</span><span class="sxs-lookup"><span data-stu-id="0c186-130">Now, each new instance starts by importing Posh-Git and Oh-My-Posh, then setting the Paradox theme from Oh-My-Posh.</span></span> <span data-ttu-id="0c186-131">Oh-My-Posh verfügt über mehrere [integrierte Designs](https://github.com/JanDeDobbeleer/oh-my-posh#themes).</span><span class="sxs-lookup"><span data-stu-id="0c186-131">Oh-My-Posh comes with several [built-in themes](https://github.com/JanDeDobbeleer/oh-my-posh#themes).</span></span>

## <a name="set-up-powerline-in-wsl-ubuntu"></a><span data-ttu-id="0c186-132">Einrichten von Powerline in WSL Ubuntu</span><span class="sxs-lookup"><span data-stu-id="0c186-132">Set up Powerline in WSL Ubuntu</span></span>

### <a name="wsl-ubuntu-prerequisites"></a><span data-ttu-id="0c186-133">Voraussetzungen für WSL Ubuntu</span><span class="sxs-lookup"><span data-stu-id="0c186-133">WSL Ubuntu prerequisites</span></span>

<span data-ttu-id="0c186-134">Ubuntu verfügt über mehrere Powerline-Optionen für die Installation.</span><span class="sxs-lookup"><span data-stu-id="0c186-134">Ubuntu has several Powerline options to install from.</span></span> <span data-ttu-id="0c186-135">In diesem Tutorial werden Go und Powerline-Go verwendet:</span><span class="sxs-lookup"><span data-stu-id="0c186-135">This tutorial will be using Go and Powerline-Go:</span></span>

```bash
sudo apt install golang-go
go get -u github.com/justjanne/powerline-go
```

### <a name="customize-your-ubuntu-prompt"></a><span data-ttu-id="0c186-136">Anpassen der Ubuntu-Eingabeaufforderung</span><span class="sxs-lookup"><span data-stu-id="0c186-136">Customize your Ubuntu prompt</span></span>

<span data-ttu-id="0c186-137">Öffnen Sie die `~/.bashrc`-Datei mit `nano ~/.bashrc` oder dem Text-Editor Ihrer Wahl.</span><span class="sxs-lookup"><span data-stu-id="0c186-137">Open your `~/.bashrc` file with `nano ~/.bashrc` or the text editor of your choice.</span></span> <span data-ttu-id="0c186-138">Dies ist ein Bash-Skript, das bei jedem Start von bash ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0c186-138">This is a bash script that runs every time bash starts.</span></span> <span data-ttu-id="0c186-139">Fügen Sie Folgendes hinzu, aber beachten Sie, dass GOPATH möglicherweise bereits vorhanden ist:</span><span class="sxs-lookup"><span data-stu-id="0c186-139">Add the following, though beware that GOPATH may already exist:</span></span>

```bash
GOPATH=$HOME/go
function _update_ps1() {
    PS1="$($GOPATH/bin/powerline-go -error $?)"
}
if [ "$TERM" != "linux" ] && [ -f "$GOPATH/bin/powerline-go" ]; then
    PROMPT_COMMAND="_update_ps1; $PROMPT_COMMAND"
fi
```

## <a name="additional-resources"></a><span data-ttu-id="0c186-140">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="0c186-140">Additional resources</span></span>

* [<span data-ttu-id="0c186-141">Scott Hanselman „How to Make a Pretty prompt in Windows Terminal“ (Erstellen einer ansprechenden Eingabeaufforderung in Windows Terminal)</span><span class="sxs-lookup"><span data-stu-id="0c186-141">Scott Hanselman's "How to make a pretty prompt in Windows Terminal"</span></span>](https://www.hanselman.com/blog/HowToMakeAPrettyPromptInWindowsTerminalWithPowerlineNerdFontsCascadiaCodeWSLAndOhmyposh.aspx)

* [<span data-ttu-id="0c186-142">Ändern/Einrichten einer benutzerdefinierten bash-Eingabeaufforderung (PS1) unter Linux</span><span class="sxs-lookup"><span data-stu-id="0c186-142">How to change/set up bash custom prompt (PS1) in Linux</span></span>](https://www.cyberciti.biz/tips/howto-linux-unix-bash-shell-setup-prompt.html)
