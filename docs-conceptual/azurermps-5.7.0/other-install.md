---
title: Andra sätt att installera Azure PowerShell
description: Så här installerar du Azure PowerShell utan PowerShellGet
ms.devlang: powershell
ms.topic: conceptual
ms.date: 06/20/2018
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: 7148188603e84efbcd784264de4c78819edf6833
ms.sourcegitcommit: 8b3126b5c79f453464d90669f0046ba86b7a3424
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 09/01/2020
ms.locfileid: "89243726"
---
# <a name="install-azure-powershell-on-windows-with-msi-or-web-platform-installer"></a>Installera Azure PowerShell på Windows med MSI eller installationsprogrammet för webbplattformen

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

Den här artikeln beskriver hur du installerar Azure PowerShell på Windows med hjälp av en hanterad tjänstidentitet eller installationsprogrammet för webbplattformen (WebPI).
Använd endast dessa installationsmetoder om de är nödvändiga för ditt system. PowerShellGet är det rekommenderade sättet att installera Azure PowerShell på Windows. Anvisningar om hur du använder PowerShellGet för att installera Azure PowerShell finns i [Installera Azure PowerShell med PowerShellGet](install-azurerm-ps.md).

## <a name="install-or-update-on-windows-using-the-msi-package"></a>Installera eller uppdatera på Windows med hjälp av MSI-paketet

Azure PowerShell kan installeras med hjälp av MSI-filen som är tillgänglig från [GitHub](https://github.com/Azure/azure-powershell/releases/tag/v5.7.0-April2018). Om du har installerat tidigare versioner av Azure-moduler som MSI så tar installationsprogrammet automatiskt bort dem. MSI-paketet installerar moduler i `${env:ProgramFiles}\WindowsPowerShell\Modules`. Både modulerna `AzureRM` och `Azure` installeras.

> [!NOTE]
> Använd endast modulen `Azure` om du arbetar med den klassiska Azure-distributionsmodellen.

Du måste läsa in `AzureRM` till din nuvarande PowerShell-session med cmdleten [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module) och sedan logga in med dina autentiseringsuppgifter för Azure för att börja arbeta med Azure PowerShell.

```powershell-interactive
# Import the module into the PowerShell session
Import-Module AzureRM
# Connect to Azure with an interactive dialog for sign-in
Connect-AzureRmAccount
```

Du måste upprepa de här stegen för varje ny PowerShell-session du startar. Om du vill importera modulen `AzureRM` automatiskt måste du konfigurera en PowerShell-profil, som du kan läsa om i [Om profiler](/powershell/module/microsoft.powershell.core/about/about_profiles).
Om du vill lära dig hur du sparar din Azure-inloggning mellan olika sessioner kan du läsa informationen om att [spara autentiseringsuppgifter för användare mellan olika PowerShell-sessioner](context-persistence.md).

## <a name="install-or-update-on-windows-using-the-web-platform-installer"></a>Installera eller uppdatera på Windows med hjälp av installationsprogrammet för webbplattformen

Hämta [Azure PowerShell WebPI-paketet](https://aka.ms/webpi-azps) och starta installationen. Om du har installerat tidigare versioner av Azure-moduler från MSI eller med installationsprogrammet för webbplattformen så tar installationsprogrammet automatiskt bort dem. Moduler installeras till `${env:ProgramFiles}\WindowsPowerShell\Modules`. Både modulerna `AzureRM` och `Azure` installeras.

> [!NOTE]
> Använd endast modulen `Azure` om du arbetar med den klassiska Azure-distributionsmodellen.

Du måste läsa in `AzureRM` till din nuvarande PowerShell-session med cmdleten [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module) och sedan logga in med dina autentiseringsuppgifter för Azure för att börja arbeta med Azure PowerShell.

```powershell-interactive
# Import the module into the PowerShell session
Import-Module AzureRM
# Connect to Azure with an interactive dialog for sign-in
Connect-AzureRmAccount
```

Du måste upprepa de här stegen för varje ny PowerShell-session du startar. Om du vill importera modulen `AzureRM` automatiskt måste du konfigurera en PowerShell-profil, som du kan läsa om i [Om profiler](/powershell/module/microsoft.powershell.core/about/about_profiles).
Om du vill lära dig hur du sparar din Azure-inloggning mellan olika sessioner kan du läsa informationen om att [spara autentiseringsuppgifter för användare mellan olika PowerShell-sessioner](context-persistence.md).
