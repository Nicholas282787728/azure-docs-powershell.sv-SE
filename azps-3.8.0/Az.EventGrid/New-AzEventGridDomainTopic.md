---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/new-azeventgriddomaintopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridDomainTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridDomainTopic.md
ms.openlocfilehash: f7870ec0d8cb75b760faab037f85f36aae88e203
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93927641"
---
# <span data-ttu-id="20d89-101">New-AzEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="20d89-101">New-AzEventGridDomainTopic</span></span>

## <span data-ttu-id="20d89-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="20d89-102">SYNOPSIS</span></span>
<span data-ttu-id="20d89-103">Skapar ett nytt avsnitt i en Azure Event Grid-domän.</span><span class="sxs-lookup"><span data-stu-id="20d89-103">Creates a new Azure Event Grid Domain Topic.</span></span>

## <span data-ttu-id="20d89-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="20d89-104">SYNTAX</span></span>

```
New-AzEventGridDomainTopic [-ResourceGroupName] <String> [-DomainName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="20d89-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="20d89-105">DESCRIPTION</span></span>
<span data-ttu-id="20d89-106">Skapar ett nytt avsnitt i en Azure Event Grid-domän.</span><span class="sxs-lookup"><span data-stu-id="20d89-106">Creates a new Azure Event Grid Domain Topic.</span></span>

## <span data-ttu-id="20d89-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="20d89-107">EXAMPLES</span></span>

### <span data-ttu-id="20d89-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="20d89-108">Example 1</span></span>

<span data-ttu-id="20d89-109">Skapar ett ämne \` för en Ämne1 \` i domänen \` domain1 \` under resurs grupps \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="20d89-109">Creates an Event Grid Domain Topic \`Topic1\` in Domain \`Domain1\` under resource group \`MyResourceGroupName\`.</span></span>

```powershell
PS C:\> New-AzEventGridDomainTopic -ResourceGroupName MyResourceGroupName -DomainName Domain1 -Name Topic1

ResourceGroupName : MyResourceGroupName
DomainName        : Domain1
DomainTopicName   : topic1
Id                : /subscriptions/<Azure Subscription Id>/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1/topics/topic1
Type              : Microsoft.EventGrid/domains/topics
ProvisioningState : Succeeded
```

## <span data-ttu-id="20d89-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="20d89-110">PARAMETERS</span></span>

### <span data-ttu-id="20d89-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20d89-111">-DefaultProfile</span></span>
<span data-ttu-id="20d89-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="20d89-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="20d89-113">-Domän namn</span><span class="sxs-lookup"><span data-stu-id="20d89-113">-DomainName</span></span>
<span data-ttu-id="20d89-114">EventGrid domän namn.</span><span class="sxs-lookup"><span data-stu-id="20d89-114">EventGrid domain name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Domain

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="20d89-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="20d89-115">-Name</span></span>
<span data-ttu-id="20d89-116">Namn på EventGrid-domän.</span><span class="sxs-lookup"><span data-stu-id="20d89-116">EventGrid domain topic name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DomainTopicName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="20d89-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="20d89-117">-ResourceGroupName</span></span>
<span data-ttu-id="20d89-118">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="20d89-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="20d89-119">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="20d89-119">-Confirm</span></span>
<span data-ttu-id="20d89-120">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="20d89-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="20d89-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="20d89-121">-WhatIf</span></span>
<span data-ttu-id="20d89-122">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="20d89-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="20d89-123">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="20d89-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="20d89-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20d89-124">CommonParameters</span></span>
<span data-ttu-id="20d89-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="20d89-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20d89-126">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="20d89-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20d89-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="20d89-127">INPUTS</span></span>

### <span data-ttu-id="20d89-128">System. String</span><span class="sxs-lookup"><span data-stu-id="20d89-128">System.String</span></span>

## <span data-ttu-id="20d89-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="20d89-129">OUTPUTS</span></span>

### <span data-ttu-id="20d89-130">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic</span><span class="sxs-lookup"><span data-stu-id="20d89-130">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic</span></span>

## <span data-ttu-id="20d89-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="20d89-131">NOTES</span></span>

## <span data-ttu-id="20d89-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="20d89-132">RELATED LINKS</span></span>