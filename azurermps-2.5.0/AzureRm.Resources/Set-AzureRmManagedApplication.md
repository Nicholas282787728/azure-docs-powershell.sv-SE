---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/set-azurermmanagedapplication
schema: 2.0.0
ms.openlocfilehash: 8fb6c2d299799849d1e9f2183621e9fc31cc0acd
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93929229"
---
# <span data-ttu-id="358ea-101">Set-AzureRmManagedApplication</span><span class="sxs-lookup"><span data-stu-id="358ea-101">Set-AzureRmManagedApplication</span></span>

## <span data-ttu-id="358ea-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="358ea-102">SYNOPSIS</span></span>
<span data-ttu-id="358ea-103">Uppdateringar hanterat program</span><span class="sxs-lookup"><span data-stu-id="358ea-103">Updates managed application</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="358ea-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="358ea-104">SYNTAX</span></span>

### <span data-ttu-id="358ea-105">SetByNameAndResourceGroup (standard)</span><span class="sxs-lookup"><span data-stu-id="358ea-105">SetByNameAndResourceGroup (Default)</span></span>
```
Set-AzureRmManagedApplication -Name <String> -ResourceGroupName <String> [-ManagedResourceGroupName <String>]
 [-ManagedApplicationDefinitionId <String>] [-Parameter <String>] [-Kind <String>] [-Plan <Hashtable>]
 [-Tag <Hashtable>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="358ea-106">SetById</span><span class="sxs-lookup"><span data-stu-id="358ea-106">SetById</span></span>
```
Set-AzureRmManagedApplication -Id <String> [-ManagedResourceGroupName <String>]
 [-ManagedApplicationDefinitionId <String>] [-Parameter <String>] [-Kind <String>] [-Plan <Hashtable>]
 [-Tag <Hashtable>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="358ea-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="358ea-107">DESCRIPTION</span></span>
<span data-ttu-id="358ea-108">Cmdleten **set-AzureRmManagedApplication** -hanterade program</span><span class="sxs-lookup"><span data-stu-id="358ea-108">The **Set-AzureRmManagedApplication** cmdlet updates managed applications</span></span>

## <span data-ttu-id="358ea-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="358ea-109">EXAMPLES</span></span>

### <span data-ttu-id="358ea-110">Exempel 1: definitions beskrivning för uppdatera hanterade program</span><span class="sxs-lookup"><span data-stu-id="358ea-110">Example 1: Update managed application definition description</span></span>
```
PS C:\>Set-AzureRmManagedApplication -ResourceId "/subscriptions/mySubId/resourcegroups/myRG/Microsoft.Solutions/applications/myApp" -Description "Updated description here"
```

<span data-ttu-id="358ea-111">Det här kommandot uppdaterar beskrivningen av hanterad program</span><span class="sxs-lookup"><span data-stu-id="358ea-111">This command updates the managed application description</span></span>

## <span data-ttu-id="358ea-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="358ea-112">PARAMETERS</span></span>

### <span data-ttu-id="358ea-113">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="358ea-113">-ApiVersion</span></span>
<span data-ttu-id="358ea-114">Anger vilken version av Resource Provider API som ska användas.</span><span class="sxs-lookup"><span data-stu-id="358ea-114">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="358ea-115">Om inget anges fastställs API-versionen automatiskt som den senaste tillgängliga.</span><span class="sxs-lookup"><span data-stu-id="358ea-115">If not specified, the API version is automatically determined as the latest available.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="358ea-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="358ea-116">-DefaultProfile</span></span>
<span data-ttu-id="358ea-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="358ea-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="358ea-118">-ID</span><span class="sxs-lookup"><span data-stu-id="358ea-118">-Id</span></span>
<span data-ttu-id="358ea-119">Fullständigt kvalificerat program-ID, inklusive prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="358ea-119">The fully qualified managed application Id, including the subscription.</span></span> <span data-ttu-id="358ea-120">till exempel/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName</span><span class="sxs-lookup"><span data-stu-id="358ea-120">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName</span></span>

```yaml
Type: String
Parameter Sets: SetById
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="358ea-121">-Sort</span><span class="sxs-lookup"><span data-stu-id="358ea-121">-Kind</span></span>
<span data-ttu-id="358ea-122">Den hanterade program typen.</span><span class="sxs-lookup"><span data-stu-id="358ea-122">The managed application kind.</span></span>
<span data-ttu-id="358ea-123">En av Marketplace eller servicecatalog</span><span class="sxs-lookup"><span data-stu-id="358ea-123">One of marketplace or servicecatalog</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="358ea-124">-ManagedApplicationDefinitionId</span><span class="sxs-lookup"><span data-stu-id="358ea-124">-ManagedApplicationDefinitionId</span></span>
<span data-ttu-id="358ea-125">Namnet på den hanterade resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="358ea-125">The managed resource group name.</span></span>

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

### <span data-ttu-id="358ea-126">-ManagedResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="358ea-126">-ManagedResourceGroupName</span></span>
<span data-ttu-id="358ea-127">Namnet på den hanterade resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="358ea-127">The managed resource group name.</span></span>

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

### <span data-ttu-id="358ea-128">-Namn</span><span class="sxs-lookup"><span data-stu-id="358ea-128">-Name</span></span>
<span data-ttu-id="358ea-129">Namnet på det hanterade programmet.</span><span class="sxs-lookup"><span data-stu-id="358ea-129">The managed application name.</span></span>

```yaml
Type: String
Parameter Sets: SetByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="358ea-130">-Parameter</span><span class="sxs-lookup"><span data-stu-id="358ea-130">-Parameter</span></span>
<span data-ttu-id="358ea-131">JSON-formaterad sträng för parametrar för hanterat program.</span><span class="sxs-lookup"><span data-stu-id="358ea-131">The JSON formatted string of parameters for managed application.</span></span>
<span data-ttu-id="358ea-132">Det kan vara en sökväg till ett fil namn eller en URI som innehåller parametrarna, eller parametrarna som sträng.</span><span class="sxs-lookup"><span data-stu-id="358ea-132">This can either be a path to a file name or uri containing the parameters, or the parameters as string.</span></span>

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

### <span data-ttu-id="358ea-133">-Planera</span><span class="sxs-lookup"><span data-stu-id="358ea-133">-Plan</span></span>
<span data-ttu-id="358ea-134">En hash-tabell som representerar hanterade program planerings egenskaper.</span><span class="sxs-lookup"><span data-stu-id="358ea-134">A hash table which represents managed application plan properties.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: PlanObject

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="358ea-135">-För</span><span class="sxs-lookup"><span data-stu-id="358ea-135">-Pre</span></span>
<span data-ttu-id="358ea-136">Anger att cmdleten bör använda för hands versionen av API-versioner när den ska avgöra vilken version som ska användas.</span><span class="sxs-lookup"><span data-stu-id="358ea-136">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="358ea-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="358ea-137">-ResourceGroupName</span></span>
<span data-ttu-id="358ea-138">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="358ea-138">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: SetByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="358ea-139">-Tagg</span><span class="sxs-lookup"><span data-stu-id="358ea-139">-Tag</span></span>
<span data-ttu-id="358ea-140">En hash-tabell som representerar resurs koder.</span><span class="sxs-lookup"><span data-stu-id="358ea-140">A hash table which represents resource tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="358ea-141">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="358ea-141">-Confirm</span></span>
<span data-ttu-id="358ea-142">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="358ea-142">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="358ea-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="358ea-143">-WhatIf</span></span>
<span data-ttu-id="358ea-144">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="358ea-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="358ea-145">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="358ea-145">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="358ea-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="358ea-146">CommonParameters</span></span>
<span data-ttu-id="358ea-147">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="358ea-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="358ea-148">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="358ea-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="358ea-149">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="358ea-149">INPUTS</span></span>

### <span data-ttu-id="358ea-150">System. String</span><span class="sxs-lookup"><span data-stu-id="358ea-150">System.String</span></span>
<span data-ttu-id="358ea-151">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="358ea-151">System.Collections.Hashtable</span></span>

## <span data-ttu-id="358ea-152">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="358ea-152">OUTPUTS</span></span>

### <span data-ttu-id="358ea-153">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="358ea-153">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="358ea-154">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="358ea-154">NOTES</span></span>

## <span data-ttu-id="358ea-155">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="358ea-155">RELATED LINKS</span></span>