---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/new-azeventhubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubKey.md
ms.openlocfilehash: 477884e676118f461578be500715fd3698957003
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94261313"
---
# <span data-ttu-id="acbd6-101">New-AzEventHubKey</span><span class="sxs-lookup"><span data-stu-id="acbd6-101">New-AzEventHubKey</span></span>

## <span data-ttu-id="acbd6-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="acbd6-102">SYNOPSIS</span></span>
<span data-ttu-id="acbd6-103">Skapar en ny primär eller sekundär nycklar för den angivna auktoriseringsregeln för Event Hub.</span><span class="sxs-lookup"><span data-stu-id="acbd6-103">Creates a new primary or secondary key for the specified Event Hubs authorization rule.</span></span>

## <span data-ttu-id="acbd6-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="acbd6-104">SYNTAX</span></span>

### <span data-ttu-id="acbd6-105">NamespaceAuthorizationRuleSet (standard)</span><span class="sxs-lookup"><span data-stu-id="acbd6-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
New-AzEventHubKey [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-RegenerateKey] <String> [[-KeyValue] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="acbd6-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="acbd6-106">EventhubAuthorizationRuleSet</span></span>
```
New-AzEventHubKey [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String> [-Name] <String>
 [-RegenerateKey] <String> [[-KeyValue] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="acbd6-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="acbd6-107">DESCRIPTION</span></span>
<span data-ttu-id="acbd6-108">New-AzEventHubKey cmdlet återskapar den primära eller sekundära säkerhets associationen för den angivna auktoriseringsregeln för Event Hub.</span><span class="sxs-lookup"><span data-stu-id="acbd6-108">The New-AzEventHubKey cmdlet regenerates the primary or secondary SAS key for the specified Event Hubs authorization rule.</span></span>

## <span data-ttu-id="acbd6-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="acbd6-109">EXAMPLES</span></span>

### <span data-ttu-id="acbd6-110">Exempel 1: namespace – AuthorizationRule PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="acbd6-110">Example 1: Namespace - AuthorizationRule PrimaryKey</span></span>
```powershell
PS C:\> New-AzEventHubKey -ResourceGroup MyResourceGroupName -Namespace MyNamespaceName -Name MyAuthRuleName -RegenerateKey PrimaryKey
```

<span data-ttu-id="acbd6-111">Återskapar primär nyckeln för auktoriseringsregeln \` MyAuthRuleName \` .</span><span class="sxs-lookup"><span data-stu-id="acbd6-111">Regenerates the primary key for the authorization rule \`MyAuthRuleName\`.</span></span>

### <span data-ttu-id="acbd6-112">Exempel 2: EventHub – AuthorizationRule PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="acbd6-112">Example 2: EventHub - AuthorizationRule PrimaryKey</span></span>
```powershell
PS C:\> New-AzEventHubKey -ResourceGroup MyResourceGroupName -Namespace MyNamespaceName -EventHub MyEventHubName -Name MyAuthRuleName -RegenerateKey PrimaryKey
```

<span data-ttu-id="acbd6-113">Återskapar primär nyckeln för auktoriseringsregeln \` MyAuthRuleName \` .</span><span class="sxs-lookup"><span data-stu-id="acbd6-113">Regenerates the primary key for the authorization rule \`MyAuthRuleName\`.</span></span>

### <span data-ttu-id="acbd6-114">Exempel 3:-namespace-AuthorizationRule SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="acbd6-114">Example 3: - Namespace - AuthorizationRule SecondaryKey</span></span>
```powershell
PS C:\> New-AzEventHubKey -ResourceGroup MyResourceGroupName -Namespace MyNamespaceName -Name MyAuthRuleName -RegenerateKey SecondaryKey
```

### <span data-ttu-id="acbd6-115">Exempel 4: EventHub – AuthorizationRule SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="acbd6-115">Example 4: EventHub - AuthorizationRule SecondaryKey</span></span>
```powershell
PS C:\> New-AzEventHubKey -ResourceGroup MyResourceGroupName -Namespace MyNamespaceName -EventHub MyEventHubName -Name MyAuthRuleName -RegenerateKey SecondaryKey
```

<span data-ttu-id="acbd6-116">Återskapar den sekundära nyckeln för \` MyAuthRuleName \` .</span><span class="sxs-lookup"><span data-stu-id="acbd6-116">Regenerates the secondary key for the authorization rule \`MyAuthRuleName\`.</span></span>

## <span data-ttu-id="acbd6-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="acbd6-117">PARAMETERS</span></span>

### <span data-ttu-id="acbd6-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="acbd6-118">-DefaultProfile</span></span>
<span data-ttu-id="acbd6-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="acbd6-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="acbd6-120">-EventHub</span><span class="sxs-lookup"><span data-stu-id="acbd6-120">-EventHub</span></span>
<span data-ttu-id="acbd6-121">Namn på EventHub</span><span class="sxs-lookup"><span data-stu-id="acbd6-121">EventHub Name</span></span>

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

### <span data-ttu-id="acbd6-122">-Nyckelvärdet</span><span class="sxs-lookup"><span data-stu-id="acbd6-122">-KeyValue</span></span>
<span data-ttu-id="acbd6-123">En Base64-kodad 256-bitars nyckel för signering och verifiering av SAS-token.</span><span class="sxs-lookup"><span data-stu-id="acbd6-123">A base64-encoded 256-bit key for signing and validating the SAS token.</span></span>

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

### <span data-ttu-id="acbd6-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="acbd6-124">-Name</span></span>
<span data-ttu-id="acbd6-125">AuthorizationRule namn</span><span class="sxs-lookup"><span data-stu-id="acbd6-125">AuthorizationRule Name</span></span>

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

### <span data-ttu-id="acbd6-126">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="acbd6-126">-Namespace</span></span>
<span data-ttu-id="acbd6-127">Namn på namn området</span><span class="sxs-lookup"><span data-stu-id="acbd6-127">Namespace Name</span></span>

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

### <span data-ttu-id="acbd6-128">-RegenerateKey</span><span class="sxs-lookup"><span data-stu-id="acbd6-128">-RegenerateKey</span></span>
<span data-ttu-id="acbd6-129">Återskapa nycklar – "PrimaryKey"/"SecondaryKey"</span><span class="sxs-lookup"><span data-stu-id="acbd6-129">Regenerate Keys - 'PrimaryKey'/'SecondaryKey'</span></span>

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

### <span data-ttu-id="acbd6-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="acbd6-130">-ResourceGroupName</span></span>
<span data-ttu-id="acbd6-131">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="acbd6-131">Resource Group Name</span></span>

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

### <span data-ttu-id="acbd6-132">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="acbd6-132">-Confirm</span></span>
<span data-ttu-id="acbd6-133">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="acbd6-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="acbd6-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="acbd6-134">-WhatIf</span></span>
<span data-ttu-id="acbd6-135">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="acbd6-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="acbd6-136">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="acbd6-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="acbd6-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="acbd6-137">CommonParameters</span></span>
<span data-ttu-id="acbd6-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="acbd6-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="acbd6-139">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="acbd6-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="acbd6-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="acbd6-140">INPUTS</span></span>

### <span data-ttu-id="acbd6-141">System. String</span><span class="sxs-lookup"><span data-stu-id="acbd6-141">System.String</span></span>

## <span data-ttu-id="acbd6-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="acbd6-142">OUTPUTS</span></span>

### <span data-ttu-id="acbd6-143">Microsoft. Azure. commands. EventHub. Models. PSListKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="acbd6-143">Microsoft.Azure.Commands.EventHub.Models.PSListKeysAttributes</span></span>

## <span data-ttu-id="acbd6-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="acbd6-144">NOTES</span></span>

## <span data-ttu-id="acbd6-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="acbd6-145">RELATED LINKS</span></span>
