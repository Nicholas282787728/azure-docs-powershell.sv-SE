---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2IntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2IntegrationRuntime.md
gitcommit: https://github.com/Azure/azure-powershell/blob/db8032a9100d47fd3aa4248c7807d8e0bb538e83
ms.openlocfilehash: ef5b99a27c547ec1e71c2339de8f4c9536549981
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93585683"
---
# <span data-ttu-id="b8fee-101">Get-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="b8fee-101">Get-AzureRmDataFactoryV2IntegrationRuntime</span></span>

## <span data-ttu-id="b8fee-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b8fee-102">SYNOPSIS</span></span>
<span data-ttu-id="b8fee-103">Hämtar information om integrerings körnas resurser.</span><span class="sxs-lookup"><span data-stu-id="b8fee-103">Gets information about integration runtime resources.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b8fee-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b8fee-104">SYNTAX</span></span>

### <span data-ttu-id="b8fee-105">ByIntegrationRuntimeName (standard)</span><span class="sxs-lookup"><span data-stu-id="b8fee-105">ByIntegrationRuntimeName (Default)</span></span>
```
Get-AzureRmDataFactoryV2IntegrationRuntime [[-Name] <String>] [-Status] [-ResourceGroupName] <String>
 [-DataFactoryName] <String>
```

### <span data-ttu-id="b8fee-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="b8fee-106">ByResourceId</span></span>
```
Get-AzureRmDataFactoryV2IntegrationRuntime [-Status] [-ResourceId] <String>
```

### <span data-ttu-id="b8fee-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="b8fee-107">ByIntegrationRuntimeObject</span></span>
```
Get-AzureRmDataFactoryV2IntegrationRuntime [-Status] [-InputObject] <PSIntegrationRuntime>
```

## <span data-ttu-id="b8fee-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b8fee-108">DESCRIPTION</span></span>
<span data-ttu-id="b8fee-109">Get-AzureRmDataFactoryV2IntegrationRuntime cmdlet får information om integrerings körningar i en data fabrik.</span><span class="sxs-lookup"><span data-stu-id="b8fee-109">The Get-AzureRmDataFactoryV2IntegrationRuntime cmdlet gets information about integration runtimes in a data factory.</span></span>
<span data-ttu-id="b8fee-110">Om du anger namnet på en integrations körning får denna cmdlet information om integrations körningen.</span><span class="sxs-lookup"><span data-stu-id="b8fee-110">If you specify the name of an integration runtime, this cmdlet gets information about that integration runtime.</span></span>
<span data-ttu-id="b8fee-111">Om du inte anger ett namn visas den här cmdleten för att få information om alla integrerings körningar i en data fabrik.</span><span class="sxs-lookup"><span data-stu-id="b8fee-111">If you do not specify a name, this cmdlet gets information about all of the integration runtimes in a data factory.</span></span>

## <span data-ttu-id="b8fee-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b8fee-112">EXAMPLES</span></span>

### <span data-ttu-id="b8fee-113">Exempel 1: lista alla integrations körningar i en data fabrik</span><span class="sxs-lookup"><span data-stu-id="b8fee-113">Example 1: List all integration runtimes in a data factory</span></span>
```
PS C:\> Get-AzureRmDataFactoryV2IntegrationRuntime -ResourceGroupName rg-test-dfv2 -DataFactoryName test-df-eu2

    ResourceGroupName DataFactoryName Name                   Description
    ----------------- --------------- ----                   -----------
    rg-test-dfv2      test-df-eu2     test-reserved-ir       Reserved IR
    rg-test-dfv2      test-df-eu2     test-dedicated-ir      Reserved IR
    rg-test-dfv2      test-df-eu2     test-selfhost-ir       selfhost IR
```

<span data-ttu-id="b8fee-114">Visa alla integrerings körningar i data fabriken "test-DF-EU2".</span><span class="sxs-lookup"><span data-stu-id="b8fee-114">List all integration runtimes in the data factory named 'test-df-eu2'.</span></span>

### <span data-ttu-id="b8fee-115">Exempel 2: skaffa en dedikerad integrerings körning</span><span class="sxs-lookup"><span data-stu-id="b8fee-115">Example 2: Get managed dedicated integration runtime</span></span>
```
PS C:\> Get-AzureRmDataFactoryV2IntegrationRuntime -ResourceGroupName rg-test-dfv2 -DataFactoryName test-df-eu2 -Name test-dedicated-ir

    Location                     : West US
    NodeSize                     : Standard_D1_v2
    NodeCount                    : 1
    MaxParallelExecutionsPerNode : 1
    CatalogServerEndpoint        : test.database.windows.net
    CatalogAdminUserName         : test
    CatalogAdminPassword         : **********
    CatalogPricingTier           : S1
    VNetId                       : 
    Subnet                       : 
    State                        : Starting
    ResourceGroupName            : rg-test-dfv2
    DataFactoryName              : test-df-eu2
    Name                         : test-dedicated-ir
    Description                  : Reserved IR
```

<span data-ttu-id="b8fee-116">Det här kommandot visar information om integrations körningen med namnet "test-Dedicated-IR" i prenumerationen för resurs gruppen "RG-test-dfv2" och data fabriken med namnet "test-DF-EU2".</span><span class="sxs-lookup"><span data-stu-id="b8fee-116">This command displays information about the integration runtime named 'test-dedicated-ir' in the subscription for the resource group named 'rg-test-dfv2' and data factory named 'test-df-eu2'.</span></span>

### <span data-ttu-id="b8fee-117">Exempel 3: få mer information om hur du kör hanterad dedikerad integrering</span><span class="sxs-lookup"><span data-stu-id="b8fee-117">Example 3: Get managed dedicated integration runtime with detail status</span></span>
```
PS C:\> Get-AzureRmDataFactoryV2IntegrationRuntime -ResourceGroupName rg-test-dfv2 -DataFactoryName test-df-eu2 -Name test-dedicated-ir -Status

    CreateTime                   : 
    Nodes                        : 
    OtherErrors                  : 
    LastOperation                : 
    State                        : Initial
    Location                     : West US
    NodeSize                     : Standard_D1_v2
    NodeCount                    : 1
    MaxParallelExecutionsPerNode : 1
    CatalogServerEndpoint        : test.database.windows.net
    CatalogAdminUserName         : test
    CatalogAdminPassword         : **********
    CatalogPricingTier           : S1
    VNetId                       : 
    Subnet                       : 
    ResourceGroupName            : rg-test-dfv2
    DataFactoryName              : test-df-eu2
    Name                         : test-dedicated-ir
    Description                  : Reserved IR
```

<span data-ttu-id="b8fee-118">Det här kommandot visar information om integrations körningen med namnet "test-Dedicated-IR" i prenumerationen för resurs gruppen "RG-test-dfv2" och data fabriken med namnet "test-DF-EU2".</span><span class="sxs-lookup"><span data-stu-id="b8fee-118">This command displays information about the integration runtime named 'test-dedicated-ir' in the subscription for the resource group named 'rg-test-dfv2' and data factory named 'test-df-eu2'.</span></span>

### <span data-ttu-id="b8fee-119">Exempel 4: hämta den självvärdbaserade integrerings körningen</span><span class="sxs-lookup"><span data-stu-id="b8fee-119">Example 4: Get self-hosted integration runtime</span></span>
```
PS C:\> Get-AzureRmDataFactoryV2IntegrationRuntime -ResourceGroupName rg-test-dfv2 -DataFactoryName test-df-eu2 -Name test-selfhost-ir

    ResourceGroupName DataFactoryName Name                 Description
    ----------------- --------------- ----                 -----------
    rg-test-dfv2      test-df-eu2     test-selfhost-ir     selfhost IR
```

<span data-ttu-id="b8fee-120">Det här kommandot visar information om integrations körningen med namnet "test-Dedicated-IR" i prenumerationen för resurs gruppen "RG-test-dfv2" och data fabriken med namnet "test-DF-EU2".</span><span class="sxs-lookup"><span data-stu-id="b8fee-120">This command displays information about the integration runtime named 'test-dedicated-ir' in the subscription for the resource group named 'rg-test-dfv2' and data factory named 'test-df-eu2'.</span></span>

## <span data-ttu-id="b8fee-121">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b8fee-121">PARAMETERS</span></span>

### <span data-ttu-id="b8fee-122">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="b8fee-122">-DataFactoryName</span></span>
<span data-ttu-id="b8fee-123">Namnet på data fabriken.</span><span class="sxs-lookup"><span data-stu-id="b8fee-123">The data factory name.</span></span>

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

### <span data-ttu-id="b8fee-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b8fee-124">-InputObject</span></span>
<span data-ttu-id="b8fee-125">Integration runtime-objekt.</span><span class="sxs-lookup"><span data-stu-id="b8fee-125">The integration runtime object.</span></span>

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

### <span data-ttu-id="b8fee-126">-Namn</span><span class="sxs-lookup"><span data-stu-id="b8fee-126">-Name</span></span>
<span data-ttu-id="b8fee-127">Integrerings körens namn.</span><span class="sxs-lookup"><span data-stu-id="b8fee-127">The integration runtime name.</span></span>

```yaml
Type: String
Parameter Sets: ByIntegrationRuntimeName
Aliases: IntegrationRuntimeName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b8fee-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b8fee-128">-ResourceGroupName</span></span>
<span data-ttu-id="b8fee-129">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="b8fee-129">The resource group name.</span></span>

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

### <span data-ttu-id="b8fee-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b8fee-130">-ResourceId</span></span>
<span data-ttu-id="b8fee-131">ID för Azure-resursen.</span><span class="sxs-lookup"><span data-stu-id="b8fee-131">The Azure resource ID.</span></span>

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

### <span data-ttu-id="b8fee-132">-Status</span><span class="sxs-lookup"><span data-stu-id="b8fee-132">-Status</span></span>
<span data-ttu-id="b8fee-133">Information om integreringens detalj status.</span><span class="sxs-lookup"><span data-stu-id="b8fee-133">The integration runtime detail status.</span></span>

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

## <span data-ttu-id="b8fee-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b8fee-134">INPUTS</span></span>

### <span data-ttu-id="b8fee-135">System. String</span><span class="sxs-lookup"><span data-stu-id="b8fee-135">System.String</span></span>
<span data-ttu-id="b8fee-136">Microsoft. Azure. commands. DataFactoryV2. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="b8fee-136">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>


## <span data-ttu-id="b8fee-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b8fee-137">OUTPUTS</span></span>

### <span data-ttu-id="b8fee-138">System. Collections. Generic. list ' 1 [[Microsoft. Azure. commands. DataFactoryV2. Models. PSIntegrationRuntime, Microsoft. Azure. commands. DataFactoryV2, version = 0.1.9.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="b8fee-138">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime, Microsoft.Azure.Commands.DataFactoryV2, Version=0.1.9.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="b8fee-139">Microsoft. Azure. commands. DataFactoryV2. Models. PSManagedIntegrationRuntime Microsoft. Azure. commands. DataFactoryV2. Models. PSSelfHostedIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="b8fee-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSManagedIntegrationRuntime Microsoft.Azure.Commands.DataFactoryV2.Models.PSSelfHostedIntegrationRuntime</span></span>


## <span data-ttu-id="b8fee-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b8fee-140">NOTES</span></span>
<span data-ttu-id="b8fee-141">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, data, faktorer, kopiera, aktiviteter, integrerings körning</span><span class="sxs-lookup"><span data-stu-id="b8fee-141">Keywords: azure, azurerm, arm, resource, management, manager, data, factories, copy, activities, integration runtime</span></span>

## <span data-ttu-id="b8fee-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b8fee-142">RELATED LINKS</span></span>
[<span data-ttu-id="b8fee-143">Set-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="b8fee-143">Set-AzureRmDataFactoryV2IntegrationRuntime</span></span>]()

[<span data-ttu-id="b8fee-144">Remove-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="b8fee-144">Remove-AzureRmDataFactoryV2IntegrationRuntime</span></span>]()
