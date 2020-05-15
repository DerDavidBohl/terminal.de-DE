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
# <a name="new-terminal-arguments-in-the-windows-terminal"></a><span data-ttu-id="f7dab-103">Neue Terminalargumente in Windows Terminal</span><span class="sxs-lookup"><span data-stu-id="f7dab-103">New Terminal Arguments in the Windows Terminal</span></span>

<span data-ttu-id="f7dab-104">Wenn Sie einen neuen Bereich oder eine neue Registerkarte mit einer Tastenzuordnung öffnen, können Sie angeben, welches Profil verwendet wird, indem Sie den Namen, die GUID oder den Index des Profils angeben.</span><span class="sxs-lookup"><span data-stu-id="f7dab-104">When opening a new pane or tab with a key binding, you can specify which profile is used by including the profile's name, guid, or index.</span></span> <span data-ttu-id="f7dab-105">Wenn Sie keinen dieser Werte angegeben, wird das Standardprofil verwendet.</span><span class="sxs-lookup"><span data-stu-id="f7dab-105">If none are specified, the default profile is used.</span></span> <span data-ttu-id="f7dab-106">Dies kann durch Hinzufügen von `profile` oder `index` als Argument zu einer `splitPane`- oder `newTab`-Tastenzuordnung erfolgen.</span><span class="sxs-lookup"><span data-stu-id="f7dab-106">This can be done by adding `profile` or `index` as an argument to a `splitPane` or `newTab` key binding.</span></span> <span data-ttu-id="f7dab-107">Beachten Sie, dass die Indizierung bei 0 beginnt.</span><span class="sxs-lookup"><span data-stu-id="f7dab-107">Note that indexing starts at 0.</span></span>

```json
{ "command": { "action": "splitPane", "split": "vertical", "profile": "profile1" }, "keys": "ctrl+a" },
{ "command": { "action": "splitPane", "split": "vertical", "profile": "{00000000-0000-0000-0000-000000000000}" }, "keys": "ctrl+b" },
{ "command": { "action": "newTab", "index": 0 }, "keys": "ctrl+c" }
```

<span data-ttu-id="f7dab-108">Zusätzlich können Sie bestimmte Aspekte des Profils außer Kraft setzen, z. B. die ausführbare Befehlszeilendatei des Profils, das Startverzeichnis oder den Registerkartentitel.</span><span class="sxs-lookup"><span data-stu-id="f7dab-108">Additionally, you can override certain aspects of the profile such as the profile's command line executable, starting directory, or tab title.</span></span> <span data-ttu-id="f7dab-109">Dies kann durch Hinzufügen von `commandline`, `startingDirectory` und/oder `tabTitle` zu einer `splitPane` oder `newTab` Tastenzuordnung erreicht werden.</span><span class="sxs-lookup"><span data-stu-id="f7dab-109">This can be accomplished by adding `commandline`, `startingDirectory`, and/or `tabTitle` to a `splitPane` or `newTab` key binding.</span></span>

```json
{ "command": { "action": "splitPane", "split": "auto", "profile": "profile1", "commandline": "foo.exe" }, "keys": "ctrl+a" },
{ "command": { "action": "newTab", "profile": "{00000000-0000-0000-0000-000000000000}", "startingDirectory": "C:\\foo" }, "keys": "ctrl+b" },
{ "command": { "action": "newTab", "index": 0, "tabTitle": "bar", "startingDirectory": "C:\\foo", "commandline": "foo.exe" }, "keys": "ctrl+c" }
```
