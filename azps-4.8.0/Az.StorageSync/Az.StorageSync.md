---
Module Name: Az.StorageSync
Module Guid: 001b4bbc-9d7d-43b2-9e95-7a70325e9509
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.storagesync
Help Version: 1.0.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Az.StorageSync.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Az.StorageSync.md
ms.openlocfilehash: bc3704c3594826f19399c1967bbe86ed7f1e8773
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94258480"
---
# Modulen AZ. StorageSync
## Problembeskrivning
Med cmdletar i modulen synkronisering av lagring kan du hantera åtgärder för Azure-filsynkronisering i PowerShell.

## AZ. StorageSync-cmdletar
### [Get-AzStorageSyncCloudEndpoint](Get-AzStorageSyncCloudEndpoint.md)
Det här kommandot visar alla moln slut punkter i en given synkroniseringskoppling.

### [Get-AzStorageSyncGroup](Get-AzStorageSyncGroup.md)
Det här kommandot visar alla synkroniseringsresurser i en given synkroniseringstjänst för lagring.

### [Get-AzStorageSyncServer](Get-AzStorageSyncServer.md)
Det här kommandot visar alla servrar registrerade till en given synkroniseringstjänst för lagring.

### [Get-AzStorageSyncServerEndpoint](Get-AzStorageSyncServerEndpoint.md)
Det här kommandot visar alla Server slut punkter i en given synkroniseringskoppling.

### [Get-AzStorageSyncService](Get-AzStorageSyncService.md)
Det här kommandot visar alla lagrings Sync-tjänster i ett givet omfång av abonnemang/resurs grupp.

### [Invoke-AzStorageSyncChangeDetection](Invoke-AzStorageSyncChangeDetection.md)
Det här kommandot kan användas för att manuellt identifiera ändringar av namn områden. Den kan riktas till hela resursen, undermappen eller uppsättningen filer. Högst 10 000-ändringar kan identifieras. Om omfattningen av ändringar är känd för dig kan du begränsa körningen av det här kommandot till delar av namn området så att ändrings kontrollen kan slutföras snabbt och i en 10 000-ändrings gräns.

### [Invoke-AzStorageSyncCompatibilityCheck](Invoke-AzStorageSyncCompatibilityCheck.md)
Kontrollerar eventuella kompatibilitetsproblem mellan din dator och Azure-filsynkronisering.

### [Invoke-AzStorageSyncFileRecall](Invoke-AzStorageSyncFileRecall.md)
Det här kommandot återställer alla nivåbaserade filer tillbaka till lokala diskar.

### [New-AzStorageSyncCloudEndpoint](New-AzStorageSyncCloudEndpoint.md)
Det här kommandot skapar en Azure File Sync-slutpunkt för moln i en synkroniseringsresurs.

### [New-AzStorageSyncGroup](New-AzStorageSyncGroup.md)
Det här kommandot skapar en ny synkroniseringsresurs i en angiven synkroniseringstjänst.

### [New-AzStorageSyncServerEndpoint](New-AzStorageSyncServerEndpoint.md)
Det här kommandot skapar en ny server slut punkt på en registrerad Server. Då aktive ras den angivna sökvägen på servern för att synkronisera filer med andra slut punkter i synkroniseringsresursen.

### [New-AzStorageSyncService](New-AzStorageSyncService.md)
Det här kommandot skapar en ny lagrings synkroniseringstjänst i en resurs grupp.

### [Set-AzStorageSyncService](New-AzStorageSyncService.md)
Det här kommandot anger en synkroniseringstjänst för lagring i en resurs grupp.

### [Register-AzStorageSyncServer](Register-AzStorageSyncServer.md)
Det här kommandot registrerar en server i en lagrings tjänst som skapar en förtroende relation. PowerShell eller Azure-portalen kan sedan användas för att konfigurera synkronisering på den här servern.

### [Remove-AzStorageSyncCloudEndpoint](Remove-AzStorageSyncCloudEndpoint.md)
Det här kommandot tar bort den angivna moln slut punkten från en synkroniseringsresurs. Utan åtminstone en moln slut punkt kan ingen annan server slut punkter i den här synkroniseringsresursen synkronisera.

### [Remove-AzStorageSyncGroup](Remove-AzStorageSyncGroup.md)
Det här kommandot tar bort den angivna synkroniseringsresursen.

### [Remove-AzStorageSyncServerEndpoint](Remove-AzStorageSyncServerEndpoint.md)
Det här kommandot tar bort den angivna Server slut punkten. Synkronisering till den här platsen stoppas omedelbart.

### [Remove-AzStorageSyncService](Remove-AzStorageSyncService.md)
Det här kommandot tar bort den angivna tjänsten för lagrings synkronisering.

### [Reset-AzStorageSyncServerCertificate](Reset-AzStorageSyncServerCertificate.md)
Används endast för fel sökning. Det här kommandot återställer Server certifikatet för lagringstester som används för att beskriva Server identiteten för Storage Sync-tjänsten.

### [Set-AzStorageSyncServerEndpoint](Set-AzStorageSyncServerEndpoint.md)
Det här kommandot möjliggör ändringar i de justerbara parametrarna för en server slut punkt.

### [Avregistrera-AzStorageSyncServer](Unregister-AzStorageSyncServer.md)
Varning! om du avregistrerar en server kommer alla Server slut punkter att tas bort från den här servern. Det här kommandot avregistrerar en server från tjänsten Storage Sync.

