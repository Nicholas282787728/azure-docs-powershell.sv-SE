---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/update-aziothubdevicetwin
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Update-AzIotHubDeviceTwin.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Update-AzIotHubDeviceTwin.md
ms.openlocfilehash: 451f809687ea768800f0e9e33ef4c5af9c425150
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98391304"
---
# <span data-ttu-id="7de41-101">Update-AzIotHubDeviceTwin</span><span class="sxs-lookup"><span data-stu-id="7de41-101">Update-AzIotHubDeviceTwin</span></span>

## <span data-ttu-id="7de41-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7de41-102">SYNOPSIS</span></span>
<span data-ttu-id="7de41-103">Uppdaterar Taggar och önskade egenskaper för en enhet.</span><span class="sxs-lookup"><span data-stu-id="7de41-103">Updates tags and desired properties of a device twin.</span></span>

## <span data-ttu-id="7de41-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7de41-104">SYNTAX</span></span>

### <span data-ttu-id="7de41-105">ResourceSet (standard)</span><span class="sxs-lookup"><span data-stu-id="7de41-105">ResourceSet (Default)</span></span>
```
Update-AzIotHubDeviceTwin [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-Tag <Hashtable>] [-Desired <Hashtable>] [-Partial] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7de41-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="7de41-106">InputObjectSet</span></span>
```
Update-AzIotHubDeviceTwin [-InputObject] <PSIotHub> [-DeviceId] <String> [-Tag <Hashtable>]
 [-Desired <Hashtable>] [-Partial] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7de41-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="7de41-107">ResourceIdSet</span></span>
```
Update-AzIotHubDeviceTwin [-ResourceId] <String> [-DeviceId] <String> [-Tag <Hashtable>] [-Desired <Hashtable>]
 [-Partial] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7de41-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7de41-108">DESCRIPTION</span></span>
<span data-ttu-id="7de41-109">Uppdaterar eller ersätter en enhet.</span><span class="sxs-lookup"><span data-stu-id="7de41-109">Updates or replaces a device twin.</span></span> <span data-ttu-id="7de41-110">Mer https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-device-twins information finns i.</span><span class="sxs-lookup"><span data-stu-id="7de41-110">See https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-device-twins for more information.</span></span>

## <span data-ttu-id="7de41-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7de41-111">EXAMPLES</span></span>

### <span data-ttu-id="7de41-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="7de41-112">Example 1</span></span>
```powershell
PS C:\> Update-AzIotHubDeviceTwin -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -Tag $updatedTag -Desired $updatedDesired -Partial
```

<span data-ttu-id="7de41-113">Returnerar den uppdaterade enhetens dubbla objekt.</span><span class="sxs-lookup"><span data-stu-id="7de41-113">Returns the updated device twin object.</span></span>

### <span data-ttu-id="7de41-114">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="7de41-114">Example 2</span></span>
```powershell
PS C:\> Update-AzIotHubDeviceTwin -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -Desired $updatedDesired -Partial
```

<span data-ttu-id="7de41-115">Returnerar enheten med dubbla objekt med uppdaterade egenskaper.</span><span class="sxs-lookup"><span data-stu-id="7de41-115">Returns the device twin object with updated desired properties.</span></span>

### <span data-ttu-id="7de41-116">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="7de41-116">Example 3</span></span>
```powershell
PS C:\> Update-AzIotHubDeviceTwin -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -Tag $updatedTag -Partial
```

<span data-ttu-id="7de41-117">Returnerar egenskapen enhets dubbla objekt med uppdaterade märknings egenskaper.</span><span class="sxs-lookup"><span data-stu-id="7de41-117">Returns the device twin object with updated tags property.</span></span>

### <span data-ttu-id="7de41-118">Exempel 4</span><span class="sxs-lookup"><span data-stu-id="7de41-118">Example 4</span></span>
```powershell
PS C:\> $updatedTag = @{}
PS C:\> $updatedTag.add("key0","value0")
PS C:\> $updatedDesired =@{}
PS C:\> $updatedDesired.add("desiredkey","desiredvalue")
PS C:\> Update-AzIotHubDeviceTwin -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -Tag $updatedTag -Desired $updatedDesired
```

<span data-ttu-id="7de41-119">Returnerar den utbytta enhetens dubbla objekt.</span><span class="sxs-lookup"><span data-stu-id="7de41-119">Returns the replaced device twin object.</span></span>

## <span data-ttu-id="7de41-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7de41-120">PARAMETERS</span></span>

### <span data-ttu-id="7de41-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7de41-121">-DefaultProfile</span></span>
<span data-ttu-id="7de41-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="7de41-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7de41-123">-Önskat</span><span class="sxs-lookup"><span data-stu-id="7de41-123">-Desired</span></span>
<span data-ttu-id="7de41-124">Lägg till eller uppdatera önskad egenskap i en enhet.</span><span class="sxs-lookup"><span data-stu-id="7de41-124">Add or update the desired property in a device twin.</span></span>

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

### <span data-ttu-id="7de41-125">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="7de41-125">-DeviceId</span></span>
<span data-ttu-id="7de41-126">Målprogram-ID.</span><span class="sxs-lookup"><span data-stu-id="7de41-126">Target Device Id.</span></span>

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

### <span data-ttu-id="7de41-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7de41-127">-InputObject</span></span>
<span data-ttu-id="7de41-128">IotHub-objekt</span><span class="sxs-lookup"><span data-stu-id="7de41-128">IotHub object</span></span>

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

### <span data-ttu-id="7de41-129">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="7de41-129">-IotHubName</span></span>
<span data-ttu-id="7de41-130">Namn på IoT Hub</span><span class="sxs-lookup"><span data-stu-id="7de41-130">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="7de41-131">-Delvis</span><span class="sxs-lookup"><span data-stu-id="7de41-131">-Partial</span></span>
<span data-ttu-id="7de41-132">Tillåter endast delvis uppdatering av taggar och önskade egenskaper för en enhet.</span><span class="sxs-lookup"><span data-stu-id="7de41-132">Allows to only partially update the tags and desired properties of a device twin.</span></span>

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

### <span data-ttu-id="7de41-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7de41-133">-ResourceGroupName</span></span>
<span data-ttu-id="7de41-134">Namn på resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="7de41-134">Name of the Resource Group</span></span>

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

### <span data-ttu-id="7de41-135">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7de41-135">-ResourceId</span></span>
<span data-ttu-id="7de41-136">Resurs-ID för IotHub</span><span class="sxs-lookup"><span data-stu-id="7de41-136">IotHub Resource Id</span></span>

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

### <span data-ttu-id="7de41-137">-Tagg</span><span class="sxs-lookup"><span data-stu-id="7de41-137">-Tag</span></span>
<span data-ttu-id="7de41-138">Lägga till eller uppdatera egenskapen Taggar i en enhet</span><span class="sxs-lookup"><span data-stu-id="7de41-138">Add or update the tags property in a device twin.</span></span>

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

### <span data-ttu-id="7de41-139">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="7de41-139">-Confirm</span></span>
<span data-ttu-id="7de41-140">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="7de41-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7de41-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7de41-141">-WhatIf</span></span>
<span data-ttu-id="7de41-142">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="7de41-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7de41-143">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="7de41-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7de41-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7de41-144">CommonParameters</span></span>
<span data-ttu-id="7de41-145">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7de41-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7de41-146">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7de41-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7de41-147">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7de41-147">INPUTS</span></span>

### <span data-ttu-id="7de41-148">Microsoft. Azure. commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="7de41-148">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="7de41-149">System. String</span><span class="sxs-lookup"><span data-stu-id="7de41-149">System.String</span></span>

## <span data-ttu-id="7de41-150">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7de41-150">OUTPUTS</span></span>

### <span data-ttu-id="7de41-151">System. String</span><span class="sxs-lookup"><span data-stu-id="7de41-151">System.String</span></span>

## <span data-ttu-id="7de41-152">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7de41-152">NOTES</span></span>

## <span data-ttu-id="7de41-153">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7de41-153">RELATED LINKS</span></span>
