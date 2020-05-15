---
title: Neue Terminalargumente in Windows Terminal
description: Neue Terminalargumente in Windows Terminal.
author: cinnamon-msft
ms.author: cinnamon
ms.date: 05/19/2020
ms.topic: include
ms.service: terminal
ms.openlocfilehash: 4430124e3f9319e79cbf7b097d8743543c1d52a6
ms.sourcegitcommit: bb5b7fd7db4b81e0d44e060989dc16b6775c802a
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/15/2020
ms.locfileid: "83416315"
---
# <a name="new-terminal-arguments-in-the-windows-terminal"></a>Neue Terminalargumente in Windows Terminal

Wenn Sie einen neuen Bereich oder eine neue Registerkarte mit einer Tastenzuordnung öffnen, können Sie angeben, welches Profil verwendet wird, indem Sie den Namen, die GUID oder den Index des Profils angeben. Wenn Sie keinen dieser Werte angegeben, wird das Standardprofil verwendet. Dies kann durch Hinzufügen von `profile` oder `index` als Argument zu einer `splitPane`- oder `newTab`-Tastenzuordnung erfolgen. Beachten Sie, dass die Indizierung bei 0 beginnt.

```json
{ "command": { "action": "splitPane", "split": "vertical", "profile": "profile1" }, "keys": "ctrl+a" },
{ "command": { "action": "splitPane", "split": "vertical", "profile": "{00000000-0000-0000-0000-000000000000}" }, "keys": "ctrl+b" },
{ "command": { "action": "newTab", "index": 0 }, "keys": "ctrl+c" }
```

Zusätzlich können Sie bestimmte Aspekte des Profils außer Kraft setzen, z. B. die ausführbare Befehlszeilendatei des Profils, das Startverzeichnis oder den Registerkartentitel. Dies kann durch Hinzufügen von `commandline`, `startingDirectory` und/oder `tabTitle` zu einer `splitPane` oder `newTab` Tastenzuordnung erreicht werden.

```json
{ "command": { "action": "splitPane", "split": "auto", "profile": "profile1", "commandline": "foo.exe" }, "keys": "ctrl+a" },
{ "command": { "action": "newTab", "profile": "{00000000-0000-0000-0000-000000000000}", "startingDirectory": "C:\\foo" }, "keys": "ctrl+b" },
{ "command": { "action": "newTab", "index": 0, "tabTitle": "bar", "startingDirectory": "C:\\foo", "commandline": "foo.exe" }, "keys": "ctrl+c" }
```
