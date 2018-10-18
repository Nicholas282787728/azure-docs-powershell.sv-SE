---
title: Andra sätt att installera Azure PowerShell
description: Så här installerar du Azure PowerShell utan PowerShellGet med MSI
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 09/11/2018
ms.openlocfilehash: 52fa80542af39a2a768cc54e5b6bd8d0b8246c9f
ms.sourcegitcommit: f6f5e256143aa6c097de3e57e930d8badea49f30
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/18/2018
ms.locfileid: "49399033"
---
# <a name="install-azure-powershell-on-windows-with-msi"></a>Installera Azure PowerShell på Windows med MSI

Den här artikeln beskriver hur du installerar Azure PowerShell på Windows med ett MSI-installationsprogram.  
Använd endast dessa installationsmetoder om de är nödvändiga för ditt system. PowerShellGet är det rekommenderade sättet att installera Azure PowerShell på Windows. Anvisningar om hur du använder PowerShellGet för att installera Azure PowerShell finns i [Installera Azure PowerShell med PowerShellGet](install-azurerm-ps.md).

> [!NOTE]
> Metoden att installera med installationsprogrammet för webbplattformen är inte längre tillgänglig för versioner av Azure PowerShell 6.x eller senare. Om du måste använda installationsprogrammet för webbplattformen kan du överväga att använda MSI istället, eller installera en tidigare version av Azure PowerShell.

Information om hur du installerar i Linux- eller macOS-miljöer finns i [Installera Azure PowerShell på macOS eller Linux](install-azurermps-maclinux.md).

## <a name="install-or-update-on-windows-using-the-msi-package"></a>Installera eller uppdatera på Windows med hjälp av MSI-paketet

Azure PowerShell kan installeras med hjälp av MSI-filen som är tillgänglig från [GitHub](https://github.com/Azure/azure-powershell/releases/latest). Om du har installerat tidigare versioner av Azure-moduler som MSI så tar installationsprogrammet automatiskt bort dem. MSI-paketet installerar moduler i `${env:ProgramFiles}\WindowsPowerShell\Modules`. Både modulerna `AzureRM` och `Azure` installeras.

> [!NOTE]
> Använd endast modulen `Azure` om du arbetar med den klassiska Azure-distributionsmodellen.

Du måste läsa in `AzureRM` till din nuvarande PowerShell-session med cmdleten [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module) och sedan logga in med dina autentiseringsuppgifter för Azure för att börja arbeta med Azure PowerShell.

```powershell
# Import the module into the PowerShell session
Import-Module AzureRM
# Connect to Azure with an interactive dialog for sign-in
Connect-AzureRmAccount
```

Du måste upprepa de här stegen för varje ny PowerShell-session du startar. Om du vill importera modulen `AzureRM` automatiskt måste du konfigurera en PowerShell-profil, som du kan läsa om i [Om profiler](/powershell/module/microsoft.powershell.core/about/about_profiles).
Om du vill lära dig hur du sparar din Azure-inloggning mellan olika sessioner kan du läsa informationen om att [spara autentiseringsuppgifter för användare mellan olika PowerShell-sessioner](context-persistence.md).
