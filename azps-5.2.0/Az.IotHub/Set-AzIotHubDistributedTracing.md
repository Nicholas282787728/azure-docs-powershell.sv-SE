---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/set-aziothubdistributedtracing
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubDistributedTracing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubDistributedTracing.md
ms.openlocfilehash: 364b54f9e0b7a9112c2ce46f33363a4510c7bb68
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98407744"
---
# <span data-ttu-id="600a1-101">Set-AzIotHubDistributedTracing</span><span class="sxs-lookup"><span data-stu-id="600a1-101">Set-AzIotHubDistributedTracing</span></span>

## <span data-ttu-id="600a1-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="600a1-102">SYNOPSIS</span></span>
<span data-ttu-id="600a1-103">Uppdatera alternativen för distribuerad spårning för en enhet.</span><span class="sxs-lookup"><span data-stu-id="600a1-103">Update the distributed tracing options for a device.</span></span>

## <span data-ttu-id="600a1-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="600a1-104">SYNTAX</span></span>

### <span data-ttu-id="600a1-105">ResourceSet (standard)</span><span class="sxs-lookup"><span data-stu-id="600a1-105">ResourceSet (Default)</span></span>
```
Set-AzIotHubDistributedTracing [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-SamplingMode] <PSDistributedTracingSamplingMode> [-SamplingRate <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="600a1-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="600a1-106">InputObjectSet</span></span>
```
Set-AzIotHubDistributedTracing [-InputObject] <PSIotHub> [-DeviceId] <String>
 [-SamplingMode] <PSDistributedTracingSamplingMode> [-SamplingRate <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="600a1-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="600a1-107">ResourceIdSet</span></span>
```
Set-AzIotHubDistributedTracing [-ResourceId] <String> [-DeviceId] <String>
 [-SamplingMode] <PSDistributedTracingSamplingMode> [-SamplingRate <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="600a1-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="600a1-108">DESCRIPTION</span></span>
<span data-ttu-id="600a1-109">Uppdatera alternativen för distribuerad spårning för en enhet.</span><span class="sxs-lookup"><span data-stu-id="600a1-109">Update the distributed tracing options for a device.</span></span>

## <span data-ttu-id="600a1-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="600a1-110">EXAMPLES</span></span>

### <span data-ttu-id="600a1-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="600a1-111">Example 1</span></span>
```powershell
PS C:\> Set-AzIotHubDistributedTracing -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -SamplingMode Enabled -SamplingRate 22

DeviceId      : mydevice1
Sampling Mode : Enabled
Sampling Rate : 22%
IsSynced      : False
```

<span data-ttu-id="600a1-112">Uppdatera alternativen för distribuerad spårning för en enhet.</span><span class="sxs-lookup"><span data-stu-id="600a1-112">Update the distributed tracing options for a device.</span></span>

## <span data-ttu-id="600a1-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="600a1-113">PARAMETERS</span></span>

### <span data-ttu-id="600a1-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="600a1-114">-DefaultProfile</span></span>
<span data-ttu-id="600a1-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="600a1-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="600a1-116">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="600a1-116">-DeviceId</span></span>
<span data-ttu-id="600a1-117">Målprogram-ID.</span><span class="sxs-lookup"><span data-stu-id="600a1-117">Target Device Id.</span></span>

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

### <span data-ttu-id="600a1-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="600a1-118">-InputObject</span></span>
<span data-ttu-id="600a1-119">IotHub-objekt</span><span class="sxs-lookup"><span data-stu-id="600a1-119">IotHub object</span></span>

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

### <span data-ttu-id="600a1-120">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="600a1-120">-IotHubName</span></span>
<span data-ttu-id="600a1-121">Namn på IoT Hub</span><span class="sxs-lookup"><span data-stu-id="600a1-121">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="600a1-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="600a1-122">-ResourceGroupName</span></span>
<span data-ttu-id="600a1-123">Namn på resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="600a1-123">Name of the Resource Group</span></span>

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

### <span data-ttu-id="600a1-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="600a1-124">-ResourceId</span></span>
<span data-ttu-id="600a1-125">Resurs-ID för IotHub</span><span class="sxs-lookup"><span data-stu-id="600a1-125">IotHub Resource Id</span></span>

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

### <span data-ttu-id="600a1-126">-SamplingMode</span><span class="sxs-lookup"><span data-stu-id="600a1-126">-SamplingMode</span></span>
<span data-ttu-id="600a1-127">Aktiverar och inaktiverar sampling för distribuerad spårning.</span><span class="sxs-lookup"><span data-stu-id="600a1-127">Turns sampling for distributed tracing enable and disable.</span></span>

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

### <span data-ttu-id="600a1-128">-SamplingRate</span><span class="sxs-lookup"><span data-stu-id="600a1-128">-SamplingRate</span></span>
<span data-ttu-id="600a1-129">Kontrollerar hur många meddelanden som samplats för att lägga till spårnings kontext.</span><span class="sxs-lookup"><span data-stu-id="600a1-129">Controls the amount of messages sampled for adding trace context.</span></span>
<span data-ttu-id="600a1-130">Det här värdet är ett procenttal.</span><span class="sxs-lookup"><span data-stu-id="600a1-130">This value is a percentage.</span></span>
<span data-ttu-id="600a1-131">Endast värden från 0 till 100 tillåts.</span><span class="sxs-lookup"><span data-stu-id="600a1-131">Only values from 0 to 100 (inclusive) are permitted.</span></span>

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

### <span data-ttu-id="600a1-132">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="600a1-132">-Confirm</span></span>
<span data-ttu-id="600a1-133">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="600a1-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="600a1-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="600a1-134">-WhatIf</span></span>
<span data-ttu-id="600a1-135">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="600a1-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="600a1-136">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="600a1-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="600a1-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="600a1-137">CommonParameters</span></span>
<span data-ttu-id="600a1-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="600a1-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="600a1-139">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="600a1-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="600a1-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="600a1-140">INPUTS</span></span>

### <span data-ttu-id="600a1-141">Microsoft. Azure. commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="600a1-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="600a1-142">System. String</span><span class="sxs-lookup"><span data-stu-id="600a1-142">System.String</span></span>

## <span data-ttu-id="600a1-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="600a1-143">OUTPUTS</span></span>

### <span data-ttu-id="600a1-144">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceTracing</span><span class="sxs-lookup"><span data-stu-id="600a1-144">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceTracing</span></span>

## <span data-ttu-id="600a1-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="600a1-145">NOTES</span></span>

## <span data-ttu-id="600a1-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="600a1-146">RELATED LINKS</span></span>
