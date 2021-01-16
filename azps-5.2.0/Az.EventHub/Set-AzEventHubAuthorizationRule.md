---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/set-azeventhubauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubAuthorizationRule.md
ms.openlocfilehash: 862b6f295a997b2027520a3f9c6a9f4f9cfb5ae9
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98406504"
---
# <span data-ttu-id="8a962-101">Set-AzEventHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="8a962-101">Set-AzEventHubAuthorizationRule</span></span>

## <span data-ttu-id="8a962-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8a962-102">SYNOPSIS</span></span>
<span data-ttu-id="8a962-103">Uppdaterar den angivna auktoriseringsregeln i en Händelsehubben.</span><span class="sxs-lookup"><span data-stu-id="8a962-103">Updates the specified authorization rule on an Event Hub.</span></span>

## <span data-ttu-id="8a962-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8a962-104">SYNTAX</span></span>

### <span data-ttu-id="8a962-105">NamespaceAuthorizationRuleSet (standard)</span><span class="sxs-lookup"><span data-stu-id="8a962-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Set-AzEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [[-InputObject] <PSSharedAccessAuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8a962-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="8a962-106">EventhubAuthorizationRuleSet</span></span>
```
Set-AzEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [-Name] <String> [[-InputObject] <PSSharedAccessAuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8a962-107">AuthoRuleInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="8a962-107">AuthoRuleInputObjectSet</span></span>
```
Set-AzEventHubAuthorizationRule [-ResourceGroupName] <String> [-Name] <String>
 [-InputObject] <PSSharedAccessAuthorizationRuleAttributes> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8a962-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8a962-108">DESCRIPTION</span></span>
<span data-ttu-id="8a962-109">Set-AzEventHubAuthorizationRule cmdlet uppdaterar den angivna auktoriseringsregeln för den angivna Händelsehubben.</span><span class="sxs-lookup"><span data-stu-id="8a962-109">The Set-AzEventHubAuthorizationRule cmdlet updates the specified authorization rule on the given Event Hub.</span></span>

## <span data-ttu-id="8a962-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8a962-110">EXAMPLES</span></span>

### <span data-ttu-id="8a962-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="8a962-111">Example 1</span></span>
```
PS C:\> Set-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -AuthorizationRuleName MyAuthRuleName -Rights @("Manage")
```

<span data-ttu-id="8a962-112">Uppdaterar \` MyAuthRuleName \` för att bevilja behörighet att hantera behörigheter till MyEventHubName för Event Hub som bevaras \` \` av namn området \` MyNamespaceName \` .</span><span class="sxs-lookup"><span data-stu-id="8a962-112">Updates the authorization rule \`MyAuthRuleName\` to grant Manage rights to the Event Hub \`MyEventHubName\`, scoped by the namespace \`MyNamespaceName\`.</span></span>

## <span data-ttu-id="8a962-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8a962-113">PARAMETERS</span></span>

### <span data-ttu-id="8a962-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a962-114">-DefaultProfile</span></span>
<span data-ttu-id="8a962-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="8a962-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8a962-116">-EventHub</span><span class="sxs-lookup"><span data-stu-id="8a962-116">-EventHub</span></span>
<span data-ttu-id="8a962-117">Namn på EventHub</span><span class="sxs-lookup"><span data-stu-id="8a962-117">EventHub Name</span></span>

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

### <span data-ttu-id="8a962-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8a962-118">-InputObject</span></span>
<span data-ttu-id="8a962-119">AuthorizationRule-objekt</span><span class="sxs-lookup"><span data-stu-id="8a962-119">AuthorizationRule Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventHub.Models.PSSharedAccessAuthorizationRuleAttributes
Parameter Sets: NamespaceAuthorizationRuleSet, EventhubAuthorizationRuleSet
Aliases: AuthRuleObj

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.EventHub.Models.PSSharedAccessAuthorizationRuleAttributes
Parameter Sets: AuthoRuleInputObjectSet
Aliases: AuthRuleObj

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8a962-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="8a962-120">-Name</span></span>
<span data-ttu-id="8a962-121">AuthorizationRule namn</span><span class="sxs-lookup"><span data-stu-id="8a962-121">AuthorizationRule Name</span></span>

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

### <span data-ttu-id="8a962-122">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="8a962-122">-Namespace</span></span>
<span data-ttu-id="8a962-123">Namn på namn området</span><span class="sxs-lookup"><span data-stu-id="8a962-123">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: NamespaceAuthorizationRuleSet, EventhubAuthorizationRuleSet
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8a962-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8a962-124">-ResourceGroupName</span></span>
<span data-ttu-id="8a962-125">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="8a962-125">Resource Group Name</span></span>

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

### <span data-ttu-id="8a962-126">-Rättigheter</span><span class="sxs-lookup"><span data-stu-id="8a962-126">-Rights</span></span>
<span data-ttu-id="8a962-127">Rättigheter, till exempel @ ("lyssna", "Skicka", "hantera")</span><span class="sxs-lookup"><span data-stu-id="8a962-127">Rights, e.g. @("Listen","Send","Manage")</span></span>

```yaml
Type: System.String[]
Parameter Sets: NamespaceAuthorizationRuleSet, EventhubAuthorizationRuleSet
Aliases:
Accepted values: Listen, Send, Manage

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8a962-128">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="8a962-128">-Confirm</span></span>
<span data-ttu-id="8a962-129">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="8a962-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8a962-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8a962-130">-WhatIf</span></span>
<span data-ttu-id="8a962-131">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="8a962-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8a962-132">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="8a962-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8a962-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a962-133">CommonParameters</span></span>
<span data-ttu-id="8a962-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8a962-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a962-135">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8a962-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a962-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8a962-136">INPUTS</span></span>

### <span data-ttu-id="8a962-137">System. String</span><span class="sxs-lookup"><span data-stu-id="8a962-137">System.String</span></span>

### <span data-ttu-id="8a962-138">Microsoft. Azure. commands. EventHub. Models. PSSharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="8a962-138">Microsoft.Azure.Commands.EventHub.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>

### <span data-ttu-id="8a962-139">System. string []</span><span class="sxs-lookup"><span data-stu-id="8a962-139">System.String[]</span></span>

## <span data-ttu-id="8a962-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8a962-140">OUTPUTS</span></span>

### <span data-ttu-id="8a962-141">Microsoft. Azure. commands. EventHub. Models. PSSharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="8a962-141">Microsoft.Azure.Commands.EventHub.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="8a962-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8a962-142">NOTES</span></span>

## <span data-ttu-id="8a962-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8a962-143">RELATED LINKS</span></span>
