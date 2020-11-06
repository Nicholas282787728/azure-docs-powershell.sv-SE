---
external help file: Microsoft.Azure.Commands.EventGrid.dll-Help.xml
Module Name: AzureRM.EventGrid
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Get-AzureRmEventGridTopicType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Get-AzureRmEventGridTopicType.md
ms.openlocfilehash: 621fb15d3a83b7c704e5828d6541ad9d4404875c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93582447"
---
# <span data-ttu-id="4efba-101">Get-AzureRmEventGridTopicType</span><span class="sxs-lookup"><span data-stu-id="4efba-101">Get-AzureRmEventGridTopicType</span></span>

## <span data-ttu-id="4efba-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4efba-102">SYNOPSIS</span></span>
<span data-ttu-id="4efba-103">Hämtar information om de avsnitts typer som stöds av Azure Event-rutnät.</span><span class="sxs-lookup"><span data-stu-id="4efba-103">Gets the details about the topic types supported by Azure Event Grid.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4efba-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4efba-104">SYNTAX</span></span>

```
Get-AzureRmEventGridTopicType [[-Name] <String>] [-IncludeEventTypeData]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4efba-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4efba-105">DESCRIPTION</span></span>
<span data-ttu-id="4efba-106">Hämtar information om vilka avsnitts typer som stöds av Azure Event-rutnät.</span><span class="sxs-lookup"><span data-stu-id="4efba-106">Gets the details of topic types supported by Azure Event Grid.</span></span>
<span data-ttu-id="4efba-107">Om ett namn för ämnes typen anges returneras information om den typen.</span><span class="sxs-lookup"><span data-stu-id="4efba-107">If a topic type name is specified, details about that topic type are returned.</span></span>
<span data-ttu-id="4efba-108">Om du inte har angett ett namn för ämnes typen returneras information om alla avsnitts typer.</span><span class="sxs-lookup"><span data-stu-id="4efba-108">If a topic type name is not specified, details about all topic types are returned.</span></span>
<span data-ttu-id="4efba-109">Om IncludeEventTypes anges ingår information om de händelse typer som stöds av varje typ av ämne i svaret.</span><span class="sxs-lookup"><span data-stu-id="4efba-109">If IncludeEventTypes is specified, information about event types supported by each topic type is included in the response.</span></span>

## <span data-ttu-id="4efba-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4efba-110">EXAMPLES</span></span>

### <span data-ttu-id="4efba-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="4efba-111">Example 1</span></span>
```
PS C:\> Get-AzureRmEventGridTopicType
```

<span data-ttu-id="4efba-112">Hämtar en lista med ämnes typer.</span><span class="sxs-lookup"><span data-stu-id="4efba-112">Gets a list of the topic types.</span></span>

### <span data-ttu-id="4efba-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="4efba-113">Example 2</span></span>
```
PS C:\> Get-AzureRmEventGridTopicType -Name "Microsoft.Storage.StorageAccounts"
```

<span data-ttu-id="4efba-114">Hämtar information om StorageAccounts.</span><span class="sxs-lookup"><span data-stu-id="4efba-114">Gets information about the StorageAccounts topic type.</span></span>

### <span data-ttu-id="4efba-115">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="4efba-115">Example 3</span></span>
```
PS C:\> Get-AzureRmEventGridTopicType -Name "Microsoft.Storage.StorageAccounts" -IncludeEventTypeData
```

<span data-ttu-id="4efba-116">Hämtar information om StorageAccounts, inklusive de händelse typer som stöds av StorageAccounts.</span><span class="sxs-lookup"><span data-stu-id="4efba-116">Gets information about the StorageAccounts topic type, including the event types supported by StorageAccounts.</span></span>

## <span data-ttu-id="4efba-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4efba-117">PARAMETERS</span></span>

### <span data-ttu-id="4efba-118">-IncludeEventTypeData</span><span class="sxs-lookup"><span data-stu-id="4efba-118">-IncludeEventTypeData</span></span>
<span data-ttu-id="4efba-119">Om det här alternativet anges innehåller svaret de händelse typer som stöds av en typ av ämne.</span><span class="sxs-lookup"><span data-stu-id="4efba-119">If specified, the response will include the event types supported by a topic type.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4efba-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="4efba-120">-Name</span></span>
<span data-ttu-id="4efba-121">EventGrid namn på ämnes typen.</span><span class="sxs-lookup"><span data-stu-id="4efba-121">EventGrid Topic Type Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4efba-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4efba-122">-DefaultProfile</span></span>
<span data-ttu-id="4efba-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="4efba-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4efba-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4efba-124">CommonParameters</span></span>
<span data-ttu-id="4efba-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4efba-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4efba-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4efba-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4efba-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4efba-127">INPUTS</span></span>

### <span data-ttu-id="4efba-128">System. String</span><span class="sxs-lookup"><span data-stu-id="4efba-128">System.String</span></span>
<span data-ttu-id="4efba-129">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="4efba-129">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="4efba-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4efba-130">OUTPUTS</span></span>

### <span data-ttu-id="4efba-131">System. Collections. Generic. list ' 1 [[Microsoft. Azure. commands. EventGrid. Models. PSTopicTypeInfoListInstance, Microsoft. Azure. commands. EventGrid, version = 1.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="4efba-131">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.EventGrid.Models.PSTopicTypeInfoListInstance, Microsoft.Azure.Commands.EventGrid, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="4efba-132">Microsoft. Azure. commands. EventGrid. Models. PSTopicTypeInfo</span><span class="sxs-lookup"><span data-stu-id="4efba-132">Microsoft.Azure.Commands.EventGrid.Models.PSTopicTypeInfo</span></span>

## <span data-ttu-id="4efba-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4efba-133">NOTES</span></span>

## <span data-ttu-id="4efba-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4efba-134">RELATED LINKS</span></span>

