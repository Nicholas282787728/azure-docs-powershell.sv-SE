---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/remove-azstackedgetrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeTrigger.md
ms.openlocfilehash: ad2761e4e0fba3ef7dbb7a28b15477a649891042
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94269589"
---
# <span data-ttu-id="5749e-101">Remove-AzStackEdgeTrigger</span><span class="sxs-lookup"><span data-stu-id="5749e-101">Remove-AzStackEdgeTrigger</span></span>

## <span data-ttu-id="5749e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5749e-102">SYNOPSIS</span></span>
<span data-ttu-id="5749e-103">Tar bort en befintlig utlösare på enheten.</span><span class="sxs-lookup"><span data-stu-id="5749e-103">Removes an existing trigger on the device.</span></span>

## <span data-ttu-id="5749e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5749e-104">SYNTAX</span></span>

### <span data-ttu-id="5749e-105">DeleteByNameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="5749e-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzStackEdgeTrigger [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5749e-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5749e-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzStackEdgeTrigger [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5749e-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5749e-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzStackEdgeTrigger [-InputObject] <PSStackEdgeTrigger> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5749e-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5749e-108">DESCRIPTION</span></span>
<span data-ttu-id="5749e-109">Cmdleten **Remove-AzStackEdgeTrigger** tar bort en befintlig utlösare på stack Edge-enheten.</span><span class="sxs-lookup"><span data-stu-id="5749e-109">The **Remove-AzStackEdgeTrigger** cmdlet removes an existing trigger on the Stack Edge device.</span></span>

## <span data-ttu-id="5749e-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5749e-110">EXAMPLES</span></span>

### <span data-ttu-id="5749e-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="5749e-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzStackEdgeTrigger -ResourceGroupName resourceGroupName -DeviceName deviceName -Name triggerName
```

## <span data-ttu-id="5749e-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5749e-112">PARAMETERS</span></span>

### <span data-ttu-id="5749e-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5749e-113">-AsJob</span></span>
<span data-ttu-id="5749e-114">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="5749e-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5749e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5749e-115">-DefaultProfile</span></span>
<span data-ttu-id="5749e-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="5749e-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5749e-117">-Enhets namn</span><span class="sxs-lookup"><span data-stu-id="5749e-117">-DeviceName</span></span>
<span data-ttu-id="5749e-118">Enhetens namn</span><span class="sxs-lookup"><span data-stu-id="5749e-118">Device Name</span></span>

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

### <span data-ttu-id="5749e-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5749e-119">-InputObject</span></span>
<span data-ttu-id="5749e-120">Infoga objekt</span><span class="sxs-lookup"><span data-stu-id="5749e-120">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeTrigger
Parameter Sets: DeleteByInputObjectParameterSet
Aliases: Trigger

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5749e-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="5749e-121">-Name</span></span>
<span data-ttu-id="5749e-122">Resurs namn</span><span class="sxs-lookup"><span data-stu-id="5749e-122">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases: TriggerName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5749e-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5749e-123">-PassThru</span></span>
<span data-ttu-id="5749e-124">Returnerar sant om det lyckas</span><span class="sxs-lookup"><span data-stu-id="5749e-124">returns true if successful</span></span>

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

### <span data-ttu-id="5749e-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5749e-125">-ResourceGroupName</span></span>
<span data-ttu-id="5749e-126">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="5749e-126">Resource Group Name</span></span>

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

### <span data-ttu-id="5749e-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5749e-127">-ResourceId</span></span>
<span data-ttu-id="5749e-128">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="5749e-128">Azure ResourceId</span></span>

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

### <span data-ttu-id="5749e-129">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="5749e-129">-Confirm</span></span>
<span data-ttu-id="5749e-130">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="5749e-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5749e-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5749e-131">-WhatIf</span></span>
<span data-ttu-id="5749e-132">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="5749e-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5749e-133">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="5749e-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5749e-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5749e-134">CommonParameters</span></span>
<span data-ttu-id="5749e-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5749e-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5749e-136">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5749e-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5749e-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5749e-137">INPUTS</span></span>

### <span data-ttu-id="5749e-138">System. String</span><span class="sxs-lookup"><span data-stu-id="5749e-138">System.String</span></span>

### <span data-ttu-id="5749e-139">Microsoft. Azure. PowerShell. cmdletar. StackEdge. Models. PSStackEdgeTrigger</span><span class="sxs-lookup"><span data-stu-id="5749e-139">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeTrigger</span></span>

## <span data-ttu-id="5749e-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5749e-140">OUTPUTS</span></span>

### <span data-ttu-id="5749e-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="5749e-141">System.Boolean</span></span>

## <span data-ttu-id="5749e-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5749e-142">NOTES</span></span>

## <span data-ttu-id="5749e-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5749e-143">RELATED LINKS</span></span>
