---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorwafpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafPolicy.md
ms.openlocfilehash: 242478245188e68fe0a5d86ee7c54aba57d4d056
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93744133"
---
# <span data-ttu-id="f6191-101">New-AzFrontDoorWafPolicy</span><span class="sxs-lookup"><span data-stu-id="f6191-101">New-AzFrontDoorWafPolicy</span></span>

## <span data-ttu-id="f6191-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f6191-102">SYNOPSIS</span></span>
<span data-ttu-id="f6191-103">Skapa WAF policy</span><span class="sxs-lookup"><span data-stu-id="f6191-103">Create WAF policy</span></span>

## <span data-ttu-id="f6191-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f6191-104">SYNTAX</span></span>

```
New-AzFrontDoorWafPolicy -ResourceGroupName <String> -Name <String> [-EnabledState <PSEnabledState>]
 [-Mode <String>] [-Customrule <PSCustomRule[]>] [-ManagedRule <PSManagedRule[]>] [-RedirectUrl <String>]
 [-CustomBlockResponseStatusCode <Int32>] [-CustomBlockResponseBody <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f6191-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f6191-105">DESCRIPTION</span></span>
<span data-ttu-id="f6191-106">Cmdleten **New-AzFrontDoorWafPolicy** skapar en ny Azure WAF-princip i den angivna resurs gruppen under aktuell prenumeration</span><span class="sxs-lookup"><span data-stu-id="f6191-106">The **New-AzFrontDoorWafPolicy** cmdlet creates a new Azure WAF policy in the specified resource group under current subscription</span></span>

## <span data-ttu-id="f6191-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f6191-107">EXAMPLES</span></span>

### <span data-ttu-id="f6191-108">Exempel 1: skapa WAF policy</span><span class="sxs-lookup"><span data-stu-id="f6191-108">Example 1: Create WAF policy</span></span>
```powershell
PS C:\> New-AzFrontDoorWafPolicy -Name $policyName -ResourceGroupName $resourceGroupName -Customrule $customRule1,$customRule2 -ManagedRule $managedRule1 -EnabledState Enabled -Mode Prevention -RedirectUrl "https://www.bing.com/" -CustomBlockResponseStatusCode 405 -CustomBlockResponseBody "<html><head><title>You are blocked!</title></head><body></body></html>"

Name         PolicyMode PolicyEnabledState RedirectUrl
----         ---------- ------------------ -----------
{policyName} Prevention            Enabled https://www.bing.com/
```

<span data-ttu-id="f6191-109">Skapa WAF policy</span><span class="sxs-lookup"><span data-stu-id="f6191-109">Create WAF policy</span></span>

## <span data-ttu-id="f6191-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f6191-110">PARAMETERS</span></span>

### <span data-ttu-id="f6191-111">-CustomBlockResponseBody</span><span class="sxs-lookup"><span data-stu-id="f6191-111">-CustomBlockResponseBody</span></span>
<span data-ttu-id="f6191-112">Anpassat svar</span><span class="sxs-lookup"><span data-stu-id="f6191-112">Custom Response Body</span></span>

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

### <span data-ttu-id="f6191-113">-CustomBlockResponseStatusCode</span><span class="sxs-lookup"><span data-stu-id="f6191-113">-CustomBlockResponseStatusCode</span></span>
<span data-ttu-id="f6191-114">Anpassad svars status kod</span><span class="sxs-lookup"><span data-stu-id="f6191-114">Custom Response Status Code</span></span>

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

### <span data-ttu-id="f6191-115">-Customrule</span><span class="sxs-lookup"><span data-stu-id="f6191-115">-Customrule</span></span>
<span data-ttu-id="f6191-116">Anpassade regler inuti policyn</span><span class="sxs-lookup"><span data-stu-id="f6191-116">Custom rules inside the policy</span></span>

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

### <span data-ttu-id="f6191-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6191-117">-DefaultProfile</span></span>
<span data-ttu-id="f6191-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f6191-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f6191-119">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="f6191-119">-EnabledState</span></span>
<span data-ttu-id="f6191-120">Om principen är aktiverat eller inte.</span><span class="sxs-lookup"><span data-stu-id="f6191-120">Whether the policy is in enabled state or disabled state.</span></span>
<span data-ttu-id="f6191-121">Möjliga värden är: ' disabled ', ' Enabled '</span><span class="sxs-lookup"><span data-stu-id="f6191-121">Possible values include: 'Disabled', 'Enabled'</span></span>

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

### <span data-ttu-id="f6191-122">-ManagedRule</span><span class="sxs-lookup"><span data-stu-id="f6191-122">-ManagedRule</span></span>
<span data-ttu-id="f6191-123">Hanterade regler inuti policyn</span><span class="sxs-lookup"><span data-stu-id="f6191-123">Managed rules inside the policy</span></span>

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

### <span data-ttu-id="f6191-124">-Mode</span><span class="sxs-lookup"><span data-stu-id="f6191-124">-Mode</span></span>
<span data-ttu-id="f6191-125">Beskriver om den är i identifierings läge eller i läget förhindra på princip nivå.</span><span class="sxs-lookup"><span data-stu-id="f6191-125">Describes if it is in detection mode  or prevention mode at policy level.</span></span>
<span data-ttu-id="f6191-126">Möjliga värden är: "förebygga", "identifiering"</span><span class="sxs-lookup"><span data-stu-id="f6191-126">Possible values include:'Prevention', 'Detection'</span></span>

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

### <span data-ttu-id="f6191-127">-Namn</span><span class="sxs-lookup"><span data-stu-id="f6191-127">-Name</span></span>
<span data-ttu-id="f6191-128">WebApplicationFireWallPolicy namn.</span><span class="sxs-lookup"><span data-stu-id="f6191-128">WebApplicationFireWallPolicy name.</span></span>

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

### <span data-ttu-id="f6191-129">-RedirectUrl</span><span class="sxs-lookup"><span data-stu-id="f6191-129">-RedirectUrl</span></span>
<span data-ttu-id="f6191-130">Omdirigera URL</span><span class="sxs-lookup"><span data-stu-id="f6191-130">Redirect URL</span></span>

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

### <span data-ttu-id="f6191-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f6191-131">-ResourceGroupName</span></span>
<span data-ttu-id="f6191-132">Resurs gruppens namn</span><span class="sxs-lookup"><span data-stu-id="f6191-132">The resource group name</span></span>

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

### <span data-ttu-id="f6191-133">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="f6191-133">-Confirm</span></span>
<span data-ttu-id="f6191-134">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="f6191-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f6191-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f6191-135">-WhatIf</span></span>
<span data-ttu-id="f6191-136">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="f6191-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f6191-137">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="f6191-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f6191-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6191-138">CommonParameters</span></span>
<span data-ttu-id="f6191-139">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f6191-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6191-140">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f6191-140">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6191-141">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f6191-141">INPUTS</span></span>

### <span data-ttu-id="f6191-142">Ingen</span><span class="sxs-lookup"><span data-stu-id="f6191-142">None</span></span>

## <span data-ttu-id="f6191-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f6191-143">OUTPUTS</span></span>

### <span data-ttu-id="f6191-144">Microsoft. Azure. commands. FrontDoor. Models. PSPolicy</span><span class="sxs-lookup"><span data-stu-id="f6191-144">Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy</span></span>

## <span data-ttu-id="f6191-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f6191-145">NOTES</span></span>

## <span data-ttu-id="f6191-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f6191-146">RELATED LINKS</span></span>

<span data-ttu-id="f6191-147">[Set-AzFrontDoorWafPolicy](./Set-AzFrontDoorWafPolicy.md) 
 [Get-AzFrontDoorWafPolicy](./Get-AzFrontDoorWafPolicy.md) 
 [Remove-AzFrontDoorWafPolicy](./Remove-AzFrontDoorWafPolicy.md) 
 [New-AzFrontDoorWafManagedRuleObject](./New-AzFrontDoorWafManagedRuleObject.md) 
 [New-AzFrontDoorWafCustomRuleObject](./New-AzFrontDoorWafManagedRuleObject.md)</span><span class="sxs-lookup"><span data-stu-id="f6191-147">[Set-AzFrontDoorWafPolicy](./Set-AzFrontDoorWafPolicy.md)
[Get-AzFrontDoorWafPolicy](./Get-AzFrontDoorWafPolicy.md)
[Remove-AzFrontDoorWafPolicy](./Remove-AzFrontDoorWafPolicy.md)
[New-AzFrontDoorWafManagedRuleObject](./New-AzFrontDoorWafManagedRuleObject.md)
[New-AzFrontDoorWafCustomRuleObject](./New-AzFrontDoorWafManagedRuleObject.md)</span></span>
