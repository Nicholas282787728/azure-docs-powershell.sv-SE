---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmManagedApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmManagedApplication.md
ms.openlocfilehash: 830b1ed91f8e6148886be9fa3d0c49d48d52d369
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93585332"
---
# <span data-ttu-id="a9059-101">New-AzureRmManagedApplication</span><span class="sxs-lookup"><span data-stu-id="a9059-101">New-AzureRmManagedApplication</span></span>

## <span data-ttu-id="a9059-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a9059-102">SYNOPSIS</span></span>
<span data-ttu-id="a9059-103">Skapar ett Azure-hanterat program.</span><span class="sxs-lookup"><span data-stu-id="a9059-103">Creates an Azure managed application.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a9059-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a9059-104">SYNTAX</span></span>

```
New-AzureRmManagedApplication -Name <String> -ResourceGroupName <String> -ManagedResourceGroupName <String>
 [-ManagedApplicationDefinitionId <String>] -Location <String> [-Parameter <String>] -Kind <ApplicationKind>
 [-Plan <Hashtable>] [-Tag <Hashtable>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a9059-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a9059-105">DESCRIPTION</span></span>
<span data-ttu-id="a9059-106">Cmdleten **New-AzureRmManagedApplication** skapar ett Azure-hanterat program.</span><span class="sxs-lookup"><span data-stu-id="a9059-106">The **New-AzureRmManagedApplication** cmdlet creates an Azure Managed Application.</span></span>

## <span data-ttu-id="a9059-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a9059-107">EXAMPLES</span></span>

### <span data-ttu-id="a9059-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="a9059-108">Example 1</span></span>
```
PS C:\>New-AzureRmManagedApplication -Name "myManagedApplication" -ResourceGroupName myRG -ManagedResourceGroupName myManagedRG -ManagedApplicationDefinitionId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myRG/providers/Microsoft.Solutions/applicationDefinitions/myAppDef" -Location eastus2euap -Kind ServiceCatalog
```

<span data-ttu-id="a9059-109">Det här kommandot skapar ett hanterat program</span><span class="sxs-lookup"><span data-stu-id="a9059-109">This command creates a managed application</span></span>

## <span data-ttu-id="a9059-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a9059-110">PARAMETERS</span></span>

### <span data-ttu-id="a9059-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="a9059-111">-ApiVersion</span></span>
<span data-ttu-id="a9059-112">Anger vilken version av Resource Provider API som ska användas.</span><span class="sxs-lookup"><span data-stu-id="a9059-112">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="a9059-113">Om inget anges fastställs API-versionen automatiskt som den senaste tillgängliga.</span><span class="sxs-lookup"><span data-stu-id="a9059-113">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="a9059-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9059-114">-DefaultProfile</span></span>
<span data-ttu-id="a9059-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a9059-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a9059-116">-Sort</span><span class="sxs-lookup"><span data-stu-id="a9059-116">-Kind</span></span>
<span data-ttu-id="a9059-117">Den hanterade program typen.</span><span class="sxs-lookup"><span data-stu-id="a9059-117">The managed application kind.</span></span>
<span data-ttu-id="a9059-118">En av Marketplace eller servicecatalog</span><span class="sxs-lookup"><span data-stu-id="a9059-118">One of marketplace or servicecatalog</span></span>

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.Entities.Application.ApplicationKind
Parameter Sets: (All)
Aliases: 
Accepted values: ServiceCatalog, MarketPlace

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9059-119">-Plats</span><span class="sxs-lookup"><span data-stu-id="a9059-119">-Location</span></span>
<span data-ttu-id="a9059-120">Resurs platsen.</span><span class="sxs-lookup"><span data-stu-id="a9059-120">The resource location.</span></span>

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

### <span data-ttu-id="a9059-121">-ManagedApplicationDefinitionId</span><span class="sxs-lookup"><span data-stu-id="a9059-121">-ManagedApplicationDefinitionId</span></span>
<span data-ttu-id="a9059-122">Namnet på den hanterade resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="a9059-122">The managed resource group name.</span></span>

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

### <span data-ttu-id="a9059-123">-ManagedResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a9059-123">-ManagedResourceGroupName</span></span>
<span data-ttu-id="a9059-124">Namnet på den hanterade resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="a9059-124">The managed resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9059-125">-Namn</span><span class="sxs-lookup"><span data-stu-id="a9059-125">-Name</span></span>
<span data-ttu-id="a9059-126">Namnet på det hanterade programmet.</span><span class="sxs-lookup"><span data-stu-id="a9059-126">The managed application name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9059-127">-Parameter</span><span class="sxs-lookup"><span data-stu-id="a9059-127">-Parameter</span></span>
<span data-ttu-id="a9059-128">JSON-formaterad sträng för parametrar för hanterat program.</span><span class="sxs-lookup"><span data-stu-id="a9059-128">The JSON formatted string of parameters for managed application.</span></span>
<span data-ttu-id="a9059-129">Det kan vara en sökväg till ett fil namn eller en URI som innehåller parametrarna, eller parametrarna som sträng.</span><span class="sxs-lookup"><span data-stu-id="a9059-129">This can either be a path to a file name or uri containing the parameters, or the parameters as string.</span></span>

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

### <span data-ttu-id="a9059-130">-Planera</span><span class="sxs-lookup"><span data-stu-id="a9059-130">-Plan</span></span>
<span data-ttu-id="a9059-131">En hash-tabell som representerar hanterade program planerings egenskaper.</span><span class="sxs-lookup"><span data-stu-id="a9059-131">A hash table which represents managed application plan properties.</span></span>

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

### <span data-ttu-id="a9059-132">-För</span><span class="sxs-lookup"><span data-stu-id="a9059-132">-Pre</span></span>
<span data-ttu-id="a9059-133">Anger att cmdleten bör använda för hands versionen av API-versioner när den ska avgöra vilken version som ska användas.</span><span class="sxs-lookup"><span data-stu-id="a9059-133">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="a9059-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a9059-134">-ResourceGroupName</span></span>
<span data-ttu-id="a9059-135">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="a9059-135">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9059-136">-Tagg</span><span class="sxs-lookup"><span data-stu-id="a9059-136">-Tag</span></span>
<span data-ttu-id="a9059-137">En hash som representerar resurs koder.</span><span class="sxs-lookup"><span data-stu-id="a9059-137">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="a9059-138">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="a9059-138">-Confirm</span></span>
<span data-ttu-id="a9059-139">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="a9059-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a9059-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a9059-140">-WhatIf</span></span>
<span data-ttu-id="a9059-141">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="a9059-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a9059-142">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="a9059-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a9059-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9059-143">CommonParameters</span></span>
<span data-ttu-id="a9059-144">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a9059-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9059-145">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a9059-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9059-146">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a9059-146">INPUTS</span></span>

### <span data-ttu-id="a9059-147">System. String</span><span class="sxs-lookup"><span data-stu-id="a9059-147">System.String</span></span>
<span data-ttu-id="a9059-148">System. Collections. hash</span><span class="sxs-lookup"><span data-stu-id="a9059-148">System.Collections.Hashtable</span></span>

## <span data-ttu-id="a9059-149">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a9059-149">OUTPUTS</span></span>

### <span data-ttu-id="a9059-150">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="a9059-150">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="a9059-151">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a9059-151">NOTES</span></span>

## <span data-ttu-id="a9059-152">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a9059-152">RELATED LINKS</span></span>
