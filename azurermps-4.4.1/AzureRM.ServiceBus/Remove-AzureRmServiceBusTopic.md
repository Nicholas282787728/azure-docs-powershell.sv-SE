---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusTopic.md
ms.openlocfilehash: 356140c964280634f469dd9b9955adaf62130090
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574515"
---
# <span data-ttu-id="7b1ca-101">Remove-AzureRmServiceBusTopic</span><span class="sxs-lookup"><span data-stu-id="7b1ca-101">Remove-AzureRmServiceBusTopic</span></span>

## <span data-ttu-id="7b1ca-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7b1ca-102">SYNOPSIS</span></span>
<span data-ttu-id="7b1ca-103">Tar bort avsnittet från det angivna Service Bus-namnområdet.</span><span class="sxs-lookup"><span data-stu-id="7b1ca-103">Removes the topic from the specified Service Bus namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7b1ca-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7b1ca-104">SYNTAX</span></span>

```
Remove-AzureRmServiceBusTopic -ResourceGroupName <String> -Namespace <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7b1ca-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7b1ca-105">DESCRIPTION</span></span>
<span data-ttu-id="7b1ca-106">Cmdleten **Remove-AzureRmServiceBusTopic** tar bort avsnittet från det angivna tjänst buss namn området.</span><span class="sxs-lookup"><span data-stu-id="7b1ca-106">The **Remove-AzureRmServiceBusTopic** cmdlet removes the topic from the specified Service Bus namespace.</span></span>

## <span data-ttu-id="7b1ca-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7b1ca-107">EXAMPLES</span></span>

### <span data-ttu-id="7b1ca-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="7b1ca-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmServiceBusTopic -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1
```

<span data-ttu-id="7b1ca-109">Tar bort avsnittet `SB-Topic_exampl1` från namn området `SB-Example1` .</span><span class="sxs-lookup"><span data-stu-id="7b1ca-109">Removes the topic `SB-Topic_exampl1` from the namespace `SB-Example1`.</span></span>

## <span data-ttu-id="7b1ca-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7b1ca-110">PARAMETERS</span></span>

### <span data-ttu-id="7b1ca-111">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="7b1ca-111">-Confirm</span></span>
<span data-ttu-id="7b1ca-112">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="7b1ca-112">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7b1ca-113">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7b1ca-113">-WhatIf</span></span>
<span data-ttu-id="7b1ca-114">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="7b1ca-114">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7b1ca-115">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="7b1ca-115">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7b1ca-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b1ca-116">-DefaultProfile</span></span>
<span data-ttu-id="7b1ca-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="7b1ca-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7b1ca-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="7b1ca-118">-Name</span></span>
<span data-ttu-id="7b1ca-119">Avsnitts namn.</span><span class="sxs-lookup"><span data-stu-id="7b1ca-119">Topic Name.</span></span>

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

### <span data-ttu-id="7b1ca-120">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="7b1ca-120">-Namespace</span></span>
<span data-ttu-id="7b1ca-121">Namn på namn området.</span><span class="sxs-lookup"><span data-stu-id="7b1ca-121">Namespace Name.</span></span>

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

### <span data-ttu-id="7b1ca-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7b1ca-122">-ResourceGroupName</span></span>
<span data-ttu-id="7b1ca-123">Namnet på resurs gruppen</span><span class="sxs-lookup"><span data-stu-id="7b1ca-123">The name of the resource group</span></span>

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

### <span data-ttu-id="7b1ca-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b1ca-124">CommonParameters</span></span>
<span data-ttu-id="7b1ca-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7b1ca-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b1ca-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7b1ca-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b1ca-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7b1ca-127">INPUTS</span></span>

### <span data-ttu-id="7b1ca-128">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="7b1ca-128">-ResourceGroup</span></span>
 <span data-ttu-id="7b1ca-129">System. String</span><span class="sxs-lookup"><span data-stu-id="7b1ca-129">System.String</span></span>

### <span data-ttu-id="7b1ca-130">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="7b1ca-130">-NamespaceName</span></span>
 <span data-ttu-id="7b1ca-131">System. String</span><span class="sxs-lookup"><span data-stu-id="7b1ca-131">System.String</span></span>

### <span data-ttu-id="7b1ca-132">-TopicName</span><span class="sxs-lookup"><span data-stu-id="7b1ca-132">-TopicName</span></span>
 <span data-ttu-id="7b1ca-133">System. String</span><span class="sxs-lookup"><span data-stu-id="7b1ca-133">System.String</span></span>

## <span data-ttu-id="7b1ca-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7b1ca-134">OUTPUTS</span></span>

### <span data-ttu-id="7b1ca-135">System. Object</span><span class="sxs-lookup"><span data-stu-id="7b1ca-135">System.Object</span></span>

## <span data-ttu-id="7b1ca-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7b1ca-136">NOTES</span></span>

## <span data-ttu-id="7b1ca-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7b1ca-137">RELATED LINKS</span></span>

