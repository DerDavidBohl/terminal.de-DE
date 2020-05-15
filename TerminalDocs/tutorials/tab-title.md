---
title: 'Windows Terminal: Einrichten der Registerkartentitel'
description: In diesem Tutorial erfahren Sie, wie Sie die Registerkartentitel in Windows Terminal einrichten.
author: cinnamon-msft
ms.author: cinnamon
ms.date: 05/19/2020
ms.topic: tutorial
ms.service: terminal
ms.openlocfilehash: 94c0d9afc8ccd3d95a3f52f5f9f6bdd0cb05bc12
ms.sourcegitcommit: bb5b7fd7db4b81e0d44e060989dc16b6775c802a
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/15/2020
ms.locfileid: "83416465"
---
# <a name="tutorial-configure-tab-titles-in-windows-terminal"></a>Tutorial: Konfigurieren von Registerkartentiteln in Windows Terminal

Standardmäßig wird der Registerkartentitel auf den Titel der Shell festgelegt. Wenn eine Registerkarte aus mehreren Bereichen besteht, wird der Registerkartentitel auf den Titel des aktuellen Fokusbereichs festgelegt. Wenn Sie den festgelegten Registerkartentitel ändern möchten, befolgen Sie die Anweisungen in diesem Tutorial.

In diesem Tutorial erfahren Sie, wie Sie die folgenden Aufgaben durchführen:

> [!div class="checklist"]
> * Verwenden der `tabTitle`-Einstellung
> * Festlegen des Titels der Shell
> * Verwenden der `suppressApplicationTitle`-Einstellung

## <a name="use-the-tabtitle-setting"></a>Verwenden der `tabTitle`-Einstellung

Mit der `tabTitle`-Einstellung können Sie den Starttitel für eine neue Instanz einer Shell definieren. Wenn die Einstellung nicht festgelegt ist, wird stattdessen das Profil `name` verwendet. Jede Shell reagiert anders auf diese Einstellung.

| Shell | Verhalten |
| ----- | -------- |
| PowerShell | Der Titel ist festgelegt. |
| Eingabeaufforderung ein | Der Titel ist festgelegt. Wenn ein Befehl ausgeführt wird, wird er temporär am Ende des Titels angefügt. |
| Ubuntu | Der Titel wird ignoriert und stattdessen auf `user@machine:path` festgelegt. |
| Debian | Der Titel ist festgelegt. |

> [!NOTE]
> Obwohl Ubuntu und Debian beide bash ausführen, haben sie unterschiedliche Verhaltensweisen. Damit soll gezeigt werden, dass unterschiedliche Distributionen unterschiedliche Verhaltensweisen aufweisen können.

## <a name="set-the-shells-title"></a>Festlegen des Titels der Shell

Eine Shell hat die volle Kontrolle über ihren eigenen Titel. Allerdings legt jede Shell ihren Titel anders fest.

| Shell | Befehl |
| ----- | ------- |
| PowerShell | `$Host.UI.RawUI.WindowTitle = "New Title"` |
| Eingabeaufforderung ein | `TITLE "New Title"` |
| bash* | `echo -ne "\033]0;New Title\a"` |

Beachten Sie, dass einige Linux-Distributionen (z. B. Ubuntu) ihren Titel automatisch festlegen, wenn Sie mit der Shell interagieren. Wenn der obige Befehl nicht funktioniert, führen Sie den folgenden Befehl aus:

```bash
PS1=$
PROMPT_COMMAND=
echo -ne "\033]0;New Title\a"
```

Dadurch wird der Titel in „Neuer Titel“ geändert und die Eingabeaufforderung auf „$“ festgelegt.

## <a name="use-the-suppressapplicationtitle-setting"></a>Verwenden der `suppressApplicationTitle`-Einstellung

Da eine Shell die Kontrolle über ihren Titel hat, kann sie den Registerkartentitel jederzeit überschreiben. Das Modul `posh-git` für PowerShell fügt z. B. Informationen zu Ihrem Git-Repository zum Titel hinzu.

Windows Terminal ermöglicht es Ihnen, Änderungen am Titel zu unterdrücken, indem Sie in Ihrem Profil `suppressApplicationTitle` auf `true` festlegen. Dadurch legen neue Instanzen des Profils Ihren sichtbaren Titel auf `tabTitle` fest. Wenn `tabTitle` nicht festgelegt ist, wird der sichtbare Titel auf den `name` des Profils festgelegt.

Beachten Sie, dass dies den Titel der Shell von dem auf der Registerkarte angezeigten sichtbaren Titel entkoppelt. Wenn Sie die Variable der Shell lesen, in der der Titel festgelegt ist, kann sie sich vom Titel der Registerkarte unterscheiden.

## <a name="resources"></a>Ressourcen

* [Festlegen des Konsolentitels als aktuelles Arbeitsverzeichnis](https://devblogs.microsoft.com/powershell/setting-the-console-title-to-be-your-current-working-directory/)
* [Ändern des Titels eines Terminals unter Ubuntu 16.04](https://www.zachpfeffer.com/single-post/Change-the-title-of-a-terminal-on-Ubuntu-1604)
