---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/remove-azeventhubiprule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubIPRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubIPRule.md
ms.openlocfilehash: 00213d4829d4b389f19a01ad9748517608657136
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98406528"
---
# <span data-ttu-id="e95b7-101">Remove-AzEventHubIPRule</span><span class="sxs-lookup"><span data-stu-id="e95b7-101">Remove-AzEventHubIPRule</span></span>

## <span data-ttu-id="e95b7-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e95b7-102">SYNOPSIS</span></span>
<span data-ttu-id="e95b7-103">Ta bort en enskild IP-regel till NetworkRuleSet för det angivna namn området</span><span class="sxs-lookup"><span data-stu-id="e95b7-103">Remove a single IP rule to the NetworkRuleSet of the given Namespace</span></span>

## <span data-ttu-id="e95b7-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e95b7-104">SYNTAX</span></span>

### <span data-ttu-id="e95b7-105">IPRulePropertiesParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="e95b7-105">IPRulePropertiesParameterSet (Default)</span></span>
```
Remove-AzEventHubIPRule [-ResourceGroupName] <String> [-Name] <String> [-IpMask] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e95b7-106">IPRuleInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e95b7-106">IPRuleInputObjectParameterSet</span></span>
```
Remove-AzEventHubIPRule [-ResourceGroupName] <String> [-Name] <String>
 [-IpRuleObject] <PSNWRuleSetIpRulesAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e95b7-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e95b7-107">DESCRIPTION</span></span>
<span data-ttu-id="e95b7-108">Ta bort en enskild IP-regel till NetworkRuleSet för det angivna namn området</span><span class="sxs-lookup"><span data-stu-id="e95b7-108">Remove a single IP rule to the NetworkRuleSet of the given Namespace</span></span>

## <span data-ttu-id="e95b7-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e95b7-109">EXAMPLES</span></span>

### <span data-ttu-id="e95b7-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="e95b7-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzEventHubIPRule -ResourceGroupName v-ajnavtest -Namespace Eventhub-Namespace1-2389 -IpMask "11.22.33.44"
```

<span data-ttu-id="e95b7-111">Tar bort IpMask för NetworkRuleSet för det givna namn området</span><span class="sxs-lookup"><span data-stu-id="e95b7-111">Removes IpMask of the NetworkRuleSet of the given namespace</span></span>

## <span data-ttu-id="e95b7-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e95b7-112">PARAMETERS</span></span>

### <span data-ttu-id="e95b7-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e95b7-113">-AsJob</span></span>
<span data-ttu-id="e95b7-114">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="e95b7-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e95b7-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e95b7-115">-DefaultProfile</span></span>
<span data-ttu-id="e95b7-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e95b7-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e95b7-117">-IpMask</span><span class="sxs-lookup"><span data-stu-id="e95b7-117">-IpMask</span></span>
<span data-ttu-id="e95b7-118">ID för under nätet</span><span class="sxs-lookup"><span data-stu-id="e95b7-118">Subnet Resource ID</span></span>

```yaml
Type: System.String
Parameter Sets: IPRulePropertiesParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e95b7-119">-IpRuleObject</span><span class="sxs-lookup"><span data-stu-id="e95b7-119">-IpRuleObject</span></span>
<span data-ttu-id="e95b7-120">IPRule-konfigurations objekt</span><span class="sxs-lookup"><span data-stu-id="e95b7-120">IPRule Configuration Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventHub.Models.PSNWRuleSetIpRulesAttributes
Parameter Sets: IPRuleInputObjectParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e95b7-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="e95b7-121">-Name</span></span>
<span data-ttu-id="e95b7-122">Namn på namn området</span><span class="sxs-lookup"><span data-stu-id="e95b7-122">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e95b7-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e95b7-123">-PassThru</span></span>
<span data-ttu-id="e95b7-124">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="e95b7-124">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="e95b7-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e95b7-125">-ResourceGroupName</span></span>
<span data-ttu-id="e95b7-126">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="e95b7-126">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e95b7-127">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="e95b7-127">-Confirm</span></span>
<span data-ttu-id="e95b7-128">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="e95b7-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e95b7-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e95b7-129">-WhatIf</span></span>
<span data-ttu-id="e95b7-130">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="e95b7-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e95b7-131">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="e95b7-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e95b7-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e95b7-132">CommonParameters</span></span>
<span data-ttu-id="e95b7-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e95b7-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="e95b7-134">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e95b7-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e95b7-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e95b7-135">INPUTS</span></span>

### <span data-ttu-id="e95b7-136">System. String</span><span class="sxs-lookup"><span data-stu-id="e95b7-136">System.String</span></span>

### <span data-ttu-id="e95b7-137">Microsoft. Azure. commands. EventHub. Models. PSNWRuleSetIpRulesAttributes</span><span class="sxs-lookup"><span data-stu-id="e95b7-137">Microsoft.Azure.Commands.EventHub.Models.PSNWRuleSetIpRulesAttributes</span></span>

## <span data-ttu-id="e95b7-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e95b7-138">OUTPUTS</span></span>

### <span data-ttu-id="e95b7-139">Microsoft. Azure. commands. EventHub. Models. PSNetworkRuleSetAttributes</span><span class="sxs-lookup"><span data-stu-id="e95b7-139">Microsoft.Azure.Commands.EventHub.Models.PSNetworkRuleSetAttributes</span></span>

## <span data-ttu-id="e95b7-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e95b7-140">NOTES</span></span>

## <span data-ttu-id="e95b7-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e95b7-141">RELATED LINKS</span></span>