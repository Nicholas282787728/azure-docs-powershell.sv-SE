---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 36399302-3EA5-45A3-A042-536CC7EC2E6D
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azpolicyassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzPolicyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzPolicyAssignment.md
ms.openlocfilehash: 00ec24c13a5c51db7da63cd1d94c01f251a7e289
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94322362"
---
# <span data-ttu-id="a1298-101">Remove-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="a1298-101">Remove-AzPolicyAssignment</span></span>

## <span data-ttu-id="a1298-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a1298-102">SYNOPSIS</span></span>
<span data-ttu-id="a1298-103">Tar bort en princip tilldelning.</span><span class="sxs-lookup"><span data-stu-id="a1298-103">Removes a policy assignment.</span></span>

## <span data-ttu-id="a1298-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a1298-104">SYNTAX</span></span>

### <span data-ttu-id="a1298-105">NameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="a1298-105">NameParameterSet (Default)</span></span>
```
Remove-AzPolicyAssignment -Name <String> [-Scope <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a1298-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a1298-106">IdParameterSet</span></span>
```
Remove-AzPolicyAssignment -Id <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a1298-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a1298-107">InputObjectParameterSet</span></span>
```
Remove-AzPolicyAssignment -InputObject <PsPolicyAssignment> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a1298-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a1298-108">DESCRIPTION</span></span>
<span data-ttu-id="a1298-109">Cmdleten **Remove-AzPolicyAssignment** tar bort den angivna princip tilldelningen.</span><span class="sxs-lookup"><span data-stu-id="a1298-109">The **Remove-AzPolicyAssignment** cmdlet removes the specified policy assignment.</span></span>

## <span data-ttu-id="a1298-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a1298-110">EXAMPLES</span></span>

### <span data-ttu-id="a1298-111">Exempel 1: ta bort princip tilldelning via namn och omfattning</span><span class="sxs-lookup"><span data-stu-id="a1298-111">Example 1: Remove policy assignment by name and scope</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> Remove-AzPolicyAssignment -Name 'PolicyAssignment07' -Scope $ResourceGroup.ResourceId -Confirm
```

<span data-ttu-id="a1298-112">Det första kommandot får en resurs grupp som heter ResourceGroup11 med hjälp av Get-AzResourceGroup cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a1298-112">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet.</span></span>
<span data-ttu-id="a1298-113">Kommandot lagrar objektet i $ResourceGroup variabel.</span><span class="sxs-lookup"><span data-stu-id="a1298-113">The command stores that object in the $ResourceGroup variable.</span></span>
<span data-ttu-id="a1298-114">Det andra kommandot tar bort princip tilldelningen med namnet PolicyAssignment07 som tilldelats i en resurs grupp nivå.</span><span class="sxs-lookup"><span data-stu-id="a1298-114">The second command removes the policy assignment named PolicyAssignment07 that was assigned at a resource group level.</span></span>
<span data-ttu-id="a1298-115">Egenskapen **ResourceID** för $ResourceGroup identifierar resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="a1298-115">The **ResourceId** property of $ResourceGroup identifies the resource group.</span></span>

### <span data-ttu-id="a1298-116">Exempel 2: ta bort princip tilldelning via ID</span><span class="sxs-lookup"><span data-stu-id="a1298-116">Example 2: Remove policy assignment by ID</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11' 
PS C:\> $PolicyAssignment = Get-AzPolicyAssignment -Name 'PolicyAssignment07' -Scope $ResourceGroup.ResourceId
PS C:\> Remove-AzPolicyAssignment -Id $PolicyAssignment.ResourceId -Confirm
```

<span data-ttu-id="a1298-117">Det första kommandot får en resurs grupp som heter ResourceGroup11 och lagrar sedan objektet i variabeln $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="a1298-117">The first command gets a resource group named ResourceGroup11, and then stores that object in the $ResourceGroup variable.</span></span>
<span data-ttu-id="a1298-118">Det andra kommandot får policy tilldelningen på en resurs grupp nivå och lagrar den sedan i $PolicyAssignment variabel.</span><span class="sxs-lookup"><span data-stu-id="a1298-118">The second command gets the policy assignment at a resource group level, and then stores it in the $PolicyAssignment variable.</span></span>
<span data-ttu-id="a1298-119">Egenskapen **ResourceID** för $ResourceGroup identifierar resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="a1298-119">The **ResourceId** property of $ResourceGroup identifies the resource group.</span></span>
<span data-ttu-id="a1298-120">Kommandot tar bort princip tilldelningen som egenskapen **ResourceID** för $PolicyAssignment identifieras.</span><span class="sxs-lookup"><span data-stu-id="a1298-120">The final command removes the policy assignment that the **ResourceId** property of $PolicyAssignment identifies.</span></span>

## <span data-ttu-id="a1298-121">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a1298-121">PARAMETERS</span></span>

### <span data-ttu-id="a1298-122">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="a1298-122">-ApiVersion</span></span>
<span data-ttu-id="a1298-123">Anger vilken version av API för Resource provider som ska användas.</span><span class="sxs-lookup"><span data-stu-id="a1298-123">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="a1298-124">Om du inte anger en version använder denna cmdlet den senaste tillgängliga versionen.</span><span class="sxs-lookup"><span data-stu-id="a1298-124">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1298-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1298-125">-DefaultProfile</span></span>
<span data-ttu-id="a1298-126">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="a1298-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a1298-127">-ID</span><span class="sxs-lookup"><span data-stu-id="a1298-127">-Id</span></span>
<span data-ttu-id="a1298-128">Anger det fullständiga resurs-ID för princip tilldelningen som denna cmdlet tar bort.</span><span class="sxs-lookup"><span data-stu-id="a1298-128">Specifies the fully qualified resource ID for the policy assignment that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: IdParameterSet
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a1298-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a1298-129">-InputObject</span></span>
<span data-ttu-id="a1298-130">Det princip tilldelnings objekt som du vill ta bort utdata från en annan cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a1298-130">The policy assignment object to remove that was output from another cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.Implementation.Policy.PsPolicyAssignment
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a1298-131">-Namn</span><span class="sxs-lookup"><span data-stu-id="a1298-131">-Name</span></span>
<span data-ttu-id="a1298-132">Anger namnet på den princip tilldelning som denna cmdlet tar bort.</span><span class="sxs-lookup"><span data-stu-id="a1298-132">Specifies the name of the policy assignment that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a1298-133">-För</span><span class="sxs-lookup"><span data-stu-id="a1298-133">-Pre</span></span>
<span data-ttu-id="a1298-134">Visar att denna cmdlet betraktar för hands version API-versioner när den automatiskt avgör vilken version som ska användas.</span><span class="sxs-lookup"><span data-stu-id="a1298-134">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="a1298-135">-Omfattning</span><span class="sxs-lookup"><span data-stu-id="a1298-135">-Scope</span></span>
<span data-ttu-id="a1298-136">Anger omfattningen som principen tillämpas på.</span><span class="sxs-lookup"><span data-stu-id="a1298-136">Specifies the scope at which the policy is applied.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a1298-137">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="a1298-137">-Confirm</span></span>
<span data-ttu-id="a1298-138">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="a1298-138">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1298-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a1298-139">-WhatIf</span></span>
<span data-ttu-id="a1298-140">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="a1298-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a1298-141">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="a1298-141">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1298-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1298-142">CommonParameters</span></span>
<span data-ttu-id="a1298-143">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a1298-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1298-144">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a1298-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1298-145">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a1298-145">INPUTS</span></span>

### <span data-ttu-id="a1298-146">System. String</span><span class="sxs-lookup"><span data-stu-id="a1298-146">System.String</span></span>

## <span data-ttu-id="a1298-147">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a1298-147">OUTPUTS</span></span>

### <span data-ttu-id="a1298-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a1298-148">System.Boolean</span></span>

## <span data-ttu-id="a1298-149">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a1298-149">NOTES</span></span>

## <span data-ttu-id="a1298-150">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a1298-150">RELATED LINKS</span></span>

[<span data-ttu-id="a1298-151">Get-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="a1298-151">Get-AzPolicyAssignment</span></span>](./Get-AzPolicyAssignment.md)

[<span data-ttu-id="a1298-152">New-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="a1298-152">New-AzPolicyAssignment</span></span>](./New-AzPolicyAssignment.md)

[<span data-ttu-id="a1298-153">Set-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="a1298-153">Set-AzPolicyAssignment</span></span>](./Set-AzPolicyAssignment.md)

