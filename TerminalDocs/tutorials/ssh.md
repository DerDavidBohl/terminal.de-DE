---
title: 'Windows Terminal: SSH'
description: In diesem Tutorial erfahren Sie, wie Sie eine SSH-Verbindung in Windows Terminal einrichten.
author: cinnamon-msft
ms.author: cinnamon
ms.date: 05/19/2020
ms.topic: tutorial
ms.service: terminal
ms.openlocfilehash: 02f4704b81cd0d287c207f0138ef27c537929711
ms.sourcegitcommit: bae07a8dd2010a95de4d53b1465abe226e4ad18e
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/26/2020
ms.locfileid: "83856338"
---
# <a name="tutorial-ssh-in-windows-terminal"></a><span data-ttu-id="fea44-103">Tutorial: SSH in Windows Terminal</span><span class="sxs-lookup"><span data-stu-id="fea44-103">Tutorial: SSH in Windows Terminal</span></span>

<span data-ttu-id="fea44-104">Windows 10 verfügt über einen integrierten SSH-Client, den Sie in Windows Terminal verwenden können.</span><span class="sxs-lookup"><span data-stu-id="fea44-104">Windows 10 has a built-in SSH client that you can use in Windows Terminal.</span></span>

<span data-ttu-id="fea44-105">In diesem Tutorial erfahren Sie, wie Sie ein Profil in Windows Terminal einrichten, das SSH verwendet.</span><span class="sxs-lookup"><span data-stu-id="fea44-105">In this tutorial, you'll learn how to set up a profile in Windows Terminal that uses SSH.</span></span>

## <a name="create-a-profile"></a><span data-ttu-id="fea44-106">Erstellen eines Profils</span><span class="sxs-lookup"><span data-stu-id="fea44-106">Create a profile</span></span>

<span data-ttu-id="fea44-107">Sie können eine SSH-Sitzung über die Eingabeaufforderung starten, indem Sie `ssh user@machine` ausführen. Sie werden dann aufgefordert, Ihr Kennwort einzugeben.</span><span class="sxs-lookup"><span data-stu-id="fea44-107">You can start an SSH session in your command prompt by executing `ssh user@machine` and you will be prompted to enter your password.</span></span> <span data-ttu-id="fea44-108">Sie können ein Windows Terminal-Profil erstellen, das dies beim Start erledigt, indem Sie die Einstellung `commandline` zu einem Profil in Ihrer Datei „settings.json“ hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="fea44-108">You can create a Windows Terminal profile that does this on startup by adding the `commandline` setting to a profile in your settings.json file.</span></span>

```js
"commandline": "ssh cinnamon@roll"
```

## <a name="specify-starting-directory"></a><span data-ttu-id="fea44-109">Startverzeichnis angeben</span><span class="sxs-lookup"><span data-stu-id="fea44-109">Specify starting directory</span></span>

<span data-ttu-id="fea44-110">Zum Angeben des Startverzeichnisses für eine von Windows Terminal aufgerufene SSH-Sitzung können Sie den folgenden Befehl verwenden:</span><span class="sxs-lookup"><span data-stu-id="fea44-110">To specify the starting directory for a ssh session invoked by Windows Terminal, you can use this command:</span></span>

```bash
"commandline": "ssh -t bob@foo \"cd /data/bob && exec bash -l\""
```

<span data-ttu-id="fea44-111">Das `-t`-Flag erzwingt die Pseudo-Terminalzuordnung.</span><span class="sxs-lookup"><span data-stu-id="fea44-111">The `-t` flag forces pseudo-terminal allocation.</span></span> <span data-ttu-id="fea44-112">Sie kann verwendet werden, um beliebige bildschirmbasierte Programme auf einem Remotecomputer auszuführen, z. B. bei der Implementierung von Menüdiensten.</span><span class="sxs-lookup"><span data-stu-id="fea44-112">This can be used to execute arbitrary screen-based programs on a remote machine, e.g. when implementing menu services.</span></span> <span data-ttu-id="fea44-113">Sie müssen doppelte Anführungszeichen mit Escapezeichen verwenden, da Ableitungen aus der Bourne-Shell für eine Zeichenfolge in einzelnen Anführungszeichen keine zusätzliche Analyse durchführen.</span><span class="sxs-lookup"><span data-stu-id="fea44-113">You will need to use escaped double quotes as bourne shell derivatives don't do any additional parsing for a string in single quotes.</span></span>

<span data-ttu-id="fea44-114">Weitere Informationen finden Sie unter:</span><span class="sxs-lookup"><span data-stu-id="fea44-114">For more information, see:</span></span>

* [<span data-ttu-id="fea44-115">GH-Problem: Wie wird das Startverzeichnis für eine SSH-Sitzung angegeben?</span><span class="sxs-lookup"><span data-stu-id="fea44-115">GH Issue: How to specify the starting directory for a ssh session?</span></span>](https://github.com/MicrosoftDocs/terminal/issues/25)
* [<span data-ttu-id="fea44-116">StackOverflow: Wie kann ich per SSH direkt zu einem bestimmten Verzeichnis wechseln?</span><span class="sxs-lookup"><span data-stu-id="fea44-116">StackOverflow: How can I ssh directly to a particular directory?</span></span>](https://stackoverflow.com/questions/626533/how-can-i-ssh-directly-to-a-particular-directory)

## <a name="resources"></a><span data-ttu-id="fea44-117">Ressourcen</span><span class="sxs-lookup"><span data-stu-id="fea44-117">Resources</span></span>

* [<span data-ttu-id="fea44-118">Aktivieren und Verwenden der neuen integrierten SSH-Befehle in Windows 10</span><span class="sxs-lookup"><span data-stu-id="fea44-118">How to Enable and Use Windows 10’s New Built-in SSH Commands</span></span>](https://www.howtogeek.com/336775/how-to-enable-and-use-windows-10s-built-in-ssh-commands/)
