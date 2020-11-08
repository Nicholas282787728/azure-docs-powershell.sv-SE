---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/remove-azstackedgebandwidthschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeBandwidthSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeBandwidthSchedule.md
ms.openlocfilehash: f3f38feff8b6d855121a6772cfb56ef0b57cebfd
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94088462"
---
# <span data-ttu-id="008b9-101">Remove-AzStackEdgeBandwidthSchedule</span><span class="sxs-lookup"><span data-stu-id="008b9-101">Remove-AzStackEdgeBandwidthSchedule</span></span>

## <span data-ttu-id="008b9-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="008b9-102">SYNOPSIS</span></span>
<span data-ttu-id="008b9-103">Tar bort ett bandbredds schema.</span><span class="sxs-lookup"><span data-stu-id="008b9-103">Removes a Bandwidth Schedule.</span></span>

## <span data-ttu-id="008b9-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="008b9-104">SYNTAX</span></span>

### <span data-ttu-id="008b9-105">DeleteByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="008b9-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzStackEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="008b9-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="008b9-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzStackEdgeBandwidthSchedule -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="008b9-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="008b9-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzStackEdgeBandwidthSchedule -InputObject <PSStackEdgeBandWidthSchedule> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="008b9-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="008b9-108">DESCRIPTION</span></span>
<span data-ttu-id="008b9-109">Cmdleten **Remove-AzStackEdgeBandwidthSchedule** tar bort bandbredds schema för en stack Edge-enhet.</span><span class="sxs-lookup"><span data-stu-id="008b9-109">The **Remove-AzStackEdgeBandwidthSchedule** cmdlet removes the Bandwidth schedule for a Stack Edge device.</span></span> 

## <span data-ttu-id="008b9-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="008b9-110">EXAMPLES</span></span>

### <span data-ttu-id="008b9-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="008b9-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzStackEdgeBandwidthSchedule -ResourceGroupName resourceGroupName -DeviceName deviceName -Name bandwidthSchedule
```

## <span data-ttu-id="008b9-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="008b9-112">PARAMETERS</span></span>

### <span data-ttu-id="008b9-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="008b9-113">-AsJob</span></span>
<span data-ttu-id="008b9-114">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="008b9-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="008b9-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="008b9-115">-DefaultProfile</span></span>
<span data-ttu-id="008b9-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="008b9-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="008b9-117">-Enhets namn</span><span class="sxs-lookup"><span data-stu-id="008b9-117">-DeviceName</span></span>
<span data-ttu-id="008b9-118">Enhetens namn</span><span class="sxs-lookup"><span data-stu-id="008b9-118">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="008b9-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="008b9-119">-InputObject</span></span>
<span data-ttu-id="008b9-120">Infoga objekt</span><span class="sxs-lookup"><span data-stu-id="008b9-120">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeBandWidthSchedule
Parameter Sets: DeleteByInputObjectParameterSet
Aliases: BandwidthSchedule

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="008b9-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="008b9-121">-Name</span></span>
<span data-ttu-id="008b9-122">Resurs namn</span><span class="sxs-lookup"><span data-stu-id="008b9-122">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases: BandwidthScheduleName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="008b9-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="008b9-123">-PassThru</span></span>
<span data-ttu-id="008b9-124">Returnerar sant om det lyckas</span><span class="sxs-lookup"><span data-stu-id="008b9-124">returns true if successful</span></span>

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

### <span data-ttu-id="008b9-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="008b9-125">-ResourceGroupName</span></span>
<span data-ttu-id="008b9-126">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="008b9-126">Resource Group Name</span></span>

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

### <span data-ttu-id="008b9-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="008b9-127">-ResourceId</span></span>
<span data-ttu-id="008b9-128">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="008b9-128">Azure ResourceId</span></span>

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

### <span data-ttu-id="008b9-129">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="008b9-129">-Confirm</span></span>
<span data-ttu-id="008b9-130">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="008b9-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="008b9-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="008b9-131">-WhatIf</span></span>
<span data-ttu-id="008b9-132">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="008b9-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="008b9-133">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="008b9-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="008b9-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="008b9-134">CommonParameters</span></span>
<span data-ttu-id="008b9-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="008b9-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="008b9-136">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="008b9-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="008b9-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="008b9-137">INPUTS</span></span>

### <span data-ttu-id="008b9-138">System. String</span><span class="sxs-lookup"><span data-stu-id="008b9-138">System.String</span></span>

### <span data-ttu-id="008b9-139">Microsoft. Azure. PowerShell. cmdletar. StackEdge. Models. PSStackEdgeBandWidthSchedule</span><span class="sxs-lookup"><span data-stu-id="008b9-139">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeBandWidthSchedule</span></span>

## <span data-ttu-id="008b9-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="008b9-140">OUTPUTS</span></span>

### <span data-ttu-id="008b9-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="008b9-141">System.Boolean</span></span>

## <span data-ttu-id="008b9-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="008b9-142">NOTES</span></span>

## <span data-ttu-id="008b9-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="008b9-143">RELATED LINKS</span></span>
