---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/remove-azurermeventhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHub.md
ms.openlocfilehash: b546c4f610bb6bc8021547fa5f7f0516ffbc2371
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93586104"
---
# <span data-ttu-id="c91ac-101">Remove-AzureRmEventHub</span><span class="sxs-lookup"><span data-stu-id="c91ac-101">Remove-AzureRmEventHub</span></span>

## <span data-ttu-id="c91ac-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c91ac-102">SYNOPSIS</span></span>
<span data-ttu-id="c91ac-103">Tar bort den angivna händelsehubben.</span><span class="sxs-lookup"><span data-stu-id="c91ac-103">Removes the specified Event Hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c91ac-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c91ac-104">SYNTAX</span></span>

```
Remove-AzureRmEventHub [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c91ac-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c91ac-105">DESCRIPTION</span></span>
<span data-ttu-id="c91ac-106">Remove-AzureRmEventHub cmdlet tar bort och tar bort den angivna händelsehubben från det angivna namn området.</span><span class="sxs-lookup"><span data-stu-id="c91ac-106">The Remove-AzureRmEventHub cmdlet removes and deletes the specified Event Hub from the given namespace.</span></span>

## <span data-ttu-id="c91ac-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c91ac-107">EXAMPLES</span></span>

### <span data-ttu-id="c91ac-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="c91ac-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmEventHub -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -Name MyEventHubName
```

<span data-ttu-id="c91ac-109">Tar bort Händelsehubben \` MyEventHubName \` .</span><span class="sxs-lookup"><span data-stu-id="c91ac-109">Removes the Event Hub \`MyEventHubName\`.</span></span>

## <span data-ttu-id="c91ac-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c91ac-110">PARAMETERS</span></span>

### <span data-ttu-id="c91ac-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c91ac-111">-DefaultProfile</span></span>
<span data-ttu-id="c91ac-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c91ac-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c91ac-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="c91ac-113">-Name</span></span>
<span data-ttu-id="c91ac-114">Namn på EventHub</span><span class="sxs-lookup"><span data-stu-id="c91ac-114">EventHub Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: EventHubName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c91ac-115">-Namnrymd</span><span class="sxs-lookup"><span data-stu-id="c91ac-115">-Namespace</span></span>
<span data-ttu-id="c91ac-116">Namn på namn området</span><span class="sxs-lookup"><span data-stu-id="c91ac-116">Namespace Name</span></span>

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

### <span data-ttu-id="c91ac-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c91ac-117">-ResourceGroupName</span></span>
<span data-ttu-id="c91ac-118">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="c91ac-118">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c91ac-119">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="c91ac-119">-Confirm</span></span>
<span data-ttu-id="c91ac-120">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="c91ac-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c91ac-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c91ac-121">-WhatIf</span></span>
<span data-ttu-id="c91ac-122">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="c91ac-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c91ac-123">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="c91ac-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c91ac-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c91ac-124">CommonParameters</span></span>
<span data-ttu-id="c91ac-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c91ac-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="c91ac-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c91ac-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c91ac-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c91ac-127">INPUTS</span></span>

### <span data-ttu-id="c91ac-128">System. String</span><span class="sxs-lookup"><span data-stu-id="c91ac-128">System.String</span></span>


## <span data-ttu-id="c91ac-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c91ac-129">OUTPUTS</span></span>

### <span data-ttu-id="c91ac-130">System. Object</span><span class="sxs-lookup"><span data-stu-id="c91ac-130">System.Object</span></span>

## <span data-ttu-id="c91ac-131">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c91ac-131">NOTES</span></span>

## <span data-ttu-id="c91ac-132">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c91ac-132">RELATED LINKS</span></span>
