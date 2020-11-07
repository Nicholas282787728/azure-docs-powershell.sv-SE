---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 36399302-3EA5-45A3-A042-536CC7EC2E6D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermpolicyassignment
schema: 2.0.0
ms.openlocfilehash: 6972d4df51222804843aa965577f7044ed4bf987
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93931137"
---
# <span data-ttu-id="90e2a-101">Remove-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="90e2a-101">Remove-AzureRmPolicyAssignment</span></span>

## <span data-ttu-id="90e2a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="90e2a-102">SYNOPSIS</span></span>
<span data-ttu-id="90e2a-103">Tar bort en princip tilldelning.</span><span class="sxs-lookup"><span data-stu-id="90e2a-103">Removes a policy assignment.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="90e2a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="90e2a-104">SYNTAX</span></span>

### <span data-ttu-id="90e2a-105">NameParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="90e2a-105">NameParameterSet (Default)</span></span>
```
Remove-AzureRmPolicyAssignment -Name <String> -Scope <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="90e2a-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="90e2a-106">IdParameterSet</span></span>
```
Remove-AzureRmPolicyAssignment -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="90e2a-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="90e2a-107">DESCRIPTION</span></span>
<span data-ttu-id="90e2a-108">Cmdleten **Remove-AzureRmPolicyAssignment** tar bort den angivna princip tilldelningen.</span><span class="sxs-lookup"><span data-stu-id="90e2a-108">The **Remove-AzureRmPolicyAssignment** cmdlet removes the specified policy assignment.</span></span>

## <span data-ttu-id="90e2a-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="90e2a-109">EXAMPLES</span></span>

### <span data-ttu-id="90e2a-110">Exempel 1: ta bort princip tilldelning via namn och omfattning</span><span class="sxs-lookup"><span data-stu-id="90e2a-110">Example 1: Remove policy assignment by name and scope</span></span>
```
PS C:\> $ResourceGroup = Get-AzureRmResourceGroup -Name 'ResourceGroup11'
PS C:\> Remove-AzureRmPolicyAssignment -Name 'PolicyAssignment07' -Scope $ResourceGroup.ResourceId -Force
```

<span data-ttu-id="90e2a-111">Det första kommandot får en resurs grupp som heter ResourceGroup11 med hjälp av Get-AzureRMResourceGroup cmdlet.</span><span class="sxs-lookup"><span data-stu-id="90e2a-111">The first command gets a resource group named ResourceGroup11 by using the Get-AzureRMResourceGroup cmdlet.</span></span>
<span data-ttu-id="90e2a-112">Kommandot lagrar objektet i $ResourceGroup variabel.</span><span class="sxs-lookup"><span data-stu-id="90e2a-112">The command stores that object in the $ResourceGroup variable.</span></span>
<span data-ttu-id="90e2a-113">Det andra kommandot tar bort princip tilldelningen med namnet PolicyAssignment07 som tilldelats i en resurs grupp nivå.</span><span class="sxs-lookup"><span data-stu-id="90e2a-113">The second command removes the policy assignment named PolicyAssignment07 that was assigned at a resource group level.</span></span>
<span data-ttu-id="90e2a-114">Egenskapen **ResourceID** för $ResourceGroup identifierar resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="90e2a-114">The **ResourceId** property of $ResourceGroup identifies the resource group.</span></span>

### <span data-ttu-id="90e2a-115">Exempel 2: ta bort princip tilldelning via ID</span><span class="sxs-lookup"><span data-stu-id="90e2a-115">Example 2: Remove policy assignment by ID</span></span>
```
PS C:\> $ResourceGroup = Get-AzureRmResourceGroup -Name 'ResourceGroup11' 
PS C:\> $PolicyAssignment = Get-AzureRmPolicyAssignment -Name 'PolicyAssignment07' -Scope $ResourceGroup.ResourceId
PS C:\> Remove-AzureRmPolicyAssignment -Id $PolicyAssignment.ResourceId -Force
```

<span data-ttu-id="90e2a-116">Det första kommandot får en resurs grupp som heter ResourceGroup11 och lagrar sedan objektet i variabeln $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="90e2a-116">The first command gets a resource group named ResourceGroup11, and then stores that object in the $ResourceGroup variable.</span></span>
<span data-ttu-id="90e2a-117">Det andra kommandot får policy tilldelningen på en resurs grupp nivå och lagrar den sedan i $PolicyAssignment variabel.</span><span class="sxs-lookup"><span data-stu-id="90e2a-117">The second command gets the policy assignment at a resource group level, and then stores it in the $PolicyAssignment variable.</span></span>
<span data-ttu-id="90e2a-118">Egenskapen **ResourceID** för $ResourceGroup identifierar resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="90e2a-118">The **ResourceId** property of $ResourceGroup identifies the resource group.</span></span>
<span data-ttu-id="90e2a-119">Kommandot tar bort princip tilldelningen som egenskapen **ResourceID** för $PolicyAssignment identifieras.</span><span class="sxs-lookup"><span data-stu-id="90e2a-119">The final command removes the policy assignment that the **ResourceId** property of $PolicyAssignment identifies.</span></span>

## <span data-ttu-id="90e2a-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="90e2a-120">PARAMETERS</span></span>

### <span data-ttu-id="90e2a-121">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="90e2a-121">-ApiVersion</span></span>
<span data-ttu-id="90e2a-122">Anger vilken version av API för Resource provider som ska användas.</span><span class="sxs-lookup"><span data-stu-id="90e2a-122">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="90e2a-123">Om du inte anger en version använder denna cmdlet den senaste tillgängliga versionen.</span><span class="sxs-lookup"><span data-stu-id="90e2a-123">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="90e2a-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90e2a-124">-DefaultProfile</span></span>
<span data-ttu-id="90e2a-125">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="90e2a-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90e2a-126">-ID</span><span class="sxs-lookup"><span data-stu-id="90e2a-126">-Id</span></span>
<span data-ttu-id="90e2a-127">Anger det fullständiga resurs-ID för princip tilldelningen som denna cmdlet tar bort.</span><span class="sxs-lookup"><span data-stu-id="90e2a-127">Specifies the fully qualified resource ID for the policy assignment that this cmdlet removes.</span></span>

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

### <span data-ttu-id="90e2a-128">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="90e2a-128">-InformationAction</span></span>
<span data-ttu-id="90e2a-129">Anger hur den här cmdleten svarar på en informations händelse.</span><span class="sxs-lookup"><span data-stu-id="90e2a-129">Specifies how this cmdlet responds to an information event.</span></span>
<span data-ttu-id="90e2a-130">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="90e2a-130">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="90e2a-131">Vidare</span><span class="sxs-lookup"><span data-stu-id="90e2a-131">Continue</span></span>
- <span data-ttu-id="90e2a-132">Över</span><span class="sxs-lookup"><span data-stu-id="90e2a-132">Ignore</span></span>
- <span data-ttu-id="90e2a-133">Inquire</span><span class="sxs-lookup"><span data-stu-id="90e2a-133">Inquire</span></span>
- <span data-ttu-id="90e2a-134">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="90e2a-134">SilentlyContinue</span></span>
- <span data-ttu-id="90e2a-135">Stanna</span><span class="sxs-lookup"><span data-stu-id="90e2a-135">Stop</span></span>
- <span data-ttu-id="90e2a-136">Avbryt</span><span class="sxs-lookup"><span data-stu-id="90e2a-136">Suspend</span></span>

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

### <span data-ttu-id="90e2a-137">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="90e2a-137">-InformationVariable</span></span>
<span data-ttu-id="90e2a-138">Anger en informations variabel.</span><span class="sxs-lookup"><span data-stu-id="90e2a-138">Specifies an information variable.</span></span>

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

### <span data-ttu-id="90e2a-139">-Namn</span><span class="sxs-lookup"><span data-stu-id="90e2a-139">-Name</span></span>
<span data-ttu-id="90e2a-140">Anger namnet på den princip tilldelning som denna cmdlet tar bort.</span><span class="sxs-lookup"><span data-stu-id="90e2a-140">Specifies the name of the policy assignment that this cmdlet removes.</span></span>

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

### <span data-ttu-id="90e2a-141">-För</span><span class="sxs-lookup"><span data-stu-id="90e2a-141">-Pre</span></span>
<span data-ttu-id="90e2a-142">Visar att denna cmdlet betraktar för hands version API-versioner när den automatiskt avgör vilken version som ska användas.</span><span class="sxs-lookup"><span data-stu-id="90e2a-142">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="90e2a-143">-Omfattning</span><span class="sxs-lookup"><span data-stu-id="90e2a-143">-Scope</span></span>
<span data-ttu-id="90e2a-144">Anger omfattningen som principen tillämpas på.</span><span class="sxs-lookup"><span data-stu-id="90e2a-144">Specifies the scope at which the policy is applied.</span></span>

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

### <span data-ttu-id="90e2a-145">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="90e2a-145">-Confirm</span></span>
<span data-ttu-id="90e2a-146">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="90e2a-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="90e2a-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="90e2a-147">-WhatIf</span></span>
<span data-ttu-id="90e2a-148">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="90e2a-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="90e2a-149">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="90e2a-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="90e2a-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90e2a-150">CommonParameters</span></span>
<span data-ttu-id="90e2a-151">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="90e2a-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90e2a-152">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="90e2a-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90e2a-153">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="90e2a-153">INPUTS</span></span>

## <span data-ttu-id="90e2a-154">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="90e2a-154">OUTPUTS</span></span>

## <span data-ttu-id="90e2a-155">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="90e2a-155">NOTES</span></span>

## <span data-ttu-id="90e2a-156">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="90e2a-156">RELATED LINKS</span></span>

[<span data-ttu-id="90e2a-157">Get-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="90e2a-157">Get-AzureRmPolicyAssignment</span></span>](./Get-AzureRmPolicyAssignment.md)

[<span data-ttu-id="90e2a-158">New-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="90e2a-158">New-AzureRmPolicyAssignment</span></span>](./New-AzureRmPolicyAssignment.md)

[<span data-ttu-id="90e2a-159">Set-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="90e2a-159">Set-AzureRmPolicyAssignment</span></span>](./Set-AzureRmPolicyAssignment.md)


