---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/remove-azdataboxedgetrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeTrigger.md
ms.openlocfilehash: a9b0d3565e2266373d3ba553be94ffd8a24707d0
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98404035"
---
# <span data-ttu-id="73f03-101">Remove-AzDataBoxEdgeTrigger</span><span class="sxs-lookup"><span data-stu-id="73f03-101">Remove-AzDataBoxEdgeTrigger</span></span>

## <span data-ttu-id="73f03-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="73f03-102">SYNOPSIS</span></span>
<span data-ttu-id="73f03-103">Tar bort en befintlig utlösare på enheten.</span><span class="sxs-lookup"><span data-stu-id="73f03-103">Removes an existing trigger on the device.</span></span>

## <span data-ttu-id="73f03-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="73f03-104">SYNTAX</span></span>

### <span data-ttu-id="73f03-105">DeleteByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="73f03-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzDataBoxEdgeTrigger [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="73f03-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="73f03-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzDataBoxEdgeTrigger [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="73f03-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="73f03-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzDataBoxEdgeTrigger [-InputObject] <PSDataBoxEdgeTrigger> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="73f03-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="73f03-108">DESCRIPTION</span></span>
<span data-ttu-id="73f03-109">Cmdleten **Remove-AzDataBoxEdgeTrigger** tar bort en befintlig utlösare för Edge-enheten.</span><span class="sxs-lookup"><span data-stu-id="73f03-109">The **Remove-AzDataBoxEdgeTrigger** cmdlet removes an existing trigger on the Data Box Edge device.</span></span>

## <span data-ttu-id="73f03-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="73f03-110">EXAMPLES</span></span>

### <span data-ttu-id="73f03-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="73f03-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzDataBoxEdgeTrigger -ResourceGroupName resourceGroupName -DeviceName deviceName -Name triggerName
```

## <span data-ttu-id="73f03-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="73f03-112">PARAMETERS</span></span>

### <span data-ttu-id="73f03-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="73f03-113">-AsJob</span></span>
<span data-ttu-id="73f03-114">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="73f03-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="73f03-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73f03-115">-DefaultProfile</span></span>
<span data-ttu-id="73f03-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="73f03-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="73f03-117">-Enhets namn</span><span class="sxs-lookup"><span data-stu-id="73f03-117">-DeviceName</span></span>
<span data-ttu-id="73f03-118">Enhetens namn</span><span class="sxs-lookup"><span data-stu-id="73f03-118">Device Name</span></span>

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

### <span data-ttu-id="73f03-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="73f03-119">-InputObject</span></span>
<span data-ttu-id="73f03-120">Infoga objekt</span><span class="sxs-lookup"><span data-stu-id="73f03-120">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeTrigger
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="73f03-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="73f03-121">-Name</span></span>
<span data-ttu-id="73f03-122">Resurs namn</span><span class="sxs-lookup"><span data-stu-id="73f03-122">Resource Name</span></span>

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

### <span data-ttu-id="73f03-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="73f03-123">-PassThru</span></span>
<span data-ttu-id="73f03-124">Returnerar sant om det lyckas</span><span class="sxs-lookup"><span data-stu-id="73f03-124">returns true if successful</span></span>

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

### <span data-ttu-id="73f03-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="73f03-125">-ResourceGroupName</span></span>
<span data-ttu-id="73f03-126">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="73f03-126">Resource Group Name</span></span>

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

### <span data-ttu-id="73f03-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="73f03-127">-ResourceId</span></span>
<span data-ttu-id="73f03-128">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="73f03-128">Azure ResourceId</span></span>

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

### <span data-ttu-id="73f03-129">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="73f03-129">-Confirm</span></span>
<span data-ttu-id="73f03-130">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="73f03-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="73f03-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="73f03-131">-WhatIf</span></span>
<span data-ttu-id="73f03-132">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="73f03-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="73f03-133">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="73f03-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="73f03-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73f03-134">CommonParameters</span></span>
<span data-ttu-id="73f03-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="73f03-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73f03-136">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="73f03-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73f03-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="73f03-137">INPUTS</span></span>

### <span data-ttu-id="73f03-138">System. String</span><span class="sxs-lookup"><span data-stu-id="73f03-138">System.String</span></span>

### <span data-ttu-id="73f03-139">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeTrigger</span><span class="sxs-lookup"><span data-stu-id="73f03-139">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeTrigger</span></span>

## <span data-ttu-id="73f03-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="73f03-140">OUTPUTS</span></span>

### <span data-ttu-id="73f03-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="73f03-141">System.Boolean</span></span>

## <span data-ttu-id="73f03-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="73f03-142">NOTES</span></span>

## <span data-ttu-id="73f03-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="73f03-143">RELATED LINKS</span></span>
