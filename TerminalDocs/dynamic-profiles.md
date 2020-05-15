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
# <a name="dynamic-profiles-in-windows-terminal"></a><span data-ttu-id="8e224-103">Dynamische Profile in Windows Terminal</span><span class="sxs-lookup"><span data-stu-id="8e224-103">Dynamic profiles in Windows Terminal</span></span>

<span data-ttu-id="8e224-104">Windows Terminal erstellt automatisch WSL- (Windows-Subsystem für Linux) und PowerShell-Profile für Sie, wenn Sie diese Shells auf Ihrem Computer installiert haben.</span><span class="sxs-lookup"><span data-stu-id="8e224-104">The Windows Terminal will automatically create Windows Subsystem for Linux (WSL) and PowerShell profiles for you if you have these shells installed on your machine.</span></span> <span data-ttu-id="8e224-105">Dies erleichtert es Ihnen, sämtliche Shells in das Terminal einzubinden, ohne dass Sie die ausführbaren Dateien suchen müssen.</span><span class="sxs-lookup"><span data-stu-id="8e224-105">This makes it easier for you to have all of your shells included in the terminal without having to locate their executable files.</span></span> <span data-ttu-id="8e224-106">Diese Profile werden mit der `source`-Eigenschaft generiert, die dem Terminal mitteilt, wo die richtige ausführbare Datei zu finden ist.</span><span class="sxs-lookup"><span data-stu-id="8e224-106">These profiles are generated with the `source` property, which tells the terminal where to locate the proper executable.</span></span>

<span data-ttu-id="8e224-107">Bei der Installation des Terminals wird PowerShell als Standardprofil festgelegt.</span><span class="sxs-lookup"><span data-stu-id="8e224-107">Upon installing the terminal, it will set PowerShell as your default profile.</span></span> <span data-ttu-id="8e224-108">Informationen zum Ändern Ihres Standardprofils finden Sie auf der Seite [Globale Einstellungen](./customize-settings/global-settings.md).</span><span class="sxs-lookup"><span data-stu-id="8e224-108">To learn how to change your default profile, visit the [Global settings page](./customize-settings/global-settings.md).</span></span>

<span data-ttu-id="8e224-109">![Windows Terminal: Dynamische Profile](./images/dynamic-profiles.png)
_Konfiguration: [Helles Design](./custom-terminal-gallery/frosted-glass-theme.md)_</span><span class="sxs-lookup"><span data-stu-id="8e224-109">![Windows Terminal dynamic profiles](./images/dynamic-profiles.png)
_Configuration: [Light Theme](./custom-terminal-gallery/frosted-glass-theme.md)_</span></span>

## <a name="installing-a-new-shell-after-installing-windows-terminal"></a><span data-ttu-id="8e224-110">Installieren einer neuen Shell nach der Installation von Windows Terminal</span><span class="sxs-lookup"><span data-stu-id="8e224-110">Installing a new shell after installing Windows Terminal</span></span>

<span data-ttu-id="8e224-111">Unabhängig davon, ob eine neue Shell vor oder nach Ihrer Terminalinstallation installiert wird, erstellt das Terminal ein neues Profil für die neu installierte Shell.</span><span class="sxs-lookup"><span data-stu-id="8e224-111">Regardless of whether a new shell is installed before or after your terminal installation, the terminal will create a new profile for the newly installed shell.</span></span>

## <a name="hide-a-profile"></a><span data-ttu-id="8e224-112">Ausblenden von Profilen</span><span class="sxs-lookup"><span data-stu-id="8e224-112">Hide a profile</span></span>

<span data-ttu-id="8e224-113">Um ein Profil aus dem Dropdownmenü Ihres Terminals auszublenden, fügen Sie dem Profilobjekt in Ihrer Datei „settings.json“ die Eigenschaft `hidden` hinzu, und legen Sie sie auf `true` fest.</span><span class="sxs-lookup"><span data-stu-id="8e224-113">To hide a profile from your terminal dropdown menu, add the `hidden` property to the profile object in your settings.json file and set it to `true`.</span></span>

```json
"hidden": true
```

<span data-ttu-id="8e224-114">Wenn Sie ein dynamisch erstelltes Profil löschen, generiert das Terminal das Profil automatisch neu und ersetzt es in der Datei „settings.json“.</span><span class="sxs-lookup"><span data-stu-id="8e224-114">If you delete a dynamically-created profile, the terminal will automatically regenerate the profile and replace it in your settings.json file.</span></span>

## <a name="prevent-a-profile-from-being-generated"></a><span data-ttu-id="8e224-115">Verhindern der Profilgenerierung</span><span class="sxs-lookup"><span data-stu-id="8e224-115">Prevent a profile from being generated</span></span>

<span data-ttu-id="8e224-116">Wenn Sie verhindern möchten, dass ein dynamisches Profil generiert wird, können Sie den Profilgenerator zum `disabledProfileSources`-Array in Ihren globalen Einstellungen hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="8e224-116">To prevent a dynamic profile from being generated, you can add the profile generator to the `disabledProfileSources` array in your global settings.</span></span> <span data-ttu-id="8e224-117">Weitere Informationen zu dieser Einstellung finden Sie auf der Seite [Globale Einstellungen](./customize-settings/global-settings.md#disable-dynamic-profiles).</span><span class="sxs-lookup"><span data-stu-id="8e224-117">More information on this setting can be found on the [Global settings page](./customize-settings/global-settings.md#disable-dynamic-profiles).</span></span>

```json
"disabledProfileSources": ["Windows.Terminal.Wsl", "Windows.Terminal.Azure", "Windows.Terminal.PowershellCore"]
```
