---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/remove-azdataboxedgedevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeDevice.md
ms.openlocfilehash: 69a484734dfde2459cf05f6eea763a8433b15827
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94321152"
---
# <span data-ttu-id="8760e-101">Remove-AzDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="8760e-101">Remove-AzDataBoxEdgeDevice</span></span>

## <span data-ttu-id="8760e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8760e-102">SYNOPSIS</span></span>
<span data-ttu-id="8760e-103">Tar bort en kant linje för en data ruta.</span><span class="sxs-lookup"><span data-stu-id="8760e-103">Removes a Data Box Edge device.</span></span>

## <span data-ttu-id="8760e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8760e-104">SYNTAX</span></span>

### <span data-ttu-id="8760e-105">DeleteByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="8760e-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzDataBoxEdgeDevice [-ResourceGroupName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8760e-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8760e-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzDataBoxEdgeDevice -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-PassThru]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8760e-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8760e-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzDataBoxEdgeDevice -InputObject <PSDataBoxEdgeDevice> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8760e-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8760e-108">DESCRIPTION</span></span>
<span data-ttu-id="8760e-109">Cmdleten **Remove-AzDataBoxEdgeDevice** tar bort konfigurationen för en Edge-enhet.</span><span class="sxs-lookup"><span data-stu-id="8760e-109">The **Remove-AzDataBoxEdgeDevice** cmdlet removes the configuration for a Data Box Edge device.</span></span>
<span data-ttu-id="8760e-110">Observera att enheten bara kan tas bort när du har placerat beställningen och innan enheten förbereds av Microsoft för leverans.</span><span class="sxs-lookup"><span data-stu-id="8760e-110">Note that the device can only be deleted after you have placed the order and before the device is prepared by Microsoft for shipment.</span></span>

<span data-ttu-id="8760e-111">Läs dokumentationen om hur du tar bort resursen innan du använder denna [cmdlet](https://docs.microsoft.com/en-us/azure/databox-online/data-box-edge-return-device#delete-the-resource)</span><span class="sxs-lookup"><span data-stu-id="8760e-111">Refer the documentation on Deleting the resource before using this [cmdlet](https://docs.microsoft.com/en-us/azure/databox-online/data-box-edge-return-device#delete-the-resource)</span></span>

## <span data-ttu-id="8760e-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8760e-112">EXAMPLES</span></span>

### <span data-ttu-id="8760e-113">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="8760e-113">Example 1</span></span>
```powershell
PS C:\> Remove-AzDataBoxEdgeDevice ResourceGroupName resourceGroupName -Name deviceName
```

## <span data-ttu-id="8760e-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8760e-114">PARAMETERS</span></span>

### <span data-ttu-id="8760e-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8760e-115">-AsJob</span></span>
<span data-ttu-id="8760e-116">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="8760e-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8760e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8760e-117">-DefaultProfile</span></span>
<span data-ttu-id="8760e-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="8760e-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8760e-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8760e-119">-InputObject</span></span>
<span data-ttu-id="8760e-120">Infoga objekt</span><span class="sxs-lookup"><span data-stu-id="8760e-120">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8760e-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="8760e-121">-Name</span></span>
<span data-ttu-id="8760e-122">Resurs namn</span><span class="sxs-lookup"><span data-stu-id="8760e-122">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8760e-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8760e-123">-PassThru</span></span>
<span data-ttu-id="8760e-124">Returnerar sant om det lyckas</span><span class="sxs-lookup"><span data-stu-id="8760e-124">returns true if successful</span></span>

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

### <span data-ttu-id="8760e-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8760e-125">-ResourceGroupName</span></span>
<span data-ttu-id="8760e-126">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="8760e-126">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8760e-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8760e-127">-ResourceId</span></span>
<span data-ttu-id="8760e-128">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="8760e-128">Azure ResourceId</span></span>

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

### <span data-ttu-id="8760e-129">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="8760e-129">-Confirm</span></span>
<span data-ttu-id="8760e-130">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="8760e-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8760e-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8760e-131">-WhatIf</span></span>
<span data-ttu-id="8760e-132">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="8760e-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8760e-133">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="8760e-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8760e-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8760e-134">CommonParameters</span></span>
<span data-ttu-id="8760e-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8760e-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8760e-136">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8760e-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8760e-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8760e-137">INPUTS</span></span>

### <span data-ttu-id="8760e-138">System. String</span><span class="sxs-lookup"><span data-stu-id="8760e-138">System.String</span></span>

### <span data-ttu-id="8760e-139">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="8760e-139">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span></span>

## <span data-ttu-id="8760e-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8760e-140">OUTPUTS</span></span>

### <span data-ttu-id="8760e-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="8760e-141">System.Boolean</span></span>

## <span data-ttu-id="8760e-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8760e-142">NOTES</span></span>

## <span data-ttu-id="8760e-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8760e-143">RELATED LINKS</span></span>
