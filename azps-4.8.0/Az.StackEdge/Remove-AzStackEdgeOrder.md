---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/remove-azstackedgeorder
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeOrder.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeOrder.md
ms.openlocfilehash: 5effec8ed39f9219bcecba23f6ca3cabaae5cec9
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94261548"
---
# <span data-ttu-id="9b873-101">Remove-AzStackEdgeOrder</span><span class="sxs-lookup"><span data-stu-id="9b873-101">Remove-AzStackEdgeOrder</span></span>

## <span data-ttu-id="9b873-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9b873-102">SYNOPSIS</span></span>
<span data-ttu-id="9b873-103">Tar bort en enhets ordning.</span><span class="sxs-lookup"><span data-stu-id="9b873-103">Removes the order for a device.</span></span>

## <span data-ttu-id="9b873-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9b873-104">SYNTAX</span></span>

### <span data-ttu-id="9b873-105">DeleteByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="9b873-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzStackEdgeOrder [-ResourceGroupName] <String> [-DeviceName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9b873-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9b873-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzStackEdgeOrder -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-PassThru]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9b873-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9b873-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzStackEdgeOrder -InputObject <PSStackEdgeOrder> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9b873-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9b873-108">DESCRIPTION</span></span>
<span data-ttu-id="9b873-109">Cmdleten **Remove-AzStackEdgeOrder** tar bort en befintlig order för en trave Edge-enhet.</span><span class="sxs-lookup"><span data-stu-id="9b873-109">The **Remove-AzStackEdgeOrder** cmdlet deletes an existing order for a Stack Edge device.</span></span>

## <span data-ttu-id="9b873-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9b873-110">EXAMPLES</span></span>

### <span data-ttu-id="9b873-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="9b873-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzStackEdgeOrder -ResourceGroupName resourceGroupName -DeviceName deviceName
```

## <span data-ttu-id="9b873-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9b873-112">PARAMETERS</span></span>

### <span data-ttu-id="9b873-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9b873-113">-AsJob</span></span>
<span data-ttu-id="9b873-114">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="9b873-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9b873-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b873-115">-DefaultProfile</span></span>
<span data-ttu-id="9b873-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="9b873-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9b873-117">-Enhets namn</span><span class="sxs-lookup"><span data-stu-id="9b873-117">-DeviceName</span></span>
<span data-ttu-id="9b873-118">Enhetens namn</span><span class="sxs-lookup"><span data-stu-id="9b873-118">Device Name</span></span>

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

### <span data-ttu-id="9b873-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9b873-119">-InputObject</span></span>
<span data-ttu-id="9b873-120">Infoga objekt</span><span class="sxs-lookup"><span data-stu-id="9b873-120">Input Object</span></span>

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

### <span data-ttu-id="9b873-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9b873-121">-PassThru</span></span>
<span data-ttu-id="9b873-122">Returnerar sant om det lyckas</span><span class="sxs-lookup"><span data-stu-id="9b873-122">returns true if successful</span></span>

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

### <span data-ttu-id="9b873-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9b873-123">-ResourceGroupName</span></span>
<span data-ttu-id="9b873-124">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="9b873-124">Resource Group Name</span></span>

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

### <span data-ttu-id="9b873-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9b873-125">-ResourceId</span></span>
<span data-ttu-id="9b873-126">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="9b873-126">Azure ResourceId</span></span>

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

### <span data-ttu-id="9b873-127">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="9b873-127">-Confirm</span></span>
<span data-ttu-id="9b873-128">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="9b873-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9b873-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9b873-129">-WhatIf</span></span>
<span data-ttu-id="9b873-130">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="9b873-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9b873-131">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="9b873-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9b873-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b873-132">CommonParameters</span></span>
<span data-ttu-id="9b873-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9b873-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b873-134">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9b873-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b873-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9b873-135">INPUTS</span></span>

### <span data-ttu-id="9b873-136">System. String</span><span class="sxs-lookup"><span data-stu-id="9b873-136">System.String</span></span>

### <span data-ttu-id="9b873-137">Microsoft. Azure. PowerShell. cmdletar. StackEdge. Models. PSStackEdgeOrder</span><span class="sxs-lookup"><span data-stu-id="9b873-137">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeOrder</span></span>

## <span data-ttu-id="9b873-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9b873-138">OUTPUTS</span></span>

### <span data-ttu-id="9b873-139">Microsoft. Azure. PowerShell. cmdletar. StackEdge. Models. PSStackEdgeOrder</span><span class="sxs-lookup"><span data-stu-id="9b873-139">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeOrder</span></span>

## <span data-ttu-id="9b873-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9b873-140">NOTES</span></span>

## <span data-ttu-id="9b873-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9b873-141">RELATED LINKS</span></span>
