---
title: Windows Terminal-Installation
description: In diesem Schnellstart erfahren Sie, wie Sie Windows Terminal installieren und ausführen.
author: cinnamon-msft
ms.author: cinnamon
ms.date: 05/19/2020
ms.topic: quickstart
ms.service: terminal
ms.localizationpriority: high
ms.openlocfilehash: e804f94643835b2286e1d7aa11c84334c4223889
ms.sourcegitcommit: d8e23557224bc50a82a36dc80ac68b9d11dfdde9
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2020
ms.locfileid: "84720106"
---
# <a name="install-and-set-up-windows-terminal"></a>Installieren und Einrichten von Windows Terminal

## <a name="installation"></a>Installation

Sie können Windows Terminal über den [Microsoft Store](https://aka.ms/terminal) installieren.

Wenn Sie keinen Zugriff auf den Microsoft Store haben, werden die Builds auf der Seite [GitHub-Versionen](https://github.com/microsoft/terminal/releases) veröffentlicht. Wenn Sie über GitHub installieren, wird das Terminal nicht automatisch mit neuen Versionen aktualisiert.

## <a name="first-run"></a>Erstausführung

Wenn Sie das Terminal nach der Installation öffnen, wird es mit PowerShell als Standardprofil auf der geöffneten Registerkarte gestartet.

![Erste Ausführung von Windows Terminal](./images/first-run.png)

### <a name="dynamic-profiles"></a>Dynamische Profile

Das Terminal erstellt automatisch Profile für Sie, wenn Sie WSL-Distributionen oder mehrere Versionen von PowerShell installiert haben. Weitere Informationen zu dynamischen Profilen finden Sie auf der Seite [Dynamische Profile](./dynamic-profiles.md).

## <a name="open-a-new-tab"></a>Öffnen einer neuen Registerkarte

Sie können eine neue Registerkarte des Standardprofils öffnen, indem Sie <kbd>STRG+UMSCHALT+T</kbd> drücken oder die Schaltfläche „+“ (Plus) auswählen. Wählen Sie zum Öffnen eines anderen Profils den „˅“ (Pfeil) neben der Schaltfläche „+“ (Plus) aus, um das Dropdownmenü zu öffnen. Darüber können Sie auswählen, welches Profil geöffnet werden soll.

## <a name="open-a-new-pane"></a>Öffnen eines neuen Bereichs

Mithilfe von Bereichen können Sie mehrere Shells nebeneinander ausführen. Verwenden Sie zum Öffnen eines Bereichs <kbd>ALT+UMSCHALT+D</kbd>. Diese Tastenzuordnung öffnet einen duplizierten Bereich des Profils, das den Fokus enthält. Weitere Informationen zu Bereichen finden Sie auf der Seite [Bereiche](./panes.md).

## <a name="configuration"></a>Konfiguration

Wählen Sie zum Anpassen der Einstellungen von Windows Terminal die Option **Einstellungen** im Dropdownmenü aus. Dadurch wird die Datei `settings.json` in Ihrem standardmäßigen Text-Editor geöffnet. (Der standardmäßige Text-Editor ist in den [Windows-Einstellungen](ms-settings:defaultapps) definiert.)

Der Terminal unterstützt die Anpassung von [globalen Eigenschaften](./customize-settings/global-settings.md), die sich auf die gesamte Anwendung auswirken, [Profileigenschaften](./customize-settings/profile-settings.md), die sich auf die Einstellungen der einzelnen Profile auswirken, und [Tastenzuordnungen](./customize-settings/key-bindings.md), die es Ihnen ermöglichen, mit dem Terminal über Ihre Tastatur zu interagieren.

## <a name="command-line-arguments"></a>Befehlszeilenargumente

Mithilfe von Befehlszeilenargumenten können Sie das Terminal in einer bestimmten Konfiguration starten. Mit diesen Argumenten können Sie das Terminal mit bestimmten Registerkarten und Bereichen mit benutzerdefinierten Profileinstellungen öffnen. Weitere Informationen zu Befehlszeilenargumenten finden Sie auf der Seite [Befehlszeilenargumente](./command-line-arguments.md).

## <a name="troubleshooting"></a>Problembehandlung

Wenn Sie bei der Verwendung des Terminals auf Probleme stoßen, finden Sie weitere Informationen auf der Seite [Problembehandlung](./troubleshooting.md). Wenn Sie Fehler finden oder ein Feature anfordern möchten, können Sie den Link „Feedback“ im Menü **Info** des Terminals auswählen, um zur [GitHub-Seite](https://github.com/microsoft/terminal) zu gelangen, wo Sie ein neues Problem einreichen können.
