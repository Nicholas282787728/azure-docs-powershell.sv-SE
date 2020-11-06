---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 26E06BA3-C550-40A5-B8E3-FEC8E9BF3867
online version: ''
schema: 2.0.0
ms.openlocfilehash: 27237a00866c42d5e7eb587267ad6573cbd6cac7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93571368"
---
# <span data-ttu-id="f302d-101">Remove-AzureStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="f302d-101">Remove-AzureStorageCORSRule</span></span>

## <span data-ttu-id="f302d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f302d-102">SYNOPSIS</span></span>
<span data-ttu-id="f302d-103">Tar bort CORS för en lagrings tjänst.</span><span class="sxs-lookup"><span data-stu-id="f302d-103">Removes CORS for a Storage service.</span></span>

## <span data-ttu-id="f302d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f302d-104">SYNTAX</span></span>

```
Remove-AzureStorageCORSRule [-ServiceType] <StorageServiceType> [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

## <span data-ttu-id="f302d-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f302d-105">DESCRIPTION</span></span>
<span data-ttu-id="f302d-106">Cmdleten **Remove-AzureStorageCORSRule** tar bort resurs delning av över-ursprung (CORS) för en Azure Storage-tjänst.</span><span class="sxs-lookup"><span data-stu-id="f302d-106">The **Remove-AzureStorageCORSRule** cmdlet removes Cross-Origin Resource Sharing (CORS) for an Azure Storage service.</span></span>
<span data-ttu-id="f302d-107">Denna cmdlet tar bort alla CORS-regler i en lagrings tjänst typ.</span><span class="sxs-lookup"><span data-stu-id="f302d-107">This cmdlet deletes all CORS rules in a Storage service type.</span></span>
<span data-ttu-id="f302d-108">Typerna av lagrings tjänster för denna cmdlet är BLOB, tabell, kö och fil.</span><span class="sxs-lookup"><span data-stu-id="f302d-108">The types of storage services for this cmdlet are Blob, Table, Queue, and File.</span></span>

## <span data-ttu-id="f302d-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f302d-109">EXAMPLES</span></span>

### <span data-ttu-id="f302d-110">Exempel 1: ta bort CORS-regler för Blob-tjänsten</span><span class="sxs-lookup"><span data-stu-id="f302d-110">Example 1: Remove CORS rules for the blob service</span></span>
```
PS C:\>Remove-AzureStorageCORSRule -ServiceType Blob
```

<span data-ttu-id="f302d-111">Det här kommandot tar bort CORS-regler för typen blob-tjänst.</span><span class="sxs-lookup"><span data-stu-id="f302d-111">This command removes CORS rules for the Blob service type.</span></span>

## <span data-ttu-id="f302d-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f302d-112">PARAMETERS</span></span>

### <span data-ttu-id="f302d-113">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="f302d-113">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="f302d-114">Anger tids gräns för klient sidan, i sekunder, för en tjänst förfrågan.</span><span class="sxs-lookup"><span data-stu-id="f302d-114">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="f302d-115">Om det föregående samtalet inte fungerar under det angivna intervallet, försöker den här cmdleten igen.</span><span class="sxs-lookup"><span data-stu-id="f302d-115">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="f302d-116">Om denna cmdlet inte får ett lyckat svar innan intervallet går ut returneras ett fel.</span><span class="sxs-lookup"><span data-stu-id="f302d-116">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="f302d-117">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="f302d-117">-ConcurrentTaskCount</span></span>
<span data-ttu-id="f302d-118">Anger maximalt antal samtidiga nätverks samtal.</span><span class="sxs-lookup"><span data-stu-id="f302d-118">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="f302d-119">Du kan använda den här parametern för att begränsa samtidigheten för att reglera den lokala processorn och bandbredds användning genom att ange det maximala antalet simultana nätverks samtal.</span><span class="sxs-lookup"><span data-stu-id="f302d-119">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="f302d-120">Det angivna värdet är ett absolut antal och multipliceras inte med antalet kärnor.</span><span class="sxs-lookup"><span data-stu-id="f302d-120">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="f302d-121">Den här parametern kan hjälpa till att minska nätverks anslutnings problem i miljöer med liten bandbredd, till exempel 100 kilobit per sekund.</span><span class="sxs-lookup"><span data-stu-id="f302d-121">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="f302d-122">Standardvärdet är 10.</span><span class="sxs-lookup"><span data-stu-id="f302d-122">The default value is 10.</span></span>

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

### <span data-ttu-id="f302d-123">-Kontext</span><span class="sxs-lookup"><span data-stu-id="f302d-123">-Context</span></span>
<span data-ttu-id="f302d-124">Anger Azure Storage-kontexten.</span><span class="sxs-lookup"><span data-stu-id="f302d-124">Specifies the Azure storage context.</span></span>
<span data-ttu-id="f302d-125">New-AzureStorageContext cmdlet för att få en lagrings kontext.</span><span class="sxs-lookup"><span data-stu-id="f302d-125">To obtain the storage context, the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="f302d-126">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="f302d-126">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="f302d-127">Anger längden på tids gränsen för en server del av en begäran.</span><span class="sxs-lookup"><span data-stu-id="f302d-127">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="f302d-128">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="f302d-128">-ServiceType</span></span>
<span data-ttu-id="f302d-129">Anger typen för Azure Storage-tjänsten för vilken denna cmdlet tar bort regler.</span><span class="sxs-lookup"><span data-stu-id="f302d-129">Specifies the Azure Storage service type for which this cmdlet removes rules.</span></span>
<span data-ttu-id="f302d-130">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="f302d-130">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f302d-131">Object</span><span class="sxs-lookup"><span data-stu-id="f302d-131">Blob</span></span> 
- <span data-ttu-id="f302d-132">Tabell</span><span class="sxs-lookup"><span data-stu-id="f302d-132">Table</span></span> 
- <span data-ttu-id="f302d-133">Svarskö</span><span class="sxs-lookup"><span data-stu-id="f302d-133">Queue</span></span> 
- <span data-ttu-id="f302d-134">Fil</span><span class="sxs-lookup"><span data-stu-id="f302d-134">File</span></span>

```yaml
Type: StorageServiceType
Parameter Sets: (All)
Aliases: 
Accepted values: Blob, Table, Queue, File

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f302d-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f302d-135">CommonParameters</span></span>
<span data-ttu-id="f302d-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f302d-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f302d-137">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f302d-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f302d-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f302d-138">INPUTS</span></span>

## <span data-ttu-id="f302d-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f302d-139">OUTPUTS</span></span>

## <span data-ttu-id="f302d-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f302d-140">NOTES</span></span>

## <span data-ttu-id="f302d-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f302d-141">RELATED LINKS</span></span>

[<span data-ttu-id="f302d-142">Get-AzureStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="f302d-142">Get-AzureStorageCORSRule</span></span>](./Get-AzureStorageCORSRule.md)

[<span data-ttu-id="f302d-143">Set-AzureStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="f302d-143">Set-AzureStorageCORSRule</span></span>](./Set-AzureStorageCORSRule.md)


