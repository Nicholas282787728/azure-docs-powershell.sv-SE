---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/start-azurermdatafactoryv2integrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Start-AzureRmDataFactoryV2IntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Start-AzureRmDataFactoryV2IntegrationRuntime.md
ms.openlocfilehash: 77c06c871d35223f296a7f318460b868e8ad0320
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574307"
---
# <span data-ttu-id="3adcd-101">Start-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="3adcd-101">Start-AzureRmDataFactoryV2IntegrationRuntime</span></span>

## <span data-ttu-id="3adcd-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3adcd-102">SYNOPSIS</span></span>
<span data-ttu-id="3adcd-103">Startar en hanterad dedikerad integrerings körning.</span><span class="sxs-lookup"><span data-stu-id="3adcd-103">Starts a managed dedicated integration runtime.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3adcd-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3adcd-104">SYNTAX</span></span>

### <span data-ttu-id="3adcd-105">ByIntegrationRuntimeName (standard)</span><span class="sxs-lookup"><span data-stu-id="3adcd-105">ByIntegrationRuntimeName (Default)</span></span>
```
Start-AzureRmDataFactoryV2IntegrationRuntime [-Force] [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3adcd-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="3adcd-106">ByResourceId</span></span>
```
Start-AzureRmDataFactoryV2IntegrationRuntime [-Force] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3adcd-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="3adcd-107">ByIntegrationRuntimeObject</span></span>
```
Start-AzureRmDataFactoryV2IntegrationRuntime [-Force] [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3adcd-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3adcd-108">DESCRIPTION</span></span>
<span data-ttu-id="3adcd-109">Cmdleten **Start-AzureRmDataFactoryV2IntegrationRuntime** startar en hanterad dedikerad integrerings körning.</span><span class="sxs-lookup"><span data-stu-id="3adcd-109">The **Start-AzureRmDataFactoryV2IntegrationRuntime** cmdlet starts a managed dedicated integration runtime.</span></span> <span data-ttu-id="3adcd-110">Resursen etableras och efter åtgärden är "startat".</span><span class="sxs-lookup"><span data-stu-id="3adcd-110">The resource is provisioned and after the operation the state is 'Started'.</span></span>

## <span data-ttu-id="3adcd-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3adcd-111">EXAMPLES</span></span>

### <span data-ttu-id="3adcd-112">Exempel 1: starta en integrations körning</span><span class="sxs-lookup"><span data-stu-id="3adcd-112">Example 1: Start an integration runtime</span></span>
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

<span data-ttu-id="3adcd-113">Denna cmdlet startar en hanterad dedikerad integrerings körning med namnet "test-Dedicated-IR".</span><span class="sxs-lookup"><span data-stu-id="3adcd-113">This cmdlet starts a managed dedicated integration runtime named 'test-dedicated-ir'.</span></span>

## <span data-ttu-id="3adcd-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3adcd-114">PARAMETERS</span></span>

### <span data-ttu-id="3adcd-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="3adcd-115">-DataFactoryName</span></span>
<span data-ttu-id="3adcd-116">Namnet på data fabriken.</span><span class="sxs-lookup"><span data-stu-id="3adcd-116">The data factory name.</span></span>

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

### <span data-ttu-id="3adcd-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3adcd-117">-DefaultProfile</span></span>
<span data-ttu-id="3adcd-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="3adcd-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3adcd-119">-Force</span><span class="sxs-lookup"><span data-stu-id="3adcd-119">-Force</span></span>
<span data-ttu-id="3adcd-120">Kör cmdleten utan att behöva bekräfta.</span><span class="sxs-lookup"><span data-stu-id="3adcd-120">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="3adcd-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3adcd-121">-InputObject</span></span>
<span data-ttu-id="3adcd-122">Integration runtime-objekt.</span><span class="sxs-lookup"><span data-stu-id="3adcd-122">The integration runtime object.</span></span>

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

### <span data-ttu-id="3adcd-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="3adcd-123">-Name</span></span>
<span data-ttu-id="3adcd-124">Integrerings körens namn.</span><span class="sxs-lookup"><span data-stu-id="3adcd-124">The integration runtime name.</span></span>

```yaml
Type: String
Parameter Sets: ByIntegrationRuntimeName
Aliases: IntegrationRuntimeName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3adcd-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3adcd-125">-ResourceGroupName</span></span>
<span data-ttu-id="3adcd-126">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="3adcd-126">The resource group name.</span></span>

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

### <span data-ttu-id="3adcd-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3adcd-127">-ResourceId</span></span>
<span data-ttu-id="3adcd-128">ID för Azure-resursen.</span><span class="sxs-lookup"><span data-stu-id="3adcd-128">The Azure resource ID.</span></span>

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

### <span data-ttu-id="3adcd-129">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="3adcd-129">-Confirm</span></span>
<span data-ttu-id="3adcd-130">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="3adcd-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3adcd-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3adcd-131">-WhatIf</span></span>
<span data-ttu-id="3adcd-132">Visar vad som händer om cmdleten körs men inte kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="3adcd-132">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="3adcd-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3adcd-133">CommonParameters</span></span>
<span data-ttu-id="3adcd-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3adcd-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3adcd-135">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3adcd-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3adcd-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3adcd-136">INPUTS</span></span>

### <span data-ttu-id="3adcd-137">System. String</span><span class="sxs-lookup"><span data-stu-id="3adcd-137">System.String</span></span>
<span data-ttu-id="3adcd-138">Microsoft. Azure. commands. DataFactoryV2. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="3adcd-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="3adcd-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3adcd-139">OUTPUTS</span></span>

### <span data-ttu-id="3adcd-140">Microsoft. Azure. commands. DataFactoryV2. Models. PSManagedIntegrationRuntimeStatus</span><span class="sxs-lookup"><span data-stu-id="3adcd-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSManagedIntegrationRuntimeStatus</span></span>

## <span data-ttu-id="3adcd-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3adcd-141">NOTES</span></span>

## <span data-ttu-id="3adcd-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3adcd-142">RELATED LINKS</span></span>

[<span data-ttu-id="3adcd-143">Stopp-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="3adcd-143">Stop-AzureRmDataFactoryV2IntegrationRuntime</span></span>]()
