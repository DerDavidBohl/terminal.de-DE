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
# <a name="tutorial-ssh-in-windows-terminal"></a>Tutorial: SSH in Windows Terminal

Windows 10 verfügt über einen integrierten SSH-Client, den Sie in Windows Terminal verwenden können.

In diesem Tutorial erfahren Sie, wie Sie ein Profil in Windows Terminal einrichten, das SSH verwendet.

## <a name="create-a-profile"></a>Erstellen eines Profils

Sie können eine SSH-Sitzung über die Eingabeaufforderung starten, indem Sie `ssh user@machine` ausführen. Sie werden dann aufgefordert, Ihr Kennwort einzugeben. Sie können ein Windows Terminal-Profil erstellen, das dies beim Start erledigt, indem Sie die Einstellung `commandline` zu einem Profil in Ihrer Datei „settings.json“ hinzufügen.

```js
"commandline": "ssh cinnamon@roll"
```

## <a name="specify-starting-directory"></a>Startverzeichnis angeben

Zum Angeben des Startverzeichnisses für eine von Windows Terminal aufgerufene SSH-Sitzung können Sie den folgenden Befehl verwenden:

```bash
"commandline": "ssh -t bob@foo \"cd /data/bob && exec bash -l\""
```

Das `-t`-Flag erzwingt die Pseudo-Terminalzuordnung. Sie kann verwendet werden, um beliebige bildschirmbasierte Programme auf einem Remotecomputer auszuführen, z. B. bei der Implementierung von Menüdiensten. Sie müssen doppelte Anführungszeichen mit Escapezeichen verwenden, da Ableitungen aus der Bourne-Shell für eine Zeichenfolge in einzelnen Anführungszeichen keine zusätzliche Analyse durchführen.

Weitere Informationen finden Sie unter:

* [GH-Problem: Wie wird das Startverzeichnis für eine SSH-Sitzung angegeben?](https://github.com/MicrosoftDocs/terminal/issues/25)
* [StackOverflow: Wie kann ich per SSH direkt zu einem bestimmten Verzeichnis wechseln?](https://stackoverflow.com/questions/626533/how-can-i-ssh-directly-to-a-particular-directory)

## <a name="resources"></a>Ressourcen

* [Aktivieren und Verwenden der neuen integrierten SSH-Befehle in Windows 10](https://www.howtogeek.com/336775/how-to-enable-and-use-windows-10s-built-in-ssh-commands/)
