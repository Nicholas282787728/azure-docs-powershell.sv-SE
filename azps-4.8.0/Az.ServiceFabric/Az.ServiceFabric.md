---
Module Name: Az.ServiceFabric
Module Guid: 60f3ba88-443f-46ff-88a3-318cfd11c1da
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric
Help Version: 0.3.4.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Az.ServiceFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Az.ServiceFabric.md
ms.openlocfilehash: 6c58f25209a0acd227e2f04e7ca808916f283d46
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94103514"
---
# Modulen AZ. ServiceFabric
## Problembeskrivning
Modul för Azure Service Fabric som du kan använda för att automatisera slut 2-avsluta-åtgärderna som att skapa ett säkert kluster, rulla över kluster certifikat, lägga till eller ta bort noder från klustret osv. Den fullständiga listan över alla åtgärder visas nedan.

## AZ. ServiceFabric-cmdletar
### [Add-AzServiceFabricClientCertificate](Add-AzServiceFabricClientCertificate.md)
Lägg till vanligt namn eller tumavtryck i klustret för användning av klientautentisering.

### [Add-AzServiceFabricClusterCertificate](Add-AzServiceFabricClusterCertificate.md)
Lägg till ett sekundärt kluster certifikat i klustret.

### [Add-AzServiceFabricManagedClusterClientCertificate](Add-AzServiceFabricManagedClusterClientCertificate.md)
Lägg till certifikatets namn eller tumavtryck i klustret. Detta registrerar certifikatet igen i klustret för klientautentisering.

### [Add-AzServiceFabricManagedNodeTypeVMExtension](Add-AzServiceFabricManagedNodeTypeVMExtension.md)
Lägg till virtuellt dator tillägg till nodtypen.

### [Add-AzServiceFabricManagedNodeTypeVMSecret](Add-AzServiceFabricManagedNodeTypeVMSecret.md)
Lägg till certifikat hemlighet till nodtyp.

### [Add-AzServiceFabricNode](Add-AzServiceFabricNode.md)
Lägga till noder till den specifika nodtypen i klustret.

### [Add-AzServiceFabricNodeType](Add-AzServiceFabricNodeType.md)
Lägg till en ny nodtyp i det befintliga klustret.

### [Get-AzServiceFabricApplication](Get-AzServiceFabricApplication.md)
Få information om tjänstens Fabric-program.

### [Get-AzServiceFabricApplicationType](Get-AzServiceFabricApplicationType.md)
Information om hur du skaffar Service Fabric-programmet.

### [Get-AzServiceFabricApplicationTypeVersion](Get-AzServiceFabricApplicationTypeVersion.md)
Hämta versions information för Service Fabric program typ.

### [Get-AzServiceFabricCluster](Get-AzServiceFabricCluster.md)
Hämta information om kluster resursen.

### [Get-AzServiceFabricManagedCluster](Get-AzServiceFabricManagedCluster.md)
Få information om de hanterade kluster resurserna.

### [Get-AzServiceFabricManagedNodeType](Get-AzServiceFabricManagedNodeType.md)
Hämta resursinformation för hanterad nod.

### [Get-AzServiceFabricService](Get-AzServiceFabricService.md)
Få information om tjänstens infrastruktur tjänst under angiven program och ett kluster.

### [New-AzServiceFabricApplication](New-AzServiceFabricApplication.md)
Skapa ett nytt tjänst Fabric-program under den angivna resurs gruppen och klustret.

### [New-AzServiceFabricApplicationType](New-AzServiceFabricApplicationType.md)
Skapa en ny program typ för tjänst Fabric under den angivna resurs gruppen och klustret.

### [New-AzServiceFabricApplicationTypeVersion](New-AzServiceFabricApplicationTypeVersion.md)
Skapa en ny program typs version under den angivna resurs gruppen och klustret.

### [New-AzServiceFabricCluster](New-AzServiceFabricCluster.md)
I det här kommandot används certifikat som du tillhandahåller eller systemgenererade självsignerade certifikat för att skapa ett nytt tjänst Fabric-kluster. Den kan använda en standardmall eller en anpassad mall som du anger. Du kan välja att ange en mapp att exportera självsignerade certifikat till eller hämta dem senare från huvud valvet.

### [New-AzServiceFabricManagedCluster](New-AzServiceFabricManagedCluster.md)
Skapa ett nytt hanterat kluster.

### [New-AzServiceFabricManagedNodeType](New-AzServiceFabricManagedNodeType.md)
Skapa en ny resurs för nodtyp.

### [New-AzServiceFabricService](New-AzServiceFabricService.md)
Skapa en ny tjänst infrastruktur tjänst under det angivna programmet och klustret.

### [Remove-AzServiceFabricApplication](Remove-AzServiceFabricApplication.md)
Ta bort ett program från klustret. Detta tar bort alla tjänster under programmet.

### [Remove-AzServiceFabricApplicationType](Remove-AzServiceFabricApplicationType.md)
Ta bort tjänstens infrastruktur program typ från klustret. Detta tar bort alla typ versioner under den här resursen.

### [Remove-AzServiceFabricApplicationTypeVersion](Remove-AzServiceFabricApplicationTypeVersion.md)
Ta bort Service Fabric en program typ version från klustret.

### [Remove-AzServiceFabricClientCertificate](Remove-AzServiceFabricClientCertificate.md)
Ta bort ett eller flera klient certifikat eller certifikat subjekt namn som används för klientautentisering till klustret.

### [Remove-AzServiceFabricClusterCertificate](Remove-AzServiceFabricClusterCertificate.md)
Ta bort ett kluster certifikat från att användas för kluster säkerhet.

### [Remove-AzServiceFabricManagedCluster](Remove-AzServiceFabricManagedCluster.md)
Ta bort en kluster resurs.

### [Remove-AzServiceFabricManagedClusterClientCertificate](Remove-AzServiceFabricManagedClusterClientCertificate.md)
Remvoe klient certifikat via tumavtryck eller eget namn.

### [Remove-AzServiceFabricManagedNodeType](Remove-AzServiceFabricManagedNodeType.md)
Ta bort nodtypen eller specifika noder inom nodtypen.

### [Remove-AzServiceFabricManagedNodeTypeVMExtension](Remove-AzServiceFabricManagedNodeTypeVMExtension.md)
Ta bort virtuellt dator tillägg från nodtyp.

### [Remove-AzServiceFabricNode](Remove-AzServiceFabricNode.md)
Ta bort noder från en viss nodtyp från ett kluster.

### [Remove-AzServiceFabricNodeType](Remove-AzServiceFabricNodeType.md)
Ta bort en fullständig nodtyp från ett kluster.

### [Remove-AzServiceFabricService](Remove-AzServiceFabricService.md)
Ta bort en tjänst från klustret.

### [Remove-AzServiceFabricSetting](Remove-AzServiceFabricSetting.md)
Ta bort en eller flera tjänst Fabric-inställningar från klustret.

### [Restart-AzServiceFabricManagedNodeType](Restart-AzServiceFabricManagedNodeType.md)
Starta om specifika noder från nodtypen.

### [Set-AzServiceFabricManagedCluster](Set-AzServiceFabricManagedCluster.md)
Ange egenskaper för en kluster resurs.

### [Set-AzServiceFabricManagedNodeType](Set-AzServiceFabricManagedNodeType.md)
Anger resurs egenskaper för nodtyp eller kör återavbildnings åtgärder för specifika NDES för noden nodtyp med-Rebild.

### [Set-AzServiceFabricSetting](Set-AzServiceFabricSetting.md)
Lägga till eller uppdatera en eller flera tjänst infrastruktur inställningar i klustret.

### [Set-AzServiceFabricUpgradeType](Set-AzServiceFabricUpgradeType.md)
Ändra kluster för Service Fabric-uppgradering.

### [Update-AzServiceFabricApplication](Update-AzServiceFabricApplication.md)
Uppdatera ett tjänst Fabric-program. Då kan du uppdatera program parametrarna och/eller uppgradera program typs versionen som utlöser en program uppgradering.

### [Update-AzServiceFabricDurability](Update-AzServiceFabricDurability.md)
Uppdatera livs längden eller VmSku för en nodtyp i klustret.

### [Update-AzServiceFabricReliability](Update-AzServiceFabricReliability.md)
Uppdatera Tillförlitlighets nivån för den primära nodtypen i ett kluster.

