---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/update-aziothubmoduletwin
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Update-AzIotHubModuleTwin.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Update-AzIotHubModuleTwin.md
ms.openlocfilehash: fb2b984453f87422d7a5b9ec5d5178ca6b6c55d5
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94319931"
---
# <span data-ttu-id="44762-101">Update-AzIotHubModuleTwin</span><span class="sxs-lookup"><span data-stu-id="44762-101">Update-AzIotHubModuleTwin</span></span>

## <span data-ttu-id="44762-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="44762-102">SYNOPSIS</span></span>
<span data-ttu-id="44762-103">Uppdaterar Taggar och önskade egenskaper för en IoT-enhet.</span><span class="sxs-lookup"><span data-stu-id="44762-103">Updates tags and desired properties of an IoT device module twin.</span></span>

## <span data-ttu-id="44762-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="44762-104">SYNTAX</span></span>

### <span data-ttu-id="44762-105">ResourceSet (standard)</span><span class="sxs-lookup"><span data-stu-id="44762-105">ResourceSet (Default)</span></span>
```
Update-AzIotHubModuleTwin [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 -ModuleId <String> [-Tag <Hashtable>] [-Desired <Hashtable>] [-Partial]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="44762-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="44762-106">InputObjectSet</span></span>
```
Update-AzIotHubModuleTwin [-InputObject] <PSIotHub> [-DeviceId] <String> -ModuleId <String> [-Tag <Hashtable>]
 [-Desired <Hashtable>] [-Partial] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="44762-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="44762-107">ResourceIdSet</span></span>
```
Update-AzIotHubModuleTwin [-ResourceId] <String> [-DeviceId] <String> -ModuleId <String> [-Tag <Hashtable>]
 [-Desired <Hashtable>] [-Partial] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="44762-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="44762-108">DESCRIPTION</span></span>
<span data-ttu-id="44762-109">Uppdaterar eller ersätter en enhet.</span><span class="sxs-lookup"><span data-stu-id="44762-109">Updates or replaces a device twin.</span></span> <span data-ttu-id="44762-110">Mer https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-devguide-module-twins information finns i.</span><span class="sxs-lookup"><span data-stu-id="44762-110">See https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-devguide-module-twins for more information.</span></span>

## <span data-ttu-id="44762-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="44762-111">EXAMPLES</span></span>

### <span data-ttu-id="44762-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="44762-112">Example 1</span></span>
```powershell
PS C:\> Update-AzIotHubModuleTwin -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -ModuleId "myModule1" -Tag $updatedTag -Desired $updatedDesired -Partial
```

<span data-ttu-id="44762-113">Returnerar den uppdaterade enhets modulens dubbla objekt.</span><span class="sxs-lookup"><span data-stu-id="44762-113">Returns the updated device module twin object.</span></span>

### <span data-ttu-id="44762-114">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="44762-114">Example 2</span></span>
```powershell
PS C:\> Update-AzIotHubModuleTwin -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -ModuleId "myModule1" -Desired $updatedDesired -Partial
```

<span data-ttu-id="44762-115">Returnerar enhets modulens dubbla objekt med uppdaterade egenskaper.</span><span class="sxs-lookup"><span data-stu-id="44762-115">Returns the device module twin object with updated desired properties.</span></span>

### <span data-ttu-id="44762-116">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="44762-116">Example 3</span></span>
```powershell
PS C:\> Update-AzIotHubModuleTwin -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -ModuleId "myModule1" -Tag $updatedTag -Partial
```

<span data-ttu-id="44762-117">Returnerar den enhets modulens dubbla objekt med uppdaterade märknings egenskaper.</span><span class="sxs-lookup"><span data-stu-id="44762-117">Returns the device module twin object with updated tags property.</span></span>

### <span data-ttu-id="44762-118">Exempel 4</span><span class="sxs-lookup"><span data-stu-id="44762-118">Example 4</span></span>
```powershell
PS C:\> Update-AzIotHubModuleTwin -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -ModuleId "myModule1" -Tag $updatedTag -Desired $updatedDesired
```

<span data-ttu-id="44762-119">Returnerar den ersatta enhets modulens dubbla objekt.</span><span class="sxs-lookup"><span data-stu-id="44762-119">Returns the replaced device module twin object.</span></span>

## <span data-ttu-id="44762-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="44762-120">PARAMETERS</span></span>

### <span data-ttu-id="44762-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44762-121">-DefaultProfile</span></span>
<span data-ttu-id="44762-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="44762-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="44762-123">-Önskat</span><span class="sxs-lookup"><span data-stu-id="44762-123">-Desired</span></span>
<span data-ttu-id="44762-124">Lägga till eller uppdatera önskad egenskap i en modul, dubbel.</span><span class="sxs-lookup"><span data-stu-id="44762-124">Add or update the desired property in a module twin.</span></span>

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

### <span data-ttu-id="44762-125">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="44762-125">-DeviceId</span></span>
<span data-ttu-id="44762-126">Målprogram-ID.</span><span class="sxs-lookup"><span data-stu-id="44762-126">Target Device Id.</span></span>

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

### <span data-ttu-id="44762-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="44762-127">-InputObject</span></span>
<span data-ttu-id="44762-128">IotHub-objekt</span><span class="sxs-lookup"><span data-stu-id="44762-128">IotHub object</span></span>

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

### <span data-ttu-id="44762-129">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="44762-129">-IotHubName</span></span>
<span data-ttu-id="44762-130">Namn på IoT Hub</span><span class="sxs-lookup"><span data-stu-id="44762-130">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="44762-131">-ModuleId</span><span class="sxs-lookup"><span data-stu-id="44762-131">-ModuleId</span></span>
<span data-ttu-id="44762-132">Målprogram-ID.</span><span class="sxs-lookup"><span data-stu-id="44762-132">Target Module Id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44762-133">-Delvis</span><span class="sxs-lookup"><span data-stu-id="44762-133">-Partial</span></span>
<span data-ttu-id="44762-134">Tillåter endast delvis uppdatering av taggar och önskade egenskaper för en modul.</span><span class="sxs-lookup"><span data-stu-id="44762-134">Allows to only partially update the tags and desired properties of a module twin.</span></span>

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

### <span data-ttu-id="44762-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="44762-135">-ResourceGroupName</span></span>
<span data-ttu-id="44762-136">Namn på resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="44762-136">Name of the Resource Group</span></span>

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

### <span data-ttu-id="44762-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="44762-137">-ResourceId</span></span>
<span data-ttu-id="44762-138">Resurs-ID för IotHub</span><span class="sxs-lookup"><span data-stu-id="44762-138">IotHub Resource Id</span></span>

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

### <span data-ttu-id="44762-139">-Tagg</span><span class="sxs-lookup"><span data-stu-id="44762-139">-Tag</span></span>
<span data-ttu-id="44762-140">Lägga till eller uppdatera egenskapen Taggar i en modul med två.</span><span class="sxs-lookup"><span data-stu-id="44762-140">Add or update the tags property in a module twin.</span></span>

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

### <span data-ttu-id="44762-141">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="44762-141">-Confirm</span></span>
<span data-ttu-id="44762-142">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="44762-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="44762-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="44762-143">-WhatIf</span></span>
<span data-ttu-id="44762-144">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="44762-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="44762-145">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="44762-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="44762-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44762-146">CommonParameters</span></span>
<span data-ttu-id="44762-147">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="44762-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44762-148">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="44762-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44762-149">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="44762-149">INPUTS</span></span>

### <span data-ttu-id="44762-150">Microsoft. Azure. commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="44762-150">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="44762-151">System. String</span><span class="sxs-lookup"><span data-stu-id="44762-151">System.String</span></span>

## <span data-ttu-id="44762-152">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="44762-152">OUTPUTS</span></span>

### <span data-ttu-id="44762-153">Microsoft. Azure. commands. Management. IotHub. Models. PSModuleTwin</span><span class="sxs-lookup"><span data-stu-id="44762-153">Microsoft.Azure.Commands.Management.IotHub.Models.PSModuleTwin</span></span>

## <span data-ttu-id="44762-154">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="44762-154">NOTES</span></span>

## <span data-ttu-id="44762-155">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="44762-155">RELATED LINKS</span></span>