---
title: Installera och konfigurera Azure PowerShell | Microsoft Docs
description: Installera och konfigurera Azure PowerShell för första gången.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/27/2018
ms.openlocfilehash: ef796bcb81e24b1942c644aad2b4ec7705916b02
ms.sourcegitcommit: 087c588169786c005a3c177624fb3ac6c8870125
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/13/2018
ms.locfileid: "53217753"
---
# <a name="install-and-configure-azure-powershell"></a>Installera och konfigurera Azure PowerShell

Den här artikeln beskriver stegen för att installera Azure PowerShell-moduler i en Windows-miljö.
Om du vill använda Azure PowerShell på macOS eller Linux kan du läsa följande artikel: [Installera och konfigurera Azure PowerShell på macOS och Linux](install-azurermps-maclinux.md).

Det rekommenderade sättet att installera Azure PowerShell är från PowerShell-galleriet.

## <a name="step-1-install-powershellget"></a>Steg 1: Installera PowerShellGet

Du måste ha modulen PowerShellGet för att kunna installera objekt från PowerShell-galleriet. Kontrollera att du har rätt version av PowerShellGet och att datorn uppfyller övriga systemkrav. Kör följande kommando för att se om du har PowerShellGet installerat på datorn.

```powershell-interactive
Get-Module -Name PowerShellGet -ListAvailable | Select-Object -Property Name,Version,Path
```

Nu bör du se utdata som ser ut ungefär så här:

```Output
Name          Version Path
----          ------- ----
Name          Version Path
----          ------- ----
PowerShellGet 1.6.0   C:\Program Files\WindowsPowerShell\Modules\PowerShellGet\1.6.0\PowerShellGet.psd1
PowerShellGet 1.0.0.1 C:\Program Files\WindowsPowerShell\Modules\PowerShellGet\1.0.0.1\PowerShellGet.psd1
```

Du behöver PowerShellGet version 1.1.2.0 eller senare. Om du vill uppdatera PowerShellGet använder du följande kommando:

```powershell-interactive
Install-Module PowerShellGet -Force
```

Om du inte har installerat PowerShellGet kan du läsa avsnittet [Hämta PowerShellGet](#how-to-get-powershellget) i den här artikeln.

> [!NOTE]
> För att kunna använda PowerShellGet, krävs en körningsprincip som låter dig köra skript. Mer information om PowerShell-körningsprincipen finns i [Om körningsprinciper](/powershell/module/microsoft.powershell.core/about/about_execution_policies).
>
> [!IMPORTANT]
> Modulen AzureRM, som beskrivs i det här dokumentet, använder .NET Framework. Det här gör att den inte är kompatibel med PowerShell 6.0, som använder .NET Core. Om du använder PowerShell 6.0 följer du [anvisningarna för installation för Mac OS och Linux](install-azurermps-maclinux.md).

## <a name="step-2-install-azure-powershell"></a>Steg 2: Installera Azure PowerShell

För installation av Azure PowerShell från PowerShell-galleriet krävs utökade behörigheter. Kör följande kommando från en utökad PowerShell-session:

```powershell-interactive
# Install the Azure Resource Manager modules from the PowerShell Gallery
Install-Module -Name AzureRM -AllowClobber
```

Som standard konfigureras inte PowerShell-galleriet som en betrodd lagringsplats för PowerShellGet. Första gången du använder PSGallery visas följande meddelande:

```Output
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the Set-PSRepository cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"): Y
```

Svara Ja, eller Ja till alla om du vill fortsätta med installationen.

> [!NOTE]
> Om du har en version av NuGet som är äldre än 2.8.5.201, uppmanas du att ladda ner och installera den senaste versionen av NuGet.

Modulen AzureRM är en sammanslagen modul för Azure Resource Manager-cmdletar. När du installerar AzureRM-modulen, kommer alla övriga Azure PowerShell-moduler som inte har installerats att laddas ner och installeras från PowerShell-galleriet.

Om du har en tidigare version av Azure PowerShell installerad så kan du få ett felmeddelande. För att lösa problemet kan du se avsnittet [uppdatera till en ny version av Azure PowerShell](#update-azps) i den här artikeln.

## <a name="step-3-load-the-azurerm-module"></a>Steg 3: Läs in AzureRM-modulen

När modulen har installerats måste du läsa in modulen i din PowerShell-session. Du bör göra det här i en normal (icke-förhöjd) PowerShell-session. Moduler läses in med `Import-Module`-cmdleten enligt följande:

```powershell-interactive
Import-Module -Name AzureRM
```

## <a name="next-steps"></a>Nästa steg

Mer information om hur du använder Azure PowerShell finns i följande artiklar:

* [Kom igång med Azure PowerShell](get-started-azureps.md)

## <a name="reporting-issues-and-feedback"></a>Rapportera problem och feedback

Om du stöter på några buggar med verktyget kan du rapportera problemet i [problem](https://github.com/Azure/azure-powershell/issues)-delen av vårt GitHub-repo. Om du vill ge feedback från kommandoraden, använder du cmdleten `Send-Feedback`.

## <a name="frequently-asked-questions"></a>Vanliga frågor och svar

### <a name="how-to-get-powershellget"></a>Hämta PowerShellGet

|OS-version|Installationsinstruktioner|
|---|---|
|Jag har Windows 10 eller Windows Server 2016|Inbyggt i Windows Management Framework (WMF) 5.0 som ingår i operativsystemet|
|Jag vill uppgradera till PowerShell 5|[Installera den senaste versionen av WMF](https://www.microsoft.com/en-us/download/details.aspx?id=54616)|
|Jag använder en Windows-version med PowerShell 3 eller PowerShell 4|[Hämta PackageManagement-moduler](http://go.microsoft.com/fwlink/?LinkID=746217)|

### <a name="div-idhelpmechoosechecking-the-version-of-azure-powershell"></a><div id="helpmechoose"/>Kontrollera Azure PowerShell-versionen

Det finns stöd för flera versioner av Azure PowerShell, men vi rekommenderar att du uppgraderar till den senaste versionen så snart som möjligt. Om du vill kontrollera vilken version av Azure PowerShell som du har installerat kör du `Get-Module AzureRM` från kommandoraden.

```powershell-interactive
Get-Module AzureRM -ListAvailable | Select-Object -Property Name,Version,Path
```

### <a name="support-for-classic-deployment-methods"></a>Stöd för klassiska distributionsmetoder

Om du har distributioner som använder den klassiska distributionsmodellen så kan du installera Service Management-versionen av Azure PowerShell. Läs mer i informationen om hur du [installerar Azure PowerShell Service Management-modulen](/powershell/azure/servicemanagement/install-azure-ps). Azure- och AzureRM-moduler delar gemensamma beroenden. Om du använder både Azure- och AzureRM-moduler, bör du installera samma version av varje paket.

### <a name="div-idupdate-azpsupdating-to-a-new-version-of-azure-powershell"></a><div id="update-azps"/>Uppdatera till en ny version av Azure PowerShell

Om du har en tidigare version av Azure PowerShell installerad som innehåller tjänsthanteringsmodulen, kan följande felmeddelande komma upp:

```Output
PackageManagement\Install-Package : A command with name 'Get-AzureStorageContainerAcl' is already
available on this system. This module 'Azure.Storage' may override the existing commands. If you
still want to install this module 'Azure.Storage', use -AllowClobber parameter.

At C:\Program Files\WindowsPowerShell\Modules\PowerShellGet\1.0.0.1\PSModule.psm1:1772 char:21
+ ...          $null = PackageManagement\Install-Package @PSBoundParameters
+                      ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
    + CategoryInfo          : InvalidOperation: (Microsoft.Power....InstallPackage:InstallPackage) [Install-Package], Exception
    + FullyQualifiedErrorId : CommandAlreadyAvailable,Validate-ModuleCommandAlreadyAvailable,Microsoft.PowerShell.PackageManagement.Cmdlets.InstallPackage
```

Precis som felmeddelandet säger så behöver du använda parametern -AllowClobber för att installera modulen. Ange följande kommando:

```powershell-interactive
# Install the Azure Resource Manager modules from the PowerShell Gallery
Install-Module -Name AzureRM -AllowClobber
```

Mer information finns i hjälpavsnittet för [Install-Module](https://msdn.microsoft.com/powershell/reference/5.1/PowerShellGet/install-module).

### <a name="installing-module-versions-side-by-side"></a>Installera modulversioner sida vid sida

PowerShellGet är den enda installationsmetoden som stöder installation av flera versioner. Du kan till exempel ha skript som är skrivna med en tidigare version av Azure PowerShell som du inte har tid eller resurser att uppdatera. Följande kommandon visar hur du installerar flera versioner av Azure PowerShell:

```powershell-interactive
Install-Module -Name AzureRM -RequiredVersion 3.7.0
Install-Module -Name AzureRM -RequiredVersion 2.3.0
```

Endast en version av modulen kan läsas in i en PowerShell-session. Du måste öppna ett nytt PowerShell-fönster och använda `Import-Module` för att importera en specifik version av AzureRM-cmdletarna:

```powershell-interactive
Import-Module -Name AzureRM -RequiredVersion 2.3.0
```

> [!NOTE]
> Version 2.1.0 och 1.2.6 är de första modulversionerna som är avsedda att installeras och användas sida vid sida. När du laddar en tidigare version av Azure PowerShell, laddas inkompatibla versioner av modulen **AzureRM.Profile**. Det gör att cmdletarna ber dig logga in när du kör en av dem.

### <a name="other-installation-methods"></a>Andra installationsmetoder

Information om hur du installerar med hjälp av installationsprogrammet för webbplattform eller MSI-paketet finns [Andra installationsmetoder](other-install.md)
