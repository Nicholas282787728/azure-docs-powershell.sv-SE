---
title: Översikt över Azure Stack PowerShell | Microsoft Docs
description: En översikt över Azure Stack PowerShell med anvisningar för installation och konfiguration.
author: bganapa
ms.author: bganapa
manager: knithinc
ms.devlang: powershell
ms.topic: conceptual
ms.manager: knithinc
ms.date: 09/21/2018
ms.openlocfilehash: d514e43d82bcb51f65831dc506e58e8747db0381
ms.sourcegitcommit: 19dffee617477001f98d43e39a50ce1fad087b74
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 09/27/2018
ms.locfileid: "47178467"
---
# <a name="azurerm-module-230"></a>AzureRM-modul 2.3.0

## <a name="requirements"></a>Krav:
Den lägsta versionen av Azure Stack som stöds är 1808.

Obs! Om du använder en tidigare version måste du installera version 1.2.11


## <a name="install"></a>Installera
```powershell
# Remove previous versions of AzureStack modules
Uninstall-Module -Name AzureStack -Force 
Uninstall-Module -Name AzureRM -Force 
Uninstall-Module AzureRM.AzureStackAdmin -Force -ErrorAction Continue
Uninstall-Module AzureRM.AzureStackStorage -Force -ErrorAction Continue
Get-Module Azs.* -ListAvailable | Uninstall-Module -Force
Get-Module Azure.* -ListAvailable | Uninstall-Module -Force


# Install the AzureRM.Bootstrapper module. Select Yes when prompted to install NuGet
Install-Module -Name AzureRm.BootStrapper

# Install and import the API Version Profile required by Azure Stack into the current PowerShell session.
Use-AzureRmProfile -Profile 2018-03-01-hybrid -Force

```

##<a name="release-notes"></a>Viktig information
* Version 2.3.0 omfattar en lista över icke-bakåtkompatibla ändringar. Om du vill uppgradera från version 1.2.11 har vi skapat en migreringsguide här: https://aka.ms/azspowershellmigration
* Den här versionen motsvarar den azurestack-specifika API-profilen 2018-03-01-hybrid
* Alla moduler använder större eller lika stort beroende på modulen AzureRm.Profile.
* API-versionen som stöds av alla moduler har uppdaterats. 
    * Compute – 2017-03-30
    * Nätverk – 2017-10-01
    * Storage – 2016-01-01
    * Resurser – 2018-02-01
    * KeyVault – 2016-10-01
    * DNS – 2016-04-01
* Den fullständiga kartan över API-versioner för var och en av resurstyperna finns på https://github.com/Azure/azure-rest-api-specs/blob/master/profile/2018-03-01-hybrid.json

## <a name="content"></a>Innehåll:
### <a name="azure-bridge"></a>Azure Bridge
Förhandsversionen av administratörsmodulen AzureBridge i Azure Stack, där du kan publicera bilder från Azure.

### <a name="backup"></a>Backup
Förhandsversionen av administratörsmodulen Backup som gör att administratörer kan:
- Konfigurera var säkerhetskopiorna ska lagras
- Säkerhetskopiera
- Lista och återställda slutförda säkerhetskopior

### <a name="commerce"></a>Commerce
Förhandsversionen av administratörsmodulen Azure Stack Commerce som innehåller funktioner för att visa sammanställd dataanvändning i hela ditt Azure Stack-system.

### <a name="compute"></a>Compute
Förhandsversionen av administratörsmodulen Azure Stack Compute som innehåller funktioner för att hantera beräkningskvoter, plattformsbilder, hanterade diskar och tillägg för virtuella datorer.

### <a name="fabric"></a>Fabric
Förhandsversionen av administratörsmodulen Azure Stack Fabric där administratörer kan visa och hantera infrastrukturskomponenter:
- Stoppa, starta och stänga ned noder för skalningsenheter
- Tömma och återuppta noder för skalningsenheter för FRU-relaterade aktiviteter
- Reparation av noder för skalningsenheter
- Omstart av infrastrukturrollen
- Stoppa, starta och stänga ned instanser av infrastrukturroller
- Skapa nya IP-pooler


### <a name="gallery"></a>Galleri
Förhandsversionen av administratörsmodulen Azure Stack Gallery som innehåller funktioner för att hantera galleriobjekt på Azure Stack Marketplace.

### <a name="infrastructure-insights"></a>Infrastructure Insights
Förhandsversionen av administratörsmodulen Infrastructure Insights där administratörer kan:
- Visa hälsotillstånd för sina stämpelresurser i Azure Stack
- Visa och hantera aviseringar

### <a name="keyvault"></a>KeyVault
Förhandsversionen av administratörsmodulen Azure Stack KeyVault, där administratören kan visa KeyVault-kvoter.

### <a name="network"></a>Nätverk
Förhandsversionen av administratörsmodulen för Network med funktioner för:
- Hantering av nätverkskvoter
- Visning av allokerade nätverksresurser, t.ex. offentliga IP-adresser, virtuella nätverk, lastbalanserare
- Tillhandahåller en cmdlet som visar en administratörsöversikt

### <a name="storage"></a>Storage
Förhandsversion av administratörsmodulen Azure Stack Storage.  I den här versionen tillhandahåller vi funktioner för:
- Hantering av lagringskvoter
- Skräpinsamling av raderade lagringsresurser
- Återställning av raderade lagringskonton
- Migrering av containrar från en resurs till en annan
- Visning av information om enskilda lagringskomponenter
- Visning av information om användning och prestanda

### <a name="subscription-admin"></a>Prenumerationsadministration
Förhandsversion av administratörsmodulen Azure Stack Subscription.  Den här modulen innehåller administratörsfunktioner för att:
- Hantera avtal och erbjudanden
- Visa information om användning och prestanda
- Hantera RBAC

### <a name="subscription"></a>Prenumeration
Förhandsversion av modulen Azure Stack Subscription.  Den här modulen innehåller användarfunktioner för att:
- Skapa, ta bort och uppdatera prenumerationer

### <a name="update"></a>Uppdatering
Förhandsversion av administratörsmodulen Azure Stack Update.  I den här kan modulen kan administratörer:
- Lista och installera tillgängliga uppdateringar
- Återuppta avbrutna uppdateringar
- Visa installerade uppdateringar
