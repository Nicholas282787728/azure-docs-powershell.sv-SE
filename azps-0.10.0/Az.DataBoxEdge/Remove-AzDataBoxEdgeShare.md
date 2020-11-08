---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/remove-azdataboxedgeshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeShare.md
ms.openlocfilehash: 0ff44dcf31b62626f17933732f9097c3c088e0b2
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93924622"
---
# <span data-ttu-id="2aa40-101">Remove-AzDataBoxEdgeShare</span><span class="sxs-lookup"><span data-stu-id="2aa40-101">Remove-AzDataBoxEdgeShare</span></span>

## <span data-ttu-id="2aa40-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2aa40-102">SYNOPSIS</span></span>
<span data-ttu-id="2aa40-103">Tar bort en resurs från enheten.</span><span class="sxs-lookup"><span data-stu-id="2aa40-103">Removes a share from the device.</span></span>

## <span data-ttu-id="2aa40-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2aa40-104">SYNTAX</span></span>

### <span data-ttu-id="2aa40-105">DeleteByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="2aa40-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzDataBoxEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2aa40-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2aa40-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzDataBoxEdgeShare [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2aa40-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2aa40-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzDataBoxEdgeShare [-InputObject] <PSDataBoxEdgeShare> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2aa40-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2aa40-108">DESCRIPTION</span></span>
<span data-ttu-id="2aa40-109">Cmdleten **Remove-AzDataBoxEdgeEdgeShare** tar bort de associerade kanterna för en Edge-enhet.</span><span class="sxs-lookup"><span data-stu-id="2aa40-109">The **Remove-AzDataBoxEdgeEdgeShare** cmdlet removes the associated edge shares for a Data Box Edge device.</span></span>

## <span data-ttu-id="2aa40-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2aa40-110">EXAMPLES</span></span>

### <span data-ttu-id="2aa40-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="2aa40-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzDataBoxEdgeShare -ResourceGroupName resourceGroupName -DeviceName deviceName -Name shareName
```

## <span data-ttu-id="2aa40-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2aa40-112">PARAMETERS</span></span>

### <span data-ttu-id="2aa40-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2aa40-113">-AsJob</span></span>
<span data-ttu-id="2aa40-114">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="2aa40-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2aa40-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2aa40-115">-DefaultProfile</span></span>
<span data-ttu-id="2aa40-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="2aa40-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2aa40-117">-Enhets namn</span><span class="sxs-lookup"><span data-stu-id="2aa40-117">-DeviceName</span></span>
<span data-ttu-id="2aa40-118">Enhetens namn</span><span class="sxs-lookup"><span data-stu-id="2aa40-118">Device Name</span></span>

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

### <span data-ttu-id="2aa40-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2aa40-119">-InputObject</span></span>
<span data-ttu-id="2aa40-120">Infoga objekt</span><span class="sxs-lookup"><span data-stu-id="2aa40-120">Input Object</span></span>

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

### <span data-ttu-id="2aa40-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="2aa40-121">-Name</span></span>
<span data-ttu-id="2aa40-122">Resurs namn</span><span class="sxs-lookup"><span data-stu-id="2aa40-122">Resource Name</span></span>

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

### <span data-ttu-id="2aa40-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2aa40-123">-PassThru</span></span>
<span data-ttu-id="2aa40-124">Returnerar sant om det lyckas</span><span class="sxs-lookup"><span data-stu-id="2aa40-124">returns true if successful</span></span>

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

### <span data-ttu-id="2aa40-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2aa40-125">-ResourceGroupName</span></span>
<span data-ttu-id="2aa40-126">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="2aa40-126">Resource Group Name</span></span>

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

### <span data-ttu-id="2aa40-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2aa40-127">-ResourceId</span></span>
<span data-ttu-id="2aa40-128">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="2aa40-128">Azure ResourceId</span></span>

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

### <span data-ttu-id="2aa40-129">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="2aa40-129">-Confirm</span></span>
<span data-ttu-id="2aa40-130">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="2aa40-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2aa40-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2aa40-131">-WhatIf</span></span>
<span data-ttu-id="2aa40-132">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="2aa40-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2aa40-133">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="2aa40-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2aa40-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2aa40-134">CommonParameters</span></span>
<span data-ttu-id="2aa40-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2aa40-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2aa40-136">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2aa40-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2aa40-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2aa40-137">INPUTS</span></span>

### <span data-ttu-id="2aa40-138">System. String</span><span class="sxs-lookup"><span data-stu-id="2aa40-138">System.String</span></span>

### <span data-ttu-id="2aa40-139">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeShare</span><span class="sxs-lookup"><span data-stu-id="2aa40-139">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeShare</span></span>

## <span data-ttu-id="2aa40-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2aa40-140">OUTPUTS</span></span>

### <span data-ttu-id="2aa40-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="2aa40-141">System.Boolean</span></span>

## <span data-ttu-id="2aa40-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2aa40-142">NOTES</span></span>

## <span data-ttu-id="2aa40-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2aa40-143">RELATED LINKS</span></span>