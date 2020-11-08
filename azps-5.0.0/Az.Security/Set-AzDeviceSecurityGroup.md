---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Set-AzDeviceSecurityGroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzDeviceSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzDeviceSecurityGroup.md
ms.openlocfilehash: 269d333c9b74ed0e3e959ef609531bcea41b724c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94269957"
---
# <span data-ttu-id="486ad-101">Set-AzDeviceSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="486ad-101">Set-AzDeviceSecurityGroup</span></span>

## <span data-ttu-id="486ad-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="486ad-102">SYNOPSIS</span></span>
<span data-ttu-id="486ad-103">Skapa eller uppdatera säkerhets grupp för enheten</span><span class="sxs-lookup"><span data-stu-id="486ad-103">Create or update device security group</span></span>

## <span data-ttu-id="486ad-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="486ad-104">SYNTAX</span></span>

### <span data-ttu-id="486ad-105">ResourceIdLevelResource (standard)</span><span class="sxs-lookup"><span data-stu-id="486ad-105">ResourceIdLevelResource (Default)</span></span>
```
Set-AzDeviceSecurityGroup -Name <String> -HubResourceId <String>
 [-ThresholdRule <PSThresholdCustomAlertRule[]>] [-TimeWindowRule <PSTimeWindowCustomAlertRule[]>]
 [-AllowlistRule <PSAllowlistCustomAlertRule[]>] [-DenylistRule <PSDenylistCustomAlertRule[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="486ad-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="486ad-106">InputObject</span></span>
```
Set-AzDeviceSecurityGroup [-ThresholdRule <PSThresholdCustomAlertRule[]>]
 [-TimeWindowRule <PSTimeWindowCustomAlertRule[]>] [-AllowlistRule <PSAllowlistCustomAlertRule[]>]
 [-DenylistRule <PSDenylistCustomAlertRule[]>] -InputObject <PSDeviceSecurityGroup>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="486ad-107">ID</span><span class="sxs-lookup"><span data-stu-id="486ad-107">ResourceId</span></span>
```
Set-AzDeviceSecurityGroup [-ThresholdRule <PSThresholdCustomAlertRule[]>]
 [-TimeWindowRule <PSTimeWindowCustomAlertRule[]>] [-AllowlistRule <PSAllowlistCustomAlertRule[]>]
 [-DenylistRule <PSDenylistCustomAlertRule[]>] -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="486ad-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="486ad-108">DESCRIPTION</span></span>
<span data-ttu-id="486ad-109">Med Set-AzDeviceSecurityGroup cmdlet skapas eller uppdateras en enhets säkerhets grupp som definierats i IoT-säkerhetslösningen.</span><span class="sxs-lookup"><span data-stu-id="486ad-109">The Set-AzDeviceSecurityGroup cmdlet creates or updates a device security group defined in iot security solution.</span></span>

## <span data-ttu-id="486ad-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="486ad-110">EXAMPLES</span></span>

### <span data-ttu-id="486ad-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="486ad-111">Example 1</span></span>
```powershell
PS C:\> $TimeWindowSize = New-TimeSpan -Minutes 5
PS C:\> $TimeWindowRule = New-AzDeviceSecurityGroupTimeWindowRuleObject -Type "ActiveConnectionsNotInAllowedRange" -Enabled $true 
-MaxThreshold 30 -MinThreshold 0 -TimeWindowSize $TimeWindowSize
PS C:\> Set-AzDeviceSecurityGroup -Name "MySecurityGroup" 
-HubResourceId "/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Devices/IotHubs/MyHub" 
-TimeWindowRule $TimeWindowRules

Id: "/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Devices/IotHubs/MyHub/providers/Microsoft.Security/deviceSecurityGroups/MySecurityGroup"
Name: "MySecurityGroup"
Type: "Microsoft.Security/deviceSecurityGroups"
ThresholdRules: []
TimeWindowRules: [
            {
              RuleType: "ActiveConnectionsNotInAllowedRange"
              DisplayName: "Number of active connections is not in allowed range"
              Description: "Get an alert when the number of active connections of a device in the time window is not in the allowed range"
              IsEnabled: true
              MinThreshold: 0
              MaxThreshold: 0
              TimeWindowSize: "PT5M"
            }]
AllowlistRules: [
            {
              RuleType": "ConnectionToIpNotAllowed",
              DisplayName: "Outbound connection to an ip that isn't allowed"
              Description: "Get an alert when an outbound connection is created between your device and an ip that isn't allowed"
              IsEnabled: false
              ValueType: "IpCidr"
              AllowlistValues: []
            },
            {
              RuleType: "LocalUserNotAllowed"
              DisplayName: "Login by a local user that isn't allowed"
              Description: "Get an alert when a local user that isn't allowed logins to the device"
              IsEnabled: false
              ValueType: "String"
              AllowlistValues: []
            }]
DenylistRules: []
```

<span data-ttu-id="486ad-112">Uppdatera befintlig säkerhets grupp från IoT Hub "/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Devices/IotHubs/MyHub" med regel typen "ActiveConnectionsNotInAllowedRange"</span><span class="sxs-lookup"><span data-stu-id="486ad-112">Update existing device security group from IoT Hub "/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Devices/IotHubs/MyHub" with rule type "ActiveConnectionsNotInAllowedRange"</span></span>

## <span data-ttu-id="486ad-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="486ad-113">PARAMETERS</span></span>

### <span data-ttu-id="486ad-114">-AllowlistRule</span><span class="sxs-lookup"><span data-stu-id="486ad-114">-AllowlistRule</span></span>
<span data-ttu-id="486ad-115">Tillåt List regler.</span><span class="sxs-lookup"><span data-stu-id="486ad-115">Allow list rules.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSAllowlistCustomAlertRule[]
Parameter Sets: ResourceIdLevelResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSAllowlistCustomAlertRule[]
Parameter Sets: InputObject, ResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="486ad-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="486ad-116">-DefaultProfile</span></span>
<span data-ttu-id="486ad-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="486ad-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="486ad-118">-DenylistRule</span><span class="sxs-lookup"><span data-stu-id="486ad-118">-DenylistRule</span></span>
<span data-ttu-id="486ad-119">Regler för neka-lista.</span><span class="sxs-lookup"><span data-stu-id="486ad-119">Deny list rules.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDenylistCustomAlertRule[]
Parameter Sets: ResourceIdLevelResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDenylistCustomAlertRule[]
Parameter Sets: InputObject, ResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="486ad-120">-HubResourceId</span><span class="sxs-lookup"><span data-stu-id="486ad-120">-HubResourceId</span></span>
<span data-ttu-id="486ad-121">IoT Hub Resource-ID.</span><span class="sxs-lookup"><span data-stu-id="486ad-121">IoT Hub resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="486ad-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="486ad-122">-InputObject</span></span>
<span data-ttu-id="486ad-123">Indatavärdet.</span><span class="sxs-lookup"><span data-stu-id="486ad-123">Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDeviceSecurityGroup
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="486ad-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="486ad-124">-Name</span></span>
<span data-ttu-id="486ad-125">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="486ad-125">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="486ad-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="486ad-126">-ResourceId</span></span>
<span data-ttu-id="486ad-127">ID för den säkerhets resurs som du vill starta kommandot på.</span><span class="sxs-lookup"><span data-stu-id="486ad-127">ID of the security resource that you want to invoke the command on.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="486ad-128">-ThresholdRule</span><span class="sxs-lookup"><span data-stu-id="486ad-128">-ThresholdRule</span></span>
<span data-ttu-id="486ad-129">Gräns regler.</span><span class="sxs-lookup"><span data-stu-id="486ad-129">Threshold rules.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSThresholdCustomAlertRule[]
Parameter Sets: ResourceIdLevelResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSThresholdCustomAlertRule[]
Parameter Sets: InputObject, ResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="486ad-130">-TimeWindowRule</span><span class="sxs-lookup"><span data-stu-id="486ad-130">-TimeWindowRule</span></span>
<span data-ttu-id="486ad-131">Tidsfönster regler.</span><span class="sxs-lookup"><span data-stu-id="486ad-131">Time window rules.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSTimeWindowCustomAlertRule[]
Parameter Sets: ResourceIdLevelResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSTimeWindowCustomAlertRule[]
Parameter Sets: InputObject, ResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="486ad-132">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="486ad-132">-Confirm</span></span>
<span data-ttu-id="486ad-133">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="486ad-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="486ad-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="486ad-134">-WhatIf</span></span>
<span data-ttu-id="486ad-135">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="486ad-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="486ad-136">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="486ad-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="486ad-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="486ad-137">CommonParameters</span></span>
<span data-ttu-id="486ad-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="486ad-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="486ad-139">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="486ad-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="486ad-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="486ad-140">INPUTS</span></span>

### <span data-ttu-id="486ad-141">Microsoft. Azure. commands. Security. Models. DeviceSecurityGroups. PSThresholdCustomAlertRule []</span><span class="sxs-lookup"><span data-stu-id="486ad-141">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSThresholdCustomAlertRule[]</span></span>

### <span data-ttu-id="486ad-142">Microsoft. Azure. commands. Security. Models. DeviceSecurityGroups. PSTimeWindowCustomAlertRule []</span><span class="sxs-lookup"><span data-stu-id="486ad-142">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSTimeWindowCustomAlertRule[]</span></span>

### <span data-ttu-id="486ad-143">Microsoft. Azure. commands. Security. Models. DeviceSecurityGroups. PSAllowlistCustomAlertRule []</span><span class="sxs-lookup"><span data-stu-id="486ad-143">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSAllowlistCustomAlertRule[]</span></span>

### <span data-ttu-id="486ad-144">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDenylistCustomAlertRule []</span><span class="sxs-lookup"><span data-stu-id="486ad-144">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDenylistCustomAlertRule[]</span></span>

### <span data-ttu-id="486ad-145">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDeviceSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="486ad-145">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDeviceSecurityGroup</span></span>

### <span data-ttu-id="486ad-146">System. String</span><span class="sxs-lookup"><span data-stu-id="486ad-146">System.String</span></span>

## <span data-ttu-id="486ad-147">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="486ad-147">OUTPUTS</span></span>

### <span data-ttu-id="486ad-148">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDeviceSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="486ad-148">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDeviceSecurityGroup</span></span>

## <span data-ttu-id="486ad-149">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="486ad-149">NOTES</span></span>

## <span data-ttu-id="486ad-150">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="486ad-150">RELATED LINKS</span></span>
