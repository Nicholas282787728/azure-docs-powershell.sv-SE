---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/new-azeventhubauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubAuthorizationRule.md
ms.openlocfilehash: 7a7c70dc9cf106aebc44df4733c4f8f9abaa78a6
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98411435"
---
# <span data-ttu-id="17174-101">New-AzEventHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="17174-101">New-AzEventHubAuthorizationRule</span></span>

## <span data-ttu-id="17174-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="17174-102">SYNOPSIS</span></span>
<span data-ttu-id="17174-103">Skapar en ny auktoriseringsregel för Event Hub för namn område eller eventhub.</span><span class="sxs-lookup"><span data-stu-id="17174-103">Creates a new Event Hubs authorization rule for namespace or eventhub.</span></span>

## <span data-ttu-id="17174-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="17174-104">SYNTAX</span></span>

### <span data-ttu-id="17174-105">NamespaceAuthorizationRuleSet (standard)</span><span class="sxs-lookup"><span data-stu-id="17174-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
New-AzEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 -Rights <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="17174-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="17174-106">EventhubAuthorizationRuleSet</span></span>
```
New-AzEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [-Name] <String> -Rights <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="17174-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="17174-107">DESCRIPTION</span></span>
<span data-ttu-id="17174-108">New-AzEventHubAuthorizationRule-cmdleten skapar en ny auktoriseringsregel för Event Hub.</span><span class="sxs-lookup"><span data-stu-id="17174-108">The New-AzEventHubAuthorizationRule cmdlet creates a new Event Hubs authorization rule.</span></span>

## <span data-ttu-id="17174-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="17174-109">EXAMPLES</span></span>

### <span data-ttu-id="17174-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="17174-110">Example 1</span></span>
```
PS C:\> New-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -AuthorizationRuleName MyAuthRuleName -Rights @("Listen","Send")
```

<span data-ttu-id="17174-111">Skapar en auktoriseringsregel \` MyAuthRuleName \` tilldelar lyssnar och skickar rättigheter till namn områdets \` MyNamespaceName \` , med resurs grupp \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="17174-111">Creates an authorization rule \`MyAuthRuleName\` granting Listen and Send rights to the namespace \`MyNamespaceName\`, with resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="17174-112">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="17174-112">Example 2</span></span>
```
PS C:\> New-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -AuthorizationRuleName MyAuthRuleName -Rights @("Listen","Send")
```

<span data-ttu-id="17174-113">Skapar en auktoriseringsregel \` för MyAuthRuleName \` bevilja lyssnings-och behörighets rättigheter till \` MyEventHubName \` i namn området \` MyNamespaceName \` , med resurs grupp \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="17174-113">Creates an authorization rule \`MyAuthRuleName\` granting Listen and Send rights to the Event Hub \`MyEventHubName\` in namespace \`MyNamespaceName\`, with resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="17174-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="17174-114">PARAMETERS</span></span>

### <span data-ttu-id="17174-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17174-115">-DefaultProfile</span></span>
<span data-ttu-id="17174-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="17174-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="17174-117">-EventHub</span><span class="sxs-lookup"><span data-stu-id="17174-117">-EventHub</span></span>
<span data-ttu-id="17174-118">Namn på EventHub</span><span class="sxs-lookup"><span data-stu-id="17174-118">EventHub Name</span></span>

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

### <span data-ttu-id="17174-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="17174-119">-Name</span></span>
<span data-ttu-id="17174-120">AuthorizationRule namn</span><span class="sxs-lookup"><span data-stu-id="17174-120">AuthorizationRule Name</span></span>

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

### <span data-ttu-id="17174-121">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="17174-121">-Namespace</span></span>
<span data-ttu-id="17174-122">Namn på namn området</span><span class="sxs-lookup"><span data-stu-id="17174-122">Namespace Name</span></span>

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

### <span data-ttu-id="17174-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="17174-123">-ResourceGroupName</span></span>
<span data-ttu-id="17174-124">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="17174-124">Resource Group Name</span></span>

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

### <span data-ttu-id="17174-125">-Rättigheter</span><span class="sxs-lookup"><span data-stu-id="17174-125">-Rights</span></span>
<span data-ttu-id="17174-126">Rättigheter, till exempel "lyssna", "Skicka", "hantera"</span><span class="sxs-lookup"><span data-stu-id="17174-126">Rights, e.g. "Listen","Send","Manage"</span></span>

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

### <span data-ttu-id="17174-127">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="17174-127">-Confirm</span></span>
<span data-ttu-id="17174-128">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="17174-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="17174-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="17174-129">-WhatIf</span></span>
<span data-ttu-id="17174-130">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="17174-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="17174-131">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="17174-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="17174-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17174-132">CommonParameters</span></span>
<span data-ttu-id="17174-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="17174-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17174-134">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="17174-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17174-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="17174-135">INPUTS</span></span>

### <span data-ttu-id="17174-136">System. String</span><span class="sxs-lookup"><span data-stu-id="17174-136">System.String</span></span>

### <span data-ttu-id="17174-137">System. string []</span><span class="sxs-lookup"><span data-stu-id="17174-137">System.String[]</span></span>

## <span data-ttu-id="17174-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="17174-138">OUTPUTS</span></span>

### <span data-ttu-id="17174-139">Microsoft. Azure. commands. EventHub. Models. PSSharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="17174-139">Microsoft.Azure.Commands.EventHub.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="17174-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="17174-140">NOTES</span></span>

## <span data-ttu-id="17174-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="17174-141">RELATED LINKS</span></span>
