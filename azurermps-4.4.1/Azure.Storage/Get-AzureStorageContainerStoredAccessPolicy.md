---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 10D5B7E0-242B-4DC0-A527-8F6388E72E0A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageContainerStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageContainerStoredAccessPolicy.md
gitcommit: https://github.com/Azure/azure-powershell/blob/1fa63f743120d7a7cd6cbb28ee43cd0f4c654af9
ms.openlocfilehash: 174353aacbfe939294f654a4f5f61548bfc672dc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93586307"
---
# <span data-ttu-id="d8344-101">Get-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="d8344-101">Get-AzureStorageContainerStoredAccessPolicy</span></span>

## <span data-ttu-id="d8344-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d8344-102">SYNOPSIS</span></span>
<span data-ttu-id="d8344-103">Hämtar den lagrade åtkomst principen eller principer för en Azure Storage-behållare.</span><span class="sxs-lookup"><span data-stu-id="d8344-103">Gets the stored access policy or policies for an Azure storage container.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d8344-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d8344-104">SYNTAX</span></span>

```
Get-AzureStorageContainerStoredAccessPolicy [-Container] <String> [[-Policy] <String>]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="d8344-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d8344-105">DESCRIPTION</span></span>
<span data-ttu-id="d8344-106">Cmdleten **Get-AzureStorageContainerStoredAccessPolicy** innehåller en lista över lagrade åtkomst principer för en Azure Storage-behållare.</span><span class="sxs-lookup"><span data-stu-id="d8344-106">The **Get-AzureStorageContainerStoredAccessPolicy** cmdlet lists the stored access policy or policies for an Azure storage container.</span></span>

## <span data-ttu-id="d8344-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d8344-107">EXAMPLES</span></span>

### <span data-ttu-id="d8344-108">Exempel 1: Hämta en lagrad åtkomst princip i en lagrings behållare</span><span class="sxs-lookup"><span data-stu-id="d8344-108">Example 1: Get a stored access policy in a storage container</span></span>
```
PS C:\>Get-AzureStorageContainerStoredAccessPolicy -Container "Container07" -Policy "Policy22"
```

<span data-ttu-id="d8344-109">Det här kommandot får åtkomst principen med namnet Policy22 i lagrings behållaren med namnet Container07.</span><span class="sxs-lookup"><span data-stu-id="d8344-109">This command gets the access policy named Policy22 in the storage container named Container07.</span></span>

### <span data-ttu-id="d8344-110">Exempel 2: Hämta alla lagrade åtkomst principer i en lagrings behållare</span><span class="sxs-lookup"><span data-stu-id="d8344-110">Example 2: Get all the stored access policies in a storage container</span></span>
```
PS C:\>Get-AzureStorageContainerStoredAccessPolicy -Container "Container07"
```

<span data-ttu-id="d8344-111">Det här kommandot får alla åtkomst principer i lagrings behållaren som heter Container07.</span><span class="sxs-lookup"><span data-stu-id="d8344-111">This command gets all access policies in the storage container named Container07.</span></span>

## <span data-ttu-id="d8344-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d8344-112">PARAMETERS</span></span>

### <span data-ttu-id="d8344-113">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="d8344-113">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="d8344-114">Anger tids gräns för klient sidan, i sekunder, för en tjänst förfrågan.</span><span class="sxs-lookup"><span data-stu-id="d8344-114">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="d8344-115">Om det föregående samtalet inte fungerar under det angivna intervallet, försöker den här cmdleten igen.</span><span class="sxs-lookup"><span data-stu-id="d8344-115">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="d8344-116">Om denna cmdlet inte får ett lyckat svar innan intervallet går ut returneras ett fel.</span><span class="sxs-lookup"><span data-stu-id="d8344-116">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="d8344-117">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="d8344-117">-ConcurrentTaskCount</span></span>
<span data-ttu-id="d8344-118">Anger maximalt antal samtidiga nätverks samtal.</span><span class="sxs-lookup"><span data-stu-id="d8344-118">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="d8344-119">Du kan använda den här parametern för att begränsa samtidigheten för att reglera den lokala processorn och bandbredds användning genom att ange det maximala antalet simultana nätverks samtal.</span><span class="sxs-lookup"><span data-stu-id="d8344-119">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="d8344-120">Det angivna värdet är ett absolut antal och multipliceras inte med antalet kärnor.</span><span class="sxs-lookup"><span data-stu-id="d8344-120">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="d8344-121">Den här parametern kan hjälpa till att minska nätverks anslutnings problem i miljöer med liten bandbredd, till exempel 100 kilobit per sekund.</span><span class="sxs-lookup"><span data-stu-id="d8344-121">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="d8344-122">Standardvärdet är 10.</span><span class="sxs-lookup"><span data-stu-id="d8344-122">The default value is 10.</span></span>

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

### <span data-ttu-id="d8344-123">-Container</span><span class="sxs-lookup"><span data-stu-id="d8344-123">-Container</span></span>
<span data-ttu-id="d8344-124">Anger namnet på din Azure Storage-behållare.</span><span class="sxs-lookup"><span data-stu-id="d8344-124">Specifies the name of your Azure storage container.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d8344-125">-Kontext</span><span class="sxs-lookup"><span data-stu-id="d8344-125">-Context</span></span>
<span data-ttu-id="d8344-126">Anger Azure Storage-kontexten.</span><span class="sxs-lookup"><span data-stu-id="d8344-126">Specifies the Azure storage context.</span></span>

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

### <span data-ttu-id="d8344-127">-Princip</span><span class="sxs-lookup"><span data-stu-id="d8344-127">-Policy</span></span>
<span data-ttu-id="d8344-128">Anger den Azure-lagrade åtkomst policyn.</span><span class="sxs-lookup"><span data-stu-id="d8344-128">Specifies the Azure stored access policy.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8344-129">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="d8344-129">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="d8344-130">Anger timeout-intervall för tjänsten i sekunder för en begäran.</span><span class="sxs-lookup"><span data-stu-id="d8344-130">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="d8344-131">Om det angivna intervallet förflyter innan tjänsten bearbetar begäran returnerar lagrings tjänsten ett fel.</span><span class="sxs-lookup"><span data-stu-id="d8344-131">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="d8344-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8344-132">CommonParameters</span></span>
<span data-ttu-id="d8344-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d8344-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8344-134">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d8344-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8344-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d8344-135">INPUTS</span></span>

### <span data-ttu-id="d8344-136">Strängvärdet</span><span class="sxs-lookup"><span data-stu-id="d8344-136">String</span></span>

<span data-ttu-id="d8344-137">Parametern "container" accepterar värdet för typen String från pipeline</span><span class="sxs-lookup"><span data-stu-id="d8344-137">Parameter 'Container' accepts value of type 'String' from the pipeline</span></span>

### <span data-ttu-id="d8344-138">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="d8344-138">IStorageContext</span></span>

<span data-ttu-id="d8344-139">Parametern ' context ' godkänner värdet av typen ' IStorageContext ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="d8344-139">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

## <span data-ttu-id="d8344-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d8344-140">OUTPUTS</span></span>

### <span data-ttu-id="d8344-141">Microsoft. WindowsAzure. Storage. blob. SharedAccessBlobPolicy</span><span class="sxs-lookup"><span data-stu-id="d8344-141">Microsoft.WindowsAzure.Storage.Blob.SharedAccessBlobPolicy</span></span>

## <span data-ttu-id="d8344-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d8344-142">NOTES</span></span>

## <span data-ttu-id="d8344-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d8344-143">RELATED LINKS</span></span>

[<span data-ttu-id="d8344-144">New-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="d8344-144">New-AzureStorageContainerStoredAccessPolicy</span></span>](./New-AzureStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="d8344-145">Remove-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="d8344-145">Remove-AzureStorageContainerStoredAccessPolicy</span></span>](./Remove-AzureStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="d8344-146">Set-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="d8344-146">Set-AzureStorageContainerStoredAccessPolicy</span></span>](./Set-AzureStorageContainerStoredAccessPolicy.md)

