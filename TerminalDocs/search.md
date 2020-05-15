---
title: Windows Terminal-Suche
description: Erfahren Sie, wie Sie einen Suchvorgang in Windows Terminal ausführen.
author: cinnamon-msft
ms.author: cinnamon
ms.date: 05/19/2020
ms.topic: how-to
ms.service: terminal
ms.openlocfilehash: 94932d71e6543a83650e2e2a5febcb0206e22548
ms.sourcegitcommit: bb5b7fd7db4b81e0d44e060989dc16b6775c802a
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/15/2020
ms.locfileid: "83416335"
---
# <a name="how-to-search-in-windows-terminal"></a><span data-ttu-id="58c52-103">Suchen in Windows Terminal</span><span class="sxs-lookup"><span data-stu-id="58c52-103">How to search in Windows Terminal</span></span>

<span data-ttu-id="58c52-104">Windows Terminal enthält eine Suchfunktion, mit der Sie den Textpuffer nach einem bestimmten Schlüsselwort durchsuchen können.</span><span class="sxs-lookup"><span data-stu-id="58c52-104">The Windows Terminal comes with a search feature that allows you to look through the text buffer for a specific keyword.</span></span> <span data-ttu-id="58c52-105">Dies ist bei der Suche nach einem Befehl hilfreich, den Sie vor einem oder für einen bestimmten Dateinamen ausgeführt haben.</span><span class="sxs-lookup"><span data-stu-id="58c52-105">This is useful when trying to find a command you had run before or for a specific file name.</span></span>

## <a name="using-search"></a><span data-ttu-id="58c52-106">Mithilfe der Suche</span><span class="sxs-lookup"><span data-stu-id="58c52-106">Using search</span></span>

<span data-ttu-id="58c52-107">Standardmäßig können Sie das Suchdialogfeld durch Eingabe von <kbd>STRG+UMSCHALT+F</kbd> öffnen.</span><span class="sxs-lookup"><span data-stu-id="58c52-107">By default, you can open the search dialog by typing <kbd>ctrl+shift+f</kbd>.</span></span> <span data-ttu-id="58c52-108">Sobald es geöffnet ist, können Sie das gesuchte Schlüsselwort in das Textfeld eingeben und die <kbd>EINGABETASTE</kbd> drücken, um zu suchen.</span><span class="sxs-lookup"><span data-stu-id="58c52-108">Once opened, you can type the keyword you're looking for into the text box and hit <kbd>enter</kbd> to search.</span></span>

<span data-ttu-id="58c52-109">![Screenshot der Windows Terminal-Suche](./images/search.png)
_Konfiguration: [Powerline in PowerShell](./custom-terminal-gallery/powerline-in-powershell.md)_</span><span class="sxs-lookup"><span data-stu-id="58c52-109">![Windows Terminal search screenshot](./images/search.png)
_Configuration: [Powerline in PowerShell](./custom-terminal-gallery/powerline-in-powershell.md)_</span></span>

## <a name="directional-search"></a><span data-ttu-id="58c52-110">Direktionale Suche</span><span class="sxs-lookup"><span data-stu-id="58c52-110">Directional search</span></span>

<span data-ttu-id="58c52-111">Das Terminal durchsucht den Textpuffer standardmäßig von unten nach oben.</span><span class="sxs-lookup"><span data-stu-id="58c52-111">The terminal will default to searching from the bottom to the top of the text buffer.</span></span> <span data-ttu-id="58c52-112">Sie können die Suchrichtung ändern, indem Sie einen der Pfeile im Suchdialogfeld auswählen.</span><span class="sxs-lookup"><span data-stu-id="58c52-112">You can change the search direction by selecting one of the arrows in the search dialog.</span></span>

![Screenshot der direktionalen Suche von Windows Terminal](./images/search-direction.gif)

## <a name="case-match-search"></a><span data-ttu-id="58c52-114">Suche mit Übereinstimmung von Groß-/Kleinschreibung</span><span class="sxs-lookup"><span data-stu-id="58c52-114">Case match search</span></span>

<span data-ttu-id="58c52-115">Wenn Sie die Suchergebnisse eingrenzen möchten, können Sie die Übereinstimmung von Groß-/Kleinschreibung als Option zu Ihrer Suche hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="58c52-115">If you'd like to narrow down your search results, you can add case matching as an option in your search.</span></span> <span data-ttu-id="58c52-116">Sie können die Übereinstimmung von Groß-/Kleinschreibung umschalten, indem Sie die Schaltfläche für die Berücksichtigung der Groß-/Kleinschreibung auswählen, und die angezeigten Ergebnisse stimmen dann nur mit dem eingegebenen Suchbegriff mit seiner bestimmten Groß-/Kleinschreibung überein.</span><span class="sxs-lookup"><span data-stu-id="58c52-116">You can toggle case matching by selecting the case match button, and the results that appear will only match the keyword entered with its specific letter casing.</span></span>

![Screenshot der Suche mit Berücksichtigung der Groß-/Kleinschreibung in Windows Terminal](./images/search-case-match.gif)

## <a name="searching-within-panes"></a><span data-ttu-id="58c52-118">Suchen in Bereichen</span><span class="sxs-lookup"><span data-stu-id="58c52-118">Searching within panes</span></span>

<span data-ttu-id="58c52-119">Das Suchdialogfeld funktioniert auch mit [Bereichen](./panes.md).</span><span class="sxs-lookup"><span data-stu-id="58c52-119">The search dialog works with [panes](./panes.md) as well.</span></span> <span data-ttu-id="58c52-120">Wenn der Fokus in einem Bereich liegt, können Sie das Suchdialogfeld öffnen, das daraufhin in der oberen rechten Ecke des Bereichs angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="58c52-120">When focused on a pane, you can open the search dialog and it will appear on the upper-right of that pane.</span></span> <span data-ttu-id="58c52-121">Ein beliebiges von Ihnen eingegebenes Schlüsselwort zeigt nur die in diesem Bereich gefundenen Ergebnisse an.</span><span class="sxs-lookup"><span data-stu-id="58c52-121">Then any keyword you enter will only show results found within that pane.</span></span>

![Screenshot der Suche in Windows Terminal-Bereichen](./images/search-panes.gif)

## <a name="customize-the-search-key-binding"></a><span data-ttu-id="58c52-123">Anpassen der Suchtastenzuordnung</span><span class="sxs-lookup"><span data-stu-id="58c52-123">Customize the search key binding</span></span>

<span data-ttu-id="58c52-124">Sie können das Suchdialogfeld mit jeder beliebigen Tastenzuordnung (Tastenkombination) öffnen, die Sie bevorzugen.</span><span class="sxs-lookup"><span data-stu-id="58c52-124">You can open the search dialog with any key binding (shortcut key combination) that you prefer.</span></span> <span data-ttu-id="58c52-125">Öffnen Sie zum Ändern der Suchtastenzuordnung die Datei „settings.json“, und suchen Sie nach dem Befehl `find`.</span><span class="sxs-lookup"><span data-stu-id="58c52-125">To change the search key binding, open your settings.json file and search for the `find` command.</span></span> <span data-ttu-id="58c52-126">Standardmäßig ist dieser Befehl auf `ctrl+shift+f` festgelegt.</span><span class="sxs-lookup"><span data-stu-id="58c52-126">By default, this command is set to `ctrl+shift+f`.</span></span>

```json
// Press ctrl+shift+f to open the search box
        { "command": "find", "keys": "ctrl+shift+f" },
```

<span data-ttu-id="58c52-127">Sie können z. B. „STRG+UMSCHALT+F“ in „STRG+F“ ändern, sodass beim Eingeben von `ctrl+f` das Suchdialogfeld geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="58c52-127">For example, you can change "ctrl+shift+f" to "ctrl+f", so when typing `ctrl+f`, the search dialog will open.</span></span>

<span data-ttu-id="58c52-128">Weitere Informationen zu Tastenzuordnungen finden Sie auf der Seite [Tastenzuordnungen](./customize-settings/key-bindings.md).</span><span class="sxs-lookup"><span data-stu-id="58c52-128">To learn more about key bindings, visit the [key bindings page](./customize-settings/key-bindings.md).</span></span>
