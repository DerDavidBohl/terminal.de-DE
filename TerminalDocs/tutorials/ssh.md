---
title: 'Windows Terminal: SSH'
description: In diesem Tutorial erfahren Sie, wie Sie eine SSH-Verbindung in Windows Terminal einrichten.
author: cinnamon-msft
ms.author: cinnamon
ms.date: 05/19/2020
ms.topic: tutorial
ms.service: terminal
ms.openlocfilehash: c418460cd47935ed8b8eb57ebdb89322d543a20e
ms.sourcegitcommit: bb5b7fd7db4b81e0d44e060989dc16b6775c802a
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/15/2020
ms.locfileid: "83415865"
---
# <a name="tutorial-ssh-in-windows-terminal"></a><span data-ttu-id="f92fb-103">Tutorial: SSH in Windows Terminal</span><span class="sxs-lookup"><span data-stu-id="f92fb-103">Tutorial: SSH in Windows Terminal</span></span>

<span data-ttu-id="f92fb-104">Windows 10 verfügt über einen integrierten SSH-Client, den Sie in Windows Terminal verwenden können.</span><span class="sxs-lookup"><span data-stu-id="f92fb-104">Windows 10 has a build-in SSH client that you can use in the Windows Terminal.</span></span>

<span data-ttu-id="f92fb-105">In diesem Tutorial erfahren Sie, wie Sie ein Profil in Windows Terminal einrichten, das SSH verwendet.</span><span class="sxs-lookup"><span data-stu-id="f92fb-105">In this tutorial, you'll learn how to set up a profile in Windows Terminal that uses SSH.</span></span>

## <a name="create-a-profile"></a><span data-ttu-id="f92fb-106">Erstellen eines Profils</span><span class="sxs-lookup"><span data-stu-id="f92fb-106">Create a profile</span></span>

<span data-ttu-id="f92fb-107">Sie können eine SSH-Sitzung über die Eingabeaufforderung starten, indem Sie `ssh user@machine` ausführen. Sie werden dann aufgefordert, Ihr Kennwort einzugeben.</span><span class="sxs-lookup"><span data-stu-id="f92fb-107">You can start an SSH session in your command prompt by executing `ssh user@machine` and you will be prompted to enter your password.</span></span> <span data-ttu-id="f92fb-108">Sie können ein Windows Terminal-Profil erstellen, das dies beim Start erledigt, indem Sie die Einstellung `commandline` zu einem Profil in Ihrer Datei „settings.json“ hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="f92fb-108">You can create a Windows Terminal profile that does this on startup by adding the `commandline` setting to a profile in your settings.json file.</span></span>

```js
"commandline": "ssh cinnamon@roll"
```

## <a name="resources"></a><span data-ttu-id="f92fb-109">Ressourcen</span><span class="sxs-lookup"><span data-stu-id="f92fb-109">Resources</span></span>

* [<span data-ttu-id="f92fb-110">Aktivieren und Verwenden der neuen integrierten SSH-Befehle in Windows 10</span><span class="sxs-lookup"><span data-stu-id="f92fb-110">How to Enable and Use Windows 10’s New Built-in SSH Commands</span></span>](https://www.howtogeek.com/336775/how-to-enable-and-use-windows-10s-built-in-ssh-commands/)
