---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 36399302-3EA5-45A3-A042-536CC7EC2E6D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmPolicyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmPolicyAssignment.md
ms.openlocfilehash: 9a238515b0482b36dcebd3bdcdf6976aebc64448
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757472"
---
# <span data-ttu-id="f2c8c-101">Remove-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="f2c8c-101">Remove-AzureRmPolicyAssignment</span></span>

## <span data-ttu-id="f2c8c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f2c8c-102">SYNOPSIS</span></span>
<span data-ttu-id="f2c8c-103">Tar bort en princip tilldelning.</span><span class="sxs-lookup"><span data-stu-id="f2c8c-103">Removes a policy assignment.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f2c8c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f2c8c-104">SYNTAX</span></span>

### <span data-ttu-id="f2c8c-105">Parametern för princip tilldelnings namn.</span><span class="sxs-lookup"><span data-stu-id="f2c8c-105">The policy assignment name parameter set.</span></span> <span data-ttu-id="f2c8c-106">Vis</span><span class="sxs-lookup"><span data-stu-id="f2c8c-106">(Default)</span></span>
```
Remove-AzureRmPolicyAssignment -Name <String> -Scope <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f2c8c-107">ID-parametern för princip tilldelningen.</span><span class="sxs-lookup"><span data-stu-id="f2c8c-107">The policy assignment Id parameter set.</span></span>
```
Remove-AzureRmPolicyAssignment -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f2c8c-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f2c8c-108">DESCRIPTION</span></span>
<span data-ttu-id="f2c8c-109">Cmdleten **Remove-AzureRmPolicyAssignment** tar bort den angivna princip tilldelningen.</span><span class="sxs-lookup"><span data-stu-id="f2c8c-109">The **Remove-AzureRmPolicyAssignment** cmdlet removes the specified policy assignment.</span></span>

## <span data-ttu-id="f2c8c-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f2c8c-110">EXAMPLES</span></span>

### <span data-ttu-id="f2c8c-111">Exempel 1: ta bort princip tilldelning via namn och omfattning</span><span class="sxs-lookup"><span data-stu-id="f2c8c-111">Example 1: Remove policy assignment by name and scope</span></span>
```
PS C:\>$ResourceGroup = Get-AzureRmResourceGroup -Name "ResourceGroup11"
PS C:\> Remove-AzureRmPolicyAssignment -Name "PolicyAssignment07" -Scope $ResourceGroup.ResourceId -Force
```

<span data-ttu-id="f2c8c-112">Det första kommandot får en resurs grupp som heter ResourceGroup11 med hjälp av Get-AzureRMResourceGroup cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f2c8c-112">The first command gets a resource group named ResourceGroup11 by using the Get-AzureRMResourceGroup cmdlet.</span></span>
<span data-ttu-id="f2c8c-113">Kommandot lagrar objektet i $ResourceGroup variabel.</span><span class="sxs-lookup"><span data-stu-id="f2c8c-113">The command stores that object in the $ResourceGroup variable.</span></span>

<span data-ttu-id="f2c8c-114">Det andra kommandot tar bort princip tilldelningen med namnet PolicyAssignment07 som tilldelats i en resurs grupp nivå.</span><span class="sxs-lookup"><span data-stu-id="f2c8c-114">The second command removes the policy assignment named PolicyAssignment07 that was assigned at a resource group level.</span></span>
<span data-ttu-id="f2c8c-115">Egenskapen **ResourceID** för $ResourceGroup identifierar resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="f2c8c-115">The **ResourceId** property of $ResourceGroup identifies the resource group.</span></span>

### <span data-ttu-id="f2c8c-116">Exempel 2: ta bort princip tilldelning via ID</span><span class="sxs-lookup"><span data-stu-id="f2c8c-116">Example 2: Remove policy assignment by ID</span></span>
```
PS C:\>$ResourceGroup = Get-AzureRmResourceGroup -Name "ResourceGroup11" 
PS C:\> $PolicyAssignment = Get-AzureRmPolicyAssignment -Name "PolicyAssignment07" -Scope $ResourceGroup.ResourceId
PS C:\> Remove-AzureRmPolicyAssignment -Id $PolicyAssignment.ResourceId -Force
```

<span data-ttu-id="f2c8c-117">Det första kommandot får en resurs grupp som heter ResourceGroup11 och lagrar sedan objektet i variabeln $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="f2c8c-117">The first command gets a resource group named ResourceGroup11, and then stores that object in the $ResourceGroup variable.</span></span>

<span data-ttu-id="f2c8c-118">Det andra kommandot får policy tilldelningen på en resurs grupp nivå och lagrar den sedan i $PolicyAssignment variabel.</span><span class="sxs-lookup"><span data-stu-id="f2c8c-118">The second command gets the policy assignment at a resource group level, and then stores it in the $PolicyAssignment variable.</span></span>
<span data-ttu-id="f2c8c-119">Egenskapen **ResourceID** för $ResourceGroup identifierar resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="f2c8c-119">The **ResourceId** property of $ResourceGroup identifies the resource group.</span></span>

<span data-ttu-id="f2c8c-120">Kommandot tar bort princip tilldelningen som egenskapen **ResourceID** för $PolicyAssignment identifieras.</span><span class="sxs-lookup"><span data-stu-id="f2c8c-120">The final command removes the policy assignment that the **ResourceId** property of $PolicyAssignment identifies.</span></span>

## <span data-ttu-id="f2c8c-121">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f2c8c-121">PARAMETERS</span></span>

### <span data-ttu-id="f2c8c-122">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="f2c8c-122">-ApiVersion</span></span>
<span data-ttu-id="f2c8c-123">Anger vilken version av API för Resource provider som ska användas.</span><span class="sxs-lookup"><span data-stu-id="f2c8c-123">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="f2c8c-124">Om du inte anger en version använder denna cmdlet den senaste tillgängliga versionen.</span><span class="sxs-lookup"><span data-stu-id="f2c8c-124">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="f2c8c-125">-ID</span><span class="sxs-lookup"><span data-stu-id="f2c8c-125">-Id</span></span>
<span data-ttu-id="f2c8c-126">Anger det fullständiga resurs-ID för princip tilldelningen som denna cmdlet tar bort.</span><span class="sxs-lookup"><span data-stu-id="f2c8c-126">Specifies the fully qualified resource ID for the policy assignment that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: The policy assignment Id parameter set.
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2c8c-127">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="f2c8c-127">-InformationAction</span></span>
<span data-ttu-id="f2c8c-128">Anger hur den här cmdleten svarar på en informations händelse.</span><span class="sxs-lookup"><span data-stu-id="f2c8c-128">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="f2c8c-129">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="f2c8c-129">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f2c8c-130">Vidare</span><span class="sxs-lookup"><span data-stu-id="f2c8c-130">Continue</span></span>
- <span data-ttu-id="f2c8c-131">Över</span><span class="sxs-lookup"><span data-stu-id="f2c8c-131">Ignore</span></span>
- <span data-ttu-id="f2c8c-132">Inquire</span><span class="sxs-lookup"><span data-stu-id="f2c8c-132">Inquire</span></span>
- <span data-ttu-id="f2c8c-133">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="f2c8c-133">SilentlyContinue</span></span>
- <span data-ttu-id="f2c8c-134">Stanna</span><span class="sxs-lookup"><span data-stu-id="f2c8c-134">Stop</span></span>
- <span data-ttu-id="f2c8c-135">Avbryt</span><span class="sxs-lookup"><span data-stu-id="f2c8c-135">Suspend</span></span>

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

### <span data-ttu-id="f2c8c-136">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="f2c8c-136">-InformationVariable</span></span>
<span data-ttu-id="f2c8c-137">Anger en informations variabel.</span><span class="sxs-lookup"><span data-stu-id="f2c8c-137">Specifies an information variable.</span></span>

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

### <span data-ttu-id="f2c8c-138">-Namn</span><span class="sxs-lookup"><span data-stu-id="f2c8c-138">-Name</span></span>
<span data-ttu-id="f2c8c-139">Anger namnet på den princip tilldelning som denna cmdlet tar bort.</span><span class="sxs-lookup"><span data-stu-id="f2c8c-139">Specifies the name of the policy assignment that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: The policy assignment name parameter set.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2c8c-140">-För</span><span class="sxs-lookup"><span data-stu-id="f2c8c-140">-Pre</span></span>
<span data-ttu-id="f2c8c-141">Visar att denna cmdlet betraktar för hands version API-versioner när den automatiskt avgör vilken version som ska användas.</span><span class="sxs-lookup"><span data-stu-id="f2c8c-141">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="f2c8c-142">-Omfattning</span><span class="sxs-lookup"><span data-stu-id="f2c8c-142">-Scope</span></span>
<span data-ttu-id="f2c8c-143">Anger omfattningen som principen tillämpas på.</span><span class="sxs-lookup"><span data-stu-id="f2c8c-143">Specifies the scope at which the policy is applied.</span></span>

```yaml
Type: System.String
Parameter Sets: The policy assignment name parameter set.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2c8c-144">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="f2c8c-144">-Confirm</span></span>
<span data-ttu-id="f2c8c-145">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="f2c8c-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f2c8c-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f2c8c-146">-WhatIf</span></span>
<span data-ttu-id="f2c8c-147">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="f2c8c-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f2c8c-148">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="f2c8c-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f2c8c-149">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2c8c-149">-DefaultProfile</span></span>
<span data-ttu-id="f2c8c-150">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f2c8c-150">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f2c8c-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2c8c-151">CommonParameters</span></span>
<span data-ttu-id="f2c8c-152">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f2c8c-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2c8c-153">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f2c8c-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2c8c-154">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f2c8c-154">INPUTS</span></span>

## <span data-ttu-id="f2c8c-155">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f2c8c-155">OUTPUTS</span></span>

### <span data-ttu-id="f2c8c-156">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f2c8c-156">System.Boolean</span></span>

## <span data-ttu-id="f2c8c-157">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f2c8c-157">NOTES</span></span>

## <span data-ttu-id="f2c8c-158">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f2c8c-158">RELATED LINKS</span></span>

[<span data-ttu-id="f2c8c-159">Get-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="f2c8c-159">Get-AzureRmPolicyAssignment</span></span>](./Get-AzureRmPolicyAssignment.md)

[<span data-ttu-id="f2c8c-160">New-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="f2c8c-160">New-AzureRmPolicyAssignment</span></span>](./New-AzureRmPolicyAssignment.md)

[<span data-ttu-id="f2c8c-161">Set-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="f2c8c-161">Set-AzureRmPolicyAssignment</span></span>](./Set-AzureRmPolicyAssignment.md)


