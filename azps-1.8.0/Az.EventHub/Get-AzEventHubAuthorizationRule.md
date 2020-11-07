---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/get-azeventhubauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubAuthorizationRule.md
ms.openlocfilehash: 66e32c19001586972cb408e61397545fb1c25d44
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93754082"
---
# <span data-ttu-id="bc21e-101">Get-AzEventHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="bc21e-101">Get-AzEventHubAuthorizationRule</span></span>

## <span data-ttu-id="bc21e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="bc21e-102">SYNOPSIS</span></span>
<span data-ttu-id="bc21e-103">Hämtar information om en auktoriseringsregel eller hämtar en lista över auktoriseringsregler.</span><span class="sxs-lookup"><span data-stu-id="bc21e-103">Gets the details of an authorization rule, or gets a list of authorization rules.</span></span>

## <span data-ttu-id="bc21e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="bc21e-104">SYNTAX</span></span>

### <span data-ttu-id="bc21e-105">NamespaceAuthorizationRuleSet (standard)</span><span class="sxs-lookup"><span data-stu-id="bc21e-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bc21e-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="bc21e-106">EventhubAuthorizationRuleSet</span></span>
```
Get-AzEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Eventhub] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bc21e-107">AliasAuthoRuleSet</span><span class="sxs-lookup"><span data-stu-id="bc21e-107">AliasAuthoRuleSet</span></span>
```
Get-AzEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-AliasName] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bc21e-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="bc21e-108">DESCRIPTION</span></span>
<span data-ttu-id="bc21e-109">Get-AzEventHubAuthorizationRule-cmdleten får antingen information om en auktoriseringsregel eller en lista över alla auktoriseringsregler för en viss händelsehubben.</span><span class="sxs-lookup"><span data-stu-id="bc21e-109">The Get-AzEventHubAuthorizationRule cmdlet gets either the details of an authorization rule, or a list of all authorization rules for a specified Event Hub.</span></span>
<span data-ttu-id="bc21e-110">Om namnet på en auktoriseringsregel tillhandahålls returneras informationen om den enskilda auktoriseringsregeln.</span><span class="sxs-lookup"><span data-stu-id="bc21e-110">If the name of an authorization rule is provided, the details of that single authorization rule are returned.</span></span>
<span data-ttu-id="bc21e-111">Om namnet på en auktoriseringsregel inte anges returneras en lista över alla auktoriseringsregler för den angivna Händelsehubben.</span><span class="sxs-lookup"><span data-stu-id="bc21e-111">If the name of an authorization rule is not provided, a list of all authorization rules for the specified Event Hub is returned.</span></span>
<span data-ttu-id="bc21e-112">Om (återställning efter katastrof) anges, returneras informationen om auktoriseringsregeln för namn området för konfigurerade alias.</span><span class="sxs-lookup"><span data-stu-id="bc21e-112">If (Disaster Recovery) Alias name provided, the details of authorization rule of the Namespace for Alias configured is returned.</span></span>

## <span data-ttu-id="bc21e-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="bc21e-113">EXAMPLES</span></span>

### <span data-ttu-id="bc21e-114">Exempel på 1,0-AuthorizationRule för namespace</span><span class="sxs-lookup"><span data-stu-id="bc21e-114">Example 1.0 - AuthorizationRule for namespace</span></span>
```
PS C:\> Get-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Name MyAuthRuleName
```

<span data-ttu-id="bc21e-115">Hämtar auktoriseringsregeln \` MyAuthRuleName \` i namn området \` MyNamespaceName \` .</span><span class="sxs-lookup"><span data-stu-id="bc21e-115">Gets the authorization rule \`MyAuthRuleName\` in the namespace \`MyNamespaceName\`.</span></span>

### <span data-ttu-id="bc21e-116">Exempel på 1,1-AuthorizationRules för namespace</span><span class="sxs-lookup"><span data-stu-id="bc21e-116">Example 1.1 - AuthorizationRules for namespace</span></span>
```
PS C:\> Get-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName
```

<span data-ttu-id="bc21e-117">Hämtar en lista över alla auktoriseringsregler i namn området \` MyNamespaceName \` .</span><span class="sxs-lookup"><span data-stu-id="bc21e-117">Gets a list of all authorization rules in the namespace \`MyNamespaceName\`.</span></span>

### <span data-ttu-id="bc21e-118">Exempel 2,0-AuthorizationRule för EventHub</span><span class="sxs-lookup"><span data-stu-id="bc21e-118">Example 2.0 - AuthorizationRule for EventHub</span></span>
```
PS C:\> Get-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -Name MyAuthRuleName
```

<span data-ttu-id="bc21e-119">Hämtar auktoriseringsregeln \` MyAuthRuleName \` i \` MyEventHubName \` som befinner sig i namn området \` MyNamespaceName \` .</span><span class="sxs-lookup"><span data-stu-id="bc21e-119">Gets the authorization rule \`MyAuthRuleName\` in the Event Hub \`MyEventHubName\`, which is scoped by the namespace \`MyNamespaceName\`.</span></span>

### <span data-ttu-id="bc21e-120">Exempel 2,1-AuthorizationRules för EventHub</span><span class="sxs-lookup"><span data-stu-id="bc21e-120">Example 2.1 - AuthorizationRules for EventHub</span></span>
```
PS C:\> Get-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName
```

<span data-ttu-id="bc21e-121">Hämtar en lista med auktoriseringsregler i händelsehubben \` MyEventHubName \` , som befinner sig i namn områdets \` MyNamespaceName \` .</span><span class="sxs-lookup"><span data-stu-id="bc21e-121">Gets list authorization rules in the Event Hub \`MyEventHubName\`, which is scoped by the namespace \`MyNamespaceName\`.</span></span>

### <span data-ttu-id="bc21e-122">Exempel 3,0-AuthorizationRule för alias (återställnings konfiguration)</span><span class="sxs-lookup"><span data-stu-id="bc21e-122">Example 3.0 - AuthorizationRule for Alias (GeoRecovery Configuration)</span></span>
```
PS C:\> Get-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -AliasName MyAliasNameName -Name MyAuthRuleName
```

<span data-ttu-id="bc21e-123">Hämtar auktoriseringsregeln \` MyAuthRuleName \` i namn området \` MyNamespaceName \` .</span><span class="sxs-lookup"><span data-stu-id="bc21e-123">Gets the authorization rule \`MyAuthRuleName\` in the namespace \`MyNamespaceName\`.</span></span>

### <span data-ttu-id="bc21e-124">Exempel 3,1-AuthorizationRules för alias (återställnings konfiguration)</span><span class="sxs-lookup"><span data-stu-id="bc21e-124">Example 3.1 -AuthorizationRules for Alias (GeoRecovery Configuration)</span></span>
```
PS C:\> Get-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -AliasName MyAliasNameName
```

<span data-ttu-id="bc21e-125">Hämtar en lista över alla \` MyAuthRuleName \` i namn området \` MyNamespaceName \` .</span><span class="sxs-lookup"><span data-stu-id="bc21e-125">Gets a list of all authorization rule \`MyAuthRuleName\` in the namespace \`MyNamespaceName\`.</span></span>

## <span data-ttu-id="bc21e-126">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="bc21e-126">PARAMETERS</span></span>

### <span data-ttu-id="bc21e-127">-AliasName</span><span class="sxs-lookup"><span data-stu-id="bc21e-127">-AliasName</span></span>
<span data-ttu-id="bc21e-128">Aliasnamn</span><span class="sxs-lookup"><span data-stu-id="bc21e-128">Alias Name</span></span>

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

### <span data-ttu-id="bc21e-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc21e-129">-DefaultProfile</span></span>
<span data-ttu-id="bc21e-130">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="bc21e-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bc21e-131">-Eventhub</span><span class="sxs-lookup"><span data-stu-id="bc21e-131">-Eventhub</span></span>
<span data-ttu-id="bc21e-132">Namn på Eventhub</span><span class="sxs-lookup"><span data-stu-id="bc21e-132">Eventhub Name</span></span>

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

### <span data-ttu-id="bc21e-133">-Namn</span><span class="sxs-lookup"><span data-stu-id="bc21e-133">-Name</span></span>
<span data-ttu-id="bc21e-134">AuthorizationRule namn</span><span class="sxs-lookup"><span data-stu-id="bc21e-134">AuthorizationRule Name</span></span>

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

### <span data-ttu-id="bc21e-135">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="bc21e-135">-Namespace</span></span>
<span data-ttu-id="bc21e-136">Namn på namn området</span><span class="sxs-lookup"><span data-stu-id="bc21e-136">Namespace Name</span></span>

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

### <span data-ttu-id="bc21e-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bc21e-137">-ResourceGroupName</span></span>
<span data-ttu-id="bc21e-138">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="bc21e-138">Resource Group Name</span></span>

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

### <span data-ttu-id="bc21e-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc21e-139">CommonParameters</span></span>
<span data-ttu-id="bc21e-140">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bc21e-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc21e-141">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bc21e-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc21e-142">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="bc21e-142">INPUTS</span></span>

### <span data-ttu-id="bc21e-143">System. String</span><span class="sxs-lookup"><span data-stu-id="bc21e-143">System.String</span></span>

## <span data-ttu-id="bc21e-144">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="bc21e-144">OUTPUTS</span></span>

### <span data-ttu-id="bc21e-145">Microsoft. Azure. commands. EventHub. Models. PSSharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="bc21e-145">Microsoft.Azure.Commands.EventHub.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="bc21e-146">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="bc21e-146">NOTES</span></span>

## <span data-ttu-id="bc21e-147">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="bc21e-147">RELATED LINKS</span></span>