---
Module Name: AzureRM.ServiceFabric
Module Guid: 60f3ba88-443f-46ff-88a3-318cfd11c1da
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicefabric
Help Version: 0.3.4.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/AzureRM.ServiceFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/AzureRM.ServiceFabric.md
ms.openlocfilehash: 0bd157b8df4cca37c92a4d4f2984011dbd924e34
ms.sourcegitcommit: 43f4bdf2a59dd82fd881512aa9761bf72eb5703c
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/23/2019
ms.locfileid: "93570636"
---
# Modulen AzureRM. ServiceFabric
## Problembeskrivning
Modul för Azure Service Fabric som du kan använda för att automatisera slut 2-avsluta-åtgärderna som att skapa ett säkert kluster, rulla över kluster certifikat, lägga till eller ta bort noder från klustret osv. Den fullständiga listan över alla åtgärder visas nedan.

## AzureRM. ServiceFabric-cmdletar
### [Add-AzureRmServiceFabricApplicationCertificate](Add-AzureRmServiceFabricApplicationCertificate.md)
Lägg till ett nytt certifikat till den virtuella datorns skal uppsättning (er) som utgör klustret. Certifikatet är avsett att användas som ett program certifikat.

### [Add-AzureRmServiceFabricClientCertificate](Add-AzureRmServiceFabricClientCertificate.md)
Lägg till vanligt namn eller tumavtryck i klustret för användning av klientautentisering.

### [Add-AzureRmServiceFabricClusterCertificate](Add-AzureRmServiceFabricClusterCertificate.md)
Lägg till ett sekundärt kluster certifikat i klustret.

### [Add-AzureRmServiceFabricNode](Add-AzureRmServiceFabricNode.md)
Lägga till noder till den specifika nodtypen i klustret.

### [Add-AzureRmServiceFabricNodeType](Add-AzureRmServiceFabricNodeType.md)
Lägg till en ny nodtyp i det befintliga klustret.

### [Get-AzureRmServiceFabricCluster](Get-AzureRmServiceFabricCluster.md)
Hämta information om kluster resursen.

### [New-AzureRmServiceFabricCluster](New-AzureRmServiceFabricCluster.md)
I det här kommandot används certifikat som du tillhandahåller eller systemgenererade självsignerade certifikat för att skapa ett nytt tjänst Fabric-kluster. Den kan använda en standardmall eller en anpassad mall som du anger. Du kan välja att ange en mapp att exportera självsignerade certifikat till eller hämta dem senare från huvud valvet. 

### [Remove-AzureRmServiceFabricClientCertificate](Remove-AzureRmServiceFabricClientCertificate.md)
Ta bort ett eller flera klient certifikat eller certifikat subjekt namn som används för klientautentisering till klustret.

### [Remove-AzureRmServiceFabricClusterCertificate](Remove-AzureRmServiceFabricClusterCertificate.md)
Ta bort ett kluster certifikat från att användas för kluster säkerhet.

### [Remove-AzureRmServiceFabricNode](Remove-AzureRmServiceFabricNode.md)
Ta bort noder från en viss nodtyp från ett kluster.

### [Remove-AzureRmServiceFabricNodeType](Remove-AzureRmServiceFabricNodeType.md)
Ta bort en fullständig nodtyp från ett kluster.

### [Remove-AzureRmServiceFabricSetting](Remove-AzureRmServiceFabricSetting.md)
Ta bort en eller flera tjänst Fabric-inställningar från klustret.

### [Set-AzureRmServiceFabricSetting](Set-AzureRmServiceFabricSetting.md)
Lägga till eller uppdatera en eller flera tjänst infrastruktur inställningar i klustret.

### [Set-AzureRmServiceFabricUpgradeType](Set-AzureRmServiceFabricUpgradeType.md)
Ändra kluster för Service Fabric-uppgradering.

### [Update-AzureRmServiceFabricDurability](Update-AzureRmServiceFabricDurability.md)
Uppdatera livs längden eller VmSku för en nodtyp i klustret.

### [Update-AzureRmServiceFabricReliability](Update-AzureRmServiceFabricReliability.md)
Uppdatera Tillförlitlighets nivån för den primära nodtypen i ett kluster.

