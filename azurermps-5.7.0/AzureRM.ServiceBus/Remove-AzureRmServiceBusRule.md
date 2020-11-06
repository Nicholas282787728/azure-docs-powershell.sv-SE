---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/remove-azurermservicebusrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusRule.md
ms.openlocfilehash: 08f3fb2654d4c0b64900a4f15bbb7816e6d44c6f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93579391"
---
# <span data-ttu-id="c0d11-101">Remove-AzureRmServiceBusRule</span><span class="sxs-lookup"><span data-stu-id="c0d11-101">Remove-AzureRmServiceBusRule</span></span>

## <span data-ttu-id="c0d11-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c0d11-102">SYNOPSIS</span></span>
<span data-ttu-id="c0d11-103">Tar bort speficied-regeln för en given prenumeration.</span><span class="sxs-lookup"><span data-stu-id="c0d11-103">Removes the speficied rule of a given subscription .</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c0d11-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c0d11-104">SYNTAX</span></span>

```
Remove-AzureRmServiceBusRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Subscription] <String> [-Name] <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c0d11-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c0d11-105">DESCRIPTION</span></span>
<span data-ttu-id="c0d11-106">Cmdleten **Remove-AzureRmServiceBusRule** tar bort regeln för ett visst ämne.</span><span class="sxs-lookup"><span data-stu-id="c0d11-106">The **Remove-AzureRmServiceBusRule** cmdlet removes the rule of a subscription of given topic.</span></span>

## <span data-ttu-id="c0d11-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c0d11-107">EXAMPLES</span></span>

### <span data-ttu-id="c0d11-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="c0d11-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -Name SBRule
```

<span data-ttu-id="c0d11-109">Tar bort regeln `SBRule` för prenumeration `SBSubscription` av angivet ämne `SBTopic` .</span><span class="sxs-lookup"><span data-stu-id="c0d11-109">Removes the rule `SBRule` of subscription `SBSubscription` of specified topic `SBTopic`.</span></span>

## <span data-ttu-id="c0d11-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c0d11-110">PARAMETERS</span></span>

### <span data-ttu-id="c0d11-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0d11-111">-DefaultProfile</span></span>
<span data-ttu-id="c0d11-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c0d11-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c0d11-113">-Force</span><span class="sxs-lookup"><span data-stu-id="c0d11-113">-Force</span></span>
<span data-ttu-id="c0d11-114">Fråga inte efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="c0d11-114">Do not ask for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0d11-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="c0d11-115">-Name</span></span>
<span data-ttu-id="c0d11-116">Regel namn.</span><span class="sxs-lookup"><span data-stu-id="c0d11-116">Rule Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c0d11-117">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="c0d11-117">-Namespace</span></span>
<span data-ttu-id="c0d11-118">Namn på namn området.</span><span class="sxs-lookup"><span data-stu-id="c0d11-118">Namespace Name.</span></span>

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

### <span data-ttu-id="c0d11-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c0d11-119">-PassThru</span></span>
<span data-ttu-id="c0d11-120">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="c0d11-120">{{Fill PassThru Description}}</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0d11-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c0d11-121">-ResourceGroupName</span></span>
<span data-ttu-id="c0d11-122">Namnet på resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="c0d11-122">The name of the resource group</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c0d11-123">-Abonnemang</span><span class="sxs-lookup"><span data-stu-id="c0d11-123">-Subscription</span></span>
<span data-ttu-id="c0d11-124">Prenumerationens namn.</span><span class="sxs-lookup"><span data-stu-id="c0d11-124">Subscription Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SubscriptionName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c0d11-125">-Ämne</span><span class="sxs-lookup"><span data-stu-id="c0d11-125">-Topic</span></span>
<span data-ttu-id="c0d11-126">Avsnitts namn.</span><span class="sxs-lookup"><span data-stu-id="c0d11-126">Topic Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: TopicName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c0d11-127">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="c0d11-127">-Confirm</span></span>
<span data-ttu-id="c0d11-128">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="c0d11-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0d11-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c0d11-129">-WhatIf</span></span>
<span data-ttu-id="c0d11-130">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="c0d11-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c0d11-131">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="c0d11-131">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0d11-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0d11-132">CommonParameters</span></span>
<span data-ttu-id="c0d11-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c0d11-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0d11-134">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c0d11-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0d11-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c0d11-135">INPUTS</span></span>

### <span data-ttu-id="c0d11-136">System. String</span><span class="sxs-lookup"><span data-stu-id="c0d11-136">System.String</span></span>

## <span data-ttu-id="c0d11-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c0d11-137">OUTPUTS</span></span>

### <span data-ttu-id="c0d11-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c0d11-138">System.Boolean</span></span>

## <span data-ttu-id="c0d11-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c0d11-139">NOTES</span></span>

## <span data-ttu-id="c0d11-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c0d11-140">RELATED LINKS</span></span>

