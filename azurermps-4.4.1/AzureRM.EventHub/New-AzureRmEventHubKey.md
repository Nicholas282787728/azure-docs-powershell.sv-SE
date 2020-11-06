---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubKey.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: 3bd06ea2534298ba81cd546e8fa6e8de02fa5928
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93585591"
---
# <span data-ttu-id="1f416-101">New-AzureRmEventHubKey</span><span class="sxs-lookup"><span data-stu-id="1f416-101">New-AzureRmEventHubKey</span></span>

## <span data-ttu-id="1f416-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1f416-102">SYNOPSIS</span></span>
<span data-ttu-id="1f416-103">Skapar en ny primär eller sekundär nycklar för den angivna auktoriseringsregeln för Event Hub.</span><span class="sxs-lookup"><span data-stu-id="1f416-103">Creates a new primary or secondary key for the specified Event Hubs authorization rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1f416-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1f416-104">SYNTAX</span></span>

### <span data-ttu-id="1f416-105">NamespaceAuthorizationRuleSet (standard)</span><span class="sxs-lookup"><span data-stu-id="1f416-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
New-AzureRmEventHubKey -ResourceGroupName <String> -Namespace <String> -Name <String> -RegenerateKey <String>
 [-WhatIf] [-Confirm]
```

### <span data-ttu-id="1f416-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="1f416-106">EventhubAuthorizationRuleSet</span></span>
```
New-AzureRmEventHubKey -ResourceGroupName <String> [-Namespace <String>] -EventHub <String> -Name <String>
 -RegenerateKey <String> [-WhatIf] [-Confirm]
```

## <span data-ttu-id="1f416-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1f416-107">DESCRIPTION</span></span>
<span data-ttu-id="1f416-108">New-AzureRmEventHubKey cmdlet återskapar den primära eller sekundära säkerhets associationen för den angivna auktoriseringsregeln för Event Hub.</span><span class="sxs-lookup"><span data-stu-id="1f416-108">The New-AzureRmEventHubKey cmdlet regenerates the primary or secondary SAS key for the specified Event Hubs authorization rule.</span></span>

## <span data-ttu-id="1f416-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1f416-109">EXAMPLES</span></span>

### <span data-ttu-id="1f416-110">Exempel 1,1</span><span class="sxs-lookup"><span data-stu-id="1f416-110">Example 1.1</span></span>
```
PS C:\> New-AzureRmEventHubKey -ResourceGroup MyResourceGroupName -Namespace MyNamespaceName -Name MyAuthRuleName -RegenerateKey PrimaryKey
```

<span data-ttu-id="1f416-111">Återskapar primär nyckeln för auktoriseringsregeln \` MyAuthRuleName \` .</span><span class="sxs-lookup"><span data-stu-id="1f416-111">Regenerates the primary key for the authorization rule \`MyAuthRuleName\`.</span></span>

### <span data-ttu-id="1f416-112">Exempel 1,2</span><span class="sxs-lookup"><span data-stu-id="1f416-112">Example 1.2</span></span>
```
PS C:\> New-AzureRmEventHubKey -ResourceGroup MyResourceGroupName -Namespace MyNamespaceName -EventHub MyEventHubName -Name MyAuthRuleName -RegenerateKey PrimaryKey
```

<span data-ttu-id="1f416-113">Återskapar primär nyckeln för auktoriseringsregeln \` MyAuthRuleName \` .</span><span class="sxs-lookup"><span data-stu-id="1f416-113">Regenerates the primary key for the authorization rule \`MyAuthRuleName\`.</span></span>

### <span data-ttu-id="1f416-114">Exempel 2,1</span><span class="sxs-lookup"><span data-stu-id="1f416-114">Example 2.1</span></span>
```
PS C:\> New-AzureRmEventHubKey -ResourceGroup MyResourceGroupName -Namespace MyNamespaceName -Name MyAuthRuleName -RegenerateKey SecondaryKey
```

### <span data-ttu-id="1f416-115">Exempel 2,2</span><span class="sxs-lookup"><span data-stu-id="1f416-115">Example 2.2</span></span>
```
PS C:\> New-AzureRmEventHubKey -ResourceGroup MyResourceGroupName -Namespace MyNamespaceName -EventHub MyEventHubName -Name MyAuthRuleName -RegenerateKey SecondaryKey
```

<span data-ttu-id="1f416-116">Återskapar den sekundära nyckeln för \` MyAuthRuleName \` .</span><span class="sxs-lookup"><span data-stu-id="1f416-116">Regenerates the secondary key for the authorization rule \`MyAuthRuleName\`.</span></span>

## <span data-ttu-id="1f416-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1f416-117">PARAMETERS</span></span>

### <span data-ttu-id="1f416-118">-RegenerateKey</span><span class="sxs-lookup"><span data-stu-id="1f416-118">-RegenerateKey</span></span>
<span data-ttu-id="1f416-119">För att återskapa: \` PrimaryKey \` eller \` SecondaryKey \` .</span><span class="sxs-lookup"><span data-stu-id="1f416-119">Key to regenerate: \`PrimaryKey\` or \`SecondaryKey\`.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: PrimaryKey, SecondaryKey

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f416-120">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="1f416-120">-Confirm</span></span>
<span data-ttu-id="1f416-121">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="1f416-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f416-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1f416-122">-WhatIf</span></span>
<span data-ttu-id="1f416-123">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="1f416-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1f416-124">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="1f416-124">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f416-125">-EventHub</span><span class="sxs-lookup"><span data-stu-id="1f416-125">-EventHub</span></span>
<span data-ttu-id="1f416-126">Namn på EventHub.</span><span class="sxs-lookup"><span data-stu-id="1f416-126">EventHub Name.</span></span>

```yaml
Type: String
Parameter Sets: EventhubAuthorizationRuleSet
Aliases: EventHubName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f416-127">-Namn</span><span class="sxs-lookup"><span data-stu-id="1f416-127">-Name</span></span>
<span data-ttu-id="1f416-128">AuthorizationRule namn.</span><span class="sxs-lookup"><span data-stu-id="1f416-128">AuthorizationRule Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f416-129">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="1f416-129">-Namespace</span></span>
<span data-ttu-id="1f416-130">Namn på namn området.</span><span class="sxs-lookup"><span data-stu-id="1f416-130">Namespace Name.</span></span>

```yaml
Type: String
Parameter Sets: NamespaceAuthorizationRuleSet
Aliases: NamespaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: EventhubAuthorizationRuleSet
Aliases: NamespaceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f416-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1f416-131">-ResourceGroupName</span></span>
<span data-ttu-id="1f416-132">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="1f416-132">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

## <span data-ttu-id="1f416-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1f416-133">INPUTS</span></span>

### <span data-ttu-id="1f416-134">System. String</span><span class="sxs-lookup"><span data-stu-id="1f416-134">System.String</span></span>

## <span data-ttu-id="1f416-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1f416-135">OUTPUTS</span></span>

### <span data-ttu-id="1f416-136">Microsoft. Azure. commands. EventHub. Models. ListKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="1f416-136">Microsoft.Azure.Commands.EventHub.Models.ListKeysAttributes</span></span>

## <span data-ttu-id="1f416-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1f416-137">NOTES</span></span>

## <span data-ttu-id="1f416-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1f416-138">RELATED LINKS</span></span>

