---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/get-azurermeventhubauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubAuthorizationRule.md
ms.openlocfilehash: 70b5ac9eb40bf6c50ebb6d09849e8185c23927e4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576282"
---
# <span data-ttu-id="5f415-101">Get-AzureRmEventHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="5f415-101">Get-AzureRmEventHubAuthorizationRule</span></span>

## <span data-ttu-id="5f415-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5f415-102">SYNOPSIS</span></span>
<span data-ttu-id="5f415-103">Hämtar information om en auktoriseringsregel eller hämtar en lista över auktoriseringsregler.</span><span class="sxs-lookup"><span data-stu-id="5f415-103">Gets the details of an authorization rule, or gets a list of authorization rules.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5f415-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5f415-104">SYNTAX</span></span>

### <span data-ttu-id="5f415-105">NamespaceAuthorizationRuleSet (standard)</span><span class="sxs-lookup"><span data-stu-id="5f415-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzureRmEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5f415-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="5f415-106">EventhubAuthorizationRuleSet</span></span>
```
Get-AzureRmEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Eventhub] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5f415-107">AliasAuthoRuleSet</span><span class="sxs-lookup"><span data-stu-id="5f415-107">AliasAuthoRuleSet</span></span>
```
Get-AzureRmEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-AliasName] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5f415-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5f415-108">DESCRIPTION</span></span>
<span data-ttu-id="5f415-109">Get-AzureRmEventHubAuthorizationRule-cmdleten får antingen information om en auktoriseringsregel eller en lista över alla auktoriseringsregler för en viss händelsehubben.</span><span class="sxs-lookup"><span data-stu-id="5f415-109">The Get-AzureRmEventHubAuthorizationRule cmdlet gets either the details of an authorization rule, or a list of all authorization rules for a specified Event Hub.</span></span>
<span data-ttu-id="5f415-110">Om namnet på en auktoriseringsregel tillhandahålls returneras informationen om den enskilda auktoriseringsregeln.</span><span class="sxs-lookup"><span data-stu-id="5f415-110">If the name of an authorization rule is provided, the details of that single authorization rule are returned.</span></span>
<span data-ttu-id="5f415-111">Om namnet på en auktoriseringsregel inte anges returneras en lista över alla auktoriseringsregler för den angivna Händelsehubben.</span><span class="sxs-lookup"><span data-stu-id="5f415-111">If the name of an authorization rule is not provided, a list of all authorization rules for the specified Event Hub is returned.</span></span>
<span data-ttu-id="5f415-112">Om (återställning efter katastrof) anges, returneras informationen om auktoriseringsregeln för namn området för konfigurerade alias.</span><span class="sxs-lookup"><span data-stu-id="5f415-112">If (Disaster Recovery) Alias name provided, the details of authorization rule of the Namespace for Alias configured is returned.</span></span>

## <span data-ttu-id="5f415-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5f415-113">EXAMPLES</span></span>

### <span data-ttu-id="5f415-114">Exempel på 1,0-AuthorizationRule för namespace</span><span class="sxs-lookup"><span data-stu-id="5f415-114">Example 1.0 - AuthorizationRule for namespace</span></span>
```
PS C:\> Get-AzureRmEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Name MyAuthRuleName
```

<span data-ttu-id="5f415-115">Hämtar auktoriseringsregeln \` MyAuthRuleName \` i namn området \` MyNamespaceName \` .</span><span class="sxs-lookup"><span data-stu-id="5f415-115">Gets the authorization rule \`MyAuthRuleName\` in the namespace \`MyNamespaceName\`.</span></span>

### <span data-ttu-id="5f415-116">Exempel på 1,1-AuthorizationRules för namespace</span><span class="sxs-lookup"><span data-stu-id="5f415-116">Example 1.1 - AuthorizationRules for namespace</span></span>
```
PS C:\> Get-AzureRmEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName
```

<span data-ttu-id="5f415-117">Hämtar en lista över alla auktoriseringsregler i namn området \` MyNamespaceName \` .</span><span class="sxs-lookup"><span data-stu-id="5f415-117">Gets a list of all authorization rules in the namespace \`MyNamespaceName\`.</span></span>

### <span data-ttu-id="5f415-118">Exempel 2,0-AuthorizationRule för EventHub</span><span class="sxs-lookup"><span data-stu-id="5f415-118">Example 2.0 - AuthorizationRule for EventHub</span></span>
```
PS C:\> Get-AzureRmEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -Name MyAuthRuleName
```

<span data-ttu-id="5f415-119">Hämtar auktoriseringsregeln \` MyAuthRuleName \` i \` MyEventHubName \` som befinner sig i namn området \` MyNamespaceName \` .</span><span class="sxs-lookup"><span data-stu-id="5f415-119">Gets the authorization rule \`MyAuthRuleName\` in the Event Hub \`MyEventHubName\`, which is scoped by the namespace \`MyNamespaceName\`.</span></span>

### <span data-ttu-id="5f415-120">Exempel 2,1-AuthorizationRules för EventHub</span><span class="sxs-lookup"><span data-stu-id="5f415-120">Example 2.1 - AuthorizationRules for EventHub</span></span>
```
PS C:\> Get-AzureRmEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName
```

<span data-ttu-id="5f415-121">Hämtar en lista med auktoriseringsregler i händelsehubben \` MyEventHubName \` , som befinner sig i namn områdets \` MyNamespaceName \` .</span><span class="sxs-lookup"><span data-stu-id="5f415-121">Gets list authorization rules in the Event Hub \`MyEventHubName\`, which is scoped by the namespace \`MyNamespaceName\`.</span></span>

### <span data-ttu-id="5f415-122">Exempel 3,0-AuthorizationRule för alias (återställnings konfiguration)</span><span class="sxs-lookup"><span data-stu-id="5f415-122">Example 3.0 - AuthorizationRule for Alias (GeoRecovery Configuration)</span></span>
```
PS C:\> Get-AzureRmEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -AliasName MyAliasNameName -Name MyAuthRuleName
```

<span data-ttu-id="5f415-123">Hämtar auktoriseringsregeln \` MyAuthRuleName \` i namn området \` MyNamespaceName \` .</span><span class="sxs-lookup"><span data-stu-id="5f415-123">Gets the authorization rule \`MyAuthRuleName\` in the namespace \`MyNamespaceName\`.</span></span>

### <span data-ttu-id="5f415-124">Exempel 3,1-AuthorizationRules för alias (återställnings konfiguration)</span><span class="sxs-lookup"><span data-stu-id="5f415-124">Example 3.1 -AuthorizationRules for Alias (GeoRecovery Configuration)</span></span>
```
PS C:\> Get-AzureRmEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -AliasName MyAliasNameName
```

<span data-ttu-id="5f415-125">Hämtar en lista över alla \` MyAuthRuleName \` i namn området \` MyNamespaceName \` .</span><span class="sxs-lookup"><span data-stu-id="5f415-125">Gets a list of all authorization rule \`MyAuthRuleName\` in the namespace \`MyNamespaceName\`.</span></span>

## <span data-ttu-id="5f415-126">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5f415-126">PARAMETERS</span></span>

### <span data-ttu-id="5f415-127">-AliasName</span><span class="sxs-lookup"><span data-stu-id="5f415-127">-AliasName</span></span>
<span data-ttu-id="5f415-128">Aliasnamn</span><span class="sxs-lookup"><span data-stu-id="5f415-128">Alias Name</span></span>

```yaml
Type: System.String
Parameter Sets: AliasAuthoRuleSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5f415-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f415-129">-DefaultProfile</span></span>
<span data-ttu-id="5f415-130">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="5f415-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5f415-131">-Eventhub</span><span class="sxs-lookup"><span data-stu-id="5f415-131">-Eventhub</span></span>
<span data-ttu-id="5f415-132">Namn på Eventhub</span><span class="sxs-lookup"><span data-stu-id="5f415-132">Eventhub Name</span></span>

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

### <span data-ttu-id="5f415-133">-Namn</span><span class="sxs-lookup"><span data-stu-id="5f415-133">-Name</span></span>
<span data-ttu-id="5f415-134">AuthorizationRule namn</span><span class="sxs-lookup"><span data-stu-id="5f415-134">AuthorizationRule Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5f415-135">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="5f415-135">-Namespace</span></span>
<span data-ttu-id="5f415-136">Namn på namn området</span><span class="sxs-lookup"><span data-stu-id="5f415-136">Namespace Name</span></span>

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

### <span data-ttu-id="5f415-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5f415-137">-ResourceGroupName</span></span>
<span data-ttu-id="5f415-138">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="5f415-138">Resource Group Name</span></span>

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

### <span data-ttu-id="5f415-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f415-139">CommonParameters</span></span>
<span data-ttu-id="5f415-140">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5f415-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f415-141">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5f415-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f415-142">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5f415-142">INPUTS</span></span>

### <span data-ttu-id="5f415-143">System. String</span><span class="sxs-lookup"><span data-stu-id="5f415-143">System.String</span></span>

## <span data-ttu-id="5f415-144">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5f415-144">OUTPUTS</span></span>

### <span data-ttu-id="5f415-145">Microsoft. Azure. commands. EventHub. Models. PSSharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="5f415-145">Microsoft.Azure.Commands.EventHub.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="5f415-146">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5f415-146">NOTES</span></span>

## <span data-ttu-id="5f415-147">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5f415-147">RELATED LINKS</span></span>
