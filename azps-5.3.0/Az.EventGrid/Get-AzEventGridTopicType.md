---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/get-azeventgridtopictype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridTopicType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridTopicType.md
ms.openlocfilehash: e2cd8cfeadf0c9574cbf39a642133109aa02ec39
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98520828"
---
# <span data-ttu-id="4a10b-101">Get-AzEventGridTopicType</span><span class="sxs-lookup"><span data-stu-id="4a10b-101">Get-AzEventGridTopicType</span></span>

## <span data-ttu-id="4a10b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4a10b-102">SYNOPSIS</span></span>
<span data-ttu-id="4a10b-103">Hämtar information om de avsnitts typer som stöds av Azure Event-rutnät.</span><span class="sxs-lookup"><span data-stu-id="4a10b-103">Gets the details about the topic types supported by Azure Event Grid.</span></span>

## <span data-ttu-id="4a10b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4a10b-104">SYNTAX</span></span>

```
Get-AzEventGridTopicType [-Name <String>] [-IncludeEventTypeData] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4a10b-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4a10b-105">DESCRIPTION</span></span>
<span data-ttu-id="4a10b-106">Hämtar information om vilka avsnitts typer som stöds av Azure Event-rutnät.</span><span class="sxs-lookup"><span data-stu-id="4a10b-106">Gets the details of topic types supported by Azure Event Grid.</span></span>
<span data-ttu-id="4a10b-107">Om ett namn för ämnes typen anges returneras information om den typen.</span><span class="sxs-lookup"><span data-stu-id="4a10b-107">If a topic type name is specified, details about that topic type are returned.</span></span>
<span data-ttu-id="4a10b-108">Om du inte har angett ett namn för ämnes typen returneras information om alla avsnitts typer.</span><span class="sxs-lookup"><span data-stu-id="4a10b-108">If a topic type name is not specified, details about all topic types are returned.</span></span>
<span data-ttu-id="4a10b-109">Om IncludeEventTypes anges ingår information om de händelse typer som stöds av varje typ av ämne i svaret.</span><span class="sxs-lookup"><span data-stu-id="4a10b-109">If IncludeEventTypes is specified, information about event types supported by each topic type is included in the response.</span></span>

## <span data-ttu-id="4a10b-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4a10b-110">EXAMPLES</span></span>

### <span data-ttu-id="4a10b-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="4a10b-111">Example 1</span></span>
```powershell
PS C:\> Get-AzEventGridTopicType
```

<span data-ttu-id="4a10b-112">Hämtar en lista med ämnes typer.</span><span class="sxs-lookup"><span data-stu-id="4a10b-112">Gets a list of the topic types.</span></span>

### <span data-ttu-id="4a10b-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="4a10b-113">Example 2</span></span>
```powershell
PS C:\> Get-AzEventGridTopicType -Name "Microsoft.Storage.StorageAccounts"
```

<span data-ttu-id="4a10b-114">Hämtar information om StorageAccounts.</span><span class="sxs-lookup"><span data-stu-id="4a10b-114">Gets information about the StorageAccounts topic type.</span></span>

### <span data-ttu-id="4a10b-115">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="4a10b-115">Example 3</span></span>
```powershell
PS C:\> Get-AzEventGridTopicType -Name "Microsoft.Storage.StorageAccounts" -IncludeEventTypeData
```

<span data-ttu-id="4a10b-116">Hämtar information om StorageAccounts, inklusive de händelse typer som stöds av StorageAccounts.</span><span class="sxs-lookup"><span data-stu-id="4a10b-116">Gets information about the StorageAccounts topic type, including the event types supported by StorageAccounts.</span></span>

## <span data-ttu-id="4a10b-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4a10b-117">PARAMETERS</span></span>

### <span data-ttu-id="4a10b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a10b-118">-DefaultProfile</span></span>
<span data-ttu-id="4a10b-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="4a10b-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4a10b-120">-IncludeEventTypeData</span><span class="sxs-lookup"><span data-stu-id="4a10b-120">-IncludeEventTypeData</span></span>
<span data-ttu-id="4a10b-121">Om det här alternativet anges innehåller svaret de händelse typer som stöds av en typ av ämne.</span><span class="sxs-lookup"><span data-stu-id="4a10b-121">If specified, the response will include the event types supported by a topic type.</span></span>

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

### <span data-ttu-id="4a10b-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="4a10b-122">-Name</span></span>
<span data-ttu-id="4a10b-123">EventGrid namn på ämnes typen.</span><span class="sxs-lookup"><span data-stu-id="4a10b-123">EventGrid Topic Type Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4a10b-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a10b-124">CommonParameters</span></span>
<span data-ttu-id="4a10b-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4a10b-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a10b-126">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4a10b-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a10b-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4a10b-127">INPUTS</span></span>

### <span data-ttu-id="4a10b-128">System. String</span><span class="sxs-lookup"><span data-stu-id="4a10b-128">System.String</span></span>

## <span data-ttu-id="4a10b-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4a10b-129">OUTPUTS</span></span>

### <span data-ttu-id="4a10b-130">Microsoft. Azure. commands. EventGrid. Models. PSTopicTypeInfoListInstance</span><span class="sxs-lookup"><span data-stu-id="4a10b-130">Microsoft.Azure.Commands.EventGrid.Models.PSTopicTypeInfoListInstance</span></span>

### <span data-ttu-id="4a10b-131">Microsoft. Azure. commands. EventGrid. Models. PSTopicTypeInfo</span><span class="sxs-lookup"><span data-stu-id="4a10b-131">Microsoft.Azure.Commands.EventGrid.Models.PSTopicTypeInfo</span></span>

## <span data-ttu-id="4a10b-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4a10b-132">NOTES</span></span>

## <span data-ttu-id="4a10b-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4a10b-133">RELATED LINKS</span></span>
