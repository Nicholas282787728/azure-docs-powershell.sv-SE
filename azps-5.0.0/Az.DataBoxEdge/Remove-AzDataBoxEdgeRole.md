---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/remove-azdataboxedgerole
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeRole.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeRole.md
ms.openlocfilehash: b3a99d286c0efcf76dee0c71d8d3b5f4e704ca40
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94321144"
---
# <span data-ttu-id="e7f2b-101">Remove-AzDataBoxEdgeRole</span><span class="sxs-lookup"><span data-stu-id="e7f2b-101">Remove-AzDataBoxEdgeRole</span></span>

## <span data-ttu-id="e7f2b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e7f2b-102">SYNOPSIS</span></span>
<span data-ttu-id="e7f2b-103">Tar bort den tillhör ande IoT-rollen för en enhet.</span><span class="sxs-lookup"><span data-stu-id="e7f2b-103">Removes the associated IoT role for a device.</span></span>

## <span data-ttu-id="e7f2b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e7f2b-104">SYNTAX</span></span>

### <span data-ttu-id="e7f2b-105">DeleteByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="e7f2b-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzDataBoxEdgeRole [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e7f2b-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e7f2b-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzDataBoxEdgeRole -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-PassThru]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e7f2b-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e7f2b-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzDataBoxEdgeRole -InputObject <PSDataBoxEdgeRole> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e7f2b-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e7f2b-108">DESCRIPTION</span></span>
<span data-ttu-id="e7f2b-109">Cmdleten **Remove-AzDataBoxEdgeRole** tar bort den tillhör ande IoT-rollen för en Edge-enhet.</span><span class="sxs-lookup"><span data-stu-id="e7f2b-109">The **Remove-AzDataBoxEdgeRole** cmdlet removes the associated IoT role for a Data Box Edge device.</span></span>

## <span data-ttu-id="e7f2b-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e7f2b-110">EXAMPLES</span></span>

### <span data-ttu-id="e7f2b-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="e7f2b-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzDataBoxEdgeRole -ResourceGroupName resourceGroupName -DeviceName deviceName -Name roleName
```

## <span data-ttu-id="e7f2b-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e7f2b-112">PARAMETERS</span></span>

### <span data-ttu-id="e7f2b-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e7f2b-113">-AsJob</span></span>
<span data-ttu-id="e7f2b-114">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="e7f2b-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e7f2b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7f2b-115">-DefaultProfile</span></span>
<span data-ttu-id="e7f2b-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e7f2b-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e7f2b-117">-Enhets namn</span><span class="sxs-lookup"><span data-stu-id="e7f2b-117">-DeviceName</span></span>
<span data-ttu-id="e7f2b-118">Enhetens namn</span><span class="sxs-lookup"><span data-stu-id="e7f2b-118">Device Name</span></span>

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

### <span data-ttu-id="e7f2b-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e7f2b-119">-InputObject</span></span>
<span data-ttu-id="e7f2b-120">Infoga objekt</span><span class="sxs-lookup"><span data-stu-id="e7f2b-120">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeRole
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e7f2b-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="e7f2b-121">-Name</span></span>
<span data-ttu-id="e7f2b-122">Resurs namn</span><span class="sxs-lookup"><span data-stu-id="e7f2b-122">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7f2b-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e7f2b-123">-PassThru</span></span>
<span data-ttu-id="e7f2b-124">Returnerar sant om det lyckas</span><span class="sxs-lookup"><span data-stu-id="e7f2b-124">returns true if successful</span></span>

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

### <span data-ttu-id="e7f2b-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e7f2b-125">-ResourceGroupName</span></span>
<span data-ttu-id="e7f2b-126">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="e7f2b-126">Resource Group Name</span></span>

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

### <span data-ttu-id="e7f2b-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e7f2b-127">-ResourceId</span></span>
<span data-ttu-id="e7f2b-128">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="e7f2b-128">Azure ResourceId</span></span>

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

### <span data-ttu-id="e7f2b-129">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="e7f2b-129">-Confirm</span></span>
<span data-ttu-id="e7f2b-130">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="e7f2b-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e7f2b-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e7f2b-131">-WhatIf</span></span>
<span data-ttu-id="e7f2b-132">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="e7f2b-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e7f2b-133">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="e7f2b-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e7f2b-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7f2b-134">CommonParameters</span></span>
<span data-ttu-id="e7f2b-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e7f2b-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7f2b-136">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e7f2b-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7f2b-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e7f2b-137">INPUTS</span></span>

### <span data-ttu-id="e7f2b-138">System. String</span><span class="sxs-lookup"><span data-stu-id="e7f2b-138">System.String</span></span>

### <span data-ttu-id="e7f2b-139">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeRole</span><span class="sxs-lookup"><span data-stu-id="e7f2b-139">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeRole</span></span>

## <span data-ttu-id="e7f2b-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e7f2b-140">OUTPUTS</span></span>

### <span data-ttu-id="e7f2b-141">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeRole</span><span class="sxs-lookup"><span data-stu-id="e7f2b-141">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeRole</span></span>

## <span data-ttu-id="e7f2b-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e7f2b-142">NOTES</span></span>

## <span data-ttu-id="e7f2b-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e7f2b-143">RELATED LINKS</span></span>
