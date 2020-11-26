---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 54DFBB63-AE8C-4918-870F-19FAD6CC5E4A
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/set-azoperationalinsightsworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsWorkspace.md
ms.openlocfilehash: 5abfd1a02687eb2715ad924510176748e04e56cd
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94260668"
---
# <span data-ttu-id="be2bc-101">Set-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="be2bc-101">Set-AzOperationalInsightsWorkspace</span></span>

## <span data-ttu-id="be2bc-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="be2bc-102">SYNOPSIS</span></span>
<span data-ttu-id="be2bc-103">Uppdaterar en arbets yta.</span><span class="sxs-lookup"><span data-stu-id="be2bc-103">Updates a workspace.</span></span>

## <span data-ttu-id="be2bc-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="be2bc-104">SYNTAX</span></span>

### <span data-ttu-id="be2bc-105">ByName (standard)</span><span class="sxs-lookup"><span data-stu-id="be2bc-105">ByName (Default)</span></span>
```
Set-AzOperationalInsightsWorkspace [-ResourceGroupName] <String> [-Name] <String> [[-Sku] <String>]
 [[-Tag] <Hashtable>] [-RetentionInDays <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [-PublicNetworkAccessForIngestion <String>] [-PublicNetworkAccessForQuery <String>] [<CommonParameters>]
```

### <span data-ttu-id="be2bc-106">ByObject</span><span class="sxs-lookup"><span data-stu-id="be2bc-106">ByObject</span></span>
```
Set-AzOperationalInsightsWorkspace [-Workspace] <PSWorkspace> [[-Sku] <String>] [[-Tag] <Hashtable>]
 [-RetentionInDays <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [-PublicNetworkAccessForIngestion <String>] [-PublicNetworkAccessForQuery <String>] [<CommonParameters>]
```

## <span data-ttu-id="be2bc-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="be2bc-107">DESCRIPTION</span></span>
<span data-ttu-id="be2bc-108">Cmdleten **set-AzOperationalInsightsWorkspace** ändrar arbets ytans konfiguration.</span><span class="sxs-lookup"><span data-stu-id="be2bc-108">The **Set-AzOperationalInsightsWorkspace** cmdlet changes the configuration of a workspace.</span></span>

## <span data-ttu-id="be2bc-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="be2bc-109">EXAMPLES</span></span>

### <span data-ttu-id="be2bc-110">Exempel 1: ändra en arbets yta efter namn</span><span class="sxs-lookup"><span data-stu-id="be2bc-110">Example 1: Modify a workspace by name</span></span>
```
PS C:\>Set-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" -Sku Standard -Tags @{ "Department" = "IT" }
```

<span data-ttu-id="be2bc-111">Det här kommandot ändrar SKU och taggar för arbets ytan med namnet min arbets yta i resurs gruppen som heter ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="be2bc-111">This command modifies the SKU and tags of the workspace named MyWorkspace in the resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="be2bc-112">Exempel 2: uppdatera en arbets yta med hjälp av pipeline</span><span class="sxs-lookup"><span data-stu-id="be2bc-112">Example 2: Update a workspace by using the pipeline</span></span>
```
PS C:\>Get-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" | Set-AzOperationalInsightsWorkspace -Sku "Premium"
```

<span data-ttu-id="be2bc-113">Det här kommandot använder cmdleten Get-AzOperationalInsightsWorkspace för att hämta arbets ytan som heter min arbets yta och skickar den till cmdleten **set-AzOperationalInsightsWorkspace** genom att använda pipeline-operatorn för att ange SKU till Premium.</span><span class="sxs-lookup"><span data-stu-id="be2bc-113">This command uses the Get-AzOperationalInsightsWorkspace cmdlet to get the workspace named MyWorkSpace, and then passes it to the **Set-AzOperationalInsightsWorkspace** cmdlet by using the pipeline operator to set the SKU to Premium.</span></span>

## <span data-ttu-id="be2bc-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="be2bc-114">PARAMETERS</span></span>

### <span data-ttu-id="be2bc-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be2bc-115">-DefaultProfile</span></span>
<span data-ttu-id="be2bc-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="be2bc-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="be2bc-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="be2bc-117">-Name</span></span>
<span data-ttu-id="be2bc-118">Anger arbets ytans namn.</span><span class="sxs-lookup"><span data-stu-id="be2bc-118">Specifies the workspace name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be2bc-119">-PublicNetworkAccessForIngestion</span><span class="sxs-lookup"><span data-stu-id="be2bc-119">-PublicNetworkAccessForIngestion</span></span>
<span data-ttu-id="be2bc-120">Nätverks åtkomst typen för att komma åt arbets ytan.</span><span class="sxs-lookup"><span data-stu-id="be2bc-120">The network access type for accessing workspace ingestion.</span></span> <span data-ttu-id="be2bc-121">Värdet ska vara Enabled eller disabled</span><span class="sxs-lookup"><span data-stu-id="be2bc-121">Value should be 'Enabled' or 'Disabled'</span></span>

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

### <span data-ttu-id="be2bc-122">-PublicNetworkAccessForQuery</span><span class="sxs-lookup"><span data-stu-id="be2bc-122">-PublicNetworkAccessForQuery</span></span>
<span data-ttu-id="be2bc-123">Nätverks åtkomst typen för åtkomst till arbets ytan.</span><span class="sxs-lookup"><span data-stu-id="be2bc-123">The network access type for accessing workspace query.</span></span> <span data-ttu-id="be2bc-124">Värdet ska vara Enabled eller disabled</span><span class="sxs-lookup"><span data-stu-id="be2bc-124">Value should be 'Enabled' or 'Disabled'</span></span>

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

### <span data-ttu-id="be2bc-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="be2bc-125">-ResourceGroupName</span></span>
<span data-ttu-id="be2bc-126">Anger namnet på Azure Resource-gruppen.</span><span class="sxs-lookup"><span data-stu-id="be2bc-126">Specifies the Azure resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be2bc-127">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="be2bc-127">-RetentionInDays</span></span>
<span data-ttu-id="be2bc-128">Arbets ytans data lagring i dagar.</span><span class="sxs-lookup"><span data-stu-id="be2bc-128">The workspace data retention in days.</span></span> <span data-ttu-id="be2bc-129">730 dagar är det högsta tillåtna antalet för alla andra SKU: er</span><span class="sxs-lookup"><span data-stu-id="be2bc-129">730 days is the maximum allowed for all other Skus</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be2bc-130">-SKU</span><span class="sxs-lookup"><span data-stu-id="be2bc-130">-Sku</span></span>
<span data-ttu-id="be2bc-131">Anger arbets ytans tjänste nivå.</span><span class="sxs-lookup"><span data-stu-id="be2bc-131">Specifies the service tier of the workspace.</span></span>
<span data-ttu-id="be2bc-132">Giltiga värden är:</span><span class="sxs-lookup"><span data-stu-id="be2bc-132">Valid values are:</span></span> 
- <span data-ttu-id="be2bc-133">gratisutdelning</span><span class="sxs-lookup"><span data-stu-id="be2bc-133">free</span></span>
- <span data-ttu-id="be2bc-134">standar</span><span class="sxs-lookup"><span data-stu-id="be2bc-134">standard</span></span>
- <span data-ttu-id="be2bc-135">Beta</span><span class="sxs-lookup"><span data-stu-id="be2bc-135">premium</span></span>
- <span data-ttu-id="be2bc-136">pernode</span><span class="sxs-lookup"><span data-stu-id="be2bc-136">pernode</span></span>
- <span data-ttu-id="be2bc-137">fristående</span><span class="sxs-lookup"><span data-stu-id="be2bc-137">standalone</span></span>
- <span data-ttu-id="be2bc-138">pergb2018</span><span class="sxs-lookup"><span data-stu-id="be2bc-138">pergb2018</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: free, standard, premium, pernode, standalone, pergb2018

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be2bc-139">-Tagg</span><span class="sxs-lookup"><span data-stu-id="be2bc-139">-Tag</span></span>
<span data-ttu-id="be2bc-140">Resurs märkningen för arbets ytan.</span><span class="sxs-lookup"><span data-stu-id="be2bc-140">The resource tags for the workspace.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be2bc-141">-Arbets yta</span><span class="sxs-lookup"><span data-stu-id="be2bc-141">-Workspace</span></span>
<span data-ttu-id="be2bc-142">Anger arbets ytan som ska uppdateras.</span><span class="sxs-lookup"><span data-stu-id="be2bc-142">Specifies the workspace to be updated.</span></span>

```yaml
Type: Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace
Parameter Sets: ByObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="be2bc-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be2bc-143">CommonParameters</span></span>
<span data-ttu-id="be2bc-144">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="be2bc-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be2bc-145">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="be2bc-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be2bc-146">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="be2bc-146">INPUTS</span></span>

### <span data-ttu-id="be2bc-147">Microsoft. Azure. commands. OperationalInsights. Models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="be2bc-147">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="be2bc-148">System. String</span><span class="sxs-lookup"><span data-stu-id="be2bc-148">System.String</span></span>

### <span data-ttu-id="be2bc-149">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="be2bc-149">System.Collections.Hashtable</span></span>

### <span data-ttu-id="be2bc-150">System. Nullable ' 1 [[system. Int32, system. privat. CoreLib, version = 4.0.0.0, Culture = neutralt, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="be2bc-150">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="be2bc-151">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="be2bc-151">OUTPUTS</span></span>

### <span data-ttu-id="be2bc-152">Microsoft. Azure. commands. OperationalInsights. Models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="be2bc-152">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

## <span data-ttu-id="be2bc-153">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="be2bc-153">NOTES</span></span>

## <span data-ttu-id="be2bc-154">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="be2bc-154">RELATED LINKS</span></span>

[<span data-ttu-id="be2bc-155">Cmdlets för Azure Operational Insights</span><span class="sxs-lookup"><span data-stu-id="be2bc-155">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)

[<span data-ttu-id="be2bc-156">Get-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="be2bc-156">Get-AzOperationalInsightsWorkspace</span></span>](./Get-AzOperationalInsightsWorkspace.md)

