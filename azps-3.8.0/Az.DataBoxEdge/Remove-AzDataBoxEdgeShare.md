---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/remove-azdataboxedgeshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeShare.md
ms.openlocfilehash: ac3282d8249eecbb6e8c7bd1fb23a5ab0f55ed95
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94092299"
---
# <span data-ttu-id="978b0-101">Remove-AzDataBoxEdgeShare</span><span class="sxs-lookup"><span data-stu-id="978b0-101">Remove-AzDataBoxEdgeShare</span></span>

## <span data-ttu-id="978b0-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="978b0-102">SYNOPSIS</span></span>
<span data-ttu-id="978b0-103">Tar bort en resurs från enheten.</span><span class="sxs-lookup"><span data-stu-id="978b0-103">Removes a share from the device.</span></span>

## <span data-ttu-id="978b0-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="978b0-104">SYNTAX</span></span>

### <span data-ttu-id="978b0-105">DeleteByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="978b0-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzDataBoxEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="978b0-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="978b0-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzDataBoxEdgeShare [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="978b0-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="978b0-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzDataBoxEdgeShare [-InputObject] <PSDataBoxEdgeShare> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="978b0-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="978b0-108">DESCRIPTION</span></span>
<span data-ttu-id="978b0-109">Cmdleten **Remove-AzDataBoxEdgeEdgeShare** tar bort de associerade kanterna för en Edge-enhet.</span><span class="sxs-lookup"><span data-stu-id="978b0-109">The **Remove-AzDataBoxEdgeEdgeShare** cmdlet removes the associated edge shares for a Data Box Edge device.</span></span>

## <span data-ttu-id="978b0-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="978b0-110">EXAMPLES</span></span>

### <span data-ttu-id="978b0-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="978b0-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzDataBoxEdgeShare -ResourceGroupName resourceGroupName -DeviceName deviceName -Name shareName
```

## <span data-ttu-id="978b0-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="978b0-112">PARAMETERS</span></span>

### <span data-ttu-id="978b0-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="978b0-113">-AsJob</span></span>
<span data-ttu-id="978b0-114">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="978b0-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="978b0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="978b0-115">-DefaultProfile</span></span>
<span data-ttu-id="978b0-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="978b0-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="978b0-117">-Enhets namn</span><span class="sxs-lookup"><span data-stu-id="978b0-117">-DeviceName</span></span>
<span data-ttu-id="978b0-118">Enhetens namn</span><span class="sxs-lookup"><span data-stu-id="978b0-118">Device Name</span></span>

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

### <span data-ttu-id="978b0-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="978b0-119">-InputObject</span></span>
<span data-ttu-id="978b0-120">Infoga objekt</span><span class="sxs-lookup"><span data-stu-id="978b0-120">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeShare
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="978b0-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="978b0-121">-Name</span></span>
<span data-ttu-id="978b0-122">Resurs namn</span><span class="sxs-lookup"><span data-stu-id="978b0-122">Resource Name</span></span>

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

### <span data-ttu-id="978b0-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="978b0-123">-PassThru</span></span>
<span data-ttu-id="978b0-124">Returnerar sant om det lyckas</span><span class="sxs-lookup"><span data-stu-id="978b0-124">returns true if successful</span></span>

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

### <span data-ttu-id="978b0-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="978b0-125">-ResourceGroupName</span></span>
<span data-ttu-id="978b0-126">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="978b0-126">Resource Group Name</span></span>

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

### <span data-ttu-id="978b0-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="978b0-127">-ResourceId</span></span>
<span data-ttu-id="978b0-128">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="978b0-128">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="978b0-129">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="978b0-129">-Confirm</span></span>
<span data-ttu-id="978b0-130">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="978b0-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="978b0-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="978b0-131">-WhatIf</span></span>
<span data-ttu-id="978b0-132">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="978b0-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="978b0-133">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="978b0-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="978b0-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="978b0-134">CommonParameters</span></span>
<span data-ttu-id="978b0-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="978b0-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="978b0-136">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="978b0-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="978b0-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="978b0-137">INPUTS</span></span>

### <span data-ttu-id="978b0-138">System. String</span><span class="sxs-lookup"><span data-stu-id="978b0-138">System.String</span></span>

### <span data-ttu-id="978b0-139">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeShare</span><span class="sxs-lookup"><span data-stu-id="978b0-139">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeShare</span></span>

## <span data-ttu-id="978b0-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="978b0-140">OUTPUTS</span></span>

### <span data-ttu-id="978b0-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="978b0-141">System.Boolean</span></span>

## <span data-ttu-id="978b0-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="978b0-142">NOTES</span></span>

## <span data-ttu-id="978b0-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="978b0-143">RELATED LINKS</span></span>
