---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/add-aziothubdevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubDevice.md
ms.openlocfilehash: e13cd1ba814bc5bea66a6a3d06506b9822dd38bd
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94271017"
---
# <span data-ttu-id="dd2df-101">Add-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="dd2df-101">Add-AzIotHubDevice</span></span>

## <span data-ttu-id="dd2df-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="dd2df-102">SYNOPSIS</span></span>
<span data-ttu-id="dd2df-103">Skapa en enhet i en IoT-hubb.</span><span class="sxs-lookup"><span data-stu-id="dd2df-103">Create a device in an IoT Hub.</span></span>

## <span data-ttu-id="dd2df-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="dd2df-104">SYNTAX</span></span>

### <span data-ttu-id="dd2df-105">ResourceSet (standard)</span><span class="sxs-lookup"><span data-stu-id="dd2df-105">ResourceSet (Default)</span></span>
```
Add-AzIotHubDevice [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-AuthMethod <PSDeviceAuthType>] [-Status <PSDeviceStatus>] [-StatusReason <String>] [-EdgeEnabled]
 [-Children <String[]>] [-ParentDeviceId <String>] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dd2df-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="dd2df-106">InputObjectSet</span></span>
```
Add-AzIotHubDevice [-InputObject] <PSIotHub> [-DeviceId] <String> [-AuthMethod <PSDeviceAuthType>]
 [-Status <PSDeviceStatus>] [-StatusReason <String>] [-EdgeEnabled] [-Children <String[]>]
 [-ParentDeviceId <String>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="dd2df-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="dd2df-107">ResourceIdSet</span></span>
```
Add-AzIotHubDevice [-ResourceId] <String> [-DeviceId] <String> [-AuthMethod <PSDeviceAuthType>]
 [-Status <PSDeviceStatus>] [-StatusReason <String>] [-EdgeEnabled] [-Children <String[]>]
 [-ParentDeviceId <String>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="dd2df-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="dd2df-108">DESCRIPTION</span></span>
<span data-ttu-id="dd2df-109">Skapa en enhet med olika godkännande typer i en IoT-hubb.</span><span class="sxs-lookup"><span data-stu-id="dd2df-109">Create a device with different authorization type in an IoT Hub.</span></span>

## <span data-ttu-id="dd2df-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="dd2df-110">EXAMPLES</span></span>

### <span data-ttu-id="dd2df-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="dd2df-111">Example 1</span></span>
```powershell
PS C:\> Add-AzIotHubDevice -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -AuthMethod "shared_private_key" -EdgeEnabled
```

<span data-ttu-id="dd2df-112">Skapa en Edge-aktiverad IoT-enhet med standard verifiering (delad privat telefon).</span><span class="sxs-lookup"><span data-stu-id="dd2df-112">Create an edge enabled IoT device with default authorization (shared private key).</span></span>

### <span data-ttu-id="dd2df-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="dd2df-113">Example 2</span></span>
```powershell
PS C:\> Add-AzIotHubDevice -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice2" -AuthMethod "x509_ca" -Status Disabled -StatusReason "Some Reason"
```

<span data-ttu-id="dd2df-114">Skapa en IoT-enhet med certifikat utfärdarens verifiering med inaktiverat status och orsak.</span><span class="sxs-lookup"><span data-stu-id="dd2df-114">Create an IoT device with root CA authorization with disabled status and reason.</span></span>

### <span data-ttu-id="dd2df-115">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="dd2df-115">Example 3</span></span>
```powershell
PS C:\> Add-AzIotHubDevice -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -AuthMethod "shared_private_key" -EdgeEnabled -Children device1,device2
```

<span data-ttu-id="dd2df-116">Skapa en underordnad IoT-enhet och Lägg till underenheter till den.</span><span class="sxs-lookup"><span data-stu-id="dd2df-116">Create an edge enabled IoT device and add child devices to it.</span></span>

### <span data-ttu-id="dd2df-117">Exempel 4</span><span class="sxs-lookup"><span data-stu-id="dd2df-117">Example 4</span></span>
```powershell
PS C:\> Add-AzIotHubDevice -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -AuthMethod "shared_private_key" -ParentDeviceId parentDevice1
```

<span data-ttu-id="dd2df-118">Skapa en IoT-enhet och ange överordnad enhet.</span><span class="sxs-lookup"><span data-stu-id="dd2df-118">Create an IoT device and set its parent device.</span></span>

## <span data-ttu-id="dd2df-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="dd2df-119">PARAMETERS</span></span>

### <span data-ttu-id="dd2df-120">-AuthMethod</span><span class="sxs-lookup"><span data-stu-id="dd2df-120">-AuthMethod</span></span>
<span data-ttu-id="dd2df-121">Den autentiseringstyp som en enhet ska skapas med.</span><span class="sxs-lookup"><span data-stu-id="dd2df-121">The authorization type an entity is to be created with.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceAuthType
Parameter Sets: (All)
Aliases:
Accepted values: shared_private_key, x509_thumbprint, x509_ca

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd2df-122">-Underordnade</span><span class="sxs-lookup"><span data-stu-id="dd2df-122">-Children</span></span>
<span data-ttu-id="dd2df-123">Lägga till underordnad enhets lista (kommaavgränsad) inkluderar bara icke-Edge-enheter.</span><span class="sxs-lookup"><span data-stu-id="dd2df-123">Add child device list (comma separated) includes only non-edge devices.</span></span>

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

### <span data-ttu-id="dd2df-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd2df-124">-DefaultProfile</span></span>
<span data-ttu-id="dd2df-125">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="dd2df-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dd2df-126">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="dd2df-126">-DeviceId</span></span>
<span data-ttu-id="dd2df-127">Målprogram-ID.</span><span class="sxs-lookup"><span data-stu-id="dd2df-127">Target Device Id.</span></span>

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

### <span data-ttu-id="dd2df-128">-EdgeEnabled</span><span class="sxs-lookup"><span data-stu-id="dd2df-128">-EdgeEnabled</span></span>
<span data-ttu-id="dd2df-129">Flagga som anger hur Edge ska aktive ras.</span><span class="sxs-lookup"><span data-stu-id="dd2df-129">Flag indicating edge enablement.</span></span>

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

### <span data-ttu-id="dd2df-130">-Force</span><span class="sxs-lookup"><span data-stu-id="dd2df-130">-Force</span></span>
<span data-ttu-id="dd2df-131">Skriver över den överordnade enheten för den icke-fristående enheten.</span><span class="sxs-lookup"><span data-stu-id="dd2df-131">Overwrites the non-edge device's parent device.</span></span>

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

### <span data-ttu-id="dd2df-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dd2df-132">-InputObject</span></span>
<span data-ttu-id="dd2df-133">IotHub-objekt</span><span class="sxs-lookup"><span data-stu-id="dd2df-133">IotHub object</span></span>

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

### <span data-ttu-id="dd2df-134">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="dd2df-134">-IotHubName</span></span>
<span data-ttu-id="dd2df-135">Namn på IoT Hub</span><span class="sxs-lookup"><span data-stu-id="dd2df-135">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="dd2df-136">-PrimaryThumbprint</span><span class="sxs-lookup"><span data-stu-id="dd2df-136">-PrimaryThumbprint</span></span>
<span data-ttu-id="dd2df-137">Uttryckligt självsignerat certifikat-tumavtryck som ska användas för primär nycklar.</span><span class="sxs-lookup"><span data-stu-id="dd2df-137">Explicit self-signed certificate thumbprint to use for primary key.</span></span>

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

### <span data-ttu-id="dd2df-138">-ParentDeviceId</span><span class="sxs-lookup"><span data-stu-id="dd2df-138">-ParentDeviceId</span></span>
<span data-ttu-id="dd2df-139">ID för Edge-enhet.</span><span class="sxs-lookup"><span data-stu-id="dd2df-139">Id of edge device.</span></span>

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

### <span data-ttu-id="dd2df-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dd2df-140">-ResourceGroupName</span></span>
<span data-ttu-id="dd2df-141">Namn på resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="dd2df-141">Name of the Resource Group</span></span>

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

### <span data-ttu-id="dd2df-142">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="dd2df-142">-ResourceId</span></span>
<span data-ttu-id="dd2df-143">Resurs-ID för IotHub</span><span class="sxs-lookup"><span data-stu-id="dd2df-143">IotHub Resource Id</span></span>

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

### <span data-ttu-id="dd2df-144">-SecondaryThumbprint</span><span class="sxs-lookup"><span data-stu-id="dd2df-144">-SecondaryThumbprint</span></span>
<span data-ttu-id="dd2df-145">Uttryckligt självsignerat certifikat-tumavtryck att använda för sekundär nycklar.</span><span class="sxs-lookup"><span data-stu-id="dd2df-145">Explicit self-signed certificate thumbprint to use for secondary key.</span></span>

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

### <span data-ttu-id="dd2df-146">-Status</span><span class="sxs-lookup"><span data-stu-id="dd2df-146">-Status</span></span>
<span data-ttu-id="dd2df-147">Ange enhetens status när den skapas.</span><span class="sxs-lookup"><span data-stu-id="dd2df-147">Set device status upon creation.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceStatus
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd2df-148">-StatusReason</span><span class="sxs-lookup"><span data-stu-id="dd2df-148">-StatusReason</span></span>
<span data-ttu-id="dd2df-149">Beskrivning av enhetens status.</span><span class="sxs-lookup"><span data-stu-id="dd2df-149">Description for device status.</span></span>

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

### <span data-ttu-id="dd2df-150">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="dd2df-150">-Confirm</span></span>
<span data-ttu-id="dd2df-151">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="dd2df-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dd2df-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dd2df-152">-WhatIf</span></span>
<span data-ttu-id="dd2df-153">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="dd2df-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dd2df-154">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="dd2df-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dd2df-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd2df-155">CommonParameters</span></span>
<span data-ttu-id="dd2df-156">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dd2df-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd2df-157">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dd2df-157">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd2df-158">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="dd2df-158">INPUTS</span></span>

### <span data-ttu-id="dd2df-159">Microsoft. Azure. commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="dd2df-159">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="dd2df-160">System. String</span><span class="sxs-lookup"><span data-stu-id="dd2df-160">System.String</span></span>

## <span data-ttu-id="dd2df-161">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="dd2df-161">OUTPUTS</span></span>

### <span data-ttu-id="dd2df-162">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevice</span><span class="sxs-lookup"><span data-stu-id="dd2df-162">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevice</span></span>

## <span data-ttu-id="dd2df-163">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="dd2df-163">NOTES</span></span>

## <span data-ttu-id="dd2df-164">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="dd2df-164">RELATED LINKS</span></span>
