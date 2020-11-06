---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2IntegrationRuntimeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2IntegrationRuntimeNode.md
gitcommit: https://github.com/Azure/azure-powershell/blob/db8032a9100d47fd3aa4248c7807d8e0bb538e83
ms.openlocfilehash: e5bf7ca6951a78fc631b5bc2ffa96a2042423d9f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93583327"
---
# <span data-ttu-id="65dfa-101">Remove-AzureRmDataFactoryV2IntegrationRuntimeNode</span><span class="sxs-lookup"><span data-stu-id="65dfa-101">Remove-AzureRmDataFactoryV2IntegrationRuntimeNode</span></span>

## <span data-ttu-id="65dfa-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="65dfa-102">SYNOPSIS</span></span>
<span data-ttu-id="65dfa-103">Ta bort en nod med det angivna namnet i en integrations körning.</span><span class="sxs-lookup"><span data-stu-id="65dfa-103">Remove a node with the given name on an integration runtime.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="65dfa-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="65dfa-104">SYNTAX</span></span>

### <span data-ttu-id="65dfa-105">ByIntegrationRuntimeName (standard)</span><span class="sxs-lookup"><span data-stu-id="65dfa-105">ByIntegrationRuntimeName (Default)</span></span>
```
Remove-AzureRmDataFactoryV2IntegrationRuntimeNode -NodeName <String> [-Force]
 [-IntegrationRuntimeName] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String> [-WhatIf]
 [-Confirm]
```

### <span data-ttu-id="65dfa-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="65dfa-106">ByResourceId</span></span>
```
Remove-AzureRmDataFactoryV2IntegrationRuntimeNode -NodeName <String> [-Force] [-ResourceId] <String> [-WhatIf]
 [-Confirm]
```

### <span data-ttu-id="65dfa-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="65dfa-107">ByIntegrationRuntimeObject</span></span>
```
Remove-AzureRmDataFactoryV2IntegrationRuntimeNode -NodeName <String> [-Force]
 [-InputObject] <PSIntegrationRuntime> [-WhatIf] [-Confirm]
```

## <span data-ttu-id="65dfa-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="65dfa-108">DESCRIPTION</span></span>
<span data-ttu-id="65dfa-109">Remove-AzureRmDataFactoryV2IntegrationRuntimeNode cmdlet tar bort en nod i en integrations körning.</span><span class="sxs-lookup"><span data-stu-id="65dfa-109">The Remove-AzureRmDataFactoryV2IntegrationRuntimeNode cmdlet removes a node in an integration runtime.</span></span>

## <span data-ttu-id="65dfa-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="65dfa-110">EXAMPLES</span></span>

### <span data-ttu-id="65dfa-111">Exempel 1: ta bort en nod från en integrations körning</span><span class="sxs-lookup"><span data-stu-id="65dfa-111">Example 1: Remove a node from an integration runtime</span></span>
```
PS C:\> Remove-AzureRmDataFactoryV2IntegrationRuntimeNode -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir' -NodeName 'Node_1'
```

<span data-ttu-id="65dfa-112">Det här kommandot tar bort en nod med namnet "Node_1" i integrations körningen med namnet "test-selfhost-IR" i prenumerationen för resurs gruppen med namnet "RG-test-dfv2" och data fabriken med namnet "test-DF-EU2".</span><span class="sxs-lookup"><span data-stu-id="65dfa-112">This command removes an node named 'Node_1' in the integration runtime named 'test-selfhost-ir' in the subscription for the resource group named 'rg-test-dfv2' and data factory named 'test-df-eu2'.</span></span>

## <span data-ttu-id="65dfa-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="65dfa-113">PARAMETERS</span></span>

### <span data-ttu-id="65dfa-114">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="65dfa-114">-Confirm</span></span>
<span data-ttu-id="65dfa-115">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="65dfa-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="65dfa-116">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="65dfa-116">-DataFactoryName</span></span>
<span data-ttu-id="65dfa-117">Namnet på data fabriken.</span><span class="sxs-lookup"><span data-stu-id="65dfa-117">The data factory name.</span></span>

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

### <span data-ttu-id="65dfa-118">-Force</span><span class="sxs-lookup"><span data-stu-id="65dfa-118">-Force</span></span>
<span data-ttu-id="65dfa-119">Kör cmdleten utan att behöva bekräfta.</span><span class="sxs-lookup"><span data-stu-id="65dfa-119">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="65dfa-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="65dfa-120">-InputObject</span></span>
<span data-ttu-id="65dfa-121">Integration runtime-objekt.</span><span class="sxs-lookup"><span data-stu-id="65dfa-121">The integration runtime object.</span></span>

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

### <span data-ttu-id="65dfa-122">-IntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="65dfa-122">-IntegrationRuntimeName</span></span>
<span data-ttu-id="65dfa-123">Integrerings körens namn.</span><span class="sxs-lookup"><span data-stu-id="65dfa-123">The integration runtime name.</span></span>

```yaml
Type: String
Parameter Sets: ByIntegrationRuntimeName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65dfa-124">-Nodnamn</span><span class="sxs-lookup"><span data-stu-id="65dfa-124">-NodeName</span></span>
<span data-ttu-id="65dfa-125">Integration runtime-nodnamnet.</span><span class="sxs-lookup"><span data-stu-id="65dfa-125">The integration runtime node name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65dfa-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="65dfa-126">-ResourceGroupName</span></span>
<span data-ttu-id="65dfa-127">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="65dfa-127">The resource group name.</span></span>

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

### <span data-ttu-id="65dfa-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="65dfa-128">-ResourceId</span></span>
<span data-ttu-id="65dfa-129">ID för Azure-resursen.</span><span class="sxs-lookup"><span data-stu-id="65dfa-129">The Azure resource ID.</span></span>

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

### <span data-ttu-id="65dfa-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="65dfa-130">-WhatIf</span></span>
<span data-ttu-id="65dfa-131">Visar vad som händer om cmdleten körs men inte kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="65dfa-131">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

## <span data-ttu-id="65dfa-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="65dfa-132">INPUTS</span></span>

### <span data-ttu-id="65dfa-133">System. String</span><span class="sxs-lookup"><span data-stu-id="65dfa-133">System.String</span></span>
<span data-ttu-id="65dfa-134">Microsoft. Azure. commands. DataFactoryV2. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="65dfa-134">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>


## <span data-ttu-id="65dfa-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="65dfa-135">OUTPUTS</span></span>

### <span data-ttu-id="65dfa-136">System. Object</span><span class="sxs-lookup"><span data-stu-id="65dfa-136">System.Object</span></span>

## <span data-ttu-id="65dfa-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="65dfa-137">NOTES</span></span>

## <span data-ttu-id="65dfa-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="65dfa-138">RELATED LINKS</span></span>

