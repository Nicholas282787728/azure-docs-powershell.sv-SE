---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusTopicKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusTopicKey.md
ms.openlocfilehash: ed31934a75d9d6826a7e0464dccd43fd2d853daa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575845"
---
# <span data-ttu-id="415a6-101">New-AzureRmServiceBusTopicKey</span><span class="sxs-lookup"><span data-stu-id="415a6-101">New-AzureRmServiceBusTopicKey</span></span>

## <span data-ttu-id="415a6-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="415a6-102">SYNOPSIS</span></span>
<span data-ttu-id="415a6-103">Återskapar primära eller sekundära anslutnings strängar för Service Bus-ämnet.</span><span class="sxs-lookup"><span data-stu-id="415a6-103">Regenerates the primary or secondary connection strings for the Service Bus topic.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="415a6-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="415a6-104">SYNTAX</span></span>

```
New-AzureRmServiceBusTopicKey [-ResourceGroup] <String> -Namespace <String> -Topic <String> -Name <String>
 [-RegenerateKeys] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="415a6-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="415a6-105">DESCRIPTION</span></span>
<span data-ttu-id="415a6-106">Cmdleten **New-AzureRmServiceBusTopicKey** skapar en ny primär eller sekundär anslutnings sträng för det angivna tjänst buss ämnet och auktoriseringsregeln.</span><span class="sxs-lookup"><span data-stu-id="415a6-106">The **New-AzureRmServiceBusTopicKey** cmdlet generates a new primary or secondary connection string for the specified Service Bus topic and authorization rule.</span></span>

## <span data-ttu-id="415a6-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="415a6-107">EXAMPLES</span></span>

### <span data-ttu-id="415a6-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="415a6-108">Example 1</span></span>
```
PS C:\> New-AzureRmServiceBusTopicKey -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -AuthorizationRuleName SBTopicAuthoRule1 -RegenerateKeys PrimaryKey
```

<span data-ttu-id="415a6-109">Återskapar den primära anslutnings strängen för namn området.</span><span class="sxs-lookup"><span data-stu-id="415a6-109">Regenerates the primary connection string for the namespace.</span></span>

### <span data-ttu-id="415a6-110">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="415a6-110">Example 2</span></span>
```
PS C:\> New-AzureRmServiceBusTopicKey -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -AuthorizationRuleName SBTopicAuthoRule1 -RegenerateKeys SecondaryKey
```

<span data-ttu-id="415a6-111">Återskapar sekundär anslutnings strängen för namn området.</span><span class="sxs-lookup"><span data-stu-id="415a6-111">Regenerates the secondary connection string for the namespace.</span></span>

## <span data-ttu-id="415a6-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="415a6-112">PARAMETERS</span></span>

### <span data-ttu-id="415a6-113">-RegenerateKeys</span><span class="sxs-lookup"><span data-stu-id="415a6-113">-RegenerateKeys</span></span>
<span data-ttu-id="415a6-114">Anger om primära eller sekundära nycklar ska återskapas.</span><span class="sxs-lookup"><span data-stu-id="415a6-114">Specifies whether to regenerate the primary or secondary keys.</span></span>

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

### <span data-ttu-id="415a6-115">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="415a6-115">-ResourceGroup</span></span>
<span data-ttu-id="415a6-116">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="415a6-116">The name of the resource group.</span></span>

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

### <span data-ttu-id="415a6-117">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="415a6-117">-Confirm</span></span>
<span data-ttu-id="415a6-118">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="415a6-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="415a6-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="415a6-119">-WhatIf</span></span>
<span data-ttu-id="415a6-120">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="415a6-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="415a6-121">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="415a6-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="415a6-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="415a6-122">-DefaultProfile</span></span>
<span data-ttu-id="415a6-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="415a6-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="415a6-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="415a6-124">-Name</span></span>
<span data-ttu-id="415a6-125">Namn på auktoriseringsregel.</span><span class="sxs-lookup"><span data-stu-id="415a6-125">Authorization Rule Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="415a6-126">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="415a6-126">-Namespace</span></span>
<span data-ttu-id="415a6-127">Namn på namn området.</span><span class="sxs-lookup"><span data-stu-id="415a6-127">Namespace Name.</span></span>

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

### <span data-ttu-id="415a6-128">-Ämne</span><span class="sxs-lookup"><span data-stu-id="415a6-128">-Topic</span></span>
<span data-ttu-id="415a6-129">Avsnitts namn.</span><span class="sxs-lookup"><span data-stu-id="415a6-129">Topic Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TopicName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="415a6-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="415a6-130">CommonParameters</span></span>
<span data-ttu-id="415a6-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="415a6-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="415a6-132">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="415a6-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="415a6-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="415a6-133">INPUTS</span></span>

### <span data-ttu-id="415a6-134">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="415a6-134">-ResourceGroup</span></span>
 <span data-ttu-id="415a6-135">System. String</span><span class="sxs-lookup"><span data-stu-id="415a6-135">System.String</span></span>
 

### <span data-ttu-id="415a6-136">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="415a6-136">-NamespaceName</span></span>
 <span data-ttu-id="415a6-137">System. String</span><span class="sxs-lookup"><span data-stu-id="415a6-137">System.String</span></span>
 

### <span data-ttu-id="415a6-138">-AuthorizationRuleName</span><span class="sxs-lookup"><span data-stu-id="415a6-138">-AuthorizationRuleName</span></span>
 <span data-ttu-id="415a6-139">System. String</span><span class="sxs-lookup"><span data-stu-id="415a6-139">System.String</span></span>
 

### <span data-ttu-id="415a6-140">-TopicName</span><span class="sxs-lookup"><span data-stu-id="415a6-140">-TopicName</span></span>
 <span data-ttu-id="415a6-141">System. String</span><span class="sxs-lookup"><span data-stu-id="415a6-141">System.String</span></span>
 

### <span data-ttu-id="415a6-142">-RegenerateKeys</span><span class="sxs-lookup"><span data-stu-id="415a6-142">-RegenerateKeys</span></span>
 <span data-ttu-id="415a6-143">System. String</span><span class="sxs-lookup"><span data-stu-id="415a6-143">System.String</span></span>

## <span data-ttu-id="415a6-144">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="415a6-144">OUTPUTS</span></span>

### <span data-ttu-id="415a6-145">Microsoft. Azure. commands. ServiceBus. Models. ListKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="415a6-145">Microsoft.Azure.Commands.ServiceBus.Models.ListKeysAttributes</span></span>
<span data-ttu-id="415a6-146">PrimaryConnectionString: slut punkt = SB://SB-example1.ServiceBus.Windows.net/; SharedAccessKeyName = SBTopicAuthoRule1; SharedAccessKey = {SharedAccessKey-Value}; EntityPath = SB-Topi c_exampl1 SecondaryConnectionString: slut punkt = SB://SB-example1.ServiceBus.Windows.net/; SharedAccessKeyName = SBTopicAuthoRule1; SharedAccessKey = {SharedAccessKey-Value}; EntityPath = SB-Topi c_exampl1 PrimaryKey: {PrimaryKey Value} SecondaryKey: {SecondaryKey värde} nyckel namn: SBTopicAuthoRule1</span><span class="sxs-lookup"><span data-stu-id="415a6-146">PrimaryConnectionString   : Endpoint=sb://sb-example1.servicebus.windows.net/;SharedAccessKeyName=SBTopicAuthoRule1;SharedAccessKey={SharedAccessKey-value};EntityPath=SB-Topi c_exampl1 SecondaryConnectionString : Endpoint=sb://sb-example1.servicebus.windows.net/;SharedAccessKeyName=SBTopicAuthoRule1;SharedAccessKey={SharedAccessKey-value};EntityPath=SB-Topi c_exampl1 PrimaryKey                : {PrimaryKey value} SecondaryKey              : {SecondaryKey value} KeyName                   : SBTopicAuthoRule1</span></span>

## <span data-ttu-id="415a6-147">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="415a6-147">NOTES</span></span>

## <span data-ttu-id="415a6-148">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="415a6-148">RELATED LINKS</span></span>

