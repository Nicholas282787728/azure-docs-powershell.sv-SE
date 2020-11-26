---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/remove-azdataboxedgedevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeDevice.md
ms.openlocfilehash: 69a484734dfde2459cf05f6eea763a8433b15827
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94260079"
---
# <span data-ttu-id="1b48f-101">Remove-AzDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="1b48f-101">Remove-AzDataBoxEdgeDevice</span></span>

## <span data-ttu-id="1b48f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1b48f-102">SYNOPSIS</span></span>
<span data-ttu-id="1b48f-103">Tar bort en kant linje för en data ruta.</span><span class="sxs-lookup"><span data-stu-id="1b48f-103">Removes a Data Box Edge device.</span></span>

## <span data-ttu-id="1b48f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1b48f-104">SYNTAX</span></span>

### <span data-ttu-id="1b48f-105">DeleteByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="1b48f-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzDataBoxEdgeDevice [-ResourceGroupName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1b48f-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1b48f-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzDataBoxEdgeDevice -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-PassThru]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1b48f-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1b48f-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzDataBoxEdgeDevice -InputObject <PSDataBoxEdgeDevice> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1b48f-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1b48f-108">DESCRIPTION</span></span>
<span data-ttu-id="1b48f-109">Cmdleten **Remove-AzDataBoxEdgeDevice** tar bort konfigurationen för en Edge-enhet.</span><span class="sxs-lookup"><span data-stu-id="1b48f-109">The **Remove-AzDataBoxEdgeDevice** cmdlet removes the configuration for a Data Box Edge device.</span></span>
<span data-ttu-id="1b48f-110">Observera att enheten bara kan tas bort när du har placerat beställningen och innan enheten förbereds av Microsoft för leverans.</span><span class="sxs-lookup"><span data-stu-id="1b48f-110">Note that the device can only be deleted after you have placed the order and before the device is prepared by Microsoft for shipment.</span></span>

<span data-ttu-id="1b48f-111">Läs dokumentationen om hur du tar bort resursen innan du använder denna [cmdlet](https://docs.microsoft.com/en-us/azure/databox-online/data-box-edge-return-device#delete-the-resource)</span><span class="sxs-lookup"><span data-stu-id="1b48f-111">Refer the documentation on Deleting the resource before using this [cmdlet](https://docs.microsoft.com/en-us/azure/databox-online/data-box-edge-return-device#delete-the-resource)</span></span>

## <span data-ttu-id="1b48f-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1b48f-112">EXAMPLES</span></span>

### <span data-ttu-id="1b48f-113">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="1b48f-113">Example 1</span></span>
```powershell
PS C:\> Remove-AzDataBoxEdgeDevice ResourceGroupName resourceGroupName -Name deviceName
```

## <span data-ttu-id="1b48f-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1b48f-114">PARAMETERS</span></span>

### <span data-ttu-id="1b48f-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1b48f-115">-AsJob</span></span>
<span data-ttu-id="1b48f-116">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="1b48f-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1b48f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b48f-117">-DefaultProfile</span></span>
<span data-ttu-id="1b48f-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="1b48f-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1b48f-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1b48f-119">-InputObject</span></span>
<span data-ttu-id="1b48f-120">Infoga objekt</span><span class="sxs-lookup"><span data-stu-id="1b48f-120">Input Object</span></span>

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

### <span data-ttu-id="1b48f-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="1b48f-121">-Name</span></span>
<span data-ttu-id="1b48f-122">Resurs namn</span><span class="sxs-lookup"><span data-stu-id="1b48f-122">Resource Name</span></span>

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

### <span data-ttu-id="1b48f-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1b48f-123">-PassThru</span></span>
<span data-ttu-id="1b48f-124">Returnerar sant om det lyckas</span><span class="sxs-lookup"><span data-stu-id="1b48f-124">returns true if successful</span></span>

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

### <span data-ttu-id="1b48f-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1b48f-125">-ResourceGroupName</span></span>
<span data-ttu-id="1b48f-126">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="1b48f-126">Resource Group Name</span></span>

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

### <span data-ttu-id="1b48f-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1b48f-127">-ResourceId</span></span>
<span data-ttu-id="1b48f-128">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="1b48f-128">Azure ResourceId</span></span>

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

### <span data-ttu-id="1b48f-129">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="1b48f-129">-Confirm</span></span>
<span data-ttu-id="1b48f-130">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="1b48f-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1b48f-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1b48f-131">-WhatIf</span></span>
<span data-ttu-id="1b48f-132">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="1b48f-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1b48f-133">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="1b48f-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1b48f-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b48f-134">CommonParameters</span></span>
<span data-ttu-id="1b48f-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1b48f-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b48f-136">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1b48f-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b48f-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1b48f-137">INPUTS</span></span>

### <span data-ttu-id="1b48f-138">System. String</span><span class="sxs-lookup"><span data-stu-id="1b48f-138">System.String</span></span>

### <span data-ttu-id="1b48f-139">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="1b48f-139">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span></span>

## <span data-ttu-id="1b48f-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1b48f-140">OUTPUTS</span></span>

### <span data-ttu-id="1b48f-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="1b48f-141">System.Boolean</span></span>

## <span data-ttu-id="1b48f-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1b48f-142">NOTES</span></span>

## <span data-ttu-id="1b48f-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1b48f-143">RELATED LINKS</span></span>