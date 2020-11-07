---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/remove-azurermdatafactoryv2integrationruntimenode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2IntegrationRuntimeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2IntegrationRuntimeNode.md
ms.openlocfilehash: 413125f6bcc9935ffae66551ba5bd178eb4a3c53
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93755204"
---
# <span data-ttu-id="478ac-101">Remove-AzureRmDataFactoryV2IntegrationRuntimeNode</span><span class="sxs-lookup"><span data-stu-id="478ac-101">Remove-AzureRmDataFactoryV2IntegrationRuntimeNode</span></span>

## <span data-ttu-id="478ac-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="478ac-102">SYNOPSIS</span></span>
<span data-ttu-id="478ac-103">Ta bort en nod med det angivna namnet i en integrations körning.</span><span class="sxs-lookup"><span data-stu-id="478ac-103">Remove a node with the given name on an integration runtime.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="478ac-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="478ac-104">SYNTAX</span></span>

### <span data-ttu-id="478ac-105">ByIntegrationRuntimeName (standard)</span><span class="sxs-lookup"><span data-stu-id="478ac-105">ByIntegrationRuntimeName (Default)</span></span>
```
Remove-AzureRmDataFactoryV2IntegrationRuntimeNode -NodeName <String> [-Force]
 [-IntegrationRuntimeName] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="478ac-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="478ac-106">ByResourceId</span></span>
```
Remove-AzureRmDataFactoryV2IntegrationRuntimeNode -NodeName <String> [-Force] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="478ac-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="478ac-107">ByIntegrationRuntimeObject</span></span>
```
Remove-AzureRmDataFactoryV2IntegrationRuntimeNode -NodeName <String> [-Force]
 [-InputObject] <PSIntegrationRuntime> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="478ac-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="478ac-108">DESCRIPTION</span></span>
<span data-ttu-id="478ac-109">Remove-AzureRmDataFactoryV2IntegrationRuntimeNode cmdlet tar bort en nod i en integrations körning.</span><span class="sxs-lookup"><span data-stu-id="478ac-109">The Remove-AzureRmDataFactoryV2IntegrationRuntimeNode cmdlet removes a node in an integration runtime.</span></span>

## <span data-ttu-id="478ac-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="478ac-110">EXAMPLES</span></span>

### <span data-ttu-id="478ac-111">Exempel 1: ta bort en nod från en integrations körning</span><span class="sxs-lookup"><span data-stu-id="478ac-111">Example 1: Remove a node from an integration runtime</span></span>
```
PS C:\> Remove-AzureRmDataFactoryV2IntegrationRuntimeNode -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir' -NodeName 'Node_1'
```

<span data-ttu-id="478ac-112">Det här kommandot tar bort en nod med namnet "Node_1" i integrations körningen med namnet "test-selfhost-IR" i prenumerationen för resurs gruppen med namnet "RG-test-dfv2" och data fabriken med namnet "test-DF-EU2".</span><span class="sxs-lookup"><span data-stu-id="478ac-112">This command removes an node named 'Node_1' in the integration runtime named 'test-selfhost-ir' in the subscription for the resource group named 'rg-test-dfv2' and data factory named 'test-df-eu2'.</span></span>

## <span data-ttu-id="478ac-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="478ac-113">PARAMETERS</span></span>

### <span data-ttu-id="478ac-114">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="478ac-114">-DataFactoryName</span></span>
<span data-ttu-id="478ac-115">Namnet på data fabriken.</span><span class="sxs-lookup"><span data-stu-id="478ac-115">The data factory name.</span></span>

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

### <span data-ttu-id="478ac-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="478ac-116">-DefaultProfile</span></span>
<span data-ttu-id="478ac-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="478ac-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="478ac-118">-Force</span><span class="sxs-lookup"><span data-stu-id="478ac-118">-Force</span></span>
<span data-ttu-id="478ac-119">Kör cmdleten utan att behöva bekräfta.</span><span class="sxs-lookup"><span data-stu-id="478ac-119">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="478ac-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="478ac-120">-InputObject</span></span>
<span data-ttu-id="478ac-121">Integration runtime-objekt.</span><span class="sxs-lookup"><span data-stu-id="478ac-121">The integration runtime object.</span></span>

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

### <span data-ttu-id="478ac-122">-IntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="478ac-122">-IntegrationRuntimeName</span></span>
<span data-ttu-id="478ac-123">Integrerings körens namn.</span><span class="sxs-lookup"><span data-stu-id="478ac-123">The integration runtime name.</span></span>

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

### <span data-ttu-id="478ac-124">-Nodnamn</span><span class="sxs-lookup"><span data-stu-id="478ac-124">-NodeName</span></span>
<span data-ttu-id="478ac-125">Integration runtime-nodnamnet.</span><span class="sxs-lookup"><span data-stu-id="478ac-125">The integration runtime node name.</span></span>

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

### <span data-ttu-id="478ac-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="478ac-126">-ResourceGroupName</span></span>
<span data-ttu-id="478ac-127">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="478ac-127">The resource group name.</span></span>

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

### <span data-ttu-id="478ac-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="478ac-128">-ResourceId</span></span>
<span data-ttu-id="478ac-129">ID för Azure-resursen.</span><span class="sxs-lookup"><span data-stu-id="478ac-129">The Azure resource ID.</span></span>

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

### <span data-ttu-id="478ac-130">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="478ac-130">-Confirm</span></span>
<span data-ttu-id="478ac-131">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="478ac-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="478ac-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="478ac-132">-WhatIf</span></span>
<span data-ttu-id="478ac-133">Visar vad som händer om cmdleten körs men inte kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="478ac-133">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="478ac-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="478ac-134">CommonParameters</span></span>
<span data-ttu-id="478ac-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="478ac-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="478ac-136">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="478ac-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="478ac-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="478ac-137">INPUTS</span></span>

### <span data-ttu-id="478ac-138">System. String</span><span class="sxs-lookup"><span data-stu-id="478ac-138">System.String</span></span>

### <span data-ttu-id="478ac-139">Microsoft. Azure. commands. DataFactoryV2. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="478ac-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>
<span data-ttu-id="478ac-140">Parametrar: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="478ac-140">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="478ac-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="478ac-141">OUTPUTS</span></span>

### <span data-ttu-id="478ac-142">System. Void</span><span class="sxs-lookup"><span data-stu-id="478ac-142">System.Void</span></span>

## <span data-ttu-id="478ac-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="478ac-143">NOTES</span></span>

## <span data-ttu-id="478ac-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="478ac-144">RELATED LINKS</span></span>
