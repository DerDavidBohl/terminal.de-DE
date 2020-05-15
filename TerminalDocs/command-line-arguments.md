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
# <a name="using-command-line-arguments-for-windows-terminal"></a>Verwenden von Befehlszeilenargumenten für Windows Terminal

Sie können `wt.exe` verwenden, um eine neue Instanz von Windows Terminal über die Befehlszeile zu öffnen. Sie können stattdessen auch den Ausführungsalias `wt` verwenden.

> [!NOTE]
> Wenn Sie Windows Terminal aus dem Quellcode auf [GitHub](https://github.com/microsoft/terminal) erstellt haben, können Sie diesen Build mit `wtd.exe` oder `wtd` öffnen.

![Windows Terminal-Befehlszeilenargument für geteilte Bereiche](./images/terminal-command-args.gif)

## <a name="command-line-syntax"></a>Befehlszeilensyntax

Die `wt`-Befehlszeile akzeptiert zwei Arten von Werten: **Optionen** und **Befehle**. **Optionen** sind eine Liste von Flags und anderen Parametern, die das Verhalten der `wt`-Befehlszeile als Ganzes steuern können. **Befehle** geben die Aktion oder eine durch Semikolon getrennte Liste von Aktionen an, die ausgeführt werden sollen. Wenn Sie keinen Befehl angeben, wird `new-tab` standardmäßig als Befehl angenommen.

```bash
wt [options] [command ; ]
```

Geben Sie Folgendes ein, um eine Hilfemeldung mit den verfügbaren Befehlszeilenargumenten anzuzeigen: `wt -h`, `wt --help`, `wt -?` oder `wt /?`.

## <a name="options-and-commands"></a>Optionen und Befehle

Im Folgenden finden Sie die vollständige Liste der unterstützten Befehle und Optionen für die `wt`-Befehlszeile.

| Option | Beschreibung |
| ------ | ----------- |
| `--help`, `-h`, `-?`, `/?` | Zeigt die Hilfemeldung an. |

| Befehl | Parameter | Beschreibung |
| ------- | ---------- | ----------- |
| `new-tab` | `--profile, -p profile-name`, `--startingDirectory, -d starting-directory`, `commandline` | Erstellt eine neue Registerkarte. |
| `split-pane` | `-H, --horizontal`, `-V, --vertical`, `--profile, -p profile-name`, `--startingDirectory, -d starting-directory`, `commandline` | Unterteilt einen neuen Bereich. |
| `focus-tab` | `--target, -t tab-index` | Setzt den Fokus auf eine bestimmte Registerkarte. |

## <a name="command-line-argument-examples"></a>Beispiele für Befehlszeilenargumente

Die Befehle können leicht variieren, je nachdem, welche Befehlszeile Sie verwenden.

### <a name="open-a-new-profile-instance"></a>Eine neue Profilinstanz öffnen

Geben Sie Folgendes ein, um eine neue Terminalinstanz zu öffnen. In diesem Fall öffnet der Befehl das Profil mit dem Namen „Ubuntu-18.04“:

<!-- Start tab selectors. -->
#### <a name="command-prompt"></a>[Eingabeaufforderung](#tab/windows)

```bash
wt -p "Ubuntu-18.04"
```

#### <a name="powershell"></a>[PowerShell](#tab/powershell)

```powershell
wt -p "Ubuntu-18.04"
```

#### <a name="linux"></a>[Linux](#tab/linux)

```bash
cmd.exe /c "wt.exe" -p "Ubuntu-18.04"
```

Ausführungsaliase funktionieren nicht in WSL-Distributionen. Wenn Sie „wt.exe“ über eine WSL-Befehlszeile verwenden möchten, können Sie es direkt über CMD erstellen, indem Sie `cmd.exe` ausführen. Die Option `/c` weist CMD an, den Vorgang nach der Ausführung zu beenden.

---
<!-- End tab selectors.  -->

 Das `-p`-Flag wird verwendet, um das zu öffnende Windows Terminal-Profil anzugeben. Ersetzen Sie „Ubuntu-18.04“ durch den Namen eines beliebigen Terminalprofils, das Sie installiert haben. Dadurch wird immer ein neues Fenster geöffnet. Windows Terminal ist noch nicht in der Lage, neue Registerkarten oder Bereiche in einer vorhandenen Instanz zu öffnen.

### <a name="target-a-directory"></a>Auswählen eines Zielverzeichnisses

Geben Sie Folgendes ein, um den Ordner anzugeben, der als Startverzeichnis für die Konsole verwendet werden soll (in diesem Fall das Verzeichnis „d:\“):

<!-- Start tab selectors. -->
#### <a name="command-prompt"></a>[Eingabeaufforderung](#tab/windows)

```bash
wt -d d:\
```

#### <a name="powershell"></a>[PowerShell](#tab/powershell)

```powershell
wt -d d:\
```

#### <a name="linux"></a>[Linux](#tab/linux)

```bash
cmd.exe /c "wt.exe" -d d:\
```

Ausführungsaliase funktionieren nicht in WSL-Distributionen. Wenn Sie „wt.exe“ über eine WSL-Befehlszeile verwenden möchten, können Sie es direkt über CMD erstellen, indem Sie `cmd.exe` ausführen. Die Option `/c` weist CMD an, den Vorgang nach der Ausführung zu beenden.

---
<!-- End tab selectors.  -->

### <a name="multiple-tabs"></a>Mehrere Registerkarten

Geben Sie Folgendes ein, um eine neue Terminalinstanz mit mehreren Registerkarten zu öffnen:

<!-- Start tab selectors. -->
#### <a name="command-prompt"></a>[Eingabeaufforderung](#tab/windows)

```bash
wt ; ;
```

#### <a name="powershell"></a>[PowerShell](#tab/powershell)

```powershell
wt `; `;
```

PowerShell verwendet ein Semikolon (;), um Anweisungen zu trennen. Wenn Sie ein Semikolon (;) als Befehlstrennzeichen für wt-Befehlszeilenargumente interpretieren möchten, müssen Sie Hochkommas als Escapezeichen für Semikolons verwenden. PowerShell verfügt auch über den Operator zum Beenden der Analyse (--%), der das Programm anweist, das Interpretieren im Anschluss an den Operator einzustellen und die Zeichen einfach unverändert weiterzugeben.

#### <a name="linux"></a>[Linux](#tab/linux)

```bash
cmd.exe /c "wt.exe" \; \;
```

Ausführungsaliase funktionieren nicht in WSL-Distributionen. Wenn Sie „wt.exe“ über eine WSL-Befehlszeile verwenden möchten, können Sie es direkt über CMD erstellen, indem Sie `cmd.exe` ausführen. Die Option `/c` weist CMD an, den Vorgang nach der Ausführung zu beenden.

---
<!-- End tab selectors.  -->

Geben Sie zum Öffnen einer neuen Terminalinstanz mit mehreren Registerkarten, in diesem Fall ein Eingabeaufforderungsprofil und ein PowerShell-Profil, Folgendes ein:

<!-- Start tab selectors. -->
#### <a name="command-prompt"></a>[Eingabeaufforderung](#tab/windows)

```bash
wt -p "Command Prompt" ; new-tab -p "Windows PowerShell"
```

#### <a name="powershell"></a>[PowerShell](#tab/powershell)

```powershell
wt -p "Command Prompt" `; new-tab -p "Windows PowerShell"
```

PowerShell verwendet ein Semikolon (;), um Anweisungen zu trennen. Wenn Sie ein Semikolon (;) als Befehlstrennzeichen für wt-Befehlszeilenargumente interpretieren möchten, müssen Sie Hochkommas als Escapezeichen für Semikolons verwenden. PowerShell verfügt auch über den Operator zum Beenden der Analyse (--%), der das Programm anweist, das Interpretieren im Anschluss an den Operator einzustellen und die Zeichen einfach unverändert weiterzugeben.

#### <a name="linux"></a>[Linux](#tab/linux)

```bash
cmd.exe /c "wt.exe" -p "Command Prompt" \; new-tab -p "Windows Powershell"
```

Ausführungsaliase funktionieren nicht in WSL-Distributionen. Wenn Sie „wt.exe“ über eine WSL-Befehlszeile verwenden möchten, können Sie es direkt über CMD erstellen, indem Sie `cmd.exe` ausführen. Die Option `/c` weist CMD an, nach der Ausführung zu beenden, und „`\;` Schrägstrich + Semikolon“ trennt Befehle.

---
<!-- End tab selectors.  -->

### <a name="multiple-panes"></a>Mehrere Bereiche

Geben Sie Folgendes ein, um eine neue Terminalinstanz mit einer Registerkarte zu öffnen, die drei Bereiche enthält, in denen ein Eingabeaufforderungsprofil, ein PowerShell-Profil und Ihr Standardprofil mit einer WSL-Befehlszeile ausgeführt wird:

<!-- Start tab selectors. -->
#### <a name="command-prompt"></a>[Eingabeaufforderung](#tab/windows)

```bash
wt -p "Command Prompt" ; split-pane -p "Windows PowerShell" ; split-pane -H wsl.exe
```

#### <a name="powershell"></a>[PowerShell](#tab/powershell)

```powershell
wt -p "Command Prompt" `; split-pane -p "Windows PowerShell" `; split-pane -H wsl.exe
```

PowerShell verwendet ein Semikolon (;), um Anweisungen zu trennen. Wenn Sie ein Semikolon (;) als Befehlstrennzeichen für wt-Befehlszeilenargumente interpretieren möchten, müssen Sie Hochkommas als Escapezeichen für Semikolons verwenden. PowerShell verfügt auch über den Operator zum Beenden der Analyse (--%), der das Programm anweist, das Interpretieren im Anschluss an den Operator einzustellen und die Zeichen einfach unverändert weiterzugeben.

#### <a name="linux"></a>[Linux](#tab/linux)

```bash
cmd.exe /c "wt.exe" -p "Command Prompt" \; split-pane -p "Windows PowerShell" \; split-pane -H wsl.exe
```

Ausführungsaliase funktionieren nicht in WSL-Distributionen. Wenn Sie „wt.exe“ über eine WSL-Befehlszeile verwenden möchten, können Sie es direkt über CMD erstellen, indem Sie `cmd.exe` ausführen. Die Option `/c` weist CMD an, nach der Ausführung zu beenden, und „`\;` Schrägstrich + Semikolon“ trennt Befehle.

---
<!-- End tab selectors.  -->

Das Flag `-H` (oder `--horizontal`) gibt an, dass die Bereiche horizontal geteilt werden sollen. Das Flag `-V` (oder `--vertical`) gibt an, dass die Bereiche vertikal geteilt werden sollen.

### <a name="tab-focus"></a>Registerkartenfokus

Verwenden Sie das Flag `-t` (oder `--target`) zusammen mit der Indexnummer der Registerkarte, um eine neue Terminalinstanz mit Fokus auf eine bestimmte Registerkarte zu öffnen. Geben Sie Folgendes ein, um Ihr Standardprofil auf der ersten Registerkarte und das auf der zweiten Registerkarte fokussierte Profil „Ubuntu-18.04“ (`-t 1`) zu öffnen:

<!-- Start tab selectors. -->
#### <a name="command-prompt"></a>[Eingabeaufforderung](#tab/windows)

```bash
wt ; new-tab -p "Ubuntu-18.04" ; focus-tab -t 1
```

#### <a name="powershell"></a>[PowerShell](#tab/powershell)

```powershell
wt `; new-tab -p "Ubuntu-18.04" `; focus-tab -t 1
```

#### <a name="linux"></a>[Linux](#tab/linux)

```bash
cmd.exe /c "wt.exe" \; new-tab -p "Ubuntu-18.04" \; focus-tab -t 1
```

Ausführungsaliase funktionieren nicht in WSL-Distributionen. Wenn Sie „wt.exe“ über eine WSL-Befehlszeile verwenden möchten, können Sie es direkt über CMD erstellen, indem Sie `cmd.exe` ausführen. Die Option `/c` weist CMD an, nach der Ausführung zu beenden, und „`\;` Schrägstrich + Semikolon“ trennt Befehle.

---
<!-- End tab selectors.  -->

## <a name="examples-of-multiple-commands-from-powershell"></a>Beispiele für mehrere Befehle von PowerShell

Windows Terminal verwendet das Semikolon (`;`) als Trennzeichen für Befehle in der `wt`-Befehlszeile. Leider verwendet auch PowerShell `;` als Befehlstrennzeichen. Um dieses Problem zu umgehen, können Sie die folgenden Tricks verwenden, um mehrere `wt`-Befehle von PowerShell auszuführen. In allen folgenden Beispielen wird ein neues Terminalfenster mit drei Bereichen erstellt: Ein Bereich, in dem die Eingabeaufforderung ausgeführt wird, ein Bereich mit PowerShell und der letzte Bereich mit WSL.

In den folgenden Beispielen wird der `Start-Process`-Befehl verwendet, um `wt` auszuführen. Weitere Informationen dazu, warum das Terminal `Start-Process` verwendet, finden Sie nachfolgend unter [Verwenden von „start“](#using-start).

### <a name="single-quoted-parameters"></a>Parameter in einfachen Anführungszeichen

In diesem Beispiel werden die `wt`-Parameter in einfache Anführungszeichen (`'`) eingeschlossen. Diese Syntax ist hilfreich, wenn keine Berechnungen durchgeführt werden.

```powershell
start wt 'new-tab "cmd" ; split-pane -p "Windows PowerShell" ; split-pane -H wsl.exe'
```

### <a name="escaped-quotes"></a>Anführungszeichen mit Escapezeichen

Verwenden Sie die folgende Syntax, wenn Sie einen in einer Variablen enthaltenen Wert an die `wt`-Befehlszeile übergeben:

```powershell
$ThirdPane = "wsl.exe"
start wt "new-tab cmd ; split-pane -p `"Windows PowerShell`" ; split-pane -H $ThirdPane"
```

Beachten Sie die Verwendung von `` ` `` als Escapezeichen für die doppelten Anführungszeichen (`"`) von "Windows PowerShell" im `-p`-Parameter für den Parameter `split-pane`.

### <a name="using-start"></a>Verwenden von `start`

In allen obigen Beispielen wurde explizit `start` verwendet, um das Terminal zu starten.

Die folgenden Beispiele verwenden nicht `start`, um die Befehlszeile auszuführen. Stattdessen gibt es zwei weitere Methoden, um Escapezeichen in der Befehlszeile zu verwenden:

* Die Semikolons werden nur mit Escapezeichen versehen, damit sie von `PowerShell` ignoriert und direkt an `wt` weitergegeben werden.
* Wenn Sie `--%` verwenden, behandelt PowerShell den Rest der Befehlszeile als Argumente für die Anwendung.

```powershell
wt new-tab "cmd" `; split-pane -p "Windows PowerShell" `; split-pane -H wsl.exe
```

```powershell
wt --% new-tab cmd ; split-pane -p "Windows PowerShell" ; split-pane -H wsl.exe
```

In beiden Beispielen erstellt das neu erstellte Windows Terminal-Fenster das Fenster durch die ordnungsgemäße Analyse aller bereitgestellten Befehlszeilenargumente.

Diese Methoden werden derzeit jedoch _nicht_ empfohlen, da PowerShell auf das Schließen des neu erstellten Terminalfensters wartet, bevor die Kontrolle an PowerShell zurückgegeben wird. Standardmäßig wartet PowerShell immer auf das Schließen von Windows Store-Anwendungen (wie Windows Terminal), bevor es zur Eingabeaufforderung zurückkehrt. Beachten Sie, dass dies nicht dem Verhalten der Eingabeaufforderung entspricht, bei dem sofort zur Eingabeaufforderung zurückkehrt wird.
