---
title: Windows Terminal-Befehlszeilenargumente
description: Erfahren Sie, wie Sie Befehlszeilenargumente für Windows Terminal erstellen.
author: cinnamon-msft
ms.author: cinnamon
ms.date: 05/19/2020
ms.topic: how-to
ms.service: terminal
ms.openlocfilehash: e30fd547052a87c88b72d015e132e32b1889af05
ms.sourcegitcommit: bb5b7fd7db4b81e0d44e060989dc16b6775c802a
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/15/2020
ms.locfileid: "83415895"
---
# <a name="using-command-line-arguments-for-windows-terminal"></a><span data-ttu-id="d12ab-103">Verwenden von Befehlszeilenargumenten für Windows Terminal</span><span class="sxs-lookup"><span data-stu-id="d12ab-103">Using command line arguments for Windows Terminal</span></span>

<span data-ttu-id="d12ab-104">Sie können `wt.exe` verwenden, um eine neue Instanz von Windows Terminal über die Befehlszeile zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="d12ab-104">You can use `wt.exe` to open a new instance of Windows Terminal from the command line.</span></span> <span data-ttu-id="d12ab-105">Sie können stattdessen auch den Ausführungsalias `wt` verwenden.</span><span class="sxs-lookup"><span data-stu-id="d12ab-105">You can also use the execution alias `wt` instead.</span></span>

> [!NOTE]
> <span data-ttu-id="d12ab-106">Wenn Sie Windows Terminal aus dem Quellcode auf [GitHub](https://github.com/microsoft/terminal) erstellt haben, können Sie diesen Build mit `wtd.exe` oder `wtd` öffnen.</span><span class="sxs-lookup"><span data-stu-id="d12ab-106">If you built the Windows Terminal from the source code on [GitHub](https://github.com/microsoft/terminal), you can open that build using `wtd.exe` or `wtd`.</span></span>

![Windows Terminal-Befehlszeilenargument für geteilte Bereiche](./images/terminal-command-args.gif)

## <a name="command-line-syntax"></a><span data-ttu-id="d12ab-108">Befehlszeilensyntax</span><span class="sxs-lookup"><span data-stu-id="d12ab-108">Command line syntax</span></span>

<span data-ttu-id="d12ab-109">Die `wt`-Befehlszeile akzeptiert zwei Arten von Werten: **Optionen** und **Befehle**.</span><span class="sxs-lookup"><span data-stu-id="d12ab-109">The `wt` command line accepts two types of values: **options** and **commands**.</span></span> <span data-ttu-id="d12ab-110">**Optionen** sind eine Liste von Flags und anderen Parametern, die das Verhalten der `wt`-Befehlszeile als Ganzes steuern können.</span><span class="sxs-lookup"><span data-stu-id="d12ab-110">**Options** are a list of flags and other parameters that can control the behavior of the `wt` command line as a whole.</span></span> <span data-ttu-id="d12ab-111">**Befehle** geben die Aktion oder eine durch Semikolon getrennte Liste von Aktionen an, die ausgeführt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="d12ab-111">**Commands** provide the action, or list of actions separated by semicolons, that should be implemented.</span></span> <span data-ttu-id="d12ab-112">Wenn Sie keinen Befehl angeben, wird `new-tab` standardmäßig als Befehl angenommen.</span><span class="sxs-lookup"><span data-stu-id="d12ab-112">If no command is specified, then the command is assumed to be `new-tab` by default.</span></span>

```bash
wt [options] [command ; ]
```

<span data-ttu-id="d12ab-113">Geben Sie Folgendes ein, um eine Hilfemeldung mit den verfügbaren Befehlszeilenargumenten anzuzeigen: `wt -h`, `wt --help`, `wt -?` oder `wt /?`.</span><span class="sxs-lookup"><span data-stu-id="d12ab-113">To display a help message listing the available command line arguments, enter: `wt -h`, `wt --help`, `wt -?`, or `wt /?`.</span></span>

## <a name="options-and-commands"></a><span data-ttu-id="d12ab-114">Optionen und Befehle</span><span class="sxs-lookup"><span data-stu-id="d12ab-114">Options and commands</span></span>

<span data-ttu-id="d12ab-115">Im Folgenden finden Sie die vollständige Liste der unterstützten Befehle und Optionen für die `wt`-Befehlszeile.</span><span class="sxs-lookup"><span data-stu-id="d12ab-115">Below is the full list of supported commands and options for the `wt` command line.</span></span>

| <span data-ttu-id="d12ab-116">Option</span><span class="sxs-lookup"><span data-stu-id="d12ab-116">Option</span></span> | <span data-ttu-id="d12ab-117">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d12ab-117">Description</span></span> |
| ------ | ----------- |
| <span data-ttu-id="d12ab-118">`--help`, `-h`, `-?`, `/?`</span><span class="sxs-lookup"><span data-stu-id="d12ab-118">`--help`, `-h`, `-?`, `/?`</span></span> | <span data-ttu-id="d12ab-119">Zeigt die Hilfemeldung an.</span><span class="sxs-lookup"><span data-stu-id="d12ab-119">Displays the help message.</span></span> |

| <span data-ttu-id="d12ab-120">Befehl</span><span class="sxs-lookup"><span data-stu-id="d12ab-120">Command</span></span> | <span data-ttu-id="d12ab-121">Parameter</span><span class="sxs-lookup"><span data-stu-id="d12ab-121">Parameters</span></span> | <span data-ttu-id="d12ab-122">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d12ab-122">Description</span></span> |
| ------- | ---------- | ----------- |
| `new-tab` | <span data-ttu-id="d12ab-123">`--profile, -p profile-name`, `--startingDirectory, -d starting-directory`, `commandline`</span><span class="sxs-lookup"><span data-stu-id="d12ab-123">`--profile, -p profile-name`, `--startingDirectory, -d starting-directory`, `commandline`</span></span> | <span data-ttu-id="d12ab-124">Erstellt eine neue Registerkarte.</span><span class="sxs-lookup"><span data-stu-id="d12ab-124">Creates a new tab.</span></span> |
| `split-pane` | <span data-ttu-id="d12ab-125">`-H, --horizontal`, `-V, --vertical`, `--profile, -p profile-name`, `--startingDirectory, -d starting-directory`, `commandline`</span><span class="sxs-lookup"><span data-stu-id="d12ab-125">`-H, --horizontal`, `-V, --vertical`, `--profile, -p profile-name`, `--startingDirectory, -d starting-directory`, `commandline`</span></span> | <span data-ttu-id="d12ab-126">Unterteilt einen neuen Bereich.</span><span class="sxs-lookup"><span data-stu-id="d12ab-126">Splits a new pane.</span></span> |
| `focus-tab` | `--target, -t tab-index` | <span data-ttu-id="d12ab-127">Setzt den Fokus auf eine bestimmte Registerkarte.</span><span class="sxs-lookup"><span data-stu-id="d12ab-127">Focuses on a specific tab.</span></span> |

## <a name="command-line-argument-examples"></a><span data-ttu-id="d12ab-128">Beispiele für Befehlszeilenargumente</span><span class="sxs-lookup"><span data-stu-id="d12ab-128">Command line argument examples</span></span>

<span data-ttu-id="d12ab-129">Die Befehle können leicht variieren, je nachdem, welche Befehlszeile Sie verwenden.</span><span class="sxs-lookup"><span data-stu-id="d12ab-129">Commands may vary slightly depending on which command line you're using.</span></span>

### <a name="open-a-new-profile-instance"></a><span data-ttu-id="d12ab-130">Eine neue Profilinstanz öffnen</span><span class="sxs-lookup"><span data-stu-id="d12ab-130">Open a new profile instance</span></span>

<span data-ttu-id="d12ab-131">Geben Sie Folgendes ein, um eine neue Terminalinstanz zu öffnen. In diesem Fall öffnet der Befehl das Profil mit dem Namen „Ubuntu-18.04“:</span><span class="sxs-lookup"><span data-stu-id="d12ab-131">To open a new terminal instance, in this case the command will open the profile named "Ubuntu-18.04", enter:</span></span>

<!-- Start tab selectors. -->
#### <a name="command-prompt"></a>[<span data-ttu-id="d12ab-132">Eingabeaufforderung</span><span class="sxs-lookup"><span data-stu-id="d12ab-132">Command Prompt</span></span>](#tab/windows)

```bash
wt -p "Ubuntu-18.04"
```

#### <a name="powershell"></a>[<span data-ttu-id="d12ab-133">PowerShell</span><span class="sxs-lookup"><span data-stu-id="d12ab-133">PowerShell</span></span>](#tab/powershell)

```powershell
wt -p "Ubuntu-18.04"
```

#### <a name="linux"></a>[<span data-ttu-id="d12ab-134">Linux</span><span class="sxs-lookup"><span data-stu-id="d12ab-134">Linux</span></span>](#tab/linux)

```bash
cmd.exe /c "wt.exe" -p "Ubuntu-18.04"
```

<span data-ttu-id="d12ab-135">Ausführungsaliase funktionieren nicht in WSL-Distributionen.</span><span class="sxs-lookup"><span data-stu-id="d12ab-135">Execution aliases do not work in WSL distributions.</span></span> <span data-ttu-id="d12ab-136">Wenn Sie „wt.exe“ über eine WSL-Befehlszeile verwenden möchten, können Sie es direkt über CMD erstellen, indem Sie `cmd.exe` ausführen.</span><span class="sxs-lookup"><span data-stu-id="d12ab-136">If you want to use wt.exe from a WSL command line, you can spawn it from CMD directly by running `cmd.exe`.</span></span> <span data-ttu-id="d12ab-137">Die Option `/c` weist CMD an, den Vorgang nach der Ausführung zu beenden.</span><span class="sxs-lookup"><span data-stu-id="d12ab-137">The `/c` option tells CMD to terminate after running.</span></span>

---
<!-- End tab selectors.  -->

 <span data-ttu-id="d12ab-138">Das `-p`-Flag wird verwendet, um das zu öffnende Windows Terminal-Profil anzugeben.</span><span class="sxs-lookup"><span data-stu-id="d12ab-138">The `-p` flag is used to specify the Windows Terminal profile that should be opened.</span></span> <span data-ttu-id="d12ab-139">Ersetzen Sie „Ubuntu-18.04“ durch den Namen eines beliebigen Terminalprofils, das Sie installiert haben.</span><span class="sxs-lookup"><span data-stu-id="d12ab-139">Substitute "Ubuntu-18.04" with the name of any terminal profile that you have installed.</span></span> <span data-ttu-id="d12ab-140">Dadurch wird immer ein neues Fenster geöffnet.</span><span class="sxs-lookup"><span data-stu-id="d12ab-140">This will always open a new window.</span></span> <span data-ttu-id="d12ab-141">Windows Terminal ist noch nicht in der Lage, neue Registerkarten oder Bereiche in einer vorhandenen Instanz zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="d12ab-141">Windows Terminal is not yet capable of opening new tabs or panes in an existing instance.</span></span>

### <a name="target-a-directory"></a><span data-ttu-id="d12ab-142">Auswählen eines Zielverzeichnisses</span><span class="sxs-lookup"><span data-stu-id="d12ab-142">Target a directory</span></span>

<span data-ttu-id="d12ab-143">Geben Sie Folgendes ein, um den Ordner anzugeben, der als Startverzeichnis für die Konsole verwendet werden soll (in diesem Fall das Verzeichnis „d:\“):</span><span class="sxs-lookup"><span data-stu-id="d12ab-143">To specify the folder that should be used as the starting directory for the console, in this case the d:\ directory, enter:</span></span>

<!-- Start tab selectors. -->
#### <a name="command-prompt"></a>[<span data-ttu-id="d12ab-144">Eingabeaufforderung</span><span class="sxs-lookup"><span data-stu-id="d12ab-144">Command Prompt</span></span>](#tab/windows)

```bash
wt -d d:\
```

#### <a name="powershell"></a>[<span data-ttu-id="d12ab-145">PowerShell</span><span class="sxs-lookup"><span data-stu-id="d12ab-145">PowerShell</span></span>](#tab/powershell)

```powershell
wt -d d:\
```

#### <a name="linux"></a>[<span data-ttu-id="d12ab-146">Linux</span><span class="sxs-lookup"><span data-stu-id="d12ab-146">Linux</span></span>](#tab/linux)

```bash
cmd.exe /c "wt.exe" -d d:\
```

<span data-ttu-id="d12ab-147">Ausführungsaliase funktionieren nicht in WSL-Distributionen.</span><span class="sxs-lookup"><span data-stu-id="d12ab-147">Execution aliases do not work in WSL distributions.</span></span> <span data-ttu-id="d12ab-148">Wenn Sie „wt.exe“ über eine WSL-Befehlszeile verwenden möchten, können Sie es direkt über CMD erstellen, indem Sie `cmd.exe` ausführen.</span><span class="sxs-lookup"><span data-stu-id="d12ab-148">If you want to use wt.exe from a WSL command line, you can spawn it from CMD directly by running `cmd.exe`.</span></span> <span data-ttu-id="d12ab-149">Die Option `/c` weist CMD an, den Vorgang nach der Ausführung zu beenden.</span><span class="sxs-lookup"><span data-stu-id="d12ab-149">The `/c` option tells CMD to terminate after running.</span></span>

---
<!-- End tab selectors.  -->

### <a name="multiple-tabs"></a><span data-ttu-id="d12ab-150">Mehrere Registerkarten</span><span class="sxs-lookup"><span data-stu-id="d12ab-150">Multiple tabs</span></span>

<span data-ttu-id="d12ab-151">Geben Sie Folgendes ein, um eine neue Terminalinstanz mit mehreren Registerkarten zu öffnen:</span><span class="sxs-lookup"><span data-stu-id="d12ab-151">To open a new terminal instance with multiple tabs, enter:</span></span>

<!-- Start tab selectors. -->
#### <a name="command-prompt"></a>[<span data-ttu-id="d12ab-152">Eingabeaufforderung</span><span class="sxs-lookup"><span data-stu-id="d12ab-152">Command Prompt</span></span>](#tab/windows)

```bash
wt ; ;
```

#### <a name="powershell"></a>[<span data-ttu-id="d12ab-153">PowerShell</span><span class="sxs-lookup"><span data-stu-id="d12ab-153">PowerShell</span></span>](#tab/powershell)

```powershell
wt `; `;
```

<span data-ttu-id="d12ab-154">PowerShell verwendet ein Semikolon (;), um Anweisungen zu trennen.</span><span class="sxs-lookup"><span data-stu-id="d12ab-154">PowerShell uses a semicolon ; to delimit statements.</span></span> <span data-ttu-id="d12ab-155">Wenn Sie ein Semikolon (;) als Befehlstrennzeichen für wt-Befehlszeilenargumente interpretieren möchten, müssen Sie Hochkommas als Escapezeichen für Semikolons verwenden.</span><span class="sxs-lookup"><span data-stu-id="d12ab-155">To interpret a semicolon ; as a command delimiter for wt command line arguments, you need to escape semicolon characters using backticks.</span></span> <span data-ttu-id="d12ab-156">PowerShell verfügt auch über den Operator zum Beenden der Analyse (--%), der das Programm anweist, das Interpretieren im Anschluss an den Operator einzustellen und die Zeichen einfach unverändert weiterzugeben.</span><span class="sxs-lookup"><span data-stu-id="d12ab-156">PowerShell also has the stop parsing operator (--%), which instructs it to stop interpreting anything after it and just pass it on verbatim.</span></span>

#### <a name="linux"></a>[<span data-ttu-id="d12ab-157">Linux</span><span class="sxs-lookup"><span data-stu-id="d12ab-157">Linux</span></span>](#tab/linux)

```bash
cmd.exe /c "wt.exe" \; \;
```

<span data-ttu-id="d12ab-158">Ausführungsaliase funktionieren nicht in WSL-Distributionen.</span><span class="sxs-lookup"><span data-stu-id="d12ab-158">Execution aliases do not work in WSL distributions.</span></span> <span data-ttu-id="d12ab-159">Wenn Sie „wt.exe“ über eine WSL-Befehlszeile verwenden möchten, können Sie es direkt über CMD erstellen, indem Sie `cmd.exe` ausführen.</span><span class="sxs-lookup"><span data-stu-id="d12ab-159">If you want to use wt.exe from a WSL command line, you can spawn it from CMD directly by running `cmd.exe`.</span></span> <span data-ttu-id="d12ab-160">Die Option `/c` weist CMD an, den Vorgang nach der Ausführung zu beenden.</span><span class="sxs-lookup"><span data-stu-id="d12ab-160">The `/c` option tells CMD to terminate after running.</span></span>

---
<!-- End tab selectors.  -->

<span data-ttu-id="d12ab-161">Geben Sie zum Öffnen einer neuen Terminalinstanz mit mehreren Registerkarten, in diesem Fall ein Eingabeaufforderungsprofil und ein PowerShell-Profil, Folgendes ein:</span><span class="sxs-lookup"><span data-stu-id="d12ab-161">To open a new terminal instance with multiple tabs, in this case a Command Prompt profile and a PowerShell profile, enter:</span></span>

<!-- Start tab selectors. -->
#### <a name="command-prompt"></a>[<span data-ttu-id="d12ab-162">Eingabeaufforderung</span><span class="sxs-lookup"><span data-stu-id="d12ab-162">Command Prompt</span></span>](#tab/windows)

```bash
wt -p "Command Prompt" ; new-tab -p "Windows PowerShell"
```

#### <a name="powershell"></a>[<span data-ttu-id="d12ab-163">PowerShell</span><span class="sxs-lookup"><span data-stu-id="d12ab-163">PowerShell</span></span>](#tab/powershell)

```powershell
wt -p "Command Prompt" `; new-tab -p "Windows PowerShell"
```

<span data-ttu-id="d12ab-164">PowerShell verwendet ein Semikolon (;), um Anweisungen zu trennen.</span><span class="sxs-lookup"><span data-stu-id="d12ab-164">PowerShell uses a semicolon ; to delimit statements.</span></span> <span data-ttu-id="d12ab-165">Wenn Sie ein Semikolon (;) als Befehlstrennzeichen für wt-Befehlszeilenargumente interpretieren möchten, müssen Sie Hochkommas als Escapezeichen für Semikolons verwenden.</span><span class="sxs-lookup"><span data-stu-id="d12ab-165">To interpret a semicolon ; as a command delimiter for wt command line arguments, you need to escape semicolon characters using backticks.</span></span> <span data-ttu-id="d12ab-166">PowerShell verfügt auch über den Operator zum Beenden der Analyse (--%), der das Programm anweist, das Interpretieren im Anschluss an den Operator einzustellen und die Zeichen einfach unverändert weiterzugeben.</span><span class="sxs-lookup"><span data-stu-id="d12ab-166">PowerShell also has the stop parsing operator (--%), which instructs it to stop interpreting anything after it and just pass it on verbatim.</span></span>

#### <a name="linux"></a>[<span data-ttu-id="d12ab-167">Linux</span><span class="sxs-lookup"><span data-stu-id="d12ab-167">Linux</span></span>](#tab/linux)

```bash
cmd.exe /c "wt.exe" -p "Command Prompt" \; new-tab -p "Windows Powershell"
```

<span data-ttu-id="d12ab-168">Ausführungsaliase funktionieren nicht in WSL-Distributionen.</span><span class="sxs-lookup"><span data-stu-id="d12ab-168">Execution aliases do not work in WSL distributions.</span></span> <span data-ttu-id="d12ab-169">Wenn Sie „wt.exe“ über eine WSL-Befehlszeile verwenden möchten, können Sie es direkt über CMD erstellen, indem Sie `cmd.exe` ausführen.</span><span class="sxs-lookup"><span data-stu-id="d12ab-169">If you want to use wt.exe from a WSL command line, you can spawn it from CMD directly by running `cmd.exe`.</span></span> <span data-ttu-id="d12ab-170">Die Option `/c` weist CMD an, nach der Ausführung zu beenden, und „`\;` Schrägstrich + Semikolon“ trennt Befehle.</span><span class="sxs-lookup"><span data-stu-id="d12ab-170">The `/c` option tells CMD to terminate after running and the `\;` forward-slash + semicolon separates commands.</span></span>

---
<!-- End tab selectors.  -->

### <a name="multiple-panes"></a><span data-ttu-id="d12ab-171">Mehrere Bereiche</span><span class="sxs-lookup"><span data-stu-id="d12ab-171">Multiple panes</span></span>

<span data-ttu-id="d12ab-172">Geben Sie Folgendes ein, um eine neue Terminalinstanz mit einer Registerkarte zu öffnen, die drei Bereiche enthält, in denen ein Eingabeaufforderungsprofil, ein PowerShell-Profil und Ihr Standardprofil mit einer WSL-Befehlszeile ausgeführt wird:</span><span class="sxs-lookup"><span data-stu-id="d12ab-172">To open a new terminal instance with one tab containing three panes running a Command Prompt profile, a PowerShell profile, and your default profile running a WSL command line, enter:</span></span>

<!-- Start tab selectors. -->
#### <a name="command-prompt"></a>[<span data-ttu-id="d12ab-173">Eingabeaufforderung</span><span class="sxs-lookup"><span data-stu-id="d12ab-173">Command Prompt</span></span>](#tab/windows)

```bash
wt -p "Command Prompt" ; split-pane -p "Windows PowerShell" ; split-pane -H wsl.exe
```

#### <a name="powershell"></a>[<span data-ttu-id="d12ab-174">PowerShell</span><span class="sxs-lookup"><span data-stu-id="d12ab-174">PowerShell</span></span>](#tab/powershell)

```powershell
wt -p "Command Prompt" `; split-pane -p "Windows PowerShell" `; split-pane -H wsl.exe
```

<span data-ttu-id="d12ab-175">PowerShell verwendet ein Semikolon (;), um Anweisungen zu trennen.</span><span class="sxs-lookup"><span data-stu-id="d12ab-175">PowerShell uses a semicolon ; to delimit statements.</span></span> <span data-ttu-id="d12ab-176">Wenn Sie ein Semikolon (;) als Befehlstrennzeichen für wt-Befehlszeilenargumente interpretieren möchten, müssen Sie Hochkommas als Escapezeichen für Semikolons verwenden.</span><span class="sxs-lookup"><span data-stu-id="d12ab-176">To interpret a semicolon ; as a command delimiter for wt command line arguments, you need to escape semicolon characters using backticks.</span></span> <span data-ttu-id="d12ab-177">PowerShell verfügt auch über den Operator zum Beenden der Analyse (--%), der das Programm anweist, das Interpretieren im Anschluss an den Operator einzustellen und die Zeichen einfach unverändert weiterzugeben.</span><span class="sxs-lookup"><span data-stu-id="d12ab-177">PowerShell also has the stop parsing operator (--%), which instructs it to stop interpreting anything after it and just pass it on verbatim.</span></span>

#### <a name="linux"></a>[<span data-ttu-id="d12ab-178">Linux</span><span class="sxs-lookup"><span data-stu-id="d12ab-178">Linux</span></span>](#tab/linux)

```bash
cmd.exe /c "wt.exe" -p "Command Prompt" \; split-pane -p "Windows PowerShell" \; split-pane -H wsl.exe
```

<span data-ttu-id="d12ab-179">Ausführungsaliase funktionieren nicht in WSL-Distributionen.</span><span class="sxs-lookup"><span data-stu-id="d12ab-179">Execution aliases do not work in WSL distributions.</span></span> <span data-ttu-id="d12ab-180">Wenn Sie „wt.exe“ über eine WSL-Befehlszeile verwenden möchten, können Sie es direkt über CMD erstellen, indem Sie `cmd.exe` ausführen.</span><span class="sxs-lookup"><span data-stu-id="d12ab-180">If you want to use wt.exe from a WSL command line, you can spawn it from CMD directly by running `cmd.exe`.</span></span> <span data-ttu-id="d12ab-181">Die Option `/c` weist CMD an, nach der Ausführung zu beenden, und „`\;` Schrägstrich + Semikolon“ trennt Befehle.</span><span class="sxs-lookup"><span data-stu-id="d12ab-181">The `/c` option tells CMD to terminate after running and the `\;` forward-slash + semicolon separates commands.</span></span>

---
<!-- End tab selectors.  -->

<span data-ttu-id="d12ab-182">Das Flag `-H` (oder `--horizontal`) gibt an, dass die Bereiche horizontal geteilt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="d12ab-182">The `-H` flag (or `--horizontal`) indicates that you would like the panes to be split horizontally.</span></span> <span data-ttu-id="d12ab-183">Das Flag `-V` (oder `--vertical`) gibt an, dass die Bereiche vertikal geteilt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="d12ab-183">The `-V` flag (or `--vertical`) indicates that you would like the panes split vertically.</span></span>

### <a name="tab-focus"></a><span data-ttu-id="d12ab-184">Registerkartenfokus</span><span class="sxs-lookup"><span data-stu-id="d12ab-184">Tab focus</span></span>

<span data-ttu-id="d12ab-185">Verwenden Sie das Flag `-t` (oder `--target`) zusammen mit der Indexnummer der Registerkarte, um eine neue Terminalinstanz mit Fokus auf eine bestimmte Registerkarte zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="d12ab-185">To open a new terminal instance with a specific tab in focus, use the `-t` flag (or `--target`), along with the tab-index number.</span></span> <span data-ttu-id="d12ab-186">Geben Sie Folgendes ein, um Ihr Standardprofil auf der ersten Registerkarte und das auf der zweiten Registerkarte fokussierte Profil „Ubuntu-18.04“ (`-t 1`) zu öffnen:</span><span class="sxs-lookup"><span data-stu-id="d12ab-186">To open your default profile in the first tab and the "Ubuntu-18.04" profile focused in the second tab (`-t 1`), enter:</span></span>

<!-- Start tab selectors. -->
#### <a name="command-prompt"></a>[<span data-ttu-id="d12ab-187">Eingabeaufforderung</span><span class="sxs-lookup"><span data-stu-id="d12ab-187">Command Prompt</span></span>](#tab/windows)

```bash
wt ; new-tab -p "Ubuntu-18.04" ; focus-tab -t 1
```

#### <a name="powershell"></a>[<span data-ttu-id="d12ab-188">PowerShell</span><span class="sxs-lookup"><span data-stu-id="d12ab-188">PowerShell</span></span>](#tab/powershell)

```powershell
wt `; new-tab -p "Ubuntu-18.04" `; focus-tab -t 1
```

#### <a name="linux"></a>[<span data-ttu-id="d12ab-189">Linux</span><span class="sxs-lookup"><span data-stu-id="d12ab-189">Linux</span></span>](#tab/linux)

```bash
cmd.exe /c "wt.exe" \; new-tab -p "Ubuntu-18.04" \; focus-tab -t 1
```

<span data-ttu-id="d12ab-190">Ausführungsaliase funktionieren nicht in WSL-Distributionen.</span><span class="sxs-lookup"><span data-stu-id="d12ab-190">Execution aliases do not work in WSL distributions.</span></span> <span data-ttu-id="d12ab-191">Wenn Sie „wt.exe“ über eine WSL-Befehlszeile verwenden möchten, können Sie es direkt über CMD erstellen, indem Sie `cmd.exe` ausführen.</span><span class="sxs-lookup"><span data-stu-id="d12ab-191">If you want to use wt.exe from a WSL command line, you can spawn it from CMD directly by running `cmd.exe`.</span></span> <span data-ttu-id="d12ab-192">Die Option `/c` weist CMD an, nach der Ausführung zu beenden, und „`\;` Schrägstrich + Semikolon“ trennt Befehle.</span><span class="sxs-lookup"><span data-stu-id="d12ab-192">The `/c` option tells CMD to terminate after running and the `\;` forward-slash + semicolon separates commands.</span></span>

---
<!-- End tab selectors.  -->

## <a name="examples-of-multiple-commands-from-powershell"></a><span data-ttu-id="d12ab-193">Beispiele für mehrere Befehle von PowerShell</span><span class="sxs-lookup"><span data-stu-id="d12ab-193">Examples of multiple commands from PowerShell</span></span>

<span data-ttu-id="d12ab-194">Windows Terminal verwendet das Semikolon (`;`) als Trennzeichen für Befehle in der `wt`-Befehlszeile.</span><span class="sxs-lookup"><span data-stu-id="d12ab-194">The Windows Terminal uses the semicolon character `;` as a delimiter for separating commands in the `wt` command line.</span></span> <span data-ttu-id="d12ab-195">Leider verwendet auch PowerShell `;` als Befehlstrennzeichen.</span><span class="sxs-lookup"><span data-stu-id="d12ab-195">Unfortunately, PowerShell also uses `;` as a command separator.</span></span> <span data-ttu-id="d12ab-196">Um dieses Problem zu umgehen, können Sie die folgenden Tricks verwenden, um mehrere `wt`-Befehle von PowerShell auszuführen.</span><span class="sxs-lookup"><span data-stu-id="d12ab-196">To work around this, you can use the following tricks to run multiple `wt` commands from PowerShell.</span></span> <span data-ttu-id="d12ab-197">In allen folgenden Beispielen wird ein neues Terminalfenster mit drei Bereichen erstellt: Ein Bereich, in dem die Eingabeaufforderung ausgeführt wird, ein Bereich mit PowerShell und der letzte Bereich mit WSL.</span><span class="sxs-lookup"><span data-stu-id="d12ab-197">In all the following examples, a new terminal window is created with three panes - one running Command Prompt, one with PowerShell, and the last one running WSL.</span></span>

<span data-ttu-id="d12ab-198">In den folgenden Beispielen wird der `Start-Process`-Befehl verwendet, um `wt` auszuführen.</span><span class="sxs-lookup"><span data-stu-id="d12ab-198">The following examples use the `Start-Process` command to run `wt`.</span></span> <span data-ttu-id="d12ab-199">Weitere Informationen dazu, warum das Terminal `Start-Process` verwendet, finden Sie nachfolgend unter [Verwenden von „start“](#using-start).</span><span class="sxs-lookup"><span data-stu-id="d12ab-199">For more information on why the terminal uses `Start-Process`, see [Using start](#using-start) below.</span></span>

### <a name="single-quoted-parameters"></a><span data-ttu-id="d12ab-200">Parameter in einfachen Anführungszeichen</span><span class="sxs-lookup"><span data-stu-id="d12ab-200">Single quoted parameters</span></span>

<span data-ttu-id="d12ab-201">In diesem Beispiel werden die `wt`-Parameter in einfache Anführungszeichen (`'`) eingeschlossen.</span><span class="sxs-lookup"><span data-stu-id="d12ab-201">In this example, the `wt` parameters are wrapped in single quotes (`'`).</span></span> <span data-ttu-id="d12ab-202">Diese Syntax ist hilfreich, wenn keine Berechnungen durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="d12ab-202">This syntax is useful if nothing is being calculated.</span></span>

```powershell
start wt 'new-tab "cmd" ; split-pane -p "Windows PowerShell" ; split-pane -H wsl.exe'
```

### <a name="escaped-quotes"></a><span data-ttu-id="d12ab-203">Anführungszeichen mit Escapezeichen</span><span class="sxs-lookup"><span data-stu-id="d12ab-203">Escaped quotes</span></span>

<span data-ttu-id="d12ab-204">Verwenden Sie die folgende Syntax, wenn Sie einen in einer Variablen enthaltenen Wert an die `wt`-Befehlszeile übergeben:</span><span class="sxs-lookup"><span data-stu-id="d12ab-204">When passing a value contained in a variable to the `wt` command line, use the following syntax:</span></span>

```powershell
$ThirdPane = "wsl.exe"
start wt "new-tab cmd ; split-pane -p `"Windows PowerShell`" ; split-pane -H $ThirdPane"
```

<span data-ttu-id="d12ab-205">Beachten Sie die Verwendung von `` ` `` als Escapezeichen für die doppelten Anführungszeichen (`"`) von "Windows PowerShell" im `-p`-Parameter für den Parameter `split-pane`.</span><span class="sxs-lookup"><span data-stu-id="d12ab-205">Note the usage of  `` ` `` to escape the double-quotes (`"`) around "Windows PowerShell" in the `-p` parameter to the `split-pane` parameter.</span></span>

### <a name="using-start"></a><span data-ttu-id="d12ab-206">Verwenden von `start`</span><span class="sxs-lookup"><span data-stu-id="d12ab-206">Using `start`</span></span>

<span data-ttu-id="d12ab-207">In allen obigen Beispielen wurde explizit `start` verwendet, um das Terminal zu starten.</span><span class="sxs-lookup"><span data-stu-id="d12ab-207">All the above examples explicitly used `start` to launch the terminal.</span></span>

<span data-ttu-id="d12ab-208">Die folgenden Beispiele verwenden nicht `start`, um die Befehlszeile auszuführen.</span><span class="sxs-lookup"><span data-stu-id="d12ab-208">The following examples do not use `start` to run the command line.</span></span> <span data-ttu-id="d12ab-209">Stattdessen gibt es zwei weitere Methoden, um Escapezeichen in der Befehlszeile zu verwenden:</span><span class="sxs-lookup"><span data-stu-id="d12ab-209">Instead, there are two other methods of escaping the command line:</span></span>

* <span data-ttu-id="d12ab-210">Die Semikolons werden nur mit Escapezeichen versehen, damit sie von `PowerShell` ignoriert und direkt an `wt` weitergegeben werden.</span><span class="sxs-lookup"><span data-stu-id="d12ab-210">Only escaping the semicolons so that `PowerShell` will ignore them and pass them straight to `wt`.</span></span>
* <span data-ttu-id="d12ab-211">Wenn Sie `--%` verwenden, behandelt PowerShell den Rest der Befehlszeile als Argumente für die Anwendung.</span><span class="sxs-lookup"><span data-stu-id="d12ab-211">Using `--%`, so PowerShell will treat the rest of the command line as arguments to the application.</span></span>

```powershell
wt new-tab "cmd" `; split-pane -p "Windows PowerShell" `; split-pane -H wsl.exe
```

```powershell
wt --% new-tab cmd ; split-pane -p "Windows PowerShell" ; split-pane -H wsl.exe
```

<span data-ttu-id="d12ab-212">In beiden Beispielen erstellt das neu erstellte Windows Terminal-Fenster das Fenster durch die ordnungsgemäße Analyse aller bereitgestellten Befehlszeilenargumente.</span><span class="sxs-lookup"><span data-stu-id="d12ab-212">In both of these examples, the newly created Windows Terminal window will create the window by correctly parsing all the provided command line arguments.</span></span>

<span data-ttu-id="d12ab-213">Diese Methoden werden derzeit jedoch _nicht_ empfohlen, da PowerShell auf das Schließen des neu erstellten Terminalfensters wartet, bevor die Kontrolle an PowerShell zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="d12ab-213">However, these methods are _not_ recommended currently, as PowerShell will wait for the newly-created terminal window to be closed before returning control to PowerShell.</span></span> <span data-ttu-id="d12ab-214">Standardmäßig wartet PowerShell immer auf das Schließen von Windows Store-Anwendungen (wie Windows Terminal), bevor es zur Eingabeaufforderung zurückkehrt.</span><span class="sxs-lookup"><span data-stu-id="d12ab-214">By default, PowerShell will always wait for Windows Store applications (like the Windows Terminal) to close before returning to the prompt.</span></span> <span data-ttu-id="d12ab-215">Beachten Sie, dass dies nicht dem Verhalten der Eingabeaufforderung entspricht, bei dem sofort zur Eingabeaufforderung zurückkehrt wird.</span><span class="sxs-lookup"><span data-stu-id="d12ab-215">Note that this is different than the behavior of Command Prompt, which will return to the prompt immediately.</span></span>
