---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorFireWallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorFireWallPolicy.md
ms.openlocfilehash: 67caf6c97c493ad1d19b95ef00c896cb96a47582
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93916745"
---
# <span data-ttu-id="8068d-101">New-AzFrontDoorFireWallPolicy</span><span class="sxs-lookup"><span data-stu-id="8068d-101">New-AzFrontDoorFireWallPolicy</span></span>

## <span data-ttu-id="8068d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8068d-102">SYNOPSIS</span></span>
<span data-ttu-id="8068d-103">Skapa WAF policy</span><span class="sxs-lookup"><span data-stu-id="8068d-103">Create WAF policy</span></span>

## <span data-ttu-id="8068d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8068d-104">SYNTAX</span></span>

```
New-AzFrontDoorFireWallPolicy -ResourceGroupName <String> -Name <String> [-EnabledState <PSEnabledState>]
 [-Mode <PSMode>] [-Customrule <PSCustomRule[]>] [-ManagedRule <PSManagedRule[]>] [-RedirectUrl <String>]
 [-CustomBlockResponseStatusCode <Int32>] [-CustomBlockResponseBody <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8068d-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8068d-105">DESCRIPTION</span></span>
<span data-ttu-id="8068d-106">Cmdleten **New-AzFrontDoorFireWallPolicy** skapar en ny Azure WAF-princip i den angivna resurs gruppen under aktuell prenumeration</span><span class="sxs-lookup"><span data-stu-id="8068d-106">The **New-AzFrontDoorFireWallPolicy** cmdlet creates a new Azure WAF policy in the specified resource group under current subscription</span></span>

## <span data-ttu-id="8068d-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8068d-107">EXAMPLES</span></span>

### <span data-ttu-id="8068d-108">Exempel 1: skapa WAF policy</span><span class="sxs-lookup"><span data-stu-id="8068d-108">Example 1: Create WAF policy</span></span>
```powershell
PS C:\> New-AzFrontDoorFireWallPolicy -Name $policyName -ResourceGroupName $resourceGroupName -Customrule $customRule1,$customRule2 -ManagedRule $managedRule1 -EnabledState Enabled -Mode Prevention -RedirectUrl "https://www.bing.com/" -CustomBlockResponseStatusCode 405 -CustomBlockResponseBody "<html><head><title>You are blocked!</title></head><body></body></html>"

Name         PolicyMode PolicyEnabledState RedirectUrl
----         ---------- ------------------ -----------
{policyName} Prevention            Enabled https://www.bing.com/
```

<span data-ttu-id="8068d-109">Skapa WAF policy</span><span class="sxs-lookup"><span data-stu-id="8068d-109">Create WAF policy</span></span>

## <span data-ttu-id="8068d-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8068d-110">PARAMETERS</span></span>

### <span data-ttu-id="8068d-111">-CustomBlockResponseBody</span><span class="sxs-lookup"><span data-stu-id="8068d-111">-CustomBlockResponseBody</span></span>
<span data-ttu-id="8068d-112">Anpassat svar</span><span class="sxs-lookup"><span data-stu-id="8068d-112">Custom Response Body</span></span>

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

### <span data-ttu-id="8068d-113">-CustomBlockResponseStatusCode</span><span class="sxs-lookup"><span data-stu-id="8068d-113">-CustomBlockResponseStatusCode</span></span>
<span data-ttu-id="8068d-114">Anpassad svars status kod</span><span class="sxs-lookup"><span data-stu-id="8068d-114">Custom Response Status Code</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8068d-115">-Customrule</span><span class="sxs-lookup"><span data-stu-id="8068d-115">-Customrule</span></span>
<span data-ttu-id="8068d-116">Anpassade regler inuti policyn</span><span class="sxs-lookup"><span data-stu-id="8068d-116">Custom rules inside the policy</span></span>

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

### <span data-ttu-id="8068d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8068d-117">-DefaultProfile</span></span>
<span data-ttu-id="8068d-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="8068d-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8068d-119">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="8068d-119">-EnabledState</span></span>
<span data-ttu-id="8068d-120">Om principen är aktiverat eller inte.</span><span class="sxs-lookup"><span data-stu-id="8068d-120">Whether the policy is in enabled state or disabled state.</span></span>
<span data-ttu-id="8068d-121">Möjliga värden är: ' disabled ', ' Enabled '</span><span class="sxs-lookup"><span data-stu-id="8068d-121">Possible values include: 'Disabled', 'Enabled'</span></span>

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

### <span data-ttu-id="8068d-122">-ManagedRule</span><span class="sxs-lookup"><span data-stu-id="8068d-122">-ManagedRule</span></span>
<span data-ttu-id="8068d-123">Hanterade regler inuti policyn</span><span class="sxs-lookup"><span data-stu-id="8068d-123">Managed rules inside the policy</span></span>

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

### <span data-ttu-id="8068d-124">-Mode</span><span class="sxs-lookup"><span data-stu-id="8068d-124">-Mode</span></span>
<span data-ttu-id="8068d-125">Beskriver om den är i identifierings läge eller i läget förhindra på princip nivå.</span><span class="sxs-lookup"><span data-stu-id="8068d-125">Describes if it is in detection mode  or prevention mode at policy level.</span></span>
<span data-ttu-id="8068d-126">Möjliga värden är: "förebygga", "identifiering"</span><span class="sxs-lookup"><span data-stu-id="8068d-126">Possible values include:'Prevention', 'Detection'</span></span>

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

### <span data-ttu-id="8068d-127">-Namn</span><span class="sxs-lookup"><span data-stu-id="8068d-127">-Name</span></span>
<span data-ttu-id="8068d-128">WebApplicationFireWallPolicy namn.</span><span class="sxs-lookup"><span data-stu-id="8068d-128">WebApplicationFireWallPolicy name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8068d-129">-RedirectUrl</span><span class="sxs-lookup"><span data-stu-id="8068d-129">-RedirectUrl</span></span>
<span data-ttu-id="8068d-130">Omdirigera URL</span><span class="sxs-lookup"><span data-stu-id="8068d-130">Redirect URL</span></span>

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

### <span data-ttu-id="8068d-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8068d-131">-ResourceGroupName</span></span>
<span data-ttu-id="8068d-132">Resurs gruppens namn</span><span class="sxs-lookup"><span data-stu-id="8068d-132">The resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8068d-133">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="8068d-133">-Confirm</span></span>
<span data-ttu-id="8068d-134">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="8068d-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8068d-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8068d-135">-WhatIf</span></span>
<span data-ttu-id="8068d-136">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="8068d-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8068d-137">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="8068d-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8068d-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8068d-138">CommonParameters</span></span>
<span data-ttu-id="8068d-139">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8068d-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8068d-140">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8068d-140">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8068d-141">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8068d-141">INPUTS</span></span>

### <span data-ttu-id="8068d-142">Ingen</span><span class="sxs-lookup"><span data-stu-id="8068d-142">None</span></span>

## <span data-ttu-id="8068d-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8068d-143">OUTPUTS</span></span>

### <span data-ttu-id="8068d-144">Microsoft. Azure. commands. FrontDoor. Models. PSPolicy</span><span class="sxs-lookup"><span data-stu-id="8068d-144">Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy</span></span>

## <span data-ttu-id="8068d-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8068d-145">NOTES</span></span>

## <span data-ttu-id="8068d-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8068d-146">RELATED LINKS</span></span>

<span data-ttu-id="8068d-147">[Set-AzFrontDoorFireWallPolicy](./Set-AzFrontDoorFireWallPolicy.md) 
 [Get-AzFrontDoorFireWallPolicy](./Get-AzFrontDoorFireWallPolicy.md) 
 [Remove-AzFrontDoorFireWallPolicy](./Remove-AzFrontDoorFireWallPolicy.md) 
 [New-AzFrontDoorManagedRuleObject](./New-AzFrontDoorManagedRuleObject.md) 
 [New-AzFrontDoorCustomRuleObject](./New-AzFrontDoorManagedRuleObject.md)</span><span class="sxs-lookup"><span data-stu-id="8068d-147">[Set-AzFrontDoorFireWallPolicy](./Set-AzFrontDoorFireWallPolicy.md)
[Get-AzFrontDoorFireWallPolicy](./Get-AzFrontDoorFireWallPolicy.md)
[Remove-AzFrontDoorFireWallPolicy](./Remove-AzFrontDoorFireWallPolicy.md)
[New-AzFrontDoorManagedRuleObject](./New-AzFrontDoorManagedRuleObject.md)
[New-AzFrontDoorCustomRuleObject](./New-AzFrontDoorManagedRuleObject.md)</span></span>
