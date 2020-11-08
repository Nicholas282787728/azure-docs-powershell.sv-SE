---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 36399302-3EA5-45A3-A042-536CC7EC2E6D
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azpolicyassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzPolicyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzPolicyAssignment.md
ms.openlocfilehash: 8c7aa559ad6fde29c32f1958a4a0e2a6406ad42d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94089487"
---
# <span data-ttu-id="1e183-101">Remove-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="1e183-101">Remove-AzPolicyAssignment</span></span>

## <span data-ttu-id="1e183-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1e183-102">SYNOPSIS</span></span>
<span data-ttu-id="1e183-103">Tar bort en princip tilldelning.</span><span class="sxs-lookup"><span data-stu-id="1e183-103">Removes a policy assignment.</span></span>

## <span data-ttu-id="1e183-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1e183-104">SYNTAX</span></span>

### <span data-ttu-id="1e183-105">NameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="1e183-105">NameParameterSet (Default)</span></span>
```
Remove-AzPolicyAssignment -Name <String> [-Scope <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1e183-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1e183-106">IdParameterSet</span></span>
```
Remove-AzPolicyAssignment -Id <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1e183-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1e183-107">DESCRIPTION</span></span>
<span data-ttu-id="1e183-108">Cmdleten **Remove-AzPolicyAssignment** tar bort den angivna princip tilldelningen.</span><span class="sxs-lookup"><span data-stu-id="1e183-108">The **Remove-AzPolicyAssignment** cmdlet removes the specified policy assignment.</span></span>

## <span data-ttu-id="1e183-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1e183-109">EXAMPLES</span></span>

### <span data-ttu-id="1e183-110">Exempel 1: ta bort princip tilldelning via namn och omfattning</span><span class="sxs-lookup"><span data-stu-id="1e183-110">Example 1: Remove policy assignment by name and scope</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> Remove-AzPolicyAssignment -Name 'PolicyAssignment07' -Scope $ResourceGroup.ResourceId -Force
```

<span data-ttu-id="1e183-111">Det första kommandot får en resurs grupp som heter ResourceGroup11 med hjälp av Get-AzResourceGroup cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1e183-111">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet.</span></span>
<span data-ttu-id="1e183-112">Kommandot lagrar objektet i $ResourceGroup variabel.</span><span class="sxs-lookup"><span data-stu-id="1e183-112">The command stores that object in the $ResourceGroup variable.</span></span>
<span data-ttu-id="1e183-113">Det andra kommandot tar bort princip tilldelningen med namnet PolicyAssignment07 som tilldelats i en resurs grupp nivå.</span><span class="sxs-lookup"><span data-stu-id="1e183-113">The second command removes the policy assignment named PolicyAssignment07 that was assigned at a resource group level.</span></span>
<span data-ttu-id="1e183-114">Egenskapen **ResourceID** för $ResourceGroup identifierar resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="1e183-114">The **ResourceId** property of $ResourceGroup identifies the resource group.</span></span>

### <span data-ttu-id="1e183-115">Exempel 2: ta bort princip tilldelning via ID</span><span class="sxs-lookup"><span data-stu-id="1e183-115">Example 2: Remove policy assignment by ID</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11' 
PS C:\> $PolicyAssignment = Get-AzPolicyAssignment -Name 'PolicyAssignment07' -Scope $ResourceGroup.ResourceId
PS C:\> Remove-AzPolicyAssignment -Id $PolicyAssignment.ResourceId -Force
```

<span data-ttu-id="1e183-116">Det första kommandot får en resurs grupp som heter ResourceGroup11 och lagrar sedan objektet i variabeln $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="1e183-116">The first command gets a resource group named ResourceGroup11, and then stores that object in the $ResourceGroup variable.</span></span>
<span data-ttu-id="1e183-117">Det andra kommandot får policy tilldelningen på en resurs grupp nivå och lagrar den sedan i $PolicyAssignment variabel.</span><span class="sxs-lookup"><span data-stu-id="1e183-117">The second command gets the policy assignment at a resource group level, and then stores it in the $PolicyAssignment variable.</span></span>
<span data-ttu-id="1e183-118">Egenskapen **ResourceID** för $ResourceGroup identifierar resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="1e183-118">The **ResourceId** property of $ResourceGroup identifies the resource group.</span></span>
<span data-ttu-id="1e183-119">Kommandot tar bort princip tilldelningen som egenskapen **ResourceID** för $PolicyAssignment identifieras.</span><span class="sxs-lookup"><span data-stu-id="1e183-119">The final command removes the policy assignment that the **ResourceId** property of $PolicyAssignment identifies.</span></span>

## <span data-ttu-id="1e183-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1e183-120">PARAMETERS</span></span>

### <span data-ttu-id="1e183-121">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="1e183-121">-ApiVersion</span></span>
<span data-ttu-id="1e183-122">Anger vilken version av API för Resource provider som ska användas.</span><span class="sxs-lookup"><span data-stu-id="1e183-122">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="1e183-123">Om du inte anger en version använder denna cmdlet den senaste tillgängliga versionen.</span><span class="sxs-lookup"><span data-stu-id="1e183-123">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="1e183-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e183-124">-DefaultProfile</span></span>
<span data-ttu-id="1e183-125">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="1e183-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1e183-126">-ID</span><span class="sxs-lookup"><span data-stu-id="1e183-126">-Id</span></span>
<span data-ttu-id="1e183-127">Anger det fullständiga resurs-ID för princip tilldelningen som denna cmdlet tar bort.</span><span class="sxs-lookup"><span data-stu-id="1e183-127">Specifies the fully qualified resource ID for the policy assignment that this cmdlet removes.</span></span>

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

### <span data-ttu-id="1e183-128">-Namn</span><span class="sxs-lookup"><span data-stu-id="1e183-128">-Name</span></span>
<span data-ttu-id="1e183-129">Anger namnet på den princip tilldelning som denna cmdlet tar bort.</span><span class="sxs-lookup"><span data-stu-id="1e183-129">Specifies the name of the policy assignment that this cmdlet removes.</span></span>

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

### <span data-ttu-id="1e183-130">-För</span><span class="sxs-lookup"><span data-stu-id="1e183-130">-Pre</span></span>
<span data-ttu-id="1e183-131">Visar att denna cmdlet betraktar för hands version API-versioner när den automatiskt avgör vilken version som ska användas.</span><span class="sxs-lookup"><span data-stu-id="1e183-131">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="1e183-132">-Omfattning</span><span class="sxs-lookup"><span data-stu-id="1e183-132">-Scope</span></span>
<span data-ttu-id="1e183-133">Anger omfattningen som principen tillämpas på.</span><span class="sxs-lookup"><span data-stu-id="1e183-133">Specifies the scope at which the policy is applied.</span></span>

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

### <span data-ttu-id="1e183-134">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="1e183-134">-Confirm</span></span>
<span data-ttu-id="1e183-135">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="1e183-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1e183-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1e183-136">-WhatIf</span></span>
<span data-ttu-id="1e183-137">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="1e183-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1e183-138">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="1e183-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1e183-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e183-139">CommonParameters</span></span>
<span data-ttu-id="1e183-140">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1e183-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e183-141">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1e183-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e183-142">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1e183-142">INPUTS</span></span>

### <span data-ttu-id="1e183-143">System. String</span><span class="sxs-lookup"><span data-stu-id="1e183-143">System.String</span></span>

## <span data-ttu-id="1e183-144">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1e183-144">OUTPUTS</span></span>

### <span data-ttu-id="1e183-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="1e183-145">System.Boolean</span></span>

## <span data-ttu-id="1e183-146">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1e183-146">NOTES</span></span>

## <span data-ttu-id="1e183-147">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1e183-147">RELATED LINKS</span></span>

[<span data-ttu-id="1e183-148">Get-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="1e183-148">Get-AzPolicyAssignment</span></span>](./Get-AzPolicyAssignment.md)

[<span data-ttu-id="1e183-149">New-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="1e183-149">New-AzPolicyAssignment</span></span>](./New-AzPolicyAssignment.md)

[<span data-ttu-id="1e183-150">Set-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="1e183-150">Set-AzPolicyAssignment</span></span>](./Set-AzPolicyAssignment.md)


