---
external help file: Microsoft.Azure.Commands.FrontDoor.dll-Help.xml
Module Name: AzureRM.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.frontdoor/new-azurermfrontdoorfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/New-AzureRmFrontDoorFireWallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/New-AzureRmFrontDoorFireWallPolicy.md
ms.openlocfilehash: b18f17830dd08f95c3d887ce272ff31e080001a0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93585004"
---
# <span data-ttu-id="cab1c-101">New-AzureRmFrontDoorFireWallPolicy</span><span class="sxs-lookup"><span data-stu-id="cab1c-101">New-AzureRmFrontDoorFireWallPolicy</span></span>

## <span data-ttu-id="cab1c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="cab1c-102">SYNOPSIS</span></span>
<span data-ttu-id="cab1c-103">Skapa WAF policy</span><span class="sxs-lookup"><span data-stu-id="cab1c-103">Create WAF policy</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cab1c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="cab1c-104">SYNTAX</span></span>

```
New-AzureRmFrontDoorFireWallPolicy -ResourceGroupName <String> -Name <String> [-EnabledState <PSEnabledState>]
 [-Mode <PSMode>] [-Customrule <PSCustomRule[]>] [-ManagedRule <PSManagedRule[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cab1c-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="cab1c-105">DESCRIPTION</span></span>
<span data-ttu-id="cab1c-106">Cmdleten **New-AzureRmFrontDoorFireWallPolicy** skapar en ny Azure WAF-princip i den angivna resurs gruppen under aktuell prenumeration</span><span class="sxs-lookup"><span data-stu-id="cab1c-106">The **New-AzureRmFrontDoorFireWallPolicy** cmdlet creates a new Azure WAF policy in the specified resource group under current subscription</span></span>

## <span data-ttu-id="cab1c-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="cab1c-107">EXAMPLES</span></span>

### <span data-ttu-id="cab1c-108">Exempel 1: skapa WAF policy</span><span class="sxs-lookup"><span data-stu-id="cab1c-108">Example 1: Create WAF policy</span></span>
```powershell
PS C:\>  New-AzureRmFrontDoorFireWallPolicy -Name $Name -ResourceGroupName $resourceGroupName -Customrule $customRule1 -ManagedRule $managedRule1 -En
abledState Enabled -Mode Prevention


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

<span data-ttu-id="cab1c-109">Skapa WAF policy</span><span class="sxs-lookup"><span data-stu-id="cab1c-109">Create WAF policy</span></span>

## <span data-ttu-id="cab1c-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="cab1c-110">PARAMETERS</span></span>

### <span data-ttu-id="cab1c-111">-Customrule</span><span class="sxs-lookup"><span data-stu-id="cab1c-111">-Customrule</span></span>
<span data-ttu-id="cab1c-112">Anpassade regler inuti policyn</span><span class="sxs-lookup"><span data-stu-id="cab1c-112">Custom rules inside the policy</span></span>

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

### <span data-ttu-id="cab1c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cab1c-113">-DefaultProfile</span></span>
<span data-ttu-id="cab1c-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="cab1c-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cab1c-115">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="cab1c-115">-EnabledState</span></span>
<span data-ttu-id="cab1c-116">Om principen är aktiverat eller inte.</span><span class="sxs-lookup"><span data-stu-id="cab1c-116">Whether the policy is in enabled state or disabled state.</span></span>
<span data-ttu-id="cab1c-117">Möjliga värden är: ' disabled ', ' Enabled '</span><span class="sxs-lookup"><span data-stu-id="cab1c-117">Possible values include: 'Disabled', 'Enabled'</span></span>

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

### <span data-ttu-id="cab1c-118">-ManagedRule</span><span class="sxs-lookup"><span data-stu-id="cab1c-118">-ManagedRule</span></span>
<span data-ttu-id="cab1c-119">Hanterade regler inuti policyn</span><span class="sxs-lookup"><span data-stu-id="cab1c-119">Managed rules inside the policy</span></span>

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

### <span data-ttu-id="cab1c-120">-Mode</span><span class="sxs-lookup"><span data-stu-id="cab1c-120">-Mode</span></span>
<span data-ttu-id="cab1c-121">Beskriver om den är i identifierings läge eller i läget förhindra på princip nivå.</span><span class="sxs-lookup"><span data-stu-id="cab1c-121">Describes if it is in detection mode  or prevention mode at policy level.</span></span>
<span data-ttu-id="cab1c-122">Möjliga värden är: "förebygga", "identifiering"</span><span class="sxs-lookup"><span data-stu-id="cab1c-122">Possible values include:'Prevention', 'Detection'</span></span>

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

### <span data-ttu-id="cab1c-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="cab1c-123">-Name</span></span>
<span data-ttu-id="cab1c-124">WebApplicationFireWallPolicy namn.</span><span class="sxs-lookup"><span data-stu-id="cab1c-124">WebApplicationFireWallPolicy name.</span></span>

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

### <span data-ttu-id="cab1c-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cab1c-125">-ResourceGroupName</span></span>
<span data-ttu-id="cab1c-126">Resurs gruppens namn</span><span class="sxs-lookup"><span data-stu-id="cab1c-126">The resource group name</span></span>

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

### <span data-ttu-id="cab1c-127">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="cab1c-127">-Confirm</span></span>
<span data-ttu-id="cab1c-128">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="cab1c-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cab1c-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cab1c-129">-WhatIf</span></span>
<span data-ttu-id="cab1c-130">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="cab1c-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cab1c-131">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="cab1c-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cab1c-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cab1c-132">CommonParameters</span></span>
<span data-ttu-id="cab1c-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cab1c-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cab1c-134">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cab1c-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cab1c-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="cab1c-135">INPUTS</span></span>

### <span data-ttu-id="cab1c-136">System. String</span><span class="sxs-lookup"><span data-stu-id="cab1c-136">System.String</span></span>

## <span data-ttu-id="cab1c-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="cab1c-137">OUTPUTS</span></span>

### <span data-ttu-id="cab1c-138">Microsoft. Azure. commands. FrontDoor. Models. PSPolicy</span><span class="sxs-lookup"><span data-stu-id="cab1c-138">Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy</span></span>

## <span data-ttu-id="cab1c-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="cab1c-139">NOTES</span></span>

## <span data-ttu-id="cab1c-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="cab1c-140">RELATED LINKS</span></span>

<span data-ttu-id="cab1c-141">[Set-AzureRmFrontDoorFireWallPolicy](./Set-AzureRmFrontDoorFireWallPolicy.md) 
 [Get-AzureRmFrontDoorFireWallPolicy](./Get-AzureRmFrontDoorFireWallPolicy.md) 
 [Remove-AzureRmFrontDoorFireWallPolicy](./Remove-AzureRmFrontDoorFireWallPolicy.md) 
 [New-AzureRmFrontDoorManagedRuleObject](./New-AzureRmFrontDoorManagedRuleObject.md) 
 [New-AzureRmFrontDoorCustomRuleObject](./New-AzureRmFrontDoorManagedRuleObject.md)</span><span class="sxs-lookup"><span data-stu-id="cab1c-141">[Set-AzureRmFrontDoorFireWallPolicy](./Set-AzureRmFrontDoorFireWallPolicy.md)
[Get-AzureRmFrontDoorFireWallPolicy](./Get-AzureRmFrontDoorFireWallPolicy.md)
[Remove-AzureRmFrontDoorFireWallPolicy](./Remove-AzureRmFrontDoorFireWallPolicy.md)
[New-AzureRmFrontDoorManagedRuleObject](./New-AzureRmFrontDoorManagedRuleObject.md)
[New-AzureRmFrontDoorCustomRuleObject](./New-AzureRmFrontDoorManagedRuleObject.md)</span></span>
