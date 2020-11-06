---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusQueue.md
ms.openlocfilehash: 8c5c614a041ff0e4ab9bc4fdc0aea944901d1efc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575839"
---
# <span data-ttu-id="01696-101">Remove-AzureRmServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="01696-101">Remove-AzureRmServiceBusQueue</span></span>

## <span data-ttu-id="01696-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="01696-102">SYNOPSIS</span></span>
<span data-ttu-id="01696-103">Tar bort kön från det angivna tjänst buss utrymmet.</span><span class="sxs-lookup"><span data-stu-id="01696-103">Removes the queue from the specified Service Bus namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="01696-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="01696-104">SYNTAX</span></span>

```
Remove-AzureRmServiceBusQueue -ResourceGroupName <String> -Namespace <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="01696-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="01696-105">DESCRIPTION</span></span>
<span data-ttu-id="01696-106">Cmdleten **Remove-AzureRmServiceBusQueue** tar bort kön från det angivna tjänst buss utrymmet.</span><span class="sxs-lookup"><span data-stu-id="01696-106">The **Remove-AzureRmServiceBusQueue** cmdlet removes the queue from the specified Service Bus namespace.</span></span>

## <span data-ttu-id="01696-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="01696-107">EXAMPLES</span></span>

### <span data-ttu-id="01696-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="01696-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmServiceBusQueue -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -QueueName SB-Queue_exampl1
```

<span data-ttu-id="01696-109">Tar bort kön `SB-Queue_exampl1` från namn området `SB-Example1` .</span><span class="sxs-lookup"><span data-stu-id="01696-109">Removes the queue `SB-Queue_exampl1` from the namespace `SB-Example1`.</span></span>

## <span data-ttu-id="01696-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="01696-110">PARAMETERS</span></span>

### <span data-ttu-id="01696-111">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="01696-111">-Confirm</span></span>
<span data-ttu-id="01696-112">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="01696-112">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="01696-113">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="01696-113">-WhatIf</span></span>
<span data-ttu-id="01696-114">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="01696-114">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="01696-115">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="01696-115">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="01696-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01696-116">-DefaultProfile</span></span>
<span data-ttu-id="01696-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="01696-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="01696-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="01696-118">-Name</span></span>
<span data-ttu-id="01696-119">Könamn.</span><span class="sxs-lookup"><span data-stu-id="01696-119">Queue Name.</span></span>

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

### <span data-ttu-id="01696-120">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="01696-120">-Namespace</span></span>
<span data-ttu-id="01696-121">Namn på namn området.</span><span class="sxs-lookup"><span data-stu-id="01696-121">Namespace Name.</span></span>

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

### <span data-ttu-id="01696-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="01696-122">-ResourceGroupName</span></span>
<span data-ttu-id="01696-123">Namnet på resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="01696-123">The name of the resource group</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="01696-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01696-124">CommonParameters</span></span>
<span data-ttu-id="01696-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="01696-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01696-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="01696-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01696-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="01696-127">INPUTS</span></span>

### <span data-ttu-id="01696-128">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="01696-128">-ResourceGroup</span></span>
 <span data-ttu-id="01696-129">System. String</span><span class="sxs-lookup"><span data-stu-id="01696-129">System.String</span></span>

### <span data-ttu-id="01696-130">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="01696-130">-NamespaceName</span></span>
 <span data-ttu-id="01696-131">System. String</span><span class="sxs-lookup"><span data-stu-id="01696-131">System.String</span></span>

### <span data-ttu-id="01696-132">-QueueName</span><span class="sxs-lookup"><span data-stu-id="01696-132">-QueueName</span></span>
 <span data-ttu-id="01696-133">System. String</span><span class="sxs-lookup"><span data-stu-id="01696-133">System.String</span></span>

## <span data-ttu-id="01696-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="01696-134">OUTPUTS</span></span>

### <span data-ttu-id="01696-135">System. Object</span><span class="sxs-lookup"><span data-stu-id="01696-135">System.Object</span></span>

## <span data-ttu-id="01696-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="01696-136">NOTES</span></span>

## <span data-ttu-id="01696-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="01696-137">RELATED LINKS</span></span>

