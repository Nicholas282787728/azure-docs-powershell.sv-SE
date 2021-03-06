---
title: Installera Azure PowerShell med MSI
description: Så här installerar du Azure PowerShell utan PowerShellGet med MSI
ms.devlang: powershell
ms.topic: conceptual
ms.date: 10/22/2019
ms.custom: devx-track-azurepowershell
ms.service: azure-powershell
ms.openlocfilehash: 77f44eb47182377b88f5f57ce66c768cbe1f9630
ms.sourcegitcommit: 2036538797dd088728aee5ac5021472454d82eb2
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 11/06/2020
ms.locfileid: "93408504"
---
# <a name="install-azure-powershell-on-windows-with-msi"></a>Installera Azure PowerShell på Windows med MSI

Den här artikeln beskriver hur du installerar Azure PowerShell på Windows med ett MSI-installationsprogram. MSI-installationsprogrammet kan användas för miljöer där PowerShell-galleriet kan vara blockerat av en brandvägg eller då ett installationsprogram för offlinemiljöer behövs. PowerShellGet är det rekommenderade sättet att installera Azure PowerShell. Anvisningar om hur du använder PowerShellGet för att installera Azure PowerShell finns i [Installera Azure PowerShell med PowerShellGet](install-az-ps.md).

## <a name="requirements"></a>Krav

MSI-installationsprogrammet i Windows är utformat för att endast installera Azure PowerShell för PowerShell 5.1. Om du vill installera på andra plattformar än Windows eller för senare versioner av PowerShell [installerar du med PowerShellGet](install-az-ps.md). Du kan kontrollera vilken PowerShell-version du har genom att köra kommandot:

```powershell-interactive
$PSVersionTable.PSVersion
```

Du måste göra följande för att använda Azure PowerShell i PowerShell 5.1:

1. Uppdatera vid behov till [Windows PowerShell 5.1](/powershell/scripting/windows-powershell/install/installing-windows-powershell#upgrading-existing-windows-powershell). Om du använder Windows 10 kan PowerShell 5.1 redan vara installerat.
2. Installera [.NET Framework 4.7.2 eller senare](/dotnet/framework/install).

## <a name="install-or-update-on-windows-using-the-msi-package"></a>Installera eller uppdatera på Windows med hjälp av MSI-paketet

MSI-paketet för Azure PowerShell är tillgängligt från [GitHub](https://github.com/Azure/azure-powershell/releases/tag/v1.8.0-April2019). Om du har installerat tidigare versioner av Azure PowerShell med hjälp av MSI tar installationsprogrammet automatiskt bort dem. MSI-paketet installerar moduler i `${env:ProgramFiles}\WindowsPowerShell\Modules`.

Börja arbeta med Azure PowerShell genom att logga in med dina autentiseringsuppgifter för Azure.

```powershell-interactive
# Connect to Azure with an interactive dialog for sign-in
Connect-AzAccount
```

> [!NOTE]
> Om du har inaktiverat modulen för automatisk inläsning måste du importera modulen manuellt med `Import-Module Az`. Det kan ta upp till en minut. Det beror på hur modulen är strukturerad.

Du måste upprepa det här steget för varje ny PowerShell-session du startar. Information om hur du sparar Azure-inloggningen mellan olika PowerShell-sessioner hittar du i artikeln om att [spara autentiseringsuppgifter för användare mellan olika PowerShell-sessioner](context-persistence.md).

## <a name="provide-feedback"></a>Ge feedback

Om du upptäcker en bugg i Azure PowerShell kan du [öppna ett ärende på GitHub](https://github.com/Azure/azure-powershell/issues). Om du vill ge feedback från kommandoraden använder du cmdleten [Send-Feedback](/powershell/module/az.accounts/send-feedback).

## <a name="next-steps"></a>Efterföljande moment

Läs informationen i [Komma igång med Azure PowerShell](get-started-azureps.md) för att komma igång med Azure PowerShell-modulerna och deras funktioner. Om du känner till Azure PowerShell och behöver migrera från AzureRM läser du [Migrera från AzureRM till Az](migrate-from-azurerm-to-az.md).
