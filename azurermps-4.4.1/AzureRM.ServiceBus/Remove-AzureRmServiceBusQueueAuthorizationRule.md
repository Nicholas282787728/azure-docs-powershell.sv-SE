---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusQueueAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusQueueAuthorizationRule.md
ms.openlocfilehash: 93efa23e802c3470d1bd1470cadd0f070cc34422
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575840"
---
# <span data-ttu-id="d19ef-101">Remove-AzureRmServiceBusQueueAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="d19ef-101">Remove-AzureRmServiceBusQueueAuthorizationRule</span></span>

## <span data-ttu-id="d19ef-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d19ef-102">SYNOPSIS</span></span>
<span data-ttu-id="d19ef-103">Tar bort auktoriseringsregeln för en kö från det angivna Service Bus-namnområdet.</span><span class="sxs-lookup"><span data-stu-id="d19ef-103">Removes the authorization rule of a queue from the specified Service Bus namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d19ef-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d19ef-104">SYNTAX</span></span>

```
Remove-AzureRmServiceBusQueueAuthorizationRule [-ResourceGroup] <String> -Namespace <String> -Queue <String>
 -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d19ef-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d19ef-105">DESCRIPTION</span></span>
<span data-ttu-id="d19ef-106">Cmdleten **Remove-AzureRmServiceBusQueueAuthorizationRule** tar bort auktoriseringsregeln för en kö från det angivna Service Bus-namnområdet.</span><span class="sxs-lookup"><span data-stu-id="d19ef-106">The **Remove-AzureRmServiceBusQueueAuthorizationRule** cmdlet removes the authorization rule of a queue from the specified Service Bus namespace.</span></span>

## <span data-ttu-id="d19ef-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d19ef-107">EXAMPLES</span></span>

### <span data-ttu-id="d19ef-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="d19ef-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmServiceBusQueueAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -QueueName SB-Queue_exampl1 -AuthorizationRuleName SBAuthoRule1
```

<span data-ttu-id="d19ef-109">Tar bort auktoriseringsregeln `SBAuthoRule1` för kön `SB-Queue_exampl1` från namn området `SB-Example1` .</span><span class="sxs-lookup"><span data-stu-id="d19ef-109">Removes the authorization rule `SBAuthoRule1` of the queue `SB-Queue_exampl1` from the namespace `SB-Example1`.</span></span>

## <span data-ttu-id="d19ef-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d19ef-110">PARAMETERS</span></span>

### <span data-ttu-id="d19ef-111">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="d19ef-111">-ResourceGroup</span></span>
<span data-ttu-id="d19ef-112">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="d19ef-112">The name of the resource group.</span></span>

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

### <span data-ttu-id="d19ef-113">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="d19ef-113">-Confirm</span></span>
<span data-ttu-id="d19ef-114">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="d19ef-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d19ef-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d19ef-115">-WhatIf</span></span>
<span data-ttu-id="d19ef-116">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="d19ef-116">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d19ef-117">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="d19ef-117">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d19ef-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d19ef-118">-DefaultProfile</span></span>
<span data-ttu-id="d19ef-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d19ef-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d19ef-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="d19ef-120">-Name</span></span>
<span data-ttu-id="d19ef-121">AuthorizationRule namn på kö.</span><span class="sxs-lookup"><span data-stu-id="d19ef-121">Queue AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="d19ef-122">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="d19ef-122">-Namespace</span></span>
<span data-ttu-id="d19ef-123">Namn på namn området.</span><span class="sxs-lookup"><span data-stu-id="d19ef-123">Namespace Name.</span></span>

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

### <span data-ttu-id="d19ef-124">-Kö</span><span class="sxs-lookup"><span data-stu-id="d19ef-124">-Queue</span></span>
<span data-ttu-id="d19ef-125">Könamn.</span><span class="sxs-lookup"><span data-stu-id="d19ef-125">Queue Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: QueueName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d19ef-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d19ef-126">CommonParameters</span></span>
<span data-ttu-id="d19ef-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d19ef-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d19ef-128">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d19ef-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d19ef-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d19ef-129">INPUTS</span></span>

### <span data-ttu-id="d19ef-130">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="d19ef-130">-ResourceGroup</span></span>
 <span data-ttu-id="d19ef-131">System. String</span><span class="sxs-lookup"><span data-stu-id="d19ef-131">System.String</span></span>

### <span data-ttu-id="d19ef-132">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="d19ef-132">-NamespaceName</span></span>
 <span data-ttu-id="d19ef-133">System. String</span><span class="sxs-lookup"><span data-stu-id="d19ef-133">System.String</span></span>

### <span data-ttu-id="d19ef-134">-QueueName</span><span class="sxs-lookup"><span data-stu-id="d19ef-134">-QueueName</span></span>
 <span data-ttu-id="d19ef-135">System. String</span><span class="sxs-lookup"><span data-stu-id="d19ef-135">System.String</span></span>

### <span data-ttu-id="d19ef-136">-AuthorizationRuleName</span><span class="sxs-lookup"><span data-stu-id="d19ef-136">-AuthorizationRuleName</span></span>
 <span data-ttu-id="d19ef-137">System. String</span><span class="sxs-lookup"><span data-stu-id="d19ef-137">System.String</span></span>

## <span data-ttu-id="d19ef-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d19ef-138">OUTPUTS</span></span>

### <span data-ttu-id="d19ef-139">System. Object</span><span class="sxs-lookup"><span data-stu-id="d19ef-139">System.Object</span></span>

## <span data-ttu-id="d19ef-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d19ef-140">NOTES</span></span>

## <span data-ttu-id="d19ef-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d19ef-141">RELATED LINKS</span></span>

