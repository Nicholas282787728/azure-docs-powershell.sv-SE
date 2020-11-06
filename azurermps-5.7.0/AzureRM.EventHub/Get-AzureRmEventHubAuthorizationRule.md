---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/get-azurermeventhubauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubAuthorizationRule.md
ms.openlocfilehash: 4d162122b82f592472fb31f1087db29faedf08cd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93583171"
---
# <span data-ttu-id="30ecb-101">Get-AzureRmEventHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="30ecb-101">Get-AzureRmEventHubAuthorizationRule</span></span>

## <span data-ttu-id="30ecb-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="30ecb-102">SYNOPSIS</span></span>
<span data-ttu-id="30ecb-103">Hämtar information om en auktoriseringsregel eller hämtar en lista över auktoriseringsregler.</span><span class="sxs-lookup"><span data-stu-id="30ecb-103">Gets the details of an authorization rule, or gets a list of authorization rules.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="30ecb-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="30ecb-104">SYNTAX</span></span>

### <span data-ttu-id="30ecb-105">NamespaceAuthorizationRuleSet (standard)</span><span class="sxs-lookup"><span data-stu-id="30ecb-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzureRmEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="30ecb-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="30ecb-106">EventhubAuthorizationRuleSet</span></span>
```
Get-AzureRmEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Eventhub] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="30ecb-107">AliasAuthoRuleSet</span><span class="sxs-lookup"><span data-stu-id="30ecb-107">AliasAuthoRuleSet</span></span>
```
Get-AzureRmEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-AliasName] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="30ecb-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="30ecb-108">DESCRIPTION</span></span>
<span data-ttu-id="30ecb-109">Get-AzureRmEventHubAuthorizationRule-cmdleten får antingen information om en auktoriseringsregel eller en lista över alla auktoriseringsregler för en viss händelsehubben.</span><span class="sxs-lookup"><span data-stu-id="30ecb-109">The Get-AzureRmEventHubAuthorizationRule cmdlet gets either the details of an authorization rule, or a list of all authorization rules for a specified Event Hub.</span></span>
<span data-ttu-id="30ecb-110">Om namnet på en auktoriseringsregel tillhandahålls returneras informationen om den enskilda auktoriseringsregeln.</span><span class="sxs-lookup"><span data-stu-id="30ecb-110">If the name of an authorization rule is provided, the details of that single authorization rule are returned.</span></span>
<span data-ttu-id="30ecb-111">Om namnet på en auktoriseringsregel inte anges returneras en lista över alla auktoriseringsregler för den angivna Händelsehubben.</span><span class="sxs-lookup"><span data-stu-id="30ecb-111">If the name of an authorization rule is not provided, a list of all authorization rules for the specified Event Hub is returned.</span></span>
<span data-ttu-id="30ecb-112">Om (återställning efter katastrof) anges, returneras informationen om auktoriseringsregeln för namn området för konfigurerade alias.</span><span class="sxs-lookup"><span data-stu-id="30ecb-112">If (Disaster Recovery) Alias name provided, the details of authorization rule of the Namespace for Alias configured is returned.</span></span> 

## <span data-ttu-id="30ecb-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="30ecb-113">EXAMPLES</span></span>

### <span data-ttu-id="30ecb-114">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="30ecb-114">Example 1</span></span>
```
PS C:\> Get-AzureRmEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -AuthorizationRule MyAuthRuleName
```

<span data-ttu-id="30ecb-115">Hämtar auktoriseringsregeln \` MyAuthRuleName \` i \` MyEventHubName \` som befinner sig i namn området \` MyNamespaceName \` .</span><span class="sxs-lookup"><span data-stu-id="30ecb-115">Gets the authorization rule \`MyAuthRuleName\` in the Event Hub \`MyEventHubName\`, which is scoped by the namespace \`MyNamespaceName\`.</span></span>

### <span data-ttu-id="30ecb-116">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="30ecb-116">Example 2</span></span>
```
PS C:\> Get-AzureRmEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName
```

<span data-ttu-id="30ecb-117">Hämtar en lista över alla auktoriseringsregler i \` MyEventHubName, som besvaras \` av namn områdes \` MyNamespaceName \` .</span><span class="sxs-lookup"><span data-stu-id="30ecb-117">Gets a list of all authorization rules in the Event Hub \`MyEventHubName\`, which is scoped by the namespace \`MyNamespaceName\`.</span></span>

### <span data-ttu-id="30ecb-118">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="30ecb-118">Example 3</span></span>
```
PS C:\> Get-AzureRmEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -AliasName MyAliasNameName -Name MyAuthRuleName
```

<span data-ttu-id="30ecb-119">Hämtar auktoriseringsregeln \` MyAuthRuleName \` i namn området \` MyNamespaceName \` .</span><span class="sxs-lookup"><span data-stu-id="30ecb-119">Gets the authorization rule \`MyAuthRuleName\` in the namespace \`MyNamespaceName\`.</span></span>

## <span data-ttu-id="30ecb-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="30ecb-120">PARAMETERS</span></span>

### <span data-ttu-id="30ecb-121">-AliasName</span><span class="sxs-lookup"><span data-stu-id="30ecb-121">-AliasName</span></span>
<span data-ttu-id="30ecb-122">Aliasnamn</span><span class="sxs-lookup"><span data-stu-id="30ecb-122">Alias Name</span></span>

```yaml
Type: String
Parameter Sets: AliasAuthoRuleSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="30ecb-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30ecb-123">-DefaultProfile</span></span>
<span data-ttu-id="30ecb-124">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="30ecb-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="30ecb-125">-Eventhub</span><span class="sxs-lookup"><span data-stu-id="30ecb-125">-Eventhub</span></span>
<span data-ttu-id="30ecb-126">Namn på Eventhub</span><span class="sxs-lookup"><span data-stu-id="30ecb-126">Eventhub Name</span></span>

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

### <span data-ttu-id="30ecb-127">-Namn</span><span class="sxs-lookup"><span data-stu-id="30ecb-127">-Name</span></span>
<span data-ttu-id="30ecb-128">AuthorizationRule namn</span><span class="sxs-lookup"><span data-stu-id="30ecb-128">AuthorizationRule Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="30ecb-129">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="30ecb-129">-Namespace</span></span>
<span data-ttu-id="30ecb-130">Namn på namn området</span><span class="sxs-lookup"><span data-stu-id="30ecb-130">Namespace Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="30ecb-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="30ecb-131">-ResourceGroupName</span></span>
<span data-ttu-id="30ecb-132">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="30ecb-132">Resource Group Name</span></span>

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

### <span data-ttu-id="30ecb-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30ecb-133">CommonParameters</span></span>
<span data-ttu-id="30ecb-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="30ecb-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="30ecb-135">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="30ecb-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30ecb-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="30ecb-136">INPUTS</span></span>

### <span data-ttu-id="30ecb-137">System. String</span><span class="sxs-lookup"><span data-stu-id="30ecb-137">System.String</span></span>


## <span data-ttu-id="30ecb-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="30ecb-138">OUTPUTS</span></span>

### <span data-ttu-id="30ecb-139">System. Collections. Generic. list ' 1 [[Microsoft. Azure. commands. EventHub. Models. PSSharedAccessAuthorizationRuleAttributes, Microsoft. Azure. commands. EventHub, version = 0.5.0.0, Culture = neutralt, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="30ecb-139">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.EventHub.Models.PSSharedAccessAuthorizationRuleAttributes, Microsoft.Azure.Commands.EventHub, Version=0.5.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>


## <span data-ttu-id="30ecb-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="30ecb-140">NOTES</span></span>

## <span data-ttu-id="30ecb-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="30ecb-141">RELATED LINKS</span></span>
