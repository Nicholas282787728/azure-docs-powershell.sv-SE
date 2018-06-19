---
title: Installera Azure PowerShell med PowerShellGet
description: Så här installerar du Azure PowerShell med PowerShellGet
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 05/31/2018
ms.openlocfilehash: 9b7046157e32a5c8473210e9840f9ae1b2f45902
ms.sourcegitcommit: bcf80dfd7fbe17e82e7ad029802cfe8a2f02b15c
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 06/11/2018
ms.locfileid: "35323109"
---
# <a name="install-azure-powershell-with-powershellget"></a>Installera Azure PowerShell med PowerShellGet

Den här artikeln beskriver stegen för att installera Azure PowerShell-moduler i en Windows-miljö med hjälp av PowerShellGet.  Det här är det bästa sättet att installera Azure PowerShell. Men om du hellre installerar med installationsprogrammet för webbplattformen eller med MSI-paketet kan du läsa om [andra installationsmetoder](other-install.md).

Läs följande artikel om du vill använda Azure PowerShell på macOS eller Linux: [Installera och konfigurera Azure PowerShell på macOS och Linux](install-azurermps-maclinux.md).

## <a name="system-requirements"></a>Systemkrav

Azure PowerShell-version 6.1.0 kräver version 5.0 (eller senare) av PowerShell. Information om hur du uppgraderar till PowerShell 5.0 finns i [Uppgradera befintlig Windows PowerShell](/powershell/scripting/setup/installing-windows-powershell?view=powershell-6#upgrading-existing-windows-powershell).

PowerShellGet inkluderas automatiskt som en del av PowerShell 5.0.

## <a name="install-or-update-the-azure-powershell-module"></a>Installera eller uppdatera Azure PowerShell-modulen

För installation av Azure PowerShell från PowerShell-galleriet krävs utökade behörigheter. Kör följande kommando från en utökad PowerShell-session:

```powershell
# Install the Azure Resource Manager modules from the PowerShell Gallery
Install-Module -Name AzureRM -AllowClobber
```

> [!IMPORTANT]
> Med det här kommandot uppdateras eventuella befintliga installationer av Azure PowerShell på datorn. Om du behöver ha mer än en version installerad kan du läsa svaret på frågan [Kan jag installera flera versioner av Azure PowerShell?](#multiple-versions) i avsnittet med vanliga frågor och svar.

Som standard konfigureras inte PowerShell-galleriet som en betrodd lagringsplats för PowerShellGet. Första gången du använder PSGallery visas följande meddelande:

```Output
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the Set-PSRepository cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"):
```

Svara Ja, eller Ja till alla om du vill fortsätta med installationen.

> [!NOTE]
> Om du har en version av NuGet som är äldre än 2.8.5.201, uppmanas du att ladda ner och installera den senaste versionen av NuGet.

Modulen AzureRM är en sammanslagen modul för Azure Resource Manager-cmdletar. När du installerar AzureRM-modulen kommer alla övriga Azure PowerShell-moduler som inte har installerats att laddas ned och installeras från PowerShell-galleriet.

## <a name="load-the-azure-powershell-module"></a>Läs in Azure PowerShell-modulen

När modulen har installerats måste du läsa in modulen i din PowerShell-session. Du bör göra det här i en normal (icke-förhöjd) PowerShell-session. Moduler läses in med `Import-Module`-cmdleten enligt följande:

```powershell
Import-Module -Name AzureRM
```

## <a name="reporting-issues-and-feedback"></a>Rapportera problem och feedback

Om du stöter på några buggar med verktyget kan du [rapportera problemet på GitHub](https://github.com/Azure/azure-powershell/issues). Om du vill ge feedback från kommandoraden, använder du cmdleten `Send-Feedback`.

## <a name="next-steps"></a>Nästa steg

Mer information om hur du använder Azure PowerShell finns i följande artiklar:

* [Kom igång med Azure PowerShell](get-started-azureps.md)

## <a name="frequently-asked-questions"></a>Vanliga frågor och svar

### <a id="helpmechoose"></a>Hur gör jag för att kontrollera vilken version av Azure PowerShell jag har?

Det finns stöd för flera versioner av Azure PowerShell, men vi rekommenderar att du uppgraderar till den senaste versionen så snart som möjligt. Om du vill kontrollera vilken version av Azure PowerShell som du har installerat kör du `Get-Module AzureRM` från kommandoraden.

```powershell
Get-Module AzureRM -ListAvailable | Select-Object -Property Name,Version,Path
```

### <a name="can-i-use-azure-powershell-for-azure-classic-deployments"></a>Kan jag använda Azure PowerShell för klassiska Azure-distributioner?

Om du har distributioner som använder den klassiska distributionsmodellen så kan du installera Service Management-versionen av Azure PowerShell. Läs mer i informationen om hur du [installerar Azure PowerShell Service Management-modulen](/powershell/azure/servicemanagement/install-azure-ps). Azure- och AzureRM-moduler delar gemensamma beroenden. Om du använder både Azure- och AzureRM-moduler, bör du installera samma version av varje paket.

### <a name="a-namemultiple-versionscan-i-install-multiple-versions-of-azure-powershell"></a><a name="multiple-versions"/>Kan jag installera flera versioner av Azure PowerShell?

PowerShellGet är den enda installationsmetoden som stöder installation av flera versioner. Om du vill installera flera versioner kan du lägga till parametern `-RequiredVersion` till cmdleten `Install-Module`. Till exempel kan du installera både version 6.1.0 och 1.2.9:

```powershell
Install-Module -Name AzureRM -RequiredVersion 6.1.0
Install-Module -Name AzureRM -RequiredVersion 1.2.9
```

Endast en version av modulen kan läsas in i en PowerShell-session. Du måste öppna ett nytt PowerShell-fönster och använda `Import-Module` för att importera en specifik version av Azure PowerShell-modulen.

```powershell
Import-Module -Name AzureRM -RequiredVersion 1.2.9
```

> [!NOTE]
> Version 2.1.0 och 1.2.6 är de första modulversionerna som är avsedda att installeras och användas sida vid sida. När du laddar en tidigare version av Azure PowerShell, laddas inkompatibla versioner av modulen **AzureRM.Profile**. Det gör att cmdletarna ber dig logga in när du kör en av dem.
