---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Remove-AzDeviceSecurityGroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzDeviceSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzDeviceSecurityGroup.md
ms.openlocfilehash: fd15ebdcb52c167441a3278769a22c277aea6982
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94269962"
---
# <span data-ttu-id="d4bc6-101">Remove-AzDeviceSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="d4bc6-101">Remove-AzDeviceSecurityGroup</span></span>

## <span data-ttu-id="d4bc6-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d4bc6-102">SYNOPSIS</span></span>
<span data-ttu-id="d4bc6-103">Ta bort säkerhets grupp för enhet</span><span class="sxs-lookup"><span data-stu-id="d4bc6-103">Delete device security group</span></span>

## <span data-ttu-id="d4bc6-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d4bc6-104">SYNTAX</span></span>

### <span data-ttu-id="d4bc6-105">ResourceIdLevelResource (standard)</span><span class="sxs-lookup"><span data-stu-id="d4bc6-105">ResourceIdLevelResource (Default)</span></span>
```
Remove-AzDeviceSecurityGroup -Name <String> -HubResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d4bc6-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="d4bc6-106">InputObject</span></span>
```
Remove-AzDeviceSecurityGroup -InputObject <PSDeviceSecurityGroup> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d4bc6-107">ID</span><span class="sxs-lookup"><span data-stu-id="d4bc6-107">ResourceId</span></span>
```
Remove-AzDeviceSecurityGroup -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d4bc6-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d4bc6-108">DESCRIPTION</span></span>
<span data-ttu-id="d4bc6-109">Remove-AzDeviceSecurityGroup-cmdleten tar bort en enhets säkerhets grupp som definierats i IoT-säkerhetslösningen.</span><span class="sxs-lookup"><span data-stu-id="d4bc6-109">The Remove-AzDeviceSecurityGroup cmdlet deletes a device security group defined in iot security solution.</span></span>

## <span data-ttu-id="d4bc6-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d4bc6-110">EXAMPLES</span></span>

### <span data-ttu-id="d4bc6-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="d4bc6-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzDeviceSecurityGroup -Name "MySecurityGroup" -HubResourceId "/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Devices/IotHubs/MyHub"
```

<span data-ttu-id="d4bc6-112">Ta bort säkerhets gruppen "MySecurityGroup" för IoT Hub med resurs-ID "/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Devices/IotHubs/MyHub"</span><span class="sxs-lookup"><span data-stu-id="d4bc6-112">Delete the device security group "MySecurityGroup" of iot hub with resource id "/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Devices/IotHubs/MyHub"</span></span>

## <span data-ttu-id="d4bc6-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d4bc6-113">PARAMETERS</span></span>

### <span data-ttu-id="d4bc6-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4bc6-114">-DefaultProfile</span></span>
<span data-ttu-id="d4bc6-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d4bc6-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d4bc6-116">-HubResourceId</span><span class="sxs-lookup"><span data-stu-id="d4bc6-116">-HubResourceId</span></span>
<span data-ttu-id="d4bc6-117">ID för den säkerhets resurs som du vill starta kommandot på.</span><span class="sxs-lookup"><span data-stu-id="d4bc6-117">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="d4bc6-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d4bc6-118">-InputObject</span></span>
<span data-ttu-id="d4bc6-119">Indatavärdet.</span><span class="sxs-lookup"><span data-stu-id="d4bc6-119">Input Object.</span></span>

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

### <span data-ttu-id="d4bc6-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="d4bc6-120">-Name</span></span>
<span data-ttu-id="d4bc6-121">Resurs namn.</span><span class="sxs-lookup"><span data-stu-id="d4bc6-121">Resource name.</span></span>

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

### <span data-ttu-id="d4bc6-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d4bc6-122">-PassThru</span></span>
<span data-ttu-id="d4bc6-123">Returnera om åtgärden lyckades.</span><span class="sxs-lookup"><span data-stu-id="d4bc6-123">Return whether the operation was successful.</span></span>

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

### <span data-ttu-id="d4bc6-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d4bc6-124">-ResourceId</span></span>
<span data-ttu-id="d4bc6-125">ID för den säkerhets resurs som du vill starta kommandot på.</span><span class="sxs-lookup"><span data-stu-id="d4bc6-125">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="d4bc6-126">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="d4bc6-126">-Confirm</span></span>
<span data-ttu-id="d4bc6-127">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="d4bc6-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d4bc6-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d4bc6-128">-WhatIf</span></span>
<span data-ttu-id="d4bc6-129">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="d4bc6-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d4bc6-130">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="d4bc6-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d4bc6-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4bc6-131">CommonParameters</span></span>
<span data-ttu-id="d4bc6-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d4bc6-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4bc6-133">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d4bc6-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4bc6-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d4bc6-134">INPUTS</span></span>

### <span data-ttu-id="d4bc6-135">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDeviceSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="d4bc6-135">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDeviceSecurityGroup</span></span>

### <span data-ttu-id="d4bc6-136">System. String</span><span class="sxs-lookup"><span data-stu-id="d4bc6-136">System.String</span></span>

## <span data-ttu-id="d4bc6-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d4bc6-137">OUTPUTS</span></span>

### <span data-ttu-id="d4bc6-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d4bc6-138">System.Boolean</span></span>

## <span data-ttu-id="d4bc6-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d4bc6-139">NOTES</span></span>

## <span data-ttu-id="d4bc6-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d4bc6-140">RELATED LINKS</span></span>
