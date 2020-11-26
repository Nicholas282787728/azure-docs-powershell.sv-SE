---
external help file: ''
Module Name: Az.ImportExport
online version: https://docs.microsoft.com/en-us/powershell/module/az.importexport/get-azimportexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Get-AzImportExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Get-AzImportExport.md
ms.openlocfilehash: 13c5a7104c0b9d2d4e11e4fe0a2da772ee271c4c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94260473"
---
# <span data-ttu-id="6d4e2-101">Get-AzImportExport</span><span class="sxs-lookup"><span data-stu-id="6d4e2-101">Get-AzImportExport</span></span>

## <span data-ttu-id="6d4e2-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6d4e2-102">SYNOPSIS</span></span>
<span data-ttu-id="6d4e2-103">Hämtar information om ett befintligt jobb.</span><span class="sxs-lookup"><span data-stu-id="6d4e2-103">Gets information about an existing job.</span></span>

## <span data-ttu-id="6d4e2-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6d4e2-104">SYNTAX</span></span>

### <span data-ttu-id="6d4e2-105">Lista (standard)</span><span class="sxs-lookup"><span data-stu-id="6d4e2-105">List (Default)</span></span>
```
Get-AzImportExport [-SubscriptionId <String[]>] [-Filter <String>] [-Top <Int32>] [-AcceptLanguage <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="6d4e2-106">Lära</span><span class="sxs-lookup"><span data-stu-id="6d4e2-106">Get</span></span>
```
Get-AzImportExport -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-AcceptLanguage <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="6d4e2-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="6d4e2-107">GetViaIdentity</span></span>
```
Get-AzImportExport -InputObject <IImportExportIdentity> [-AcceptLanguage <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="6d4e2-108">List1</span><span class="sxs-lookup"><span data-stu-id="6d4e2-108">List1</span></span>
```
Get-AzImportExport -ResourceGroupName <String> [-SubscriptionId <String[]>] [-Filter <String>] [-Top <Int32>]
 [-AcceptLanguage <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="6d4e2-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6d4e2-109">DESCRIPTION</span></span>
<span data-ttu-id="6d4e2-110">Hämtar information om ett befintligt jobb.</span><span class="sxs-lookup"><span data-stu-id="6d4e2-110">Gets information about an existing job.</span></span>

## <span data-ttu-id="6d4e2-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6d4e2-111">EXAMPLES</span></span>

### <span data-ttu-id="6d4e2-112">Exempel 1: få ImportExport-jobbet med standard kontext</span><span class="sxs-lookup"><span data-stu-id="6d4e2-112">Example 1: Get ImportExport job with default context</span></span>
```powershell
PS C:\> Get-AzImportExport
Location Name     Type
-------- ----     ----
East US  test-job Microsoft.ImportExport/jobs
```

<span data-ttu-id="6d4e2-113">Denna cmdlet hämtar ImportExport jobb med standard kontext.</span><span class="sxs-lookup"><span data-stu-id="6d4e2-113">This cmdlet gets ImportExport job with default context.</span></span>

### <span data-ttu-id="6d4e2-114">Exempel 2: Hämta ImportExport-jobbet efter resurs grupp och jobbnamn</span><span class="sxs-lookup"><span data-stu-id="6d4e2-114">Example 2: Get ImportExport job by resource group and job name</span></span>
```powershell
PS C:\> Get-AzImportExport -Name test-job -ResourceGroupName ImportTestRG
Location Name     Type
-------- ----     ----
East US  test-job Microsoft.ImportExport/jobs
```

<span data-ttu-id="6d4e2-115">Denna cmdlet hämtar ImportExport-jobbet efter resurs grupp och jobbnamn.</span><span class="sxs-lookup"><span data-stu-id="6d4e2-115">This cmdlet gets ImportExport job by resource group and job name.</span></span>

### <span data-ttu-id="6d4e2-116">Exempel 3: visar alla ImportExport-jobb i angiven resurs grupp</span><span class="sxs-lookup"><span data-stu-id="6d4e2-116">Example 3: Lists all the ImportExport jobs in specified resource group</span></span>
```powershell
PS C:\> Get-AzImportExport -ResourceGroupName ImportTestRG
Location Name     Type
-------- ----     ----
East US  test-job Microsoft.ImportExport/jobs
```

<span data-ttu-id="6d4e2-117">Denna cmdlet visar alla ImportExport-jobb i angiven resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="6d4e2-117">This cmdlet lists all the ImportExport jobs in specified resource group.</span></span>

### <span data-ttu-id="6d4e2-118">Exempel 4: Hämta ImportExport-jobbet efter identitet</span><span class="sxs-lookup"><span data-stu-id="6d4e2-118">Example 4: Get ImportExport job by identity</span></span>
```powershell
PS C:\> $Id = "/subscriptions/<SubscriptionId>/resourceGroups/ImportTestRG/providers/Microsoft.ImportExport/jobs/test-job"
PS C:\> Get-AzImportExport -InputObject $Id
Location Name     Type
-------- ----     ----
East US  test-job Microsoft.ImportExport/jobs
```

<span data-ttu-id="6d4e2-119">Med denna cmdlet-lista får du ImportExport jobb efter identitet.</span><span class="sxs-lookup"><span data-stu-id="6d4e2-119">This cmdlet lists gets ImportExport job by identity.</span></span>

## <span data-ttu-id="6d4e2-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6d4e2-120">PARAMETERS</span></span>

### <span data-ttu-id="6d4e2-121">-AcceptLanguage</span><span class="sxs-lookup"><span data-stu-id="6d4e2-121">-AcceptLanguage</span></span>
<span data-ttu-id="6d4e2-122">Anger önskat språk för svaret.</span><span class="sxs-lookup"><span data-stu-id="6d4e2-122">Specifies the preferred language for the response.</span></span>

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

### <span data-ttu-id="6d4e2-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d4e2-123">-DefaultProfile</span></span>
<span data-ttu-id="6d4e2-124">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="6d4e2-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6d4e2-125">-Filter</span><span class="sxs-lookup"><span data-stu-id="6d4e2-125">-Filter</span></span>
<span data-ttu-id="6d4e2-126">Kan användas för att begränsa resultatet till vissa villkor.</span><span class="sxs-lookup"><span data-stu-id="6d4e2-126">Can be used to restrict the results to certain conditions.</span></span>

```yaml
Type: System.String
Parameter Sets: List, List1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d4e2-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6d4e2-127">-InputObject</span></span>
<span data-ttu-id="6d4e2-128">Identitets parameter för att konstruera, se avsnittet anteckningar för INPUTOBJECT-egenskaper och skapa en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="6d4e2-128">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="6d4e2-129">-Namn</span><span class="sxs-lookup"><span data-stu-id="6d4e2-129">-Name</span></span>
<span data-ttu-id="6d4e2-130">Namnet på import-och export jobbet.</span><span class="sxs-lookup"><span data-stu-id="6d4e2-130">The name of the import/export job.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: JobName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d4e2-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6d4e2-131">-ResourceGroupName</span></span>
<span data-ttu-id="6d4e2-132">Resurs gruppens namn identifierar unikt resurs gruppen i användar abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="6d4e2-132">The resource group name uniquely identifies the resource group within the user subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List1
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d4e2-133">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6d4e2-133">-SubscriptionId</span></span>
<span data-ttu-id="6d4e2-134">Abonnemangs-ID för Azure-användaren.</span><span class="sxs-lookup"><span data-stu-id="6d4e2-134">The subscription ID for the Azure user.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List, List1
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d4e2-135">-Överst</span><span class="sxs-lookup"><span data-stu-id="6d4e2-135">-Top</span></span>
<span data-ttu-id="6d4e2-136">Ett heltals värde som anger hur många jobb som bäst ska returneras.</span><span class="sxs-lookup"><span data-stu-id="6d4e2-136">An integer value that specifies how many jobs at most should be returned.</span></span>
<span data-ttu-id="6d4e2-137">Värdet får inte överstiga 100.</span><span class="sxs-lookup"><span data-stu-id="6d4e2-137">The value cannot exceed 100.</span></span>

```yaml
Type: System.Int32
Parameter Sets: List, List1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d4e2-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d4e2-138">CommonParameters</span></span>
<span data-ttu-id="6d4e2-139">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6d4e2-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d4e2-140">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6d4e2-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d4e2-141">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6d4e2-141">INPUTS</span></span>

### <span data-ttu-id="6d4e2-142">Microsoft. Azure. PowerShell. cmdletar. ImportExport. Models. IImportExportIdentity</span><span class="sxs-lookup"><span data-stu-id="6d4e2-142">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.IImportExportIdentity</span></span>

## <span data-ttu-id="6d4e2-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6d4e2-143">OUTPUTS</span></span>

### <span data-ttu-id="6d4e2-144">Microsoft. Azure. PowerShell. cmdletar. ImportExport. Models. Api20161101. IJobResponse</span><span class="sxs-lookup"><span data-stu-id="6d4e2-144">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.Api20161101.IJobResponse</span></span>

## <span data-ttu-id="6d4e2-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6d4e2-145">NOTES</span></span>

<span data-ttu-id="6d4e2-146">ALIAS</span><span class="sxs-lookup"><span data-stu-id="6d4e2-146">ALIASES</span></span>

<span data-ttu-id="6d4e2-147">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="6d4e2-147">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="6d4e2-148">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="6d4e2-148">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="6d4e2-149">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="6d4e2-149">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="6d4e2-150">INPUTOBJECT <IImportExportIdentity> : identitets parameter</span><span class="sxs-lookup"><span data-stu-id="6d4e2-150">INPUTOBJECT <IImportExportIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="6d4e2-151">`[Id <String>]`: Sökväg till resurs identitet</span><span class="sxs-lookup"><span data-stu-id="6d4e2-151">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="6d4e2-152">`[JobName <String>]`: Import-och export jobbets namn.</span><span class="sxs-lookup"><span data-stu-id="6d4e2-152">`[JobName <String>]`: The name of the import/export job.</span></span>
  - <span data-ttu-id="6d4e2-153">`[LocationName <String>]`: Namnet på platsen.</span><span class="sxs-lookup"><span data-stu-id="6d4e2-153">`[LocationName <String>]`: The name of the location.</span></span> <span data-ttu-id="6d4e2-154">Till exempel West, USA eller västkusten.</span><span class="sxs-lookup"><span data-stu-id="6d4e2-154">For example, West US or westus.</span></span>
  - <span data-ttu-id="6d4e2-155">`[ResourceGroupName <String>]`: Resurs grupp namnet identifierar unikt resurs gruppen i användar abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="6d4e2-155">`[ResourceGroupName <String>]`: The resource group name uniquely identifies the resource group within the user subscription.</span></span>
  - <span data-ttu-id="6d4e2-156">`[SubscriptionId <String>]`: Prenumerations-ID för Azure-användaren.</span><span class="sxs-lookup"><span data-stu-id="6d4e2-156">`[SubscriptionId <String>]`: The subscription ID for the Azure user.</span></span>

## <span data-ttu-id="6d4e2-157">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6d4e2-157">RELATED LINKS</span></span>
