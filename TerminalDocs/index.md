---
title: 'Windows Terminal: Übersicht'
description: Erfahren Sie mehr über Windows Terminal und wie es den Befehlszeilenworkflow verbessern kann.
author: cinnamon-msft
ms.author: cinnamon
ms.date: 05/19/2020
ms.topic: overview
ms.service: terminal
ms.localizationpriority: high
ms.openlocfilehash: ab29130e34e6d3adbda37a002a03383211d27bce
ms.sourcegitcommit: a77ad8aec5bbeba1e58a92c49dc2ebd67a426ae7
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/26/2020
ms.locfileid: "83866362"
---
# <a name="what-is-windows-terminal"></a>Informationen zu Windows Terminal

Windows Terminal ist eine moderne Terminalanwendung für Benutzer von Befehlszeilentools und Shells wie die Eingabeaufforderung, PowerShell und das Windows-Subsystem für Linux (WSL). Zu den Hauptmerkmalen gehören mehrere Registerkarten, Bereiche, Unterstützung für Unicode- und UTF-8-Zeichen, eine GPU-beschleunigte Engine zum Rendern von Text sowie die Möglichkeit, eigene Designs zu erstellen und Text, Farben, Hintergründe und Tastenzuordnungen anzupassen.

![Screenshot zu Windows Terminal](./images/overview.png)

> [!NOTE]
> [Worin besteht der Unterschied zwischen einer Konsole, einem Terminal und einer Shell?](https://www.hanselman.com/blog/WhatsTheDifferenceBetweenAConsoleATerminalAndAShell.aspx) Lesen Sie die Erläuterung von Scott Hanselman.

## <a name="multiple-profiles-supporting-a-variety-of-command-line-applications"></a>Mehrere Profile, die eine Vielzahl von Befehlszeilenanwendungen unterstützen

Jede Anwendung, die über eine Befehlszeilenschnittstelle verfügt, kann in Windows Terminal ausgeführt werden. Dies umfasst alles von PowerShell und der Eingabeaufforderung bis hin zu Azure Cloud Shell und beliebigen WSL-Distributionen wie Ubuntu oder Oh-My-Zsh.

## <a name="customized-schemes-and-configurations"></a>Angepasste Schemas und Konfigurationen

Sie können Ihr Windows Terminal so konfigurieren, dass es über eine Vielzahl von Farbschemas und Einstellungen verfügt. Besuchen Sie die Seite [Farbschemas](./customize-settings/color-schemes.md), um zu erfahren, wie Sie Ihr eigenes Farbschema erstellen können. Benutzerdefinierte Terminalkonfigurationen finden Sie auch im [Katalog für benutzerdefiniertes Terminal](./custom-terminal-gallery/powerline-in-powershell.md).

## <a name="custom-key-bindings"></a>Benutzerdefinierte Tastenzuordnungen

Es gibt eine Vielzahl von benutzerdefinierten Tastenzuordnungen, die Sie in Windows Terminal verwenden können, damit es sich für Sie natürlicher anfühlt. Wenn Ihnen eine bestimmte Tastenzuordnung nicht gefällt, können Sie sie nach Belieben ändern.

Beispielsweise ist die standardmäßige Tastenkombination zum Kopieren von Text über die Befehlszeile <kbd>STRG+UMSCHALT+C</kbd>. Sie können dies in <kbd>STRG+1</kbd> (oder was immer Sie bevorzugen) ändern. Die Standardtastenkombination zum Öffnen einer neuen Registerkarte ist <kbd>STRG+UMSCHALT+T</kbd>, aber vielleicht möchten Sie dies in <kbd>STRG+2</kbd> ändern. Die Standardtastenkombination für den Wechsel zwischen den geöffneten Registerkarten ist <kbd>STRG+TAB</kbd>. Dies kann aber in <kbd>STRG+-</kbd> geändert verwendet werden, und stattdessen zum Erstellen einer neuen Registerkarte verwendet werden.

Weitere Informationen zum Anpassen der Tastenzuordnungen finden Sie auf der Seite [Tastenzuordnungen](./customize-settings/key-bindings.md).

## <a name="unicode-and-utf-8-character-support"></a>Unterstützung für Unicode- und UTF-8-Zeichen

Windows Terminal kann Unicode- und UTF-8-Zeichen (z. B. Emoji und Zeichen aus einer Vielzahl von Sprachen) anzeigen.

## <a name="gpu-accelerated-text-rendering"></a>Beschleunigtes GPU-Textrendering

Windows Terminal verwendet die GPU zum Rendern des Texts und bietet somit eine bessere Leistung im Vergleich zur standardmäßigen Windows-Befehlszeilenumgebung.

## <a name="background-image-support"></a>Unterstützung für Hintergrundbilder

Sie können Hintergrundbilder und GIF-Dateien in Ihrem Windows Terminal-Fenster verwenden. Informationen zum Hinzufügen von Hintergrundbildern zu Ihrem Profil finden Sie auf der Seite [Profileinstellungen](./customize-settings/profile-settings.md#background-image-settings).

## <a name="command-line-arguments"></a>Befehlszeilenargumente

Sie können Windows Terminal mithilfe von Befehlszeilenargumenten so einstellen, dass es in einer bestimmten Konfiguration startet. Sie können angeben, welches Profil in einer neuen Registerkarte geöffnet werden soll, das auszuwählende Ordnerverzeichnis angeben, das Terminal mit geteilten Fensterbereichen öffnen und auswählen, welche Registerkarte den Fokus erhalten soll.

Wenn Sie z. B. Windows Terminal von PowerShell aus mit drei Bereichen öffnen möchten, wobei im linken Bereich ein Eingabeaufforderungsprofil ausgeführt wird und der rechte Bereich zwischen Ihrem PowerShell- und Ihrem WSL ausführenden Standardprofil aufgeteilt ist, geben Sie Folgendes ein:

```bash
wt -p "Command Prompt" `; split-pane -p "Windows PowerShell" `; split-pane -H wsl.exe
```

Weitere Informationen zum Einrichten von Befehlszeilenargumenten finden Sie auf der Seite [Befehlszeilenargumente](./command-line-arguments.md).
