---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/new-azeventhubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubKey.md
ms.openlocfilehash: bb66aacb406871731cb2f356c19a91e8bb27429c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93754063"
---
# <span data-ttu-id="b76cf-101">New-AzEventHubKey</span><span class="sxs-lookup"><span data-stu-id="b76cf-101">New-AzEventHubKey</span></span>

## <span data-ttu-id="b76cf-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b76cf-102">SYNOPSIS</span></span>
<span data-ttu-id="b76cf-103">Skapar en ny primär eller sekundär nycklar för den angivna auktoriseringsregeln för Event Hub.</span><span class="sxs-lookup"><span data-stu-id="b76cf-103">Creates a new primary or secondary key for the specified Event Hubs authorization rule.</span></span>

## <span data-ttu-id="b76cf-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b76cf-104">SYNTAX</span></span>

### <span data-ttu-id="b76cf-105">NamespaceAuthorizationRuleSet (standard)</span><span class="sxs-lookup"><span data-stu-id="b76cf-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
New-AzEventHubKey [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-RegenerateKey] <String> [[-KeyValue] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b76cf-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="b76cf-106">EventhubAuthorizationRuleSet</span></span>
```
New-AzEventHubKey [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String> [-Name] <String>
 [-RegenerateKey] <String> [[-KeyValue] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b76cf-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b76cf-107">DESCRIPTION</span></span>
<span data-ttu-id="b76cf-108">New-AzEventHubKey cmdlet återskapar den primära eller sekundära säkerhets associationen för den angivna auktoriseringsregeln för Event Hub.</span><span class="sxs-lookup"><span data-stu-id="b76cf-108">The New-AzEventHubKey cmdlet regenerates the primary or secondary SAS key for the specified Event Hubs authorization rule.</span></span>

## <span data-ttu-id="b76cf-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b76cf-109">EXAMPLES</span></span>

### <span data-ttu-id="b76cf-110">Exempel 1,1-namnrymd – AuthorizationRule PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="b76cf-110">Example 1.1 - Namespace - AuthorizationRule PrimaryKey</span></span>
```
PS C:\> New-AzEventHubKey -ResourceGroup MyResourceGroupName -Namespace MyNamespaceName -Name MyAuthRuleName -RegenerateKey PrimaryKey
```

<span data-ttu-id="b76cf-111">Återskapar primär nyckeln för auktoriseringsregeln \` MyAuthRuleName \` .</span><span class="sxs-lookup"><span data-stu-id="b76cf-111">Regenerates the primary key for the authorization rule \`MyAuthRuleName\`.</span></span>

### <span data-ttu-id="b76cf-112">Exempel 1,2-EventHub-AuthorizationRule PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="b76cf-112">Example 1.2 - EventHub - AuthorizationRule PrimaryKey</span></span>
```
PS C:\> New-AzEventHubKey -ResourceGroup MyResourceGroupName -Namespace MyNamespaceName -EventHub MyEventHubName -Name MyAuthRuleName -RegenerateKey PrimaryKey
```

<span data-ttu-id="b76cf-113">Återskapar primär nyckeln för auktoriseringsregeln \` MyAuthRuleName \` .</span><span class="sxs-lookup"><span data-stu-id="b76cf-113">Regenerates the primary key for the authorization rule \`MyAuthRuleName\`.</span></span>

### <span data-ttu-id="b76cf-114">Exempel 2,1-namespace-AuthorizationRule SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="b76cf-114">Example 2.1  - Namespace - AuthorizationRule SecondaryKey</span></span>
```
PS C:\> New-AzEventHubKey -ResourceGroup MyResourceGroupName -Namespace MyNamespaceName -Name MyAuthRuleName -RegenerateKey SecondaryKey
```

### <span data-ttu-id="b76cf-115">Exempel 2,2-EventHub-AuthorizationRule SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="b76cf-115">Example 2.2 - EventHub - AuthorizationRule SecondaryKey</span></span>
```
PS C:\> New-AzEventHubKey -ResourceGroup MyResourceGroupName -Namespace MyNamespaceName -EventHub MyEventHubName -Name MyAuthRuleName -RegenerateKey SecondaryKey
```

<span data-ttu-id="b76cf-116">Återskapar den sekundära nyckeln för \` MyAuthRuleName \` .</span><span class="sxs-lookup"><span data-stu-id="b76cf-116">Regenerates the secondary key for the authorization rule \`MyAuthRuleName\`.</span></span>

## <span data-ttu-id="b76cf-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b76cf-117">PARAMETERS</span></span>

### <span data-ttu-id="b76cf-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b76cf-118">-DefaultProfile</span></span>
<span data-ttu-id="b76cf-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b76cf-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b76cf-120">-EventHub</span><span class="sxs-lookup"><span data-stu-id="b76cf-120">-EventHub</span></span>
<span data-ttu-id="b76cf-121">Namn på EventHub</span><span class="sxs-lookup"><span data-stu-id="b76cf-121">EventHub Name</span></span>

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

### <span data-ttu-id="b76cf-122">-Nyckelvärdet</span><span class="sxs-lookup"><span data-stu-id="b76cf-122">-KeyValue</span></span>
<span data-ttu-id="b76cf-123">En Base64-kodad 256-bitars nyckel för signering och verifiering av SAS-token.</span><span class="sxs-lookup"><span data-stu-id="b76cf-123">A base64-encoded 256-bit key for signing and validating the SAS token.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b76cf-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="b76cf-124">-Name</span></span>
<span data-ttu-id="b76cf-125">AuthorizationRule namn</span><span class="sxs-lookup"><span data-stu-id="b76cf-125">AuthorizationRule Name</span></span>

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

### <span data-ttu-id="b76cf-126">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="b76cf-126">-Namespace</span></span>
<span data-ttu-id="b76cf-127">Namn på namn området</span><span class="sxs-lookup"><span data-stu-id="b76cf-127">Namespace Name</span></span>

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

### <span data-ttu-id="b76cf-128">-RegenerateKey</span><span class="sxs-lookup"><span data-stu-id="b76cf-128">-RegenerateKey</span></span>
<span data-ttu-id="b76cf-129">Återskapa nycklar – "PrimaryKey"/"SecondaryKey"</span><span class="sxs-lookup"><span data-stu-id="b76cf-129">Regenerate Keys - 'PrimaryKey'/'SecondaryKey'</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: PrimaryKey, SecondaryKey

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b76cf-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b76cf-130">-ResourceGroupName</span></span>
<span data-ttu-id="b76cf-131">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="b76cf-131">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b76cf-132">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="b76cf-132">-Confirm</span></span>
<span data-ttu-id="b76cf-133">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="b76cf-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b76cf-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b76cf-134">-WhatIf</span></span>
<span data-ttu-id="b76cf-135">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="b76cf-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b76cf-136">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="b76cf-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b76cf-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b76cf-137">CommonParameters</span></span>
<span data-ttu-id="b76cf-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b76cf-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b76cf-139">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b76cf-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b76cf-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b76cf-140">INPUTS</span></span>

### <span data-ttu-id="b76cf-141">System. String</span><span class="sxs-lookup"><span data-stu-id="b76cf-141">System.String</span></span>

## <span data-ttu-id="b76cf-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b76cf-142">OUTPUTS</span></span>

### <span data-ttu-id="b76cf-143">Microsoft. Azure. commands. EventHub. Models. PSListKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="b76cf-143">Microsoft.Azure.Commands.EventHub.Models.PSListKeysAttributes</span></span>

## <span data-ttu-id="b76cf-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b76cf-144">NOTES</span></span>

## <span data-ttu-id="b76cf-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b76cf-145">RELATED LINKS</span></span>
