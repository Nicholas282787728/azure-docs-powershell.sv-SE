---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryv2integrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2IntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2IntegrationRuntime.md
ms.openlocfilehash: 5525dc4613fc1d6bccc56e27de065151b1890f7d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94260256"
---
# <span data-ttu-id="8f8c6-101">Get-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="8f8c6-101">Get-AzDataFactoryV2IntegrationRuntime</span></span>

## <span data-ttu-id="8f8c6-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8f8c6-102">SYNOPSIS</span></span>
<span data-ttu-id="8f8c6-103">Hämtar information om integrerings körnas resurser.</span><span class="sxs-lookup"><span data-stu-id="8f8c6-103">Gets information about integration runtime resources.</span></span>

## <span data-ttu-id="8f8c6-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8f8c6-104">SYNTAX</span></span>

### <span data-ttu-id="8f8c6-105">ByIntegrationRuntimeName (standard)</span><span class="sxs-lookup"><span data-stu-id="8f8c6-105">ByIntegrationRuntimeName (Default)</span></span>
```
Get-AzDataFactoryV2IntegrationRuntime [[-Name] <String>] [-Status] [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8f8c6-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="8f8c6-106">ByResourceId</span></span>
```
Get-AzDataFactoryV2IntegrationRuntime [-Status] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8f8c6-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="8f8c6-107">ByIntegrationRuntimeObject</span></span>
```
Get-AzDataFactoryV2IntegrationRuntime [-Status] [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8f8c6-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8f8c6-108">DESCRIPTION</span></span>
<span data-ttu-id="8f8c6-109">Get-AzDataFactoryV2IntegrationRuntime cmdlet får information om integrerings körningar i en data fabrik.</span><span class="sxs-lookup"><span data-stu-id="8f8c6-109">The Get-AzDataFactoryV2IntegrationRuntime cmdlet gets information about integration runtimes in a data factory.</span></span>
<span data-ttu-id="8f8c6-110">Om du anger namnet på en integrations körning får denna cmdlet information om integrations körningen.</span><span class="sxs-lookup"><span data-stu-id="8f8c6-110">If you specify the name of an integration runtime, this cmdlet gets information about that integration runtime.</span></span>
<span data-ttu-id="8f8c6-111">Om du inte anger ett namn visas den här cmdleten för att få information om alla integrerings körningar i en data fabrik.</span><span class="sxs-lookup"><span data-stu-id="8f8c6-111">If you do not specify a name, this cmdlet gets information about all of the integration runtimes in a data factory.</span></span>

## <span data-ttu-id="8f8c6-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8f8c6-112">EXAMPLES</span></span>

### <span data-ttu-id="8f8c6-113">Exempel 1: lista alla integrations körningar i en data fabrik</span><span class="sxs-lookup"><span data-stu-id="8f8c6-113">Example 1: List all integration runtimes in a data factory</span></span>
```
PS C:\> Get-AzDataFactoryV2IntegrationRuntime -ResourceGroupName rg-test-dfv2 -DataFactoryName test-df-eu2

    ResourceGroupName DataFactoryName Name                   Description
    ----------------- --------------- ----                   -----------
    rg-test-dfv2      test-df-eu2     test-reserved-ir       Reserved IR
    rg-test-dfv2      test-df-eu2     test-dedicated-ir      Reserved IR
    rg-test-dfv2      test-df-eu2     test-selfhost-ir       selfhost IR
```

<span data-ttu-id="8f8c6-114">Visa alla integrerings körningar i data fabriken "test-DF-EU2".</span><span class="sxs-lookup"><span data-stu-id="8f8c6-114">List all integration runtimes in the data factory named 'test-df-eu2'.</span></span>

### <span data-ttu-id="8f8c6-115">Exempel 2: skaffa en dedikerad integrerings körning</span><span class="sxs-lookup"><span data-stu-id="8f8c6-115">Example 2: Get managed dedicated integration runtime</span></span>
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
    PublicIPs                    : 
    State                        : Starting
    ResourceGroupName            : rg-test-dfv2
    DataFactoryName              : test-df-eu2
    Name                         : test-dedicated-ir
    Description                  : Reserved IR
```

<span data-ttu-id="8f8c6-116">Det här kommandot visar information om integrations körningen med namnet "test-Dedicated-IR" i prenumerationen för resurs gruppen "RG-test-dfv2" och data fabriken med namnet "test-DF-EU2".</span><span class="sxs-lookup"><span data-stu-id="8f8c6-116">This command displays information about the integration runtime named 'test-dedicated-ir' in the subscription for the resource group named 'rg-test-dfv2' and data factory named 'test-df-eu2'.</span></span>

### <span data-ttu-id="8f8c6-117">Exempel 3: få mer information om hur du kör hanterad dedikerad integrering</span><span class="sxs-lookup"><span data-stu-id="8f8c6-117">Example 3: Get managed dedicated integration runtime with detail status</span></span>
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
    PublicIPs                    : 
    ResourceGroupName            : rg-test-dfv2
    DataFactoryName              : test-df-eu2
    Name                         : test-dedicated-ir
    Description                  : Reserved IR
```

<span data-ttu-id="8f8c6-118">Det här kommandot visar information om integrations körningen med namnet "test-Dedicated-IR" i prenumerationen för resurs gruppen "RG-test-dfv2" och data fabriken med namnet "test-DF-EU2".</span><span class="sxs-lookup"><span data-stu-id="8f8c6-118">This command displays information about the integration runtime named 'test-dedicated-ir' in the subscription for the resource group named 'rg-test-dfv2' and data factory named 'test-df-eu2'.</span></span>

### <span data-ttu-id="8f8c6-119">Exempel 4: hämta den självvärdbaserade integrerings körningen</span><span class="sxs-lookup"><span data-stu-id="8f8c6-119">Example 4: Get self-hosted integration runtime</span></span>
```
PS C:\> Get-AzDataFactoryV2IntegrationRuntime -ResourceGroupName rg-test-dfv2 -DataFactoryName test-df-eu2 -Name test-selfhost-ir

    ResourceGroupName DataFactoryName Name                 Description
    ----------------- --------------- ----                 -----------
    rg-test-dfv2      test-df-eu2     test-selfhost-ir     selfhost IR
```

<span data-ttu-id="8f8c6-120">Det här kommandot visar information om integrations körningen med namnet "test-Dedicated-IR" i prenumerationen för resurs gruppen "RG-test-dfv2" och data fabriken med namnet "test-DF-EU2".</span><span class="sxs-lookup"><span data-stu-id="8f8c6-120">This command displays information about the integration runtime named 'test-dedicated-ir' in the subscription for the resource group named 'rg-test-dfv2' and data factory named 'test-df-eu2'.</span></span>

### <span data-ttu-id="8f8c6-121">Exempel 5: få självvärdbaserade integrerings körning med detaljerad status</span><span class="sxs-lookup"><span data-stu-id="8f8c6-121">Example 5: Get self-hosted integration runtime with detail status</span></span>
```
PS C:\> Get-AzDataFactoryV2IntegrationRuntime -ResourceGroupName rg-test-dfv2 -DataFactoryName test-df-eu2 -Name test-selfhost-ir -Status

    State                     : Online
    Version                   : 4.2.7233.1
    CreateTime                : 9/26/2019 6:00:08 AM
    AutoUpdate                : Off
    ScheduledUpdateDate       :
    UpdateDelayOffset         : 03:00:00
    LocalTimeZoneOffset       : 08:00:00
    InternalChannelEncryption :
    Capabilities              : {[serviceBusConnected, True], [httpsPortEnabled, True], [credentialInSync, True], [connectedToResourceManager, True]...}
    ServiceUrls               : {}
    Nodes                     : {}
    Links                     : {}
    AutoUpdateETA             :
    LatestVersion             : 4.3.7265.1
    PushedVersion             : 4.3.7265.1
    TaskQueueId               : fe2d60b5-86f5-58bf-bdae-7ef698284088
    VersionStatus             : UpdateAvailable
    Name                      : test-selfhost-ir
    Type                      : SelfHosted
    ResourceGroupName         : rg-test-dfv2
    DataFactoryName           : test-df-eu2
    Description               :
    Id                        : /subscriptions/41fcbc45-c594-4152-a8f1-fcbcd6452aea/resourceGroups/rg-test-dfv2/providers/Microsoft.DataFactory/factories/test-df-eu2/integrationruntimes/test-selfhost-ir
```

## <span data-ttu-id="8f8c6-122">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8f8c6-122">PARAMETERS</span></span>

### <span data-ttu-id="8f8c6-123">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="8f8c6-123">-DataFactoryName</span></span>
<span data-ttu-id="8f8c6-124">Namnet på data fabriken.</span><span class="sxs-lookup"><span data-stu-id="8f8c6-124">The data factory name.</span></span>

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

### <span data-ttu-id="8f8c6-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f8c6-125">-DefaultProfile</span></span>
<span data-ttu-id="8f8c6-126">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="8f8c6-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8f8c6-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8f8c6-127">-InputObject</span></span>
<span data-ttu-id="8f8c6-128">Integration runtime-objekt.</span><span class="sxs-lookup"><span data-stu-id="8f8c6-128">The integration runtime object.</span></span>

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

### <span data-ttu-id="8f8c6-129">-Namn</span><span class="sxs-lookup"><span data-stu-id="8f8c6-129">-Name</span></span>
<span data-ttu-id="8f8c6-130">Integrerings körens namn.</span><span class="sxs-lookup"><span data-stu-id="8f8c6-130">The integration runtime name.</span></span>

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

### <span data-ttu-id="8f8c6-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8f8c6-131">-ResourceGroupName</span></span>
<span data-ttu-id="8f8c6-132">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="8f8c6-132">The resource group name.</span></span>

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

### <span data-ttu-id="8f8c6-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8f8c6-133">-ResourceId</span></span>
<span data-ttu-id="8f8c6-134">ID för Azure-resursen.</span><span class="sxs-lookup"><span data-stu-id="8f8c6-134">The Azure resource ID.</span></span>

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

### <span data-ttu-id="8f8c6-135">-Status</span><span class="sxs-lookup"><span data-stu-id="8f8c6-135">-Status</span></span>
<span data-ttu-id="8f8c6-136">Information om integreringens detalj status.</span><span class="sxs-lookup"><span data-stu-id="8f8c6-136">The integration runtime detail status.</span></span>

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

### <span data-ttu-id="8f8c6-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f8c6-137">CommonParameters</span></span>
<span data-ttu-id="8f8c6-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8f8c6-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f8c6-139">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8f8c6-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f8c6-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8f8c6-140">INPUTS</span></span>

### <span data-ttu-id="8f8c6-141">System. String</span><span class="sxs-lookup"><span data-stu-id="8f8c6-141">System.String</span></span>

### <span data-ttu-id="8f8c6-142">Microsoft. Azure. commands. DataFactoryV2. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="8f8c6-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="8f8c6-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8f8c6-143">OUTPUTS</span></span>

### <span data-ttu-id="8f8c6-144">Microsoft. Azure. commands. DataFactoryV2. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="8f8c6-144">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

### <span data-ttu-id="8f8c6-145">Microsoft. Azure. commands. DataFactoryV2. Models. PSManagedIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="8f8c6-145">Microsoft.Azure.Commands.DataFactoryV2.Models.PSManagedIntegrationRuntime</span></span>

### <span data-ttu-id="8f8c6-146">Microsoft. Azure. commands. DataFactoryV2. Models. PSSelfHostedIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="8f8c6-146">Microsoft.Azure.Commands.DataFactoryV2.Models.PSSelfHostedIntegrationRuntime</span></span>

### <span data-ttu-id="8f8c6-147">Microsoft. Azure. commands. DataFactoryV2. Models. PSLinkedIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="8f8c6-147">Microsoft.Azure.Commands.DataFactoryV2.Models.PSLinkedIntegrationRuntime</span></span>

## <span data-ttu-id="8f8c6-148">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8f8c6-148">NOTES</span></span>
<span data-ttu-id="8f8c6-149">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, data, faktorer, kopiera, aktiviteter, integrerings körning</span><span class="sxs-lookup"><span data-stu-id="8f8c6-149">Keywords: azure, azurerm, arm, resource, management, manager, data, factories, copy, activities, integration runtime</span></span>

## <span data-ttu-id="8f8c6-150">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8f8c6-150">RELATED LINKS</span></span>

[<span data-ttu-id="8f8c6-151">Set-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="8f8c6-151">Set-AzDataFactoryV2IntegrationRuntime</span></span>]()

[<span data-ttu-id="8f8c6-152">Remove-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="8f8c6-152">Remove-AzDataFactoryV2IntegrationRuntime</span></span>]()
