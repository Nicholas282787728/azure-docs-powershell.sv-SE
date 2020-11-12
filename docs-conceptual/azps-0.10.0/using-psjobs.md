---
title: Köra Azure PowerShell-cmdletar i PowerShell-jobb
description: Lär dig hur du kör Azure PowerShell-cmdletar parallellt eller som bakgrundsaktiviteter med hjälp av -AsJob och Start-Job.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 10/21/2019
ms.custom: devx-track-azurepowershell
ms.service: azure-powershell
ms.openlocfilehash: b76e310e1677e539927ebc4746df67c1d1accc16
ms.sourcegitcommit: 2036538797dd088728aee5ac5021472454d82eb2
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 11/06/2020
ms.locfileid: "93408828"
---
# <a name="run-azure-powershell-cmdlets-in-powershell-jobs"></a>Köra Azure PowerShell-cmdletar i PowerShell-jobb

Azure PowerShell är beroende av att ansluta till ett Azure-moln och vänta på svar, så att de flesta av dessa cmdletar blockerar PowerShell-sessionen tills de får ett svar från molnet.
Med PowerShell-jobb kan du köra cmdletar i bakgrunden eller utföra flera uppgifter på Azure samtidigt, inifrån en och samma PowerShell-session.

Den här artikeln ger en kort översikt över hur du kör Azure PowerShell-cmdletar som PowerShell-jobb och kontrollerar att de är klara. Om du ska köra kommandon i Azure PowerShell måste du använda Azure PowerShell-kontexter som beskrivs i detalj i [Azure-kontexter och inloggningsuppgifter](context-persistence.md).
Mer information om PowerShell-jobb finns i [Om PowerShell-jobb](/powershell/module/microsoft.powershell.core/about/about_jobs).

## <a name="azure-contexts-with-powershell-jobs"></a>Azure-kontexter med PowerShell-jobb

PowerShell-jobb körs som separata processer utan en ansluten PowerShell-session, så dina Azure-autentiseringsuppgifter måste delas med dem. Autentiseringsuppgifterna skickas som Azure-kontextobjekt med någon av följande metoder:

* Automatisk kontextpersistens. Kontextpersistens är aktiverat som standard och bevarar din inloggningsinformation över flera sessioner. Med kontextpersistens aktiverat skickas den aktuella Azure-kontexten till den nya processen:

  ```azurepowershell-interactive
  Enable-AzContextAutosave # Enables context autosave if not already on
  $creds = Get-Credential
  $job = Start-Job { param($vmadmin) New-AzVM -Name MyVm -Credential $vmadmin } -ArgumentList $creds
  ```

* Använd parametern `-AzContext` med alla Azure PowerShell-cmdletar för att ange ett Azure-kontextobjekt:

  ```azurepowershell-interactive
  $context = Get-AzContext -Name 'mycontext' # Get an Azure context object
  $creds = Get-Credential
  $job = Start-Job { param($context, $vmadmin) New-AzVM -Name MyVm -AzContext $context -Credential $vmadmin} -ArgumentList $context,$creds }
  ```

  Om kontextpersistens är inaktiverat krävs argumentet `-AzContext`.

* Använd växeln `-AsJob` som tillhandahålls av vissa Azure PowerShell-cmdletar. Den här växeln startar automatiskt cmdleten som ett PowerShell-jobb med den aktuella aktiva Azure-kontexten:

  ```azurepowershell-interactive
  $creds = Get-Credential
  $job = New-AzVM -Name MyVm -Credential $creds -AsJob
  ```

  Om du vill se om en cmdlet stöder `-AsJob` kan du kontrollera referensdokumentationen. Växeln `-AsJob` kräver inte att kontexten sparas automatiskt.

Du kan kontrollera statusen för ett jobb som körs med cmdleten [Get-Job](/powershell/module/microsoft.powershell.core/get-job). Om du vill hämta utdata från ett jobb hittills använder du cmdleten [Receive-Job](/powershell/module/microsoft.powershell.core/receive-job).

Om du vill kontrollera en åtgärds status på Azure via en fjärranslutning använder du de `Get-`-cmdletar som är kopplade till den typ av resurs som ändras av jobbet:

```azurepowershell-interactive
$creds = Get-Credential
$context = Get-AzContext -Name 'mycontext'
$vmName = "MyVm"

$job = Start-Job { param($context, $vmName, $vmadmin) New-AzVM -Name $vmName -AzContext $context -Credential $vmadmin} -ArgumentList $context,$vmName,$creds }

Get-Job $job
Get-AzVM -Name $vmName
```

## <a name="see-also"></a>Se även

* [Azure PowerShell-kontexter](context-persistence.md)
* [Om PowerShell-jobb](/powershell/module/microsoft.powershell.core/about/about_jobs)
* [Referens för Get-Job](/powershell/module/microsoft.powershell.core/get-job)
* [Referens för Receive-Job](/powershell/module/microsoft.powershell.core/receive-job)
