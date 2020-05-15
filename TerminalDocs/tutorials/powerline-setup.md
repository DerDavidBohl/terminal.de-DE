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
# <a name="tutorial-set-up-powerline-in-windows-terminal"></a>Tutorial: Einrichten von Powerline in Windows Terminal

Powerline bietet eine angepasste Erfahrung für die Eingabeaufforderung, die Farbcodierungen und Aufforderungen für den Git-Status bietet.

![Windows Terminal: Powerline in PowerShell](./../images/powerline-powershell.png)

In diesem Tutorial erfahren Sie, wie Sie die folgenden Aufgaben durchführen:

> [!div class="checklist"]
> * Einrichten von Powerline in PowerShell
> * Einrichten von Powerline in Ubuntu/WSL
> * Hinzufügen fehlender Powerline-Glyphen

## <a name="prerequisites"></a>Voraussetzungen

### <a name="install-a-powerline-font"></a>Installieren einer Powerline-Schriftart

Powerline verwendet Glyphen, um die Eingabeaufforderung zu formatieren. Wenn Ihre Schriftart keine Powerline-Glyphen enthält, werden an der Eingabeaufforderung möglicherweise mehrere Unicode-Ersetzungszeichen „“ angezeigt. Obwohl [Cascadia Mono](./../cascadia-code.md) keine Powerline-Glyphen enthält, können Sie Cascadia Code PL oder Cascadia Mono PL installieren, die die Powerline-Glyphen enthalten. Diese Schriftarten können auf der GitHub-Seite mit [Cascadia Code-Versionen](https://github.com/microsoft/cascadia-code/releases) installiert werden.

## <a name="set-up-powerline-in-powershell"></a>Einrichten von Powerline in PowerShell

### <a name="powershell-prerequisites"></a>PowerShell-Voraussetzungen

Wenn Sie dies nicht bereits erledigt haben, [installieren Sie Git für Windows](https://git-scm.com/downloads).

Installieren Sie mit PowerShell Posh-Git und Oh-My-Posh:

```powershell
Install-Module posh-git -Scope CurrentUser
Install-Module oh-my-posh -Scope CurrentUser
```

[Posh-Git](https://github.com/dahlbyk/posh-git) fügt Git-Statusinformationen zu Ihrer Eingabeaufforderung sowie die Befehlszeilenergänzung für Git-Befehle, Parameter, Remotes und Branchnamen hinzu. [Oh-My-Posh](https://github.com/JanDeDobbeleer/oh-my-posh) bietet Designfunktionen für Ihre PowerShell-Eingabeaufforderung.

Wenn Sie PowerShell Core verwenden, installieren Sie PSReadline:

```powershell
Install-Module -Name PSReadLine -AllowPrerelease -Scope CurrentUser -Force -SkipPublisherCheck
```

Mit [PSReadline](https://docs.microsoft.com/powershell/module/psreadline/?view=powershell-6) können Sie die Bearbeitungsumgebung für die Befehlszeile in PowerShell anpassen.

### <a name="customize-your-powershell-prompt"></a>Anpassen der PowerShell-Eingabeaufforderung

Öffnen Sie Ihr PowerShell-Profil mit `notepad $PROFILE` oder dem Texteditor Ihrer Wahl. Dabei handelt es sich nicht um Ihr Windows Terminal-Profil. Ihr PowerShell-Profil ist ein Skript, das bei jedem Start von PowerShell ausgeführt wird. [Weitere Informationen zu PowerShell-Profilen](https://docs.microsoft.com/powershell/module/microsoft.powershell.core/about/about_profiles?view=powershell-7).

Fügen Sie in Ihrem PowerShell-Profil am Ende der Datei Folgendes hinzu:

```powershell
Import-Module posh-git
Import-Module oh-my-posh
Set-Theme Paradox
```

Nun beginnt jede neue Instanz mit dem Import von Posh-Git und Oh-My-Posh und legt dann das Paradox-Design von Oh-My-Posh fest. Oh-My-Posh verfügt über mehrere [integrierte Designs](https://github.com/JanDeDobbeleer/oh-my-posh#themes).

## <a name="set-up-powerline-in-wsl-ubuntu"></a>Einrichten von Powerline in WSL Ubuntu

### <a name="wsl-ubuntu-prerequisites"></a>Voraussetzungen für WSL Ubuntu

Ubuntu verfügt über mehrere Powerline-Optionen für die Installation. In diesem Tutorial werden Go und Powerline-Go verwendet:

```bash
sudo apt install golang-go
go get -u github.com/justjanne/powerline-go
```

### <a name="customize-your-ubuntu-prompt"></a>Anpassen der Ubuntu-Eingabeaufforderung

Öffnen Sie die `~/.bashrc`-Datei mit `nano ~/.bashrc` oder dem Text-Editor Ihrer Wahl. Dies ist ein Bash-Skript, das bei jedem Start von bash ausgeführt wird. Fügen Sie Folgendes hinzu, aber beachten Sie, dass GOPATH möglicherweise bereits vorhanden ist:

```bash
GOPATH=$HOME/go
function _update_ps1() {
    PS1="$($GOPATH/bin/powerline-go -error $?)"
}
if [ "$TERM" != "linux" ] && [ -f "$GOPATH/bin/powerline-go" ]; then
    PROMPT_COMMAND="_update_ps1; $PROMPT_COMMAND"
fi
```

## <a name="additional-resources"></a>Zusätzliche Ressourcen

* [Scott Hanselman „How to Make a Pretty prompt in Windows Terminal“ (Erstellen einer ansprechenden Eingabeaufforderung in Windows Terminal)](https://www.hanselman.com/blog/HowToMakeAPrettyPromptInWindowsTerminalWithPowerlineNerdFontsCascadiaCodeWSLAndOhmyposh.aspx)

* [Ändern/Einrichten einer benutzerdefinierten bash-Eingabeaufforderung (PS1) unter Linux](https://www.cyberciti.biz/tips/howto-linux-unix-bash-shell-setup-prompt.html)
