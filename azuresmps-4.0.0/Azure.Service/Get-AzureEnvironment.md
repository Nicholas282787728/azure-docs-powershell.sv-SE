---
external help file: Microsoft.WindowsAzure.Commands.Profile.dll-Help.xml
ms.assetid: BF5E3E1A-14B6-4630-8168-628057009D5E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 284d1601746254b2e10fdfe042e5882e94ca1bd9
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099582"
---
# <span data-ttu-id="0003e-101">Get-AzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="0003e-101">Get-AzureEnvironment</span></span>

## <span data-ttu-id="0003e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0003e-102">SYNOPSIS</span></span>
<span data-ttu-id="0003e-103">Hämtar Azure-miljöer</span><span class="sxs-lookup"><span data-stu-id="0003e-103">Gets Azure environments</span></span>

## <span data-ttu-id="0003e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0003e-104">SYNTAX</span></span>

```
Get-AzureEnvironment [-Name <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="0003e-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0003e-105">DESCRIPTION</span></span>
<span data-ttu-id="0003e-106">Cmdleten **Get-AzureEnvironment** hämtar Azure-miljörna som är tillgängliga för Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="0003e-106">The **Get-AzureEnvironment** cmdlet gets the Azure environments that are available to Windows PowerShell.</span></span>

<span data-ttu-id="0003e-107">En Azure-miljö en oberoende distribution av Microsoft Azure, till exempel AzureCloud för globala Azure-och AzureChinaCloud för Azure som drivs av 21Vianet i Kina.</span><span class="sxs-lookup"><span data-stu-id="0003e-107">An Azure environment an independent deployment of Microsoft Azure, such as AzureCloud for global Azure and AzureChinaCloud for Azure operated by 21Vianet in China.</span></span>
<span data-ttu-id="0003e-108">Du kan också skapa lokala Azure-miljöer med Azure Pack och WAPack cmdlets.</span><span class="sxs-lookup"><span data-stu-id="0003e-108">You can also create on-premises Azure environments by using Azure Pack and the WAPack cmdlets.</span></span>
<span data-ttu-id="0003e-109">Mer information finns i [Azure Pack](https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx)  ( https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx) .</span><span class="sxs-lookup"><span data-stu-id="0003e-109">For more information, see [Azure Pack](https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx)  (https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx).</span></span>

<span data-ttu-id="0003e-110">Cmdleten **Get-AzureEnvironment** hämtar miljöer från din prenumerations data fil, inte från Azure.</span><span class="sxs-lookup"><span data-stu-id="0003e-110">The **Get-AzureEnvironment** cmdlet gets environments from your subscription data file, not from Azure.</span></span>
<span data-ttu-id="0003e-111">Om prenumerations data filen är inaktuell kör du cmdleten **Add-AzureAccount** eller **import-PublishSettingsFile** för att uppdatera den.</span><span class="sxs-lookup"><span data-stu-id="0003e-111">If the subscription data file is outdated, run the **Add-AzureAccount** or **Import-PublishSettingsFile** cmdlet to refresh it.</span></span>

<span data-ttu-id="0003e-112">I det här avsnittet beskrivs cmdleten i 0.8.10-versionen av Microsoft Azure PowerShell-modulen.</span><span class="sxs-lookup"><span data-stu-id="0003e-112">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="0003e-113">För att få den version av modulen du använder, gå till Azure PowerShell-konsolen och skriv `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="0003e-113">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

## <span data-ttu-id="0003e-114">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0003e-114">EXAMPLES</span></span>

### <span data-ttu-id="0003e-115">Exempel 1: Hämta alla miljöer</span><span class="sxs-lookup"><span data-stu-id="0003e-115">Example 1: Get all environments</span></span>
```
PS C:\> Get-AzureEnvironment

EnvironmentName               ServiceEndpoint               ResourceManagerEndpoint       PublishSettingsFileUrl
---------------               ---------------               -----------------------       ----------------------

AzureCloud                    https://management.core.wi... https://management.azure.com/ https://go.microsoft.com/fw... 
AzureChinaCloud               https://management.core.ch... https://not-supported-serv... https://go.microsoft.com/fw...
```

<span data-ttu-id="0003e-116">Det här kommandot får alla miljöer som är tillgängliga för Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="0003e-116">This command gets all environments that are available to Windows PowerShell.</span></span>

### <span data-ttu-id="0003e-117">Exempel 2: skaffa en miljö med namn</span><span class="sxs-lookup"><span data-stu-id="0003e-117">Example 2: Get an environment by name</span></span>
```
PS C:\> Get-AzureEnvironment -Name AzureCloud

Name                          : AzureCloud

PublishSettingsFileUrl        : https://go.microsoft.com/fwlink/?LinkID=301775

ServiceEndpoint               : https://management.core.windows.net/

ResourceManagerEndpoint       : https://management.azure.com/

ManagementPortalUrl           : https://go.microsoft.com/fwlink/?LinkId=254433

ActiveDirectoryEndpoint       : https://login.windows.net/

ActiveDirectoryCommonTenantId : common

StorageEndpointSuffix         : core.windows.net

StorageBlobEndpointFormat     : {0}://{1}.blob.core.windows.net/

StorageQueueEndpointFormat    : {0}://{1}.queue.core.windows.net/

StorageTableEndpointFormat    : {0}://{1}.table.core.windows.net/

GalleryEndpoint               : https://gallery.azure.com/
```

<span data-ttu-id="0003e-118">Det här exemplet får du AzureCloud-miljön.</span><span class="sxs-lookup"><span data-stu-id="0003e-118">This example gets the AzureCloud environment.</span></span>

### <span data-ttu-id="0003e-119">Exempel 3: Hämta alla egenskaper för alla miljöer</span><span class="sxs-lookup"><span data-stu-id="0003e-119">Example 3: Get all properties of all environments</span></span>
```
PS C:\> Get-AzureEnvironment | ForEach-Object {Get-AzureEnvironment -Name $_.EnvironmentName}
```

<span data-ttu-id="0003e-120">Det här kommandot får alla egenskaper i alla miljöer.</span><span class="sxs-lookup"><span data-stu-id="0003e-120">This command gets all properties of all environments.</span></span>

<span data-ttu-id="0003e-121">Kommandot använder cmdleten **Get-AzureEnvironment** för att hämta alla Azure-miljöer för det här kontot.</span><span class="sxs-lookup"><span data-stu-id="0003e-121">The command uses the **Get-AzureEnvironment** cmdlet to get all Azure environments for this account.</span></span>
<span data-ttu-id="0003e-122">Sedan använder den **förgrunds-objekt-** cmdleten för att köra kommandot **Get-AzureEnvironment** med parametern **Name** i varje miljö.</span><span class="sxs-lookup"><span data-stu-id="0003e-122">Then, it uses the **Foreach-Object** cmdlet to run a **Get-AzureEnvironment** command with the **Name** parameter on each environment.</span></span>
<span data-ttu-id="0003e-123">Värdet på parametern **Name** är egenskapen **EnvironmentName** för varje miljö.</span><span class="sxs-lookup"><span data-stu-id="0003e-123">The value of the **Name** parameter is the **EnvironmentName** property of each environment.</span></span>

<span data-ttu-id="0003e-124">Utan parametrar får **Get-AzureEnvironment** endast valda egenskaper för en miljö.</span><span class="sxs-lookup"><span data-stu-id="0003e-124">Without parameters, **Get-AzureEnvironment** gets only selected properties of an environment.</span></span>

## <span data-ttu-id="0003e-125">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0003e-125">PARAMETERS</span></span>

### <span data-ttu-id="0003e-126">-Namn</span><span class="sxs-lookup"><span data-stu-id="0003e-126">-Name</span></span>
<span data-ttu-id="0003e-127">Hämtar endast den angivna miljön.</span><span class="sxs-lookup"><span data-stu-id="0003e-127">Gets only the specified environment.</span></span>
<span data-ttu-id="0003e-128">Skriv miljö namnet.</span><span class="sxs-lookup"><span data-stu-id="0003e-128">Type the environment name.</span></span>
<span data-ttu-id="0003e-129">Parametervärdet är Skift läges känsligt.</span><span class="sxs-lookup"><span data-stu-id="0003e-129">The parameter value is case-sensitive.</span></span>
<span data-ttu-id="0003e-130">Jokertecken är inte tillåtna.</span><span class="sxs-lookup"><span data-stu-id="0003e-130">Wildcard characters are not permitted.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0003e-131">-Profil</span><span class="sxs-lookup"><span data-stu-id="0003e-131">-Profile</span></span>
<span data-ttu-id="0003e-132">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="0003e-132">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="0003e-133">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="0003e-133">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0003e-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0003e-134">CommonParameters</span></span>
<span data-ttu-id="0003e-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0003e-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0003e-136">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0003e-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0003e-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0003e-137">INPUTS</span></span>

### <span data-ttu-id="0003e-138">Ingen</span><span class="sxs-lookup"><span data-stu-id="0003e-138">None</span></span>
<span data-ttu-id="0003e-139">Du kan ange indata för denna cmdlet efter egenskaps namn, men inte efter värde.</span><span class="sxs-lookup"><span data-stu-id="0003e-139">You can pipe input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="0003e-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0003e-140">OUTPUTS</span></span>

### <span data-ttu-id="0003e-141">System. Management. Automation. PSCustomObject</span><span class="sxs-lookup"><span data-stu-id="0003e-141">System.Management.Automation.PSCustomObject</span></span>
<span data-ttu-id="0003e-142">Som standard returnerar **Get-AzureEnvironment** ett anpassat objekt.</span><span class="sxs-lookup"><span data-stu-id="0003e-142">By default, **Get-AzureEnvironment** returns a custom object.</span></span>

### <span data-ttu-id="0003e-143">Microsoft. WindowsAzure. commands. Utilitiess. Common. WindowsAzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="0003e-143">Microsoft.WindowsAzure.Commands.Utilities.Common.WindowsAzureEnvironment</span></span>
<span data-ttu-id="0003e-144">När du kör **Get-AzureEnvironment** med parametern **Name** returnerar den ett  **WindowsAzureEnvironment** -objekt.</span><span class="sxs-lookup"><span data-stu-id="0003e-144">When you run **Get-AzureEnvironment** with the **Name** parameter, it returns a  **WindowsAzureEnvironment** object.</span></span>

## <span data-ttu-id="0003e-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0003e-145">NOTES</span></span>

## <span data-ttu-id="0003e-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0003e-146">RELATED LINKS</span></span>

[<span data-ttu-id="0003e-147">Add-AzureAccount</span><span class="sxs-lookup"><span data-stu-id="0003e-147">Add-AzureAccount</span></span>](./Add-AzureAccount.md)

[<span data-ttu-id="0003e-148">Add-AzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="0003e-148">Add-AzureEnvironment</span></span>](./Add-AzureEnvironment.md)

[<span data-ttu-id="0003e-149">Get-AzurePublishSettingsFile</span><span class="sxs-lookup"><span data-stu-id="0003e-149">Get-AzurePublishSettingsFile</span></span>](./Get-AzurePublishSettingsFile.md)

[<span data-ttu-id="0003e-150">Import-AzurePublishSettingsFile</span><span class="sxs-lookup"><span data-stu-id="0003e-150">Import-AzurePublishSettingsFile</span></span>](./Import-AzurePublishSettingsFile.md)

[<span data-ttu-id="0003e-151">Remove-AzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="0003e-151">Remove-AzureEnvironment</span></span>](./Remove-AzureEnvironment.md)

[<span data-ttu-id="0003e-152">Set-AzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="0003e-152">Set-AzureEnvironment</span></span>](./Set-AzureEnvironment.md)


