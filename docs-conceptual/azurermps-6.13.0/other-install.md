---
title: Andra sätt att installera Azure PowerShell
description: Så här installerar du Azure PowerShell utan PowerShellGet med MSI
ms.devlang: powershell
ms.topic: conceptual
ms.date: 11/16/2018
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: 41edefe96ecebf0a7276cdc3b4510acd7e8098f4
ms.sourcegitcommit: 8b3126b5c79f453464d90669f0046ba86b7a3424
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 09/01/2020
ms.locfileid: "89241615"
---
# <a name="install-azure-powershell-on-windows-with-msi"></a>Installera Azure PowerShell på Windows med MSI

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

Den här artikeln beskriver hur du installerar Azure PowerShell på Windows med ett MSI-installationsprogram.
Använd endast dessa installationsmetoder om de är nödvändiga för ditt system. PowerShellGet är det rekommenderade sättet att installera Azure PowerShell på Windows. Anvisningar om hur du använder PowerShellGet för att installera Azure PowerShell finns i [Installera Azure PowerShell med PowerShellGet](install-azurerm-ps.md).

> [!NOTE]
> Metoden att installera med installationsprogrammet för webbplattformen är inte längre tillgänglig för versioner av Azure PowerShell 6.x eller senare. Om du måste använda installationsprogrammet för webbplattformen kan du överväga att använda MSI istället, eller installera en tidigare version av Azure PowerShell.

## <a name="install-or-update-on-windows-using-the-msi-package"></a>Installera eller uppdatera på Windows med hjälp av MSI-paketet

Azure PowerShell för Windows PowerShell 5.x kan installeras med hjälp av MSI-filen som är tillgänglig från [GitHub](https://github.com/Azure/azure-powershell/releases/tag/v6.13.1-November2018). Om du har installerat tidigare versioner av Azure-moduler som MSI så tar installationsprogrammet automatiskt bort dem. MSI-paketet installerar moduler i `${env:ProgramFiles}\WindowsPowerShell\Modules`. Både modulerna `AzureRM` och `Azure` installeras.

> [!NOTE]
> Använd endast modulen `Azure` om du arbetar med den klassiska Azure-distributionsmodellen.

Börja arbeta med Azure PowerShell genom att logga in med dina autentiseringsuppgifter för Azure.

```powershell-interactive
# Connect to Azure with an interactive dialog for sign-in
Connect-AzureRmAccount
```

> [!NOTE]
>
> Om du har inaktiverat modulen för automatisk inläsning måste du importera modulen manuellt med `Import-Module AzureRM`. Det kan ta några sekunder. Det beror på hur modulen är strukturerad.

Du måste upprepa det här steget för varje ny PowerShell-session du startar. Information om hur du sparar Azure-inloggningen mellan olika PowerShell-sessioner hittar du i artikeln om att [spara autentiseringsuppgifter för användare mellan olika PowerShell-sessioner](context-persistence.md).
