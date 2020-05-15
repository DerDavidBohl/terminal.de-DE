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
# <a name="tutorial-configure-tab-titles-in-windows-terminal"></a><span data-ttu-id="1f009-103">Tutorial: Konfigurieren von Registerkartentiteln in Windows Terminal</span><span class="sxs-lookup"><span data-stu-id="1f009-103">Tutorial: Configure tab titles in Windows Terminal</span></span>

<span data-ttu-id="1f009-104">Standardmäßig wird der Registerkartentitel auf den Titel der Shell festgelegt.</span><span class="sxs-lookup"><span data-stu-id="1f009-104">By default, the tab title is set to the shell's title.</span></span> <span data-ttu-id="1f009-105">Wenn eine Registerkarte aus mehreren Bereichen besteht, wird der Registerkartentitel auf den Titel des aktuellen Fokusbereichs festgelegt.</span><span class="sxs-lookup"><span data-stu-id="1f009-105">If a tab is composed of multiple panes, the tab's title is set to that of the currently focused pane.</span></span> <span data-ttu-id="1f009-106">Wenn Sie den festgelegten Registerkartentitel ändern möchten, befolgen Sie die Anweisungen in diesem Tutorial.</span><span class="sxs-lookup"><span data-stu-id="1f009-106">If you want to customize what is set as the tab title, follow this tutorial.</span></span>

<span data-ttu-id="1f009-107">In diesem Tutorial erfahren Sie, wie Sie die folgenden Aufgaben durchführen:</span><span class="sxs-lookup"><span data-stu-id="1f009-107">In this tutorial, you learn how to:</span></span>

> [!div class="checklist"]
> * <span data-ttu-id="1f009-108">Verwenden der `tabTitle`-Einstellung</span><span class="sxs-lookup"><span data-stu-id="1f009-108">Use the `tabTitle` setting</span></span>
> * <span data-ttu-id="1f009-109">Festlegen des Titels der Shell</span><span class="sxs-lookup"><span data-stu-id="1f009-109">Set the shell's title</span></span>
> * <span data-ttu-id="1f009-110">Verwenden der `suppressApplicationTitle`-Einstellung</span><span class="sxs-lookup"><span data-stu-id="1f009-110">Using the `suppressApplicationTitle` setting</span></span>

## <a name="use-the-tabtitle-setting"></a><span data-ttu-id="1f009-111">Verwenden der `tabTitle`-Einstellung</span><span class="sxs-lookup"><span data-stu-id="1f009-111">Use the `tabTitle` setting</span></span>

<span data-ttu-id="1f009-112">Mit der `tabTitle`-Einstellung können Sie den Starttitel für eine neue Instanz einer Shell definieren.</span><span class="sxs-lookup"><span data-stu-id="1f009-112">The `tabTitle` setting allows you to define the starting title for a new instance of a shell.</span></span> <span data-ttu-id="1f009-113">Wenn die Einstellung nicht festgelegt ist, wird stattdessen das Profil `name` verwendet.</span><span class="sxs-lookup"><span data-stu-id="1f009-113">If it is not set, the profile `name` is used instead.</span></span> <span data-ttu-id="1f009-114">Jede Shell reagiert anders auf diese Einstellung.</span><span class="sxs-lookup"><span data-stu-id="1f009-114">Each shell responds to this setting differently.</span></span>

| <span data-ttu-id="1f009-115">Shell</span><span class="sxs-lookup"><span data-stu-id="1f009-115">Shell</span></span> | <span data-ttu-id="1f009-116">Verhalten</span><span class="sxs-lookup"><span data-stu-id="1f009-116">Behavior</span></span> |
| ----- | -------- |
| <span data-ttu-id="1f009-117">PowerShell</span><span class="sxs-lookup"><span data-stu-id="1f009-117">PowerShell</span></span> | <span data-ttu-id="1f009-118">Der Titel ist festgelegt.</span><span class="sxs-lookup"><span data-stu-id="1f009-118">The title is set.</span></span> |
| <span data-ttu-id="1f009-119">Eingabeaufforderung ein</span><span class="sxs-lookup"><span data-stu-id="1f009-119">Command Prompt</span></span> | <span data-ttu-id="1f009-120">Der Titel ist festgelegt.</span><span class="sxs-lookup"><span data-stu-id="1f009-120">The title is set.</span></span> <span data-ttu-id="1f009-121">Wenn ein Befehl ausgeführt wird, wird er temporär am Ende des Titels angefügt.</span><span class="sxs-lookup"><span data-stu-id="1f009-121">If a command is running, it is temporarily appended to the end of the title.</span></span> |
| <span data-ttu-id="1f009-122">Ubuntu</span><span class="sxs-lookup"><span data-stu-id="1f009-122">Ubuntu</span></span> | <span data-ttu-id="1f009-123">Der Titel wird ignoriert und stattdessen auf `user@machine:path` festgelegt.</span><span class="sxs-lookup"><span data-stu-id="1f009-123">The title is ignored, and instead set to `user@machine:path`</span></span> |
| <span data-ttu-id="1f009-124">Debian</span><span class="sxs-lookup"><span data-stu-id="1f009-124">Debian</span></span> | <span data-ttu-id="1f009-125">Der Titel ist festgelegt.</span><span class="sxs-lookup"><span data-stu-id="1f009-125">The title is set.</span></span> |

> [!NOTE]
> <span data-ttu-id="1f009-126">Obwohl Ubuntu und Debian beide bash ausführen, haben sie unterschiedliche Verhaltensweisen.</span><span class="sxs-lookup"><span data-stu-id="1f009-126">Though Ubuntu and Debian both run bash, they have different behaviors.</span></span> <span data-ttu-id="1f009-127">Damit soll gezeigt werden, dass unterschiedliche Distributionen unterschiedliche Verhaltensweisen aufweisen können.</span><span class="sxs-lookup"><span data-stu-id="1f009-127">This is to show that different distributions may have different behaviors.</span></span>

## <a name="set-the-shells-title"></a><span data-ttu-id="1f009-128">Festlegen des Titels der Shell</span><span class="sxs-lookup"><span data-stu-id="1f009-128">Set the shell's title</span></span>

<span data-ttu-id="1f009-129">Eine Shell hat die volle Kontrolle über ihren eigenen Titel.</span><span class="sxs-lookup"><span data-stu-id="1f009-129">A shell has full control over its own title.</span></span> <span data-ttu-id="1f009-130">Allerdings legt jede Shell ihren Titel anders fest.</span><span class="sxs-lookup"><span data-stu-id="1f009-130">However, each shell sets its title differently.</span></span>

| <span data-ttu-id="1f009-131">Shell</span><span class="sxs-lookup"><span data-stu-id="1f009-131">Shell</span></span> | <span data-ttu-id="1f009-132">Befehl</span><span class="sxs-lookup"><span data-stu-id="1f009-132">Command</span></span> |
| ----- | ------- |
| <span data-ttu-id="1f009-133">PowerShell</span><span class="sxs-lookup"><span data-stu-id="1f009-133">PowerShell</span></span> | `$Host.UI.RawUI.WindowTitle = "New Title"` |
| <span data-ttu-id="1f009-134">Eingabeaufforderung ein</span><span class="sxs-lookup"><span data-stu-id="1f009-134">Command Prompt</span></span> | `TITLE "New Title"` |
| <span data-ttu-id="1f009-135">bash\*</span><span class="sxs-lookup"><span data-stu-id="1f009-135">bash\*</span></span> | `echo -ne "\033]0;New Title\a"` |

<span data-ttu-id="1f009-136">Beachten Sie, dass einige Linux-Distributionen (z. B. Ubuntu) ihren Titel automatisch festlegen, wenn Sie mit der Shell interagieren.</span><span class="sxs-lookup"><span data-stu-id="1f009-136">Note that some Linux distributions (i.e. Ubuntu) set their title automatically as you interact with the shell.</span></span> <span data-ttu-id="1f009-137">Wenn der obige Befehl nicht funktioniert, führen Sie den folgenden Befehl aus:</span><span class="sxs-lookup"><span data-stu-id="1f009-137">If the above command doesn't work, run the following command:</span></span>

```bash
PS1=$
PROMPT_COMMAND=
echo -ne "\033]0;New Title\a"
```

<span data-ttu-id="1f009-138">Dadurch wird der Titel in „Neuer Titel“ geändert und die Eingabeaufforderung auf „$“ festgelegt.</span><span class="sxs-lookup"><span data-stu-id="1f009-138">This will change the title to 'New Title', and also set the prompt to '$'.</span></span>

## <a name="use-the-suppressapplicationtitle-setting"></a><span data-ttu-id="1f009-139">Verwenden der `suppressApplicationTitle`-Einstellung</span><span class="sxs-lookup"><span data-stu-id="1f009-139">Use the `suppressApplicationTitle` setting</span></span>

<span data-ttu-id="1f009-140">Da eine Shell die Kontrolle über ihren Titel hat, kann sie den Registerkartentitel jederzeit überschreiben.</span><span class="sxs-lookup"><span data-stu-id="1f009-140">Since a shell has control over its title, it may choose to overwrite the tab title at any time.</span></span> <span data-ttu-id="1f009-141">Das Modul `posh-git` für PowerShell fügt z. B. Informationen zu Ihrem Git-Repository zum Titel hinzu.</span><span class="sxs-lookup"><span data-stu-id="1f009-141">For example, the `posh-git` module for PowerShell adds information about your Git repository to the title.</span></span>

<span data-ttu-id="1f009-142">Windows Terminal ermöglicht es Ihnen, Änderungen am Titel zu unterdrücken, indem Sie in Ihrem Profil `suppressApplicationTitle` auf `true` festlegen.</span><span class="sxs-lookup"><span data-stu-id="1f009-142">Windows Terminal allows you to suppress changes to the title by setting `suppressApplicationTitle` to `true` in your profile.</span></span> <span data-ttu-id="1f009-143">Dadurch legen neue Instanzen des Profils Ihren sichtbaren Titel auf `tabTitle` fest.</span><span class="sxs-lookup"><span data-stu-id="1f009-143">This makes new instances of the profile set your visible title to `tabTitle`.</span></span> <span data-ttu-id="1f009-144">Wenn `tabTitle` nicht festgelegt ist, wird der sichtbare Titel auf den `name` des Profils festgelegt.</span><span class="sxs-lookup"><span data-stu-id="1f009-144">If `tabTitle` is not set, the visible title is set to the profile's `name`.</span></span>

<span data-ttu-id="1f009-145">Beachten Sie, dass dies den Titel der Shell von dem auf der Registerkarte angezeigten sichtbaren Titel entkoppelt. Wenn Sie die Variable der Shell lesen, in der der Titel festgelegt ist, kann sie sich vom Titel der Registerkarte unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="1f009-145">Note that this decouples the shell's title from the visible title presented on the tab. If you read the shell's variable where the title is set, it may differ from the tab's title.</span></span>

## <a name="resources"></a><span data-ttu-id="1f009-146">Ressourcen</span><span class="sxs-lookup"><span data-stu-id="1f009-146">Resources</span></span>

* [<span data-ttu-id="1f009-147">Festlegen des Konsolentitels als aktuelles Arbeitsverzeichnis</span><span class="sxs-lookup"><span data-stu-id="1f009-147">Setting the console title to be your current working directory</span></span>](https://devblogs.microsoft.com/powershell/setting-the-console-title-to-be-your-current-working-directory/)
* [<span data-ttu-id="1f009-148">Ändern des Titels eines Terminals unter Ubuntu 16.04</span><span class="sxs-lookup"><span data-stu-id="1f009-148">Change the title of a terminal on Ubuntu 16.04</span></span>](https://www.zachpfeffer.com/single-post/Change-the-title-of-a-terminal-on-Ubuntu-1604)
