---
title: Översikt över Azure Stack PowerShell för administratörer | Microsoft Docs
description: En översikt över Azure Stack PowerShell för administratörer med anvisningar för installation och konfiguration.
author: bganapa
ms.author: bganapa
manager: knithinc
ms.devlang: powershell
ms.topic: conceptual
ms.manager: knithinc
ms.date: 09/21/2018
ms.openlocfilehash: afa83a6258e57e961576b328e67fad634704dddf
ms.sourcegitcommit: 4afdba3cd7e1d348876ce59f3503fdcd258f79ab
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 11/15/2018
ms.locfileid: "51580569"
---
# <a name="azure-stack-module-150"></a>Modulen Azure Stack 1.5.0

## <a name="requirements"></a>Krav:
Den lägsta versionen av Azure Stack som stöds är 1808.

Obs! Om du använder en tidigare version så måste du installera version 1.4.0

## <a name="known-issues"></a>Kända problem:

- Med New-AzsOffer kan du inte skapa ett erbjudande med tillståndet Offentlig. Cmdleten Set-AzsOffer måste anropas efteråt om du vill ändra tillståndet.
- För att en IP-pool ska kunna tas bort krävs en omdistribution

## <a name="install"></a>Installera
```
# Remove previous versions of AzureStack modules
Uninstall-Module -Name AzureStack -Force 
Uninstall-Module AzureRM.AzureStackAdmin -Force
Uninstall-Module AzureRM.AzureStackStorage -Force
Get-Module Azs.* -ListAvailable | Uninstall-Module -Force


# Install the AzureRM.Bootstrapper module. Select Yes when prompted to install NuGet
Install-Module -Name AzureRm.BootStrapper

# Install and import the API Version Profile required by Azure Stack into the current PowerShell session.
Use-AzureRmProfile -Profile 2018-03-01-hybrid -Force

# Install Azure Stack Admin Module
Install-Module -Name AzureStack -RequiredVersion 1.5.0
```

## <a name="release-notes"></a>Viktig information
* Alla administratörsmoduler i Azure Stack har uppdaterats för större eller lika stort beroende på modulen AzureRm.Profile
* Stöd för hantering av kapslade resursnamn i alla moduler
* Ett fel i alla moduler där ErrorActionPreference har åsidosattes för att bli Stop har korrigerats
* Administratörsmodul för Azs.Compute
    * Nya kvotegenskaper har lagts till för att stödja hanterade diskar
    * Cmdletar som rör diskmigrering har lagts till
    * Ytterligare egenskaper i objekt för plattformsavbildningen och VM-tilläggen
* Azs.Fabric.Admin 
    * Ny cmdlet för att lägga till nod för skalningsenhet
* Azs.Backup.Admin
    * Set-AzsBackupShare är nu ett alias till cmdleten Set-AzsBackupConfiguration
    * Get-AzsBackupLocation är nu ett alias till cmdleten Get-AzsBackupConfiguration
    * Set-AzsBackupConfiguration, parametern BackupShare är nu ett alias för parametersökvägen
* Azs.Subscriptions
    * Get-AzsDelegatedProviderOffer, parametern OfferName är nu ett alias för Offer
* Azs.Subscriptions.Admin
    * Get-AzsDelegatedProviderOffer, parametern OfferName är nu ett alias för Offer

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
