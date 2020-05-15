---
title: 'Windows Terminal: Cascadia Code'
description: Erfahren Sie mehr über die verschiedenen Cascadia Code-Schriftarten und deren Verwendung in Windows Terminal.
author: cinnamon-msft
ms.author: cinnamon
ms.date: 05/19/2020
ms.topic: overview
ms.service: terminal
ms.openlocfilehash: e9af1ea8445514534c64410fe494d35186d028b5
ms.sourcegitcommit: bb5b7fd7db4b81e0d44e060989dc16b6775c802a
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/15/2020
ms.locfileid: "83415855"
---
# <a name="cascadia-code"></a>Cascadia Code

Cascadia Code ist eine neue Festbreitenschriftart von Microsoft, die eine neue Erfahrung für Befehlszeilenanwendungen und Text-Editoren bietet. Cascadia Code wurde zusammen mit Windows Terminal entwickelt. Diese Schriftart wird vor allem für die Verwendung mit Terminalanwendungen und Text-Editoren wie Visual Studio und Visual Studio Code empfohlen.

## <a name="cascadia-code-versions"></a>Cascadia Code-Versionen

Es sind mehrere Versionen von Cascadia Code verfügbar, die Ligaturen und Glyphen enthalten. Alle Versionen von Cascadia Code können von der GitHub-Seite [Cascadia Code](https://github.com/microsoft/cascadia-code/releases) heruntergeladen werden. Windows Terminal enthält Cascadia Code und Cascadia Mono in seinem Paket und verwendet standardmäßig Cascadia Mono.

| Schriftartname | Enthält Ligaturen | Enthält Powerline-Glyphen |
| --------- | ------------------ | ------------------------- |
| Cascadia Code | Ja | Nein |
| Cascadia Mono | Nein  | Nein |
| Cascadia Code PL | Ja | Ja |
| Cascadia Mono PL | Nein | Ja |

## <a name="powerline-and-programming-ligatures"></a>Powerline und Programmierligaturen

Powerline ist ein gängiges Befehlszeilen-Plug-In, mit dem Sie zusätzliche Informationen in Ihrer Eingabeaufforderung anzeigen können. Es verwendet einige zusätzliche Glyphen, um diese Informationen richtig darzustellen. Weitere Informationen zum Einrichten von Powerline für die Eingabeaufforderung finden Sie auf der Seite [Powerline in Windows Terminal](./tutorials/powerline-setup.md).

Programmierligaturen sind Glyphen, die durch Kombinieren von Zeichen erstellt werden. Sie müssen beim Schreiben von Code nützlich sein. Die „Code“-Varianten enthalten Ligaturen, während die „Mono“-Varianten sie ausschließen.

![Cascadia Code: Programmierligaturen](./images/programming-ligatures.gif)

## <a name="contributing-to-cascadia-code"></a>Beitragen zu Cascadia Code

Cascadia Code ist unter der [SIL Open Font-Lizenz](https://scripts.sil.org/cms/scripts/page.php?site_id=nrsi&id=OFL) auf [GitHub](https://github.com/microsoft/cascadia-code) lizenziert.
