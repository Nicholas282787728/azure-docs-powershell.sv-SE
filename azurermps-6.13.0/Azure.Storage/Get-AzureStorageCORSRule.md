---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: 5FA8A3F3-F52C-40BC-94C2-4CDA00C6F32F
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/get-azurestoragecorsrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageCORSRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageCORSRule.md
ms.openlocfilehash: 6b5d7fa889810563964aa66a34b567f482781ac6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576372"
---
# <span data-ttu-id="6b22a-101">Get-AzureStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="6b22a-101">Get-AzureStorageCORSRule</span></span>

## <span data-ttu-id="6b22a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6b22a-102">SYNOPSIS</span></span>
<span data-ttu-id="6b22a-103">Hämtar CORS-regler för en lagrings tjänst typ.</span><span class="sxs-lookup"><span data-stu-id="6b22a-103">Gets CORS rules for a Storage service type.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6b22a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6b22a-104">SYNTAX</span></span>

```
Get-AzureStorageCORSRule [-ServiceType] <StorageServiceType> [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="6b22a-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6b22a-105">DESCRIPTION</span></span>
<span data-ttu-id="6b22a-106">Cmdleten **Get-AzureStorageCORSRule** får CORS-regler (Cross-Resource Sharing) för en Azure Storage Service-typ.</span><span class="sxs-lookup"><span data-stu-id="6b22a-106">The **Get-AzureStorageCORSRule** cmdlet gets Cross-Origin Resource Sharing (CORS) rules for an Azure Storage service type.</span></span>

## <span data-ttu-id="6b22a-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6b22a-107">EXAMPLES</span></span>

### <span data-ttu-id="6b22a-108">Exempel 1: Hämta CORS-regler för Blob-tjänsten</span><span class="sxs-lookup"><span data-stu-id="6b22a-108">Example 1: Get CORS rules of blob service</span></span>
```
PS C:\>Get-AzureStorageCORSRule -ServiceType Blob
```

<span data-ttu-id="6b22a-109">Det här kommandot får CORS-reglerna för typen blob-tjänst.</span><span class="sxs-lookup"><span data-stu-id="6b22a-109">This command gets the CORS rules for the Blob service type.</span></span>

## <span data-ttu-id="6b22a-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6b22a-110">PARAMETERS</span></span>

### <span data-ttu-id="6b22a-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="6b22a-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="6b22a-112">Anger tids gräns för klient sidan, i sekunder, för en tjänst förfrågan.</span><span class="sxs-lookup"><span data-stu-id="6b22a-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="6b22a-113">Om det föregående samtalet inte fungerar under det angivna intervallet, försöker den här cmdleten igen.</span><span class="sxs-lookup"><span data-stu-id="6b22a-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="6b22a-114">Om denna cmdlet inte får ett lyckat svar innan intervallet går ut returneras ett fel.</span><span class="sxs-lookup"><span data-stu-id="6b22a-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b22a-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="6b22a-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="6b22a-116">Anger maximalt antal samtidiga nätverks samtal.</span><span class="sxs-lookup"><span data-stu-id="6b22a-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="6b22a-117">Du kan använda den här parametern för att begränsa samtidigheten för att reglera den lokala processorn och bandbredds användning genom att ange det maximala antalet simultana nätverks samtal.</span><span class="sxs-lookup"><span data-stu-id="6b22a-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="6b22a-118">Det angivna värdet är ett absolut antal och multipliceras inte med antalet kärnor.</span><span class="sxs-lookup"><span data-stu-id="6b22a-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="6b22a-119">Den här parametern kan hjälpa till att minska nätverks anslutnings problem i miljöer med liten bandbredd, till exempel 100 kilobit per sekund.</span><span class="sxs-lookup"><span data-stu-id="6b22a-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="6b22a-120">Standardvärdet är 10.</span><span class="sxs-lookup"><span data-stu-id="6b22a-120">The default value is 10.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b22a-121">-Kontext</span><span class="sxs-lookup"><span data-stu-id="6b22a-121">-Context</span></span>
<span data-ttu-id="6b22a-122">Anger en Azure Storage-kontext.</span><span class="sxs-lookup"><span data-stu-id="6b22a-122">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="6b22a-123">Använd New-AzureStorageContext cmdlet för att få en kontext.</span><span class="sxs-lookup"><span data-stu-id="6b22a-123">To obtain a context, use the New-AzureStorageContext cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6b22a-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b22a-124">-DefaultProfile</span></span>
<span data-ttu-id="6b22a-125">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="6b22a-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6b22a-126">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="6b22a-126">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="6b22a-127">Anger längden på tids gränsen för en server del av en begäran.</span><span class="sxs-lookup"><span data-stu-id="6b22a-127">Specifies the length of the time-out period for the server part of a request.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b22a-128">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="6b22a-128">-ServiceType</span></span>
<span data-ttu-id="6b22a-129">Anger typen för Azure Storage-tjänsten för vilken denna cmdlet får CORS-regler.</span><span class="sxs-lookup"><span data-stu-id="6b22a-129">Specifies the Azure Storage service type for which this cmdlet gets CORS rules.</span></span>
<span data-ttu-id="6b22a-130">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="6b22a-130">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="6b22a-131">Object</span><span class="sxs-lookup"><span data-stu-id="6b22a-131">Blob</span></span> 
- <span data-ttu-id="6b22a-132">Tabell</span><span class="sxs-lookup"><span data-stu-id="6b22a-132">Table</span></span> 
- <span data-ttu-id="6b22a-133">Svarskö</span><span class="sxs-lookup"><span data-stu-id="6b22a-133">Queue</span></span> 
- <span data-ttu-id="6b22a-134">Fil</span><span class="sxs-lookup"><span data-stu-id="6b22a-134">File</span></span>

```yaml
Type: Microsoft.WindowsAzure.Commands.Storage.Common.StorageServiceType
Parameter Sets: (All)
Aliases:
Accepted values: Blob, Table, Queue, File

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b22a-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b22a-135">CommonParameters</span></span>
<span data-ttu-id="6b22a-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6b22a-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b22a-137">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6b22a-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b22a-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6b22a-138">INPUTS</span></span>

### <span data-ttu-id="6b22a-139">Microsoft. Azure. commands. Common. verifikation. abstraktioner. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="6b22a-139">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="6b22a-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6b22a-140">OUTPUTS</span></span>

### <span data-ttu-id="6b22a-141">Microsoft. WindowsAzure. commands. Storage. Model. ResourceModel. PSCorsRule</span><span class="sxs-lookup"><span data-stu-id="6b22a-141">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSCorsRule</span></span>

## <span data-ttu-id="6b22a-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6b22a-142">NOTES</span></span>

## <span data-ttu-id="6b22a-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6b22a-143">RELATED LINKS</span></span>

[<span data-ttu-id="6b22a-144">Remove-AzureStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="6b22a-144">Remove-AzureStorageCORSRule</span></span>](./Remove-AzureStorageCORSRule.md)

[<span data-ttu-id="6b22a-145">Set-AzureStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="6b22a-145">Set-AzureStorageCORSRule</span></span>](./Set-AzureStorageCORSRule.md)


