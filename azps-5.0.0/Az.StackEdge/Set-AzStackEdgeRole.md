---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/set-azstackedgerole
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Set-AzStackEdgeRole.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Set-AzStackEdgeRole.md
ms.openlocfilehash: 17e152d9fb94dc8c2d8d27157f278952a0844ecd
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94270435"
---
# <span data-ttu-id="b1881-101">Set-AzStackEdgeRole</span><span class="sxs-lookup"><span data-stu-id="b1881-101">Set-AzStackEdgeRole</span></span>

## <span data-ttu-id="b1881-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b1881-102">SYNOPSIS</span></span>
<span data-ttu-id="b1881-103">Uppdaterar en roll för en enhet</span><span class="sxs-lookup"><span data-stu-id="b1881-103">Updates a Role for a device</span></span>

## <span data-ttu-id="b1881-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b1881-104">SYNTAX</span></span>

### <span data-ttu-id="b1881-105">SetByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="b1881-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzStackEdgeRole [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> -ShareName <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b1881-106">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b1881-106">SetByResourceIdParameterSet</span></span>
```
Set-AzStackEdgeRole -ResourceId <String> -ShareName <String[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b1881-107">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b1881-107">SetByInputObjectParameterSet</span></span>
```
Set-AzStackEdgeRole -ShareName <String[]> [-DefaultProfile <IAzureContextContainer>]
 -InputObject <PSStackEdgeRole> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b1881-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b1881-108">DESCRIPTION</span></span>
<span data-ttu-id="b1881-109">Cmdleten **set-AzStackEdgeRole** uppdaterar en IoT-roll för en stack Edge-enhet.</span><span class="sxs-lookup"><span data-stu-id="b1881-109">The **Set-AzStackEdgeRole** cmdlet updates an IoT role for a Stack Edge device.</span></span> <span data-ttu-id="b1881-110">De gamla monterade resurserna ersätts med de nya i parametern ShareName.</span><span class="sxs-lookup"><span data-stu-id="b1881-110">The old mounted shares will be replaced with the newly provided ones in the ShareName parameter.</span></span>

## <span data-ttu-id="b1881-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b1881-111">EXAMPLES</span></span>

### <span data-ttu-id="b1881-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="b1881-112">Example 1</span></span>
```powershell
PS C:\> Set-AzStackEdgeRole -ResourceGroupName resourceGroupName -DeviceName deviceName -Name roleiot -ShareName sharename1,sharename2,sharename3

Name    IoTHostHub             Platform Status  IotEdgeDeviceId   IotDeviceId  ResourceGroupName
----    ----------             -------- ------  ---------------   -----------  -----------------
roleiot ehub.azure-devices.net Linux    Enabled iotEdgeDeviceUd   iotDevice    resourceGroupName
```

<span data-ttu-id="b1881-113">Dela namn ersätter de gamla monterade resurserna med de nyss tillhandahållna</span><span class="sxs-lookup"><span data-stu-id="b1881-113">Share Names will replace the old mounted shares with the newly provided ones</span></span>

### <span data-ttu-id="b1881-114">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="b1881-114">Example 2</span></span>
```powershell
PS C:\> Set-AzStackEdgeRole -ResourceGroupName resourceGroupName -DeviceName deviceName -Name roleiot -ShareName @()

Name    IoTHostHub             Platform Status  IotEdgeDeviceId   IotDeviceId  ResourceGroupName
----    ----------             -------- ------  ---------------   -----------  -----------------
roleiot ehub.azure-devices.net Linux    Enabled iotEdgeDeviceUd   iotDevice    resourceGroupName
```

<span data-ttu-id="b1881-115">Demontera alla resurser</span><span class="sxs-lookup"><span data-stu-id="b1881-115">To unmount all shares</span></span>

## <span data-ttu-id="b1881-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b1881-116">PARAMETERS</span></span>

### <span data-ttu-id="b1881-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1881-117">-DefaultProfile</span></span>
<span data-ttu-id="b1881-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b1881-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b1881-119">-Enhets namn</span><span class="sxs-lookup"><span data-stu-id="b1881-119">-DeviceName</span></span>
<span data-ttu-id="b1881-120">Enhetens namn</span><span class="sxs-lookup"><span data-stu-id="b1881-120">Device Name</span></span>

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

### <span data-ttu-id="b1881-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b1881-121">-InputObject</span></span>
<span data-ttu-id="b1881-122">Ange motsvarande enhets objekt</span><span class="sxs-lookup"><span data-stu-id="b1881-122">Please provide corresponding device object</span></span>

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

### <span data-ttu-id="b1881-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="b1881-123">-Name</span></span>
<span data-ttu-id="b1881-124">Namnet på rollen</span><span class="sxs-lookup"><span data-stu-id="b1881-124">Name of the Role</span></span>

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

### <span data-ttu-id="b1881-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b1881-125">-ResourceGroupName</span></span>
<span data-ttu-id="b1881-126">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="b1881-126">Resource Group Name</span></span>

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

### <span data-ttu-id="b1881-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b1881-127">-ResourceId</span></span>
<span data-ttu-id="b1881-128">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="b1881-128">Azure ResourceId</span></span>

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

### <span data-ttu-id="b1881-129">-ShareName</span><span class="sxs-lookup"><span data-stu-id="b1881-129">-ShareName</span></span>
<span data-ttu-id="b1881-130">Dela/ta delar i en roll</span><span class="sxs-lookup"><span data-stu-id="b1881-130">Share(s) in a role</span></span>

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

### <span data-ttu-id="b1881-131">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="b1881-131">-Confirm</span></span>
<span data-ttu-id="b1881-132">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="b1881-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b1881-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b1881-133">-WhatIf</span></span>
<span data-ttu-id="b1881-134">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="b1881-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b1881-135">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="b1881-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b1881-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1881-136">CommonParameters</span></span>
<span data-ttu-id="b1881-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b1881-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1881-138">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b1881-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1881-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b1881-139">INPUTS</span></span>

### <span data-ttu-id="b1881-140">System. String</span><span class="sxs-lookup"><span data-stu-id="b1881-140">System.String</span></span>

### <span data-ttu-id="b1881-141">Microsoft. Azure. PowerShell. cmdletar. StackEdge. Models. PSStackEdgeRole</span><span class="sxs-lookup"><span data-stu-id="b1881-141">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeRole</span></span>

## <span data-ttu-id="b1881-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b1881-142">OUTPUTS</span></span>

### <span data-ttu-id="b1881-143">Microsoft. Azure. PowerShell. cmdletar. StackEdge. Models. PSStackEdgeRole</span><span class="sxs-lookup"><span data-stu-id="b1881-143">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeRole</span></span>

## <span data-ttu-id="b1881-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b1881-144">NOTES</span></span>

## <span data-ttu-id="b1881-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b1881-145">RELATED LINKS</span></span>