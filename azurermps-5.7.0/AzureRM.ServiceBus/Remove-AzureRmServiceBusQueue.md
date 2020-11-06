---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/remove-azurermservicebusqueue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusQueue.md
ms.openlocfilehash: 28c6bf4d463331755121e8a1ea14bf7f93407017
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93579388"
---
# <span data-ttu-id="db22e-101">Remove-AzureRmServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="db22e-101">Remove-AzureRmServiceBusQueue</span></span>

## <span data-ttu-id="db22e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="db22e-102">SYNOPSIS</span></span>
<span data-ttu-id="db22e-103">Tar bort kön från det angivna tjänst buss utrymmet.</span><span class="sxs-lookup"><span data-stu-id="db22e-103">Removes the queue from the specified Service Bus namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="db22e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="db22e-104">SYNTAX</span></span>

```
Remove-AzureRmServiceBusQueue [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="db22e-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="db22e-105">DESCRIPTION</span></span>
<span data-ttu-id="db22e-106">Cmdleten **Remove-AzureRmServiceBusQueue** tar bort kön från det angivna tjänst buss utrymmet.</span><span class="sxs-lookup"><span data-stu-id="db22e-106">The **Remove-AzureRmServiceBusQueue** cmdlet removes the queue from the specified Service Bus namespace.</span></span>

## <span data-ttu-id="db22e-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="db22e-107">EXAMPLES</span></span>

### <span data-ttu-id="db22e-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="db22e-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmServiceBusQueue -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -QueueName SB-Queue_exampl1
```

<span data-ttu-id="db22e-109">Tar bort kön `SB-Queue_exampl1` från namn området `SB-Example1` .</span><span class="sxs-lookup"><span data-stu-id="db22e-109">Removes the queue `SB-Queue_exampl1` from the namespace `SB-Example1`.</span></span>

## <span data-ttu-id="db22e-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="db22e-110">PARAMETERS</span></span>

### <span data-ttu-id="db22e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db22e-111">-DefaultProfile</span></span>
<span data-ttu-id="db22e-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="db22e-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="db22e-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="db22e-113">-Name</span></span>
<span data-ttu-id="db22e-114">Könamn.</span><span class="sxs-lookup"><span data-stu-id="db22e-114">Queue Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: QueueName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db22e-115">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="db22e-115">-Namespace</span></span>
<span data-ttu-id="db22e-116">Namn på namn området.</span><span class="sxs-lookup"><span data-stu-id="db22e-116">Namespace Name.</span></span>

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

### <span data-ttu-id="db22e-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="db22e-117">-ResourceGroupName</span></span>
<span data-ttu-id="db22e-118">Namnet på resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="db22e-118">The name of the resource group</span></span>

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

### <span data-ttu-id="db22e-119">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="db22e-119">-Confirm</span></span>
<span data-ttu-id="db22e-120">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="db22e-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="db22e-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="db22e-121">-WhatIf</span></span>
<span data-ttu-id="db22e-122">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="db22e-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="db22e-123">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="db22e-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="db22e-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db22e-124">CommonParameters</span></span>
<span data-ttu-id="db22e-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="db22e-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db22e-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="db22e-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db22e-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="db22e-127">INPUTS</span></span>

### <span data-ttu-id="db22e-128">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="db22e-128">-ResourceGroup</span></span>
 <span data-ttu-id="db22e-129">System. String</span><span class="sxs-lookup"><span data-stu-id="db22e-129">System.String</span></span>

### <span data-ttu-id="db22e-130">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="db22e-130">-NamespaceName</span></span>
 <span data-ttu-id="db22e-131">System. String</span><span class="sxs-lookup"><span data-stu-id="db22e-131">System.String</span></span>

### <span data-ttu-id="db22e-132">-QueueName</span><span class="sxs-lookup"><span data-stu-id="db22e-132">-QueueName</span></span>
 <span data-ttu-id="db22e-133">System. String</span><span class="sxs-lookup"><span data-stu-id="db22e-133">System.String</span></span>

## <span data-ttu-id="db22e-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="db22e-134">OUTPUTS</span></span>

### <span data-ttu-id="db22e-135">System. Object</span><span class="sxs-lookup"><span data-stu-id="db22e-135">System.Object</span></span>

## <span data-ttu-id="db22e-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="db22e-136">NOTES</span></span>

## <span data-ttu-id="db22e-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="db22e-137">RELATED LINKS</span></span>

