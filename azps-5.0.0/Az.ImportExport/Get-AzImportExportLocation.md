---
external help file: ''
Module Name: Az.ImportExport
online version: https://docs.microsoft.com/en-us/powershell/module/az.importexport/get-azimportexportlocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Get-AzImportExportLocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Get-AzImportExportLocation.md
ms.openlocfilehash: c603c01619128d1697256174e9d0bc00a1cea8ff
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94319496"
---
# <span data-ttu-id="f2a6a-101">Get-AzImportExportLocation</span><span class="sxs-lookup"><span data-stu-id="f2a6a-101">Get-AzImportExportLocation</span></span>

## <span data-ttu-id="f2a6a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f2a6a-102">SYNOPSIS</span></span>
<span data-ttu-id="f2a6a-103">Returnerar informationen om en plats där du kan leverera de diskar som är associerade med ett import-eller export jobb.</span><span class="sxs-lookup"><span data-stu-id="f2a6a-103">Returns the details about a location to which you can ship the disks associated with an import or export job.</span></span>
<span data-ttu-id="f2a6a-104">En plats är ett Azure-område.</span><span class="sxs-lookup"><span data-stu-id="f2a6a-104">A location is an Azure region.</span></span>

## <span data-ttu-id="f2a6a-105">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f2a6a-105">SYNTAX</span></span>

### <span data-ttu-id="f2a6a-106">Lista (standard)</span><span class="sxs-lookup"><span data-stu-id="f2a6a-106">List (Default)</span></span>
```
Get-AzImportExportLocation [-AcceptLanguage <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="f2a6a-107">Lära</span><span class="sxs-lookup"><span data-stu-id="f2a6a-107">Get</span></span>
```
Get-AzImportExportLocation -Name <String> [-AcceptLanguage <String>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="f2a6a-108">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="f2a6a-108">GetViaIdentity</span></span>
```
Get-AzImportExportLocation -InputObject <IImportExportIdentity> [-AcceptLanguage <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="f2a6a-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f2a6a-109">DESCRIPTION</span></span>
<span data-ttu-id="f2a6a-110">Returnerar informationen om en plats där du kan leverera de diskar som är associerade med ett import-eller export jobb.</span><span class="sxs-lookup"><span data-stu-id="f2a6a-110">Returns the details about a location to which you can ship the disks associated with an import or export job.</span></span>
<span data-ttu-id="f2a6a-111">En plats är ett Azure-område.</span><span class="sxs-lookup"><span data-stu-id="f2a6a-111">A location is an Azure region.</span></span>

## <span data-ttu-id="f2a6a-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f2a6a-112">EXAMPLES</span></span>

### <span data-ttu-id="f2a6a-113">Exempel 1: Hämta alla Azure regions plats uppgifter med standard kontext</span><span class="sxs-lookup"><span data-stu-id="f2a6a-113">Example 1: Get all Azure region location details with default context</span></span>
```powershell
PS C:\> Get-AzImportExportLocation
Name                 Type
----                 ----
Australia East       Microsoft.ImportExport/locations
Australia Southeast  Microsoft.ImportExport/locations
Brazil South         Microsoft.ImportExport/locations
Canada Central       Microsoft.ImportExport/locations
Canada East          Microsoft.ImportExport/locations
...
West Central US      Microsoft.ImportExport/locations
West Europe          Microsoft.ImportExport/locations
West India           Microsoft.ImportExport/locations
West US              Microsoft.ImportExport/locations
West US 2            Microsoft.ImportExport/locations
```

<span data-ttu-id="f2a6a-114">Denna cmdlet får alla Azure region plats uppgifter med standard kontext.</span><span class="sxs-lookup"><span data-stu-id="f2a6a-114">This cmdlet gets all Azure region location details with default context.</span></span>

### <span data-ttu-id="f2a6a-115">Exempel 2: Hämta plats information för Azure region med plats namn</span><span class="sxs-lookup"><span data-stu-id="f2a6a-115">Example 2: Get Azure region location details by location name</span></span>
```powershell
PS C:\> Get-AzImportExportLocation -Name eastus
Name    Type
----    ----
East US Microsoft.ImportExport/locations
```

<span data-ttu-id="f2a6a-116">Denna cmdlet hämtar Azure region plats uppgifter efter plats namn.</span><span class="sxs-lookup"><span data-stu-id="f2a6a-116">This cmdlet gets Azure region location details by location name.</span></span>

### <span data-ttu-id="f2a6a-117">Exempel 3: skaffa plats uppgifter för Azure region efter identitet</span><span class="sxs-lookup"><span data-stu-id="f2a6a-117">Example 3: Get Azure region location details by identity</span></span>
```powershell
PS C:\> $Id = "/providers/Microsoft.ImportExport/locations/eastus"
PS C:\> Get-AzImportExportLocation -InputObject $Id
Name    Type
----    ----
East US Microsoft.ImportExport/locations
```

<span data-ttu-id="f2a6a-118">I den här cmdleten får du information om Azure regions plats för identiteten.</span><span class="sxs-lookup"><span data-stu-id="f2a6a-118">This cmdlet lists gets Azure region location details by identity.</span></span>

## <span data-ttu-id="f2a6a-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f2a6a-119">PARAMETERS</span></span>

### <span data-ttu-id="f2a6a-120">-AcceptLanguage</span><span class="sxs-lookup"><span data-stu-id="f2a6a-120">-AcceptLanguage</span></span>
<span data-ttu-id="f2a6a-121">Anger önskat språk för svaret.</span><span class="sxs-lookup"><span data-stu-id="f2a6a-121">Specifies the preferred language for the response.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2a6a-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2a6a-122">-DefaultProfile</span></span>
<span data-ttu-id="f2a6a-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f2a6a-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2a6a-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f2a6a-124">-InputObject</span></span>
<span data-ttu-id="f2a6a-125">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="f2a6a-125">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.IImportExportIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f2a6a-126">-Namn</span><span class="sxs-lookup"><span data-stu-id="f2a6a-126">-Name</span></span>
<span data-ttu-id="f2a6a-127">Namnet på platsen.</span><span class="sxs-lookup"><span data-stu-id="f2a6a-127">The name of the location.</span></span>
<span data-ttu-id="f2a6a-128">Till exempel West, USA eller västkusten.</span><span class="sxs-lookup"><span data-stu-id="f2a6a-128">For example, West US or westus.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: LocationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2a6a-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2a6a-129">CommonParameters</span></span>
<span data-ttu-id="f2a6a-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f2a6a-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2a6a-131">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f2a6a-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2a6a-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f2a6a-132">INPUTS</span></span>

### <span data-ttu-id="f2a6a-133">Microsoft. Azure. PowerShell. cmdletar. ImportExport. Models. IImportExportIdentity</span><span class="sxs-lookup"><span data-stu-id="f2a6a-133">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.IImportExportIdentity</span></span>

## <span data-ttu-id="f2a6a-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f2a6a-134">OUTPUTS</span></span>

### <span data-ttu-id="f2a6a-135">Microsoft. Azure. PowerShell. cmdletar. ImportExport. Models. Api20161101. ILocation</span><span class="sxs-lookup"><span data-stu-id="f2a6a-135">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.Api20161101.ILocation</span></span>

## <span data-ttu-id="f2a6a-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f2a6a-136">NOTES</span></span>

<span data-ttu-id="f2a6a-137">ALIAS</span><span class="sxs-lookup"><span data-stu-id="f2a6a-137">ALIASES</span></span>

<span data-ttu-id="f2a6a-138">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="f2a6a-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="f2a6a-139">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="f2a6a-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="f2a6a-140">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="f2a6a-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="f2a6a-141">INPUTOBJECT <IImportExportIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="f2a6a-141">INPUTOBJECT <IImportExportIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="f2a6a-142">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="f2a6a-142">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="f2a6a-143">`[JobName <String>]`: Import-och export jobbets namn.</span><span class="sxs-lookup"><span data-stu-id="f2a6a-143">`[JobName <String>]`: The name of the import/export job.</span></span>
  - <span data-ttu-id="f2a6a-144">`[LocationName <String>]`: Namnet på platsen.</span><span class="sxs-lookup"><span data-stu-id="f2a6a-144">`[LocationName <String>]`: The name of the location.</span></span> <span data-ttu-id="f2a6a-145">Till exempel West, USA eller västkusten.</span><span class="sxs-lookup"><span data-stu-id="f2a6a-145">For example, West US or westus.</span></span>
  - <span data-ttu-id="f2a6a-146">`[ResourceGroupName <String>]`: Resurs grupp namnet identifierar unikt resurs gruppen i användar abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="f2a6a-146">`[ResourceGroupName <String>]`: The resource group name uniquely identifies the resource group within the user subscription.</span></span>
  - <span data-ttu-id="f2a6a-147">`[SubscriptionId <String>]`: Prenumerations-ID för Azure-användaren.</span><span class="sxs-lookup"><span data-stu-id="f2a6a-147">`[SubscriptionId <String>]`: The subscription ID for the Azure user.</span></span>

## <span data-ttu-id="f2a6a-148">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f2a6a-148">RELATED LINKS</span></span>

