---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/start-azurermdatafactoryv2integrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Start-AzureRmDataFactoryV2IntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Start-AzureRmDataFactoryV2IntegrationRuntime.md
ms.openlocfilehash: a9254fbac7e0c98413f4367d9b5e62581f6cb64c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93755848"
---
# <span data-ttu-id="c5bf0-101">Start-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="c5bf0-101">Start-AzureRmDataFactoryV2IntegrationRuntime</span></span>

## <span data-ttu-id="c5bf0-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c5bf0-102">SYNOPSIS</span></span>
<span data-ttu-id="c5bf0-103">Startar en hanterad dedikerad integrerings körning.</span><span class="sxs-lookup"><span data-stu-id="c5bf0-103">Starts a managed dedicated integration runtime.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c5bf0-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c5bf0-104">SYNTAX</span></span>

### <span data-ttu-id="c5bf0-105">ByIntegrationRuntimeName (standard)</span><span class="sxs-lookup"><span data-stu-id="c5bf0-105">ByIntegrationRuntimeName (Default)</span></span>
```
Start-AzureRmDataFactoryV2IntegrationRuntime [-Force] [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c5bf0-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="c5bf0-106">ByResourceId</span></span>
```
Start-AzureRmDataFactoryV2IntegrationRuntime [-Force] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c5bf0-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="c5bf0-107">ByIntegrationRuntimeObject</span></span>
```
Start-AzureRmDataFactoryV2IntegrationRuntime [-Force] [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c5bf0-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c5bf0-108">DESCRIPTION</span></span>
<span data-ttu-id="c5bf0-109">Cmdleten **Start-AzureRmDataFactoryV2IntegrationRuntime** startar en hanterad dedikerad integrerings körning.</span><span class="sxs-lookup"><span data-stu-id="c5bf0-109">The **Start-AzureRmDataFactoryV2IntegrationRuntime** cmdlet starts a managed dedicated integration runtime.</span></span> <span data-ttu-id="c5bf0-110">Resursen etableras och efter åtgärden är "startat".</span><span class="sxs-lookup"><span data-stu-id="c5bf0-110">The resource is provisioned and after the operation the state is 'Started'.</span></span>

## <span data-ttu-id="c5bf0-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c5bf0-111">EXAMPLES</span></span>

### <span data-ttu-id="c5bf0-112">Exempel 1: starta en integrations körning</span><span class="sxs-lookup"><span data-stu-id="c5bf0-112">Example 1: Start an integration runtime</span></span>
```
PS C:\> Start-AzureRmDataFactoryV2IntegrationRuntime -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name test-dedicated-ir' -Force

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
    Id                           : /subscriptions/b3ee3a7f-7614-4644-ad07-afa832620b4b/resourceGroups/rg-test-dfv2/providers/Microsoft.DataFactory/factories/test-df-eu2/integrationruntimes/test-dedicated-ir
    ResourceGroupName            : rg-test-dfv2
    DataFactoryName              : test-df-eu2
    Name                         : test-dedicated-ir
    Description                  : Reserved IR
```

<span data-ttu-id="c5bf0-113">Denna cmdlet startar en hanterad dedikerad integrerings körning med namnet "test-Dedicated-IR".</span><span class="sxs-lookup"><span data-stu-id="c5bf0-113">This cmdlet starts a managed dedicated integration runtime named 'test-dedicated-ir'.</span></span>

## <span data-ttu-id="c5bf0-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c5bf0-114">PARAMETERS</span></span>

### <span data-ttu-id="c5bf0-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="c5bf0-115">-DataFactoryName</span></span>
<span data-ttu-id="c5bf0-116">Namnet på data fabriken.</span><span class="sxs-lookup"><span data-stu-id="c5bf0-116">The data factory name.</span></span>

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

### <span data-ttu-id="c5bf0-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5bf0-117">-DefaultProfile</span></span>
<span data-ttu-id="c5bf0-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c5bf0-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c5bf0-119">-Force</span><span class="sxs-lookup"><span data-stu-id="c5bf0-119">-Force</span></span>
<span data-ttu-id="c5bf0-120">Kör cmdleten utan att behöva bekräfta.</span><span class="sxs-lookup"><span data-stu-id="c5bf0-120">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="c5bf0-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c5bf0-121">-InputObject</span></span>
<span data-ttu-id="c5bf0-122">Integration runtime-objekt.</span><span class="sxs-lookup"><span data-stu-id="c5bf0-122">The integration runtime object.</span></span>

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

### <span data-ttu-id="c5bf0-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="c5bf0-123">-Name</span></span>
<span data-ttu-id="c5bf0-124">Integrerings körens namn.</span><span class="sxs-lookup"><span data-stu-id="c5bf0-124">The integration runtime name.</span></span>

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

### <span data-ttu-id="c5bf0-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c5bf0-125">-ResourceGroupName</span></span>
<span data-ttu-id="c5bf0-126">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="c5bf0-126">The resource group name.</span></span>

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

### <span data-ttu-id="c5bf0-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c5bf0-127">-ResourceId</span></span>
<span data-ttu-id="c5bf0-128">ID för Azure-resursen.</span><span class="sxs-lookup"><span data-stu-id="c5bf0-128">The Azure resource ID.</span></span>

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

### <span data-ttu-id="c5bf0-129">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="c5bf0-129">-Confirm</span></span>
<span data-ttu-id="c5bf0-130">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="c5bf0-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c5bf0-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c5bf0-131">-WhatIf</span></span>
<span data-ttu-id="c5bf0-132">Visar vad som händer om cmdleten körs men inte kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="c5bf0-132">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="c5bf0-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5bf0-133">CommonParameters</span></span>
<span data-ttu-id="c5bf0-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c5bf0-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5bf0-135">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c5bf0-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5bf0-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c5bf0-136">INPUTS</span></span>

### <span data-ttu-id="c5bf0-137">System. String</span><span class="sxs-lookup"><span data-stu-id="c5bf0-137">System.String</span></span>

### <span data-ttu-id="c5bf0-138">Microsoft. Azure. commands. DataFactoryV2. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="c5bf0-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>
<span data-ttu-id="c5bf0-139">Parametrar: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="c5bf0-139">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="c5bf0-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c5bf0-140">OUTPUTS</span></span>

### <span data-ttu-id="c5bf0-141">Microsoft. Azure. commands. DataFactoryV2. Models. PSManagedIntegrationRuntimeStatus</span><span class="sxs-lookup"><span data-stu-id="c5bf0-141">Microsoft.Azure.Commands.DataFactoryV2.Models.PSManagedIntegrationRuntimeStatus</span></span>

## <span data-ttu-id="c5bf0-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c5bf0-142">NOTES</span></span>

## <span data-ttu-id="c5bf0-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c5bf0-143">RELATED LINKS</span></span>

[<span data-ttu-id="c5bf0-144">Stopp-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="c5bf0-144">Stop-AzureRmDataFactoryV2IntegrationRuntime</span></span>]()
