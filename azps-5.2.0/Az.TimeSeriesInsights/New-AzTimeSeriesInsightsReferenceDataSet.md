---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.timeseriesinsights/new-aztimeseriesinsightsreferencedataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/New-AzTimeSeriesInsightsReferenceDataSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/New-AzTimeSeriesInsightsReferenceDataSet.md
ms.openlocfilehash: 39bbdf61a5068ea32f1febf66249213264235dfc
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98417331"
---
# <span data-ttu-id="b475f-101">New-AzTimeSeriesInsightsReferenceDataSet</span><span class="sxs-lookup"><span data-stu-id="b475f-101">New-AzTimeSeriesInsightsReferenceDataSet</span></span>

## <span data-ttu-id="b475f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b475f-102">SYNOPSIS</span></span>
<span data-ttu-id="b475f-103">Skapa eller uppdatera en referens data uppsättning i den angivna miljön.</span><span class="sxs-lookup"><span data-stu-id="b475f-103">Create or update a reference data set in the specified environment.</span></span>

## <span data-ttu-id="b475f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b475f-104">SYNTAX</span></span>

```
New-AzTimeSeriesInsightsReferenceDataSet -EnvironmentName <String> -Name <String> -ResourceGroupName <String>
 -KeyProperty <IReferenceDataSetKeyProperty[]> -Location <String> [-SubscriptionId <String>]
 [-DataStringComparisonBehavior <DataStringComparisonBehavior>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="b475f-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b475f-105">DESCRIPTION</span></span>
<span data-ttu-id="b475f-106">Skapa eller uppdatera en referens data uppsättning i den angivna miljön.</span><span class="sxs-lookup"><span data-stu-id="b475f-106">Create or update a reference data set in the specified environment.</span></span>

## <span data-ttu-id="b475f-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b475f-107">EXAMPLES</span></span>

### <span data-ttu-id="b475f-108">Exempel 1: skapa en referens data uppsättning för en viss miljö</span><span class="sxs-lookup"><span data-stu-id="b475f-108">Example 1: Create a reference data set for a specified environment</span></span>  
```powershell
PS C:\> $mykeyproperties = @{ "name" = "device01"; "type" = "Double"}
PS C:\> New-AzTimeSeriesInsightsReferenceDataSet -EnvironmentName tsitest001 -Name dstest001 -ResourceGroupName testgroup -Location eastus -DataStringComparisonBehavior Ordinal -KeyProperty $mykeyproperties

Location Name      Type
-------- ----      ----
eastus   dstest001 Microsoft.TimeSeriesInsights/Environments/ReferenceDataSets
```

<span data-ttu-id="b475f-109">Det här kommandot skapar en referens data uppsättning för en viss miljö.</span><span class="sxs-lookup"><span data-stu-id="b475f-109">This command creates a reference data set for a specific environment.</span></span>

## <span data-ttu-id="b475f-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b475f-110">PARAMETERS</span></span>

### <span data-ttu-id="b475f-111">-DataStringComparisonBehavior</span><span class="sxs-lookup"><span data-stu-id="b475f-111">-DataStringComparisonBehavior</span></span>
<span data-ttu-id="b475f-112">Det går att ange den här egenskapen med hjälp av funktionen för jämförelse av referens data uppsättning.</span><span class="sxs-lookup"><span data-stu-id="b475f-112">The reference data set key comparison behavior can be set using this property.</span></span>
<span data-ttu-id="b475f-113">Som standard är värdet ' ordinal '-vilket innebär Skift läges känslig jämförelse av nycklar som utförs när du ansluter till referens data med händelser eller när du lägger till nya referens data.</span><span class="sxs-lookup"><span data-stu-id="b475f-113">By default, the value is 'Ordinal' - which means case sensitive key comparison will be performed while joining reference data with events or while adding new reference data.</span></span>
<span data-ttu-id="b475f-114">När "OrdinalIgnoreCase" anges används Skift läges okänslig jämförelse.</span><span class="sxs-lookup"><span data-stu-id="b475f-114">When 'OrdinalIgnoreCase' is set, case insensitive comparison will be used.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Support.DataStringComparisonBehavior
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b475f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b475f-115">-DefaultProfile</span></span>
<span data-ttu-id="b475f-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b475f-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b475f-117">-EnvironmentName</span><span class="sxs-lookup"><span data-stu-id="b475f-117">-EnvironmentName</span></span>
<span data-ttu-id="b475f-118">Namnet på den miljö för tids serie som är kopplad till den angivna resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="b475f-118">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b475f-119">-Egenskapen-egenskap</span><span class="sxs-lookup"><span data-stu-id="b475f-119">-KeyProperty</span></span>
<span data-ttu-id="b475f-120">Listan över centrala egenskaper för referens data uppsättningen.</span><span class="sxs-lookup"><span data-stu-id="b475f-120">The list of key properties for the reference data set.</span></span>
<span data-ttu-id="b475f-121">Om du vill skapa läser du avsnittet anteckningar för egenskaper för nyckel egenskaper och skapar en hash-tabell.</span><span class="sxs-lookup"><span data-stu-id="b475f-121">To construct, see NOTES section for KEYPROPERTY properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IReferenceDataSetKeyProperty[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b475f-122">-Plats</span><span class="sxs-lookup"><span data-stu-id="b475f-122">-Location</span></span>
<span data-ttu-id="b475f-123">Resursens plats.</span><span class="sxs-lookup"><span data-stu-id="b475f-123">The location of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b475f-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="b475f-124">-Name</span></span>
<span data-ttu-id="b475f-125">Referens data uppsättningens namn.</span><span class="sxs-lookup"><span data-stu-id="b475f-125">Name of the reference data set.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ReferenceDataSetName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b475f-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b475f-126">-ResourceGroupName</span></span>
<span data-ttu-id="b475f-127">Namn på en Azure-resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="b475f-127">Name of an Azure Resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b475f-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b475f-128">-SubscriptionId</span></span>
<span data-ttu-id="b475f-129">ID för Azure-prenumeration.</span><span class="sxs-lookup"><span data-stu-id="b475f-129">Azure Subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b475f-130">-Tagg</span><span class="sxs-lookup"><span data-stu-id="b475f-130">-Tag</span></span>
<span data-ttu-id="b475f-131">Nyckeltal för fler egenskaper för resursen.</span><span class="sxs-lookup"><span data-stu-id="b475f-131">Key-value pairs of additional properties for the resource.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b475f-132">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="b475f-132">-Confirm</span></span>
<span data-ttu-id="b475f-133">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="b475f-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b475f-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b475f-134">-WhatIf</span></span>
<span data-ttu-id="b475f-135">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="b475f-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b475f-136">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="b475f-136">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b475f-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b475f-137">CommonParameters</span></span>
<span data-ttu-id="b475f-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b475f-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b475f-139">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b475f-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b475f-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b475f-140">INPUTS</span></span>

## <span data-ttu-id="b475f-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b475f-141">OUTPUTS</span></span>

### <span data-ttu-id="b475f-142">Microsoft. Azure. PowerShell. cmdletar. TimeSeriesInsights. Models. Api20200515. IReferenceDataSetResource</span><span class="sxs-lookup"><span data-stu-id="b475f-142">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IReferenceDataSetResource</span></span>

## <span data-ttu-id="b475f-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b475f-143">NOTES</span></span>

<span data-ttu-id="b475f-144">ALIAS</span><span class="sxs-lookup"><span data-stu-id="b475f-144">ALIASES</span></span>

<span data-ttu-id="b475f-145">KOMPLEXA PARAMETER EGENSKAPER</span><span class="sxs-lookup"><span data-stu-id="b475f-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="b475f-146">Skapa en hash-tabell som innehåller lämpliga egenskaper för att lägga till de parametrar som beskrivs nedan.</span><span class="sxs-lookup"><span data-stu-id="b475f-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b475f-147">Om du vill ha information om hash-tabeller kör Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="b475f-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="b475f-148"><egenskapen IReferenceDataSetKeyProperty [] >: listan med nyckel egenskaper för referens data uppsättningen.</span><span class="sxs-lookup"><span data-stu-id="b475f-148">KEYPROPERTY <IReferenceDataSetKeyProperty[]>: The list of key properties for the reference data set.</span></span>
  - <span data-ttu-id="b475f-149">`[Name <String>]`: Namnet på nyckel egenskapen.</span><span class="sxs-lookup"><span data-stu-id="b475f-149">`[Name <String>]`: The name of the key property.</span></span>
  - <span data-ttu-id="b475f-150">`[Type <ReferenceDataKeyPropertyType?>]`: Typen av nyckel egenskap.</span><span class="sxs-lookup"><span data-stu-id="b475f-150">`[Type <ReferenceDataKeyPropertyType?>]`: The type of the key property.</span></span>

## <span data-ttu-id="b475f-151">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b475f-151">RELATED LINKS</span></span>

