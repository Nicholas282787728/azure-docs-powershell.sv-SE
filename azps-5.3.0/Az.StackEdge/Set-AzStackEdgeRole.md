---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/set-azstackedgerole
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Set-AzStackEdgeRole.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Set-AzStackEdgeRole.md
ms.openlocfilehash: 17e152d9fb94dc8c2d8d27157f278952a0844ecd
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98418939"
---
# <span data-ttu-id="239ee-101">Set-AzStackEdgeRole</span><span class="sxs-lookup"><span data-stu-id="239ee-101">Set-AzStackEdgeRole</span></span>

## <span data-ttu-id="239ee-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="239ee-102">SYNOPSIS</span></span>
<span data-ttu-id="239ee-103">Uppdaterar en roll för en enhet</span><span class="sxs-lookup"><span data-stu-id="239ee-103">Updates a Role for a device</span></span>

## <span data-ttu-id="239ee-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="239ee-104">SYNTAX</span></span>

### <span data-ttu-id="239ee-105">SetByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="239ee-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzStackEdgeRole [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> -ShareName <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="239ee-106">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="239ee-106">SetByResourceIdParameterSet</span></span>
```
Set-AzStackEdgeRole -ResourceId <String> -ShareName <String[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="239ee-107">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="239ee-107">SetByInputObjectParameterSet</span></span>
```
Set-AzStackEdgeRole -ShareName <String[]> [-DefaultProfile <IAzureContextContainer>]
 -InputObject <PSStackEdgeRole> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="239ee-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="239ee-108">DESCRIPTION</span></span>
<span data-ttu-id="239ee-109">Cmdleten **set-AzStackEdgeRole** uppdaterar en IoT-roll för en stack Edge-enhet.</span><span class="sxs-lookup"><span data-stu-id="239ee-109">The **Set-AzStackEdgeRole** cmdlet updates an IoT role for a Stack Edge device.</span></span> <span data-ttu-id="239ee-110">De gamla monterade resurserna ersätts med de nya i parametern ShareName.</span><span class="sxs-lookup"><span data-stu-id="239ee-110">The old mounted shares will be replaced with the newly provided ones in the ShareName parameter.</span></span>

## <span data-ttu-id="239ee-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="239ee-111">EXAMPLES</span></span>

### <span data-ttu-id="239ee-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="239ee-112">Example 1</span></span>
```powershell
PS C:\> Set-AzStackEdgeRole -ResourceGroupName resourceGroupName -DeviceName deviceName -Name roleiot -ShareName sharename1,sharename2,sharename3

Name    IoTHostHub             Platform Status  IotEdgeDeviceId   IotDeviceId  ResourceGroupName
----    ----------             -------- ------  ---------------   -----------  -----------------
roleiot ehub.azure-devices.net Linux    Enabled iotEdgeDeviceUd   iotDevice    resourceGroupName
```

<span data-ttu-id="239ee-113">Dela namn ersätter de gamla monterade resurserna med de nyss tillhandahållna</span><span class="sxs-lookup"><span data-stu-id="239ee-113">Share Names will replace the old mounted shares with the newly provided ones</span></span>

### <span data-ttu-id="239ee-114">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="239ee-114">Example 2</span></span>
```powershell
PS C:\> Set-AzStackEdgeRole -ResourceGroupName resourceGroupName -DeviceName deviceName -Name roleiot -ShareName @()

Name    IoTHostHub             Platform Status  IotEdgeDeviceId   IotDeviceId  ResourceGroupName
----    ----------             -------- ------  ---------------   -----------  -----------------
roleiot ehub.azure-devices.net Linux    Enabled iotEdgeDeviceUd   iotDevice    resourceGroupName
```

<span data-ttu-id="239ee-115">Demontera alla resurser</span><span class="sxs-lookup"><span data-stu-id="239ee-115">To unmount all shares</span></span>

## <span data-ttu-id="239ee-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="239ee-116">PARAMETERS</span></span>

### <span data-ttu-id="239ee-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="239ee-117">-DefaultProfile</span></span>
<span data-ttu-id="239ee-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="239ee-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="239ee-119">-Enhets namn</span><span class="sxs-lookup"><span data-stu-id="239ee-119">-DeviceName</span></span>
<span data-ttu-id="239ee-120">Enhetens namn</span><span class="sxs-lookup"><span data-stu-id="239ee-120">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="239ee-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="239ee-121">-InputObject</span></span>
<span data-ttu-id="239ee-122">Ange motsvarande enhets objekt</span><span class="sxs-lookup"><span data-stu-id="239ee-122">Please provide corresponding device object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeRole
Parameter Sets: SetByInputObjectParameterSet
Aliases: Role

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="239ee-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="239ee-123">-Name</span></span>
<span data-ttu-id="239ee-124">Namnet på rollen</span><span class="sxs-lookup"><span data-stu-id="239ee-124">Name of the Role</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases: RoleName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="239ee-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="239ee-125">-ResourceGroupName</span></span>
<span data-ttu-id="239ee-126">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="239ee-126">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="239ee-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="239ee-127">-ResourceId</span></span>
<span data-ttu-id="239ee-128">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="239ee-128">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="239ee-129">-ShareName</span><span class="sxs-lookup"><span data-stu-id="239ee-129">-ShareName</span></span>
<span data-ttu-id="239ee-130">Dela/ta delar i en roll</span><span class="sxs-lookup"><span data-stu-id="239ee-130">Share(s) in a role</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="239ee-131">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="239ee-131">-Confirm</span></span>
<span data-ttu-id="239ee-132">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="239ee-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="239ee-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="239ee-133">-WhatIf</span></span>
<span data-ttu-id="239ee-134">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="239ee-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="239ee-135">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="239ee-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="239ee-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="239ee-136">CommonParameters</span></span>
<span data-ttu-id="239ee-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="239ee-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="239ee-138">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="239ee-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="239ee-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="239ee-139">INPUTS</span></span>

### <span data-ttu-id="239ee-140">System. String</span><span class="sxs-lookup"><span data-stu-id="239ee-140">System.String</span></span>

### <span data-ttu-id="239ee-141">Microsoft. Azure. PowerShell. cmdletar. StackEdge. Models. PSStackEdgeRole</span><span class="sxs-lookup"><span data-stu-id="239ee-141">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeRole</span></span>

## <span data-ttu-id="239ee-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="239ee-142">OUTPUTS</span></span>

### <span data-ttu-id="239ee-143">Microsoft. Azure. PowerShell. cmdletar. StackEdge. Models. PSStackEdgeRole</span><span class="sxs-lookup"><span data-stu-id="239ee-143">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeRole</span></span>

## <span data-ttu-id="239ee-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="239ee-144">NOTES</span></span>

## <span data-ttu-id="239ee-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="239ee-145">RELATED LINKS</span></span>
