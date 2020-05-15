---
title: 'Windows Terminal: SSH'
description: In diesem Tutorial erfahren Sie, wie Sie eine SSH-Verbindung in Windows Terminal einrichten.
author: cinnamon-msft
ms.author: cinnamon
ms.date: 05/19/2020
ms.topic: tutorial
ms.service: terminal
ms.openlocfilehash: c418460cd47935ed8b8eb57ebdb89322d543a20e
ms.sourcegitcommit: bb5b7fd7db4b81e0d44e060989dc16b6775c802a
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/15/2020
ms.locfileid: "83415865"
---
# <a name="tutorial-ssh-in-windows-terminal"></a>Tutorial: SSH in Windows Terminal

Windows 10 verfügt über einen integrierten SSH-Client, den Sie in Windows Terminal verwenden können.

In diesem Tutorial erfahren Sie, wie Sie ein Profil in Windows Terminal einrichten, das SSH verwendet.

## <a name="create-a-profile"></a>Erstellen eines Profils

Sie können eine SSH-Sitzung über die Eingabeaufforderung starten, indem Sie `ssh user@machine` ausführen. Sie werden dann aufgefordert, Ihr Kennwort einzugeben. Sie können ein Windows Terminal-Profil erstellen, das dies beim Start erledigt, indem Sie die Einstellung `commandline` zu einem Profil in Ihrer Datei „settings.json“ hinzufügen.

```js
"commandline": "ssh cinnamon@roll"
```

## <a name="resources"></a>Ressourcen

* [Aktivieren und Verwenden der neuen integrierten SSH-Befehle in Windows 10](https://www.howtogeek.com/336775/how-to-enable-and-use-windows-10s-built-in-ssh-commands/)
