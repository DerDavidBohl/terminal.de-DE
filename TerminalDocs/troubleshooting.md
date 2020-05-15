---
title: 'Windows Terminal: Problembehandlung'
description: Hier erfahren Sie mehr über die Lösungen für häufige Probleme in Windows Terminal.
author: cinnamon-msft
ms.author: cinnamon
ms.date: 05/19/2020
ms.topic: overview
ms.service: terminal
ms.localizationpriority: high
ms.openlocfilehash: 29d3ce72210c30fcbf38393d733c6157670465bb
ms.sourcegitcommit: bb5b7fd7db4b81e0d44e060989dc16b6775c802a
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/15/2020
ms.locfileid: "83415875"
---
# <a name="troubleshooting-in-windows-terminal"></a>Problembehandlung in Windows Terminal

Dieser Leitfaden behandelt einige der häufigsten Fehler und Probleme, die bei der Verwendung von Windows Terminal auftreten können.

## <a name="set-your-wsl-distribution-to-start-in-the-home--directory-when-launched"></a>Legen Sie Ihre WSL-Distribution so fest, dass sie beim Start im Basisverzeichnis `~` beginnt.

Standardmäßig ist das `startingDirectory` eines Profils `%USERPROFILE%` (`C:\Users\<YourUsername>`). Dies ist ein Windows-Pfad. Für WSL empfiehlt es sich jedoch, stattdessen den WSL-Basispfad zu verwenden. `startingDirectory` akzeptiert nur einen Pfad im Windows-Format, sodass das Festlegen des Startvorgangs innerhalb einer WSL-Distribution ein Präfix erfordert.

Ab Windows 10 Version 1903 können die Dateisysteme von WSL-Distributionen mit dem Präfix `\\wsl$\` adressiert werden. Verwenden Sie für jede WSL-Distribution mit dem Namen `DistroName` `\\wsl$\DistroName` als Windows-Pfad, der auf das Stammverzeichnis des Dateisystems dieser Distribution verweist.

Die folgende Einstellung startet z. B. die „Ubuntu-18.04“-Distribution in ihrem Basisdateipfad:

```json
{
    "name": "Ubuntu-18.04",
    "commandline" : "wsl -d Ubuntu-18.04",
    "startingDirectory" : "//wsl$/Ubuntu-18.04/home/<Your Ubuntu Username>",
}
```

## <a name="setting-the-tab-title"></a>Festlegen des Registerkartentitels

Informationen zum automatischen Festlegen des Registerkartentitels durch die Shell [finden Sie im Tutorial zum Festlegen des Registerkartentitels](./tutorials/tab-title.md). Wenn Sie einen eigenen Registerkartentitel festlegen möchten, öffnen Sie die Datei „settings.json“ und folgen Sie diesen Schritten:

1. Fügen Sie im Profil für die Befehlszeile Ihrer Wahl `"suppressApplicationTitle": true` hinzu, um alle Titeländerungsereignisse zu unterdrücken, die von der Shell gesendet werden. Wenn Sie *nur* diese Einstellung zu Ihrem Profil hinzufügen, wird der Registerkartentitel auf den Namen Ihres Profils festgelegt.

2. Wenn Sie einen benutzerdefinierten Registerkartentitel wünschen, der nicht der Name Ihres Profils ist, fügen Sie `"tabTitle": "TITLE"` hinzu. Ersetzen Sie „TITLE“ durch Ihren bevorzugten Registerkartentitel.

## <a name="command-line-arguments-in-powershell"></a>Befehlszeilenargumente in PowerShell

Besuchen Sie die Seite [Befehlszeilenargumente](./command-line-arguments.md), um zu erfahren, wie Befehlszeilenargumente in PowerShell funktionieren.

## <a name="command-line-arguments-in-wsl"></a>Befehlszeilenargumente in WSL

Besuchen Sie die Seite [Befehlszeilenargumente](./command-line-arguments.md), um zu erfahren, wie Befehlszeilenargumente in WSL funktionieren.

## <a name="problem-setting-startingdirectory"></a>Problemeinstellung `startingDirectory`

Wenn das `startingDirectory` in Ihrem Profil ignoriert wird, überprüfen Sie zunächst, ob die Syntax Ihrer „settings.json“ fehlerfrei ist. `"$schema": "https://aka.ms/terminal-profiles-schema"` wird automatisch eingefügt, um Sie bei der Überprüfung dieser Syntax zu unterstützen. Einige Anwendungen, z. B. [Visual Studio Code](https://code.visualstudio.com/download), können dieses eingefügte Schema zur Überprüfung Ihrer JSON-Datei verwenden, während Sie Änderungen vornehmen.

Wenn Ihre Einstellungen richtig sind, führen Sie möglicherweise ein Startskript aus, das das Startverzeichnis Ihres Terminals separat festlegt. PowerShell verfügt z. B. über ein eigenes separates Profilkonzept. Wenn Sie dort Ihr Startverzeichnis ändern, hat es Vorrang vor der in Windows Terminal definierten Einstellung.

Wenn Sie alternativ ein Skript mit der Profileinstellung `commandline` ausführen, kann es sein, dass Sie dort den Speicherort festlegen. Ähnlich wie bei PowerShell-Profilen haben Ihre Befehle dort Vorrang vor der `startingDirectory`-Profileinstellung.

Der Zweck von `startingDirectory` ist es, eine neue Windows Terminal-Instanz im angegebenen Verzeichnis zu starten. Wenn das Terminal irgendeinen Code ausführt, der sein Verzeichnis ändert, könnte es angebracht sein, hier einen Blick drauf zu werfen.

## <a name="ctrl-does-not-increase-the-font-size"></a>STRG+= erhöht nicht den Schriftgrad

Wenn Sie ein deutsches Tastaturlayout verwenden, kann dieses Problem auftreten. <kbd>STRG+=</kbd> wird zu <kbd>STRG+UMSCHALT+0</kbd> deserialisiert, wenn Ihr Haupttastaturlayout auf „Deutsch“ festgelegt ist. Dies ist die ordnungsgemäße Zuordnung für deutsche Tastaturen.

Noch wichtiger ist, dass die App niemals den Tastenanschlag <kbd>STRG+UMSCHALT+0</kbd> erhält. Dies liegt daran, dass <kbd>STRG+UMSCHALT+0</kbd> von Windows reserviert ist, wenn mehrere Tastaturlayouts aktiv sind.

Wenn Sie dieses Feature deaktivieren möchten, damit `Ctrl+=` richtig funktioniert, folgen Sie den Anweisungen für „Ändern der Abkürzungstasten zum Wechseln des Tastaturlayouts in Windows 10“ in diesem [Blogbeitrag](https://winaero.com/blog/change-hotkeys-switch-keyboard-layout-windows-10/).

Ändern Sie die Option „Tastaturlayout wechseln“ in „Nicht zugewiesen“ (oder deaktivieren Sie <kbd>STRG+UMSCHALT</kbd>), und wählen Sie dann **OK** sowie **Übernehmen** aus. <kbd>STRG+UMSCHALT+0</kbd> sollte jetzt als Tastenzuordnung funktionieren und wird an das Terminal weitergegeben.

Wenn Sie andererseits dieses Abkürzungstastenfeature für mehrere Eingabesprachen verwenden, können Sie [eine eigene benutzerdefinierte Tastenzuordnung](./customize-settings/key-bindings.md) in Ihrer Datei „settings.json“ konfigurieren.
