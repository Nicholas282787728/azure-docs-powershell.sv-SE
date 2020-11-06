---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 36399302-3EA5-45A3-A042-536CC7EC2E6D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermpolicyassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmPolicyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmPolicyAssignment.md
ms.openlocfilehash: d78cf9d28c453626c26656b9f9280f5c52695434
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576418"
---
# <span data-ttu-id="4ee6e-101">Remove-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="4ee6e-101">Remove-AzureRmPolicyAssignment</span></span>

## <span data-ttu-id="4ee6e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4ee6e-102">SYNOPSIS</span></span>
<span data-ttu-id="4ee6e-103">Tar bort en princip tilldelning.</span><span class="sxs-lookup"><span data-stu-id="4ee6e-103">Removes a policy assignment.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4ee6e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4ee6e-104">SYNTAX</span></span>

### <span data-ttu-id="4ee6e-105">RemoveByPolicyAssignmentName (standard)</span><span class="sxs-lookup"><span data-stu-id="4ee6e-105">RemoveByPolicyAssignmentName (Default)</span></span>
```
Remove-AzureRmPolicyAssignment -Name <String> -Scope <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4ee6e-106">RemoveByPolicyAssignmentId</span><span class="sxs-lookup"><span data-stu-id="4ee6e-106">RemoveByPolicyAssignmentId</span></span>
```
Remove-AzureRmPolicyAssignment -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4ee6e-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4ee6e-107">DESCRIPTION</span></span>
<span data-ttu-id="4ee6e-108">Cmdleten **Remove-AzureRmPolicyAssignment** tar bort den angivna princip tilldelningen.</span><span class="sxs-lookup"><span data-stu-id="4ee6e-108">The **Remove-AzureRmPolicyAssignment** cmdlet removes the specified policy assignment.</span></span>

## <span data-ttu-id="4ee6e-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4ee6e-109">EXAMPLES</span></span>

### <span data-ttu-id="4ee6e-110">Exempel 1: ta bort princip tilldelning via namn och omfattning</span><span class="sxs-lookup"><span data-stu-id="4ee6e-110">Example 1: Remove policy assignment by name and scope</span></span>
```
PS C:\>$ResourceGroup = Get-AzureRmResourceGroup -Name "ResourceGroup11"
PS C:\> Remove-AzureRmPolicyAssignment -Name "PolicyAssignment07" -Scope $ResourceGroup.ResourceId -Force
```

<span data-ttu-id="4ee6e-111">Det första kommandot får en resurs grupp som heter ResourceGroup11 med hjälp av Get-AzureRMResourceGroup cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4ee6e-111">The first command gets a resource group named ResourceGroup11 by using the Get-AzureRMResourceGroup cmdlet.</span></span>
<span data-ttu-id="4ee6e-112">Kommandot lagrar objektet i $ResourceGroup variabel.</span><span class="sxs-lookup"><span data-stu-id="4ee6e-112">The command stores that object in the $ResourceGroup variable.</span></span>

<span data-ttu-id="4ee6e-113">Det andra kommandot tar bort princip tilldelningen med namnet PolicyAssignment07 som tilldelats i en resurs grupp nivå.</span><span class="sxs-lookup"><span data-stu-id="4ee6e-113">The second command removes the policy assignment named PolicyAssignment07 that was assigned at a resource group level.</span></span>
<span data-ttu-id="4ee6e-114">Egenskapen **ResourceID** för $ResourceGroup identifierar resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="4ee6e-114">The **ResourceId** property of $ResourceGroup identifies the resource group.</span></span>

### <span data-ttu-id="4ee6e-115">Exempel 2: ta bort princip tilldelning via ID</span><span class="sxs-lookup"><span data-stu-id="4ee6e-115">Example 2: Remove policy assignment by ID</span></span>
```
PS C:\>$ResourceGroup = Get-AzureRmResourceGroup -Name "ResourceGroup11" 
PS C:\> $PolicyAssignment = Get-AzureRmPolicyAssignment -Name "PolicyAssignment07" -Scope $ResourceGroup.ResourceId
PS C:\> Remove-AzureRmPolicyAssignment -Id $PolicyAssignment.ResourceId -Force
```

<span data-ttu-id="4ee6e-116">Det första kommandot får en resurs grupp som heter ResourceGroup11 och lagrar sedan objektet i variabeln $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="4ee6e-116">The first command gets a resource group named ResourceGroup11, and then stores that object in the $ResourceGroup variable.</span></span>

<span data-ttu-id="4ee6e-117">Det andra kommandot får policy tilldelningen på en resurs grupp nivå och lagrar den sedan i $PolicyAssignment variabel.</span><span class="sxs-lookup"><span data-stu-id="4ee6e-117">The second command gets the policy assignment at a resource group level, and then stores it in the $PolicyAssignment variable.</span></span>
<span data-ttu-id="4ee6e-118">Egenskapen **ResourceID** för $ResourceGroup identifierar resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="4ee6e-118">The **ResourceId** property of $ResourceGroup identifies the resource group.</span></span>

<span data-ttu-id="4ee6e-119">Kommandot tar bort princip tilldelningen som egenskapen **ResourceID** för $PolicyAssignment identifieras.</span><span class="sxs-lookup"><span data-stu-id="4ee6e-119">The final command removes the policy assignment that the **ResourceId** property of $PolicyAssignment identifies.</span></span>

## <span data-ttu-id="4ee6e-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4ee6e-120">PARAMETERS</span></span>

### <span data-ttu-id="4ee6e-121">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="4ee6e-121">-ApiVersion</span></span>
<span data-ttu-id="4ee6e-122">Anger vilken version av API för Resource provider som ska användas.</span><span class="sxs-lookup"><span data-stu-id="4ee6e-122">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="4ee6e-123">Om du inte anger en version använder denna cmdlet den senaste tillgängliga versionen.</span><span class="sxs-lookup"><span data-stu-id="4ee6e-123">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ee6e-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ee6e-124">-DefaultProfile</span></span>
<span data-ttu-id="4ee6e-125">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="4ee6e-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ee6e-126">-ID</span><span class="sxs-lookup"><span data-stu-id="4ee6e-126">-Id</span></span>
<span data-ttu-id="4ee6e-127">Anger det fullständiga resurs-ID för princip tilldelningen som denna cmdlet tar bort.</span><span class="sxs-lookup"><span data-stu-id="4ee6e-127">Specifies the fully qualified resource ID for the policy assignment that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByPolicyAssignmentId
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ee6e-128">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="4ee6e-128">-InformationAction</span></span>
<span data-ttu-id="4ee6e-129">Anger hur den här cmdleten svarar på en informations händelse.</span><span class="sxs-lookup"><span data-stu-id="4ee6e-129">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="4ee6e-130">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="4ee6e-130">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="4ee6e-131">Vidare</span><span class="sxs-lookup"><span data-stu-id="4ee6e-131">Continue</span></span>
- <span data-ttu-id="4ee6e-132">Över</span><span class="sxs-lookup"><span data-stu-id="4ee6e-132">Ignore</span></span>
- <span data-ttu-id="4ee6e-133">Inquire</span><span class="sxs-lookup"><span data-stu-id="4ee6e-133">Inquire</span></span>
- <span data-ttu-id="4ee6e-134">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="4ee6e-134">SilentlyContinue</span></span>
- <span data-ttu-id="4ee6e-135">Stanna</span><span class="sxs-lookup"><span data-stu-id="4ee6e-135">Stop</span></span>
- <span data-ttu-id="4ee6e-136">Avbryt</span><span class="sxs-lookup"><span data-stu-id="4ee6e-136">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ee6e-137">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="4ee6e-137">-InformationVariable</span></span>
<span data-ttu-id="4ee6e-138">Anger en informations variabel.</span><span class="sxs-lookup"><span data-stu-id="4ee6e-138">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ee6e-139">-Namn</span><span class="sxs-lookup"><span data-stu-id="4ee6e-139">-Name</span></span>
<span data-ttu-id="4ee6e-140">Anger namnet på den princip tilldelning som denna cmdlet tar bort.</span><span class="sxs-lookup"><span data-stu-id="4ee6e-140">Specifies the name of the policy assignment that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByPolicyAssignmentName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ee6e-141">-För</span><span class="sxs-lookup"><span data-stu-id="4ee6e-141">-Pre</span></span>
<span data-ttu-id="4ee6e-142">Visar att denna cmdlet betraktar för hands version API-versioner när den automatiskt avgör vilken version som ska användas.</span><span class="sxs-lookup"><span data-stu-id="4ee6e-142">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ee6e-143">-Omfattning</span><span class="sxs-lookup"><span data-stu-id="4ee6e-143">-Scope</span></span>
<span data-ttu-id="4ee6e-144">Anger omfattningen som principen tillämpas på.</span><span class="sxs-lookup"><span data-stu-id="4ee6e-144">Specifies the scope at which the policy is applied.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByPolicyAssignmentName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ee6e-145">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="4ee6e-145">-Confirm</span></span>
<span data-ttu-id="4ee6e-146">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="4ee6e-146">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ee6e-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4ee6e-147">-WhatIf</span></span>
<span data-ttu-id="4ee6e-148">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="4ee6e-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4ee6e-149">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="4ee6e-149">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ee6e-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ee6e-150">CommonParameters</span></span>
<span data-ttu-id="4ee6e-151">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4ee6e-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ee6e-152">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4ee6e-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ee6e-153">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4ee6e-153">INPUTS</span></span>

### <span data-ttu-id="4ee6e-154">Ingen</span><span class="sxs-lookup"><span data-stu-id="4ee6e-154">None</span></span>
<span data-ttu-id="4ee6e-155">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="4ee6e-155">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="4ee6e-156">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4ee6e-156">OUTPUTS</span></span>

### <span data-ttu-id="4ee6e-157">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="4ee6e-157">System.Boolean</span></span>

## <span data-ttu-id="4ee6e-158">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4ee6e-158">NOTES</span></span>

## <span data-ttu-id="4ee6e-159">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4ee6e-159">RELATED LINKS</span></span>

[<span data-ttu-id="4ee6e-160">Get-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="4ee6e-160">Get-AzureRmPolicyAssignment</span></span>](./Get-AzureRmPolicyAssignment.md)

[<span data-ttu-id="4ee6e-161">New-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="4ee6e-161">New-AzureRmPolicyAssignment</span></span>](./New-AzureRmPolicyAssignment.md)

[<span data-ttu-id="4ee6e-162">Set-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="4ee6e-162">Set-AzureRmPolicyAssignment</span></span>](./Set-AzureRmPolicyAssignment.md)


