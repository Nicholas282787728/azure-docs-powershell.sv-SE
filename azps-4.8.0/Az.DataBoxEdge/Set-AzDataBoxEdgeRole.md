---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/set-azdataboxedgerole
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Set-AzDataBoxEdgeRole.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Set-AzDataBoxEdgeRole.md
ms.openlocfilehash: 71e1cd6ea8f7aaa228ccdc5032971decfb21b2f2
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94102945"
---
# <span data-ttu-id="5b454-101">Set-AzDataBoxEdgeRole</span><span class="sxs-lookup"><span data-stu-id="5b454-101">Set-AzDataBoxEdgeRole</span></span>

## <span data-ttu-id="5b454-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5b454-102">SYNOPSIS</span></span>
<span data-ttu-id="5b454-103">Uppdaterar en roll för en enhet</span><span class="sxs-lookup"><span data-stu-id="5b454-103">Updates a Role for a device</span></span>

## <span data-ttu-id="5b454-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5b454-104">SYNTAX</span></span>

### <span data-ttu-id="5b454-105">SetByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="5b454-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzDataBoxEdgeRole [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -ShareName <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5b454-106">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5b454-106">SetByResourceIdParameterSet</span></span>
```
Set-AzDataBoxEdgeRole -ResourceId <String> -ShareName <String[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5b454-107">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5b454-107">SetByInputObjectParameterSet</span></span>
```
Set-AzDataBoxEdgeRole -ShareName <String[]> [-DefaultProfile <IAzureContextContainer>]
 -InputObject <PSDataBoxEdgeRole> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5b454-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5b454-108">DESCRIPTION</span></span>
<span data-ttu-id="5b454-109">Cmdleten **set-AzDataBoxEdgeRole** uppdaterar en IoT-roll för en Edge-enhet.</span><span class="sxs-lookup"><span data-stu-id="5b454-109">The **Set-AzDataBoxEdgeRole** cmdlet updates an IoT role for a Data Box Edge device.</span></span> <span data-ttu-id="5b454-110">De gamla monterade resurserna ersätts med de nya i parametern ShareName.</span><span class="sxs-lookup"><span data-stu-id="5b454-110">The old mounted shares will be replaced with the newly provided ones in the ShareName parameter.</span></span>

## <span data-ttu-id="5b454-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5b454-111">EXAMPLES</span></span>

### <span data-ttu-id="5b454-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="5b454-112">Example 1</span></span>
```powershell
PS C:\> Set-AzDataBoxEdgeRole -ResourceGroupName resourceGroupName -DeviceName deviceName -Name IotRole -ShareName sharename1,sharename2,sharename3

Name    IoTHostHub             Platform Status  IotEdgeDeviceId   IotDeviceId  ResourceGroupName
----    ----------             -------- ------  ---------------   -----------  -----------------
IotRole ehub.azure-devices.net Linux    Enabled iotEdgeDeviceUd   iotDevice    resourceGroupName
```

<span data-ttu-id="5b454-113">Dela namn ersätter de gamla monterade resurserna med de nyss tillhandahållna</span><span class="sxs-lookup"><span data-stu-id="5b454-113">Share Names will replace the old mounted shares with the newly provided ones</span></span>

### <span data-ttu-id="5b454-114">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="5b454-114">Example 2</span></span>
```powershell
PS C:\> Set-AzDataBoxEdgeRole -ResourceGroupName resourceGroupName -DeviceName deviceName -Name IotRole -ShareName @()

Name    IoTHostHub             Platform Status  IotEdgeDeviceId   IotDeviceId  ResourceGroupName
----    ----------             -------- ------  ---------------   -----------  -----------------
IotRole ehub.azure-devices.net Linux    Enabled iotEdgeDeviceUd   iotDevice    resourceGroupName
```

<span data-ttu-id="5b454-115">Demontera alla resurser</span><span class="sxs-lookup"><span data-stu-id="5b454-115">To unmount all shares</span></span>

## <span data-ttu-id="5b454-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5b454-116">PARAMETERS</span></span>

### <span data-ttu-id="5b454-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b454-117">-DefaultProfile</span></span>
<span data-ttu-id="5b454-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="5b454-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5b454-119">-Enhets namn</span><span class="sxs-lookup"><span data-stu-id="5b454-119">-DeviceName</span></span>
<span data-ttu-id="5b454-120">Enhetens namn</span><span class="sxs-lookup"><span data-stu-id="5b454-120">Device Name</span></span>

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

### <span data-ttu-id="5b454-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5b454-121">-InputObject</span></span>
<span data-ttu-id="5b454-122">Ange motsvarande enhets objekt</span><span class="sxs-lookup"><span data-stu-id="5b454-122">Please provide corresponding device object</span></span>

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

### <span data-ttu-id="5b454-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="5b454-123">-Name</span></span>
<span data-ttu-id="5b454-124">Namnet på rollen</span><span class="sxs-lookup"><span data-stu-id="5b454-124">Name of the Role</span></span>

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

### <span data-ttu-id="5b454-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5b454-125">-ResourceGroupName</span></span>
<span data-ttu-id="5b454-126">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="5b454-126">Resource Group Name</span></span>

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

### <span data-ttu-id="5b454-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5b454-127">-ResourceId</span></span>
<span data-ttu-id="5b454-128">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="5b454-128">Azure ResourceId</span></span>

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

### <span data-ttu-id="5b454-129">-ShareName</span><span class="sxs-lookup"><span data-stu-id="5b454-129">-ShareName</span></span>
<span data-ttu-id="5b454-130">Dela/ta delar i en roll</span><span class="sxs-lookup"><span data-stu-id="5b454-130">Share(s) in a role</span></span>

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

### <span data-ttu-id="5b454-131">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="5b454-131">-Confirm</span></span>
<span data-ttu-id="5b454-132">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="5b454-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5b454-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5b454-133">-WhatIf</span></span>
<span data-ttu-id="5b454-134">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="5b454-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5b454-135">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="5b454-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5b454-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b454-136">CommonParameters</span></span>
<span data-ttu-id="5b454-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5b454-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b454-138">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5b454-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b454-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5b454-139">INPUTS</span></span>

### <span data-ttu-id="5b454-140">System. String</span><span class="sxs-lookup"><span data-stu-id="5b454-140">System.String</span></span>

### <span data-ttu-id="5b454-141">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeRole</span><span class="sxs-lookup"><span data-stu-id="5b454-141">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeRole</span></span>

## <span data-ttu-id="5b454-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5b454-142">OUTPUTS</span></span>

### <span data-ttu-id="5b454-143">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeRole</span><span class="sxs-lookup"><span data-stu-id="5b454-143">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeRole</span></span>

## <span data-ttu-id="5b454-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5b454-144">NOTES</span></span>

## <span data-ttu-id="5b454-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5b454-145">RELATED LINKS</span></span>