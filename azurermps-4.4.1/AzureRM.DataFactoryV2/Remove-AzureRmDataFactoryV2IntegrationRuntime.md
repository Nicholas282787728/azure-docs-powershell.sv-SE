---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2IntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2IntegrationRuntime.md
gitcommit: https://github.com/Azure/azure-powershell/blob/db8032a9100d47fd3aa4248c7807d8e0bb538e83
ms.openlocfilehash: 81b05b8229530a8975be023a3b4a5e8c93d93c80
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93585664"
---
# <span data-ttu-id="443de-101">Remove-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="443de-101">Remove-AzureRmDataFactoryV2IntegrationRuntime</span></span>

## <span data-ttu-id="443de-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="443de-102">SYNOPSIS</span></span>
<span data-ttu-id="443de-103">Tar bort en integrations körning.</span><span class="sxs-lookup"><span data-stu-id="443de-103">Removes an integration runtime.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="443de-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="443de-104">SYNTAX</span></span>

### <span data-ttu-id="443de-105">ByIntegrationRuntimeName (standard)</span><span class="sxs-lookup"><span data-stu-id="443de-105">ByIntegrationRuntimeName (Default)</span></span>
```
Remove-AzureRmDataFactoryV2IntegrationRuntime [-Force] [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-WhatIf] [-Confirm]
```

### <span data-ttu-id="443de-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="443de-106">ByResourceId</span></span>
```
Remove-AzureRmDataFactoryV2IntegrationRuntime [-Force] [-ResourceId] <String> [-WhatIf] [-Confirm]
```

### <span data-ttu-id="443de-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="443de-107">ByIntegrationRuntimeObject</span></span>
```
Remove-AzureRmDataFactoryV2IntegrationRuntime [-Force] [-InputObject] <PSIntegrationRuntime> [-WhatIf]
 [-Confirm]
```

## <span data-ttu-id="443de-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="443de-108">DESCRIPTION</span></span>
<span data-ttu-id="443de-109">Remove-AzureRmDataFactoryV2IntegrationRuntime cmdlet tar bort en integrations körning.</span><span class="sxs-lookup"><span data-stu-id="443de-109">The Remove-AzureRmDataFactoryV2IntegrationRuntime cmdlet removes a integration runtime.</span></span>

## <span data-ttu-id="443de-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="443de-110">EXAMPLES</span></span>

### <span data-ttu-id="443de-111">Exempel 1: ta bort en integrations körning</span><span class="sxs-lookup"><span data-stu-id="443de-111">Example 1: Remove a integration runtime</span></span>
```
PS C:\> Remove-AzureRmDataFactoryV2IntegrationRuntime  -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df' -Name 'test-reserved-ir' -Confirm
```

<span data-ttu-id="443de-112">Det här kommandot tar bort integrations körningen med namnet "test-reserverad-IR" från data fabriken med namnet "test-DF".</span><span class="sxs-lookup"><span data-stu-id="443de-112">This command removes the integration runtime named 'test-reserved-ir' from the data factory named 'test-df'.</span></span>
<span data-ttu-id="443de-113">Det här kommandot returnerar ett värde för $True.</span><span class="sxs-lookup"><span data-stu-id="443de-113">This command returns a value of $True.</span></span>

## <span data-ttu-id="443de-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="443de-114">PARAMETERS</span></span>

### <span data-ttu-id="443de-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="443de-115">-DataFactoryName</span></span>
<span data-ttu-id="443de-116">Namnet på data fabriken.</span><span class="sxs-lookup"><span data-stu-id="443de-116">The data factory name.</span></span>

```yaml
Type: String
Parameter Sets: ByIntegrationRuntimeName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="443de-117">-Force</span><span class="sxs-lookup"><span data-stu-id="443de-117">-Force</span></span>
<span data-ttu-id="443de-118">Kör cmdleten utan att behöva bekräfta.</span><span class="sxs-lookup"><span data-stu-id="443de-118">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="443de-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="443de-119">-InputObject</span></span>
<span data-ttu-id="443de-120">Integration runtime-objekt.</span><span class="sxs-lookup"><span data-stu-id="443de-120">The integration runtime object.</span></span>

```yaml
Type: PSIntegrationRuntime
Parameter Sets: ByIntegrationRuntimeObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="443de-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="443de-121">-Name</span></span>
<span data-ttu-id="443de-122">Integrerings körens namn.</span><span class="sxs-lookup"><span data-stu-id="443de-122">The integration runtime name.</span></span>

```yaml
Type: String
Parameter Sets: ByIntegrationRuntimeName
Aliases: IntegrationRuntimeName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="443de-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="443de-123">-ResourceGroupName</span></span>
<span data-ttu-id="443de-124">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="443de-124">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByIntegrationRuntimeName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="443de-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="443de-125">-ResourceId</span></span>
<span data-ttu-id="443de-126">ID för Azure-resursen.</span><span class="sxs-lookup"><span data-stu-id="443de-126">The Azure resource ID.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases: Id

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="443de-127">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="443de-127">-Confirm</span></span>
<span data-ttu-id="443de-128">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="443de-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="443de-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="443de-129">-WhatIf</span></span>
<span data-ttu-id="443de-130">Visar vad som händer om cmdleten körs men inte kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="443de-130">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

## <span data-ttu-id="443de-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="443de-131">INPUTS</span></span>

### <span data-ttu-id="443de-132">System. String</span><span class="sxs-lookup"><span data-stu-id="443de-132">System.String</span></span>
<span data-ttu-id="443de-133">Microsoft. Azure. commands. DataFactoryV2. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="443de-133">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="443de-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="443de-134">OUTPUTS</span></span>

### <span data-ttu-id="443de-135">System. Object</span><span class="sxs-lookup"><span data-stu-id="443de-135">System.Object</span></span>

## <span data-ttu-id="443de-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="443de-136">NOTES</span></span>
<span data-ttu-id="443de-137">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, data, faktorer, kopiera, aktiviteter, integrerings körning</span><span class="sxs-lookup"><span data-stu-id="443de-137">Keywords: azure, azurerm, arm, resource, management, manager, data, factories, copy, activities, integration runtime</span></span>

## <span data-ttu-id="443de-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="443de-138">RELATED LINKS</span></span>
[<span data-ttu-id="443de-139">Set-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="443de-139">Set-AzureRmDataFactoryV2IntegrationRuntime</span></span>]()

[<span data-ttu-id="443de-140">Get-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="443de-140">Get-AzureRmDataFactoryV2IntegrationRuntime</span></span>]()

