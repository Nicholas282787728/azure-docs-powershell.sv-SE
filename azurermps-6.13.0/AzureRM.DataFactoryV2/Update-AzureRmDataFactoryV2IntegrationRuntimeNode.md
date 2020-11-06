---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/update-azurermdatafactoryv2integrationruntimenode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Update-AzureRmDataFactoryV2IntegrationRuntimeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Update-AzureRmDataFactoryV2IntegrationRuntimeNode.md
ms.openlocfilehash: a69e051fb8f2cba30fba8419a818346e044f8462
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93577051"
---
# <span data-ttu-id="a8156-101">Update-AzureRmDataFactoryV2IntegrationRuntimeNode</span><span class="sxs-lookup"><span data-stu-id="a8156-101">Update-AzureRmDataFactoryV2IntegrationRuntimeNode</span></span>

## <span data-ttu-id="a8156-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a8156-102">SYNOPSIS</span></span>
<span data-ttu-id="a8156-103">Uppdaterar noden för integrering med egen värd.</span><span class="sxs-lookup"><span data-stu-id="a8156-103">Updates self-hosted integration runtime node.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a8156-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a8156-104">SYNTAX</span></span>

### <span data-ttu-id="a8156-105">ByIntegrationRuntimeName (standard)</span><span class="sxs-lookup"><span data-stu-id="a8156-105">ByIntegrationRuntimeName (Default)</span></span>
```
Update-AzureRmDataFactoryV2IntegrationRuntimeNode -Name <String> -ConcurrentJobsLimit <Int32>
 [-IntegrationRuntimeName] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a8156-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="a8156-106">ByResourceId</span></span>
```
Update-AzureRmDataFactoryV2IntegrationRuntimeNode -Name <String> -ConcurrentJobsLimit <Int32>
 [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a8156-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="a8156-107">ByIntegrationRuntimeObject</span></span>
```
Update-AzureRmDataFactoryV2IntegrationRuntimeNode -Name <String> -ConcurrentJobsLimit <Int32>
 [-InputObject] <PSIntegrationRuntime> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a8156-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a8156-108">DESCRIPTION</span></span>
<span data-ttu-id="a8156-109">Cmdleten **Update-AzureRmDataFactoryV2IntegrationRuntimeNode** uppdaterar egenskaper för den självvärdbaserade integrations körnings miljön i en data fabrik.</span><span class="sxs-lookup"><span data-stu-id="a8156-109">The **Update-AzureRmDataFactoryV2IntegrationRuntimeNode** cmdlet updates properties of self-hosted integration runtime node in a data factory.</span></span> <span data-ttu-id="a8156-110">För närvarande stöds endast uppdatering av ' ConcurrentJobsLimit '.</span><span class="sxs-lookup"><span data-stu-id="a8156-110">Currently only supports updating 'ConcurrentJobsLimit'.</span></span>

## <span data-ttu-id="a8156-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a8156-111">EXAMPLES</span></span>

### <span data-ttu-id="a8156-112">Exempel 1: uppdatera noden för integrering med egen värd</span><span class="sxs-lookup"><span data-stu-id="a8156-112">Example 1: Updates self-hosted integration runtime node</span></span>
```
PS C:\> Update-AzureRmDataFactoryV2IntegrationRuntimeNode `
    -ResourceGroupName 'rg-test-dfv2' `
    -DataFactoryName 'test-df-eu2' `
    -IntegrationRuntimeName 'test-selfhost-ir' `
    -Name 'Node_1' `
    -ConcurrentJobsLimit 3
```

<span data-ttu-id="a8156-113">Cmdleten uppdaterar ' ConcurrentJobsLimit ' till 3 för nod ' Node_1 ' i test-selfhost-IR för självvärdisk integrering.</span><span class="sxs-lookup"><span data-stu-id="a8156-113">The cmdlet updates 'ConcurrentJobsLimit' to 3 for node 'Node_1' in self-hosted integration runtime 'test-selfhost-ir'.</span></span>

## <span data-ttu-id="a8156-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a8156-114">PARAMETERS</span></span>

### <span data-ttu-id="a8156-115">-ConcurrentJobsLimit</span><span class="sxs-lookup"><span data-stu-id="a8156-115">-ConcurrentJobsLimit</span></span>
<span data-ttu-id="a8156-116">Antalet samtidiga jobb som får köras på integration runtime-noden.</span><span class="sxs-lookup"><span data-stu-id="a8156-116">The number of concurrent jobs permitted to run on the integration runtime node.</span></span>
<span data-ttu-id="a8156-117">Värden mellan 1 och maxConcurrentJobs är tillåtna.</span><span class="sxs-lookup"><span data-stu-id="a8156-117">Values between 1 and maxConcurrentJobs are allowed.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8156-118">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="a8156-118">-DataFactoryName</span></span>
<span data-ttu-id="a8156-119">Namnet på data fabriken.</span><span class="sxs-lookup"><span data-stu-id="a8156-119">The data factory name.</span></span>

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

### <span data-ttu-id="a8156-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8156-120">-DefaultProfile</span></span>
<span data-ttu-id="a8156-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a8156-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a8156-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a8156-122">-InputObject</span></span>
<span data-ttu-id="a8156-123">Integration runtime-objekt.</span><span class="sxs-lookup"><span data-stu-id="a8156-123">The integration runtime object.</span></span>

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

### <span data-ttu-id="a8156-124">-IntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="a8156-124">-IntegrationRuntimeName</span></span>
<span data-ttu-id="a8156-125">Integrerings körens namn.</span><span class="sxs-lookup"><span data-stu-id="a8156-125">The integration runtime name.</span></span>

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

### <span data-ttu-id="a8156-126">-Namn</span><span class="sxs-lookup"><span data-stu-id="a8156-126">-Name</span></span>
<span data-ttu-id="a8156-127">Integration runtime-nodnamnet.</span><span class="sxs-lookup"><span data-stu-id="a8156-127">The integration runtime node name.</span></span>

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

### <span data-ttu-id="a8156-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a8156-128">-ResourceGroupName</span></span>
<span data-ttu-id="a8156-129">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="a8156-129">The resource group name.</span></span>

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

### <span data-ttu-id="a8156-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a8156-130">-ResourceId</span></span>
<span data-ttu-id="a8156-131">ID för Azure-resursen.</span><span class="sxs-lookup"><span data-stu-id="a8156-131">The Azure resource ID.</span></span>

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

### <span data-ttu-id="a8156-132">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="a8156-132">-Confirm</span></span>
<span data-ttu-id="a8156-133">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="a8156-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a8156-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a8156-134">-WhatIf</span></span>
<span data-ttu-id="a8156-135">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="a8156-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a8156-136">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="a8156-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a8156-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8156-137">CommonParameters</span></span>
<span data-ttu-id="a8156-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a8156-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8156-139">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a8156-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8156-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a8156-140">INPUTS</span></span>

### <span data-ttu-id="a8156-141">System. String</span><span class="sxs-lookup"><span data-stu-id="a8156-141">System.String</span></span>

### <span data-ttu-id="a8156-142">Microsoft. Azure. commands. DataFactoryV2. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="a8156-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>
<span data-ttu-id="a8156-143">Parametrar: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="a8156-143">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="a8156-144">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a8156-144">OUTPUTS</span></span>

### <span data-ttu-id="a8156-145">Microsoft. Azure. commands. DataFactoryV2. Models. PSSelfHostedIntegrationRuntimeNode</span><span class="sxs-lookup"><span data-stu-id="a8156-145">Microsoft.Azure.Commands.DataFactoryV2.Models.PSSelfHostedIntegrationRuntimeNode</span></span>

## <span data-ttu-id="a8156-146">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a8156-146">NOTES</span></span>
<span data-ttu-id="a8156-147">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, data, faktorer, kopiera, aktiviteter, integrerings körning</span><span class="sxs-lookup"><span data-stu-id="a8156-147">Keywords: azure, azurerm, arm, resource, management, manager, data, factories, copy, activities, integration runtime</span></span>

## <span data-ttu-id="a8156-148">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a8156-148">RELATED LINKS</span></span>

<span data-ttu-id="a8156-149">[Set-AzureRmDataFactoryV2IntegrationRuntime]() 
 [Get-AzureRmDataFactoryV2IntegrationRuntime]()</span><span class="sxs-lookup"><span data-stu-id="a8156-149">[Set-AzureRmDataFactoryV2IntegrationRuntime]()
[Get-AzureRmDataFactoryV2IntegrationRuntime]()</span></span>

