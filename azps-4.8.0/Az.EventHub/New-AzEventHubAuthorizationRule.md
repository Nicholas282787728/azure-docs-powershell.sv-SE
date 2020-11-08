---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/new-azeventhubauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubAuthorizationRule.md
ms.openlocfilehash: 7a7c70dc9cf106aebc44df4733c4f8f9abaa78a6
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94262257"
---
# <span data-ttu-id="c4033-101">New-AzEventHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="c4033-101">New-AzEventHubAuthorizationRule</span></span>

## <span data-ttu-id="c4033-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c4033-102">SYNOPSIS</span></span>
<span data-ttu-id="c4033-103">Skapar en ny auktoriseringsregel för Event Hub för namn område eller eventhub.</span><span class="sxs-lookup"><span data-stu-id="c4033-103">Creates a new Event Hubs authorization rule for namespace or eventhub.</span></span>

## <span data-ttu-id="c4033-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c4033-104">SYNTAX</span></span>

### <span data-ttu-id="c4033-105">NamespaceAuthorizationRuleSet (standard)</span><span class="sxs-lookup"><span data-stu-id="c4033-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
New-AzEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 -Rights <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c4033-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="c4033-106">EventhubAuthorizationRuleSet</span></span>
```
New-AzEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [-Name] <String> -Rights <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c4033-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c4033-107">DESCRIPTION</span></span>
<span data-ttu-id="c4033-108">New-AzEventHubAuthorizationRule-cmdleten skapar en ny auktoriseringsregel för Event Hub.</span><span class="sxs-lookup"><span data-stu-id="c4033-108">The New-AzEventHubAuthorizationRule cmdlet creates a new Event Hubs authorization rule.</span></span>

## <span data-ttu-id="c4033-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c4033-109">EXAMPLES</span></span>

### <span data-ttu-id="c4033-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="c4033-110">Example 1</span></span>
```
PS C:\> New-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -AuthorizationRuleName MyAuthRuleName -Rights @("Listen","Send")
```

<span data-ttu-id="c4033-111">Skapar en auktoriseringsregel \` MyAuthRuleName \` tilldelar lyssnar och skickar rättigheter till namn områdets \` MyNamespaceName \` , med resurs grupp \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="c4033-111">Creates an authorization rule \`MyAuthRuleName\` granting Listen and Send rights to the namespace \`MyNamespaceName\`, with resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="c4033-112">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="c4033-112">Example 2</span></span>
```
PS C:\> New-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -AuthorizationRuleName MyAuthRuleName -Rights @("Listen","Send")
```

<span data-ttu-id="c4033-113">Skapar en auktoriseringsregel \` för MyAuthRuleName \` bevilja lyssnings-och behörighets rättigheter till \` MyEventHubName \` i namn området \` MyNamespaceName \` , med resurs grupp \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="c4033-113">Creates an authorization rule \`MyAuthRuleName\` granting Listen and Send rights to the Event Hub \`MyEventHubName\` in namespace \`MyNamespaceName\`, with resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="c4033-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c4033-114">PARAMETERS</span></span>

### <span data-ttu-id="c4033-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4033-115">-DefaultProfile</span></span>
<span data-ttu-id="c4033-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c4033-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c4033-117">-EventHub</span><span class="sxs-lookup"><span data-stu-id="c4033-117">-EventHub</span></span>
<span data-ttu-id="c4033-118">Namn på EventHub</span><span class="sxs-lookup"><span data-stu-id="c4033-118">EventHub Name</span></span>

```yaml
Type: System.String
Parameter Sets: EventhubAuthorizationRuleSet
Aliases: EventHubName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4033-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="c4033-119">-Name</span></span>
<span data-ttu-id="c4033-120">AuthorizationRule namn</span><span class="sxs-lookup"><span data-stu-id="c4033-120">AuthorizationRule Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4033-121">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="c4033-121">-Namespace</span></span>
<span data-ttu-id="c4033-122">Namn på namn området</span><span class="sxs-lookup"><span data-stu-id="c4033-122">Namespace Name</span></span>

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

### <span data-ttu-id="c4033-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c4033-123">-ResourceGroupName</span></span>
<span data-ttu-id="c4033-124">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="c4033-124">Resource Group Name</span></span>

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

### <span data-ttu-id="c4033-125">-Rättigheter</span><span class="sxs-lookup"><span data-stu-id="c4033-125">-Rights</span></span>
<span data-ttu-id="c4033-126">Rättigheter, till exempel "lyssna", "Skicka", "hantera"</span><span class="sxs-lookup"><span data-stu-id="c4033-126">Rights, e.g. "Listen","Send","Manage"</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:
Accepted values: Listen, Send, Manage

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4033-127">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="c4033-127">-Confirm</span></span>
<span data-ttu-id="c4033-128">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="c4033-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c4033-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c4033-129">-WhatIf</span></span>
<span data-ttu-id="c4033-130">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="c4033-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c4033-131">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="c4033-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c4033-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4033-132">CommonParameters</span></span>
<span data-ttu-id="c4033-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c4033-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4033-134">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c4033-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4033-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c4033-135">INPUTS</span></span>

### <span data-ttu-id="c4033-136">System. String</span><span class="sxs-lookup"><span data-stu-id="c4033-136">System.String</span></span>

### <span data-ttu-id="c4033-137">System. string []</span><span class="sxs-lookup"><span data-stu-id="c4033-137">System.String[]</span></span>

## <span data-ttu-id="c4033-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c4033-138">OUTPUTS</span></span>

### <span data-ttu-id="c4033-139">Microsoft. Azure. commands. EventHub. Models. PSSharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="c4033-139">Microsoft.Azure.Commands.EventHub.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="c4033-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c4033-140">NOTES</span></span>

## <span data-ttu-id="c4033-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c4033-141">RELATED LINKS</span></span>
