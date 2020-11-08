---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 10D5B7E0-242B-4DC0-A527-8F6388E72E0A
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstoragecontainerstoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Get-AzStorageContainerStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Get-AzStorageContainerStoredAccessPolicy.md
ms.openlocfilehash: c4190508a50a8267108b428f4bf993be226cec2b
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93923670"
---
# <span data-ttu-id="ef994-101">Get-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="ef994-101">Get-AzStorageContainerStoredAccessPolicy</span></span>

## <span data-ttu-id="ef994-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ef994-102">SYNOPSIS</span></span>
<span data-ttu-id="ef994-103">Hämtar den lagrade åtkomst principen eller principer för en Azure Storage-behållare.</span><span class="sxs-lookup"><span data-stu-id="ef994-103">Gets the stored access policy or policies for an Azure storage container.</span></span>

## <span data-ttu-id="ef994-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ef994-104">SYNTAX</span></span>

```
Get-AzStorageContainerStoredAccessPolicy [-Container] <String> [[-Policy] <String>]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="ef994-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ef994-105">DESCRIPTION</span></span>
<span data-ttu-id="ef994-106">Cmdleten **Get-AzStorageContainerStoredAccessPolicy** innehåller en lista över lagrade åtkomst principer för en Azure Storage-behållare.</span><span class="sxs-lookup"><span data-stu-id="ef994-106">The **Get-AzStorageContainerStoredAccessPolicy** cmdlet lists the stored access policy or policies for an Azure storage container.</span></span>

## <span data-ttu-id="ef994-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ef994-107">EXAMPLES</span></span>

### <span data-ttu-id="ef994-108">Exempel 1: Hämta en lagrad åtkomst princip i en lagrings behållare</span><span class="sxs-lookup"><span data-stu-id="ef994-108">Example 1: Get a stored access policy in a storage container</span></span>
```
PS C:\>Get-AzStorageContainerStoredAccessPolicy -Container "Container07" -Policy "Policy22"
```

<span data-ttu-id="ef994-109">Det här kommandot får åtkomst principen med namnet Policy22 i lagrings behållaren med namnet Container07.</span><span class="sxs-lookup"><span data-stu-id="ef994-109">This command gets the access policy named Policy22 in the storage container named Container07.</span></span>

### <span data-ttu-id="ef994-110">Exempel 2: Hämta alla lagrade åtkomst principer i en lagrings behållare</span><span class="sxs-lookup"><span data-stu-id="ef994-110">Example 2: Get all the stored access policies in a storage container</span></span>
```
PS C:\>Get-AzStorageContainerStoredAccessPolicy -Container "Container07"
```

<span data-ttu-id="ef994-111">Det här kommandot får alla åtkomst principer i lagrings behållaren som heter Container07.</span><span class="sxs-lookup"><span data-stu-id="ef994-111">This command gets all access policies in the storage container named Container07.</span></span>

## <span data-ttu-id="ef994-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ef994-112">PARAMETERS</span></span>

### <span data-ttu-id="ef994-113">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="ef994-113">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="ef994-114">Anger tids gräns för klient sidan, i sekunder, för en tjänst förfrågan.</span><span class="sxs-lookup"><span data-stu-id="ef994-114">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="ef994-115">Om det föregående samtalet inte fungerar under det angivna intervallet, försöker den här cmdleten igen.</span><span class="sxs-lookup"><span data-stu-id="ef994-115">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="ef994-116">Om denna cmdlet inte får ett lyckat svar innan intervallet går ut returneras ett fel.</span><span class="sxs-lookup"><span data-stu-id="ef994-116">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="ef994-117">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="ef994-117">-ConcurrentTaskCount</span></span>
<span data-ttu-id="ef994-118">Anger maximalt antal samtidiga nätverks samtal.</span><span class="sxs-lookup"><span data-stu-id="ef994-118">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="ef994-119">Du kan använda den här parametern för att begränsa samtidigheten för att reglera den lokala processorn och bandbredds användning genom att ange det maximala antalet simultana nätverks samtal.</span><span class="sxs-lookup"><span data-stu-id="ef994-119">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="ef994-120">Det angivna värdet är ett absolut antal och multipliceras inte med antalet kärnor.</span><span class="sxs-lookup"><span data-stu-id="ef994-120">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="ef994-121">Den här parametern kan hjälpa till att minska nätverks anslutnings problem i miljöer med liten bandbredd, till exempel 100 kilobit per sekund.</span><span class="sxs-lookup"><span data-stu-id="ef994-121">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="ef994-122">Standardvärdet är 10.</span><span class="sxs-lookup"><span data-stu-id="ef994-122">The default value is 10.</span></span>

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

### <span data-ttu-id="ef994-123">-Container</span><span class="sxs-lookup"><span data-stu-id="ef994-123">-Container</span></span>
<span data-ttu-id="ef994-124">Anger namnet på din Azure Storage-behållare.</span><span class="sxs-lookup"><span data-stu-id="ef994-124">Specifies the name of your Azure storage container.</span></span>

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

### <span data-ttu-id="ef994-125">-Kontext</span><span class="sxs-lookup"><span data-stu-id="ef994-125">-Context</span></span>
<span data-ttu-id="ef994-126">Anger Azure Storage-kontexten.</span><span class="sxs-lookup"><span data-stu-id="ef994-126">Specifies the Azure storage context.</span></span>

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

### <span data-ttu-id="ef994-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef994-127">-DefaultProfile</span></span>
<span data-ttu-id="ef994-128">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ef994-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ef994-129">-Princip</span><span class="sxs-lookup"><span data-stu-id="ef994-129">-Policy</span></span>
<span data-ttu-id="ef994-130">Anger den Azure-lagrade åtkomst policyn.</span><span class="sxs-lookup"><span data-stu-id="ef994-130">Specifies the Azure stored access policy.</span></span>

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

### <span data-ttu-id="ef994-131">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="ef994-131">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="ef994-132">Anger timeout-intervall för tjänsten i sekunder för en begäran.</span><span class="sxs-lookup"><span data-stu-id="ef994-132">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="ef994-133">Om det angivna intervallet förflyter innan tjänsten bearbetar begäran returnerar lagrings tjänsten ett fel.</span><span class="sxs-lookup"><span data-stu-id="ef994-133">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="ef994-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef994-134">CommonParameters</span></span>
<span data-ttu-id="ef994-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ef994-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef994-136">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ef994-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef994-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ef994-137">INPUTS</span></span>

### <span data-ttu-id="ef994-138">System. String</span><span class="sxs-lookup"><span data-stu-id="ef994-138">System.String</span></span>

### <span data-ttu-id="ef994-139">Microsoft. Azure. commands. Common. verifikation. abstraktioner. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="ef994-139">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="ef994-140">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ef994-140">OUTPUTS</span></span>

### <span data-ttu-id="ef994-141">Microsoft. WindowsAz. Storage. blob. SharedAccessBlobPolicy</span><span class="sxs-lookup"><span data-stu-id="ef994-141">Microsoft.WindowsAz.Storage.Blob.SharedAccessBlobPolicy</span></span>

## <span data-ttu-id="ef994-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ef994-142">NOTES</span></span>

## <span data-ttu-id="ef994-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ef994-143">RELATED LINKS</span></span>

[<span data-ttu-id="ef994-144">New-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="ef994-144">New-AzStorageContainerStoredAccessPolicy</span></span>](./New-AzStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="ef994-145">Remove-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="ef994-145">Remove-AzStorageContainerStoredAccessPolicy</span></span>](./Remove-AzStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="ef994-146">Set-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="ef994-146">Set-AzStorageContainerStoredAccessPolicy</span></span>](./Set-AzStorageContainerStoredAccessPolicy.md)

