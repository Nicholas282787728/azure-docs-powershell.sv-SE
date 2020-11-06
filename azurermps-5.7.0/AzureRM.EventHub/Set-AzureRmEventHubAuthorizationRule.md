---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/set-azurermeventhubauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Set-AzureRmEventHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Set-AzureRmEventHubAuthorizationRule.md
ms.openlocfilehash: 4965fb6047ca31d2c5b70276a777235d2a3cb050
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93577222"
---
# <span data-ttu-id="bb504-101">Set-AzureRmEventHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="bb504-101">Set-AzureRmEventHubAuthorizationRule</span></span>

## <span data-ttu-id="bb504-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="bb504-102">SYNOPSIS</span></span>
<span data-ttu-id="bb504-103">Uppdaterar den angivna auktoriseringsregeln i en Händelsehubben.</span><span class="sxs-lookup"><span data-stu-id="bb504-103">Updates the specified authorization rule on an Event Hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bb504-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="bb504-104">SYNTAX</span></span>

### <span data-ttu-id="bb504-105">NamespaceAuthorizationRuleSet (standard)</span><span class="sxs-lookup"><span data-stu-id="bb504-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Set-AzureRmEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [[-InputObject] <PSSharedAccessAuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bb504-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="bb504-106">EventhubAuthorizationRuleSet</span></span>
```
Set-AzureRmEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [-Name] <String> [[-InputObject] <PSSharedAccessAuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bb504-107">AuthoRuleInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="bb504-107">AuthoRuleInputObjectSet</span></span>
```
Set-AzureRmEventHubAuthorizationRule [-ResourceGroupName] <String> [-Name] <String>
 [-InputObject] <PSSharedAccessAuthorizationRuleAttributes> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bb504-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="bb504-108">DESCRIPTION</span></span>
<span data-ttu-id="bb504-109">Set-AzureRmEventHubAuthorizationRule cmdlet uppdaterar den angivna auktoriseringsregeln för den angivna Händelsehubben.</span><span class="sxs-lookup"><span data-stu-id="bb504-109">The Set-AzureRmEventHubAuthorizationRule cmdlet updates the specified authorization rule on the given Event Hub.</span></span>

## <span data-ttu-id="bb504-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="bb504-110">EXAMPLES</span></span>

### <span data-ttu-id="bb504-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="bb504-111">Example 1</span></span>
```
PS C:\> Set-AzureRmEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -AuthorizationRuleName MyAuthRuleName -Rights @("Manage")
```

<span data-ttu-id="bb504-112">Uppdaterar \` MyAuthRuleName \` för att bevilja behörighet att hantera behörigheter till MyEventHubName för Event Hub som bevaras \` \` av namn området \` MyNamespaceName \` .</span><span class="sxs-lookup"><span data-stu-id="bb504-112">Updates the authorization rule \`MyAuthRuleName\` to grant Manage rights to the Event Hub \`MyEventHubName\`, scoped by the namespace \`MyNamespaceName\`.</span></span>

## <span data-ttu-id="bb504-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="bb504-113">PARAMETERS</span></span>

### <span data-ttu-id="bb504-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb504-114">-DefaultProfile</span></span>
<span data-ttu-id="bb504-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="bb504-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb504-116">-EventHub</span><span class="sxs-lookup"><span data-stu-id="bb504-116">-EventHub</span></span>
<span data-ttu-id="bb504-117">Namn på EventHub</span><span class="sxs-lookup"><span data-stu-id="bb504-117">EventHub Name</span></span>

```yaml
Type: String
Parameter Sets: EventhubAuthorizationRuleSet
Aliases: EventHubName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bb504-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bb504-118">-InputObject</span></span>
<span data-ttu-id="bb504-119">AuthorizationRule-objekt</span><span class="sxs-lookup"><span data-stu-id="bb504-119">AuthorizationRule Object</span></span>

```yaml
Type: PSSharedAccessAuthorizationRuleAttributes
Parameter Sets: NamespaceAuthorizationRuleSet, EventhubAuthorizationRuleSet
Aliases: AuthRuleObj

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

```yaml
Type: PSSharedAccessAuthorizationRuleAttributes
Parameter Sets: AuthoRuleInputObjectSet
Aliases: AuthRuleObj

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bb504-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="bb504-120">-Name</span></span>
<span data-ttu-id="bb504-121">AuthorizationRule namn</span><span class="sxs-lookup"><span data-stu-id="bb504-121">AuthorizationRule Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bb504-122">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="bb504-122">-Namespace</span></span>
<span data-ttu-id="bb504-123">Namn på namn området</span><span class="sxs-lookup"><span data-stu-id="bb504-123">Namespace Name</span></span>

```yaml
Type: String
Parameter Sets: NamespaceAuthorizationRuleSet, EventhubAuthorizationRuleSet
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bb504-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bb504-124">-ResourceGroupName</span></span>
<span data-ttu-id="bb504-125">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="bb504-125">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bb504-126">-Rättigheter</span><span class="sxs-lookup"><span data-stu-id="bb504-126">-Rights</span></span>
<span data-ttu-id="bb504-127">Rättigheter, till exempel @ ("lyssna", "Skicka", "hantera")</span><span class="sxs-lookup"><span data-stu-id="bb504-127">Rights, e.g. @("Listen","Send","Manage")</span></span>

```yaml
Type: String[]
Parameter Sets: NamespaceAuthorizationRuleSet, EventhubAuthorizationRuleSet
Aliases:
Accepted values: Listen, Send, Manage

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String[]
Parameter Sets: AuthoRulePropertiesSet
Aliases:
Accepted values: Listen, Send, Manage

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bb504-128">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="bb504-128">-Confirm</span></span>
<span data-ttu-id="bb504-129">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="bb504-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb504-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bb504-130">-WhatIf</span></span>
<span data-ttu-id="bb504-131">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="bb504-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bb504-132">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="bb504-132">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb504-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb504-133">CommonParameters</span></span>
<span data-ttu-id="bb504-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bb504-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="bb504-135">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bb504-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb504-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="bb504-136">INPUTS</span></span>

### <span data-ttu-id="bb504-137">System. String</span><span class="sxs-lookup"><span data-stu-id="bb504-137">System.String</span></span>
<span data-ttu-id="bb504-138">Microsoft. Azure. commands. EventHub. Models. PSSharedAccessAuthorizationRuleAttributes system. string []</span><span class="sxs-lookup"><span data-stu-id="bb504-138">Microsoft.Azure.Commands.EventHub.Models.PSSharedAccessAuthorizationRuleAttributes System.String[]</span></span>


## <span data-ttu-id="bb504-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="bb504-139">OUTPUTS</span></span>

### <span data-ttu-id="bb504-140">Microsoft. Azure. commands. EventHub. Models. PSSharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="bb504-140">Microsoft.Azure.Commands.EventHub.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>


## <span data-ttu-id="bb504-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="bb504-141">NOTES</span></span>

## <span data-ttu-id="bb504-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="bb504-142">RELATED LINKS</span></span>
