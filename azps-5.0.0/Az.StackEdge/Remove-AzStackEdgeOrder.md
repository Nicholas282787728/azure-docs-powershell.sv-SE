---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/remove-azstackedgeorder
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeOrder.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeOrder.md
ms.openlocfilehash: 5effec8ed39f9219bcecba23f6ca3cabaae5cec9
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94269743"
---
# <span data-ttu-id="6803a-101">Remove-AzStackEdgeOrder</span><span class="sxs-lookup"><span data-stu-id="6803a-101">Remove-AzStackEdgeOrder</span></span>

## <span data-ttu-id="6803a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6803a-102">SYNOPSIS</span></span>
<span data-ttu-id="6803a-103">Tar bort en enhets ordning.</span><span class="sxs-lookup"><span data-stu-id="6803a-103">Removes the order for a device.</span></span>

## <span data-ttu-id="6803a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6803a-104">SYNTAX</span></span>

### <span data-ttu-id="6803a-105">DeleteByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="6803a-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzStackEdgeOrder [-ResourceGroupName] <String> [-DeviceName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6803a-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6803a-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzStackEdgeOrder -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-PassThru]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6803a-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6803a-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzStackEdgeOrder -InputObject <PSStackEdgeOrder> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6803a-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6803a-108">DESCRIPTION</span></span>
<span data-ttu-id="6803a-109">Cmdleten **Remove-AzStackEdgeOrder** tar bort en befintlig order för en trave Edge-enhet.</span><span class="sxs-lookup"><span data-stu-id="6803a-109">The **Remove-AzStackEdgeOrder** cmdlet deletes an existing order for a Stack Edge device.</span></span>

## <span data-ttu-id="6803a-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6803a-110">EXAMPLES</span></span>

### <span data-ttu-id="6803a-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="6803a-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzStackEdgeOrder -ResourceGroupName resourceGroupName -DeviceName deviceName
```

## <span data-ttu-id="6803a-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6803a-112">PARAMETERS</span></span>

### <span data-ttu-id="6803a-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6803a-113">-AsJob</span></span>
<span data-ttu-id="6803a-114">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="6803a-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6803a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6803a-115">-DefaultProfile</span></span>
<span data-ttu-id="6803a-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="6803a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6803a-117">-Enhets namn</span><span class="sxs-lookup"><span data-stu-id="6803a-117">-DeviceName</span></span>
<span data-ttu-id="6803a-118">Enhetens namn</span><span class="sxs-lookup"><span data-stu-id="6803a-118">Device Name</span></span>

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

### <span data-ttu-id="6803a-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6803a-119">-InputObject</span></span>
<span data-ttu-id="6803a-120">Infoga objekt</span><span class="sxs-lookup"><span data-stu-id="6803a-120">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeOrder
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6803a-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6803a-121">-PassThru</span></span>
<span data-ttu-id="6803a-122">Returnerar sant om det lyckas</span><span class="sxs-lookup"><span data-stu-id="6803a-122">returns true if successful</span></span>

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

### <span data-ttu-id="6803a-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6803a-123">-ResourceGroupName</span></span>
<span data-ttu-id="6803a-124">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="6803a-124">Resource Group Name</span></span>

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

### <span data-ttu-id="6803a-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6803a-125">-ResourceId</span></span>
<span data-ttu-id="6803a-126">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="6803a-126">Azure ResourceId</span></span>

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

### <span data-ttu-id="6803a-127">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="6803a-127">-Confirm</span></span>
<span data-ttu-id="6803a-128">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="6803a-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6803a-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6803a-129">-WhatIf</span></span>
<span data-ttu-id="6803a-130">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="6803a-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6803a-131">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="6803a-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6803a-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6803a-132">CommonParameters</span></span>
<span data-ttu-id="6803a-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6803a-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6803a-134">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6803a-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6803a-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6803a-135">INPUTS</span></span>

### <span data-ttu-id="6803a-136">System. String</span><span class="sxs-lookup"><span data-stu-id="6803a-136">System.String</span></span>

### <span data-ttu-id="6803a-137">Microsoft. Azure. PowerShell. cmdletar. StackEdge. Models. PSStackEdgeOrder</span><span class="sxs-lookup"><span data-stu-id="6803a-137">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeOrder</span></span>

## <span data-ttu-id="6803a-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6803a-138">OUTPUTS</span></span>

### <span data-ttu-id="6803a-139">Microsoft. Azure. PowerShell. cmdletar. StackEdge. Models. PSStackEdgeOrder</span><span class="sxs-lookup"><span data-stu-id="6803a-139">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeOrder</span></span>

## <span data-ttu-id="6803a-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6803a-140">NOTES</span></span>

## <span data-ttu-id="6803a-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6803a-141">RELATED LINKS</span></span>
