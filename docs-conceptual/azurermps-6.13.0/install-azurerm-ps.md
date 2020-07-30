---
title: Installera Azure PowerShell på Windows med PowerShellGet
description: Så här installerar du Azure PowerShell med PowerShellGet
ms.devlang: powershell
ms.topic: conceptual
ms.date: 11/16/2018
ms.openlocfilehash: 2615d1efef05c892552d7ccbea6fcff37f871039
ms.sourcegitcommit: c19bf5a96a82a56e2b1fa9ab5e106690f850cedf
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/27/2020
ms.locfileid: "87177466"
---
# <a name="install-azure-powershell-on-windows-with-powershellget"></a>Installera Azure PowerShell på Windows med PowerShellGet

[!INCLUDE [migrate-to-az](../includes/migrate-to-az.md)]

I den här artikeln beskrivs stegen för att installera Azure PowerShell-modulerna för PowerShell 5.x för Windows med PowerShellGet. PowerShellGet och modulhantering är det bästa sättet att installera Azure PowerShell. Men om du hellre installerar med installationsprogrammet för webbplattformen eller med MSI-paketet kan du läsa om [andra installationsmetoder](other-install.md).

Den klassiska Azure-distributionsmodellen har inte stöd på den här versionen av Azure PowerShell. Följ anvisningarna i [Installera Azure PowerShell Service Management-modulen](/powershell/azure/servicemanagement/install-azure-ps) för stöd för klassiska distributioner.

> [!IMPORTANT]
> AzureRM-modulen stöds inte för macOS eller Linux. [Installera Az-modulen](/powershell/azure/install-az-ps) för att använda Azure PowerShell-cmdletar på dessa plattformar.

## <a name="requirements"></a>Krav

Från och med PowerShell version 6.0 kräver Azure PowerShell version 5.0. Kör följande kommando för att kontrollera vilken version av PowerShell som körs på din dator:

```powershell-interactive
$PSVersionTable.PSVersion
```

Läs informationen om att [uppgradera befintliga Windows PowerShell](/powershell/scripting/windows-powershell/install/installing-windows-powershell#upgrading-existing-windows-powershell) om du har en inaktuell version.

> [!IMPORTANT]
> Modulen AzureRM, som beskrivs i det här dokumentet, använder .NET Framework. Det här gör att den inte är kompatibel med PowerShell 6.0, som använder .NET Core. Om du använder PowerShell 6.0 följer du [anvisningarna för installation för Mac OS och Linux](/powershell/azure/install-az-ps).

## <a name="install-the-azure-powershell-module"></a>Installera Azure PowerShell-modulen

Du behöver ha utökade behörigheter för att installera moduler från PowerShell-galleriet. Kör följande kommando i en upphöjd session för att installera Azure PowerShell:

```azurepowershell-interactive
Install-Module -Name AzureRM -AllowClobber
```

> [!NOTE]
> Om du har en version av NuGet som är äldre än 2.8.5.201, uppmanas du att ladda ner och installera den senaste versionen av NuGet.

Som standard konfigureras inte PowerShell-galleriet som en betrodd lagringsplats för PowerShellGet. Första gången du använder PSGallery visas följande meddelande:

```Output
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the Set-PSRepository cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"):
```

Svara `Yes` eller `Yes to All` för att fortsätta med installationen.

Modulen `AzureRM` är en sammanslagen modul för Azure PowerShell-cmdletar. När du installerar den laddar den ned alla tillgängliga Azure Resource Manager-moduler och gör dess cmdletar tillgängliga för användning.

## <a name="sign-in"></a>Logga in

Börja arbeta med Azure PowerShell genom att logga in med dina autentiseringsuppgifter för Azure.

```azurepowershell-interactive
# Connect to Azure with an interactive dialog for sign-in
Connect-AzureRmAccount
```

> [!NOTE]
> Om du har inaktiverat modulen för automatisk inläsning måste du importera modulen manuellt med `Import-Module AzureRM`. Det kan ta några sekunder. Det beror på hur modulen är strukturerad.

Du måste upprepa de här stegen för varje ny PowerShell-session du startar. Information om hur du sparar Azure-inloggningen mellan olika PowerShell-sessioner hittar du i artikeln om att [spara autentiseringsuppgifter för användare mellan olika PowerShell-sessioner](context-persistence.md).

## <a name="update-the-azure-powershell-module"></a>Uppdatera Azure PowerShell-modulen

Du kan uppdatera din Azure PowerShell-installation genom att köra [Update-Module](/powershell/module/powershellget/update-module). Det här kommandot avinstallerar **inte** tidigare versioner.

```powershell-interactive
Update-Module -Name AzureRM
```

Se [Avinstallera Azure PowerShell-modulen](uninstall-azurerm-ps.md) om du vill ta bort äldre versioner av Azure PowerShell från ditt system.

## <a name="use-multiple-versions-of-azure-powershell"></a>Använd flera versioner av Azure PowerShell

Det är möjligt att installera fler än en version av Azure PowerShell. Använd följande kommando för att kontrollera om du har flera versioner av Azure PowerShell installerade:

```azurepowershell-interactive
Get-InstalledModule -Name AzureRM -AllVersions | select Name,Version
```

Se [Avinstallera Azure PowerShell-modulen](uninstall-azurerm-ps.md) om du vill ta bort en version av Azure PowerShell.

Du kan behöva fler än en version om du arbetar med lokala Azure Stack-resurser, kör en äldre version av Windows eller använder den klassiska Azure-distributionsmodellen. Ange argumentet `-RequiredVersion` när du installerar för att installera en äldre version.

```azurepowershell-interactive
# Install version 2.3.0 of Azure PowerShell
Install-Module -Name AzureRM -RequiredVersion 2.3.0
```

När du läser in Azure PowerShell-modulen läses den senaste versionen in som standard. Ange argumentet `-RequiredVersion` för att läsa in en annan version.

```azurepowershell-interactive
# Load version 2.3.0 of Azure PowerShell
Import-Module -Name AzureRM -RequiredVersion 2.3.0
```

## <a name="provide-feedback"></a>Ge feedback

Om du upptäcker en bugg när du använder Azure PowerShell kan du [öppna ett ärende på GitHub](https://github.com/Azure/azure-powershell/issues). Om du vill ge feedback från kommandoraden använder du cmdleten [Send-Feedback](/powershell/module/azurerm.profile/send-feedback).

## <a name="next-steps"></a>Efterföljande moment

Läs informationen i [Komma igång med Azure PowerShell](get-started-azureps.md) för att komma igång med Azure PowerShell och lära dig mer om modulerna och dess funktioner.
