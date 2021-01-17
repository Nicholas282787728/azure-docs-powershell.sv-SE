---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Invoke-AzVmPatchAssessment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Invoke-AzVmPatchAssessment.md
ms.openlocfilehash: 5ccaccdc5d447ac9ccdc49cf53230c58a5758e4d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98415832"
---
# <span data-ttu-id="a4f32-101">Invoke-AzVMPatchAssessment</span><span class="sxs-lookup"><span data-stu-id="a4f32-101">Invoke-AzVMPatchAssessment</span></span>

## <span data-ttu-id="a4f32-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a4f32-102">SYNOPSIS</span></span>
<span data-ttu-id="a4f32-103">Bedöm uppdaterings status för en virtuell dator.</span><span class="sxs-lookup"><span data-stu-id="a4f32-103">Assess patch state of a virtual machine.</span></span>

## <span data-ttu-id="a4f32-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a4f32-104">SYNTAX</span></span>

### <span data-ttu-id="a4f32-105">DefaultParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="a4f32-105">DefaultParameterSet (Default)</span></span>
```
Invoke-AzVMPatchAssessment [-ResourceGroupName] <String> [-VMName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a4f32-106">ResourceIDParameterSet</span><span class="sxs-lookup"><span data-stu-id="a4f32-106">ResourceIDParameterSet</span></span>
```
Invoke-AzVMPatchAssessment [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a4f32-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a4f32-107">InputObjectParameterSet</span></span>
```
Invoke-AzVMPatchAssessment [-VM] <PSVirtualMachine> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a4f32-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a4f32-108">DESCRIPTION</span></span>
<span data-ttu-id="a4f32-109">Utvärderar korrigerings status för en virtuell dator och rapporterar alla upptäckta korrigeringsfiler som är tillgängliga för installation.</span><span class="sxs-lookup"><span data-stu-id="a4f32-109">Assesses the patch status of a VM and reports all detected patches that are available for installation.</span></span>

## <span data-ttu-id="a4f32-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a4f32-110">EXAMPLES</span></span>

### <span data-ttu-id="a4f32-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="a4f32-111">Example 1</span></span>
```
PS C:\> Invoke-AzVmPatchAssessment -ResourceGroupName "myRG" -VMName "myVM"
```

## <span data-ttu-id="a4f32-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a4f32-112">PARAMETERS</span></span>

### <span data-ttu-id="a4f32-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a4f32-113">-AsJob</span></span>
<span data-ttu-id="a4f32-114">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="a4f32-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a4f32-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4f32-115">-DefaultProfile</span></span>
<span data-ttu-id="a4f32-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a4f32-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a4f32-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a4f32-117">-ResourceGroupName</span></span>
<span data-ttu-id="a4f32-118">Anger namnet på en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="a4f32-118">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a4f32-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a4f32-119">-ResourceId</span></span>
<span data-ttu-id="a4f32-120">Resurs-ID för din virtuella dator.</span><span class="sxs-lookup"><span data-stu-id="a4f32-120">Resource ID for your virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIDParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a4f32-121">-VM</span><span class="sxs-lookup"><span data-stu-id="a4f32-121">-VM</span></span>
<span data-ttu-id="a4f32-122">Objekt för virtuell dator i PowerShell</span><span class="sxs-lookup"><span data-stu-id="a4f32-122">PowerShell Virtual Machine Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: InputObjectParameterSet
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a4f32-123">-VMName</span><span class="sxs-lookup"><span data-stu-id="a4f32-123">-VMName</span></span>
<span data-ttu-id="a4f32-124">Namn på virtuell dator</span><span class="sxs-lookup"><span data-stu-id="a4f32-124">Virtual Machine name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a4f32-125">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="a4f32-125">-Confirm</span></span>
<span data-ttu-id="a4f32-126">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="a4f32-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a4f32-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a4f32-127">-WhatIf</span></span>
<span data-ttu-id="a4f32-128">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="a4f32-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a4f32-129">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="a4f32-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a4f32-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4f32-130">CommonParameters</span></span>
<span data-ttu-id="a4f32-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a4f32-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4f32-132">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a4f32-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4f32-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a4f32-133">INPUTS</span></span>

### <span data-ttu-id="a4f32-134">System. String</span><span class="sxs-lookup"><span data-stu-id="a4f32-134">System.String</span></span>

## <span data-ttu-id="a4f32-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a4f32-135">OUTPUTS</span></span>

### <span data-ttu-id="a4f32-136">Microsoft. Azure. commands. Compute. Automation. Models. PSVirtualMachinePatchAssessmentResult</span><span class="sxs-lookup"><span data-stu-id="a4f32-136">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachinePatchAssessmentResult</span></span>

## <span data-ttu-id="a4f32-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a4f32-137">NOTES</span></span>

## <span data-ttu-id="a4f32-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a4f32-138">RELATED LINKS</span></span>
