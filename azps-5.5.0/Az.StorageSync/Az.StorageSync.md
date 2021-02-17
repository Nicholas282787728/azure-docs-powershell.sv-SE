---
Module Name: Az.StorageSync
Module Guid: 001b4bbc-9d7d-43b2-9e95-7a70325e9509
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.storagesync
Help Version: 1.0.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Az.StorageSync.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Az.StorageSync.md
ms.openlocfilehash: bc3704c3594826f19399c1967bbe86ed7f1e8773
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100217198"
---
# Az.StorageSync-modul
## Beskrivning
Med cmdletarna i modulen Lagringssynkronisering kan du hantera åtgärder som gäller Azure File Sync i PowerShell.

## Az.StorageSync-cmdlets
### [Get-AzStorageSyncCloudEndpoint](Get-AzStorageSyncCloudEndpoint.md)
Det här kommandot listar alla molnslutpunkter i en viss synkroniseringsgrupp.

### [Get-AzStorageSyncGroup](Get-AzStorageSyncGroup.md)
Det här kommandot listar alla synkroniseringsgrupper i en viss lagringssynkroniseringstjänst.

### [Get-AzStorageSyncServer](Get-AzStorageSyncServer.md)
Det här kommandot listar alla servrar som är registrerade på en viss lagringssynkroniseringstjänst.

### [Get-AzStorageSyncServerEndpoint](Get-AzStorageSyncServerEndpoint.md)
Det här kommandot listar alla serverslutpunkter i en viss synkroniseringsgrupp.

### [Get-AzStorageSyncService](Get-AzStorageSyncService.md)
Det här kommandot listar alla lagringssynkroniseringstjänster inom en viss omfattning för prenumeration/resursgrupp.

### [Invoke-AzStorageSyncChangeDetection](Invoke-AzStorageSyncChangeDetection.md)
Det här kommandot kan användas för att manuellt starta identifieringen av namnområdesändringar. Den kan riktas till hela delnings-, undermappen eller uppsättningen filer. Maximalt 10 000 ändringar kan identifieras. Om du känner till omfattningen av ändringarna kan du begränsa körningen av det här kommandot till delar av namnområdet, så ändringsidentifiering kan avslutas snabbt och inom en gräns på 10 000 ändringar.

### [Invoke-AzStorageSyncCompatibilityCheck](Invoke-AzStorageSyncCompatibilityCheck.md)
Söker efter potentiella kompatibilitetsproblem mellan systemet och Azure File Sync.

### [Invoke-AzStorageSyncFileRecall](Invoke-AzStorageSyncFileRecall.md)
Det här kommandot återkallar alla nivåfiler tillbaka till den lokala hårddisken.

### [New-AzStorageSyncCloudEndpoint](New-AzStorageSyncCloudEndpoint.md)
Med det här kommandot skapas en molnslutpunkt för Azure-filsynkronisering i en synkroniseringsgrupp.

### [New-AzStorageSyncGroup](New-AzStorageSyncGroup.md)
Med det här kommandot skapas en ny synkroniseringsgrupp inom en angiven lagringssynkroniseringstjänst.

### [New-AzStorageSyncServerEndpoint](New-AzStorageSyncServerEndpoint.md)
Det här kommandot skapar en ny serverslutpunkt på en registrerad server. Då kan den angivna sökvägen på servern börja synkronisera filerna med andra slutpunkter i synkroniseringsgruppen.

### [New-AzStorageSyncService](New-AzStorageSyncService.md)
Med det här kommandot skapas en ny tjänst för lagringssynkronisering i en resursgrupp.

### [Set-AzStorageSyncService](New-AzStorageSyncService.md)
Det här kommandot anger en lagringssynkroniseringstjänst i en resursgrupp.

### [Register-AzStorageSyncServer](Register-AzStorageSyncServer.md)
Det här kommandot registrerar en server till en lagringssynkroniseringstjänst som skapar en förtroenderelation. PowerShell eller Azure-portalen kan sedan användas för att konfigurera synkronisering på den här servern.

### [Remove-AzStorageSyncCloudEndpoint](Remove-AzStorageSyncCloudEndpoint.md)
Det här kommandot tar bort den angivna molnslutpunkten från en synkroniseringsgrupp. Utan minst en molnslutpunkt kan inga andra serverslutpunkter i den här synkroniseringsgruppen synkronisera.

### [Remove-AzStorageSyncGroup](Remove-AzStorageSyncGroup.md)
Med det här kommandot tas den angivna synkroniseringsgruppen bort.

### [Remove-AzStorageSyncServerEndpoint](Remove-AzStorageSyncServerEndpoint.md)
Det här kommandot tar bort den angivna serverslutpunkten. Synkroniseringen till den här platsen avbryts omedelbart.

### [Remove-AzStorageSyncService](Remove-AzStorageSyncService.md)
Det här kommandot tar bort den angivna lagringssynkroniseringstjänsten.

### [Reset-AzStorageSyncServerCertificate](Reset-AzStorageSyncServerCertificate.md)
Används endast för felsökning. Det här kommandot rullar det servercertifikat för lagringssynkronisering som används för att beskriva serveridentiteten till lagringssynkroniseringstjänsten.

### [Set-AzStorageSyncServerEndpoint](Set-AzStorageSyncServerEndpoint.md)
Med det här kommandot kan du ändra de justerbara parametrarna i en serverslutpunkt.

### [Unregister-AzStorageSyncServer](Unregister-AzStorageSyncServer.md)
Varning! Om du avregistrerar en server kan det resultera i sammanhängande borttagningar av alla serverslutpunkter på den här servern. Det här kommandot avregistrerar en server från sin lagringssynkroniseringstjänst.

