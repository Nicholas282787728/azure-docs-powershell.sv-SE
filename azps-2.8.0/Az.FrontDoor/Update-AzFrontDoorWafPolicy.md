---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/update-azfrontdoorwafpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Update-AzFrontDoorWafPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Update-AzFrontDoorWafPolicy.md
ms.openlocfilehash: fe7fb7c2c70563ef44cbdab6b3cfbf0ec7eeea7d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93744121"
---
# <span data-ttu-id="8218c-101">Update-AzFrontDoorWafPolicy</span><span class="sxs-lookup"><span data-stu-id="8218c-101">Update-AzFrontDoorWafPolicy</span></span>

## <span data-ttu-id="8218c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8218c-102">SYNOPSIS</span></span>
<span data-ttu-id="8218c-103">Uppdatera WAF policy</span><span class="sxs-lookup"><span data-stu-id="8218c-103">Update WAF policy</span></span>

## <span data-ttu-id="8218c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8218c-104">SYNTAX</span></span>

### <span data-ttu-id="8218c-105">ByFieldsParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="8218c-105">ByFieldsParameterSet (Default)</span></span>
```
Update-AzFrontDoorWafPolicy -ResourceGroupName <String> -Name <String> [-EnabledState <PSEnabledState>]
 [-Mode <String>] [-Customrule <PSCustomRule[]>] [-ManagedRule <PSManagedRule[]>] [-RedirectUrl <String>]
 [-CustomBlockResponseStatusCode <Int32>] [-CustomBlockResponseBody <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8218c-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8218c-106">ByObjectParameterSet</span></span>
```
Update-AzFrontDoorWafPolicy -InputObject <PSPolicy> [-EnabledState <PSEnabledState>] [-Mode <String>]
 [-Customrule <PSCustomRule[]>] [-ManagedRule <PSManagedRule[]>] [-RedirectUrl <String>]
 [-CustomBlockResponseStatusCode <Int32>] [-CustomBlockResponseBody <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8218c-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8218c-107">ByResourceIdParameterSet</span></span>
```
Update-AzFrontDoorWafPolicy -ResourceId <String> [-EnabledState <PSEnabledState>] [-Mode <String>]
 [-Customrule <PSCustomRule[]>] [-ManagedRule <PSManagedRule[]>] [-RedirectUrl <String>]
 [-CustomBlockResponseStatusCode <Int32>] [-CustomBlockResponseBody <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8218c-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8218c-108">DESCRIPTION</span></span>
<span data-ttu-id="8218c-109">Cmdleten **Update-AzFrontDoorWafPolicy** uppdaterar en befintlig WAF-princip.</span><span class="sxs-lookup"><span data-stu-id="8218c-109">The **Update-AzFrontDoorWafPolicy** cmdlet updates an existing WAF policy.</span></span> <span data-ttu-id="8218c-110">Om indataparametrarna inte anges används gamla parametrar från den befintliga WAF-principen.</span><span class="sxs-lookup"><span data-stu-id="8218c-110">If input parameters are not provided, old parameters from the existing WAF policy will be used.</span></span>

## <span data-ttu-id="8218c-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8218c-111">EXAMPLES</span></span>

### <span data-ttu-id="8218c-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="8218c-112">Example 1</span></span>
```powershell
PS C:\> Update-AzFrontDoorWafPolicy -Name $policyName -ResourceGroupName $resourceGroupName -CustomBlockResponseStatusCode 403

Name         PolicyMode PolicyEnabledState CustomBlockResponseStatusCode RedirectUrl
----         ---------- ------------------ ----------------------------- -----------
{policyName} Prevention            Enabled                           403 https://www.bing.com/
```

<span data-ttu-id="8218c-113">Uppdatera en befintlig anpassad WAF-kod för en policy.</span><span class="sxs-lookup"><span data-stu-id="8218c-113">Update an existing WAF policy custom status code.</span></span>

### <span data-ttu-id="8218c-114">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="8218c-114">Example 2</span></span>
```powershell
PS C:\> Update-AzFrontDoorWafPolicy -Name $policyName -ResourceGroupName $resourceGroupName -Mode Detection

Name         PolicyMode PolicyEnabledState CustomBlockResponseStatusCode RedirectUrl
----         ---------- ------------------ ----------------------------- -----------
{policyName} Detection            Enabled                           403 https://www.bing.com/
```

<span data-ttu-id="8218c-115">Uppdatera ett befintligt WAF.</span><span class="sxs-lookup"><span data-stu-id="8218c-115">Update an existing WAF policy mode.</span></span>

### <span data-ttu-id="8218c-116">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="8218c-116">Example 3</span></span>
```powershell
PS C:\> Update-AzFrontDoorWafPolicy -Name $policyName -ResourceGroupName $resourceGroupName -Mode Detection -EnabledState Disabled

Name          PolicyMode PolicyEnabledState CustomBlockResponseStatusCode RedirectUrl
----          ---------- ------------------ ----------------------------- -----------
{policyName}  Detection           Disabled                           403 https://www.bing.com/
```

<span data-ttu-id="8218c-117">Uppdatera en befintlig policy för WAF aktiverat tillstånd och läge.</span><span class="sxs-lookup"><span data-stu-id="8218c-117">Update an existing WAF policy enabled state and mode.</span></span>

### <span data-ttu-id="8218c-118">Exempel 4</span><span class="sxs-lookup"><span data-stu-id="8218c-118">Example 4</span></span>
```powershell
PS C:\> Get-AzFrontDoorWafPolicy -ResourceGroupName $resourceGroupName | Update-AzFrontDoorWafPolicy -Mode Detection -EnabledState Disabled
```

<span data-ttu-id="8218c-119">Uppdatera alla WAF-principer i $resourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8218c-119">Update all WAF policies in $resourceGroupName</span></span>

## <span data-ttu-id="8218c-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8218c-120">PARAMETERS</span></span>

### <span data-ttu-id="8218c-121">-CustomBlockResponseBody</span><span class="sxs-lookup"><span data-stu-id="8218c-121">-CustomBlockResponseBody</span></span>
<span data-ttu-id="8218c-122">Anpassat svar</span><span class="sxs-lookup"><span data-stu-id="8218c-122">Custom Response Body</span></span>

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

### <span data-ttu-id="8218c-123">-CustomBlockResponseStatusCode</span><span class="sxs-lookup"><span data-stu-id="8218c-123">-CustomBlockResponseStatusCode</span></span>
<span data-ttu-id="8218c-124">Anpassad svars status kod</span><span class="sxs-lookup"><span data-stu-id="8218c-124">Custom Response Status Code</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8218c-125">-Customrule</span><span class="sxs-lookup"><span data-stu-id="8218c-125">-Customrule</span></span>
<span data-ttu-id="8218c-126">Anpassade regler inuti policyn</span><span class="sxs-lookup"><span data-stu-id="8218c-126">Custom rules inside the policy</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSCustomRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8218c-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8218c-127">-DefaultProfile</span></span>
<span data-ttu-id="8218c-128">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="8218c-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8218c-129">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="8218c-129">-EnabledState</span></span>
<span data-ttu-id="8218c-130">Om principen är aktiverat eller inte.</span><span class="sxs-lookup"><span data-stu-id="8218c-130">Whether the policy is in enabled state or disabled state.</span></span>
<span data-ttu-id="8218c-131">Möjliga värden är: ' disabled ', ' Enabled '</span><span class="sxs-lookup"><span data-stu-id="8218c-131">Possible values include: 'Disabled', 'Enabled'</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSEnabledState
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8218c-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8218c-132">-InputObject</span></span>
<span data-ttu-id="8218c-133">FireWallPolicy-objekt som ska uppdateras.</span><span class="sxs-lookup"><span data-stu-id="8218c-133">The FireWallPolicy object to update.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8218c-134">-ManagedRule</span><span class="sxs-lookup"><span data-stu-id="8218c-134">-ManagedRule</span></span>
<span data-ttu-id="8218c-135">Hanterade regler inuti policyn</span><span class="sxs-lookup"><span data-stu-id="8218c-135">Managed rules inside the policy</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSManagedRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8218c-136">-Mode</span><span class="sxs-lookup"><span data-stu-id="8218c-136">-Mode</span></span>
<span data-ttu-id="8218c-137">Beskriver om den är i identifierings läge eller i läget förhindra på princip nivå.</span><span class="sxs-lookup"><span data-stu-id="8218c-137">Describes if it is in detection mode  or prevention mode at policy level.</span></span>
<span data-ttu-id="8218c-138">Möjliga värden är: "förebygga", "identifiering"</span><span class="sxs-lookup"><span data-stu-id="8218c-138">Possible values include:'Prevention', 'Detection'</span></span>

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

### <span data-ttu-id="8218c-139">-Namn</span><span class="sxs-lookup"><span data-stu-id="8218c-139">-Name</span></span>
<span data-ttu-id="8218c-140">Namnet på den FireWallPolicy som ska uppdateras.</span><span class="sxs-lookup"><span data-stu-id="8218c-140">The name of the FireWallPolicy to update.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8218c-141">-RedirectUrl</span><span class="sxs-lookup"><span data-stu-id="8218c-141">-RedirectUrl</span></span>
<span data-ttu-id="8218c-142">Omdirigera URL</span><span class="sxs-lookup"><span data-stu-id="8218c-142">Redirect URL</span></span>

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

### <span data-ttu-id="8218c-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8218c-143">-ResourceGroupName</span></span>
<span data-ttu-id="8218c-144">Resurs gruppen som FireWallPolicy hör till.</span><span class="sxs-lookup"><span data-stu-id="8218c-144">The resource group to which the FireWallPolicy belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8218c-145">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8218c-145">-ResourceId</span></span>
<span data-ttu-id="8218c-146">Resurs-ID för FireWallPolicy som ska uppdateras</span><span class="sxs-lookup"><span data-stu-id="8218c-146">Resource Id of the FireWallPolicy to update</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8218c-147">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="8218c-147">-Confirm</span></span>
<span data-ttu-id="8218c-148">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="8218c-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8218c-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8218c-149">-WhatIf</span></span>
<span data-ttu-id="8218c-150">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="8218c-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8218c-151">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="8218c-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8218c-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8218c-152">CommonParameters</span></span>
<span data-ttu-id="8218c-153">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8218c-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8218c-154">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8218c-154">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8218c-155">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8218c-155">INPUTS</span></span>

### <span data-ttu-id="8218c-156">Microsoft. Azure. commands. FrontDoor. Models. PSPolicy</span><span class="sxs-lookup"><span data-stu-id="8218c-156">Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy</span></span>

### <span data-ttu-id="8218c-157">System. String</span><span class="sxs-lookup"><span data-stu-id="8218c-157">System.String</span></span>

## <span data-ttu-id="8218c-158">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8218c-158">OUTPUTS</span></span>

### <span data-ttu-id="8218c-159">Microsoft. Azure. commands. FrontDoor. Models. PSPolicy</span><span class="sxs-lookup"><span data-stu-id="8218c-159">Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy</span></span>

## <span data-ttu-id="8218c-160">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8218c-160">NOTES</span></span>

## <span data-ttu-id="8218c-161">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8218c-161">RELATED LINKS</span></span>

<span data-ttu-id="8218c-162">[New-AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md) 
 [Get-AzFrontDoorWafPolicy](./Get-AzFrontDoorWafPolicy.md) 
 [New-AzFrontDoorWafManagedRuleObject](./New-AzFrontDoorWafManagedRuleObject.md) 
 [New-AzFrontDoorWafCustomRuleObject](./New-AzFrontDoorWafManagedRuleObject.md)</span><span class="sxs-lookup"><span data-stu-id="8218c-162">[New-AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md)
[Get-AzFrontDoorWafPolicy](./Get-AzFrontDoorWafPolicy.md)
[New-AzFrontDoorWafManagedRuleObject](./New-AzFrontDoorWafManagedRuleObject.md)
[New-AzFrontDoorWafCustomRuleObject](./New-AzFrontDoorWafManagedRuleObject.md)</span></span>
