---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/remove-azdatafactoryv2integrationruntimenode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2IntegrationRuntimeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2IntegrationRuntimeNode.md
ms.openlocfilehash: dbf5b4eba8c6fe2dc55e55a58df79ed9b7d08afb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93754357"
---
# <span data-ttu-id="7d3fe-101">Remove-AzDataFactoryV2IntegrationRuntimeNode</span><span class="sxs-lookup"><span data-stu-id="7d3fe-101">Remove-AzDataFactoryV2IntegrationRuntimeNode</span></span>

## <span data-ttu-id="7d3fe-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7d3fe-102">SYNOPSIS</span></span>
<span data-ttu-id="7d3fe-103">Ta bort en nod med det angivna namnet i en integrations körning.</span><span class="sxs-lookup"><span data-stu-id="7d3fe-103">Remove a node with the given name on an integration runtime.</span></span>

## <span data-ttu-id="7d3fe-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7d3fe-104">SYNTAX</span></span>

### <span data-ttu-id="7d3fe-105">ByIntegrationRuntimeName (standard)</span><span class="sxs-lookup"><span data-stu-id="7d3fe-105">ByIntegrationRuntimeName (Default)</span></span>
```
Remove-AzDataFactoryV2IntegrationRuntimeNode -NodeName <String> [-Force] [-IntegrationRuntimeName] <String>
 [-ResourceGroupName] <String> [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7d3fe-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="7d3fe-106">ByResourceId</span></span>
```
Remove-AzDataFactoryV2IntegrationRuntimeNode -NodeName <String> [-Force] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7d3fe-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="7d3fe-107">ByIntegrationRuntimeObject</span></span>
```
Remove-AzDataFactoryV2IntegrationRuntimeNode -NodeName <String> [-Force] [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7d3fe-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7d3fe-108">DESCRIPTION</span></span>
<span data-ttu-id="7d3fe-109">Remove-AzDataFactoryV2IntegrationRuntimeNode cmdlet tar bort en nod i en integrations körning.</span><span class="sxs-lookup"><span data-stu-id="7d3fe-109">The Remove-AzDataFactoryV2IntegrationRuntimeNode cmdlet removes a node in an integration runtime.</span></span>

## <span data-ttu-id="7d3fe-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7d3fe-110">EXAMPLES</span></span>

### <span data-ttu-id="7d3fe-111">Exempel 1: ta bort en nod från en integrations körning</span><span class="sxs-lookup"><span data-stu-id="7d3fe-111">Example 1: Remove a node from an integration runtime</span></span>
```
PS C:\> Remove-AzDataFactoryV2IntegrationRuntimeNode -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir' -NodeName 'Node_1'
```

<span data-ttu-id="7d3fe-112">Det här kommandot tar bort en nod med namnet "Node_1" i integrations körningen med namnet "test-selfhost-IR" i prenumerationen för resurs gruppen med namnet "RG-test-dfv2" och data fabriken med namnet "test-DF-EU2".</span><span class="sxs-lookup"><span data-stu-id="7d3fe-112">This command removes an node named 'Node_1' in the integration runtime named 'test-selfhost-ir' in the subscription for the resource group named 'rg-test-dfv2' and data factory named 'test-df-eu2'.</span></span>

## <span data-ttu-id="7d3fe-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7d3fe-113">PARAMETERS</span></span>

### <span data-ttu-id="7d3fe-114">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="7d3fe-114">-DataFactoryName</span></span>
<span data-ttu-id="7d3fe-115">Namnet på data fabriken.</span><span class="sxs-lookup"><span data-stu-id="7d3fe-115">The data factory name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d3fe-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d3fe-116">-DefaultProfile</span></span>
<span data-ttu-id="7d3fe-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="7d3fe-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7d3fe-118">-Force</span><span class="sxs-lookup"><span data-stu-id="7d3fe-118">-Force</span></span>
<span data-ttu-id="7d3fe-119">Kör cmdleten utan att behöva bekräfta.</span><span class="sxs-lookup"><span data-stu-id="7d3fe-119">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="7d3fe-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7d3fe-120">-InputObject</span></span>
<span data-ttu-id="7d3fe-121">Integration runtime-objekt.</span><span class="sxs-lookup"><span data-stu-id="7d3fe-121">The integration runtime object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime
Parameter Sets: ByIntegrationRuntimeObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7d3fe-122">-IntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="7d3fe-122">-IntegrationRuntimeName</span></span>
<span data-ttu-id="7d3fe-123">Integrerings körens namn.</span><span class="sxs-lookup"><span data-stu-id="7d3fe-123">The integration runtime name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d3fe-124">-Nodnamn</span><span class="sxs-lookup"><span data-stu-id="7d3fe-124">-NodeName</span></span>
<span data-ttu-id="7d3fe-125">Integration runtime-nodnamnet.</span><span class="sxs-lookup"><span data-stu-id="7d3fe-125">The integration runtime node name.</span></span>

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

### <span data-ttu-id="7d3fe-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7d3fe-126">-ResourceGroupName</span></span>
<span data-ttu-id="7d3fe-127">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="7d3fe-127">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d3fe-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7d3fe-128">-ResourceId</span></span>
<span data-ttu-id="7d3fe-129">ID för Azure-resursen.</span><span class="sxs-lookup"><span data-stu-id="7d3fe-129">The Azure resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases: Id

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d3fe-130">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="7d3fe-130">-Confirm</span></span>
<span data-ttu-id="7d3fe-131">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="7d3fe-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7d3fe-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7d3fe-132">-WhatIf</span></span>
<span data-ttu-id="7d3fe-133">Visar vad som händer om cmdleten körs men inte kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="7d3fe-133">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="7d3fe-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d3fe-134">CommonParameters</span></span>
<span data-ttu-id="7d3fe-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7d3fe-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d3fe-136">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7d3fe-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d3fe-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7d3fe-137">INPUTS</span></span>

### <span data-ttu-id="7d3fe-138">System. String</span><span class="sxs-lookup"><span data-stu-id="7d3fe-138">System.String</span></span>

### <span data-ttu-id="7d3fe-139">Microsoft. Azure. commands. DataFactoryV2. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="7d3fe-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="7d3fe-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7d3fe-140">OUTPUTS</span></span>

### <span data-ttu-id="7d3fe-141">System. Void</span><span class="sxs-lookup"><span data-stu-id="7d3fe-141">System.Void</span></span>

## <span data-ttu-id="7d3fe-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7d3fe-142">NOTES</span></span>

## <span data-ttu-id="7d3fe-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7d3fe-143">RELATED LINKS</span></span>
