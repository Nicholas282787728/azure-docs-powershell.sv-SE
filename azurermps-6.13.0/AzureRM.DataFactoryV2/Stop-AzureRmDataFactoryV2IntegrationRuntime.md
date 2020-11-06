---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/stop-azurermdatafactoryv2integrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Stop-AzureRmDataFactoryV2IntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Stop-AzureRmDataFactoryV2IntegrationRuntime.md
ms.openlocfilehash: ce9ca0f1581bc995f9ea18b3b87169ed979dd92c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93583547"
---
# <span data-ttu-id="48801-101">Stop-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="48801-101">Stop-AzureRmDataFactoryV2IntegrationRuntime</span></span>

## <span data-ttu-id="48801-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="48801-102">SYNOPSIS</span></span>
<span data-ttu-id="48801-103">Stoppar en hanterad dedikerad integrerings körning.</span><span class="sxs-lookup"><span data-stu-id="48801-103">Stops a managed dedicated integration runtime.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="48801-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="48801-104">SYNTAX</span></span>

### <span data-ttu-id="48801-105">ByIntegrationRuntimeName (standard)</span><span class="sxs-lookup"><span data-stu-id="48801-105">ByIntegrationRuntimeName (Default)</span></span>
```
Stop-AzureRmDataFactoryV2IntegrationRuntime [-Force] [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="48801-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="48801-106">ByResourceId</span></span>
```
Stop-AzureRmDataFactoryV2IntegrationRuntime [-Force] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="48801-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="48801-107">ByIntegrationRuntimeObject</span></span>
```
Stop-AzureRmDataFactoryV2IntegrationRuntime [-Force] [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="48801-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="48801-108">DESCRIPTION</span></span>
<span data-ttu-id="48801-109">Cmdleten **Stop-AzureRmDataFactoryV2IntegrationRuntime** stoppar den hanterade dedikerade integrerings miljön i tillståndet ' start ', som startas av Start-AzureRmDataFactoryV2IntegrationRuntime cmdlet.</span><span class="sxs-lookup"><span data-stu-id="48801-109">The **Stop-AzureRmDataFactoryV2IntegrationRuntime** cmdlet stops a managed dedicated integration runtime in 'Started' state, which was started by the Start-AzureRmDataFactoryV2IntegrationRuntime cmdlet.</span></span> <span data-ttu-id="48801-110">Resurserna släpps och delstatlig överföring till "stoppad".</span><span class="sxs-lookup"><span data-stu-id="48801-110">The resources are released and the state transfers to 'Stopped'.</span></span>

## <span data-ttu-id="48801-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="48801-111">EXAMPLES</span></span>

### <span data-ttu-id="48801-112">Exempel 1: stoppa en hanterad integrations körning som är i ' start '-tillstånd.</span><span class="sxs-lookup"><span data-stu-id="48801-112">Example 1: Stop a managed integration runtime that is in 'Started' state.</span></span>
```
PS C:\> Stop-AzureRmDataFactoryV2IntegrationRuntime -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df' -Name 'test-reserlved-ir'
```

<span data-ttu-id="48801-113">Körnings miljön test-reserlved-IR är i starta-läge.</span><span class="sxs-lookup"><span data-stu-id="48801-113">The managed integration runtime 'test-reserlved-ir' is in 'Started' state.</span></span> <span data-ttu-id="48801-114">När du har kört Stop-AzureRmDataFactoryV2IntegrationRuntime cmdleten släpps resurserna och läget överförs till "stoppad".</span><span class="sxs-lookup"><span data-stu-id="48801-114">After running Stop-AzureRmDataFactoryV2IntegrationRuntime cmdlet, the resources are released and the state transfers to 'Stopped'.</span></span>

## <span data-ttu-id="48801-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="48801-115">PARAMETERS</span></span>

### <span data-ttu-id="48801-116">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="48801-116">-DataFactoryName</span></span>
<span data-ttu-id="48801-117">Namnet på data fabriken.</span><span class="sxs-lookup"><span data-stu-id="48801-117">The data factory name.</span></span>

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

### <span data-ttu-id="48801-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48801-118">-DefaultProfile</span></span>
<span data-ttu-id="48801-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="48801-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="48801-120">-Force</span><span class="sxs-lookup"><span data-stu-id="48801-120">-Force</span></span>
<span data-ttu-id="48801-121">Kör cmdleten utan att behöva bekräfta.</span><span class="sxs-lookup"><span data-stu-id="48801-121">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="48801-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="48801-122">-InputObject</span></span>
<span data-ttu-id="48801-123">Integration runtime-objekt.</span><span class="sxs-lookup"><span data-stu-id="48801-123">The integration runtime object.</span></span>

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

### <span data-ttu-id="48801-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="48801-124">-Name</span></span>
<span data-ttu-id="48801-125">Integrerings körens namn.</span><span class="sxs-lookup"><span data-stu-id="48801-125">The integration runtime name.</span></span>

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

### <span data-ttu-id="48801-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="48801-126">-ResourceGroupName</span></span>
<span data-ttu-id="48801-127">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="48801-127">The resource group name.</span></span>

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

### <span data-ttu-id="48801-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="48801-128">-ResourceId</span></span>
<span data-ttu-id="48801-129">ID för Azure-resursen.</span><span class="sxs-lookup"><span data-stu-id="48801-129">The Azure resource ID.</span></span>

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

### <span data-ttu-id="48801-130">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="48801-130">-Confirm</span></span>
<span data-ttu-id="48801-131">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="48801-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="48801-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="48801-132">-WhatIf</span></span>
<span data-ttu-id="48801-133">Visar vad som händer om cmdleten körs men inte kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="48801-133">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="48801-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48801-134">CommonParameters</span></span>
<span data-ttu-id="48801-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="48801-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48801-136">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="48801-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48801-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="48801-137">INPUTS</span></span>

### <span data-ttu-id="48801-138">System. String</span><span class="sxs-lookup"><span data-stu-id="48801-138">System.String</span></span>

### <span data-ttu-id="48801-139">Microsoft. Azure. commands. DataFactoryV2. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="48801-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>
<span data-ttu-id="48801-140">Parametrar: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="48801-140">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="48801-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="48801-141">OUTPUTS</span></span>

### <span data-ttu-id="48801-142">System. Void</span><span class="sxs-lookup"><span data-stu-id="48801-142">System.Void</span></span>

## <span data-ttu-id="48801-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="48801-143">NOTES</span></span>
<span data-ttu-id="48801-144">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, data, faktorer, kopiera, aktiviteter, integrerings körning</span><span class="sxs-lookup"><span data-stu-id="48801-144">Keywords: azure, azurerm, arm, resource, management, manager, data, factories, copy, activities, integration runtime</span></span>

## <span data-ttu-id="48801-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="48801-145">RELATED LINKS</span></span>

[<span data-ttu-id="48801-146">Start-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="48801-146">Start-AzureRmDataFactoryV2IntegrationRuntime</span></span>]()
