---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/new-azservicebuskey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusKey.md
ms.openlocfilehash: c0c413918a986da4eaea8d9ef5f0f6a091b8b2e4
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94259881"
---
# <span data-ttu-id="a1d85-101">New-AzServiceBusKey</span><span class="sxs-lookup"><span data-stu-id="a1d85-101">New-AzServiceBusKey</span></span>

## <span data-ttu-id="a1d85-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a1d85-102">SYNOPSIS</span></span>
<span data-ttu-id="a1d85-103">Återskapar primära eller sekundära anslutnings strängar för Service Bus namn området eller kön eller avsnittet.</span><span class="sxs-lookup"><span data-stu-id="a1d85-103">Regenerates the primary or secondary connection strings for the Service Bus namespace or queue or topic.</span></span>

## <span data-ttu-id="a1d85-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a1d85-104">SYNTAX</span></span>

### <span data-ttu-id="a1d85-105">NamespaceAuthorizationRuleSet (standard)</span><span class="sxs-lookup"><span data-stu-id="a1d85-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
New-AzServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 -RegenerateKey <String> [-KeyValue <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a1d85-106">QueueAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="a1d85-106">QueueAuthorizationRuleSet</span></span>
```
New-AzServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Queue] <String> [-Name] <String>
 -RegenerateKey <String> [-KeyValue <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a1d85-107">TopicAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="a1d85-107">TopicAuthorizationRuleSet</span></span>
```
New-AzServiceBusKey [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String> [-Name] <String>
 -RegenerateKey <String> [-KeyValue <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a1d85-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a1d85-108">DESCRIPTION</span></span>
<span data-ttu-id="a1d85-109">**New-AzServiceBusKey-** cmdleten skapar nya primära eller sekundära anslutnings strängar för det angivna namn området eller kön eller ämnet och auktoriseringsregeln.</span><span class="sxs-lookup"><span data-stu-id="a1d85-109">The **New-AzServiceBusKey** cmdlet generates new primary or secondary connection strings for the specified namespace or queue or topic and authorization rule.</span></span>

## <span data-ttu-id="a1d85-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a1d85-110">EXAMPLES</span></span>

### <span data-ttu-id="a1d85-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="a1d85-111">Example 1</span></span>
```powershell
PS C:\> New-AzServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1 -RegenerateKey PrimaryKey
```

<span data-ttu-id="a1d85-112">Återskapar primära eller sekundära anslutnings strängar för namn området.</span><span class="sxs-lookup"><span data-stu-id="a1d85-112">Regenerates the primary or secondary connection strings for the namespace.</span></span>

### <span data-ttu-id="a1d85-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="a1d85-113">Example 2</span></span>
```powershell
PS C:\> New-AzServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1 -RegenerateKey PrimaryKey -KeyValue {base64-encoded 256-bit key}
```

<span data-ttu-id="a1d85-114">Återskapar primära eller sekundära anslutnings strängar med angivet nyckelvärdet för namn området.</span><span class="sxs-lookup"><span data-stu-id="a1d85-114">Regenerates the primary or secondary connection strings with provided Key value for the namespace.</span></span>

### <span data-ttu-id="a1d85-115">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="a1d85-115">Example 3</span></span>
```powershell
PS C:\> New-AzServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1 -RegenerateKey PrimaryKey
```

<span data-ttu-id="a1d85-116">Återskapar primära eller sekundära anslutnings strängar för kön.</span><span class="sxs-lookup"><span data-stu-id="a1d85-116">Regenerates the primary or secondary connection strings for the queue.</span></span>

### <span data-ttu-id="a1d85-117">Exempel 4</span><span class="sxs-lookup"><span data-stu-id="a1d85-117">Example 4</span></span>
```powershell
PS C:\> New-AzServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1 -RegenerateKey PrimaryKey -KeyValue {base64-encoded 256-bit key}
```

<span data-ttu-id="a1d85-118">Återskapar primära eller sekundära anslutnings strängar med angivet nyckelvärdet för kön.</span><span class="sxs-lookup"><span data-stu-id="a1d85-118">Regenerates the primary or secondary connection strings with provided Key value for the queue.</span></span>

### <span data-ttu-id="a1d85-119">Exempel 5</span><span class="sxs-lookup"><span data-stu-id="a1d85-119">Example 5</span></span>
```powershell
PS C:\> New-AzServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1 -RegenerateKey PrimaryKey
```

<span data-ttu-id="a1d85-120">Återskapar de primära eller sekundära anslutnings strängarna för ämnet.</span><span class="sxs-lookup"><span data-stu-id="a1d85-120">Regenerates the primary or secondary connection strings for the topic.</span></span>

### <span data-ttu-id="a1d85-121">Exempel 6</span><span class="sxs-lookup"><span data-stu-id="a1d85-121">Example 6</span></span>
```powershell
PS C:\> New-AzServiceBusKey -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1 -RegenerateKey PrimaryKey -KeyValue {base64-encoded 256-bit key}
```

<span data-ttu-id="a1d85-122">Återskapar primära eller sekundära anslutnings strängar med angivet nyckelvärdet.</span><span class="sxs-lookup"><span data-stu-id="a1d85-122">Regenerates the primary or secondary connection strings with provided Key value for the topic.</span></span>

## <span data-ttu-id="a1d85-123">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a1d85-123">PARAMETERS</span></span>

### <span data-ttu-id="a1d85-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1d85-124">-DefaultProfile</span></span>
<span data-ttu-id="a1d85-125">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a1d85-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a1d85-126">-Nyckelvärdet</span><span class="sxs-lookup"><span data-stu-id="a1d85-126">-KeyValue</span></span>
<span data-ttu-id="a1d85-127">En Base64-kodad 256-bitars nyckel för signering och verifiering av SAS-token.</span><span class="sxs-lookup"><span data-stu-id="a1d85-127">A base64-encoded 256-bit key for signing and validating the SAS token.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1d85-128">-Namn</span><span class="sxs-lookup"><span data-stu-id="a1d85-128">-Name</span></span>
<span data-ttu-id="a1d85-129">AuthorizationRule namn.</span><span class="sxs-lookup"><span data-stu-id="a1d85-129">AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="a1d85-130">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="a1d85-130">-Namespace</span></span>
<span data-ttu-id="a1d85-131">Namn på namn området</span><span class="sxs-lookup"><span data-stu-id="a1d85-131">Namespace Name</span></span>

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

### <span data-ttu-id="a1d85-132">-Kö</span><span class="sxs-lookup"><span data-stu-id="a1d85-132">-Queue</span></span>
<span data-ttu-id="a1d85-133">Könamn</span><span class="sxs-lookup"><span data-stu-id="a1d85-133">Queue Name</span></span>

```yaml
Type: System.String
Parameter Sets: QueueAuthorizationRuleSet
Aliases: QueueName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a1d85-134">-RegenerateKey</span><span class="sxs-lookup"><span data-stu-id="a1d85-134">-RegenerateKey</span></span>
<span data-ttu-id="a1d85-135">Återskapa nycklar – "PrimaryKey"/"SecondaryKey".</span><span class="sxs-lookup"><span data-stu-id="a1d85-135">Regenerate Keys - 'PrimaryKey'/'SecondaryKey'.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: PrimaryKey, SecondaryKey

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a1d85-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a1d85-136">-ResourceGroupName</span></span>
<span data-ttu-id="a1d85-137">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="a1d85-137">Resource Group Name</span></span>

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

### <span data-ttu-id="a1d85-138">-Ämne</span><span class="sxs-lookup"><span data-stu-id="a1d85-138">-Topic</span></span>
<span data-ttu-id="a1d85-139">Namn på avsnitt</span><span class="sxs-lookup"><span data-stu-id="a1d85-139">Topic Name</span></span>

```yaml
Type: System.String
Parameter Sets: TopicAuthorizationRuleSet
Aliases: TopicName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a1d85-140">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="a1d85-140">-Confirm</span></span>
<span data-ttu-id="a1d85-141">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="a1d85-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a1d85-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a1d85-142">-WhatIf</span></span>
<span data-ttu-id="a1d85-143">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="a1d85-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a1d85-144">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="a1d85-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a1d85-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1d85-145">CommonParameters</span></span>
<span data-ttu-id="a1d85-146">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a1d85-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1d85-147">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a1d85-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1d85-148">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a1d85-148">INPUTS</span></span>

### <span data-ttu-id="a1d85-149">System. String</span><span class="sxs-lookup"><span data-stu-id="a1d85-149">System.String</span></span>

## <span data-ttu-id="a1d85-150">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a1d85-150">OUTPUTS</span></span>

### <span data-ttu-id="a1d85-151">Microsoft. Azure. commands. ServiceBus. Models. PSListKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="a1d85-151">Microsoft.Azure.Commands.ServiceBus.Models.PSListKeysAttributes</span></span>

## <span data-ttu-id="a1d85-152">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a1d85-152">NOTES</span></span>

## <span data-ttu-id="a1d85-153">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a1d85-153">RELATED LINKS</span></span>
