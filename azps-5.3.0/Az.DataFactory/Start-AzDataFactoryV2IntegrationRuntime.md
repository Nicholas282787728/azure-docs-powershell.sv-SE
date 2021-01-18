---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/start-azdatafactoryv2integrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Start-AzDataFactoryV2IntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Start-AzDataFactoryV2IntegrationRuntime.md
ms.openlocfilehash: 1fc86fe0cd8d36e0bfcc1790c4e47f83daef9909
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98524149"
---
# <span data-ttu-id="63f9d-101">Start-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="63f9d-101">Start-AzDataFactoryV2IntegrationRuntime</span></span>

## <span data-ttu-id="63f9d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="63f9d-102">SYNOPSIS</span></span>
<span data-ttu-id="63f9d-103">Startar en hanterad dedikerad integrerings körning.</span><span class="sxs-lookup"><span data-stu-id="63f9d-103">Starts a managed dedicated integration runtime.</span></span>

## <span data-ttu-id="63f9d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="63f9d-104">SYNTAX</span></span>

### <span data-ttu-id="63f9d-105">ByIntegrationRuntimeName (standard)</span><span class="sxs-lookup"><span data-stu-id="63f9d-105">ByIntegrationRuntimeName (Default)</span></span>
```
Start-AzDataFactoryV2IntegrationRuntime [-Force] [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="63f9d-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="63f9d-106">ByResourceId</span></span>
```
Start-AzDataFactoryV2IntegrationRuntime [-Force] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="63f9d-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="63f9d-107">ByIntegrationRuntimeObject</span></span>
```
Start-AzDataFactoryV2IntegrationRuntime [-Force] [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="63f9d-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="63f9d-108">DESCRIPTION</span></span>
<span data-ttu-id="63f9d-109">Cmdleten **Start-AzDataFactoryV2IntegrationRuntime** startar en hanterad dedikerad integrerings körning.</span><span class="sxs-lookup"><span data-stu-id="63f9d-109">The **Start-AzDataFactoryV2IntegrationRuntime** cmdlet starts a managed dedicated integration runtime.</span></span> <span data-ttu-id="63f9d-110">Resursen etableras och efter åtgärden är "startat".</span><span class="sxs-lookup"><span data-stu-id="63f9d-110">The resource is provisioned and after the operation the state is 'Started'.</span></span>

## <span data-ttu-id="63f9d-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="63f9d-111">EXAMPLES</span></span>

### <span data-ttu-id="63f9d-112">Exempel 1: starta en integrations körning</span><span class="sxs-lookup"><span data-stu-id="63f9d-112">Example 1: Start an integration runtime</span></span>
```
PS C:\> Start-AzDataFactoryV2IntegrationRuntime -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name test-dedicated-ir' -Force

    CreateTime                   : 9/11/2017 2:16:12 PM
    Nodes                        : {tvm-1650185656_1-20170911t141751z}
    OtherErrors                  : {}
    LastOperation                : 
    State                        : Started
    Location                     : West US
    NodeSize                     : Standard_D1_v2
    NodeCount                    : 1
    MaxParallelExecutionsPerNode : 1
    CatalogServerEndpoint        : testsvr.database.windows.net
    CatalogAdminUserName         : admin
    CatalogAdminPassword         : **********
    CatalogPricingTier           : S1
    VNetId                       : 
    Subnet                       : 
    PublicIPs                    : 
    Id                           : /subscriptions/b3ee3a7f-7614-4644-ad07-afa832620b4b/resourceGroups/rg-test-dfv2/providers/Microsoft.DataFactory/factories/test-df-eu2/integrationruntimes/test-dedicated-ir
    ResourceGroupName            : rg-test-dfv2
    DataFactoryName              : test-df-eu2
    Name                         : test-dedicated-ir
    Description                  : Reserved IR
```

<span data-ttu-id="63f9d-113">Denna cmdlet startar en hanterad dedikerad integrerings körning med namnet "test-Dedicated-IR".</span><span class="sxs-lookup"><span data-stu-id="63f9d-113">This cmdlet starts a managed dedicated integration runtime named 'test-dedicated-ir'.</span></span>

## <span data-ttu-id="63f9d-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="63f9d-114">PARAMETERS</span></span>

### <span data-ttu-id="63f9d-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="63f9d-115">-DataFactoryName</span></span>
<span data-ttu-id="63f9d-116">Namnet på data fabriken.</span><span class="sxs-lookup"><span data-stu-id="63f9d-116">The data factory name.</span></span>

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

### <span data-ttu-id="63f9d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63f9d-117">-DefaultProfile</span></span>
<span data-ttu-id="63f9d-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="63f9d-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="63f9d-119">-Force</span><span class="sxs-lookup"><span data-stu-id="63f9d-119">-Force</span></span>
<span data-ttu-id="63f9d-120">Kör cmdleten utan att behöva bekräfta.</span><span class="sxs-lookup"><span data-stu-id="63f9d-120">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="63f9d-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="63f9d-121">-InputObject</span></span>
<span data-ttu-id="63f9d-122">Integration runtime-objekt.</span><span class="sxs-lookup"><span data-stu-id="63f9d-122">The integration runtime object.</span></span>

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

### <span data-ttu-id="63f9d-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="63f9d-123">-Name</span></span>
<span data-ttu-id="63f9d-124">Integrerings körens namn.</span><span class="sxs-lookup"><span data-stu-id="63f9d-124">The integration runtime name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName
Aliases: IntegrationRuntimeName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="63f9d-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="63f9d-125">-ResourceGroupName</span></span>
<span data-ttu-id="63f9d-126">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="63f9d-126">The resource group name.</span></span>

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

### <span data-ttu-id="63f9d-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="63f9d-127">-ResourceId</span></span>
<span data-ttu-id="63f9d-128">ID för Azure-resursen.</span><span class="sxs-lookup"><span data-stu-id="63f9d-128">The Azure resource ID.</span></span>

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

### <span data-ttu-id="63f9d-129">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="63f9d-129">-Confirm</span></span>
<span data-ttu-id="63f9d-130">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="63f9d-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="63f9d-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="63f9d-131">-WhatIf</span></span>
<span data-ttu-id="63f9d-132">Visar vad som händer om cmdleten körs men inte kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="63f9d-132">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="63f9d-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63f9d-133">CommonParameters</span></span>
<span data-ttu-id="63f9d-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="63f9d-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63f9d-135">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="63f9d-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63f9d-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="63f9d-136">INPUTS</span></span>

### <span data-ttu-id="63f9d-137">System. String</span><span class="sxs-lookup"><span data-stu-id="63f9d-137">System.String</span></span>

### <span data-ttu-id="63f9d-138">Microsoft. Azure. commands. DataFactoryV2. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="63f9d-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="63f9d-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="63f9d-139">OUTPUTS</span></span>

### <span data-ttu-id="63f9d-140">Microsoft. Azure. commands. DataFactoryV2. Models. PSManagedIntegrationRuntimeStatus</span><span class="sxs-lookup"><span data-stu-id="63f9d-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSManagedIntegrationRuntimeStatus</span></span>

## <span data-ttu-id="63f9d-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="63f9d-141">NOTES</span></span>

## <span data-ttu-id="63f9d-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="63f9d-142">RELATED LINKS</span></span>

[<span data-ttu-id="63f9d-143">Stopp-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="63f9d-143">Stop-AzDataFactoryV2IntegrationRuntime</span></span>]()
