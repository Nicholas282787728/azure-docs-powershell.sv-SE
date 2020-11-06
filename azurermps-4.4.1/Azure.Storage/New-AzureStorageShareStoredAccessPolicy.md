---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 37E76360-B683-407C-9AEF-7138374562D8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageShareStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageShareStoredAccessPolicy.md
gitcommit: https://github.com/Azure/azure-powershell/blob/1fa63f743120d7a7cd6cbb28ee43cd0f4c654af9
ms.openlocfilehash: 49d966c23569080ab72d0793014fe4fa5dd71b55
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573799"
---
# <span data-ttu-id="e9ef7-101">New-AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="e9ef7-101">New-AzureStorageShareStoredAccessPolicy</span></span>

## <span data-ttu-id="e9ef7-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e9ef7-102">SYNOPSIS</span></span>
<span data-ttu-id="e9ef7-103">Skapar en lagrad åtkomst princip på en lagrings plats.</span><span class="sxs-lookup"><span data-stu-id="e9ef7-103">Creates a stored access policy on a Storage share.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e9ef7-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e9ef7-104">SYNTAX</span></span>

```
New-AzureStorageShareStoredAccessPolicy [-ShareName] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

## <span data-ttu-id="e9ef7-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e9ef7-105">DESCRIPTION</span></span>
<span data-ttu-id="e9ef7-106">Cmdleten **New-AzureStorageShareStoredAccessPolicy** skapar en lagrad åtkomst princip på en Azure lagrings plats.</span><span class="sxs-lookup"><span data-stu-id="e9ef7-106">The **New-AzureStorageShareStoredAccessPolicy** cmdlet creates a stored access policy on an Azure Storage share.</span></span>

## <span data-ttu-id="e9ef7-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e9ef7-107">EXAMPLES</span></span>

### <span data-ttu-id="e9ef7-108">Exempel 1: skapa en lagrad åtkomst princip i en resurs</span><span class="sxs-lookup"><span data-stu-id="e9ef7-108">Example 1: Create a stored access policy in a share</span></span>
```
PS C:\>New-AzureStorageShareStoredAccessPolicy -ShareName "ContosoShare" -Policy "GeneralPolicy" -Permission "rwdl"
```

<span data-ttu-id="e9ef7-109">Det här kommandot skapar en lagrad åtkomst princip med fullständig behörighet i en resurs.</span><span class="sxs-lookup"><span data-stu-id="e9ef7-109">This command creates a stored access policy that has full permission in a share.</span></span>

## <span data-ttu-id="e9ef7-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e9ef7-110">PARAMETERS</span></span>

### <span data-ttu-id="e9ef7-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="e9ef7-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="e9ef7-112">Anger tids gräns för klient sidan, i sekunder, för en tjänst förfrågan.</span><span class="sxs-lookup"><span data-stu-id="e9ef7-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="e9ef7-113">Om det föregående samtalet inte fungerar under det angivna intervallet, försöker den här cmdleten igen.</span><span class="sxs-lookup"><span data-stu-id="e9ef7-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="e9ef7-114">Om denna cmdlet inte får ett lyckat svar innan intervallet går ut returneras ett fel.</span><span class="sxs-lookup"><span data-stu-id="e9ef7-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="e9ef7-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="e9ef7-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="e9ef7-116">Anger maximalt antal samtidiga nätverks samtal.</span><span class="sxs-lookup"><span data-stu-id="e9ef7-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="e9ef7-117">Du kan använda den här parametern för att begränsa samtidigheten för att reglera den lokala processorn och bandbredds användning genom att ange det maximala antalet simultana nätverks samtal.</span><span class="sxs-lookup"><span data-stu-id="e9ef7-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="e9ef7-118">Det angivna värdet är ett absolut antal och multipliceras inte med antalet kärnor.</span><span class="sxs-lookup"><span data-stu-id="e9ef7-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="e9ef7-119">Den här parametern kan hjälpa till att minska nätverks anslutnings problem i miljöer med liten bandbredd, till exempel 100 kilobit per sekund.</span><span class="sxs-lookup"><span data-stu-id="e9ef7-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="e9ef7-120">Standardvärdet är 10.</span><span class="sxs-lookup"><span data-stu-id="e9ef7-120">The default value is 10.</span></span>

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

### <span data-ttu-id="e9ef7-121">-Kontext</span><span class="sxs-lookup"><span data-stu-id="e9ef7-121">-Context</span></span>
<span data-ttu-id="e9ef7-122">Anger en Azure Storage-kontext.</span><span class="sxs-lookup"><span data-stu-id="e9ef7-122">Specifies an Azure storage context.</span></span>
<span data-ttu-id="e9ef7-123">Använd cmdleten [New-AzureStorageContext](./New-AzureStorageContext.md) för att få en lagrings kontext.</span><span class="sxs-lookup"><span data-stu-id="e9ef7-123">To obtain a storage context, use the [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="e9ef7-124">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="e9ef7-124">-ExpiryTime</span></span>
<span data-ttu-id="e9ef7-125">Anger den tid då den lagrade åtkomst policyn blir ogiltig.</span><span class="sxs-lookup"><span data-stu-id="e9ef7-125">Specifies the time at which the stored access policy becomes invalid.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9ef7-126">-Tillstånd</span><span class="sxs-lookup"><span data-stu-id="e9ef7-126">-Permission</span></span>
<span data-ttu-id="e9ef7-127">Anger behörigheter i den lagrade åtkomst principen för att komma åt lagrings resursen eller filerna under den.</span><span class="sxs-lookup"><span data-stu-id="e9ef7-127">Specifies permissions in the stored access policy to access the Storage share or files under it.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9ef7-128">-Princip</span><span class="sxs-lookup"><span data-stu-id="e9ef7-128">-Policy</span></span>
<span data-ttu-id="e9ef7-129">Anger ett namn för den lagrade åtkomst principen.</span><span class="sxs-lookup"><span data-stu-id="e9ef7-129">Specifies a name for the stored access policy.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9ef7-130">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="e9ef7-130">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="e9ef7-131">Anger längden på tids gränsen för en server del av en begäran.</span><span class="sxs-lookup"><span data-stu-id="e9ef7-131">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="e9ef7-132">-ShareName</span><span class="sxs-lookup"><span data-stu-id="e9ef7-132">-ShareName</span></span>
<span data-ttu-id="e9ef7-133">Anger namnet på lagrings resursen.</span><span class="sxs-lookup"><span data-stu-id="e9ef7-133">Specifies the name of the Storage share.</span></span>

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

### <span data-ttu-id="e9ef7-134">-StartTime</span><span class="sxs-lookup"><span data-stu-id="e9ef7-134">-StartTime</span></span>
<span data-ttu-id="e9ef7-135">Anger den tid då den lagrade åtkomst policyn blir giltig.</span><span class="sxs-lookup"><span data-stu-id="e9ef7-135">Specifies the time at which the stored access policy becomes valid.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9ef7-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9ef7-136">CommonParameters</span></span>
<span data-ttu-id="e9ef7-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e9ef7-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9ef7-138">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e9ef7-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9ef7-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e9ef7-139">INPUTS</span></span>

### <span data-ttu-id="e9ef7-140">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="e9ef7-140">IStorageContext</span></span>

<span data-ttu-id="e9ef7-141">Parametern ' context ' godkänner värdet av typen ' IStorageContext ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="e9ef7-141">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="e9ef7-142">Strängvärdet</span><span class="sxs-lookup"><span data-stu-id="e9ef7-142">String</span></span>

<span data-ttu-id="e9ef7-143">Parametern ' ShareName ' godkänner värdet för typen ' String ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="e9ef7-143">Parameter 'ShareName' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="e9ef7-144">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e9ef7-144">OUTPUTS</span></span>

### <span data-ttu-id="e9ef7-145">System. String</span><span class="sxs-lookup"><span data-stu-id="e9ef7-145">System.String</span></span>

## <span data-ttu-id="e9ef7-146">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e9ef7-146">NOTES</span></span>

## <span data-ttu-id="e9ef7-147">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e9ef7-147">RELATED LINKS</span></span>

[<span data-ttu-id="e9ef7-148">Get-AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="e9ef7-148">Get-AzureStorageShareStoredAccessPolicy</span></span>](./Get-AzureStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="e9ef7-149">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="e9ef7-149">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="e9ef7-150">Remove-AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="e9ef7-150">Remove-AzureStorageShareStoredAccessPolicy</span></span>](./Remove-AzureStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="e9ef7-151">Set-AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="e9ef7-151">Set-AzureStorageShareStoredAccessPolicy</span></span>](./Set-AzureStorageShareStoredAccessPolicy.md)
