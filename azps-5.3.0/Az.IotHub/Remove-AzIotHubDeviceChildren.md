---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/remove-aziothubdevicechildren
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubDeviceChildren.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubDeviceChildren.md
ms.openlocfilehash: 8d22b5923b59ef5807419fac4486cd64d5d2b86e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98426035"
---
# <span data-ttu-id="e1416-101">Remove-AzIotHubDeviceChildren</span><span class="sxs-lookup"><span data-stu-id="e1416-101">Remove-AzIotHubDeviceChildren</span></span>

## <span data-ttu-id="e1416-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e1416-102">SYNOPSIS</span></span>
<span data-ttu-id="e1416-103">Ta bort icke kantbaserade enheter som barn från angiven Edge-enhet.</span><span class="sxs-lookup"><span data-stu-id="e1416-103">Remove non edge devices as children from specified edge device.</span></span>

## <span data-ttu-id="e1416-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e1416-104">SYNTAX</span></span>

### <span data-ttu-id="e1416-105">ResourceSet (standard)</span><span class="sxs-lookup"><span data-stu-id="e1416-105">ResourceSet (Default)</span></span>
```
Remove-AzIotHubDeviceChildren [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-Children <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e1416-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="e1416-106">InputObjectSet</span></span>
```
Remove-AzIotHubDeviceChildren [-InputObject] <PSIotHub> [-DeviceId] <String> [-Children <String[]>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e1416-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="e1416-107">ResourceIdSet</span></span>
```
Remove-AzIotHubDeviceChildren [-ResourceId] <String> [-DeviceId] <String> [-Children <String[]>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e1416-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e1416-108">DESCRIPTION</span></span>
<span data-ttu-id="e1416-109">Ta bort alla eller nämnda icke-arbetsenheter som barn angivna i Edge-enheten.</span><span class="sxs-lookup"><span data-stu-id="e1416-109">Remove all or mentioned non-edge devices as children specified edge device.</span></span>

## <span data-ttu-id="e1416-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e1416-110">EXAMPLES</span></span>

### <span data-ttu-id="e1416-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="e1416-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzIotHubDeviceChildren -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -Children device1,device2 -Passthru

True
```

<span data-ttu-id="e1416-112">Ta bort angivna enheter som barn till angiven enhet.</span><span class="sxs-lookup"><span data-stu-id="e1416-112">Remove mentioned devices as children of specified device.</span></span>

### <span data-ttu-id="e1416-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="e1416-113">Example 2</span></span>
```powershell
PS C:\> Remove-AzIotHubDeviceChildren -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -Passthru

True
```

<span data-ttu-id="e1416-114">Ta bort alla icke-arbetsenheter som barn angivna i Edge-enheten.</span><span class="sxs-lookup"><span data-stu-id="e1416-114">Remove all non-edge devices as children specified edge device.</span></span>

## <span data-ttu-id="e1416-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e1416-115">PARAMETERS</span></span>

### <span data-ttu-id="e1416-116">-Underordnade</span><span class="sxs-lookup"><span data-stu-id="e1416-116">-Children</span></span>
<span data-ttu-id="e1416-117">Underordnad enhets lista (kommaavgränsad) innehåller endast icke-Edge-enheter.</span><span class="sxs-lookup"><span data-stu-id="e1416-117">Child device list (comma separated) includes only non-edge devices.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1416-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1416-118">-DefaultProfile</span></span>
<span data-ttu-id="e1416-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e1416-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e1416-120">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="e1416-120">-DeviceId</span></span>
<span data-ttu-id="e1416-121">ID för Edge-enhet.</span><span class="sxs-lookup"><span data-stu-id="e1416-121">Id of edge device.</span></span>

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

### <span data-ttu-id="e1416-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e1416-122">-InputObject</span></span>
<span data-ttu-id="e1416-123">IotHub-objekt</span><span class="sxs-lookup"><span data-stu-id="e1416-123">IotHub object</span></span>

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

### <span data-ttu-id="e1416-124">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="e1416-124">-IotHubName</span></span>
<span data-ttu-id="e1416-125">Namn på IoT Hub</span><span class="sxs-lookup"><span data-stu-id="e1416-125">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="e1416-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e1416-126">-PassThru</span></span>
<span data-ttu-id="e1416-127">Tillåter att det booleska objektet returneras.</span><span class="sxs-lookup"><span data-stu-id="e1416-127">Allows to return the boolean object.</span></span>
<span data-ttu-id="e1416-128">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="e1416-128">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="e1416-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e1416-129">-ResourceGroupName</span></span>
<span data-ttu-id="e1416-130">Namn på resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="e1416-130">Name of the Resource Group</span></span>

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

### <span data-ttu-id="e1416-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e1416-131">-ResourceId</span></span>
<span data-ttu-id="e1416-132">Resurs-ID för IotHub</span><span class="sxs-lookup"><span data-stu-id="e1416-132">IotHub Resource Id</span></span>

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

### <span data-ttu-id="e1416-133">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="e1416-133">-Confirm</span></span>
<span data-ttu-id="e1416-134">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="e1416-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e1416-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e1416-135">-WhatIf</span></span>
<span data-ttu-id="e1416-136">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="e1416-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e1416-137">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="e1416-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e1416-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1416-138">CommonParameters</span></span>
<span data-ttu-id="e1416-139">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e1416-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1416-140">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e1416-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1416-141">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e1416-141">INPUTS</span></span>

### <span data-ttu-id="e1416-142">Microsoft. Azure. commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="e1416-142">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="e1416-143">System. String</span><span class="sxs-lookup"><span data-stu-id="e1416-143">System.String</span></span>

## <span data-ttu-id="e1416-144">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e1416-144">OUTPUTS</span></span>

### <span data-ttu-id="e1416-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e1416-145">System.Boolean</span></span>

## <span data-ttu-id="e1416-146">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e1416-146">NOTES</span></span>

## <span data-ttu-id="e1416-147">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e1416-147">RELATED LINKS</span></span>
