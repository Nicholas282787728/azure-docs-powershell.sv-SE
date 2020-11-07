---
Module Name: Az.ServiceFabric
Module Guid: 60f3ba88-443f-46ff-88a3-318cfd11c1da
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric
Help Version: 0.3.4.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Az.ServiceFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Az.ServiceFabric.md
ms.openlocfilehash: 01bf8c630f4fc4d137e98be5b1996eaf47ea3363
ms.sourcegitcommit: 43f4bdf2a59dd82fd881512aa9761bf72eb5703c
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/23/2019
ms.locfileid: "93743139"
---
# Modulen AZ. ServiceFabric
## Problembeskrivning
Modul för Azure Service Fabric som du kan använda för att automatisera slut 2-avsluta-åtgärderna som att skapa ett säkert kluster, rulla över kluster certifikat, lägga till eller ta bort noder från klustret osv. Den fullständiga listan över alla åtgärder visas nedan.

## AZ. ServiceFabric-cmdletar
### [Add-AzServiceFabricApplicationCertificate](Add-AzServiceFabricApplicationCertificate.md)
Lägg till ett nytt certifikat till den virtuella datorns skal uppsättning (er) som utgör klustret. Certifikatet är avsett att användas som ett program certifikat.

### [Add-AzServiceFabricClientCertificate](Add-AzServiceFabricClientCertificate.md)
Lägg till vanligt namn eller tumavtryck i klustret för användning av klientautentisering.

### [Add-AzServiceFabricClusterCertificate](Add-AzServiceFabricClusterCertificate.md)
Lägg till ett sekundärt kluster certifikat i klustret.

### [Add-AzServiceFabricNode](Add-AzServiceFabricNode.md)
Lägga till noder till den specifika nodtypen i klustret.

### [Add-AzServiceFabricNodeType](Add-AzServiceFabricNodeType.md)
Lägg till en ny nodtyp i det befintliga klustret.

### [Get-AzServiceFabricCluster](Get-AzServiceFabricCluster.md)
Hämta information om kluster resursen.

### [New-AzServiceFabricCluster](New-AzServiceFabricCluster.md)
I det här kommandot används certifikat som du tillhandahåller eller systemgenererade självsignerade certifikat för att skapa ett nytt tjänst Fabric-kluster. Den kan använda en standardmall eller en anpassad mall som du anger. Du kan välja att ange en mapp att exportera självsignerade certifikat till eller hämta dem senare från huvud valvet. 

### [Remove-AzServiceFabricClientCertificate](Remove-AzServiceFabricClientCertificate.md)
Ta bort ett eller flera klient certifikat eller certifikat subjekt namn som används för klientautentisering till klustret.

### [Remove-AzServiceFabricClusterCertificate](Remove-AzServiceFabricClusterCertificate.md)
Ta bort ett kluster certifikat från att användas för kluster säkerhet.

### [Remove-AzServiceFabricNode](Remove-AzServiceFabricNode.md)
Ta bort noder från en viss nodtyp från ett kluster.

### [Remove-AzServiceFabricNodeType](Remove-AzServiceFabricNodeType.md)
Ta bort en fullständig nodtyp från ett kluster.

### [Remove-AzServiceFabricSetting](Remove-AzServiceFabricSetting.md)
Ta bort en eller flera tjänst Fabric-inställningar från klustret.

### [Set-AzServiceFabricSetting](Set-AzServiceFabricSetting.md)
Lägga till eller uppdatera en eller flera tjänst infrastruktur inställningar i klustret.

### [Set-AzServiceFabricUpgradeType](Set-AzServiceFabricUpgradeType.md)
Ändra kluster för Service Fabric-uppgradering.

### [Update-AzServiceFabricDurability](Update-AzServiceFabricDurability.md)
Uppdatera livs längden eller VmSku för en nodtyp i klustret.

### [Update-AzServiceFabricReliability](Update-AzServiceFabricReliability.md)
Uppdatera Tillförlitlighets nivån för den primära nodtypen i ett kluster.

