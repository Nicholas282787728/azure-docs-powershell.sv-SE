---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: FCDCEF0B-6E2C-480E-9841-EF4E64D61D54
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageShare.md
gitcommit: https://github.com/Azure/azure-powershell/blob/173e94aec59d7f539b72e43e90e5e7f8ba5f62bc
ms.openlocfilehash: a1be5816427ac1aa91b9daa98701abaec044c20f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93586284"
---
# <span data-ttu-id="14219-101">New-AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="14219-101">New-AzureStorageShare</span></span>

## <span data-ttu-id="14219-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="14219-102">SYNOPSIS</span></span>
<span data-ttu-id="14219-103">Skapar en fil resurs.</span><span class="sxs-lookup"><span data-stu-id="14219-103">Creates a file share.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="14219-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="14219-104">SYNTAX</span></span>

```
New-AzureStorageShare [-Name] <String> [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="14219-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="14219-105">DESCRIPTION</span></span>
<span data-ttu-id="14219-106">Cmdleten **New-AzureStorageShare** skapar en fil resurs.</span><span class="sxs-lookup"><span data-stu-id="14219-106">The **New-AzureStorageShare** cmdlet creates a file share.</span></span>

## <span data-ttu-id="14219-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="14219-107">EXAMPLES</span></span>

### <span data-ttu-id="14219-108">Exempel 1: skapa en fil resurs</span><span class="sxs-lookup"><span data-stu-id="14219-108">Example 1: Create a file share</span></span>
```
PS C:\>New-AzureStorageShare -Name "ContosoShare06"
```

<span data-ttu-id="14219-109">Det här kommandot skapar en fil resurs med namnet ContosoShare06.</span><span class="sxs-lookup"><span data-stu-id="14219-109">This command creates a file share named ContosoShare06.</span></span>

## <span data-ttu-id="14219-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="14219-110">PARAMETERS</span></span>

### <span data-ttu-id="14219-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="14219-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="14219-112">Anger tids gräns för klient sidan, i sekunder, för en tjänst förfrågan.</span><span class="sxs-lookup"><span data-stu-id="14219-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="14219-113">Om det föregående samtalet inte fungerar under det angivna intervallet, försöker den här cmdleten igen.</span><span class="sxs-lookup"><span data-stu-id="14219-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="14219-114">Om denna cmdlet inte får ett lyckat svar innan intervallet går ut returneras ett fel.</span><span class="sxs-lookup"><span data-stu-id="14219-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14219-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="14219-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="14219-116">Anger maximalt antal samtidiga nätverks samtal.</span><span class="sxs-lookup"><span data-stu-id="14219-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="14219-117">Du kan använda den här parametern för att begränsa samtidigheten för att reglera den lokala processorn och bandbredds användning genom att ange det maximala antalet simultana nätverks samtal.</span><span class="sxs-lookup"><span data-stu-id="14219-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="14219-118">Det angivna värdet är ett absolut antal och multipliceras inte med antalet kärnor.</span><span class="sxs-lookup"><span data-stu-id="14219-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="14219-119">Den här parametern kan hjälpa till att minska nätverks anslutnings problem i miljöer med liten bandbredd, till exempel 100 kilobit per sekund.</span><span class="sxs-lookup"><span data-stu-id="14219-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="14219-120">Standardvärdet är 10.</span><span class="sxs-lookup"><span data-stu-id="14219-120">The default value is 10.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14219-121">-Kontext</span><span class="sxs-lookup"><span data-stu-id="14219-121">-Context</span></span>
<span data-ttu-id="14219-122">Anger en Azure Storage-kontext.</span><span class="sxs-lookup"><span data-stu-id="14219-122">Specifies an Azure storage context.</span></span>
<span data-ttu-id="14219-123">Använd cmdleten [New-AzureStorageContext](./New-AzureStorageContext.md) för att få en lagrings kontext.</span><span class="sxs-lookup"><span data-stu-id="14219-123">To obtain a storage context, use the [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet.</span></span>

```yaml
Type: IStorageContext
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="14219-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="14219-124">-Name</span></span>
<span data-ttu-id="14219-125">Anger namnet på en fil resurs.</span><span class="sxs-lookup"><span data-stu-id="14219-125">Specifies the name of a file share.</span></span>
<span data-ttu-id="14219-126">Denna cmdlet skapar en fil resurs som har det namn som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="14219-126">This cmdlet creates a file share that has the name that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="14219-127">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="14219-127">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="14219-128">Anger längden på tids gränsen för en server del av en begäran.</span><span class="sxs-lookup"><span data-stu-id="14219-128">Specifies the length of the time-out period for the server part of a request.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14219-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14219-129">CommonParameters</span></span>
<span data-ttu-id="14219-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="14219-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14219-131">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="14219-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14219-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="14219-132">INPUTS</span></span>

### <span data-ttu-id="14219-133">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="14219-133">IStorageContext</span></span>

<span data-ttu-id="14219-134">Parametern ' context ' godkänner värdet av typen ' IStorageContext ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="14219-134">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="14219-135">Strängvärdet</span><span class="sxs-lookup"><span data-stu-id="14219-135">String</span></span>

<span data-ttu-id="14219-136">Parametern "name" accepterar värdet för typen String från pipeline</span><span class="sxs-lookup"><span data-stu-id="14219-136">Parameter 'Name' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="14219-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="14219-137">OUTPUTS</span></span>

## <span data-ttu-id="14219-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="14219-138">NOTES</span></span>

## <span data-ttu-id="14219-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="14219-139">RELATED LINKS</span></span>

[<span data-ttu-id="14219-140">Get-AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="14219-140">Get-AzureStorageShare</span></span>](./Get-AzureStorageShare.md)

[<span data-ttu-id="14219-141">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="14219-141">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="14219-142">Remove-AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="14219-142">Remove-AzureStorageShare</span></span>](./Remove-AzureStorageShare.md)
