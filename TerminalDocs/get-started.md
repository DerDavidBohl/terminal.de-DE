---
title: Windows Terminal-Installation
description: In diesem Schnellstart erfahren Sie, wie Sie Windows Terminal installieren und ausführen.
author: cinnamon-msft
ms.author: cinnamon
ms.date: 05/19/2020
ms.topic: quickstart
ms.service: terminal
ms.localizationpriority: high
ms.openlocfilehash: 901e3a0f447cdfe19a69ee43c7f76ed529d87108
ms.sourcegitcommit: bb5b7fd7db4b81e0d44e060989dc16b6775c802a
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/15/2020
ms.locfileid: "83415845"
---
# <a name="install-and-set-up-windows-terminal"></a><span data-ttu-id="98932-103">Installieren und Einrichten von Windows Terminal</span><span class="sxs-lookup"><span data-stu-id="98932-103">Install and set up Windows Terminal</span></span>

## <a name="installation"></a><span data-ttu-id="98932-104">Installation</span><span class="sxs-lookup"><span data-stu-id="98932-104">Installation</span></span>

<span data-ttu-id="98932-105">Sie können Windows Terminal über den [Microsoft Store](https://aka.ms/terminal) installieren.</span><span class="sxs-lookup"><span data-stu-id="98932-105">You can install the Windows Terminal from the [Microsoft Store](https://aka.ms/terminal).</span></span>

<span data-ttu-id="98932-106">Wenn Sie keinen Zugriff auf den Microsoft Store haben, werden die Builds auf der Seite [GitHub-Versionen](https://github.com/microsoft/terminal/releases) veröffentlicht.</span><span class="sxs-lookup"><span data-stu-id="98932-106">If you don't have access to the Microsoft Store, the builds are published on the [GitHub releases page](https://github.com/microsoft/terminal/releases).</span></span> <span data-ttu-id="98932-107">Wenn Sie über GitHub installieren, wird das Terminal nicht automatisch mit neuen Versionen aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="98932-107">If you install from GitHub, the terminal will not automatically update with new versions.</span></span>

## <a name="first-run"></a><span data-ttu-id="98932-108">Erstausführung</span><span class="sxs-lookup"><span data-stu-id="98932-108">First run</span></span>

<span data-ttu-id="98932-109">Wenn Sie das Terminal nach der Installation öffnen, wird es mit PowerShell als Standardprofil auf der geöffneten Registerkarte gestartet.</span><span class="sxs-lookup"><span data-stu-id="98932-109">After installation, when you open the terminal, it will start with PowerShell as the default profile in the open tab.</span></span>

![Erste Ausführung von Windows Terminal](./images/first-run.png)

### <a name="dynamic-profiles"></a><span data-ttu-id="98932-111">Dynamische Profile</span><span class="sxs-lookup"><span data-stu-id="98932-111">Dynamic profiles</span></span>

<span data-ttu-id="98932-112">Das Terminal erstellt automatisch Profile für Sie, wenn Sie WSL-Distributionen oder mehrere Versionen von PowerShell installiert haben.</span><span class="sxs-lookup"><span data-stu-id="98932-112">The terminal will automatically create profiles for you if you have WSL distros or multiple versions of PowerShell installed.</span></span> <span data-ttu-id="98932-113">Weitere Informationen zu dynamischen Profilen finden Sie auf der Seite [Dynamische Profile](./dynamic-profiles.md).</span><span class="sxs-lookup"><span data-stu-id="98932-113">Learn more about dynamic profiles on the [Dynamic profiles page](./dynamic-profiles.md).</span></span>

## <a name="open-a-new-tab"></a><span data-ttu-id="98932-114">Öffnen einer neuen Registerkarte</span><span class="sxs-lookup"><span data-stu-id="98932-114">Open a new tab</span></span>

<span data-ttu-id="98932-115">Sie können eine neue Registerkarte des Standardprofils öffnen, indem Sie <kbd>STRG+UMSCHALT+T</kbd> drücken oder die Schaltfläche „+“ (Plus) auswählen.</span><span class="sxs-lookup"><span data-stu-id="98932-115">You can open a new tab of the default profile by pressing <kbd>ctrl+shift+t</kbd> or by selecting the + (plus) button.</span></span> <span data-ttu-id="98932-116">Wählen Sie zum Öffnen eines anderen Profils den „˅“ (Pfeil) neben der Schaltfläche „+“ (Plus) aus, um das Dropdownmenü zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="98932-116">To open a different profile, select the ˅ (arrow) next to the + button to open the dropdown menu.</span></span> <span data-ttu-id="98932-117">Darüber können Sie auswählen, welches Profil geöffnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="98932-117">From there, you can select which profile to open.</span></span>

## <a name="open-a-new-pane"></a><span data-ttu-id="98932-118">Öffnen eines neuen Bereichs</span><span class="sxs-lookup"><span data-stu-id="98932-118">Open a new pane</span></span>

<span data-ttu-id="98932-119">Mithilfe von Bereichen können Sie mehrere Shells nebeneinander ausführen.</span><span class="sxs-lookup"><span data-stu-id="98932-119">You can run multiple shells side-by-side using panes.</span></span> <span data-ttu-id="98932-120">Verwenden Sie zum Öffnen eines Bereichs <kbd>ALT+UMSCHALT+D</kbd>.</span><span class="sxs-lookup"><span data-stu-id="98932-120">To open a pane, you can use <kbd>alt+shift+d</kbd>.</span></span> <span data-ttu-id="98932-121">Diese Tastenzuordnung öffnet einen duplizierten Bereich des Profils, das den Fokus enthält.</span><span class="sxs-lookup"><span data-stu-id="98932-121">This key binding will open a duplicate pane of your focused profile.</span></span> <span data-ttu-id="98932-122">Weitere Informationen zu Bereichen finden Sie auf der Seite [Bereiche](./panes.md).</span><span class="sxs-lookup"><span data-stu-id="98932-122">Learn more about panes on the [Panes page](./panes.md).</span></span>

## <a name="configuration"></a><span data-ttu-id="98932-123">Konfiguration</span><span class="sxs-lookup"><span data-stu-id="98932-123">Configuration</span></span>

<span data-ttu-id="98932-124">Wählen Sie zum Anpassen der Einstellungen von Windows Terminal die Option **Einstellungen** im Dropdownmenü aus.</span><span class="sxs-lookup"><span data-stu-id="98932-124">To customize the settings of your Windows Terminal, select **Settings** in the dropdown menu.</span></span> <span data-ttu-id="98932-125">Dadurch wird die Datei `settings.json` in Ihrem standardmäßigen Text-Editor geöffnet.</span><span class="sxs-lookup"><span data-stu-id="98932-125">This will open the `settings.json` file in your default text editor.</span></span> <span data-ttu-id="98932-126">(Der standardmäßige Text-Editor ist in den [Windows-Einstellungen](ms-settings:defaultapps) definiert.)</span><span class="sxs-lookup"><span data-stu-id="98932-126">(The default text editor is defined in your [Windows settings](ms-settings:defaultapps).)</span></span>

<span data-ttu-id="98932-127">Der Terminal unterstützt die Anpassung von [globalen Eigenschaften](./customize-settings/global-settings.md), die sich auf die gesamte Anwendung auswirken, [Profileigenschaften](./customize-settings/profile-settings.md), die sich auf die Einstellungen der einzelnen Profile auswirken, und [Tastenzuordnungen](./customize-settings/key-bindings.md), die es Ihnen ermöglichen, mit dem Terminal über Ihre Tastatur zu interagieren.</span><span class="sxs-lookup"><span data-stu-id="98932-127">The terminal supports customization of [global properties](./customize-settings/global-settings.md) that affect the whole application, [profile properties](./customize-settings/profile-settings.md) that affect the settings of each profile, and [key bindings](./customize-settings/key-bindings.md) that allow you to interact with the terminal using your keyboard.</span></span>

## <a name="command-line-arguments"></a><span data-ttu-id="98932-128">Befehlszeilenargumente</span><span class="sxs-lookup"><span data-stu-id="98932-128">Command line arguments</span></span>

<span data-ttu-id="98932-129">Mithilfe von Befehlszeilenargumenten können Sie das Terminal in einer bestimmten Konfiguration starten.</span><span class="sxs-lookup"><span data-stu-id="98932-129">You can launch the terminal in a specific configuration using command line arguments.</span></span> <span data-ttu-id="98932-130">Mit diesen Argumenten können Sie das Terminal mit bestimmten Registerkarten und Bereichen mit benutzerdefinierten Profileinstellungen öffnen.</span><span class="sxs-lookup"><span data-stu-id="98932-130">These arguments let you open the terminal with specific tabs and panes with custom profile settings.</span></span> <span data-ttu-id="98932-131">Weitere Informationen zu Befehlszeilenargumenten finden Sie auf der Seite [Befehlszeilenargumente](./command-line-arguments.md).</span><span class="sxs-lookup"><span data-stu-id="98932-131">Learn more about command line arguments on the [Command line arguments page](./command-line-arguments.md).</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="98932-132">Problembehandlung</span><span class="sxs-lookup"><span data-stu-id="98932-132">Troubleshooting</span></span>

<span data-ttu-id="98932-133">Wenn Sie bei der Verwendung des Terminals auf Probleme stoßen, finden Sie weitere Informationen auf der Seite [Problembehandlung](./troubleshooting.md).</span><span class="sxs-lookup"><span data-stu-id="98932-133">If you encounter any difficulties using the terminal, reference the [Troubleshooting page](./troubleshooting.md).</span></span> <span data-ttu-id="98932-134">Wenn Sie Fehler finden oder ein Feature anfordern möchten, können Sie den Link „Feedback“ im Menü **Info** des Terminals auswählen, um zur [GitHub-Seite](https://github.com/microsoft/terminal) zu gelangen, wo Sie ein neues Problem einreichen können.</span><span class="sxs-lookup"><span data-stu-id="98932-134">If you find any bugs or have a feature request, you can select the feedback link in the **About** menu of the terminal to go to the [GitHub page](https://github.com/microsoft/terminal) where you can file a new issue.</span></span>
