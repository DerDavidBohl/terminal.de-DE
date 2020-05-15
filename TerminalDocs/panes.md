---
title: Windows Terminal-Bereiche
description: Erfahren Sie, wie Sie Bereiche in Windows Terminal unterteilen.
author: cinnamon-msft
ms.author: cinnamon
ms.date: 05/19/2020
ms.topic: how-to
ms.service: terminal
ms.openlocfilehash: 5d13d48d8e9317c229720937f916f57769da7261
ms.sourcegitcommit: bb5b7fd7db4b81e0d44e060989dc16b6775c802a
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/15/2020
ms.locfileid: "83416305"
---
# <a name="panes-in-windows-terminal"></a><span data-ttu-id="14e81-103">Bereiche in Windows Terminal</span><span class="sxs-lookup"><span data-stu-id="14e81-103">Panes in Windows Terminal</span></span>

<span data-ttu-id="14e81-104">Bereiche bieten Ihnen die Möglichkeit, mehrere Befehlszeilenanwendungen nebeneinander auf derselben Registerkarte auszuführen. Dadurch ist es nicht mehr erforderlich, zwischen Registerkarten zu wechseln, und Sie können mehrere Eingabeaufforderungen gleichzeitig anzeigen.</span><span class="sxs-lookup"><span data-stu-id="14e81-104">Panes give you the ability to run multiple command line applications next to each other within the same tab. This minimizes the need to switch between tabs and lets you see multiple prompts at once.</span></span>

## <a name="creating-a-new-pane"></a><span data-ttu-id="14e81-105">Erstellen eines neuen Bereichs</span><span class="sxs-lookup"><span data-stu-id="14e81-105">Creating a new pane</span></span>

<span data-ttu-id="14e81-106">Sie können entweder einen neuen vertikalen oder horizontalen Bereich in Windows Terminal erstellen.</span><span class="sxs-lookup"><span data-stu-id="14e81-106">You can either create a new vertical or horizontal pane in the Windows Terminal.</span></span> <span data-ttu-id="14e81-107">Bei vertikaler Teilung wird ein neuer Bereich rechts von dem Bereich geöffnet, der den Fokus enthält. Bei horizontaler Teilung wird ein neuer Bereich unterhalb des Bereichs geöffnet, der den Fokus enthält.</span><span class="sxs-lookup"><span data-stu-id="14e81-107">Splitting vertically will open a new pane to the right of the focused pane and splitting horizontally will open a new pane below the focused pane.</span></span> <span data-ttu-id="14e81-108">Wenn Sie einen neuen vertikalen Bereich für Ihr Standardprofil erstellen möchten, können Sie <kbd>ALT+UMSCHALT+PLUS</kbd> (+) eingeben.</span><span class="sxs-lookup"><span data-stu-id="14e81-108">To create a new vertical pane of your default profile, you can type <kbd>alt+shift+plus</kbd>.</span></span> <span data-ttu-id="14e81-109">Wenn Sie einen horizontalen Bereich für Ihr Standardprofil erstellen möchten, können Sie <kbd>ALT+UMSCHALT+MINUS</kbd> (-) eingeben.</span><span class="sxs-lookup"><span data-stu-id="14e81-109">For a horizontal pane of your default profile, you can type <kbd>alt+shift+-</kbd>.</span></span>

<span data-ttu-id="14e81-110">![Windows Terminal: Bereich erstellen](./images/open-panes.gif)
_Konfiguration: [Raspberry Ubuntu](./custom-terminal-gallery/raspberry-ubuntu.md)_</span><span class="sxs-lookup"><span data-stu-id="14e81-110">![Windows Terminal create pane](./images/open-panes.gif)
_Configuration: [Raspberry Ubuntu](./custom-terminal-gallery/raspberry-ubuntu.md)_</span></span>

<span data-ttu-id="14e81-111">Wenn Sie diese Tastenzuordnungen ändern möchten, können Sie neue erstellen, indem Sie die Aktion `splitPane` und die Werte `vertical` oder `horizontal` für die Eigenschaft `split` in Ihrer Datei „profiles.json“ verwenden.</span><span class="sxs-lookup"><span data-stu-id="14e81-111">If you would like to change these key bindings, you can create new ones using the `splitPane` action and `vertical` or `horizontal` values for the `split` property in your profiles.json file.</span></span> <span data-ttu-id="14e81-112">Wenn Sie nur einen Bereich mit der maximal möglichen Oberfläche wünschen, können Sie `split` auf `auto` festlegen.</span><span class="sxs-lookup"><span data-stu-id="14e81-112">If you just want a pane with the maximum amount of surface area, you can set `split` to `auto`.</span></span> <span data-ttu-id="14e81-113">Weitere Informationen zu Tastenzuordnungen finden Sie auf der Seite [Tastenzuordnungen](./customize-settings/key-bindings.md).</span><span class="sxs-lookup"><span data-stu-id="14e81-113">To learn more about key bindings, visit the [key bindings page](./customize-settings/key-bindings.md).</span></span>

```json
{ "command": { "action": "splitPane", "split": "vertical" }, "keys": "alt+shift+plus" },
{ "command": { "action": "splitPane", "split": "horizontal" }, "keys": "alt+shift+-" },
{ "command": { "action": "splitPane", "split": "auto" }, "keys": "alt+shift+|" }
```

## <a name="switching-between-panes"></a><span data-ttu-id="14e81-114">Wechseln zwischen Bereichen</span><span class="sxs-lookup"><span data-stu-id="14e81-114">Switching between panes</span></span>

<span data-ttu-id="14e81-115">Das Terminal ermöglicht mithilfe der Tastatur die Navigation zwischen Bereichen.</span><span class="sxs-lookup"><span data-stu-id="14e81-115">The terminal allows you to navigate between panes by using the keyboard.</span></span> <span data-ttu-id="14e81-116">Wenn Sie die <kbd>ALT</kbd>-TASTE gedrückt halten, können Sie die Pfeiltasten verwenden, um den Fokus zwischen den Bereichen zu verschieben.</span><span class="sxs-lookup"><span data-stu-id="14e81-116">If you hold the <kbd>alt</kbd> key, you can use your arrow keys to move your focus between panes.</span></span> <span data-ttu-id="14e81-117">Sie können erkennen, welcher Bereich den Fokus hat, indem Sie den ihn umgebenden Akzentfarbenrahmen betrachten.</span><span class="sxs-lookup"><span data-stu-id="14e81-117">You can identify which pane is in focus by the accent color border surrounding it.</span></span> <span data-ttu-id="14e81-118">Beachten Sie, dass diese Akzentfarbe in den Windows-Farbeinstellungen festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="14e81-118">Note that this accent color is set in your Windows color settings.</span></span>

![Windows Terminal: Zwischen Bereichen wechseln](./images/navigate-panes.gif)

<span data-ttu-id="14e81-120">Sie können dies anpassen, indem Sie Tastenzuordnungen für den Befehl `moveFocus` hinzufügen und `direction` auf `down`, `left`, `right` oder `up` festlegen.</span><span class="sxs-lookup"><span data-stu-id="14e81-120">You can customize this by adding key bindings for the `moveFocus` command and setting the `direction` to either `down`, `left`, `right` or `up`.</span></span>

```json
{ "command": { "action": "moveFocus", "direction": "down" }, "keys": "alt+down" },
{ "command": { "action": "moveFocus", "direction": "left" }, "keys": "alt+left" },
{ "command": { "action": "moveFocus", "direction": "right" }, "keys": "alt+right" },
{ "command": { "action": "moveFocus", "direction": "up" }, "keys": "alt+up" }
```

## <a name="resizing-a-pane"></a><span data-ttu-id="14e81-121">Ändern der Bereichsgröße</span><span class="sxs-lookup"><span data-stu-id="14e81-121">Resizing a pane</span></span>

<span data-ttu-id="14e81-122">Sie können die Größe Ihrer Bereiche anpassen, indem Sie <kbd>ALT+UMSCHALT</kbd> gedrückt halten und mithilfe der Pfeiltasten die Größe des Bereichs ändern, der den Fokus enthält.</span><span class="sxs-lookup"><span data-stu-id="14e81-122">You can adjust the size of your panes by holding <kbd>alt+shift</kbd> and using your arrow keys to resize the focused pane.</span></span>

![Windows Terminal: Bereich erstellen](./images/resize-panes.gif)

<span data-ttu-id="14e81-124">Wenn Sie diese Tastenzuordnung anpassen möchten, können Sie neue hinzufügen, indem Sie die Aktion `resizePane` verwenden und `direction` auf `down`, `left`, `right` oder `up` festlegen.</span><span class="sxs-lookup"><span data-stu-id="14e81-124">To customize this key binding, you can add new ones using the `resizePane` action and setting the `direction` to either `down`, `left`, `right`, or `up`.</span></span>

```json
{ "command": { "action": "resizePane", "direction": "down" }, "keys": "alt+shift+down" },
{ "command": { "action": "resizePane", "direction": "left" }, "keys": "alt+shift+left" },
{ "command": { "action": "resizePane", "direction": "right" }, "keys": "alt+shift+right" },
{ "command": { "action": "resizePane", "direction": "up" }, "keys": "alt+shift+up" }
```

## <a name="closing-a-pane"></a><span data-ttu-id="14e81-125">Schließen eines Bereichs</span><span class="sxs-lookup"><span data-stu-id="14e81-125">Closing a pane</span></span>

<span data-ttu-id="14e81-126">Sie können den Fokusbereich schließen, indem Sie <kbd>STRG+UMSCHALT+W</kbd> eingeben.</span><span class="sxs-lookup"><span data-stu-id="14e81-126">You can close the focused pane by typing <kbd>ctrl+shift+w</kbd>.</span></span> <span data-ttu-id="14e81-127">Wenn Sie nur über einen Bereich verfügen, schließt <kbd>STRG+UMSCHALT+W</kbd> die Registerkarte. Wie immer wird das Fenster durch Schließen der letzten Registerkarte geschlossen.</span><span class="sxs-lookup"><span data-stu-id="14e81-127">If you only have one pane, <kbd>ctrl+shift+w</kbd> will close the tab. As always, closing the last tab will close the window.</span></span>

![Windows Terminal: Bereiche schließen](./images/close-panes.gif)

<span data-ttu-id="14e81-129">Sie können ändern, welche Tasten den Bereich schließen, indem Sie eine Tastenzuordnung hinzufügen, die den Befehl `closePane` verwendet.</span><span class="sxs-lookup"><span data-stu-id="14e81-129">You can change which keys close the pane by adding a key binding that uses the `closePane` command.</span></span>

```json
{ "command": "closePane", "keys": "ctrl+shift+w" }
```

## <a name="customizing-panes-using-key-bindings"></a><span data-ttu-id="14e81-130">Anpassen von Bereichen mithilfe von Tastenzuordnungen</span><span class="sxs-lookup"><span data-stu-id="14e81-130">Customizing panes using key bindings</span></span>

<span data-ttu-id="14e81-131">Abhängig von den benutzerdefinierten Tastenzuordnungen können Sie anpassen, was in einem neuen Bereich geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="14e81-131">You can customize what opens inside a new pane depending on your custom key bindings.</span></span>

### <a name="duplicating-a-pane"></a><span data-ttu-id="14e81-132">Duplizieren eines Bereichs</span><span class="sxs-lookup"><span data-stu-id="14e81-132">Duplicating a pane</span></span>

<span data-ttu-id="14e81-133">Das Terminal ermöglicht es Ihnen, das Profil des Fokusbereichs in einem anderen Bereich zu duplizieren.</span><span class="sxs-lookup"><span data-stu-id="14e81-133">The terminal allows you to duplicate the focused pane's profile into another pane.</span></span>

![Windows Terminal: Bereiche duplizieren](./images/duplicate-panes.gif)

<span data-ttu-id="14e81-135">Dies kann durch Hinzufügen der Eigenschaft `splitMode` mit `duplicate` als Wert zu einer `splitPane`-Tastenzuordnung erfolgen.</span><span class="sxs-lookup"><span data-stu-id="14e81-135">This can be done by adding the `splitMode` property with `duplicate` as the value to a `splitPane` key binding.</span></span>

```json
{ "command": { "action": "splitPane", "split": "auto", "splitMode": "duplicate" }, "keys": "alt+shift+d" }
```

### <a name="new-terminal-arguments"></a><span data-ttu-id="14e81-136">Neue Terminalargumente</span><span class="sxs-lookup"><span data-stu-id="14e81-136">New terminal arguments</span></span>

[!INCLUDE [new-terminal-arguments](./new-terminal-arguments.md)]
