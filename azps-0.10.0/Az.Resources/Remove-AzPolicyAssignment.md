---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 36399302-3EA5-45A3-A042-536CC7EC2E6D
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-Azpolicyassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Remove-AzPolicyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Remove-AzPolicyAssignment.md
ms.openlocfilehash: 8fbf6c16dce1f8d96dcc9546c801e389493e7bcd
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93923834"
---
# <span data-ttu-id="3f4f7-101">Remove-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="3f4f7-101">Remove-AzPolicyAssignment</span></span>

## <span data-ttu-id="3f4f7-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3f4f7-102">SYNOPSIS</span></span>
<span data-ttu-id="3f4f7-103">Tar bort en princip tilldelning.</span><span class="sxs-lookup"><span data-stu-id="3f4f7-103">Removes a policy assignment.</span></span>

## <span data-ttu-id="3f4f7-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3f4f7-104">SYNTAX</span></span>

### <span data-ttu-id="3f4f7-105">NameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="3f4f7-105">NameParameterSet (Default)</span></span>
```
Remove-AzPolicyAssignment -Name <String> -Scope <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3f4f7-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3f4f7-106">IdParameterSet</span></span>
```
Remove-AzPolicyAssignment -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3f4f7-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3f4f7-107">DESCRIPTION</span></span>
<span data-ttu-id="3f4f7-108">Cmdleten **Remove-AzPolicyAssignment** tar bort den angivna princip tilldelningen.</span><span class="sxs-lookup"><span data-stu-id="3f4f7-108">The **Remove-AzPolicyAssignment** cmdlet removes the specified policy assignment.</span></span>

## <span data-ttu-id="3f4f7-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3f4f7-109">EXAMPLES</span></span>

### <span data-ttu-id="3f4f7-110">Exempel 1: ta bort princip tilldelning via namn och omfattning</span><span class="sxs-lookup"><span data-stu-id="3f4f7-110">Example 1: Remove policy assignment by name and scope</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> Remove-AzPolicyAssignment -Name 'PolicyAssignment07' -Scope $ResourceGroup.ResourceId -Force
```

<span data-ttu-id="3f4f7-111">Det första kommandot får en resurs grupp som heter ResourceGroup11 med hjälp av Get-AzResourceGroup cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3f4f7-111">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet.</span></span>
<span data-ttu-id="3f4f7-112">Kommandot lagrar objektet i $ResourceGroup variabel.</span><span class="sxs-lookup"><span data-stu-id="3f4f7-112">The command stores that object in the $ResourceGroup variable.</span></span>
<span data-ttu-id="3f4f7-113">Det andra kommandot tar bort princip tilldelningen med namnet PolicyAssignment07 som tilldelats i en resurs grupp nivå.</span><span class="sxs-lookup"><span data-stu-id="3f4f7-113">The second command removes the policy assignment named PolicyAssignment07 that was assigned at a resource group level.</span></span>
<span data-ttu-id="3f4f7-114">Egenskapen **ResourceID** för $ResourceGroup identifierar resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="3f4f7-114">The **ResourceId** property of $ResourceGroup identifies the resource group.</span></span>

### <span data-ttu-id="3f4f7-115">Exempel 2: ta bort princip tilldelning via ID</span><span class="sxs-lookup"><span data-stu-id="3f4f7-115">Example 2: Remove policy assignment by ID</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11' 
PS C:\> $PolicyAssignment = Get-AzPolicyAssignment -Name 'PolicyAssignment07' -Scope $ResourceGroup.ResourceId
PS C:\> Remove-AzPolicyAssignment -Id $PolicyAssignment.ResourceId -Force
```

<span data-ttu-id="3f4f7-116">Det första kommandot får en resurs grupp som heter ResourceGroup11 och lagrar sedan objektet i variabeln $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="3f4f7-116">The first command gets a resource group named ResourceGroup11, and then stores that object in the $ResourceGroup variable.</span></span>
<span data-ttu-id="3f4f7-117">Det andra kommandot får policy tilldelningen på en resurs grupp nivå och lagrar den sedan i $PolicyAssignment variabel.</span><span class="sxs-lookup"><span data-stu-id="3f4f7-117">The second command gets the policy assignment at a resource group level, and then stores it in the $PolicyAssignment variable.</span></span>
<span data-ttu-id="3f4f7-118">Egenskapen **ResourceID** för $ResourceGroup identifierar resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="3f4f7-118">The **ResourceId** property of $ResourceGroup identifies the resource group.</span></span>
<span data-ttu-id="3f4f7-119">Kommandot tar bort princip tilldelningen som egenskapen **ResourceID** för $PolicyAssignment identifieras.</span><span class="sxs-lookup"><span data-stu-id="3f4f7-119">The final command removes the policy assignment that the **ResourceId** property of $PolicyAssignment identifies.</span></span>

## <span data-ttu-id="3f4f7-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3f4f7-120">PARAMETERS</span></span>

### <span data-ttu-id="3f4f7-121">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="3f4f7-121">-ApiVersion</span></span>
<span data-ttu-id="3f4f7-122">Anger vilken version av API för Resource provider som ska användas.</span><span class="sxs-lookup"><span data-stu-id="3f4f7-122">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="3f4f7-123">Om du inte anger en version använder denna cmdlet den senaste tillgängliga versionen.</span><span class="sxs-lookup"><span data-stu-id="3f4f7-123">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="3f4f7-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f4f7-124">-DefaultProfile</span></span>
<span data-ttu-id="3f4f7-125">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="3f4f7-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f4f7-126">-ID</span><span class="sxs-lookup"><span data-stu-id="3f4f7-126">-Id</span></span>
<span data-ttu-id="3f4f7-127">Anger det fullständiga resurs-ID för princip tilldelningen som denna cmdlet tar bort.</span><span class="sxs-lookup"><span data-stu-id="3f4f7-127">Specifies the fully qualified resource ID for the policy assignment that this cmdlet removes.</span></span>

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

### <span data-ttu-id="3f4f7-128">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="3f4f7-128">-InformationAction</span></span>
<span data-ttu-id="3f4f7-129">Anger hur den här cmdleten svarar på en informations händelse.</span><span class="sxs-lookup"><span data-stu-id="3f4f7-129">Specifies how this cmdlet responds to an information event.</span></span>
<span data-ttu-id="3f4f7-130">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="3f4f7-130">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="3f4f7-131">Vidare</span><span class="sxs-lookup"><span data-stu-id="3f4f7-131">Continue</span></span>
- <span data-ttu-id="3f4f7-132">Över</span><span class="sxs-lookup"><span data-stu-id="3f4f7-132">Ignore</span></span>
- <span data-ttu-id="3f4f7-133">Inquire</span><span class="sxs-lookup"><span data-stu-id="3f4f7-133">Inquire</span></span>
- <span data-ttu-id="3f4f7-134">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="3f4f7-134">SilentlyContinue</span></span>
- <span data-ttu-id="3f4f7-135">Stanna</span><span class="sxs-lookup"><span data-stu-id="3f4f7-135">Stop</span></span>
- <span data-ttu-id="3f4f7-136">Avbryt</span><span class="sxs-lookup"><span data-stu-id="3f4f7-136">Suspend</span></span>

```yaml
Type: System.Management.Automation.ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f4f7-137">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="3f4f7-137">-InformationVariable</span></span>
<span data-ttu-id="3f4f7-138">Anger en informations variabel.</span><span class="sxs-lookup"><span data-stu-id="3f4f7-138">Specifies an information variable.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f4f7-139">-Namn</span><span class="sxs-lookup"><span data-stu-id="3f4f7-139">-Name</span></span>
<span data-ttu-id="3f4f7-140">Anger namnet på den princip tilldelning som denna cmdlet tar bort.</span><span class="sxs-lookup"><span data-stu-id="3f4f7-140">Specifies the name of the policy assignment that this cmdlet removes.</span></span>

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

### <span data-ttu-id="3f4f7-141">-För</span><span class="sxs-lookup"><span data-stu-id="3f4f7-141">-Pre</span></span>
<span data-ttu-id="3f4f7-142">Visar att denna cmdlet betraktar för hands version API-versioner när den automatiskt avgör vilken version som ska användas.</span><span class="sxs-lookup"><span data-stu-id="3f4f7-142">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="3f4f7-143">-Omfattning</span><span class="sxs-lookup"><span data-stu-id="3f4f7-143">-Scope</span></span>
<span data-ttu-id="3f4f7-144">Anger omfattningen som principen tillämpas på.</span><span class="sxs-lookup"><span data-stu-id="3f4f7-144">Specifies the scope at which the policy is applied.</span></span>

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

### <span data-ttu-id="3f4f7-145">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="3f4f7-145">-Confirm</span></span>
<span data-ttu-id="3f4f7-146">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="3f4f7-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3f4f7-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3f4f7-147">-WhatIf</span></span>
<span data-ttu-id="3f4f7-148">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="3f4f7-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3f4f7-149">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="3f4f7-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3f4f7-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f4f7-150">CommonParameters</span></span>
<span data-ttu-id="3f4f7-151">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3f4f7-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f4f7-152">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3f4f7-152">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f4f7-153">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3f4f7-153">INPUTS</span></span>

## <span data-ttu-id="3f4f7-154">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3f4f7-154">OUTPUTS</span></span>

## <span data-ttu-id="3f4f7-155">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3f4f7-155">NOTES</span></span>

## <span data-ttu-id="3f4f7-156">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3f4f7-156">RELATED LINKS</span></span>

[<span data-ttu-id="3f4f7-157">Get-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="3f4f7-157">Get-AzPolicyAssignment</span></span>](./Get-AzPolicyAssignment.md)

[<span data-ttu-id="3f4f7-158">New-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="3f4f7-158">New-AzPolicyAssignment</span></span>](./New-AzPolicyAssignment.md)

[<span data-ttu-id="3f4f7-159">Set-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="3f4f7-159">Set-AzPolicyAssignment</span></span>](./Set-AzPolicyAssignment.md)


