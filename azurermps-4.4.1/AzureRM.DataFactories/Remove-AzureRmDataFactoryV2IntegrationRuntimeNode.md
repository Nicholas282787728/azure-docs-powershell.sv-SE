---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2IntegrationRuntimeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2IntegrationRuntimeNode.md
ms.openlocfilehash: 4c46ebfb5031d64e685a77768ef6d4c7353d8462
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93579727"
---
# <span data-ttu-id="50127-101">Remove-AzureRmDataFactoryV2IntegrationRuntimeNode</span><span class="sxs-lookup"><span data-stu-id="50127-101">Remove-AzureRmDataFactoryV2IntegrationRuntimeNode</span></span>

## <span data-ttu-id="50127-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="50127-102">SYNOPSIS</span></span>
<span data-ttu-id="50127-103">Ta bort en nod med det angivna namnet i en integrations körning.</span><span class="sxs-lookup"><span data-stu-id="50127-103">Remove a node with the given name on an integration runtime.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="50127-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="50127-104">SYNTAX</span></span>

### <span data-ttu-id="50127-105">ByIntegrationRuntimeName (standard)</span><span class="sxs-lookup"><span data-stu-id="50127-105">ByIntegrationRuntimeName (Default)</span></span>
```
Remove-AzureRmDataFactoryV2IntegrationRuntimeNode -NodeName <String> [-Force]
 [-IntegrationRuntimeName] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="50127-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="50127-106">ByResourceId</span></span>
```
Remove-AzureRmDataFactoryV2IntegrationRuntimeNode -NodeName <String> [-Force] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="50127-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="50127-107">ByIntegrationRuntimeObject</span></span>
```
Remove-AzureRmDataFactoryV2IntegrationRuntimeNode -NodeName <String> [-Force]
 [-InputObject] <PSIntegrationRuntime> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="50127-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="50127-108">DESCRIPTION</span></span>
<span data-ttu-id="50127-109">Remove-AzureRmDataFactoryV2IntegrationRuntimeNode cmdlet tar bort en nod i en integrations körning.</span><span class="sxs-lookup"><span data-stu-id="50127-109">The Remove-AzureRmDataFactoryV2IntegrationRuntimeNode cmdlet removes a node in an integration runtime.</span></span>

## <span data-ttu-id="50127-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="50127-110">EXAMPLES</span></span>

### <span data-ttu-id="50127-111">Exempel 1: ta bort en nod från en integrations körning</span><span class="sxs-lookup"><span data-stu-id="50127-111">Example 1: Remove a node from an integration runtime</span></span>
```
PS C:\> Remove-AzureRmDataFactoryV2IntegrationRuntimeNode -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir' -NodeName 'Node_1'
```

<span data-ttu-id="50127-112">Det här kommandot tar bort en nod med namnet "Node_1" i integrations körningen med namnet "test-selfhost-IR" i prenumerationen för resurs gruppen med namnet "RG-test-dfv2" och data fabriken med namnet "test-DF-EU2".</span><span class="sxs-lookup"><span data-stu-id="50127-112">This command removes an node named 'Node_1' in the integration runtime named 'test-selfhost-ir' in the subscription for the resource group named 'rg-test-dfv2' and data factory named 'test-df-eu2'.</span></span>

## <span data-ttu-id="50127-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="50127-113">PARAMETERS</span></span>

### <span data-ttu-id="50127-114">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="50127-114">-Confirm</span></span>
<span data-ttu-id="50127-115">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="50127-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="50127-116">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="50127-116">-DataFactoryName</span></span>
<span data-ttu-id="50127-117">Namnet på data fabriken.</span><span class="sxs-lookup"><span data-stu-id="50127-117">The data factory name.</span></span>

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

### <span data-ttu-id="50127-118">-Force</span><span class="sxs-lookup"><span data-stu-id="50127-118">-Force</span></span>
<span data-ttu-id="50127-119">Kör cmdleten utan att behöva bekräfta.</span><span class="sxs-lookup"><span data-stu-id="50127-119">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="50127-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="50127-120">-InputObject</span></span>
<span data-ttu-id="50127-121">Integration runtime-objekt.</span><span class="sxs-lookup"><span data-stu-id="50127-121">The integration runtime object.</span></span>

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

### <span data-ttu-id="50127-122">-IntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="50127-122">-IntegrationRuntimeName</span></span>
<span data-ttu-id="50127-123">Integrerings körens namn.</span><span class="sxs-lookup"><span data-stu-id="50127-123">The integration runtime name.</span></span>

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

### <span data-ttu-id="50127-124">-Nodnamn</span><span class="sxs-lookup"><span data-stu-id="50127-124">-NodeName</span></span>
<span data-ttu-id="50127-125">Integration runtime-nodnamnet.</span><span class="sxs-lookup"><span data-stu-id="50127-125">The integration runtime node name.</span></span>

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

### <span data-ttu-id="50127-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="50127-126">-ResourceGroupName</span></span>
<span data-ttu-id="50127-127">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="50127-127">The resource group name.</span></span>

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

### <span data-ttu-id="50127-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="50127-128">-ResourceId</span></span>
<span data-ttu-id="50127-129">ID för Azure-resursen.</span><span class="sxs-lookup"><span data-stu-id="50127-129">The Azure resource ID.</span></span>

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

### <span data-ttu-id="50127-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="50127-130">-WhatIf</span></span>
<span data-ttu-id="50127-131">Visar vad som händer om cmdleten körs men inte kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="50127-131">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="50127-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50127-132">-DefaultProfile</span></span>
<span data-ttu-id="50127-133">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="50127-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="50127-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50127-134">CommonParameters</span></span>
<span data-ttu-id="50127-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="50127-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50127-136">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="50127-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50127-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="50127-137">INPUTS</span></span>

### <span data-ttu-id="50127-138">System. String</span><span class="sxs-lookup"><span data-stu-id="50127-138">System.String</span></span>
<span data-ttu-id="50127-139">Microsoft. Azure. commands. DataFactoryV2. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="50127-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="50127-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="50127-140">OUTPUTS</span></span>

### <span data-ttu-id="50127-141">System. Object</span><span class="sxs-lookup"><span data-stu-id="50127-141">System.Object</span></span>

## <span data-ttu-id="50127-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="50127-142">NOTES</span></span>

## <span data-ttu-id="50127-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="50127-143">RELATED LINKS</span></span>

