---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/invoke-aziothubmanualfailover
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubManualFailover.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubManualFailover.md
ms.openlocfilehash: 9ff15f3400dda4d9aa44b40575b14d99ae484512
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93743989"
---
# <span data-ttu-id="319b1-101">Invoke-AzIotHubManualFailover</span><span class="sxs-lookup"><span data-stu-id="319b1-101">Invoke-AzIotHubManualFailover</span></span>

## <span data-ttu-id="319b1-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="319b1-102">SYNOPSIS</span></span>
<span data-ttu-id="319b1-103">Aktivera redundans för IoT Hub till det geobaserade återställnings området för katastrof återställning.</span><span class="sxs-lookup"><span data-stu-id="319b1-103">Invoke failover process for the IoT Hub to the geo-paired disaster recovery region.</span></span>

## <span data-ttu-id="319b1-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="319b1-104">SYNTAX</span></span>

### <span data-ttu-id="319b1-105">ResourceSet (standard)</span><span class="sxs-lookup"><span data-stu-id="319b1-105">ResourceSet (Default)</span></span>
```
Invoke-AzIotHubManualFailover [-ResourceGroupName] <String> [-Name] <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="319b1-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="319b1-106">InputObjectSet</span></span>
```
Invoke-AzIotHubManualFailover [-InputObject] <PSIotHub> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="319b1-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="319b1-107">ResourceIdSet</span></span>
```
Invoke-AzIotHubManualFailover [-ResourceId] <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="319b1-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="319b1-108">DESCRIPTION</span></span>
<span data-ttu-id="319b1-109">Den initierar din IoT-hubb till den sekundära platsen.</span><span class="sxs-lookup"><span data-stu-id="319b1-109">It will trigger the failover your IoT hub to the secondary location.</span></span> <span data-ttu-id="319b1-110">Med den här åtgärden kan du förlora tid och telemetri för din lösning.</span><span class="sxs-lookup"><span data-stu-id="319b1-110">This action will cause down time and telemetry loss to your solution.</span></span> <span data-ttu-id="319b1-111">Det kan ta flera minuter att slutföra.</span><span class="sxs-lookup"><span data-stu-id="319b1-111">This is a long running operation and could take several minutes to finish.</span></span> <span data-ttu-id="319b1-112">Var försiktig när du använder den.</span><span class="sxs-lookup"><span data-stu-id="319b1-112">Please exercise with caution when using it.</span></span>

## <span data-ttu-id="319b1-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="319b1-113">EXAMPLES</span></span>

### <span data-ttu-id="319b1-114">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="319b1-114">Example 1</span></span>
```powershell
PS C:\> Invoke-AzIotHubManualFailover -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="319b1-115">Initierar redundans för "myiothub" IoT Hub.</span><span class="sxs-lookup"><span data-stu-id="319b1-115">Initiating failover process of "myiothub" IoT Hub.</span></span>

### <span data-ttu-id="319b1-116">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="319b1-116">Example 2</span></span>
```powershell
PS C:\> Invoke-AzIotHubManualFailover -ResourceGroupName "myresourcegroup" -Name "myiothub" -AsJob
```

<span data-ttu-id="319b1-117">Initierar redundansväxlingen av "myiothub" IoT Hub i bakgrunden.</span><span class="sxs-lookup"><span data-stu-id="319b1-117">Initiating failover process of "myiothub" IoT Hub in the background.</span></span>

## <span data-ttu-id="319b1-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="319b1-118">PARAMETERS</span></span>

### <span data-ttu-id="319b1-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="319b1-119">-AsJob</span></span>
<span data-ttu-id="319b1-120">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="319b1-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="319b1-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="319b1-121">-DefaultProfile</span></span>
<span data-ttu-id="319b1-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="319b1-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="319b1-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="319b1-123">-InputObject</span></span>
<span data-ttu-id="319b1-124">IoT Hub-objekt</span><span class="sxs-lookup"><span data-stu-id="319b1-124">Iot Hub Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub
Parameter Sets: InputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="319b1-125">-Namn</span><span class="sxs-lookup"><span data-stu-id="319b1-125">-Name</span></span>
<span data-ttu-id="319b1-126">Namn på IoT Hub</span><span class="sxs-lookup"><span data-stu-id="319b1-126">Name of the Iot Hub</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="319b1-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="319b1-127">-PassThru</span></span>
<span data-ttu-id="319b1-128">Tillåter att det booleska objektet returneras.</span><span class="sxs-lookup"><span data-stu-id="319b1-128">Allows to return the boolean object.</span></span> <span data-ttu-id="319b1-129">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="319b1-129">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="319b1-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="319b1-130">-ResourceGroupName</span></span>
<span data-ttu-id="319b1-131">Namn på resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="319b1-131">Name of the Resource Group</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="319b1-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="319b1-132">-ResourceId</span></span>
<span data-ttu-id="319b1-133">IoT Hub Resource-ID</span><span class="sxs-lookup"><span data-stu-id="319b1-133">Iot Hub Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="319b1-134">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="319b1-134">-Confirm</span></span>
<span data-ttu-id="319b1-135">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="319b1-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="319b1-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="319b1-136">-WhatIf</span></span>
<span data-ttu-id="319b1-137">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="319b1-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="319b1-138">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="319b1-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="319b1-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="319b1-139">CommonParameters</span></span>
<span data-ttu-id="319b1-140">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="319b1-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="319b1-141">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="319b1-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="319b1-142">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="319b1-142">INPUTS</span></span>

### <span data-ttu-id="319b1-143">Microsoft. Azure. commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="319b1-143">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="319b1-144">System. String</span><span class="sxs-lookup"><span data-stu-id="319b1-144">System.String</span></span>

## <span data-ttu-id="319b1-145">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="319b1-145">OUTPUTS</span></span>

### <span data-ttu-id="319b1-146">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="319b1-146">System.Boolean</span></span>

## <span data-ttu-id="319b1-147">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="319b1-147">NOTES</span></span>

## <span data-ttu-id="319b1-148">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="319b1-148">RELATED LINKS</span></span>
