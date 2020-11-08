---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/update-aziothubdevicetwin
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Update-AzIotHubDeviceTwin.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Update-AzIotHubDeviceTwin.md
ms.openlocfilehash: 16c3ab31959268aa998d50290180d4d8b3231ccf
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94259615"
---
# <span data-ttu-id="7048d-101">Update-AzIotHubDeviceTwin</span><span class="sxs-lookup"><span data-stu-id="7048d-101">Update-AzIotHubDeviceTwin</span></span>

## <span data-ttu-id="7048d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7048d-102">SYNOPSIS</span></span>
<span data-ttu-id="7048d-103">Uppdaterar Taggar och önskade egenskaper för en enhet.</span><span class="sxs-lookup"><span data-stu-id="7048d-103">Updates tags and desired properties of a device twin.</span></span>

## <span data-ttu-id="7048d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7048d-104">SYNTAX</span></span>

### <span data-ttu-id="7048d-105">ResourceSet (standard)</span><span class="sxs-lookup"><span data-stu-id="7048d-105">ResourceSet (Default)</span></span>
```
Update-AzIotHubDeviceTwin [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-Tag <Hashtable>] [-Desired <Hashtable>] [-Partial] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7048d-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="7048d-106">InputObjectSet</span></span>
```
Update-AzIotHubDeviceTwin [-InputObject] <PSIotHub> [-DeviceId] <String> [-Tag <Hashtable>]
 [-Desired <Hashtable>] [-Partial] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7048d-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="7048d-107">ResourceIdSet</span></span>
```
Update-AzIotHubDeviceTwin [-ResourceId] <String> [-DeviceId] <String> [-Tag <Hashtable>] [-Desired <Hashtable>]
 [-Partial] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7048d-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7048d-108">DESCRIPTION</span></span>
<span data-ttu-id="7048d-109">Uppdaterar eller ersätter en enhet.</span><span class="sxs-lookup"><span data-stu-id="7048d-109">Updates or replaces a device twin.</span></span> <span data-ttu-id="7048d-110">Mer https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-device-twins information finns i.</span><span class="sxs-lookup"><span data-stu-id="7048d-110">See https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-device-twins for more information.</span></span>

## <span data-ttu-id="7048d-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7048d-111">EXAMPLES</span></span>

### <span data-ttu-id="7048d-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="7048d-112">Example 1</span></span>
```powershell
PS C:\> Update-AzIotHubDeviceTwin -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -Tag $updatedTag -Desired $updatedDesired -Partial
```

<span data-ttu-id="7048d-113">Returnerar den uppdaterade enhetens dubbla objekt.</span><span class="sxs-lookup"><span data-stu-id="7048d-113">Returns the updated device twin object.</span></span>

### <span data-ttu-id="7048d-114">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="7048d-114">Example 2</span></span>
```powershell
PS C:\> Update-AzIotHubDeviceTwin -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -Desired $updatedDesired -Partial
```

<span data-ttu-id="7048d-115">Returnerar enheten med dubbla objekt med uppdaterade egenskaper.</span><span class="sxs-lookup"><span data-stu-id="7048d-115">Returns the device twin object with updated desired properties.</span></span>

### <span data-ttu-id="7048d-116">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="7048d-116">Example 3</span></span>
```powershell
PS C:\> Update-AzIotHubDeviceTwin -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -Tag $updatedTag -Partial
```

<span data-ttu-id="7048d-117">Returnerar egenskapen enhets dubbla objekt med uppdaterade märknings egenskaper.</span><span class="sxs-lookup"><span data-stu-id="7048d-117">Returns the device twin object with updated tags property.</span></span>

### <span data-ttu-id="7048d-118">Exempel 4</span><span class="sxs-lookup"><span data-stu-id="7048d-118">Example 4</span></span>
```powershell
PS C:\> Update-AzIotHubDeviceTwin -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -Tag $updatedTag -Desired $updatedDesired
```

<span data-ttu-id="7048d-119">Returnerar den utbytta enhetens dubbla objekt.</span><span class="sxs-lookup"><span data-stu-id="7048d-119">Returns the replaced device twin object.</span></span>

## <span data-ttu-id="7048d-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7048d-120">PARAMETERS</span></span>

### <span data-ttu-id="7048d-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7048d-121">-DefaultProfile</span></span>
<span data-ttu-id="7048d-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="7048d-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7048d-123">-Önskat</span><span class="sxs-lookup"><span data-stu-id="7048d-123">-Desired</span></span>
<span data-ttu-id="7048d-124">Lägg till eller uppdatera önskad egenskap i en enhet.</span><span class="sxs-lookup"><span data-stu-id="7048d-124">Add or update the desired property in a device twin.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7048d-125">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="7048d-125">-DeviceId</span></span>
<span data-ttu-id="7048d-126">Målprogram-ID.</span><span class="sxs-lookup"><span data-stu-id="7048d-126">Target Device Id.</span></span>

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

### <span data-ttu-id="7048d-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7048d-127">-InputObject</span></span>
<span data-ttu-id="7048d-128">IotHub-objekt</span><span class="sxs-lookup"><span data-stu-id="7048d-128">IotHub object</span></span>

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

### <span data-ttu-id="7048d-129">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="7048d-129">-IotHubName</span></span>
<span data-ttu-id="7048d-130">Namn på IoT Hub</span><span class="sxs-lookup"><span data-stu-id="7048d-130">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="7048d-131">-Delvis</span><span class="sxs-lookup"><span data-stu-id="7048d-131">-Partial</span></span>
<span data-ttu-id="7048d-132">Tillåter endast delvis uppdatering av taggar och önskade egenskaper för en enhet.</span><span class="sxs-lookup"><span data-stu-id="7048d-132">Allows to only partially update the tags and desired properties of a device twin.</span></span>

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

### <span data-ttu-id="7048d-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7048d-133">-ResourceGroupName</span></span>
<span data-ttu-id="7048d-134">Namn på resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="7048d-134">Name of the Resource Group</span></span>

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

### <span data-ttu-id="7048d-135">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7048d-135">-ResourceId</span></span>
<span data-ttu-id="7048d-136">Resurs-ID för IotHub</span><span class="sxs-lookup"><span data-stu-id="7048d-136">IotHub Resource Id</span></span>

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

### <span data-ttu-id="7048d-137">-Tagg</span><span class="sxs-lookup"><span data-stu-id="7048d-137">-Tag</span></span>
<span data-ttu-id="7048d-138">Lägga till eller uppdatera egenskapen Taggar i en enhet</span><span class="sxs-lookup"><span data-stu-id="7048d-138">Add or update the tags property in a device twin.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7048d-139">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="7048d-139">-Confirm</span></span>
<span data-ttu-id="7048d-140">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="7048d-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7048d-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7048d-141">-WhatIf</span></span>
<span data-ttu-id="7048d-142">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="7048d-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7048d-143">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="7048d-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7048d-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7048d-144">CommonParameters</span></span>
<span data-ttu-id="7048d-145">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7048d-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7048d-146">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7048d-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7048d-147">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7048d-147">INPUTS</span></span>

### <span data-ttu-id="7048d-148">Microsoft. Azure. commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="7048d-148">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="7048d-149">System. String</span><span class="sxs-lookup"><span data-stu-id="7048d-149">System.String</span></span>

## <span data-ttu-id="7048d-150">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7048d-150">OUTPUTS</span></span>

### <span data-ttu-id="7048d-151">System. String</span><span class="sxs-lookup"><span data-stu-id="7048d-151">System.String</span></span>

## <span data-ttu-id="7048d-152">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7048d-152">NOTES</span></span>

## <span data-ttu-id="7048d-153">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7048d-153">RELATED LINKS</span></span>
