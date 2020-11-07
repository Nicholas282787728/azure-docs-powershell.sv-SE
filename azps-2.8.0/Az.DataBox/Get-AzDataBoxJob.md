---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBox.dll-Help.xml
Module Name: Az.DataBox
online version: https://docs.microsoft.com/en-us/powershell/module/az.databox/get-azdataboxjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBox/DataBox/help/Get-AzDataBoxJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBox/DataBox/help/Get-AzDataBoxJob.md
ms.openlocfilehash: 9bb1fdd02b77a530f6bf4d8ea47a041f22e38b48
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93744828"
---
# <span data-ttu-id="9958a-101">Get-AzDataBoxJob</span><span class="sxs-lookup"><span data-stu-id="9958a-101">Get-AzDataBoxJob</span></span>

## <span data-ttu-id="9958a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9958a-102">SYNOPSIS</span></span>
<span data-ttu-id="9958a-103">Hämtar information om datavyer</span><span class="sxs-lookup"><span data-stu-id="9958a-103">Gets information about Databox Jobs</span></span>

## <span data-ttu-id="9958a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9958a-104">SYNTAX</span></span>

### <span data-ttu-id="9958a-105">ListParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="9958a-105">ListParameterSet (Default)</span></span>
```
Get-AzDataBoxJob [-ResourceGroupName <String>] [-Completed] [-CompletedWithError] [-Cancelled] [-Aborted]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9958a-106">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="9958a-106">GetByNameParameterSet</span></span>
```
Get-AzDataBoxJob -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9958a-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9958a-107">GetByResourceIdParameterSet</span></span>
```
Get-AzDataBoxJob -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9958a-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9958a-108">DESCRIPTION</span></span>
<span data-ttu-id="9958a-109">Cmdleten **Get-AzDataBoxJobs** hämtar information om DataList jobb i en Azure-prenumeration.</span><span class="sxs-lookup"><span data-stu-id="9958a-109">The **Get-AzDataBoxJobs** cmdlet gets information about databox jobs in an Azure subscription.</span></span>
<span data-ttu-id="9958a-110">Om du anger resurs gruppen får denna cmdlet alla data i den resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="9958a-110">If you specify the Resource Group, this cmdlet gets all the databox jobs under that resource group.</span></span> <span data-ttu-id="9958a-111">Om du anger namnet på jobbet tillsammans med resurs grupp namnet får denna cmdlet information om det specifika datamappen.</span><span class="sxs-lookup"><span data-stu-id="9958a-111">If you specify the Name of the job along with the resource group name, this cmdlet gets information about that specific databox job.</span></span>
<span data-ttu-id="9958a-112">Om du inte anger något annat än prenumerations-ID får den här cmdleten information om alla datamappen under det abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="9958a-112">If you do not specify anything other than subscription id, this cmdlet gets information about all of the databox jobs under that subscription.</span></span>

## <span data-ttu-id="9958a-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9958a-113">EXAMPLES</span></span>

### <span data-ttu-id="9958a-114">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="9958a-114">Example 1</span></span>
```powershell
PS C:\> Get-AzDataBoxJob

jobResource.Name        jobResource.Sku.Name jobResource.Status  jobResource.StartTime jobResource.Location ResourceGroup
----------------        -------------------- ------------------  --------------------- -------------------- -------------
testtip2                DataBox              Cancelled           10-09-2018 06:34:53   westus               TestRg1
cleanbox                DataBox              Aborted             04-12-2018 16:07:41   westus               TestRg2
cleanbox-Clone          DataBox              Cancelled           25-04-2019 11:31:36   westus               TestRg2
.
.
.
```

<span data-ttu-id="9958a-115">Get-AzDataBoxJob utan parameter hämtas alla data i jobben under prenumerationen</span><span class="sxs-lookup"><span data-stu-id="9958a-115">Get-AzDataBoxJob without any parameter fetches all the databox jobs under the subscription</span></span>

### <span data-ttu-id="9958a-116">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="9958a-116">Example 2</span></span>
```powershell
PS C:\> Get-AzDataBoxJob -ResourceGroupName TestRg1

jobResource.Name        jobResource.Sku.Name jobResource.Status  jobResource.StartTime jobResource.Location ResourceGroup
----------------        -------------------- ------------------  --------------------- -------------------- -------------
testtip2                DataBox              Cancelled           10-09-2018 06:34:53   westus               TestRg1
.
.
.
```

<span data-ttu-id="9958a-117">Get-AzDataBoxJob med ResourceGroupName parameter hämtar alla data i jobben under den angivna resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="9958a-117">Get-AzDataBoxJob with ResourceGroupName parameter fetches all the databox jobs under the specified resource group</span></span>

### <span data-ttu-id="9958a-118">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="9958a-118">Example 3</span></span>
```powershell
PS C:\> Get-AzDataBoxJob -ResourceGroupName TestRg1 -Name testtip2

jobResource.Name        jobResource.Sku.Name jobResource.Status  jobResource.StartTime jobResource.Location ResourceGroup
----------------        -------------------- ------------------  --------------------- -------------------- -------------
testtip2                DataBox              Cancelled           10-09-2018 06:34:53   westus               TestRg1

```

<span data-ttu-id="9958a-119">Get-AzDataBoxJob med ResourceGroupName och namnet som anges hämtas det specifika datajob-jobbet</span><span class="sxs-lookup"><span data-stu-id="9958a-119">Get-AzDataBoxJob with ResourceGroupName and Name specified will fetch that specific databox job</span></span>

### <span data-ttu-id="9958a-120">Exempel 4</span><span class="sxs-lookup"><span data-stu-id="9958a-120">Example 4</span></span>
```powershell
PS C:\> Get-AzDataBoxJob -ResourceId "/subscriptions/05b5dd1c-793d-41de-be9f-6f9ed142f695/resourceGroups/TestRg1/providers/Microsoft.DataBox/jobs/testtip2"

jobResource.Name        jobResource.Sku.Name jobResource.Status  jobResource.StartTime jobResource.Location ResourceGroup
----------------        -------------------- ------------------  --------------------- -------------------- -------------
testtip2                DataBox              Cancelled           10-09-2018 06:34:53   westus               TestRg1

```

<span data-ttu-id="9958a-121">Get-AzDataBoxJob med ResourceId kan du hämta det specifika datajob-jobbet</span><span class="sxs-lookup"><span data-stu-id="9958a-121">Get-AzDataBoxJob with ResourceId specified will fetch that specific databox job</span></span>

## <span data-ttu-id="9958a-122">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9958a-122">PARAMETERS</span></span>

### <span data-ttu-id="9958a-123">-Avbruten</span><span class="sxs-lookup"><span data-stu-id="9958a-123">-Aborted</span></span>
<span data-ttu-id="9958a-124">Växla parameter för att hämta avbrutna jobb</span><span class="sxs-lookup"><span data-stu-id="9958a-124">Switch Parameter to fetch Aborted jobs</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ListParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9958a-125">-Annullerad</span><span class="sxs-lookup"><span data-stu-id="9958a-125">-Cancelled</span></span>
<span data-ttu-id="9958a-126">Växla parameter för att hämta avbrutna jobb</span><span class="sxs-lookup"><span data-stu-id="9958a-126">Switch Parameter to fetch Cancelled jobs</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ListParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9958a-127">-Klar</span><span class="sxs-lookup"><span data-stu-id="9958a-127">-Completed</span></span>
<span data-ttu-id="9958a-128">Växla parameter för att hämta slutförda jobb</span><span class="sxs-lookup"><span data-stu-id="9958a-128">Switch Parameter to fetch Completed jobs</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ListParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9958a-129">-CompletedWithError</span><span class="sxs-lookup"><span data-stu-id="9958a-129">-CompletedWithError</span></span>
<span data-ttu-id="9958a-130">Växla parameter till att hämta jobb slutfört med fel</span><span class="sxs-lookup"><span data-stu-id="9958a-130">Switch Parameter to fetch jobs completed with errors</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ListParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9958a-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9958a-131">-DefaultProfile</span></span>
<span data-ttu-id="9958a-132">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="9958a-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9958a-133">-Namn</span><span class="sxs-lookup"><span data-stu-id="9958a-133">-Name</span></span>
<span data-ttu-id="9958a-134">Jobbnamn</span><span class="sxs-lookup"><span data-stu-id="9958a-134">Databox Job Name</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9958a-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9958a-135">-ResourceGroupName</span></span>
<span data-ttu-id="9958a-136">Namn på jobb i en datastapel</span><span class="sxs-lookup"><span data-stu-id="9958a-136">Databox Job Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9958a-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9958a-137">-ResourceId</span></span>
<span data-ttu-id="9958a-138">Resurs-ID för datastapel</span><span class="sxs-lookup"><span data-stu-id="9958a-138">Databox Job Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9958a-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9958a-139">CommonParameters</span></span>
<span data-ttu-id="9958a-140">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9958a-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9958a-141">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9958a-141">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9958a-142">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9958a-142">INPUTS</span></span>

### <span data-ttu-id="9958a-143">System. String</span><span class="sxs-lookup"><span data-stu-id="9958a-143">System.String</span></span>

## <span data-ttu-id="9958a-144">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9958a-144">OUTPUTS</span></span>

### <span data-ttu-id="9958a-145">Microsoft.Azure.PowerShell.Cmdlets.DataBox.Models.PSDataBoxJob</span><span class="sxs-lookup"><span data-stu-id="9958a-145">Microsoft.Azure.PowerShell.Cmdlets.DataBox.Models.PSDataBoxJob</span></span>

## <span data-ttu-id="9958a-146">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9958a-146">NOTES</span></span>

## <span data-ttu-id="9958a-147">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9958a-147">RELATED LINKS</span></span>
