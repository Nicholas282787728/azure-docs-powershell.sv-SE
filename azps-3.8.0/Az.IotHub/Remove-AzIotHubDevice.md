---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/remove-aziothubdevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubDevice.md
ms.openlocfilehash: 3d137f93c32b77afd29a833086ff5c55823bc104
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94091525"
---
# <span data-ttu-id="9f67d-101">Remove-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="9f67d-101">Remove-AzIotHubDevice</span></span>

## <span data-ttu-id="9f67d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9f67d-102">SYNOPSIS</span></span>
<span data-ttu-id="9f67d-103">Ta bort en IoT Hub-enhet.</span><span class="sxs-lookup"><span data-stu-id="9f67d-103">Delete an IoT Hub device.</span></span>

## <span data-ttu-id="9f67d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9f67d-104">SYNTAX</span></span>

### <span data-ttu-id="9f67d-105">ResourceSet (standard)</span><span class="sxs-lookup"><span data-stu-id="9f67d-105">ResourceSet (Default)</span></span>
```
Remove-AzIotHubDevice [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9f67d-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="9f67d-106">InputObjectSet</span></span>
```
Remove-AzIotHubDevice [-InputObject] <PSIotHub> [-DeviceId <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9f67d-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="9f67d-107">ResourceIdSet</span></span>
```
Remove-AzIotHubDevice [-ResourceId] <String> [-DeviceId <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9f67d-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9f67d-108">DESCRIPTION</span></span>
<span data-ttu-id="9f67d-109">Ta bort alla enheter eller en viss enhet från ett IoT-hubb.</span><span class="sxs-lookup"><span data-stu-id="9f67d-109">Delete all devices or a specific device from an Iot Hub.</span></span>

## <span data-ttu-id="9f67d-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9f67d-110">EXAMPLES</span></span>

### <span data-ttu-id="9f67d-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="9f67d-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzIotHubDevice -ResourceGroupName "myresourcegroup" -IotHubName "myiothub"
```

<span data-ttu-id="9f67d-112">Ta bort alla IoT Hub-enheter.</span><span class="sxs-lookup"><span data-stu-id="9f67d-112">Delete all Iot Hub devices.</span></span>

### <span data-ttu-id="9f67d-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="9f67d-113">Example 2</span></span>
```powershell
PS C:\> Remove-AzIotHubDevice -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -PassThru

True
```

<span data-ttu-id="9f67d-114">Ta bort en IoT Hub-enhet.</span><span class="sxs-lookup"><span data-stu-id="9f67d-114">Delete an Iot Hub device.</span></span>

## <span data-ttu-id="9f67d-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9f67d-115">PARAMETERS</span></span>

### <span data-ttu-id="9f67d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f67d-116">-DefaultProfile</span></span>
<span data-ttu-id="9f67d-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="9f67d-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9f67d-118">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="9f67d-118">-DeviceId</span></span>
<span data-ttu-id="9f67d-119">Målprogram-ID.</span><span class="sxs-lookup"><span data-stu-id="9f67d-119">Target Device Id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f67d-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9f67d-120">-InputObject</span></span>
<span data-ttu-id="9f67d-121">IotHub-objekt</span><span class="sxs-lookup"><span data-stu-id="9f67d-121">IotHub object</span></span>

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

### <span data-ttu-id="9f67d-122">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="9f67d-122">-IotHubName</span></span>
<span data-ttu-id="9f67d-123">Namn på IoT Hub</span><span class="sxs-lookup"><span data-stu-id="9f67d-123">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="9f67d-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9f67d-124">-PassThru</span></span>
<span data-ttu-id="9f67d-125">Tillåter att det booleska objektet returneras.</span><span class="sxs-lookup"><span data-stu-id="9f67d-125">Allows to return the boolean object.</span></span>
<span data-ttu-id="9f67d-126">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="9f67d-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="9f67d-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9f67d-127">-ResourceGroupName</span></span>
<span data-ttu-id="9f67d-128">Namn på resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="9f67d-128">Name of the Resource Group</span></span>

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

### <span data-ttu-id="9f67d-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9f67d-129">-ResourceId</span></span>
<span data-ttu-id="9f67d-130">Resurs-ID för IotHub</span><span class="sxs-lookup"><span data-stu-id="9f67d-130">IotHub Resource Id</span></span>

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

### <span data-ttu-id="9f67d-131">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="9f67d-131">-Confirm</span></span>
<span data-ttu-id="9f67d-132">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="9f67d-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9f67d-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9f67d-133">-WhatIf</span></span>
<span data-ttu-id="9f67d-134">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="9f67d-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9f67d-135">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="9f67d-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9f67d-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f67d-136">CommonParameters</span></span>
<span data-ttu-id="9f67d-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9f67d-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f67d-138">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9f67d-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f67d-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9f67d-139">INPUTS</span></span>

### <span data-ttu-id="9f67d-140">Microsoft. Azure. commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="9f67d-140">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="9f67d-141">System. String</span><span class="sxs-lookup"><span data-stu-id="9f67d-141">System.String</span></span>

## <span data-ttu-id="9f67d-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9f67d-142">OUTPUTS</span></span>

### <span data-ttu-id="9f67d-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="9f67d-143">System.Boolean</span></span>

## <span data-ttu-id="9f67d-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9f67d-144">NOTES</span></span>

## <span data-ttu-id="9f67d-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9f67d-145">RELATED LINKS</span></span>
