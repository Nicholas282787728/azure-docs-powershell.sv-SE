---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/remove-azstackedgedevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeDevice.md
ms.openlocfilehash: 431726e1bcbc0045cb1b9958ce9513638259bd8f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94261549"
---
# <span data-ttu-id="c6569-101">Remove-AzStackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="c6569-101">Remove-AzStackEdgeDevice</span></span>

## <span data-ttu-id="c6569-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c6569-102">SYNOPSIS</span></span>
<span data-ttu-id="c6569-103">Tar bort en trave Edge-enhet.</span><span class="sxs-lookup"><span data-stu-id="c6569-103">Removes a Stack Edge device.</span></span>

## <span data-ttu-id="c6569-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c6569-104">SYNTAX</span></span>

### <span data-ttu-id="c6569-105">DeleteByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="c6569-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzStackEdgeDevice [-ResourceGroupName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c6569-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c6569-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzStackEdgeDevice -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-PassThru]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c6569-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c6569-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzStackEdgeDevice -DeviceObject <PSStackEdgeDevice> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c6569-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c6569-108">DESCRIPTION</span></span>
<span data-ttu-id="c6569-109">Cmdleten **Remove-AzStackEdgeDevice** tar bort konfigurationen för en trave Edge-enhet.</span><span class="sxs-lookup"><span data-stu-id="c6569-109">The **Remove-AzStackEdgeDevice** cmdlet removes the configuration for a Stack Edge device.</span></span>
<span data-ttu-id="c6569-110">Observera att enheten bara kan tas bort när du har placerat beställningen och innan enheten förbereds av Microsoft för leverans.</span><span class="sxs-lookup"><span data-stu-id="c6569-110">Note that the device can only be deleted after you have placed the order and before the device is prepared by Microsoft for shipment.</span></span>

<span data-ttu-id="c6569-111">Läs dokumentationen om hur du tar bort resursen innan du använder denna [cmdlet](https://docs.microsoft.com/en-us/azure/databox-online/data-box-edge-return-device#delete-the-resource)</span><span class="sxs-lookup"><span data-stu-id="c6569-111">Refer the documentation on Deleting the resource before using this [cmdlet](https://docs.microsoft.com/en-us/azure/databox-online/data-box-edge-return-device#delete-the-resource)</span></span>

## <span data-ttu-id="c6569-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c6569-112">EXAMPLES</span></span>

### <span data-ttu-id="c6569-113">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="c6569-113">Example 1</span></span>
```powershell
PS C:\> Remove-AzStackEdgeDevice ResourceGroupName resourceGroupName -Name deviceName
```

## <span data-ttu-id="c6569-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c6569-114">PARAMETERS</span></span>

### <span data-ttu-id="c6569-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c6569-115">-AsJob</span></span>
<span data-ttu-id="c6569-116">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="c6569-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c6569-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6569-117">-DefaultProfile</span></span>
<span data-ttu-id="c6569-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c6569-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c6569-119">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="c6569-119">-DeviceObject</span></span>
<span data-ttu-id="c6569-120">Infoga objekt</span><span class="sxs-lookup"><span data-stu-id="c6569-120">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice
Parameter Sets: DeleteByInputObjectParameterSet
Aliases: Device

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c6569-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="c6569-121">-Name</span></span>
<span data-ttu-id="c6569-122">Resurs namn</span><span class="sxs-lookup"><span data-stu-id="c6569-122">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases: DeviceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c6569-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c6569-123">-PassThru</span></span>
<span data-ttu-id="c6569-124">Returnerar sant om det lyckas</span><span class="sxs-lookup"><span data-stu-id="c6569-124">returns true if successful</span></span>

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

### <span data-ttu-id="c6569-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c6569-125">-ResourceGroupName</span></span>
<span data-ttu-id="c6569-126">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="c6569-126">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c6569-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c6569-127">-ResourceId</span></span>
<span data-ttu-id="c6569-128">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="c6569-128">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c6569-129">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="c6569-129">-Confirm</span></span>
<span data-ttu-id="c6569-130">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="c6569-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c6569-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c6569-131">-WhatIf</span></span>
<span data-ttu-id="c6569-132">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="c6569-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c6569-133">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="c6569-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c6569-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6569-134">CommonParameters</span></span>
<span data-ttu-id="c6569-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c6569-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6569-136">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c6569-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6569-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c6569-137">INPUTS</span></span>

### <span data-ttu-id="c6569-138">System. String</span><span class="sxs-lookup"><span data-stu-id="c6569-138">System.String</span></span>

### <span data-ttu-id="c6569-139">Microsoft. Azure. PowerShell. cmdletar. StackEdge. Models. PSStackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="c6569-139">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span></span>

## <span data-ttu-id="c6569-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c6569-140">OUTPUTS</span></span>

### <span data-ttu-id="c6569-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c6569-141">System.Boolean</span></span>

## <span data-ttu-id="c6569-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c6569-142">NOTES</span></span>

## <span data-ttu-id="c6569-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c6569-143">RELATED LINKS</span></span>
