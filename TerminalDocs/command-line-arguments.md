---
title: Windows Terminal-Befehlszeilenargumente
description: Erfahren Sie, wie Sie Befehlszeilenargumente für Windows Terminal erstellen.
author: cinnamon-msft
ms.author: cinnamon
ms.date: 06/18/2020
ms.topic: how-to
ms.service: terminal
ms.openlocfilehash: d40b0527bab94289457cf8c8a88931f4df943496
ms.sourcegitcommit: 91a802863cd0730d2e364377ffe44f819a66ff2a
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/18/2020
ms.locfileid: "84994376"
---
# <a name="using-command-line-arguments-for-windows-terminal"></a><span data-ttu-id="d4363-103">Verwenden von Befehlszeilenargumenten für Windows Terminal</span><span class="sxs-lookup"><span data-stu-id="d4363-103">Using command-line arguments for Windows Terminal</span></span>

<span data-ttu-id="d4363-104">Sie können `wt.exe` verwenden, um eine neue Instanz von Windows Terminal über die Befehlszeile zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="d4363-104">You can use `wt.exe` to open a new instance of Windows Terminal from the command line.</span></span> <span data-ttu-id="d4363-105">Sie können stattdessen auch den Ausführungsalias `wt` verwenden.</span><span class="sxs-lookup"><span data-stu-id="d4363-105">You can also use the execution alias `wt` instead.</span></span>

> [!NOTE]
> <span data-ttu-id="d4363-106">Wenn Sie Windows Terminal aus dem Quellcode auf [GitHub](https://github.com/microsoft/terminal) erstellt haben, können Sie diesen Build mit `wtd.exe` oder `wtd` öffnen.</span><span class="sxs-lookup"><span data-stu-id="d4363-106">If you built Windows Terminal from the source code on [GitHub](https://github.com/microsoft/terminal), you can open that build using `wtd.exe` or `wtd`.</span></span>

![Windows Terminal-Befehlszeilenargument für geteilte Bereiche](./images/terminal-command-args.gif)

## <a name="command-line-syntax"></a><span data-ttu-id="d4363-108">Befehlszeilensyntax</span><span class="sxs-lookup"><span data-stu-id="d4363-108">Command line syntax</span></span>

<span data-ttu-id="d4363-109">Die `wt`-Befehlszeile akzeptiert zwei Arten von Werten: **Optionen** und **Befehle**.</span><span class="sxs-lookup"><span data-stu-id="d4363-109">The `wt` command line accepts two types of values: **options** and **commands**.</span></span> <span data-ttu-id="d4363-110">**Optionen** sind eine Liste von Flags und anderen Parametern, die das Verhalten der `wt`-Befehlszeile als Ganzes steuern können.</span><span class="sxs-lookup"><span data-stu-id="d4363-110">**Options** are a list of flags and other parameters that can control the behavior of the `wt` command line as a whole.</span></span> <span data-ttu-id="d4363-111">**Befehle** geben die Aktion oder eine durch Semikolon getrennte Liste von Aktionen an, die ausgeführt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="d4363-111">**Commands** provide the action, or list of actions separated by semicolons, that should be implemented.</span></span> <span data-ttu-id="d4363-112">Wenn Sie keinen Befehl angeben, wird `new-tab` standardmäßig als Befehl angenommen.</span><span class="sxs-lookup"><span data-stu-id="d4363-112">If no command is specified, then the command is assumed to be `new-tab` by default.</span></span>

```bash
wt [options] [command ; ]
```

<span data-ttu-id="d4363-113">Geben Sie Folgendes ein, um eine Hilfemeldung mit den verfügbaren Befehlszeilenargumenten anzuzeigen: `wt -h`, `wt --help`, `wt -?` oder `wt /?`.</span><span class="sxs-lookup"><span data-stu-id="d4363-113">To display a help message listing the available command-line arguments, enter: `wt -h`, `wt --help`, `wt -?`, or `wt /?`.</span></span>

## <a name="options-and-commands"></a><span data-ttu-id="d4363-114">Optionen und Befehle</span><span class="sxs-lookup"><span data-stu-id="d4363-114">Options and commands</span></span>

<span data-ttu-id="d4363-115">Im Folgenden finden Sie die vollständige Liste der unterstützten Befehle und Optionen für die `wt`-Befehlszeile.</span><span class="sxs-lookup"><span data-stu-id="d4363-115">Below is the full list of supported commands and options for the `wt` command line.</span></span>

| <span data-ttu-id="d4363-116">Option</span><span class="sxs-lookup"><span data-stu-id="d4363-116">Option</span></span> | <span data-ttu-id="d4363-117">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d4363-117">Description</span></span> |
| ------ | ----------- |
| <span data-ttu-id="d4363-118">`--help`, `-h`, `-?`, `/?`</span><span class="sxs-lookup"><span data-stu-id="d4363-118">`--help`, `-h`, `-?`, `/?`</span></span> | <span data-ttu-id="d4363-119">Zeigt die Hilfemeldung an.</span><span class="sxs-lookup"><span data-stu-id="d4363-119">Displays the help message.</span></span> |
| <span data-ttu-id="d4363-120">`--maximized`, `-M`</span><span class="sxs-lookup"><span data-stu-id="d4363-120">`--maximized`, `-M`</span></span> | <span data-ttu-id="d4363-121">Öffnet das Terminal maximiert.</span><span class="sxs-lookup"><span data-stu-id="d4363-121">Launches the terminal maximized.</span></span> |
| <span data-ttu-id="d4363-122">`--fullscreen`, `-F`</span><span class="sxs-lookup"><span data-stu-id="d4363-122">`--fullscreen`, `-F`</span></span> | <span data-ttu-id="d4363-123">Öffnet das Terminal im Vollbildmodus.</span><span class="sxs-lookup"><span data-stu-id="d4363-123">Launches the terminal as full screen.</span></span> |

> [!IMPORTANT]
> <span data-ttu-id="d4363-124">`--maximized`, `-M` und `--fullscreen`, `-F` stehen nur in der [Windows Terminal-Vorschau](https://aka.ms/terminal-preview/) zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="d4363-124">`--maximized`, `-M` and `--fullscreen`, `-F` are only available in [Windows Terminal Preview](https://aka.ms/terminal-preview/).</span></span>

| <span data-ttu-id="d4363-125">Befehl</span><span class="sxs-lookup"><span data-stu-id="d4363-125">Command</span></span> | <span data-ttu-id="d4363-126">Parameter</span><span class="sxs-lookup"><span data-stu-id="d4363-126">Parameters</span></span> | <span data-ttu-id="d4363-127">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d4363-127">Description</span></span> |
| ------- | ---------- | ----------- |
| `new-tab` | <span data-ttu-id="d4363-128">`--profile, -p profile-name`, `--startingDirectory, -d starting-directory`, `commandline`, `--title`</span><span class="sxs-lookup"><span data-stu-id="d4363-128">`--profile, -p profile-name`, `--startingDirectory, -d starting-directory`, `commandline`, `--title`</span></span> | <span data-ttu-id="d4363-129">Erstellt eine neue Registerkarte.</span><span class="sxs-lookup"><span data-stu-id="d4363-129">Creates a new tab.</span></span> |
| `split-pane` | <span data-ttu-id="d4363-130">`-H, --horizontal`, `-V, --vertical`, `--profile, -p profile-name`, `--startingDirectory, -d starting-directory`, `commandline`, `--title`</span><span class="sxs-lookup"><span data-stu-id="d4363-130">`-H, --horizontal`, `-V, --vertical`, `--profile, -p profile-name`, `--startingDirectory, -d starting-directory`, `commandline`, `--title`</span></span> | <span data-ttu-id="d4363-131">Unterteilt einen neuen Bereich.</span><span class="sxs-lookup"><span data-stu-id="d4363-131">Splits a new pane.</span></span> |
| `focus-tab` | `--target, -t tab-index` | <span data-ttu-id="d4363-132">Setzt den Fokus auf eine bestimmte Registerkarte.</span><span class="sxs-lookup"><span data-stu-id="d4363-132">Focuses on a specific tab.</span></span> |

> [!IMPORTANT]
> <span data-ttu-id="d4363-133">`--title` steht nur in der [Windows Terminal-Vorschau](https://aka.ms/terminal-preview/) zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="d4363-133">`--title` is only available in [Windows Terminal Preview](https://aka.ms/terminal-preview/).</span></span>

## <a name="command-line-argument-examples"></a><span data-ttu-id="d4363-134">Beispiele für Befehlszeilenargumente</span><span class="sxs-lookup"><span data-stu-id="d4363-134">Command line argument examples</span></span>

<span data-ttu-id="d4363-135">Die Befehle können leicht variieren, je nachdem, welche Befehlszeile Sie verwenden.</span><span class="sxs-lookup"><span data-stu-id="d4363-135">Commands may vary slightly depending on which command line you're using.</span></span>

### <a name="open-a-new-profile-instance"></a><span data-ttu-id="d4363-136">Eine neue Profilinstanz öffnen</span><span class="sxs-lookup"><span data-stu-id="d4363-136">Open a new profile instance</span></span>

<span data-ttu-id="d4363-137">Geben Sie Folgendes ein, um eine neue Terminalinstanz zu öffnen. In diesem Fall öffnet der Befehl das Profil mit dem Namen „Ubuntu-18.04“:</span><span class="sxs-lookup"><span data-stu-id="d4363-137">To open a new terminal instance, in this case the command will open the profile named "Ubuntu-18.04", enter:</span></span>

<!-- Start tab selectors. -->
#### <a name="command-prompt"></a>[<span data-ttu-id="d4363-138">Eingabeaufforderung</span><span class="sxs-lookup"><span data-stu-id="d4363-138">Command Prompt</span></span>](#tab/windows)

```bash
wt -p "Ubuntu-18.04"
```

#### <a name="powershell"></a>[<span data-ttu-id="d4363-139">PowerShell</span><span class="sxs-lookup"><span data-stu-id="d4363-139">PowerShell</span></span>](#tab/powershell)

```powershell
wt -p "Ubuntu-18.04"
```

#### <a name="linux"></a>[<span data-ttu-id="d4363-140">Linux</span><span class="sxs-lookup"><span data-stu-id="d4363-140">Linux</span></span>](#tab/linux)

```bash
cmd.exe /c "wt.exe" -p "Ubuntu-18.04"
```

<span data-ttu-id="d4363-141">Ausführungsaliase funktionieren nicht in WSL-Distributionen.</span><span class="sxs-lookup"><span data-stu-id="d4363-141">Execution aliases do not work in WSL distributions.</span></span> <span data-ttu-id="d4363-142">Wenn Sie „wt.exe“ über eine WSL-Befehlszeile verwenden möchten, können Sie es direkt über CMD erstellen, indem Sie `cmd.exe` ausführen.</span><span class="sxs-lookup"><span data-stu-id="d4363-142">If you want to use wt.exe from a WSL command line, you can spawn it from CMD directly by running `cmd.exe`.</span></span> <span data-ttu-id="d4363-143">Die Option `/c` weist CMD an, den Vorgang nach der Ausführung zu beenden.</span><span class="sxs-lookup"><span data-stu-id="d4363-143">The `/c` option tells CMD to terminate after running.</span></span>

---
<!-- End tab selectors.  -->

 <span data-ttu-id="d4363-144">Das `-p`-Flag wird verwendet, um das zu öffnende Windows Terminal-Profil anzugeben.</span><span class="sxs-lookup"><span data-stu-id="d4363-144">The `-p` flag is used to specify the Windows Terminal profile that should be opened.</span></span> <span data-ttu-id="d4363-145">Ersetzen Sie „Ubuntu-18.04“ durch den Namen eines beliebigen Terminalprofils, das Sie installiert haben.</span><span class="sxs-lookup"><span data-stu-id="d4363-145">Substitute "Ubuntu-18.04" with the name of any terminal profile that you have installed.</span></span> <span data-ttu-id="d4363-146">Dadurch wird immer ein neues Fenster geöffnet.</span><span class="sxs-lookup"><span data-stu-id="d4363-146">This will always open a new window.</span></span> <span data-ttu-id="d4363-147">Windows Terminal ist noch nicht in der Lage, neue Registerkarten oder Bereiche in einer vorhandenen Instanz zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="d4363-147">Windows Terminal is not yet capable of opening new tabs or panes in an existing instance.</span></span>

### <a name="target-a-directory"></a><span data-ttu-id="d4363-148">Auswählen eines Zielverzeichnisses</span><span class="sxs-lookup"><span data-stu-id="d4363-148">Target a directory</span></span>

<span data-ttu-id="d4363-149">Geben Sie Folgendes ein, um den Ordner anzugeben, der als Startverzeichnis für die Konsole verwendet werden soll (in diesem Fall das Verzeichnis „d:\“):</span><span class="sxs-lookup"><span data-stu-id="d4363-149">To specify the folder that should be used as the starting directory for the console, in this case the d:\ directory, enter:</span></span>

<!-- Start tab selectors. -->
#### <a name="command-prompt"></a>[<span data-ttu-id="d4363-150">Eingabeaufforderung</span><span class="sxs-lookup"><span data-stu-id="d4363-150">Command Prompt</span></span>](#tab/windows)

```bash
wt -d d:\
```

#### <a name="powershell"></a>[<span data-ttu-id="d4363-151">PowerShell</span><span class="sxs-lookup"><span data-stu-id="d4363-151">PowerShell</span></span>](#tab/powershell)

```powershell
wt -d d:\
```

#### <a name="linux"></a>[<span data-ttu-id="d4363-152">Linux</span><span class="sxs-lookup"><span data-stu-id="d4363-152">Linux</span></span>](#tab/linux)

```bash
cmd.exe /c "wt.exe" -d d:\
```

<span data-ttu-id="d4363-153">Ausführungsaliase funktionieren nicht in WSL-Distributionen.</span><span class="sxs-lookup"><span data-stu-id="d4363-153">Execution aliases do not work in WSL distributions.</span></span> <span data-ttu-id="d4363-154">Wenn Sie „wt.exe“ über eine WSL-Befehlszeile verwenden möchten, können Sie es direkt über CMD erstellen, indem Sie `cmd.exe` ausführen.</span><span class="sxs-lookup"><span data-stu-id="d4363-154">If you want to use wt.exe from a WSL command line, you can spawn it from CMD directly by running `cmd.exe`.</span></span> <span data-ttu-id="d4363-155">Die Option `/c` weist CMD an, den Vorgang nach der Ausführung zu beenden.</span><span class="sxs-lookup"><span data-stu-id="d4363-155">The `/c` option tells CMD to terminate after running.</span></span>

---
<!-- End tab selectors.  -->

### <a name="multiple-tabs"></a><span data-ttu-id="d4363-156">Mehrere Registerkarten</span><span class="sxs-lookup"><span data-stu-id="d4363-156">Multiple tabs</span></span>

<span data-ttu-id="d4363-157">Geben Sie Folgendes ein, um eine neue Terminalinstanz mit mehreren Registerkarten zu öffnen:</span><span class="sxs-lookup"><span data-stu-id="d4363-157">To open a new terminal instance with multiple tabs, enter:</span></span>

<!-- Start tab selectors. -->
#### <a name="command-prompt"></a>[<span data-ttu-id="d4363-158">Eingabeaufforderung</span><span class="sxs-lookup"><span data-stu-id="d4363-158">Command Prompt</span></span>](#tab/windows)

```bash
wt ; ;
```

#### <a name="powershell"></a>[<span data-ttu-id="d4363-159">PowerShell</span><span class="sxs-lookup"><span data-stu-id="d4363-159">PowerShell</span></span>](#tab/powershell)

```powershell
wt `; `;
```

<span data-ttu-id="d4363-160">PowerShell verwendet ein Semikolon (;), um Anweisungen zu trennen.</span><span class="sxs-lookup"><span data-stu-id="d4363-160">PowerShell uses a semicolon ; to delimit statements.</span></span> <span data-ttu-id="d4363-161">Wenn Sie ein Semikolon (;) als Befehlstrennzeichen für wt-Befehlszeilenargumente interpretieren möchten, müssen Sie Hochkommas als Escapezeichen für Semikolons verwenden.</span><span class="sxs-lookup"><span data-stu-id="d4363-161">To interpret a semicolon ; as a command delimiter for wt command-line arguments, you need to escape semicolon characters using backticks.</span></span> <span data-ttu-id="d4363-162">PowerShell verfügt auch über den Operator zum Beenden der Analyse (--%), der das Programm anweist, das Interpretieren im Anschluss an den Operator einzustellen und die Zeichen einfach unverändert weiterzugeben.</span><span class="sxs-lookup"><span data-stu-id="d4363-162">PowerShell also has the stop parsing operator (--%), which instructs it to stop interpreting anything after it and just pass it on verbatim.</span></span>

#### <a name="linux"></a>[<span data-ttu-id="d4363-163">Linux</span><span class="sxs-lookup"><span data-stu-id="d4363-163">Linux</span></span>](#tab/linux)

```bash
cmd.exe /c "wt.exe" \; \;
```

<span data-ttu-id="d4363-164">Ausführungsaliase funktionieren nicht in WSL-Distributionen.</span><span class="sxs-lookup"><span data-stu-id="d4363-164">Execution aliases do not work in WSL distributions.</span></span> <span data-ttu-id="d4363-165">Wenn Sie „wt.exe“ über eine WSL-Befehlszeile verwenden möchten, können Sie es direkt über CMD erstellen, indem Sie `cmd.exe` ausführen.</span><span class="sxs-lookup"><span data-stu-id="d4363-165">If you want to use wt.exe from a WSL command line, you can spawn it from CMD directly by running `cmd.exe`.</span></span> <span data-ttu-id="d4363-166">Die Option `/c` weist CMD an, den Vorgang nach der Ausführung zu beenden.</span><span class="sxs-lookup"><span data-stu-id="d4363-166">The `/c` option tells CMD to terminate after running.</span></span>

---
<!-- End tab selectors.  -->

<span data-ttu-id="d4363-167">Geben Sie zum Öffnen einer neuen Terminalinstanz mit mehreren Registerkarten, in diesem Fall ein Eingabeaufforderungsprofil und ein PowerShell-Profil, Folgendes ein:</span><span class="sxs-lookup"><span data-stu-id="d4363-167">To open a new terminal instance with multiple tabs, in this case a Command Prompt profile and a PowerShell profile, enter:</span></span>

<!-- Start tab selectors. -->
#### <a name="command-prompt"></a>[<span data-ttu-id="d4363-168">Eingabeaufforderung</span><span class="sxs-lookup"><span data-stu-id="d4363-168">Command Prompt</span></span>](#tab/windows)

```bash
wt -p "Command Prompt" ; new-tab -p "Windows PowerShell"
```

#### <a name="powershell"></a>[<span data-ttu-id="d4363-169">PowerShell</span><span class="sxs-lookup"><span data-stu-id="d4363-169">PowerShell</span></span>](#tab/powershell)

```powershell
wt -p "Command Prompt" `; new-tab -p "Windows PowerShell"
```

<span data-ttu-id="d4363-170">PowerShell verwendet ein Semikolon (;), um Anweisungen zu trennen.</span><span class="sxs-lookup"><span data-stu-id="d4363-170">PowerShell uses a semicolon ; to delimit statements.</span></span> <span data-ttu-id="d4363-171">Wenn Sie ein Semikolon (;) als Befehlstrennzeichen für wt-Befehlszeilenargumente interpretieren möchten, müssen Sie Hochkommas als Escapezeichen für Semikolons verwenden.</span><span class="sxs-lookup"><span data-stu-id="d4363-171">To interpret a semicolon ; as a command delimiter for wt command-line arguments, you need to escape semicolon characters using backticks.</span></span> <span data-ttu-id="d4363-172">PowerShell verfügt auch über den Operator zum Beenden der Analyse (--%), der das Programm anweist, das Interpretieren im Anschluss an den Operator einzustellen und die Zeichen einfach unverändert weiterzugeben.</span><span class="sxs-lookup"><span data-stu-id="d4363-172">PowerShell also has the stop parsing operator (--%), which instructs it to stop interpreting anything after it and just pass it on verbatim.</span></span>

#### <a name="linux"></a>[<span data-ttu-id="d4363-173">Linux</span><span class="sxs-lookup"><span data-stu-id="d4363-173">Linux</span></span>](#tab/linux)

```bash
cmd.exe /c "wt.exe" -p "Command Prompt" \; new-tab -p "Windows Powershell"
```

<span data-ttu-id="d4363-174">Ausführungsaliase funktionieren nicht in WSL-Distributionen.</span><span class="sxs-lookup"><span data-stu-id="d4363-174">Execution aliases do not work in WSL distributions.</span></span> <span data-ttu-id="d4363-175">Wenn Sie „wt.exe“ über eine WSL-Befehlszeile verwenden möchten, können Sie es direkt über CMD erstellen, indem Sie `cmd.exe` ausführen.</span><span class="sxs-lookup"><span data-stu-id="d4363-175">If you want to use wt.exe from a WSL command line, you can spawn it from CMD directly by running `cmd.exe`.</span></span> <span data-ttu-id="d4363-176">Die Option `/c` weist CMD an, nach der Ausführung zu beenden, und „`\;` Schrägstrich + Semikolon“ trennt Befehle.</span><span class="sxs-lookup"><span data-stu-id="d4363-176">The `/c` option tells CMD to terminate after running and the `\;` forward-slash + semicolon separates commands.</span></span>

---
<!-- End tab selectors.  -->

### <a name="multiple-panes"></a><span data-ttu-id="d4363-177">Mehrere Bereiche</span><span class="sxs-lookup"><span data-stu-id="d4363-177">Multiple panes</span></span>

<span data-ttu-id="d4363-178">Geben Sie Folgendes ein, um eine neue Terminalinstanz mit einer Registerkarte zu öffnen, die drei Bereiche enthält, in denen ein Eingabeaufforderungsprofil, ein PowerShell-Profil und Ihr Standardprofil mit einer WSL-Befehlszeile ausgeführt wird:</span><span class="sxs-lookup"><span data-stu-id="d4363-178">To open a new terminal instance with one tab containing three panes running a Command Prompt profile, a PowerShell profile, and your default profile running a WSL command line, enter:</span></span>

<!-- Start tab selectors. -->
#### <a name="command-prompt"></a>[<span data-ttu-id="d4363-179">Eingabeaufforderung</span><span class="sxs-lookup"><span data-stu-id="d4363-179">Command Prompt</span></span>](#tab/windows)

```bash
wt -p "Command Prompt" ; split-pane -p "Windows PowerShell" ; split-pane -H wsl.exe
```

#### <a name="powershell"></a>[<span data-ttu-id="d4363-180">PowerShell</span><span class="sxs-lookup"><span data-stu-id="d4363-180">PowerShell</span></span>](#tab/powershell)

```powershell
wt -p "Command Prompt" `; split-pane -p "Windows PowerShell" `; split-pane -H wsl.exe
```

<span data-ttu-id="d4363-181">PowerShell verwendet ein Semikolon (;), um Anweisungen zu trennen.</span><span class="sxs-lookup"><span data-stu-id="d4363-181">PowerShell uses a semicolon ; to delimit statements.</span></span> <span data-ttu-id="d4363-182">Wenn Sie ein Semikolon (;) als Befehlstrennzeichen für wt-Befehlszeilenargumente interpretieren möchten, müssen Sie Hochkommas als Escapezeichen für Semikolons verwenden.</span><span class="sxs-lookup"><span data-stu-id="d4363-182">To interpret a semicolon ; as a command delimiter for wt command-line arguments, you need to escape semicolon characters using backticks.</span></span> <span data-ttu-id="d4363-183">PowerShell verfügt auch über den Operator zum Beenden der Analyse (--%), der das Programm anweist, das Interpretieren im Anschluss an den Operator einzustellen und die Zeichen einfach unverändert weiterzugeben.</span><span class="sxs-lookup"><span data-stu-id="d4363-183">PowerShell also has the stop parsing operator (--%), which instructs it to stop interpreting anything after it and just pass it on verbatim.</span></span>

#### <a name="linux"></a>[<span data-ttu-id="d4363-184">Linux</span><span class="sxs-lookup"><span data-stu-id="d4363-184">Linux</span></span>](#tab/linux)

```bash
cmd.exe /c "wt.exe" -p "Command Prompt" \; split-pane -p "Windows PowerShell" \; split-pane -H wsl.exe
```

<span data-ttu-id="d4363-185">Ausführungsaliase funktionieren nicht in WSL-Distributionen.</span><span class="sxs-lookup"><span data-stu-id="d4363-185">Execution aliases do not work in WSL distributions.</span></span> <span data-ttu-id="d4363-186">Wenn Sie „wt.exe“ über eine WSL-Befehlszeile verwenden möchten, können Sie es direkt über CMD erstellen, indem Sie `cmd.exe` ausführen.</span><span class="sxs-lookup"><span data-stu-id="d4363-186">If you want to use wt.exe from a WSL command line, you can spawn it from CMD directly by running `cmd.exe`.</span></span> <span data-ttu-id="d4363-187">Die Option `/c` weist CMD an, nach der Ausführung zu beenden, und „`\;` Schrägstrich + Semikolon“ trennt Befehle.</span><span class="sxs-lookup"><span data-stu-id="d4363-187">The `/c` option tells CMD to terminate after running and the `\;` forward-slash + semicolon separates commands.</span></span>

---
<!-- End tab selectors.  -->

<span data-ttu-id="d4363-188">Das Flag `-H` (oder `--horizontal`) gibt an, dass die Bereiche horizontal geteilt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="d4363-188">The `-H` flag (or `--horizontal`) indicates that you would like the panes to be split horizontally.</span></span> <span data-ttu-id="d4363-189">Das Flag `-V` (oder `--vertical`) gibt an, dass die Bereiche vertikal geteilt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="d4363-189">The `-V` flag (or `--vertical`) indicates that you would like the panes split vertically.</span></span>

### <a name="tab-title-preview"></a><span data-ttu-id="d4363-190">Registerkartentitel ([Vorschau](https://aka.ms/terminal-preview/))</span><span class="sxs-lookup"><span data-stu-id="d4363-190">Tab title ([Preview](https://aka.ms/terminal-preview/))</span></span>

<span data-ttu-id="d4363-191">Um eine neue Terminalinstanz mit benutzerdefinierten Registerkartentiteln zu öffnen, verwenden Sie das `--title`-Argument.</span><span class="sxs-lookup"><span data-stu-id="d4363-191">To open a new terminal instance with custom tab titles, use the `--title` argument.</span></span> <span data-ttu-id="d4363-192">Um beim Öffnen von zwei Registerkarten die Titel beider Registerkarten festzulegen, geben Sie Folgendes ein:</span><span class="sxs-lookup"><span data-stu-id="d4363-192">To set the title of each tab when opening two tabs, enter:</span></span>

<!-- Start tab selectors. -->
#### <a name="command-prompt"></a>[<span data-ttu-id="d4363-193">Eingabeaufforderung</span><span class="sxs-lookup"><span data-stu-id="d4363-193">Command Prompt</span></span>](#tab/windows)

```bash
wt --title tabname1 ; new-tab -p "Ubuntu-18.04" --title tabname2
```

#### <a name="powershell"></a>[<span data-ttu-id="d4363-194">PowerShell</span><span class="sxs-lookup"><span data-stu-id="d4363-194">PowerShell</span></span>](#tab/powershell)

```powershell
wt --title tabname1 `; new-tab -p "Ubuntu-18.04" --title tabname2
```

#### <a name="linux"></a>[<span data-ttu-id="d4363-195">Linux</span><span class="sxs-lookup"><span data-stu-id="d4363-195">Linux</span></span>](#tab/linux)

```bash
cmd.exe /c "wt.exe" --title tabname1 \; new-tab -p "Ubuntu-18.04" --title tabname2
```

<span data-ttu-id="d4363-196">Ausführungsaliase funktionieren nicht in WSL-Distributionen.</span><span class="sxs-lookup"><span data-stu-id="d4363-196">Execution aliases do not work in WSL distributions.</span></span> <span data-ttu-id="d4363-197">Wenn Sie „wt.exe“ über eine WSL-Befehlszeile verwenden möchten, können Sie es direkt über CMD erstellen, indem Sie `cmd.exe` ausführen.</span><span class="sxs-lookup"><span data-stu-id="d4363-197">If you want to use wt.exe from a WSL command line, you can spawn it from CMD directly by running `cmd.exe`.</span></span> <span data-ttu-id="d4363-198">Die Option `/c` weist CMD an, nach der Ausführung zu beenden, und „`\;` Schrägstrich + Semikolon“ trennt Befehle.</span><span class="sxs-lookup"><span data-stu-id="d4363-198">The `/c` option tells CMD to terminate after running and the `\;` forward-slash + semicolon separates commands.</span></span>

---
<!-- End tab selectors.  -->

> [!IMPORTANT]
> <span data-ttu-id="d4363-199">Diese Funktion steht nur in der [Windows Terminal-Vorschau](https://aka.ms/terminal-preview/) zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="d4363-199">This feature is only available in [Windows Terminal Preview](https://aka.ms/terminal-preview/).</span></span>

### <a name="tab-focus"></a><span data-ttu-id="d4363-200">Registerkartenfokus</span><span class="sxs-lookup"><span data-stu-id="d4363-200">Tab focus</span></span>

<span data-ttu-id="d4363-201">Verwenden Sie das Flag `-t` (oder `--target`) zusammen mit der Indexnummer der Registerkarte, um eine neue Terminalinstanz mit Fokus auf eine bestimmte Registerkarte zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="d4363-201">To open a new terminal instance with a specific tab in focus, use the `-t` flag (or `--target`), along with the tab-index number.</span></span> <span data-ttu-id="d4363-202">Geben Sie Folgendes ein, um Ihr Standardprofil auf der ersten Registerkarte und das auf der zweiten Registerkarte fokussierte Profil „Ubuntu-18.04“ (`-t 1`) zu öffnen:</span><span class="sxs-lookup"><span data-stu-id="d4363-202">To open your default profile in the first tab and the "Ubuntu-18.04" profile focused in the second tab (`-t 1`), enter:</span></span>

<!-- Start tab selectors. -->
#### <a name="command-prompt"></a>[<span data-ttu-id="d4363-203">Eingabeaufforderung</span><span class="sxs-lookup"><span data-stu-id="d4363-203">Command Prompt</span></span>](#tab/windows)

```bash
wt ; new-tab -p "Ubuntu-18.04" ; focus-tab -t 1
```

#### <a name="powershell"></a>[<span data-ttu-id="d4363-204">PowerShell</span><span class="sxs-lookup"><span data-stu-id="d4363-204">PowerShell</span></span>](#tab/powershell)

```powershell
wt `; new-tab -p "Ubuntu-18.04" `; focus-tab -t 1
```

#### <a name="linux"></a>[<span data-ttu-id="d4363-205">Linux</span><span class="sxs-lookup"><span data-stu-id="d4363-205">Linux</span></span>](#tab/linux)

```bash
cmd.exe /c "wt.exe" \; new-tab -p "Ubuntu-18.04" \; focus-tab -t 1
```

<span data-ttu-id="d4363-206">Ausführungsaliase funktionieren nicht in WSL-Distributionen.</span><span class="sxs-lookup"><span data-stu-id="d4363-206">Execution aliases do not work in WSL distributions.</span></span> <span data-ttu-id="d4363-207">Wenn Sie „wt.exe“ über eine WSL-Befehlszeile verwenden möchten, können Sie es direkt über CMD erstellen, indem Sie `cmd.exe` ausführen.</span><span class="sxs-lookup"><span data-stu-id="d4363-207">If you want to use wt.exe from a WSL command line, you can spawn it from CMD directly by running `cmd.exe`.</span></span> <span data-ttu-id="d4363-208">Die Option `/c` weist CMD an, nach der Ausführung zu beenden, und „`\;` Schrägstrich + Semikolon“ trennt Befehle.</span><span class="sxs-lookup"><span data-stu-id="d4363-208">The `/c` option tells CMD to terminate after running and the `\;` forward-slash + semicolon separates commands.</span></span>

---
<!-- End tab selectors.  -->

## <a name="examples-of-multiple-commands-from-powershell"></a><span data-ttu-id="d4363-209">Beispiele für mehrere Befehle von PowerShell</span><span class="sxs-lookup"><span data-stu-id="d4363-209">Examples of multiple commands from PowerShell</span></span>

<span data-ttu-id="d4363-210">Windows Terminal verwendet das Semikolon (`;`) als Trennzeichen für Befehle in der `wt`-Befehlszeile.</span><span class="sxs-lookup"><span data-stu-id="d4363-210">Windows Terminal uses the semicolon character `;` as a delimiter for separating commands in the `wt` command line.</span></span> <span data-ttu-id="d4363-211">Leider verwendet auch PowerShell `;` als Befehlstrennzeichen.</span><span class="sxs-lookup"><span data-stu-id="d4363-211">Unfortunately, PowerShell also uses `;` as a command separator.</span></span> <span data-ttu-id="d4363-212">Um dieses Problem zu umgehen, können Sie die folgenden Tricks verwenden, um mehrere `wt`-Befehle von PowerShell auszuführen.</span><span class="sxs-lookup"><span data-stu-id="d4363-212">To work around this, you can use the following tricks to run multiple `wt` commands from PowerShell.</span></span> <span data-ttu-id="d4363-213">In allen folgenden Beispielen wird ein neues Terminalfenster mit drei Bereichen erstellt: Ein Bereich, in dem die Eingabeaufforderung ausgeführt wird, ein Bereich mit PowerShell und der letzte Bereich mit WSL.</span><span class="sxs-lookup"><span data-stu-id="d4363-213">In all the following examples, a new terminal window is created with three panes - one running Command Prompt, one with PowerShell, and the last one running WSL.</span></span>

<span data-ttu-id="d4363-214">In den folgenden Beispielen wird der `Start-Process`-Befehl verwendet, um `wt` auszuführen.</span><span class="sxs-lookup"><span data-stu-id="d4363-214">The following examples use the `Start-Process` command to run `wt`.</span></span> <span data-ttu-id="d4363-215">Weitere Informationen dazu, warum das Terminal `Start-Process` verwendet, finden Sie nachfolgend unter [Verwenden von „start“](#using-start).</span><span class="sxs-lookup"><span data-stu-id="d4363-215">For more information on why the terminal uses `Start-Process`, see [Using start](#using-start) below.</span></span>

### <a name="single-quoted-parameters"></a><span data-ttu-id="d4363-216">Parameter in einfachen Anführungszeichen</span><span class="sxs-lookup"><span data-stu-id="d4363-216">Single quoted parameters</span></span>

<span data-ttu-id="d4363-217">In diesem Beispiel werden die `wt`-Parameter in einfache Anführungszeichen (`'`) eingeschlossen.</span><span class="sxs-lookup"><span data-stu-id="d4363-217">In this example, the `wt` parameters are wrapped in single quotes (`'`).</span></span> <span data-ttu-id="d4363-218">Diese Syntax ist hilfreich, wenn keine Berechnungen durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="d4363-218">This syntax is useful if nothing is being calculated.</span></span>

```powershell
start wt 'new-tab "cmd" ; split-pane -p "Windows PowerShell" ; split-pane -H wsl.exe'
```

### <a name="escaped-quotes"></a><span data-ttu-id="d4363-219">Anführungszeichen mit Escapezeichen</span><span class="sxs-lookup"><span data-stu-id="d4363-219">Escaped quotes</span></span>

<span data-ttu-id="d4363-220">Verwenden Sie die folgende Syntax, wenn Sie einen in einer Variablen enthaltenen Wert an die `wt`-Befehlszeile übergeben:</span><span class="sxs-lookup"><span data-stu-id="d4363-220">When passing a value contained in a variable to the `wt` command line, use the following syntax:</span></span>

```powershell
$ThirdPane = "wsl.exe"
start wt "new-tab cmd ; split-pane -p `"Windows PowerShell`" ; split-pane -H $ThirdPane"
```

<span data-ttu-id="d4363-221">Beachten Sie die Verwendung von `` ` `` als Escapezeichen für die doppelten Anführungszeichen (`"`) von "Windows PowerShell" im `-p`-Parameter für den Parameter `split-pane`.</span><span class="sxs-lookup"><span data-stu-id="d4363-221">Note the usage of  `` ` `` to escape the double-quotes (`"`) around "Windows PowerShell" in the `-p` parameter to the `split-pane` parameter.</span></span>

### <a name="using-start"></a><span data-ttu-id="d4363-222">Verwenden von `start`</span><span class="sxs-lookup"><span data-stu-id="d4363-222">Using `start`</span></span>

<span data-ttu-id="d4363-223">In allen obigen Beispielen wurde explizit `start` verwendet, um das Terminal zu starten.</span><span class="sxs-lookup"><span data-stu-id="d4363-223">All the above examples explicitly used `start` to launch the terminal.</span></span>

<span data-ttu-id="d4363-224">Die folgenden Beispiele verwenden nicht `start`, um die Befehlszeile auszuführen.</span><span class="sxs-lookup"><span data-stu-id="d4363-224">The following examples do not use `start` to run the command line.</span></span> <span data-ttu-id="d4363-225">Stattdessen gibt es zwei weitere Methoden, um Escapezeichen in der Befehlszeile zu verwenden:</span><span class="sxs-lookup"><span data-stu-id="d4363-225">Instead, there are two other methods of escaping the command line:</span></span>

* <span data-ttu-id="d4363-226">Die Semikolons werden nur mit Escapezeichen versehen, damit sie von `PowerShell` ignoriert und direkt an `wt` weitergegeben werden.</span><span class="sxs-lookup"><span data-stu-id="d4363-226">Only escaping the semicolons so that `PowerShell` will ignore them and pass them straight to `wt`.</span></span>
* <span data-ttu-id="d4363-227">Wenn Sie `--%` verwenden, behandelt PowerShell den Rest der Befehlszeile als Argumente für die Anwendung.</span><span class="sxs-lookup"><span data-stu-id="d4363-227">Using `--%`, so PowerShell will treat the rest of the command line as arguments to the application.</span></span>

```powershell
wt new-tab "cmd" `; split-pane -p "Windows PowerShell" `; split-pane -H wsl.exe
```

```powershell
wt --% new-tab cmd ; split-pane -p "Windows PowerShell" ; split-pane -H wsl.exe
```

<span data-ttu-id="d4363-228">In beiden Beispielen erstellt das neu erstellte Windows Terminal-Fenster das Fenster durch die ordnungsgemäße Analyse aller angegebenen Befehlszeilenargumente.</span><span class="sxs-lookup"><span data-stu-id="d4363-228">In both of these examples, the newly created Windows Terminal window will create the window by correctly parsing all the provided command-line arguments.</span></span>

<span data-ttu-id="d4363-229">Diese Methoden werden derzeit jedoch _nicht_ empfohlen, da PowerShell auf das Schließen des neu erstellten Terminalfensters wartet, bevor die Kontrolle an PowerShell zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="d4363-229">However, these methods are _not_ recommended currently, as PowerShell will wait for the newly-created terminal window to be closed before returning control to PowerShell.</span></span> <span data-ttu-id="d4363-230">Standardmäßig wartet PowerShell immer auf das Schließen von Windows Store-Anwendungen (wie Windows Terminal), bevor es zur Eingabeaufforderung zurückkehrt.</span><span class="sxs-lookup"><span data-stu-id="d4363-230">By default, PowerShell will always wait for Windows Store applications (like Windows Terminal) to close before returning to the prompt.</span></span> <span data-ttu-id="d4363-231">Beachten Sie, dass dies nicht dem Verhalten der Eingabeaufforderung entspricht, bei dem sofort zur Eingabeaufforderung zurückkehrt wird.</span><span class="sxs-lookup"><span data-stu-id="d4363-231">Note that this is different than the behavior of Command Prompt, which will return to the prompt immediately.</span></span>
