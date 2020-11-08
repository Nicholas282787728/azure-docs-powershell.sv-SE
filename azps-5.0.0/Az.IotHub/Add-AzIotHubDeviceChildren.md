---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/add-aziothubdevicechildren
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubDeviceChildren.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubDeviceChildren.md
ms.openlocfilehash: f6996a97d0e3a9ad654c4ea6aac421c8218c729a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94271011"
---
# <span data-ttu-id="47cd7-101">Add-AzIotHubDeviceChildren</span><span class="sxs-lookup"><span data-stu-id="47cd7-101">Add-AzIotHubDeviceChildren</span></span>

## <span data-ttu-id="47cd7-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="47cd7-102">SYNOPSIS</span></span>
<span data-ttu-id="47cd7-103">Lägga till icke-arbetsenheter som underordnade till Edge-enheten.</span><span class="sxs-lookup"><span data-stu-id="47cd7-103">Add non-edge devices as a children to the edge device.</span></span>

## <span data-ttu-id="47cd7-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="47cd7-104">SYNTAX</span></span>

### <span data-ttu-id="47cd7-105">ResourceSet (standard)</span><span class="sxs-lookup"><span data-stu-id="47cd7-105">ResourceSet (Default)</span></span>
```
Add-AzIotHubDeviceChildren [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-Children] <String[]> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="47cd7-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="47cd7-106">InputObjectSet</span></span>
```
Add-AzIotHubDeviceChildren [-InputObject] <PSIotHub> [-DeviceId] <String> [-Children] <String[]> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="47cd7-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="47cd7-107">ResourceIdSet</span></span>
```
Add-AzIotHubDeviceChildren [-ResourceId] <String> [-DeviceId] <String> [-Children] <String[]> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="47cd7-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="47cd7-108">DESCRIPTION</span></span>
<span data-ttu-id="47cd7-109">Lägg till angiven kommaseparerad lista över icke gräns linje-ID: n som barn till angiven Edge-enhet.</span><span class="sxs-lookup"><span data-stu-id="47cd7-109">Add specified comma-separated list of non edge device ids as children of specified edge device.</span></span>

## <span data-ttu-id="47cd7-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="47cd7-110">EXAMPLES</span></span>

### <span data-ttu-id="47cd7-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="47cd7-111">Example 1</span></span>
```powershell
PS C:\> Add-AzIotHubDeviceChildren -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -Children device1,device2

DeviceId  ChildrenDeviceId
--------  ----------------
myDevice1 {device1, device2}
```

<span data-ttu-id="47cd7-112">Lägga till icke-arbetsenheter som underordnade till Edge-enheten.</span><span class="sxs-lookup"><span data-stu-id="47cd7-112">Add non-edge devices as a children to the edge device.</span></span>

### <span data-ttu-id="47cd7-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="47cd7-113">Example 2</span></span>
```powershell
PS C:\> Add-AzIotHubDeviceChildren -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice2" -Children "device1,device2" -Force

DeviceId  ChildrenDeviceId
--------  ----------------
myDevice2 {device1, device2}
```

<span data-ttu-id="47cd7-114">Lägga till icke-Edge-enheter som barn i Edge-enheten irrespectively den icke gränsen är redan underordnad till en annan enhet.</span><span class="sxs-lookup"><span data-stu-id="47cd7-114">Add non-edge devices as a children to the edge device irrespectively the non-edge device is already a child of other edge device.</span></span>

## <span data-ttu-id="47cd7-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="47cd7-115">PARAMETERS</span></span>

### <span data-ttu-id="47cd7-116">-Underordnade</span><span class="sxs-lookup"><span data-stu-id="47cd7-116">-Children</span></span>
<span data-ttu-id="47cd7-117">Underordnad enhets lista (kommaavgränsad) innehåller endast icke-Edge-enheter.</span><span class="sxs-lookup"><span data-stu-id="47cd7-117">Child device list (comma separated) includes only non-edge devices.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47cd7-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47cd7-118">-DefaultProfile</span></span>
<span data-ttu-id="47cd7-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="47cd7-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="47cd7-120">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="47cd7-120">-DeviceId</span></span>
<span data-ttu-id="47cd7-121">ID för Edge-enhet.</span><span class="sxs-lookup"><span data-stu-id="47cd7-121">Id of edge device.</span></span>

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

### <span data-ttu-id="47cd7-122">-Force</span><span class="sxs-lookup"><span data-stu-id="47cd7-122">-Force</span></span>
<span data-ttu-id="47cd7-123">Skriver över den överordnade enheten för den icke-fristående enheten.</span><span class="sxs-lookup"><span data-stu-id="47cd7-123">Overwrites the non-edge device's parent device.</span></span>

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

### <span data-ttu-id="47cd7-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="47cd7-124">-InputObject</span></span>
<span data-ttu-id="47cd7-125">IotHub-objekt</span><span class="sxs-lookup"><span data-stu-id="47cd7-125">IotHub object</span></span>

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

### <span data-ttu-id="47cd7-126">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="47cd7-126">-IotHubName</span></span>
<span data-ttu-id="47cd7-127">Namn på IoT Hub</span><span class="sxs-lookup"><span data-stu-id="47cd7-127">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="47cd7-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="47cd7-128">-ResourceGroupName</span></span>
<span data-ttu-id="47cd7-129">Namn på resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="47cd7-129">Name of the Resource Group</span></span>

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

### <span data-ttu-id="47cd7-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="47cd7-130">-ResourceId</span></span>
<span data-ttu-id="47cd7-131">Resurs-ID för IotHub</span><span class="sxs-lookup"><span data-stu-id="47cd7-131">IotHub Resource Id</span></span>

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

### <span data-ttu-id="47cd7-132">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="47cd7-132">-Confirm</span></span>
<span data-ttu-id="47cd7-133">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="47cd7-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="47cd7-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="47cd7-134">-WhatIf</span></span>
<span data-ttu-id="47cd7-135">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="47cd7-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="47cd7-136">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="47cd7-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="47cd7-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47cd7-137">CommonParameters</span></span>
<span data-ttu-id="47cd7-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="47cd7-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47cd7-139">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="47cd7-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47cd7-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="47cd7-140">INPUTS</span></span>

### <span data-ttu-id="47cd7-141">Microsoft. Azure. commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="47cd7-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="47cd7-142">System. String</span><span class="sxs-lookup"><span data-stu-id="47cd7-142">System.String</span></span>

## <span data-ttu-id="47cd7-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="47cd7-143">OUTPUTS</span></span>

### <span data-ttu-id="47cd7-144">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceChildren</span><span class="sxs-lookup"><span data-stu-id="47cd7-144">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceChildren</span></span>

## <span data-ttu-id="47cd7-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="47cd7-145">NOTES</span></span>

## <span data-ttu-id="47cd7-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="47cd7-146">RELATED LINKS</span></span>
