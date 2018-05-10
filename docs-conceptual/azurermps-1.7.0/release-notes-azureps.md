---
title: Ändringslogg för Azure PowerShell | Microsoft Docs
description: Det här är en historik över de ändringar som gjorts i den senaste versionen av Azure PowerShell.
services: azure
author: sdwheeler
ms.author: sewhee
manager: carmonm
ms.service: azure-powershell
ms.product: azure
ms.devlang: powershell
ms.topic: conceptual
ms.workload: ''
ms.date: 05/18/2017
ms.openlocfilehash: 0a3f152751fee569d3ac5fba6bcff8c1737f7b8c
ms.sourcegitcommit: 37bfbf11fd0967a8e7977c692ab829d286baf88a
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 05/08/2018
---
# <a name="release-notes"></a>Viktig information

Det här är en lista över ändringar som har gjorts i Azure PowerShell i den här versionen.

## <a name="version-170"></a>Version 1.7.0

* **Beteendet har ändrats för parametrarna -Force, –Confirm och $ConfirmPreference för alla cmdletar. Vi håller på att ändra den här implementeringen så att den följer riktlinjerna för PowerShell. För de flesta cmdletarna innebär detta borttagning av parametern Force och att ShouldProcess-meddelandet hoppas över. Användarna måste ta med parametern -Confirm:$false i sina PowerShell-skript.** Den här ändringarna åtgärdar följande problem:
  - Rätt implementering av –WhatIf-funktioner, vilket gör att en användare att bestämma effekterna av en cmdlet eller ett skript utan att göra ändringar
  - Kontroll över uppmaningar med sessionsomfattande $ConfirmPreference, så att användaren får en uppmaning baserat på en presumtiv ändring (såsom rapporteras i inställningen ConfirmImpact i cmdleten)
  - Cmdlet-specifik kontroll över bekräftelseuppmaningar med parametern –Confirm
  - Konsekvent användning av ShouldContinue och parametern –Force i cmdletar, endast för de åtgärder som kräver uppmaning från användaren på grund av ändringarnas särskilda karaktär (till exempel borttagning av dolda filer)
  - Konsekvens med andra PowerShell-cmdletar, så att PowerShell-skriptkunskaper från andra cmdletar är direkt tillämpliga på Azure PowerShell-cmdletar.

**Observera att användaren nu måste ange två parametrar för *Azure PowerShell-cmdletar för att* automatiskt hoppa över alla uppmaningar (gäller samtliga fall):**
```powershell
My-CmdletWithConfirmation –Confirm:$false -Force
```
* Azure Compute
  - Set-AzureRmVMADDomainExtension
  - Get-AzureRmVMADDomainExtension
  - Parametern -Redeploy för Restart-AzureVM
  - Parametern -Validate för Move-AzureService, Move-AzureStorageAccount och Move-AzureVirtualNetwork
  - Parametrarna för namn och version för cmdletar för tillägg är valfria som tidigare.
  - New-AzureVM kan få en licenstyp från VM-objektet.
* Azure Storage
  - Ändra parametern Tags till Tag och lägg till parameteralias Tags
    + New-AzureRmStorageAccount
    + Set-AzureRmStorageAccount
* Azure-nätverk
  - Ny cmdlet har lagts till för virtuell nätverkspeering
* Azure Redis Cache
  - Ny cmdlet har lagts till för Reset-AzureRmRedisCache
  - Ny cmdlet har lagts till för Export-AzureRmRedisCache
  - Ny cmdlet har lagts till för Import-AzureRmRedisCache
  - Cmdleten New-AzureRmRedisCache har ändrats för att innefatta parameterändring för vNet
* Säkerhetskopiering och återställning av Azure SQL-databas
  - Cmdletar för säkerhetskopieringsfunktionen för långsiktig kvarhållning
  - Get-AzureRmSqlServerBackupLongTermRetentionVault
  - Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy
  - Set-AzureRmSqlServerBackupLongTermRetentionVault
  - Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy
  - Restore-AzureRmSqlDatabase stöder nu återställning till tidpunkt för en borttagen databas
  - Restore-AzureRmSqlDatabase stöder nu återställning från en säkerhetskopiering med långsiktig kvarhållning
* Azure LogicApp
  - Cmdletar har lagts till för LogicApp-integreringskonton.
  - Get-AzureRmIntegrationAccountAgreement
  - Get-AzureRmIntegrationAccountCallbackUrl
  - Get-AzureRmIntegrationAccountCertificate
  - Get-AzureRmIntegrationAccount
  - Get-AzureRmIntegrationAccountMap
  - Get-AzureRmIntegrationAccountPartner
  - Get-AzureRmIntegrationAccountSchema
  - New-AzureRmIntegrationAccountAgreement
  - New-AzureRmIntegrationAccountCertificate
  - New-AzureRmIntegrationAccount
  - New-AzureRmIntegrationAccountMap
  - New-AzureRmIntegrationAccountPartner
  - New-AzureRmIntegrationAccountSchema
  - Remove-AzureRmIntegrationAccountAgreement
  - Remove-AzureRmIntegrationAccountCertificate
  - Remove-AzureRmIntegrationAccount
  - Remove-AzureRmIntegrationAccountMap
  - Remove-AzureRmIntegrationAccountPartner
  - Remove-AzureRmIntegrationAccountSchema
  - Set-AzureRmIntegrationAccountAgreement
  - Set-AzureRmIntegrationAccountCertificate
  - Set-AzureRmIntegrationAccount
  - Set-AzureRmIntegrationAccountMap
  - Set-AzureRmIntegrationAccountPartner
  - Set-AzureRmIntegrationAccountSchema
* Azure Data Lake Store
  - Kraftig förbättring av prestanda för uppladdning och nedladdning av filer och mappar.
  - Detta innefattar en liten ändring i parameternamnen för nedladdning och två nya parametrar för uppladdning:
    + NumThreads -> PerFileThreadCount, används för att ange antal trådar som ska användas i en enskild fil
    + ConcurrentFileCount, används för att ange antal filer som ska överföras/ladda ned parallellt vid uppladdning/nedladdning av mappar.
  - Standardtrådkörningsvärden har utformats för att ge ett bättre dataflöde för de flesta filstorlekar. Om önskade prestanda inte uppnås kan värdena ovan ändras för att uppfylla kraven.
* Azure Data Lake Analytics
  - Nu returnerar Get-AzureRMDataLakeAnalyticsDataSource alla datakällor vid anrop utan argument.
  - Med denna ändring tas också parametern för datakälltyp bort från cmdleten.
  - Den här ändringen gör att ett nytt objekt returneras för liståtgärden med följande egenskaper:
    + Type (typ av datakälla)
    + Name (namnet på datakällan)
    + IsDefault (har värdet true om detta är standarddatakällan för kontot)
  - Get-AzureRMDataLakeAnalyticsJob har åtgärdats. Detta gäller vissa förskjutningsvärden för datum och tid i listan vid filtrering på submittedBefore och submittedAfter.
* Web Apps
  - Lägg till cmdleten Swap-AzureRmWebAppSlot för vanlig växling och växling med förhandsgranskning
  - Utöka cmdleten Set-AzureRmWebAppSlot för att stödja automatisk växling
* Azure API Management
  - Cmdletar för Azure Api-hanteringsdistribution har åtgärdats för AzureChinaCloud.
  - Cmdleten Set-AzureRmApiManagementTenantGitAccess har tagits bort eftersom Git-åtkomst är aktiverat som standard.
* Azure Recovery Services Backup
  - Stöd för Azure SQL-arbetsbelastningen har lagts till
  - Stöd för att säkerhetskopiera och återställa krypterade virtuella Azure-datorer har lagts till
  - Backup-AzureRmRecoveryServicesBackupItem – funktion för valfri kvarhållningstid har lagts till för återställningspunkter
  - Mindre filterrelaterade fel har åtgärdats i cmdletarna Get-AzureRmRecoveryServicesBackupContainer och Get-AzureRmRecoveryServicesBackupItem
* Azure Automation
  - Get-AzureRmAutomationHybridWorkerGroup har lagts till
