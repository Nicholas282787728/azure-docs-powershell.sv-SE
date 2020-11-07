---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: 10D5B7E0-242B-4DC0-A527-8F6388E72E0A
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/get-azurestoragecontainerstoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageContainerStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageContainerStoredAccessPolicy.md
ms.openlocfilehash: c9032b70b6a7b1884ce5ff4128e7953bf7d68cf2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756426"
---
# <span data-ttu-id="6e572-101">Get-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="6e572-101">Get-AzureStorageContainerStoredAccessPolicy</span></span>

## <span data-ttu-id="6e572-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6e572-102">SYNOPSIS</span></span>
<span data-ttu-id="6e572-103">Hämtar den lagrade åtkomst principen eller principer för en Azure Storage-behållare.</span><span class="sxs-lookup"><span data-stu-id="6e572-103">Gets the stored access policy or policies for an Azure storage container.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6e572-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6e572-104">SYNTAX</span></span>

```
Get-AzureStorageContainerStoredAccessPolicy [-Container] <String> [[-Policy] <String>]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="6e572-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6e572-105">DESCRIPTION</span></span>
<span data-ttu-id="6e572-106">Cmdleten **Get-AzureStorageContainerStoredAccessPolicy** innehåller en lista över lagrade åtkomst principer för en Azure Storage-behållare.</span><span class="sxs-lookup"><span data-stu-id="6e572-106">The **Get-AzureStorageContainerStoredAccessPolicy** cmdlet lists the stored access policy or policies for an Azure storage container.</span></span>

## <span data-ttu-id="6e572-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6e572-107">EXAMPLES</span></span>

### <span data-ttu-id="6e572-108">Exempel 1: Hämta en lagrad åtkomst princip i en lagrings behållare</span><span class="sxs-lookup"><span data-stu-id="6e572-108">Example 1: Get a stored access policy in a storage container</span></span>
```
PS C:\>Get-AzureStorageContainerStoredAccessPolicy -Container "Container07" -Policy "Policy22"
```

<span data-ttu-id="6e572-109">Det här kommandot får åtkomst principen med namnet Policy22 i lagrings behållaren med namnet Container07.</span><span class="sxs-lookup"><span data-stu-id="6e572-109">This command gets the access policy named Policy22 in the storage container named Container07.</span></span>

### <span data-ttu-id="6e572-110">Exempel 2: Hämta alla lagrade åtkomst principer i en lagrings behållare</span><span class="sxs-lookup"><span data-stu-id="6e572-110">Example 2: Get all the stored access policies in a storage container</span></span>
```
PS C:\>Get-AzureStorageContainerStoredAccessPolicy -Container "Container07"
```

<span data-ttu-id="6e572-111">Det här kommandot får alla åtkomst principer i lagrings behållaren som heter Container07.</span><span class="sxs-lookup"><span data-stu-id="6e572-111">This command gets all access policies in the storage container named Container07.</span></span>

## <span data-ttu-id="6e572-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6e572-112">PARAMETERS</span></span>

### <span data-ttu-id="6e572-113">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="6e572-113">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="6e572-114">Anger tids gräns för klient sidan, i sekunder, för en tjänst förfrågan.</span><span class="sxs-lookup"><span data-stu-id="6e572-114">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="6e572-115">Om det föregående samtalet inte fungerar under det angivna intervallet, försöker den här cmdleten igen.</span><span class="sxs-lookup"><span data-stu-id="6e572-115">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="6e572-116">Om denna cmdlet inte får ett lyckat svar innan intervallet går ut returneras ett fel.</span><span class="sxs-lookup"><span data-stu-id="6e572-116">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="6e572-117">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="6e572-117">-ConcurrentTaskCount</span></span>
<span data-ttu-id="6e572-118">Anger maximalt antal samtidiga nätverks samtal.</span><span class="sxs-lookup"><span data-stu-id="6e572-118">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="6e572-119">Du kan använda den här parametern för att begränsa samtidigheten för att reglera den lokala processorn och bandbredds användning genom att ange det maximala antalet simultana nätverks samtal.</span><span class="sxs-lookup"><span data-stu-id="6e572-119">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="6e572-120">Det angivna värdet är ett absolut antal och multipliceras inte med antalet kärnor.</span><span class="sxs-lookup"><span data-stu-id="6e572-120">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="6e572-121">Den här parametern kan hjälpa till att minska nätverks anslutnings problem i miljöer med liten bandbredd, till exempel 100 kilobit per sekund.</span><span class="sxs-lookup"><span data-stu-id="6e572-121">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="6e572-122">Standardvärdet är 10.</span><span class="sxs-lookup"><span data-stu-id="6e572-122">The default value is 10.</span></span>

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

### <span data-ttu-id="6e572-123">-Container</span><span class="sxs-lookup"><span data-stu-id="6e572-123">-Container</span></span>
<span data-ttu-id="6e572-124">Anger namnet på din Azure Storage-behållare.</span><span class="sxs-lookup"><span data-stu-id="6e572-124">Specifies the name of your Azure storage container.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6e572-125">-Kontext</span><span class="sxs-lookup"><span data-stu-id="6e572-125">-Context</span></span>
<span data-ttu-id="6e572-126">Anger Azure Storage-kontexten.</span><span class="sxs-lookup"><span data-stu-id="6e572-126">Specifies the Azure storage context.</span></span>

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

### <span data-ttu-id="6e572-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e572-127">-DefaultProfile</span></span>
<span data-ttu-id="6e572-128">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="6e572-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6e572-129">-Princip</span><span class="sxs-lookup"><span data-stu-id="6e572-129">-Policy</span></span>
<span data-ttu-id="6e572-130">Anger den Azure-lagrade åtkomst policyn.</span><span class="sxs-lookup"><span data-stu-id="6e572-130">Specifies the Azure stored access policy.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e572-131">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="6e572-131">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="6e572-132">Anger timeout-intervall för tjänsten i sekunder för en begäran.</span><span class="sxs-lookup"><span data-stu-id="6e572-132">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="6e572-133">Om det angivna intervallet förflyter innan tjänsten bearbetar begäran returnerar lagrings tjänsten ett fel.</span><span class="sxs-lookup"><span data-stu-id="6e572-133">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="6e572-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e572-134">CommonParameters</span></span>
<span data-ttu-id="6e572-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6e572-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e572-136">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6e572-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e572-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6e572-137">INPUTS</span></span>

### <span data-ttu-id="6e572-138">System. String</span><span class="sxs-lookup"><span data-stu-id="6e572-138">System.String</span></span>

### <span data-ttu-id="6e572-139">Microsoft. Azure. commands. Common. verifikation. abstraktioner. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="6e572-139">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="6e572-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6e572-140">OUTPUTS</span></span>

### <span data-ttu-id="6e572-141">Microsoft. WindowsAzure. Storage. blob. SharedAccessBlobPolicy</span><span class="sxs-lookup"><span data-stu-id="6e572-141">Microsoft.WindowsAzure.Storage.Blob.SharedAccessBlobPolicy</span></span>

## <span data-ttu-id="6e572-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6e572-142">NOTES</span></span>

## <span data-ttu-id="6e572-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6e572-143">RELATED LINKS</span></span>

[<span data-ttu-id="6e572-144">New-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="6e572-144">New-AzureStorageContainerStoredAccessPolicy</span></span>](./New-AzureStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="6e572-145">Remove-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="6e572-145">Remove-AzureStorageContainerStoredAccessPolicy</span></span>](./Remove-AzureStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="6e572-146">Set-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="6e572-146">Set-AzureStorageContainerStoredAccessPolicy</span></span>](./Set-AzureStorageContainerStoredAccessPolicy.md)


