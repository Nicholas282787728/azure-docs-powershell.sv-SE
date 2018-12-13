---
title: Installera Azure PowerShell ”Az” med PowerShellGet
description: Så här installerar du Azure PowerShell med PowerShellGet på Windows, macOS och Linux.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 11/26/2018
ms.openlocfilehash: 3d52b18750341f220dc8e10d6bf89796457c5a10
ms.sourcegitcommit: 087c588169786c005a3c177624fb3ac6c8870125
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/13/2018
ms.locfileid: "53217005"
---
# <a name="install-the-azure-powershell-az-module"></a>Installera modulen Azure PowerShell ”Az”

Den här artikeln beskriver hur du installerar Azure PowerShell-modulerna med hjälp av PowerShellGet. De här instruktionerna fungerar för Windows-, macOS- och Linux-plattformar. För förhandsversionen av Az stöds inga andra installationsmetoder. 

## <a name="requirements"></a>Krav

Azure PowerShell fungerar med PowerShell 5.x på Windows eller PowerShell 6.x på valfri plattform. Kör följande kommando för att kontrollera vilken version av PowerShell som körs på din dator:

```powershell-interactive
$PSVersionTable.PSVersion
```

Om du har en inaktuell version eller behöver installera PowerShell kan du läsa [Installation av olika versioner av PowerShell](https://docs.microsoft.com/en-us/powershell/scripting/setup/installing-powershell?view=powershell-6). Installationsinformation för din plattform är länkad från den sidan.

## <a name="install-the-azure-powershell-module"></a>Installera Azure PowerShell-modulen

> [!IMPORTANT]
>
> Du kan ha både modulen `AzureRM` och modulen `Az` installerade samtidigt. Om du har båda modulerna installerade __ska du inte aktivera__ -alias.
> Om du aktiverar alias skapas konflikter mellan `AzureRM`-cmdletar och `Az`-kommandoalias och detta kan orsaka oväntat beteende.
> Vi rekommenderar att du avinstallerar `AzureRM` innan du installerar modulen `Az`. Du kan alltid avinstallera `AzureRM` eller aktivera alias när som helst. Anvisningar om hur du avinstallerar finns i [Avinstallera Azure PowerShell-modulen (AzureRM)](uninstall-azurerm-ps.md). 

Om du vill installera moduler med globalt omfång behöver du ha utökade privilegier för att installera moduler från PowerShell-galleriet. Du installerar Azure PowerShell genom att köra följande kommando i en upphöjd session (”Kör som administratör” på Windows eller med superanvändarprivilegier på macOS eller Linux):

```powershell-interactive
Install-Module -Name Az -AllowClobber
```

Om du inte har åtkomst till administratörsprivilegier kan du installera för den aktuella användaren genom att lägga till argumentet `-Scope`.

```powershell-interactive
Install-Module -Name Az -AllowClobber -Scope CurrentUser
```

Som standard konfigureras inte PowerShell-galleriet som en betrodd lagringsplats för PowerShellGet. Första gången du använder PSGallery visas följande meddelande:

```output
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the Set-PSRepository cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"):
```

Svara `Yes` eller `Yes to All` för att fortsätta med installationen.

Modulen `Az` är en sammanslagen modul för Azure PowerShell-cmdletar. När du installerar den laddar den ned alla tillgängliga Azure Resource Manager-moduler och gör dess cmdletar tillgängliga för användning.

## <a name="sign-in"></a>Logga in

Börja arbeta med Azure PowerShell genom att logga in med dina autentiseringsuppgifter för Azure.

```powershell-interactive
# Connect to Azure with a browser sign in token
Connect-AzAccount
```

> [!NOTE]
>
> Om du har inaktiverat modulen för automatisk inläsning måste du importera modulen manuellt med `Import-Module Az`. Det kan ta några sekunder. Det beror på hur modulen är strukturerad.

Du måste upprepa de här stegen för varje ny PowerShell-session du startar. Information om hur du sparar Azure-inloggningen mellan olika PowerShell-sessioner hittar du i artikeln om att [spara autentiseringsuppgifter för användare mellan olika PowerShell-sessioner](context-persistence.md).

## <a name="update-the-azure-powershell-module"></a>Uppdatera Azure PowerShell-modulen

Du kan uppdatera din Azure PowerShell-installation genom att köra [Update-Module](/powershell/module/powershellget/update-module). Det här kommandot avinstallerar __inte__ tidigare versioner.

```powershell-interactive
Update-Module -Name Az
```

Se [Avinstallera Azure PowerShell-modulen](uninstall-azurerm-ps.md) om du vill ta bort äldre versioner av Azure PowerShell från ditt system.

## <a name="use-multiple-versions-of-azure-powershell"></a>Använd flera versioner av Azure PowerShell

Det är möjligt att installera fler än en version av Azure PowerShell. Använd följande kommando för att kontrollera om du har flera versioner av Azure PowerShell installerade:

```powershell-interactive
Get-Module -Name Az -List | select Name,Version
```

Se [Avinstallera Azure PowerShell-modulen](uninstall-azurerm-ps.md) om du vill ta bort en version av Azure PowerShell.

Du kan läsa in en specifik version av `Az`-modulen med hjälp av argumentet `-RequiredVersion` med `Install-Module` eller `Import-Module`:

```powershell-interactive
Install-Module -Name Az -RequiredVersion 0.4.0
Import-Module -Name Az -RequiredVersion 0.4.0
```

Om du har flera versioner av modulen installerade läses den senaste versionen in som standard.

## <a name="provide-feedback"></a>Ge feedback

Om du upptäcker en bugg när du använder Azure PowerShell kan du [öppna ett ärende på GitHub](https://github.com/Azure/azure-powershell/issues).
Om du vill ge feedback från kommandoraden använder du cmdleten [Send-Feedback](/powershell/module/az.profile/send-feedback).

## <a name="next-steps"></a>Nästa steg

Läs informationen i [Komma igång med Azure PowerShell](get-started-azureps.md) för att komma igång med Azure PowerShell och lära dig mer om modulerna och dess funktioner.
