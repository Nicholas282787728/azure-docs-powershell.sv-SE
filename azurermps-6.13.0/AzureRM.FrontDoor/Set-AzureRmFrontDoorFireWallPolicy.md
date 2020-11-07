---
external help file: Microsoft.Azure.Commands.FrontDoor.dll-Help.xml
Module Name: AzureRM.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.frontdoor/set-azurermfrontdoorfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/Set-AzureRmFrontDoorFireWallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/Set-AzureRmFrontDoorFireWallPolicy.md
ms.openlocfilehash: a02510cc72b9e674f9d4fded1355ae5b2cadc807
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93755198"
---
# <span data-ttu-id="d6330-101">Set-AzureRmFrontDoorFireWallPolicy</span><span class="sxs-lookup"><span data-stu-id="d6330-101">Set-AzureRmFrontDoorFireWallPolicy</span></span>

## <span data-ttu-id="d6330-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d6330-102">SYNOPSIS</span></span>
<span data-ttu-id="d6330-103">uppdatera WAF policy</span><span class="sxs-lookup"><span data-stu-id="d6330-103">update WAF policy</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d6330-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d6330-104">SYNTAX</span></span>

### <span data-ttu-id="d6330-105">ByFieldsParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="d6330-105">ByFieldsParameterSet (Default)</span></span>
```
Set-AzureRmFrontDoorFireWallPolicy -ResourceGroupName <String> -Name <String> [-EnabledState <PSEnabledState>]
 [-Mode <PSMode>] [-Customrule <PSCustomRule[]>] [-ManagedRule <PSManagedRule[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d6330-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d6330-106">ByObjectParameterSet</span></span>
```
Set-AzureRmFrontDoorFireWallPolicy -InputObject <PSPolicy> [-EnabledState <PSEnabledState>] [-Mode <PSMode>]
 [-Customrule <PSCustomRule[]>] [-ManagedRule <PSManagedRule[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d6330-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d6330-107">ResourceIdParameterSet</span></span>
```
Set-AzureRmFrontDoorFireWallPolicy -ResourceId <String> [-EnabledState <PSEnabledState>] [-Mode <PSMode>]
 [-Customrule <PSCustomRule[]>] [-ManagedRule <PSManagedRule[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d6330-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d6330-108">DESCRIPTION</span></span>
<span data-ttu-id="d6330-109">Cmdleten **set-AzureRmFrontDoor** uppdaterar en befintlig WAF-princip.</span><span class="sxs-lookup"><span data-stu-id="d6330-109">The **Set-AzureRmFrontDoor** cmdlet updates an existing WAF policy.</span></span> <span data-ttu-id="d6330-110">Om indataparametrarna inte anges används gamla parametrar från den befintliga WAF-principen.</span><span class="sxs-lookup"><span data-stu-id="d6330-110">If input parameters are not provided, old parameters from the existing WAF policy will be used.</span></span>

## <span data-ttu-id="d6330-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d6330-111">EXAMPLES</span></span>

### <span data-ttu-id="d6330-112">Exempel 1: uppdatera en befintlig WAF-policy</span><span class="sxs-lookup"><span data-stu-id="d6330-112">Example 1: update an existing WAF policy</span></span>
```powershell
PS C:\> Set-AzureRmFrontDoorFireWallPolicy -Name $name -ResourceGroupName $resourceGroup -Customrule $customRule -ManagedRule $managedRule -EnabledState $enabledState -Mode $node

PolicyMode         : Prevention
PolicyEnabledState : Enabled
CustomRules        : {Rule1}
ManagedRules       : {Microsoft.Azure.Commands.FrontDoor.Models.PSAzureManagedRule}
Etag               :
ProvisioningState  : Succeeded
Tags               :
Id                 : /subscriptions/{subid}/resourcegroups/{resourceGroupName}/providers/Micr
                     osoft.Network/frontdoorwebapplicationfirewallpolicies/{Name}
Name               : {Name}
Type               :
```

<span data-ttu-id="d6330-113">uppdatera en befintlig WAF-princip</span><span class="sxs-lookup"><span data-stu-id="d6330-113">update an existing WAF policy</span></span>

### <span data-ttu-id="d6330-114">Exempel 2: uppdatera en befintlig WAF-policy</span><span class="sxs-lookup"><span data-stu-id="d6330-114">Example 2: update an existing WAF policy</span></span>
```powershell
PS C:\> Set-AzureRmFrontDoorFireWallPolicy -InputObject $policy1 -Customrule $customRule -ManagedRule $managedRule -EnabledState $enabledState -Mode $mode

PolicyMode         : Prevention
PolicyEnabledState : Enabled
CustomRules        : {Rule1}
ManagedRules       : {Microsoft.Azure.Commands.FrontDoor.Models.PSAzureManagedRule}
Etag               :
ProvisioningState  : Succeeded
Tags               :
Id                 : /subscriptions/{subid}/resourcegroups/{resourceGroupName}/providers/Micr
                     osoft.Network/frontdoorwebapplicationfirewallpolicies/{Name}
Name               : {Name}
Type               :
```

<span data-ttu-id="d6330-115">uppdatera en befintlig WAF-princip</span><span class="sxs-lookup"><span data-stu-id="d6330-115">update an existing WAF policy</span></span>

### <span data-ttu-id="d6330-116">Exempel 3: uppdatera en befintlig WAF-princip</span><span class="sxs-lookup"><span data-stu-id="d6330-116">Example 3: update an existing WAF policy</span></span>
```powershell
PS C:\> Set-AzureRmFrontDoorFireWallPolicy -ResourceId $resourcdId -Customrule $customRule -ManagedRule $managedRule -EnabledState $enabledState -Mode $mode

PolicyMode         : Prevention
PolicyEnabledState : Enabled
CustomRules        : {Rule1}
ManagedRules       : {Microsoft.Azure.Commands.FrontDoor.Models.PSAzureManagedRule}
Etag               :
ProvisioningState  : Succeeded
Tags               :
Id                 : /subscriptions/{subid}/resourcegroups/{resourceGroupName}/providers/Micr
                     osoft.Network/frontdoorwebapplicationfirewallpolicies/{Name}
Name               : {Name}
Type               :
```

<span data-ttu-id="d6330-117">uppdatera en befintlig WAF-princip</span><span class="sxs-lookup"><span data-stu-id="d6330-117">update an existing WAF policy</span></span>

### <span data-ttu-id="d6330-118">Exempel 4: uppdatera alla WAF-principer i $resourceGroup</span><span class="sxs-lookup"><span data-stu-id="d6330-118">Example 4: update all WAF policies in $resourceGroup</span></span>
```powershell
PS C:\> Get-AzureRmFrontDoorFireWallPolicy -ResourceGroupName $resourceGroup | Set-AzureRmFrontDoorFireWallPolicy -Customrule $customRule -ManagedRule $managedRule -EnabledState $enabledState -Mode $mode
```

<span data-ttu-id="d6330-119">uppdatera alla WAF-principer i $resourceGroup</span><span class="sxs-lookup"><span data-stu-id="d6330-119">update all WAF policies in $resourceGroup</span></span>

## <span data-ttu-id="d6330-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d6330-120">PARAMETERS</span></span>

### <span data-ttu-id="d6330-121">-Customrule</span><span class="sxs-lookup"><span data-stu-id="d6330-121">-Customrule</span></span>
<span data-ttu-id="d6330-122">Anpassade regler inuti policyn</span><span class="sxs-lookup"><span data-stu-id="d6330-122">Custom rules inside the policy</span></span>

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

### <span data-ttu-id="d6330-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6330-123">-DefaultProfile</span></span>
<span data-ttu-id="d6330-124">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d6330-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d6330-125">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="d6330-125">-EnabledState</span></span>
<span data-ttu-id="d6330-126">Om principen är aktiverat eller inte.</span><span class="sxs-lookup"><span data-stu-id="d6330-126">Whether the policy is in enabled state or disabled state.</span></span>
<span data-ttu-id="d6330-127">Möjliga värden är: ' disabled ', ' Enabled '</span><span class="sxs-lookup"><span data-stu-id="d6330-127">Possible values include: 'Disabled', 'Enabled'</span></span>

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

### <span data-ttu-id="d6330-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d6330-128">-InputObject</span></span>
<span data-ttu-id="d6330-129">FireWallPolicy-objekt som ska uppdateras.</span><span class="sxs-lookup"><span data-stu-id="d6330-129">The FireWallPolicy object to update.</span></span>

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

### <span data-ttu-id="d6330-130">-ManagedRule</span><span class="sxs-lookup"><span data-stu-id="d6330-130">-ManagedRule</span></span>
<span data-ttu-id="d6330-131">Hanterade regler inuti policyn</span><span class="sxs-lookup"><span data-stu-id="d6330-131">Managed rules inside the policy</span></span>

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

### <span data-ttu-id="d6330-132">-Mode</span><span class="sxs-lookup"><span data-stu-id="d6330-132">-Mode</span></span>
<span data-ttu-id="d6330-133">Beskriver om den är i identifierings läge eller i läget förhindra på princip nivå.</span><span class="sxs-lookup"><span data-stu-id="d6330-133">Describes if it is in detection mode  or prevention mode at policy level.</span></span>
<span data-ttu-id="d6330-134">Möjliga värden är: "förebygga", "identifiering"</span><span class="sxs-lookup"><span data-stu-id="d6330-134">Possible values include:'Prevention', 'Detection'</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSMode
Parameter Sets: (All)
Aliases:
Accepted values: Prevention, Detection

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6330-135">-Namn</span><span class="sxs-lookup"><span data-stu-id="d6330-135">-Name</span></span>
<span data-ttu-id="d6330-136">Namnet på den FireWallPolicy som ska uppdateras.</span><span class="sxs-lookup"><span data-stu-id="d6330-136">The name of the FireWallPolicy to update.</span></span>

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

### <span data-ttu-id="d6330-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d6330-137">-ResourceGroupName</span></span>
<span data-ttu-id="d6330-138">Resurs gruppen som FireWallPolicy hör till.</span><span class="sxs-lookup"><span data-stu-id="d6330-138">The resource group to which the FireWallPolicy belongs.</span></span>

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

### <span data-ttu-id="d6330-139">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d6330-139">-ResourceId</span></span>
<span data-ttu-id="d6330-140">Resurs-ID för FireWallPolicy som ska uppdateras</span><span class="sxs-lookup"><span data-stu-id="d6330-140">Resource Id of the FireWallPolicy to update</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6330-141">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="d6330-141">-Confirm</span></span>
<span data-ttu-id="d6330-142">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="d6330-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d6330-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d6330-143">-WhatIf</span></span>
<span data-ttu-id="d6330-144">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="d6330-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d6330-145">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="d6330-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d6330-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6330-146">CommonParameters</span></span>
<span data-ttu-id="d6330-147">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d6330-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6330-148">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d6330-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6330-149">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d6330-149">INPUTS</span></span>

### <span data-ttu-id="d6330-150">Microsoft. Azure. commands. FrontDoor. Models. PSPolicy</span><span class="sxs-lookup"><span data-stu-id="d6330-150">Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy</span></span>

### <span data-ttu-id="d6330-151">System. String</span><span class="sxs-lookup"><span data-stu-id="d6330-151">System.String</span></span>

## <span data-ttu-id="d6330-152">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d6330-152">OUTPUTS</span></span>

### <span data-ttu-id="d6330-153">Microsoft. Azure. commands. FrontDoor. Models. PSPolicy</span><span class="sxs-lookup"><span data-stu-id="d6330-153">Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy</span></span>

## <span data-ttu-id="d6330-154">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d6330-154">NOTES</span></span>

## <span data-ttu-id="d6330-155">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d6330-155">RELATED LINKS</span></span>

<span data-ttu-id="d6330-156">[New-AzureRmFrontDoorFireWallPolicy](./New-AzureRmFrontDoorFireWallPolicy.md) 
 [Get-AzureRmFrontDoorFireWallPolicy](./Get-AzureRmFrontDoorFireWallPolicy.md) 
 [New-AzureRmFrontDoorManagedRuleObject](./New-AzureRmFrontDoorManagedRuleObject.md) 
 [New-AzureRmFrontDoorCustomRuleObject](./New-AzureRmFrontDoorManagedRuleObject.md)</span><span class="sxs-lookup"><span data-stu-id="d6330-156">[New-AzureRmFrontDoorFireWallPolicy](./New-AzureRmFrontDoorFireWallPolicy.md)
[Get-AzureRmFrontDoorFireWallPolicy](./Get-AzureRmFrontDoorFireWallPolicy.md)
[New-AzureRmFrontDoorManagedRuleObject](./New-AzureRmFrontDoorManagedRuleObject.md)
[New-AzureRmFrontDoorCustomRuleObject](./New-AzureRmFrontDoorManagedRuleObject.md)</span></span>
