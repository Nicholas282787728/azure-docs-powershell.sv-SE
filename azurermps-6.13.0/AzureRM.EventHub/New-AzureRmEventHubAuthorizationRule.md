---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/new-azurermeventhubauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubAuthorizationRule.md
ms.openlocfilehash: 63da2be82f8af6339a68eab580c6871b05f2d884
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757361"
---
# <span data-ttu-id="13311-101">New-AzureRmEventHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="13311-101">New-AzureRmEventHubAuthorizationRule</span></span>

## <span data-ttu-id="13311-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="13311-102">SYNOPSIS</span></span>
<span data-ttu-id="13311-103">Skapar en ny auktoriseringsregel för Event Hub för namn område eller eventhub.</span><span class="sxs-lookup"><span data-stu-id="13311-103">Creates a new Event Hubs authorization rule for namespace or eventhub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="13311-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="13311-104">SYNTAX</span></span>

### <span data-ttu-id="13311-105">NamespaceAuthorizationRuleSet (standard)</span><span class="sxs-lookup"><span data-stu-id="13311-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
New-AzureRmEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 -Rights <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="13311-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="13311-106">EventhubAuthorizationRuleSet</span></span>
```
New-AzureRmEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [-Name] <String> -Rights <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="13311-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="13311-107">DESCRIPTION</span></span>
<span data-ttu-id="13311-108">New-AzureRmEventHubAuthorizationRule-cmdleten skapar en ny auktoriseringsregel för Event Hub.</span><span class="sxs-lookup"><span data-stu-id="13311-108">The New-AzureRmEventHubAuthorizationRule cmdlet creates a new Event Hubs authorization rule.</span></span>

## <span data-ttu-id="13311-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="13311-109">EXAMPLES</span></span>

### <span data-ttu-id="13311-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="13311-110">Example 1</span></span>
```
PS C:\> New-AzureRmEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -AuthorizationRuleName MyAuthRuleName -Rights @("Listen","Send")
```

<span data-ttu-id="13311-111">Skapar en auktoriseringsregel \` MyAuthRuleName \` tilldelar lyssnar och skickar rättigheter till namn områdets \` MyNamespaceName \` , med resurs grupp \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="13311-111">Creates an authorization rule \`MyAuthRuleName\` granting Listen and Send rights to the namespace \`MyNamespaceName\`, with resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="13311-112">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="13311-112">Example 2</span></span>
```
PS C:\> New-AzureRmEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -AuthorizationRuleName MyAuthRuleName -Rights @("Listen","Send")
```

<span data-ttu-id="13311-113">Skapar en auktoriseringsregel \` för MyAuthRuleName \` bevilja lyssnings-och behörighets rättigheter till \` MyEventHubName \` i namn området \` MyNamespaceName \` , med resurs grupp \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="13311-113">Creates an authorization rule \`MyAuthRuleName\` granting Listen and Send rights to the Event Hub \`MyEventHubName\` in namespace \`MyNamespaceName\`, with resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="13311-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="13311-114">PARAMETERS</span></span>

### <span data-ttu-id="13311-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13311-115">-DefaultProfile</span></span>
<span data-ttu-id="13311-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="13311-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="13311-117">-EventHub</span><span class="sxs-lookup"><span data-stu-id="13311-117">-EventHub</span></span>
<span data-ttu-id="13311-118">Namn på EventHub</span><span class="sxs-lookup"><span data-stu-id="13311-118">EventHub Name</span></span>

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

### <span data-ttu-id="13311-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="13311-119">-Name</span></span>
<span data-ttu-id="13311-120">AuthorizationRule namn</span><span class="sxs-lookup"><span data-stu-id="13311-120">AuthorizationRule Name</span></span>

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

### <span data-ttu-id="13311-121">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="13311-121">-Namespace</span></span>
<span data-ttu-id="13311-122">Namn på namn området</span><span class="sxs-lookup"><span data-stu-id="13311-122">Namespace Name</span></span>

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

### <span data-ttu-id="13311-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="13311-123">-ResourceGroupName</span></span>
<span data-ttu-id="13311-124">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="13311-124">Resource Group Name</span></span>

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

### <span data-ttu-id="13311-125">-Rättigheter</span><span class="sxs-lookup"><span data-stu-id="13311-125">-Rights</span></span>
<span data-ttu-id="13311-126">Rättigheter, till exempel "lyssna", "Skicka", "hantera"</span><span class="sxs-lookup"><span data-stu-id="13311-126">Rights, e.g. "Listen","Send","Manage"</span></span>

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

### <span data-ttu-id="13311-127">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="13311-127">-Confirm</span></span>
<span data-ttu-id="13311-128">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="13311-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="13311-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="13311-129">-WhatIf</span></span>
<span data-ttu-id="13311-130">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="13311-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="13311-131">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="13311-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="13311-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13311-132">CommonParameters</span></span>
<span data-ttu-id="13311-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="13311-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13311-134">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="13311-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13311-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="13311-135">INPUTS</span></span>

### <span data-ttu-id="13311-136">System. String</span><span class="sxs-lookup"><span data-stu-id="13311-136">System.String</span></span>

### <span data-ttu-id="13311-137">System. string []</span><span class="sxs-lookup"><span data-stu-id="13311-137">System.String[]</span></span>

## <span data-ttu-id="13311-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="13311-138">OUTPUTS</span></span>

### <span data-ttu-id="13311-139">Microsoft. Azure. commands. EventHub. Models. PSSharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="13311-139">Microsoft.Azure.Commands.EventHub.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="13311-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="13311-140">NOTES</span></span>

## <span data-ttu-id="13311-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="13311-141">RELATED LINKS</span></span>
