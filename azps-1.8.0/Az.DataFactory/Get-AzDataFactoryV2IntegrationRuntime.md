---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryv2integrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2IntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2IntegrationRuntime.md
ms.openlocfilehash: 96c635caef26a1dc90ae2646cb4899012105f526
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93754387"
---
# <span data-ttu-id="112ff-101">Get-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="112ff-101">Get-AzDataFactoryV2IntegrationRuntime</span></span>

## <span data-ttu-id="112ff-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="112ff-102">SYNOPSIS</span></span>
<span data-ttu-id="112ff-103">Hämtar information om integrerings körnas resurser.</span><span class="sxs-lookup"><span data-stu-id="112ff-103">Gets information about integration runtime resources.</span></span>

## <span data-ttu-id="112ff-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="112ff-104">SYNTAX</span></span>

### <span data-ttu-id="112ff-105">ByIntegrationRuntimeName (standard)</span><span class="sxs-lookup"><span data-stu-id="112ff-105">ByIntegrationRuntimeName (Default)</span></span>
```
Get-AzDataFactoryV2IntegrationRuntime [[-Name] <String>] [-Status] [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="112ff-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="112ff-106">ByResourceId</span></span>
```
Get-AzDataFactoryV2IntegrationRuntime [-Status] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="112ff-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="112ff-107">ByIntegrationRuntimeObject</span></span>
```
Get-AzDataFactoryV2IntegrationRuntime [-Status] [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="112ff-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="112ff-108">DESCRIPTION</span></span>
<span data-ttu-id="112ff-109">Get-AzDataFactoryV2IntegrationRuntime cmdlet får information om integrerings körningar i en data fabrik.</span><span class="sxs-lookup"><span data-stu-id="112ff-109">The Get-AzDataFactoryV2IntegrationRuntime cmdlet gets information about integration runtimes in a data factory.</span></span>
<span data-ttu-id="112ff-110">Om du anger namnet på en integrations körning får denna cmdlet information om integrations körningen.</span><span class="sxs-lookup"><span data-stu-id="112ff-110">If you specify the name of an integration runtime, this cmdlet gets information about that integration runtime.</span></span>
<span data-ttu-id="112ff-111">Om du inte anger ett namn visas den här cmdleten för att få information om alla integrerings körningar i en data fabrik.</span><span class="sxs-lookup"><span data-stu-id="112ff-111">If you do not specify a name, this cmdlet gets information about all of the integration runtimes in a data factory.</span></span>

## <span data-ttu-id="112ff-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="112ff-112">EXAMPLES</span></span>

### <span data-ttu-id="112ff-113">Exempel 1: lista alla integrations körningar i en data fabrik</span><span class="sxs-lookup"><span data-stu-id="112ff-113">Example 1: List all integration runtimes in a data factory</span></span>
```
PS C:\> Get-AzDataFactoryV2IntegrationRuntime -ResourceGroupName rg-test-dfv2 -DataFactoryName test-df-eu2

    ResourceGroupName DataFactoryName Name                   Description
    ----------------- --------------- ----                   -----------
    rg-test-dfv2      test-df-eu2     test-reserved-ir       Reserved IR
    rg-test-dfv2      test-df-eu2     test-dedicated-ir      Reserved IR
    rg-test-dfv2      test-df-eu2     test-selfhost-ir       selfhost IR
```

<span data-ttu-id="112ff-114">Visa alla integrerings körningar i data fabriken "test-DF-EU2".</span><span class="sxs-lookup"><span data-stu-id="112ff-114">List all integration runtimes in the data factory named 'test-df-eu2'.</span></span>

### <span data-ttu-id="112ff-115">Exempel 2: skaffa en dedikerad integrerings körning</span><span class="sxs-lookup"><span data-stu-id="112ff-115">Example 2: Get managed dedicated integration runtime</span></span>
```
PS C:\> Get-AzDataFactoryV2IntegrationRuntime -ResourceGroupName rg-test-dfv2 -DataFactoryName test-df-eu2 -Name test-dedicated-ir

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

<span data-ttu-id="112ff-116">Det här kommandot visar information om integrations körningen med namnet "test-Dedicated-IR" i prenumerationen för resurs gruppen "RG-test-dfv2" och data fabriken med namnet "test-DF-EU2".</span><span class="sxs-lookup"><span data-stu-id="112ff-116">This command displays information about the integration runtime named 'test-dedicated-ir' in the subscription for the resource group named 'rg-test-dfv2' and data factory named 'test-df-eu2'.</span></span>

### <span data-ttu-id="112ff-117">Exempel 3: få mer information om hur du kör hanterad dedikerad integrering</span><span class="sxs-lookup"><span data-stu-id="112ff-117">Example 3: Get managed dedicated integration runtime with detail status</span></span>
```
PS C:\> Get-AzDataFactoryV2IntegrationRuntime -ResourceGroupName rg-test-dfv2 -DataFactoryName test-df-eu2 -Name test-dedicated-ir -Status

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

<span data-ttu-id="112ff-118">Det här kommandot visar information om integrations körningen med namnet "test-Dedicated-IR" i prenumerationen för resurs gruppen "RG-test-dfv2" och data fabriken med namnet "test-DF-EU2".</span><span class="sxs-lookup"><span data-stu-id="112ff-118">This command displays information about the integration runtime named 'test-dedicated-ir' in the subscription for the resource group named 'rg-test-dfv2' and data factory named 'test-df-eu2'.</span></span>

### <span data-ttu-id="112ff-119">Exempel 4: hämta den självvärdbaserade integrerings körningen</span><span class="sxs-lookup"><span data-stu-id="112ff-119">Example 4: Get self-hosted integration runtime</span></span>
```
PS C:\> Get-AzDataFactoryV2IntegrationRuntime -ResourceGroupName rg-test-dfv2 -DataFactoryName test-df-eu2 -Name test-selfhost-ir

    ResourceGroupName DataFactoryName Name                 Description
    ----------------- --------------- ----                 -----------
    rg-test-dfv2      test-df-eu2     test-selfhost-ir     selfhost IR
```

<span data-ttu-id="112ff-120">Det här kommandot visar information om integrations körningen med namnet "test-Dedicated-IR" i prenumerationen för resurs gruppen "RG-test-dfv2" och data fabriken med namnet "test-DF-EU2".</span><span class="sxs-lookup"><span data-stu-id="112ff-120">This command displays information about the integration runtime named 'test-dedicated-ir' in the subscription for the resource group named 'rg-test-dfv2' and data factory named 'test-df-eu2'.</span></span>

## <span data-ttu-id="112ff-121">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="112ff-121">PARAMETERS</span></span>

### <span data-ttu-id="112ff-122">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="112ff-122">-DataFactoryName</span></span>
<span data-ttu-id="112ff-123">Namnet på data fabriken.</span><span class="sxs-lookup"><span data-stu-id="112ff-123">The data factory name.</span></span>

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

### <span data-ttu-id="112ff-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="112ff-124">-DefaultProfile</span></span>
<span data-ttu-id="112ff-125">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="112ff-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="112ff-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="112ff-126">-InputObject</span></span>
<span data-ttu-id="112ff-127">Integration runtime-objekt.</span><span class="sxs-lookup"><span data-stu-id="112ff-127">The integration runtime object.</span></span>

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

### <span data-ttu-id="112ff-128">-Namn</span><span class="sxs-lookup"><span data-stu-id="112ff-128">-Name</span></span>
<span data-ttu-id="112ff-129">Integrerings körens namn.</span><span class="sxs-lookup"><span data-stu-id="112ff-129">The integration runtime name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName
Aliases: IntegrationRuntimeName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="112ff-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="112ff-130">-ResourceGroupName</span></span>
<span data-ttu-id="112ff-131">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="112ff-131">The resource group name.</span></span>

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

### <span data-ttu-id="112ff-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="112ff-132">-ResourceId</span></span>
<span data-ttu-id="112ff-133">ID för Azure-resursen.</span><span class="sxs-lookup"><span data-stu-id="112ff-133">The Azure resource ID.</span></span>

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

### <span data-ttu-id="112ff-134">-Status</span><span class="sxs-lookup"><span data-stu-id="112ff-134">-Status</span></span>
<span data-ttu-id="112ff-135">Information om integreringens detalj status.</span><span class="sxs-lookup"><span data-stu-id="112ff-135">The integration runtime detail status.</span></span>

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

### <span data-ttu-id="112ff-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="112ff-136">CommonParameters</span></span>
<span data-ttu-id="112ff-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="112ff-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="112ff-138">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="112ff-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="112ff-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="112ff-139">INPUTS</span></span>

### <span data-ttu-id="112ff-140">System. String</span><span class="sxs-lookup"><span data-stu-id="112ff-140">System.String</span></span>

### <span data-ttu-id="112ff-141">Microsoft. Azure. commands. DataFactoryV2. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="112ff-141">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="112ff-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="112ff-142">OUTPUTS</span></span>

### <span data-ttu-id="112ff-143">Microsoft. Azure. commands. DataFactoryV2. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="112ff-143">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

### <span data-ttu-id="112ff-144">Microsoft. Azure. commands. DataFactoryV2. Models. PSManagedIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="112ff-144">Microsoft.Azure.Commands.DataFactoryV2.Models.PSManagedIntegrationRuntime</span></span>

### <span data-ttu-id="112ff-145">Microsoft. Azure. commands. DataFactoryV2. Models. PSSelfHostedIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="112ff-145">Microsoft.Azure.Commands.DataFactoryV2.Models.PSSelfHostedIntegrationRuntime</span></span>

### <span data-ttu-id="112ff-146">Microsoft. Azure. commands. DataFactoryV2. Models. PSLinkedIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="112ff-146">Microsoft.Azure.Commands.DataFactoryV2.Models.PSLinkedIntegrationRuntime</span></span>

## <span data-ttu-id="112ff-147">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="112ff-147">NOTES</span></span>
<span data-ttu-id="112ff-148">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, data, faktorer, kopiera, aktiviteter, integrerings körning</span><span class="sxs-lookup"><span data-stu-id="112ff-148">Keywords: azure, azurerm, arm, resource, management, manager, data, factories, copy, activities, integration runtime</span></span>

## <span data-ttu-id="112ff-149">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="112ff-149">RELATED LINKS</span></span>

[<span data-ttu-id="112ff-150">Set-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="112ff-150">Set-AzDataFactoryV2IntegrationRuntime</span></span>]()

[<span data-ttu-id="112ff-151">Remove-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="112ff-151">Remove-AzDataFactoryV2IntegrationRuntime</span></span>]()
