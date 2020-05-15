---
title: 'Windows Terminal: Dynamische Profile'
description: Erfahren Sie mehr über dynamische Profile in Windows Terminal.
author: cinnamon-msft
ms.author: cinnamon
ms.date: 05/19/2020
ms.topic: concept
ms.service: terminal
ms.openlocfilehash: 9c54dc2182584873d9d0c1358083d5142d07ef48
ms.sourcegitcommit: bb5b7fd7db4b81e0d44e060989dc16b6775c802a
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/15/2020
ms.locfileid: "83416125"
---
# <a name="dynamic-profiles-in-windows-terminal"></a>Dynamische Profile in Windows Terminal

Windows Terminal erstellt automatisch WSL- (Windows-Subsystem für Linux) und PowerShell-Profile für Sie, wenn Sie diese Shells auf Ihrem Computer installiert haben. Dies erleichtert es Ihnen, sämtliche Shells in das Terminal einzubinden, ohne dass Sie die ausführbaren Dateien suchen müssen. Diese Profile werden mit der `source`-Eigenschaft generiert, die dem Terminal mitteilt, wo die richtige ausführbare Datei zu finden ist.

Bei der Installation des Terminals wird PowerShell als Standardprofil festgelegt. Informationen zum Ändern Ihres Standardprofils finden Sie auf der Seite [Globale Einstellungen](./customize-settings/global-settings.md).

![Windows Terminal: Dynamische Profile](./images/dynamic-profiles.png)
_Konfiguration: [Helles Design](./custom-terminal-gallery/frosted-glass-theme.md)_

## <a name="installing-a-new-shell-after-installing-windows-terminal"></a>Installieren einer neuen Shell nach der Installation von Windows Terminal

Unabhängig davon, ob eine neue Shell vor oder nach Ihrer Terminalinstallation installiert wird, erstellt das Terminal ein neues Profil für die neu installierte Shell.

## <a name="hide-a-profile"></a>Ausblenden von Profilen

Um ein Profil aus dem Dropdownmenü Ihres Terminals auszublenden, fügen Sie dem Profilobjekt in Ihrer Datei „settings.json“ die Eigenschaft `hidden` hinzu, und legen Sie sie auf `true` fest.

```json
"hidden": true
```

Wenn Sie ein dynamisch erstelltes Profil löschen, generiert das Terminal das Profil automatisch neu und ersetzt es in der Datei „settings.json“.

## <a name="prevent-a-profile-from-being-generated"></a>Verhindern der Profilgenerierung

Wenn Sie verhindern möchten, dass ein dynamisches Profil generiert wird, können Sie den Profilgenerator zum `disabledProfileSources`-Array in Ihren globalen Einstellungen hinzufügen. Weitere Informationen zu dieser Einstellung finden Sie auf der Seite [Globale Einstellungen](./customize-settings/global-settings.md#disable-dynamic-profiles).

```json
"disabledProfileSources": ["Windows.Terminal.Wsl", "Windows.Terminal.Azure", "Windows.Terminal.PowershellCore"]
```
