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
ms.openlocfilehash: 72d147f5bc9c882083dda6b33b1c89663fd2eb34
ms.sourcegitcommit: 5f946a535eccca0b3ddf3db8f617b32564a88938
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/25/2018
ms.locfileid: "50001685"
---
# <a name="azure-stack-module-140"></a>Modulen Azure Stack 1.4.0

## <a name="requirements"></a>Krav:
Lägsta version av Azure Stack som stöds är 1804.

Obs! Om du använder en tidigare version måste du installera version 1.2.11

## <a name="known-issues"></a>Kända problem:

- Stäng avisering kräver Azure Stack version 1803
- Med New-AzsOffer kan du inte skapa ett erbjudande med tillståndet Offentlig. Cmdleten Set-AzsOffer måste anropas efteråt om du vill ändra tillståndet.
- För att en IP-pool ska kunna tas bort krävs en omdistribution

## <a name="breaking-changes"></a>Icke-bakåtkompatibla ändringar
Det är inga nya ändringar från version 1.3.0. Alla icke-bakåtkompatibla ändringar för migrering från 1.2.11 dokumenteras här https://aka.ms/azspowershellmigration

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
Use-AzureRmProfile -Profile 2017-03-09-profile -Force

# Install Azure Stack Admin Module
Install-Module -Name AzureStack -RequiredVersion 1.4.0
```
## <a name="release-notes"></a>Viktig information
    * Azurestack 1.4.0 har inga nya ändringar från den tidigare versionen 1.3.0
    * Azs.AzureBridge.Admin
        - Korrigering för felet som returnerade en enda sida i sidnumrerade resultat
    * Azs.Backup.Admin
        - Nya parametrar BackupFrequencyInHours, IsBackupSchedulerEnabled, BackupRetentionPeriodInDays har lagts till i cmdlet:en Set-AzsBackupShare
        - En cmdlet, New-EncyptionKeyBase64, har lagts till för att göra det möjligt att skapa en krypteringsnyckel
        - Korrigering för felet som returnerade en enda sida i sidnumrerade resultat
    * Azs.Commerce.Admin
        - Korrigering för felet som returnerade en enda sida i sidnumrerade resultat
    * Azs.Fabric.Admin
        - Korrigering för felet som returnerade en enda sida i sidnumrerade resultat
        - En cmdlet, Add-AzsScaleUnitNode, har lagts till för att administratörer ska kunna lägga till nya skalningsenhetsnoder till azurestack-stämpeln
        - En ny cmdlet, New-AzsScaleUnitNodeObject, har lagts till för att göra det möjligt att skapa parameterobjekt för skalningsenhet
    * Azs.Gallery.Admin
        - Korrigering för felet som returnerade en enda sida i sidnumrerade resultat
    * Azs.InfrastructureInsights.Admin
        - Korrigering för felet som returnerade en enda sida i sidnumrerade resultat
    * Azs.Network.Admin
        - Korrigering för felet som returnerade en enda sida i sidnumrerade resultat
    * Azs.Update.Admin
        - Korrigering för felet som returnerade en enda sida i sidnumrerade resultat
    * Azs.Subscriptions
        - Korrigering för felet som returnerade en enda sida i sidnumrerade resultat
    * Azs.Subscriptions.Admin
        - En cmdlet, Move-AzsSubscription, har lagts till för flytt av prenumerationer mellan delegerade providererbjudanden
        - En cmdlet, Test-AzsMoveSubscription, har lagts till för att validera att användarprenumerationer kan flyttas mellan delegerade providererbjudanden
        - Korrigering för felet som returnerade en enda sida i sidnumrerade resultat

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
Förhandsversionen av administratörsmodulen Azure Stack Compute som innehåller funktioner för att hantera beräkningskvoter, plattformsbilder och tillägg för virtuella datorer.

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
