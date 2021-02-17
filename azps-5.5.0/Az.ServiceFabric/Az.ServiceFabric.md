---
Module Name: Az.ServiceFabric
Module Guid: 60f3ba88-443f-46ff-88a3-318cfd11c1da
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric
Help Version: 0.3.4.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Az.ServiceFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Az.ServiceFabric.md
ms.openlocfilehash: 6c58f25209a0acd227e2f04e7ca808916f283d46
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100253013"
---
# Az.ServiceFabric-modul
## Beskrivning
Azure Service Fabric Module som du kan använda för att automatisera end-2-end-åtgärder som att skapa ett säkert kluster, rulla över klustercertifikat, lägga till eller ta bort noder från klustret osv. En fullständig lista över alla åtgärder visas nedan.

## Az.ServiceFabric Cmdlets
### [Add-AzServiceFabricClientCertificate](Add-AzServiceFabricClientCertificate.md)
Lägg till ett vanligt namn eller tumavtryck i klustret för klientautentisering.

### [Add-AzServiceFabricClusterCertificate](Add-AzServiceFabricClusterCertificate.md)
Lägga till ett sekundärt klustercertifikat i klustret.

### [Add-AzServiceFabricManagedClusterClientCertificate](Add-AzServiceFabricManagedClusterClientCertificate.md)
Lägg till ett vanligt namn eller thumbprint för certifikatet i klustret. Då registreras certifikatet igen för klientautentisering.

### [Add-AzServiceFabricManagedNodeTypeVMExtension](Add-AzServiceFabricManagedNodeTypeVMExtension.md)
Lägg till vm-tillägg till nodtypen.

### [Add-AzServiceFabricManagedNodeTypeVMSecret](Add-AzServiceFabricManagedNodeTypeVMSecret.md)
Lägg till certifikathemlighet i nodtypen.

### [Add-AzServiceFabricNode](Add-AzServiceFabricNode.md)
Lägg till noder i den specifika nodtypen i klustret.

### [Add-AzServiceFabricNodeType](Add-AzServiceFabricNodeType.md)
Lägga till en ny nodtyp i det befintliga klustret.

### [Get-AzServiceFabricApplication](Get-AzServiceFabricApplication.md)
Hämta programinformation för Service Fabric.

### [Get-AzServiceFabricApplicationType](Get-AzServiceFabricApplicationType.md)
Hämta programtypen Service Fabric.

### [Get-AzServiceFabricApplicationTypeVersion](Get-AzServiceFabricApplicationTypeVersion.md)
Versionsinformation för programtypen Service Fabric.

### [Get-AzServiceFabricCluster](Get-AzServiceFabricCluster.md)
Få information om klusterresursen.

### [Get-AzServiceFabricManagedCluster](Get-AzServiceFabricManagedCluster.md)
Hämta information om hanterade klusterresurser.

### [Get-AzServiceFabricManagedNodeType](Get-AzServiceFabricManagedNodeType.md)
Hämta information om den hanterade nodens typ av resurs.

### [Get-AzServiceFabricService](Get-AzServiceFabricService.md)
Hämta tjänstinformation för Service Fabric under det angivna programmet och klustret.

### [New-AzServiceFabricApplication](New-AzServiceFabricApplication.md)
Skapa nytt program för tjänsten under den angivna resursgruppen och det angivna resursklustret.

### [New-AzServiceFabricApplicationType](New-AzServiceFabricApplicationType.md)
Skapa den nya programtypen för tjänstkluster under den angivna resursgruppen och det angivna klustret.

### [New-AzServiceFabricApplicationTypeVersion](New-AzServiceFabricApplicationTypeVersion.md)
Skapa en ny programtypsversion i angiven resursgrupp och angivet resurskluster.

### [New-AzServiceFabricCluster](New-AzServiceFabricCluster.md)
Det här kommandot använder certifikat som du tillhandahåller eller systemgenererade själv signerade certifikat för att skapa ett nytt tjänstkluster. Du kan använda en standardmall eller en anpassad mall som du anger. Du kan ange en mapp för att exportera de själv signerade certifikaten till eller hämta dem senare från nyckelvalvet.

### [New-AzServiceFabricManagedCluster](New-AzServiceFabricManagedCluster.md)
Skapa ett nytt hanterat kluster.

### [New-AzServiceFabricManagedNodeType](New-AzServiceFabricManagedNodeType.md)
Skapa en ny nodtypsresurs.

### [New-AzServiceFabricService](New-AzServiceFabricService.md)
Skapa ny tjänst påkluster under det angivna programmet och klustret.

### [Remove-AzServiceFabricApplication](Remove-AzServiceFabricApplication.md)
Ta bort ett program från klustret. Då tas alla tjänster i programmet bort.

### [Remove-AzServiceFabricApplicationType](Remove-AzServiceFabricApplicationType.md)
Ta bort tjänstkluster och programtyper från klustret. Då tas alla typer av versioner under resursen bort.

### [Remove-AzServiceFabricApplicationTypeVersion](Remove-AzServiceFabricApplicationTypeVersion.md)
Ta bort tjänstematerial en programtypsversion från klustret.

### [Remove-AzServiceFabricClientCertificate](Remove-AzServiceFabricClientCertificate.md)
Ta bort ett klientcertifikat eller certifikatämnesnamn från att användas för klientautentisering till klustret.

### [Remove-AzServiceFabricClusterCertificate](Remove-AzServiceFabricClusterCertificate.md)
Ta bort ett klustercertifikat från att användas för klustersäkerhet.

### [Remove-AzServiceFabricManagedCluster](Remove-AzServiceFabricManagedCluster.md)
Ta bort klusterresursen.

### [Remove-AzServiceFabricManagedClusterClientCertificate](Remove-AzServiceFabricManagedClusterClientCertificate.md)
Remvoe-klientcertifikat med thumbprint eller vanligt namn.

### [Remove-AzServiceFabricManagedNodeType](Remove-AzServiceFabricManagedNodeType.md)
Ta bort nodtypen eller specifika noder i nodtypen.

### [Remove-AzServiceFabricManagedNodeTypeVMExtension](Remove-AzServiceFabricManagedNodeTypeVMExtension.md)
Ta bort vm-tillägg från nodtypen.

### [Remove-AzServiceFabricNode](Remove-AzServiceFabricNode.md)
Ta bort noder från den specifika nodtypen från ett kluster.

### [Remove-AzServiceFabricNodeType](Remove-AzServiceFabricNodeType.md)
Ta bort en fullständig nodtyp från ett kluster.

### [Remove-AzServiceFabricService](Remove-AzServiceFabricService.md)
Ta bort en tjänst från klustret.

### [Remove-AzServiceFabricSetting](Remove-AzServiceFabricSetting.md)
Ta bort en eller flera Service Fabric-inställningar från klustret.

### [Restart-AzServiceFabricManagedNodeType](Restart-AzServiceFabricManagedNodeType.md)
Starta om specifika noder från nodtypen.

### [Set-AzServiceFabricManagedCluster](Set-AzServiceFabricManagedCluster.md)
Ange egenskaper för klusterresurser.

### [Set-AzServiceFabricManagedNodeType](Set-AzServiceFabricManagedNodeType.md)
Anger nodtypsresursegenskaper eller kör reimageåtgärder på specifika nodtyper med -reimageparameter.

### [Set-AzServiceFabricSetting](Set-AzServiceFabricSetting.md)
Lägga till eller uppdatera en eller flera Service Fabric-inställningar i klustret.

### [Set-AzServiceFabricUpgradeType](Set-AzServiceFabricUpgradeType.md)
Ändra typ av uppgraderingstyp för Service Fabric för klustret.

### [Update-AzServiceFabricApplication](Update-AzServiceFabricApplication.md)
Uppdatera ett program för tjänsten. Det här gör att du kan uppdatera programparametrar och/eller uppgradera den programtypsversion som utlöser en programuppgradering.

### [Update-AzServiceFabricDurability](Update-AzServiceFabricDurability.md)
Uppdatera prestandanivån eller VmSku för en nodtyp i klustret.

### [Update-AzServiceFabricReliability](Update-AzServiceFabricReliability.md)
Uppdatera tillförlitlighetsnivån för primärnodstypen i ett kluster.

