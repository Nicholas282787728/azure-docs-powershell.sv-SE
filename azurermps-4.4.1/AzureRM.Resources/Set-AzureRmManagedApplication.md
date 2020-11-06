---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmManagedApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmManagedApplication.md
ms.openlocfilehash: 2a242f7a265efa2dd97f967101074615381d4cd5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575856"
---
# <span data-ttu-id="6d11f-101">Set-AzureRmManagedApplication</span><span class="sxs-lookup"><span data-stu-id="6d11f-101">Set-AzureRmManagedApplication</span></span>

## <span data-ttu-id="6d11f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6d11f-102">SYNOPSIS</span></span>
<span data-ttu-id="6d11f-103">Uppdateringar hanterat program</span><span class="sxs-lookup"><span data-stu-id="6d11f-103">Updates managed application</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6d11f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6d11f-104">SYNTAX</span></span>

### <span data-ttu-id="6d11f-105">Parametern för hanterade program namn.</span><span class="sxs-lookup"><span data-stu-id="6d11f-105">The managed application name parameter set.</span></span> <span data-ttu-id="6d11f-106">Vis</span><span class="sxs-lookup"><span data-stu-id="6d11f-106">(Default)</span></span>
```
Set-AzureRmManagedApplication -Name <String> -ResourceGroupName <String> [-ManagedResourceGroupName <String>]
 [-ManagedApplicationDefinitionId <String>] [-Parameter <String>] [-Kind <String>] [-Plan <Hashtable>]
 [-Tag <Hashtable>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6d11f-107">Parametern hanterad program-ID.</span><span class="sxs-lookup"><span data-stu-id="6d11f-107">The managed application Id parameter set.</span></span>
```
Set-AzureRmManagedApplication -Id <String> [-ManagedResourceGroupName <String>]
 [-ManagedApplicationDefinitionId <String>] [-Parameter <String>] [-Kind <String>] [-Plan <Hashtable>]
 [-Tag <Hashtable>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6d11f-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6d11f-108">DESCRIPTION</span></span>
<span data-ttu-id="6d11f-109">Cmdleten **set-AzureRmManagedApplication** -hanterade program</span><span class="sxs-lookup"><span data-stu-id="6d11f-109">The **Set-AzureRmManagedApplication** cmdlet updates managed applications</span></span>

## <span data-ttu-id="6d11f-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6d11f-110">EXAMPLES</span></span>

### <span data-ttu-id="6d11f-111">Exempel 1: definitions beskrivning för uppdatera hanterade program</span><span class="sxs-lookup"><span data-stu-id="6d11f-111">Example 1: Update managed application definition description</span></span>
```
PS C:\>Set-AzureRmManagedApplication -ResourceId "/subscriptions/mySubId/resourcegroups/myRG/Microsoft.Solutions/applications/myApp" -Description "Updated description here"
```

<span data-ttu-id="6d11f-112">Det här kommandot uppdaterar beskrivningen av hanterad program</span><span class="sxs-lookup"><span data-stu-id="6d11f-112">This command updates the managed application description</span></span>

## <span data-ttu-id="6d11f-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6d11f-113">PARAMETERS</span></span>

### <span data-ttu-id="6d11f-114">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="6d11f-114">-ApiVersion</span></span>
<span data-ttu-id="6d11f-115">Anger vilken version av Resource Provider API som ska användas.</span><span class="sxs-lookup"><span data-stu-id="6d11f-115">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="6d11f-116">Om inget anges fastställs API-versionen automatiskt som den senaste tillgängliga.</span><span class="sxs-lookup"><span data-stu-id="6d11f-116">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="6d11f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d11f-117">-DefaultProfile</span></span>
<span data-ttu-id="6d11f-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="6d11f-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d11f-119">-Sort</span><span class="sxs-lookup"><span data-stu-id="6d11f-119">-Kind</span></span>
<span data-ttu-id="6d11f-120">Den hanterade program typen.</span><span class="sxs-lookup"><span data-stu-id="6d11f-120">The managed application kind.</span></span>
<span data-ttu-id="6d11f-121">En av Marketplace eller servicecatalog</span><span class="sxs-lookup"><span data-stu-id="6d11f-121">One of marketplace or servicecatalog</span></span>

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

### <span data-ttu-id="6d11f-122">-ManagedApplicationDefinitionId</span><span class="sxs-lookup"><span data-stu-id="6d11f-122">-ManagedApplicationDefinitionId</span></span>
<span data-ttu-id="6d11f-123">Namnet på den hanterade resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="6d11f-123">The managed resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d11f-124">-ManagedResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6d11f-124">-ManagedResourceGroupName</span></span>
<span data-ttu-id="6d11f-125">Namnet på den hanterade resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="6d11f-125">The managed resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d11f-126">-Namn</span><span class="sxs-lookup"><span data-stu-id="6d11f-126">-Name</span></span>
<span data-ttu-id="6d11f-127">Namnet på det hanterade programmet.</span><span class="sxs-lookup"><span data-stu-id="6d11f-127">The managed application name.</span></span>

```yaml
Type: System.String
Parameter Sets: The managed application name parameter set.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d11f-128">-Parameter</span><span class="sxs-lookup"><span data-stu-id="6d11f-128">-Parameter</span></span>
<span data-ttu-id="6d11f-129">JSON-formaterad sträng för parametrar för hanterat program.</span><span class="sxs-lookup"><span data-stu-id="6d11f-129">The JSON formatted string of parameters for managed application.</span></span>
<span data-ttu-id="6d11f-130">Det kan vara en sökväg till ett fil namn eller en URI som innehåller parametrarna, eller parametrarna som sträng.</span><span class="sxs-lookup"><span data-stu-id="6d11f-130">This can either be a path to a file name or uri containing the parameters, or the parameters as string.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d11f-131">-Planera</span><span class="sxs-lookup"><span data-stu-id="6d11f-131">-Plan</span></span>
<span data-ttu-id="6d11f-132">En hash-tabell som representerar hanterade program planerings egenskaper.</span><span class="sxs-lookup"><span data-stu-id="6d11f-132">A hash table which represents managed application plan properties.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: PlanObject

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d11f-133">-För</span><span class="sxs-lookup"><span data-stu-id="6d11f-133">-Pre</span></span>
<span data-ttu-id="6d11f-134">Anger att cmdleten bör använda för hands versionen av API-versioner när den ska avgöra vilken version som ska användas.</span><span class="sxs-lookup"><span data-stu-id="6d11f-134">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d11f-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6d11f-135">-ResourceGroupName</span></span>
<span data-ttu-id="6d11f-136">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="6d11f-136">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: The managed application name parameter set.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d11f-137">-Tagg</span><span class="sxs-lookup"><span data-stu-id="6d11f-137">-Tag</span></span>
<span data-ttu-id="6d11f-138">En hash-tabell som representerar resurs koder.</span><span class="sxs-lookup"><span data-stu-id="6d11f-138">A hash table which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d11f-139">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="6d11f-139">-Confirm</span></span>
<span data-ttu-id="6d11f-140">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="6d11f-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6d11f-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6d11f-141">-WhatIf</span></span>
<span data-ttu-id="6d11f-142">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="6d11f-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6d11f-143">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="6d11f-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6d11f-144">-ID</span><span class="sxs-lookup"><span data-stu-id="6d11f-144">-Id</span></span>
<span data-ttu-id="6d11f-145">Fullständigt kvalificerat program-ID, inklusive prenumerationen.</span><span class="sxs-lookup"><span data-stu-id="6d11f-145">The fully qualified managed application Id, including the subscription.</span></span> <span data-ttu-id="6d11f-146">till exempel/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="6d11f-146">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

```yaml
Type: System.String
Parameter Sets: The managed application Id parameter set.
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d11f-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d11f-147">CommonParameters</span></span>
<span data-ttu-id="6d11f-148">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6d11f-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d11f-149">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6d11f-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d11f-150">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6d11f-150">INPUTS</span></span>

### <span data-ttu-id="6d11f-151">System. String</span><span class="sxs-lookup"><span data-stu-id="6d11f-151">System.String</span></span>
<span data-ttu-id="6d11f-152">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="6d11f-152">System.Collections.Hashtable</span></span>

## <span data-ttu-id="6d11f-153">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6d11f-153">OUTPUTS</span></span>

### <span data-ttu-id="6d11f-154">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="6d11f-154">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="6d11f-155">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6d11f-155">NOTES</span></span>

## <span data-ttu-id="6d11f-156">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6d11f-156">RELATED LINKS</span></span>

