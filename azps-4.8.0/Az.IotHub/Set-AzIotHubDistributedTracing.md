---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/set-aziothubdistributedtracing
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubDistributedTracing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubDistributedTracing.md
ms.openlocfilehash: 364b54f9e0b7a9112c2ce46f33363a4510c7bb68
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94102841"
---
# <span data-ttu-id="59b89-101">Set-AzIotHubDistributedTracing</span><span class="sxs-lookup"><span data-stu-id="59b89-101">Set-AzIotHubDistributedTracing</span></span>

## <span data-ttu-id="59b89-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="59b89-102">SYNOPSIS</span></span>
<span data-ttu-id="59b89-103">Uppdatera alternativen för distribuerad spårning för en enhet.</span><span class="sxs-lookup"><span data-stu-id="59b89-103">Update the distributed tracing options for a device.</span></span>

## <span data-ttu-id="59b89-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="59b89-104">SYNTAX</span></span>

### <span data-ttu-id="59b89-105">ResourceSet (standard)</span><span class="sxs-lookup"><span data-stu-id="59b89-105">ResourceSet (Default)</span></span>
```
Set-AzIotHubDistributedTracing [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-SamplingMode] <PSDistributedTracingSamplingMode> [-SamplingRate <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="59b89-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="59b89-106">InputObjectSet</span></span>
```
Set-AzIotHubDistributedTracing [-InputObject] <PSIotHub> [-DeviceId] <String>
 [-SamplingMode] <PSDistributedTracingSamplingMode> [-SamplingRate <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="59b89-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="59b89-107">ResourceIdSet</span></span>
```
Set-AzIotHubDistributedTracing [-ResourceId] <String> [-DeviceId] <String>
 [-SamplingMode] <PSDistributedTracingSamplingMode> [-SamplingRate <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="59b89-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="59b89-108">DESCRIPTION</span></span>
<span data-ttu-id="59b89-109">Uppdatera alternativen för distribuerad spårning för en enhet.</span><span class="sxs-lookup"><span data-stu-id="59b89-109">Update the distributed tracing options for a device.</span></span>

## <span data-ttu-id="59b89-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="59b89-110">EXAMPLES</span></span>

### <span data-ttu-id="59b89-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="59b89-111">Example 1</span></span>
```powershell
PS C:\> Set-AzIotHubDistributedTracing -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -SamplingMode Enabled -SamplingRate 22

DeviceId      : mydevice1
Sampling Mode : Enabled
Sampling Rate : 22%
IsSynced      : False
```

<span data-ttu-id="59b89-112">Uppdatera alternativen för distribuerad spårning för en enhet.</span><span class="sxs-lookup"><span data-stu-id="59b89-112">Update the distributed tracing options for a device.</span></span>

## <span data-ttu-id="59b89-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="59b89-113">PARAMETERS</span></span>

### <span data-ttu-id="59b89-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59b89-114">-DefaultProfile</span></span>
<span data-ttu-id="59b89-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="59b89-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="59b89-116">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="59b89-116">-DeviceId</span></span>
<span data-ttu-id="59b89-117">Målprogram-ID.</span><span class="sxs-lookup"><span data-stu-id="59b89-117">Target Device Id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59b89-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="59b89-118">-InputObject</span></span>
<span data-ttu-id="59b89-119">IotHub-objekt</span><span class="sxs-lookup"><span data-stu-id="59b89-119">IotHub object</span></span>

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

### <span data-ttu-id="59b89-120">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="59b89-120">-IotHubName</span></span>
<span data-ttu-id="59b89-121">Namn på IoT Hub</span><span class="sxs-lookup"><span data-stu-id="59b89-121">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="59b89-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="59b89-122">-ResourceGroupName</span></span>
<span data-ttu-id="59b89-123">Namn på resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="59b89-123">Name of the Resource Group</span></span>

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

### <span data-ttu-id="59b89-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="59b89-124">-ResourceId</span></span>
<span data-ttu-id="59b89-125">Resurs-ID för IotHub</span><span class="sxs-lookup"><span data-stu-id="59b89-125">IotHub Resource Id</span></span>

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

### <span data-ttu-id="59b89-126">-SamplingMode</span><span class="sxs-lookup"><span data-stu-id="59b89-126">-SamplingMode</span></span>
<span data-ttu-id="59b89-127">Aktiverar och inaktiverar sampling för distribuerad spårning.</span><span class="sxs-lookup"><span data-stu-id="59b89-127">Turns sampling for distributed tracing enable and disable.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSDistributedTracingSamplingMode
Parameter Sets: (All)
Aliases: Mode
Accepted values: Disabled, Enabled

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59b89-128">-SamplingRate</span><span class="sxs-lookup"><span data-stu-id="59b89-128">-SamplingRate</span></span>
<span data-ttu-id="59b89-129">Kontrollerar hur många meddelanden som samplats för att lägga till spårnings kontext.</span><span class="sxs-lookup"><span data-stu-id="59b89-129">Controls the amount of messages sampled for adding trace context.</span></span>
<span data-ttu-id="59b89-130">Det här värdet är ett procenttal.</span><span class="sxs-lookup"><span data-stu-id="59b89-130">This value is a percentage.</span></span>
<span data-ttu-id="59b89-131">Endast värden från 0 till 100 tillåts.</span><span class="sxs-lookup"><span data-stu-id="59b89-131">Only values from 0 to 100 (inclusive) are permitted.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: Rate

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59b89-132">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="59b89-132">-Confirm</span></span>
<span data-ttu-id="59b89-133">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="59b89-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="59b89-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="59b89-134">-WhatIf</span></span>
<span data-ttu-id="59b89-135">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="59b89-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="59b89-136">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="59b89-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="59b89-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59b89-137">CommonParameters</span></span>
<span data-ttu-id="59b89-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="59b89-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59b89-139">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="59b89-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59b89-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="59b89-140">INPUTS</span></span>

### <span data-ttu-id="59b89-141">Microsoft. Azure. commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="59b89-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="59b89-142">System. String</span><span class="sxs-lookup"><span data-stu-id="59b89-142">System.String</span></span>

## <span data-ttu-id="59b89-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="59b89-143">OUTPUTS</span></span>

### <span data-ttu-id="59b89-144">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceTracing</span><span class="sxs-lookup"><span data-stu-id="59b89-144">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceTracing</span></span>

## <span data-ttu-id="59b89-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="59b89-145">NOTES</span></span>

## <span data-ttu-id="59b89-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="59b89-146">RELATED LINKS</span></span>
