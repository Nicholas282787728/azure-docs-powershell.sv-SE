---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusTopicAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusTopicAuthorizationRule.md
ms.openlocfilehash: 5694d46e44931d59f79a5ac7b86ceabf7632f945
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93584535"
---
# <span data-ttu-id="b7c66-101">Remove-AzureRmServiceBusTopicAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="b7c66-101">Remove-AzureRmServiceBusTopicAuthorizationRule</span></span>

## <span data-ttu-id="b7c66-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b7c66-102">SYNOPSIS</span></span>
<span data-ttu-id="b7c66-103">Tar bort auktoriseringsregeln för ett ämne från det angivna Service Bus-namnområdet.</span><span class="sxs-lookup"><span data-stu-id="b7c66-103">Removes the authorization rule of a topic from the specified Service Bus Namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b7c66-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b7c66-104">SYNTAX</span></span>

```
Remove-AzureRmServiceBusTopicAuthorizationRule [-ResourceGroup] <String> -Namespace <String> -Topic <String>
 -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b7c66-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b7c66-105">DESCRIPTION</span></span>
<span data-ttu-id="b7c66-106">Cmdleten **Remove-AzureRmServiceBusTopicAuthorizationRule** tar bort auktoriseringsregeln för ett ämne från det angivna tjänst buss namn området.</span><span class="sxs-lookup"><span data-stu-id="b7c66-106">The **Remove-AzureRmServiceBusTopicAuthorizationRule** cmdlet removes the authorization rule of a topic from the specified Service Bus namespace.</span></span>

## <span data-ttu-id="b7c66-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b7c66-107">EXAMPLES</span></span>

### <span data-ttu-id="b7c66-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="b7c66-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmServiceBusTopicAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -AuthorizationRuleName SBTopicAuthoRule1
```

<span data-ttu-id="b7c66-109">Tar bort auktoriseringsregeln `SBTopicAuthoRule1` för avsnittet `SB-Topic_exampl1` från namn området `SB-Example1` .</span><span class="sxs-lookup"><span data-stu-id="b7c66-109">Removes the authorization rule `SBTopicAuthoRule1` of the topic `SB-Topic_exampl1` from the namespace `SB-Example1`.</span></span>

## <span data-ttu-id="b7c66-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b7c66-110">PARAMETERS</span></span>

### <span data-ttu-id="b7c66-111">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="b7c66-111">-ResourceGroup</span></span>
<span data-ttu-id="b7c66-112">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="b7c66-112">The name of the resource group.</span></span>

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

### <span data-ttu-id="b7c66-113">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="b7c66-113">-Confirm</span></span>
<span data-ttu-id="b7c66-114">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="b7c66-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b7c66-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b7c66-115">-WhatIf</span></span>
<span data-ttu-id="b7c66-116">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="b7c66-116">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b7c66-117">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="b7c66-117">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b7c66-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7c66-118">-DefaultProfile</span></span>
<span data-ttu-id="b7c66-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b7c66-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b7c66-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="b7c66-120">-Name</span></span>
<span data-ttu-id="b7c66-121">Ämnes namn för AuthorizationRule.</span><span class="sxs-lookup"><span data-stu-id="b7c66-121">Topic AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="b7c66-122">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="b7c66-122">-Namespace</span></span>
<span data-ttu-id="b7c66-123">Namn på namn området.</span><span class="sxs-lookup"><span data-stu-id="b7c66-123">Namespace Name.</span></span>

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

### <span data-ttu-id="b7c66-124">-Ämne</span><span class="sxs-lookup"><span data-stu-id="b7c66-124">-Topic</span></span>
<span data-ttu-id="b7c66-125">Avsnitts namn.</span><span class="sxs-lookup"><span data-stu-id="b7c66-125">Topic Name.</span></span>

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

### <span data-ttu-id="b7c66-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7c66-126">CommonParameters</span></span>
<span data-ttu-id="b7c66-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b7c66-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7c66-128">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b7c66-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7c66-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b7c66-129">INPUTS</span></span>

### <span data-ttu-id="b7c66-130">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="b7c66-130">-ResourceGroup</span></span>
 <span data-ttu-id="b7c66-131">System. String</span><span class="sxs-lookup"><span data-stu-id="b7c66-131">System.String</span></span>

### <span data-ttu-id="b7c66-132">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="b7c66-132">-NamespaceName</span></span>
 <span data-ttu-id="b7c66-133">System. String</span><span class="sxs-lookup"><span data-stu-id="b7c66-133">System.String</span></span>

### <span data-ttu-id="b7c66-134">-TopicName</span><span class="sxs-lookup"><span data-stu-id="b7c66-134">-TopicName</span></span>
 <span data-ttu-id="b7c66-135">System. String</span><span class="sxs-lookup"><span data-stu-id="b7c66-135">System.String</span></span>

### <span data-ttu-id="b7c66-136">-AuthorizationRuleName</span><span class="sxs-lookup"><span data-stu-id="b7c66-136">-AuthorizationRuleName</span></span>
 <span data-ttu-id="b7c66-137">System. String</span><span class="sxs-lookup"><span data-stu-id="b7c66-137">System.String</span></span>

## <span data-ttu-id="b7c66-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b7c66-138">OUTPUTS</span></span>

### <span data-ttu-id="b7c66-139">System. Object</span><span class="sxs-lookup"><span data-stu-id="b7c66-139">System.Object</span></span>

## <span data-ttu-id="b7c66-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b7c66-140">NOTES</span></span>

## <span data-ttu-id="b7c66-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b7c66-141">RELATED LINKS</span></span>

