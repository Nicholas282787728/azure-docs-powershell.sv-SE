---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusNamespaceAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusNamespaceAuthorizationRule.md
ms.openlocfilehash: a56f9b27e19868d22eed94fbcf7717fbe1c68b39
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757746"
---
# <span data-ttu-id="95708-101">Set-AzureRmServiceBusNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="95708-101">Set-AzureRmServiceBusNamespaceAuthorizationRule</span></span>

## <span data-ttu-id="95708-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="95708-102">SYNOPSIS</span></span>
<span data-ttu-id="95708-103">Uppdaterar den angivna beskrivningen av auktoriseringsregeln för det angivna Service Bus-namnområdet.</span><span class="sxs-lookup"><span data-stu-id="95708-103">Updates the specified authorization rule description for the given Service Bus namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="95708-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="95708-104">SYNTAX</span></span>

```
Set-AzureRmServiceBusNamespaceAuthorizationRule [-ResourceGroup] <String> -Namespace <String>
 -InputObj <SharedAccessAuthorizationRuleAttributes> [-Name <String>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="95708-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="95708-105">DESCRIPTION</span></span>
<span data-ttu-id="95708-106">Cmdleten **set-AzureRmServiceBusNamespaceAuthorizationRule** uppdaterar beskrivningen för den angivna auktoriseringsregeln i angivet Service Bus-namnområde.</span><span class="sxs-lookup"><span data-stu-id="95708-106">The **Set-AzureRmServiceBusNamespaceAuthorizationRule** cmdlet updates the description for the specified authorization rule in the given Service Bus namespace.</span></span>

## <span data-ttu-id="95708-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="95708-107">EXAMPLES</span></span>

### <span data-ttu-id="95708-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="95708-108">Example 1</span></span>
```
PS C:\> $authRuleObj = Get-AzureRmServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -AuthorizationRuleName AuthoRule1

PS C:\> $authRuleObj.Rights.Remove("Manage")

PS C:\> Set-AzureRmServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -AuthRuleObj $authRuleObj
```

<span data-ttu-id="95708-109">Tar bort **Hantera** från åtkomst rättigheterna för auktoriseringsregeln `AuthoRule1` i namn området `SB-Example1` .</span><span class="sxs-lookup"><span data-stu-id="95708-109">Removes **Manage** from the access rights of the authorization rule `AuthoRule1` in namespace `SB-Example1`.</span></span>

## <span data-ttu-id="95708-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="95708-110">PARAMETERS</span></span>

### <span data-ttu-id="95708-111">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="95708-111">-ResourceGroup</span></span>
<span data-ttu-id="95708-112">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="95708-112">The name of the resource group.</span></span>

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

### <span data-ttu-id="95708-113">-Rättigheter</span><span class="sxs-lookup"><span data-stu-id="95708-113">-Rights</span></span>
<span data-ttu-id="95708-114">Behörighet till exempel @ ("lyssna", "Skicka", "hantera").</span><span class="sxs-lookup"><span data-stu-id="95708-114">Rights; for example @("Listen","Send","Manage").</span></span> <span data-ttu-id="95708-115">Obligatoriskt om **AuthruleObj** inte har angetts.</span><span class="sxs-lookup"><span data-stu-id="95708-115">Required if **AuthruleObj** is not specified.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95708-116">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="95708-116">-Confirm</span></span>
<span data-ttu-id="95708-117">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="95708-117">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95708-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="95708-118">-WhatIf</span></span>
<span data-ttu-id="95708-119">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="95708-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="95708-120">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="95708-120">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95708-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95708-121">-DefaultProfile</span></span>
<span data-ttu-id="95708-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="95708-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="95708-123">-InputObj</span><span class="sxs-lookup"><span data-stu-id="95708-123">-InputObj</span></span>
<span data-ttu-id="95708-124">ServiceBus NameSpace AuthorizationRule objekt.</span><span class="sxs-lookup"><span data-stu-id="95708-124">ServiceBus NameSpace AuthorizationRule Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.SharedAccessAuthorizationRuleAttributes
Parameter Sets: (All)
Aliases: AuthRuleObj

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95708-125">-Namn</span><span class="sxs-lookup"><span data-stu-id="95708-125">-Name</span></span>
<span data-ttu-id="95708-126">AuthorizationRule-namn – obligatoriskt om ' AuthruleObj ' inte har angetts.</span><span class="sxs-lookup"><span data-stu-id="95708-126">AuthorizationRule Name - Required if 'AuthruleObj' not specified.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95708-127">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="95708-127">-Namespace</span></span>
<span data-ttu-id="95708-128">Namn områdes namnet ServiceBus.</span><span class="sxs-lookup"><span data-stu-id="95708-128">ServiceBus Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95708-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95708-129">CommonParameters</span></span>
<span data-ttu-id="95708-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="95708-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95708-131">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="95708-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95708-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="95708-132">INPUTS</span></span>

### <span data-ttu-id="95708-133">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="95708-133">-ResourceGroup</span></span>
 <span data-ttu-id="95708-134">System. String</span><span class="sxs-lookup"><span data-stu-id="95708-134">System.String</span></span>

### <span data-ttu-id="95708-135">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="95708-135">-NamespaceName</span></span>
 <span data-ttu-id="95708-136">System. String</span><span class="sxs-lookup"><span data-stu-id="95708-136">System.String</span></span>

### <span data-ttu-id="95708-137">-AuthRuleObj</span><span class="sxs-lookup"><span data-stu-id="95708-137">-AuthRuleObj</span></span>
 <span data-ttu-id="95708-138">Microsoft. Azure. commands. ServiceBus. Models. SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="95708-138">Microsoft.Azure.Commands.ServiceBus.Models.SharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="95708-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="95708-139">OUTPUTS</span></span>

### <span data-ttu-id="95708-140">Microsoft. Azure. commands. ServiceBus. Models. SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="95708-140">Microsoft.Azure.Commands.ServiceBus.Models.SharedAccessAuthorizationRuleAttributes</span></span>
<span data-ttu-id="95708-141">ID:/subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1/AuthorizationRules/AuthoRule1 typ: Microsoft. ServiceBus/AuthorizationRules namn: AuthoRule1 Location: tagg: Rights: {Listener, Send}</span><span class="sxs-lookup"><span data-stu-id="95708-141">Id       : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1/AuthorizationRules/AuthoRule1 Type     : Microsoft.ServiceBus/AuthorizationRules Name     : AuthoRule1 Location : Tags     : Rights   : {Listen, Send}</span></span>

## <span data-ttu-id="95708-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="95708-142">NOTES</span></span>

## <span data-ttu-id="95708-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="95708-143">RELATED LINKS</span></span>

