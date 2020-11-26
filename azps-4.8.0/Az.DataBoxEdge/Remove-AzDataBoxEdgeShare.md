---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/remove-azdataboxedgeshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeShare.md
ms.openlocfilehash: ac3282d8249eecbb6e8c7bd1fb23a5ab0f55ed95
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94262318"
---
# <span data-ttu-id="d766d-101">Remove-AzDataBoxEdgeShare</span><span class="sxs-lookup"><span data-stu-id="d766d-101">Remove-AzDataBoxEdgeShare</span></span>

## <span data-ttu-id="d766d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d766d-102">SYNOPSIS</span></span>
<span data-ttu-id="d766d-103">Tar bort en resurs från enheten.</span><span class="sxs-lookup"><span data-stu-id="d766d-103">Removes a share from the device.</span></span>

## <span data-ttu-id="d766d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d766d-104">SYNTAX</span></span>

### <span data-ttu-id="d766d-105">DeleteByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="d766d-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzDataBoxEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d766d-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d766d-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzDataBoxEdgeShare [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d766d-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d766d-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzDataBoxEdgeShare [-InputObject] <PSDataBoxEdgeShare> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d766d-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d766d-108">DESCRIPTION</span></span>
<span data-ttu-id="d766d-109">Cmdleten **Remove-AzDataBoxEdgeEdgeShare** tar bort de associerade kanterna för en Edge-enhet.</span><span class="sxs-lookup"><span data-stu-id="d766d-109">The **Remove-AzDataBoxEdgeEdgeShare** cmdlet removes the associated edge shares for a Data Box Edge device.</span></span>

## <span data-ttu-id="d766d-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d766d-110">EXAMPLES</span></span>

### <span data-ttu-id="d766d-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="d766d-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzDataBoxEdgeShare -ResourceGroupName resourceGroupName -DeviceName deviceName -Name shareName
```

## <span data-ttu-id="d766d-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d766d-112">PARAMETERS</span></span>

### <span data-ttu-id="d766d-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d766d-113">-AsJob</span></span>
<span data-ttu-id="d766d-114">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="d766d-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d766d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d766d-115">-DefaultProfile</span></span>
<span data-ttu-id="d766d-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d766d-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d766d-117">-Enhets namn</span><span class="sxs-lookup"><span data-stu-id="d766d-117">-DeviceName</span></span>
<span data-ttu-id="d766d-118">Enhetens namn</span><span class="sxs-lookup"><span data-stu-id="d766d-118">Device Name</span></span>

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

### <span data-ttu-id="d766d-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d766d-119">-InputObject</span></span>
<span data-ttu-id="d766d-120">Infoga objekt</span><span class="sxs-lookup"><span data-stu-id="d766d-120">Input Object</span></span>

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

### <span data-ttu-id="d766d-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="d766d-121">-Name</span></span>
<span data-ttu-id="d766d-122">Resurs namn</span><span class="sxs-lookup"><span data-stu-id="d766d-122">Resource Name</span></span>

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

### <span data-ttu-id="d766d-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d766d-123">-PassThru</span></span>
<span data-ttu-id="d766d-124">Returnerar sant om det lyckas</span><span class="sxs-lookup"><span data-stu-id="d766d-124">returns true if successful</span></span>

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

### <span data-ttu-id="d766d-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d766d-125">-ResourceGroupName</span></span>
<span data-ttu-id="d766d-126">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="d766d-126">Resource Group Name</span></span>

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

### <span data-ttu-id="d766d-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d766d-127">-ResourceId</span></span>
<span data-ttu-id="d766d-128">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="d766d-128">Azure ResourceId</span></span>

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

### <span data-ttu-id="d766d-129">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="d766d-129">-Confirm</span></span>
<span data-ttu-id="d766d-130">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="d766d-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d766d-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d766d-131">-WhatIf</span></span>
<span data-ttu-id="d766d-132">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="d766d-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d766d-133">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="d766d-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d766d-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d766d-134">CommonParameters</span></span>
<span data-ttu-id="d766d-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d766d-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d766d-136">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d766d-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d766d-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d766d-137">INPUTS</span></span>

### <span data-ttu-id="d766d-138">System. String</span><span class="sxs-lookup"><span data-stu-id="d766d-138">System.String</span></span>

### <span data-ttu-id="d766d-139">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeShare</span><span class="sxs-lookup"><span data-stu-id="d766d-139">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeShare</span></span>

## <span data-ttu-id="d766d-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d766d-140">OUTPUTS</span></span>

### <span data-ttu-id="d766d-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d766d-141">System.Boolean</span></span>

## <span data-ttu-id="d766d-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d766d-142">NOTES</span></span>

## <span data-ttu-id="d766d-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d766d-143">RELATED LINKS</span></span>