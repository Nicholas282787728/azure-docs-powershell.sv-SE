---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/set-aziothubdevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubDevice.md
ms.openlocfilehash: 0779403a23a36c972a0d5597d40231b5cc026b37
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94089144"
---
# <span data-ttu-id="23cf6-101">Set-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="23cf6-101">Set-AzIotHubDevice</span></span>

## <span data-ttu-id="23cf6-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="23cf6-102">SYNOPSIS</span></span>
<span data-ttu-id="23cf6-103">Uppdatera en IoT Hub-enhet.</span><span class="sxs-lookup"><span data-stu-id="23cf6-103">Update an IoT Hub device.</span></span>

## <span data-ttu-id="23cf6-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="23cf6-104">SYNTAX</span></span>

### <span data-ttu-id="23cf6-105">ResourceSetForStatus (standard)</span><span class="sxs-lookup"><span data-stu-id="23cf6-105">ResourceSetForStatus (Default)</span></span>
```
Set-AzIotHubDevice [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-Status <PSDeviceStatus>] [-StatusReason <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="23cf6-106">InputObjectSetForAuth</span><span class="sxs-lookup"><span data-stu-id="23cf6-106">InputObjectSetForAuth</span></span>
```
Set-AzIotHubDevice [-InputObject] <PSIotHub> [-DeviceId] <String> [-AuthMethod <PSDeviceAuthType>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="23cf6-107">InputObjectSetForStatus</span><span class="sxs-lookup"><span data-stu-id="23cf6-107">InputObjectSetForStatus</span></span>
```
Set-AzIotHubDevice [-InputObject] <PSIotHub> [-DeviceId] <String> [-Status <PSDeviceStatus>]
 [-StatusReason <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="23cf6-108">InputObjectSetForEdgeEnabled</span><span class="sxs-lookup"><span data-stu-id="23cf6-108">InputObjectSetForEdgeEnabled</span></span>
```
Set-AzIotHubDevice [-InputObject] <PSIotHub> [-DeviceId] <String> [-EdgeEnabled <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="23cf6-109">ResourceSetForAuth</span><span class="sxs-lookup"><span data-stu-id="23cf6-109">ResourceSetForAuth</span></span>
```
Set-AzIotHubDevice [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-AuthMethod <PSDeviceAuthType>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="23cf6-110">ResourceSetForEdgeEnabled</span><span class="sxs-lookup"><span data-stu-id="23cf6-110">ResourceSetForEdgeEnabled</span></span>
```
Set-AzIotHubDevice [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-EdgeEnabled <Boolean>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="23cf6-111">ResourceIdSetForAuth</span><span class="sxs-lookup"><span data-stu-id="23cf6-111">ResourceIdSetForAuth</span></span>
```
Set-AzIotHubDevice [-ResourceId] <String> [-DeviceId] <String> [-AuthMethod <PSDeviceAuthType>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="23cf6-112">ResourceIdSetForStatus</span><span class="sxs-lookup"><span data-stu-id="23cf6-112">ResourceIdSetForStatus</span></span>
```
Set-AzIotHubDevice [-ResourceId] <String> [-DeviceId] <String> [-Status <PSDeviceStatus>]
 [-StatusReason <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="23cf6-113">ResourceIdSetForEdgeEnabled</span><span class="sxs-lookup"><span data-stu-id="23cf6-113">ResourceIdSetForEdgeEnabled</span></span>
```
Set-AzIotHubDevice [-ResourceId] <String> [-DeviceId] <String> [-EdgeEnabled <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="23cf6-114">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="23cf6-114">DESCRIPTION</span></span>
<span data-ttu-id="23cf6-115">Uppdatera en IoT Hub-enhet.</span><span class="sxs-lookup"><span data-stu-id="23cf6-115">Update an IoT Hub device.</span></span>

## <span data-ttu-id="23cf6-116">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="23cf6-116">EXAMPLES</span></span>

### <span data-ttu-id="23cf6-117">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="23cf6-117">Example 1</span></span>
```powershell
PS C:\> Set-AzIotHubDevice -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -EdgeEnabled
```

<span data-ttu-id="23cf6-118">Aktivera Edge-funktioner för enheten.</span><span class="sxs-lookup"><span data-stu-id="23cf6-118">Turn on edge capabilities for device.</span></span>

### <span data-ttu-id="23cf6-119">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="23cf6-119">Example 2</span></span>
```powershell
PS C:\> Set-AzIotHubDevice -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -Status Disabled
```

<span data-ttu-id="23cf6-120">Inaktivera enhets status.</span><span class="sxs-lookup"><span data-stu-id="23cf6-120">Disable device status.</span></span>

### <span data-ttu-id="23cf6-121">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="23cf6-121">Example 3</span></span>
```powershell
PS C:\> Set-AzIotHubDevice -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -AuthMethod "x509_ca"
```

<span data-ttu-id="23cf6-122">Uppdatera Authorization-typen för en IoT Hub-enhet.</span><span class="sxs-lookup"><span data-stu-id="23cf6-122">Update authorization type of an Iot Hub device.</span></span>

## <span data-ttu-id="23cf6-123">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="23cf6-123">PARAMETERS</span></span>

### <span data-ttu-id="23cf6-124">-AuthMethod</span><span class="sxs-lookup"><span data-stu-id="23cf6-124">-AuthMethod</span></span>
<span data-ttu-id="23cf6-125">Den autentiseringstyp som en enhet ska skapas med.</span><span class="sxs-lookup"><span data-stu-id="23cf6-125">The authorization type an entity is to be created with.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceAuthType
Parameter Sets: InputObjectSetForAuth, ResourceSetForAuth, ResourceIdSetForAuth
Aliases:
Accepted values: shared_private_key, x509_thumbprint, x509_ca

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23cf6-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23cf6-126">-DefaultProfile</span></span>
<span data-ttu-id="23cf6-127">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="23cf6-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="23cf6-128">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="23cf6-128">-DeviceId</span></span>
<span data-ttu-id="23cf6-129">Målprogram-ID.</span><span class="sxs-lookup"><span data-stu-id="23cf6-129">Target Device Id.</span></span>

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

### <span data-ttu-id="23cf6-130">-EdgeEnabled</span><span class="sxs-lookup"><span data-stu-id="23cf6-130">-EdgeEnabled</span></span>
<span data-ttu-id="23cf6-131">Flagga som anger hur Edge ska aktive ras.</span><span class="sxs-lookup"><span data-stu-id="23cf6-131">Flag indicating edge enablement.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: InputObjectSetForEdgeEnabled, ResourceSetForEdgeEnabled, ResourceIdSetForEdgeEnabled
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23cf6-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="23cf6-132">-InputObject</span></span>
<span data-ttu-id="23cf6-133">IotHub-objekt</span><span class="sxs-lookup"><span data-stu-id="23cf6-133">IotHub object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub
Parameter Sets: InputObjectSetForAuth, InputObjectSetForStatus, InputObjectSetForEdgeEnabled
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="23cf6-134">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="23cf6-134">-IotHubName</span></span>
<span data-ttu-id="23cf6-135">Namn på IoT Hub</span><span class="sxs-lookup"><span data-stu-id="23cf6-135">Name of the Iot Hub</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSetForStatus, ResourceSetForAuth, ResourceSetForEdgeEnabled
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23cf6-136">-PrimaryThumbprint</span><span class="sxs-lookup"><span data-stu-id="23cf6-136">-PrimaryThumbprint</span></span>
<span data-ttu-id="23cf6-137">Uttryckligt självsignerat certifikat-tumavtryck som ska användas för primär nycklar.</span><span class="sxs-lookup"><span data-stu-id="23cf6-137">Explicit self-signed certificate thumbprint to use for primary key.</span></span>

```yaml
Type: System.String
Parameter Sets: InputObjectSetForAuth, ResourceSetForAuth, ResourceIdSetForAuth
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23cf6-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="23cf6-138">-ResourceGroupName</span></span>
<span data-ttu-id="23cf6-139">Namn på resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="23cf6-139">Name of the Resource Group</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSetForStatus, ResourceSetForAuth, ResourceSetForEdgeEnabled
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23cf6-140">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="23cf6-140">-ResourceId</span></span>
<span data-ttu-id="23cf6-141">Resurs-ID för IotHub</span><span class="sxs-lookup"><span data-stu-id="23cf6-141">IotHub Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSetForAuth, ResourceIdSetForStatus, ResourceIdSetForEdgeEnabled
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="23cf6-142">-SecondaryThumbprint</span><span class="sxs-lookup"><span data-stu-id="23cf6-142">-SecondaryThumbprint</span></span>
<span data-ttu-id="23cf6-143">Uttryckligt självsignerat certifikat-tumavtryck att använda för sekundär nycklar.</span><span class="sxs-lookup"><span data-stu-id="23cf6-143">Explicit self-signed certificate thumbprint to use for secondary key.</span></span>

```yaml
Type: System.String
Parameter Sets: InputObjectSetForAuth, ResourceSetForAuth, ResourceIdSetForAuth
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23cf6-144">-Status</span><span class="sxs-lookup"><span data-stu-id="23cf6-144">-Status</span></span>
<span data-ttu-id="23cf6-145">Ange enhetens status när den skapas.</span><span class="sxs-lookup"><span data-stu-id="23cf6-145">Set device status upon creation.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceStatus
Parameter Sets: ResourceSetForStatus, InputObjectSetForStatus, ResourceIdSetForStatus
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23cf6-146">-StatusReason</span><span class="sxs-lookup"><span data-stu-id="23cf6-146">-StatusReason</span></span>
<span data-ttu-id="23cf6-147">Beskrivning av enhetens status.</span><span class="sxs-lookup"><span data-stu-id="23cf6-147">Description for device status.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSetForStatus, InputObjectSetForStatus, ResourceIdSetForStatus
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23cf6-148">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="23cf6-148">-Confirm</span></span>
<span data-ttu-id="23cf6-149">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="23cf6-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="23cf6-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="23cf6-150">-WhatIf</span></span>
<span data-ttu-id="23cf6-151">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="23cf6-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="23cf6-152">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="23cf6-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="23cf6-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23cf6-153">CommonParameters</span></span>
<span data-ttu-id="23cf6-154">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="23cf6-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23cf6-155">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="23cf6-155">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23cf6-156">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="23cf6-156">INPUTS</span></span>

### <span data-ttu-id="23cf6-157">Microsoft. Azure. commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="23cf6-157">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="23cf6-158">System. String</span><span class="sxs-lookup"><span data-stu-id="23cf6-158">System.String</span></span>

## <span data-ttu-id="23cf6-159">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="23cf6-159">OUTPUTS</span></span>

### <span data-ttu-id="23cf6-160">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevice</span><span class="sxs-lookup"><span data-stu-id="23cf6-160">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevice</span></span>

## <span data-ttu-id="23cf6-161">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="23cf6-161">NOTES</span></span>

## <span data-ttu-id="23cf6-162">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="23cf6-162">RELATED LINKS</span></span>
