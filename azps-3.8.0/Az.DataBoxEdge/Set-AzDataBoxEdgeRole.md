---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/set-azdataboxedgerole
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Set-AzDataBoxEdgeRole.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Set-AzDataBoxEdgeRole.md
ms.openlocfilehash: fb53f13bf6455770b272ae253a9bbe412d048064
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94088783"
---
# <span data-ttu-id="5353a-101">Set-AzDataBoxEdgeRole</span><span class="sxs-lookup"><span data-stu-id="5353a-101">Set-AzDataBoxEdgeRole</span></span>

## <span data-ttu-id="5353a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5353a-102">SYNOPSIS</span></span>
<span data-ttu-id="5353a-103">Uppdaterar en roll för en enhet</span><span class="sxs-lookup"><span data-stu-id="5353a-103">Updates a Role for a device</span></span>

## <span data-ttu-id="5353a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5353a-104">SYNTAX</span></span>

### <span data-ttu-id="5353a-105">SetByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="5353a-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzDataBoxEdgeRole [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -ShareName <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5353a-106">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5353a-106">SetByResourceIdParameterSet</span></span>
```
Set-AzDataBoxEdgeRole -ResourceId <String> -ShareName <String[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5353a-107">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5353a-107">SetByInputObjectParameterSet</span></span>
```
Set-AzDataBoxEdgeRole -ShareName <String[]> [-DefaultProfile <IAzureContextContainer>]
 -InputObject <PSDataBoxEdgeRole> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5353a-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5353a-108">DESCRIPTION</span></span>
<span data-ttu-id="5353a-109">Cmdleten **set-AzDataBoxEdgeRole** uppdaterar en IoT-roll för en Edge-enhet.</span><span class="sxs-lookup"><span data-stu-id="5353a-109">The **Set-AzDataBoxEdgeRole** cmdlet updates an IoT role for a Data Box Edge device.</span></span> <span data-ttu-id="5353a-110">De gamla monterade resurserna ersätts med de nya i parametern ShareName.</span><span class="sxs-lookup"><span data-stu-id="5353a-110">The old mounted shares will be replaced with the newly provided ones in the ShareName parameter.</span></span>

## <span data-ttu-id="5353a-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5353a-111">EXAMPLES</span></span>

### <span data-ttu-id="5353a-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="5353a-112">Example 1</span></span>
```powershell
PS C:\> Set-AzDataBoxEdgeRole -ResourceGroupName resourceGroupName -DeviceName deviceName -Name roleiot -ShareName sharename1,sharename2,sharename3

Name    IoTHostHub             Platform Status  IotEdgeDeviceId   IotDeviceId  ResourceGroupName
----    ----------             -------- ------  ---------------   -----------  -----------------
roleiot ehub.azure-devices.net Linux    Enabled iotEdgeDeviceUd   iotDevice    resourceGroupName
```

<span data-ttu-id="5353a-113">Dela namn ersätter de gamla monterade resurserna med de nyss tillhandahållna</span><span class="sxs-lookup"><span data-stu-id="5353a-113">Share Names will replace the old mounted shares with the newly provided ones</span></span>

### <span data-ttu-id="5353a-114">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="5353a-114">Example 2</span></span>
```powershell
PS C:\> Set-AzDataBoxEdgeRole -ResourceGroupName resourceGroupName -DeviceName deviceName -Name roleiot -ShareName @()

Name    IoTHostHub             Platform Status  IotEdgeDeviceId   IotDeviceId  ResourceGroupName
----    ----------             -------- ------  ---------------   -----------  -----------------
roleiot ehub.azure-devices.net Linux    Enabled iotEdgeDeviceUd   iotDevice    resourceGroupName
```

<span data-ttu-id="5353a-115">Demontera alla resurser</span><span class="sxs-lookup"><span data-stu-id="5353a-115">To unmount all shares</span></span>

## <span data-ttu-id="5353a-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5353a-116">PARAMETERS</span></span>

### <span data-ttu-id="5353a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5353a-117">-DefaultProfile</span></span>
<span data-ttu-id="5353a-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="5353a-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5353a-119">-Enhets namn</span><span class="sxs-lookup"><span data-stu-id="5353a-119">-DeviceName</span></span>
<span data-ttu-id="5353a-120">Enhetens namn</span><span class="sxs-lookup"><span data-stu-id="5353a-120">Device Name</span></span>

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

### <span data-ttu-id="5353a-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5353a-121">-InputObject</span></span>
<span data-ttu-id="5353a-122">Ange motsvarande enhets objekt</span><span class="sxs-lookup"><span data-stu-id="5353a-122">Please provide corresponding device object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeRole
Parameter Sets: SetByInputObjectParameterSet
Aliases: Role

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5353a-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="5353a-123">-Name</span></span>
<span data-ttu-id="5353a-124">Namnet på rollen</span><span class="sxs-lookup"><span data-stu-id="5353a-124">Name of the Role</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5353a-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5353a-125">-ResourceGroupName</span></span>
<span data-ttu-id="5353a-126">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="5353a-126">Resource Group Name</span></span>

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

### <span data-ttu-id="5353a-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5353a-127">-ResourceId</span></span>
<span data-ttu-id="5353a-128">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="5353a-128">Azure ResourceId</span></span>

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

### <span data-ttu-id="5353a-129">-ShareName</span><span class="sxs-lookup"><span data-stu-id="5353a-129">-ShareName</span></span>
<span data-ttu-id="5353a-130">Dela/ta delar i en roll</span><span class="sxs-lookup"><span data-stu-id="5353a-130">Share(s) in a role</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5353a-131">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="5353a-131">-Confirm</span></span>
<span data-ttu-id="5353a-132">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="5353a-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5353a-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5353a-133">-WhatIf</span></span>
<span data-ttu-id="5353a-134">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="5353a-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5353a-135">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="5353a-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5353a-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5353a-136">CommonParameters</span></span>
<span data-ttu-id="5353a-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5353a-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5353a-138">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5353a-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5353a-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5353a-139">INPUTS</span></span>

### <span data-ttu-id="5353a-140">System. String</span><span class="sxs-lookup"><span data-stu-id="5353a-140">System.String</span></span>

### <span data-ttu-id="5353a-141">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeRole</span><span class="sxs-lookup"><span data-stu-id="5353a-141">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeRole</span></span>

## <span data-ttu-id="5353a-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5353a-142">OUTPUTS</span></span>

### <span data-ttu-id="5353a-143">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeRole</span><span class="sxs-lookup"><span data-stu-id="5353a-143">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeRole</span></span>

## <span data-ttu-id="5353a-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5353a-144">NOTES</span></span>

## <span data-ttu-id="5353a-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5353a-145">RELATED LINKS</span></span>