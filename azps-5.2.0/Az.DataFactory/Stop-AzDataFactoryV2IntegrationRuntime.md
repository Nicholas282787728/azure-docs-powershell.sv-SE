---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/stop-azdatafactoryv2integrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Stop-AzDataFactoryV2IntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Stop-AzDataFactoryV2IntegrationRuntime.md
ms.openlocfilehash: aa838b24cc2410d9d699bac4dc8d4c00e3153174
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98407816"
---
# <span data-ttu-id="0458d-101">Stop-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="0458d-101">Stop-AzDataFactoryV2IntegrationRuntime</span></span>

## <span data-ttu-id="0458d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0458d-102">SYNOPSIS</span></span>
<span data-ttu-id="0458d-103">Stoppar en hanterad dedikerad integrerings körning.</span><span class="sxs-lookup"><span data-stu-id="0458d-103">Stops a managed dedicated integration runtime.</span></span>

## <span data-ttu-id="0458d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0458d-104">SYNTAX</span></span>

### <span data-ttu-id="0458d-105">ByIntegrationRuntimeName (standard)</span><span class="sxs-lookup"><span data-stu-id="0458d-105">ByIntegrationRuntimeName (Default)</span></span>
```
Stop-AzDataFactoryV2IntegrationRuntime [-Force] [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0458d-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="0458d-106">ByResourceId</span></span>
```
Stop-AzDataFactoryV2IntegrationRuntime [-Force] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0458d-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="0458d-107">ByIntegrationRuntimeObject</span></span>
```
Stop-AzDataFactoryV2IntegrationRuntime [-Force] [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0458d-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0458d-108">DESCRIPTION</span></span>
<span data-ttu-id="0458d-109">Cmdleten **Stop-AzDataFactoryV2IntegrationRuntime** stoppar den hanterade dedikerade integrerings miljön i tillståndet ' start ', som startas av Start-AzDataFactoryV2IntegrationRuntime cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0458d-109">The **Stop-AzDataFactoryV2IntegrationRuntime** cmdlet stops a managed dedicated integration runtime in 'Started' state, which was started by the Start-AzDataFactoryV2IntegrationRuntime cmdlet.</span></span> <span data-ttu-id="0458d-110">Resurserna släpps och delstatlig överföring till "stoppad".</span><span class="sxs-lookup"><span data-stu-id="0458d-110">The resources are released and the state transfers to 'Stopped'.</span></span>

## <span data-ttu-id="0458d-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0458d-111">EXAMPLES</span></span>

### <span data-ttu-id="0458d-112">Exempel 1: stoppa en hanterad integrations körning som är i ' start '-tillstånd.</span><span class="sxs-lookup"><span data-stu-id="0458d-112">Example 1: Stop a managed integration runtime that is in 'Started' state.</span></span>
```
PS C:\> Stop-AzDataFactoryV2IntegrationRuntime -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df' -Name 'test-reserlved-ir'
```

<span data-ttu-id="0458d-113">Körnings miljön test-reserlved-IR är i starta-läge.</span><span class="sxs-lookup"><span data-stu-id="0458d-113">The managed integration runtime 'test-reserlved-ir' is in 'Started' state.</span></span> <span data-ttu-id="0458d-114">När du har kört Stop-AzDataFactoryV2IntegrationRuntime cmdleten släpps resurserna och läget överförs till "stoppad".</span><span class="sxs-lookup"><span data-stu-id="0458d-114">After running Stop-AzDataFactoryV2IntegrationRuntime cmdlet, the resources are released and the state transfers to 'Stopped'.</span></span>

## <span data-ttu-id="0458d-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0458d-115">PARAMETERS</span></span>

### <span data-ttu-id="0458d-116">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="0458d-116">-DataFactoryName</span></span>
<span data-ttu-id="0458d-117">Namnet på data fabriken.</span><span class="sxs-lookup"><span data-stu-id="0458d-117">The data factory name.</span></span>

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

### <span data-ttu-id="0458d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0458d-118">-DefaultProfile</span></span>
<span data-ttu-id="0458d-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="0458d-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0458d-120">-Force</span><span class="sxs-lookup"><span data-stu-id="0458d-120">-Force</span></span>
<span data-ttu-id="0458d-121">Kör cmdleten utan att behöva bekräfta.</span><span class="sxs-lookup"><span data-stu-id="0458d-121">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="0458d-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0458d-122">-InputObject</span></span>
<span data-ttu-id="0458d-123">Integration runtime-objekt.</span><span class="sxs-lookup"><span data-stu-id="0458d-123">The integration runtime object.</span></span>

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

### <span data-ttu-id="0458d-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="0458d-124">-Name</span></span>
<span data-ttu-id="0458d-125">Integrerings körens namn.</span><span class="sxs-lookup"><span data-stu-id="0458d-125">The integration runtime name.</span></span>

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

### <span data-ttu-id="0458d-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0458d-126">-ResourceGroupName</span></span>
<span data-ttu-id="0458d-127">Resurs gruppens namn.</span><span class="sxs-lookup"><span data-stu-id="0458d-127">The resource group name.</span></span>

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

### <span data-ttu-id="0458d-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0458d-128">-ResourceId</span></span>
<span data-ttu-id="0458d-129">ID för Azure-resursen.</span><span class="sxs-lookup"><span data-stu-id="0458d-129">The Azure resource ID.</span></span>

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

### <span data-ttu-id="0458d-130">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="0458d-130">-Confirm</span></span>
<span data-ttu-id="0458d-131">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="0458d-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0458d-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0458d-132">-WhatIf</span></span>
<span data-ttu-id="0458d-133">Visar vad som händer om cmdleten körs men inte kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="0458d-133">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="0458d-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0458d-134">CommonParameters</span></span>
<span data-ttu-id="0458d-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0458d-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0458d-136">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0458d-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0458d-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0458d-137">INPUTS</span></span>

### <span data-ttu-id="0458d-138">System. String</span><span class="sxs-lookup"><span data-stu-id="0458d-138">System.String</span></span>

### <span data-ttu-id="0458d-139">Microsoft. Azure. commands. DataFactoryV2. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="0458d-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="0458d-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0458d-140">OUTPUTS</span></span>

### <span data-ttu-id="0458d-141">System. Void</span><span class="sxs-lookup"><span data-stu-id="0458d-141">System.Void</span></span>

## <span data-ttu-id="0458d-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0458d-142">NOTES</span></span>
<span data-ttu-id="0458d-143">Nyckelord: Azure, azurerm, arm, resurs, hantering, chef, data, faktorer, kopiera, aktiviteter, integrerings körning</span><span class="sxs-lookup"><span data-stu-id="0458d-143">Keywords: azure, azurerm, arm, resource, management, manager, data, factories, copy, activities, integration runtime</span></span>

## <span data-ttu-id="0458d-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0458d-144">RELATED LINKS</span></span>

[<span data-ttu-id="0458d-145">Start-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="0458d-145">Start-AzDataFactoryV2IntegrationRuntime</span></span>]()
