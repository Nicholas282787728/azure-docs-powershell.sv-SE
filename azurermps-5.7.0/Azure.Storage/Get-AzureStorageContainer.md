---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 90C3DF13-0010-49B6-A8CD-C6AC34BC3EFA
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/get-azurestoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageContainer.md
ms.openlocfilehash: 45368a3abe428c65604d4ba103cf793972e50ea1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93577367"
---
# <span data-ttu-id="37bd3-101">Get-AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="37bd3-101">Get-AzureStorageContainer</span></span>

## <span data-ttu-id="37bd3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="37bd3-102">SYNOPSIS</span></span>
<span data-ttu-id="37bd3-103">Visar lagrings behållarna.</span><span class="sxs-lookup"><span data-stu-id="37bd3-103">Lists the storage containers.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="37bd3-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="37bd3-104">SYNTAX</span></span>

### <span data-ttu-id="37bd3-105">ContainerName (standard)</span><span class="sxs-lookup"><span data-stu-id="37bd3-105">ContainerName (Default)</span></span>
```
Get-AzureStorageContainer [[-Name] <String>] [-MaxCount <Int32>] [-ContinuationToken <BlobContinuationToken>]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="37bd3-106">ContainerPrefix</span><span class="sxs-lookup"><span data-stu-id="37bd3-106">ContainerPrefix</span></span>
```
Get-AzureStorageContainer -Prefix <String> [-MaxCount <Int32>] [-ContinuationToken <BlobContinuationToken>]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="37bd3-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="37bd3-107">DESCRIPTION</span></span>
<span data-ttu-id="37bd3-108">Cmdleten **Get-AzureStorageContainer** innehåller lagrings containrarna som är kopplade till lagrings kontot i Azure.</span><span class="sxs-lookup"><span data-stu-id="37bd3-108">The **Get-AzureStorageContainer** cmdlet lists the storage containers associated with the storage account in Azure.</span></span>

## <span data-ttu-id="37bd3-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="37bd3-109">EXAMPLES</span></span>

### <span data-ttu-id="37bd3-110">Exempel 1: skaffa Azure Storage BLOB efter namn</span><span class="sxs-lookup"><span data-stu-id="37bd3-110">Example 1: Get Azure Storage blob by name</span></span>
```
PS C:\>Get-AzureStorageContainer -Name container*
```

<span data-ttu-id="37bd3-111">I det här exemplet används ett jokertecken för att returnera en lista över alla behållare med ett namn som börjar med en container.</span><span class="sxs-lookup"><span data-stu-id="37bd3-111">This example uses a wildcard character to return a list of all containers with a name that starts with container.</span></span>

### <span data-ttu-id="37bd3-112">Exempel 2: Hämta en Azure Storage-behållare efter container namn</span><span class="sxs-lookup"><span data-stu-id="37bd3-112">Example 2: Get Azure Storage container by container name prefix</span></span>
```
PS C:\>Get-AzureStorageContainer -Prefix "container"
```

<span data-ttu-id="37bd3-113">I det här exemplet används parametern *prefix* för att returnera en lista över alla behållare med ett namn som börjar med en container.</span><span class="sxs-lookup"><span data-stu-id="37bd3-113">This example uses the *Prefix* parameter to return a list of all containers with a name that starts with container.</span></span>

## <span data-ttu-id="37bd3-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="37bd3-114">PARAMETERS</span></span>

### <span data-ttu-id="37bd3-115">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="37bd3-115">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="37bd3-116">Anger tids gräns för klient sidan, i sekunder, för en tjänst förfrågan.</span><span class="sxs-lookup"><span data-stu-id="37bd3-116">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="37bd3-117">Om det föregående samtalet inte fungerar under det angivna intervallet, försöker den här cmdleten igen.</span><span class="sxs-lookup"><span data-stu-id="37bd3-117">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="37bd3-118">Om denna cmdlet inte får ett lyckat svar innan intervallet går ut returneras ett fel.</span><span class="sxs-lookup"><span data-stu-id="37bd3-118">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="37bd3-119">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="37bd3-119">-ConcurrentTaskCount</span></span>
<span data-ttu-id="37bd3-120">Anger maximalt antal samtidiga nätverks samtal.</span><span class="sxs-lookup"><span data-stu-id="37bd3-120">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="37bd3-121">Du kan använda den här parametern för att begränsa samtidigheten för att reglera den lokala processorn och bandbredds användning genom att ange det maximala antalet simultana nätverks samtal.</span><span class="sxs-lookup"><span data-stu-id="37bd3-121">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="37bd3-122">Det angivna värdet är ett absolut antal och multipliceras inte med antalet kärnor.</span><span class="sxs-lookup"><span data-stu-id="37bd3-122">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="37bd3-123">Den här parametern kan hjälpa till att minska nätverks anslutnings problem i miljöer med liten bandbredd, till exempel 100 kilobit per sekund.</span><span class="sxs-lookup"><span data-stu-id="37bd3-123">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="37bd3-124">Standardvärdet är 10.</span><span class="sxs-lookup"><span data-stu-id="37bd3-124">The default value is 10.</span></span>

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

### <span data-ttu-id="37bd3-125">-Kontext</span><span class="sxs-lookup"><span data-stu-id="37bd3-125">-Context</span></span>
<span data-ttu-id="37bd3-126">Anger lagrings kontexten.</span><span class="sxs-lookup"><span data-stu-id="37bd3-126">Specifies the storage context.</span></span>
<span data-ttu-id="37bd3-127">För att skapa den kan du använda New-AzureStorageContext cmdlet.</span><span class="sxs-lookup"><span data-stu-id="37bd3-127">To create it, you can use the New-AzureStorageContext cmdlet.</span></span>
<span data-ttu-id="37bd3-128">Cmdleten Miss lyckas när du använder en lagrings kontext som skapats från SAS-token eftersom cmdleten frågar efter behållar behörigheter som kräver nyckel behörighet för lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="37bd3-128">The cmdlet will fail when you use a storage context created from SAS Token because the cmdlet will query for container permissions which require Storage account key permission.</span></span>

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

### <span data-ttu-id="37bd3-129">-ContinuationToken</span><span class="sxs-lookup"><span data-stu-id="37bd3-129">-ContinuationToken</span></span>
<span data-ttu-id="37bd3-130">Anger ett fortsättnings-token för BLOB-listan.</span><span class="sxs-lookup"><span data-stu-id="37bd3-130">Specifies a continuation token for the blob list.</span></span>

```yaml
Type: BlobContinuationToken
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37bd3-131">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="37bd3-131">-MaxCount</span></span>
<span data-ttu-id="37bd3-132">Anger det maximala antalet objekt som denna cmdlet returnerar.</span><span class="sxs-lookup"><span data-stu-id="37bd3-132">Specifies the maximum number of objects that this cmdlet returns.</span></span>

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

### <span data-ttu-id="37bd3-133">-Namn</span><span class="sxs-lookup"><span data-stu-id="37bd3-133">-Name</span></span>
<span data-ttu-id="37bd3-134">Anger namnet på behållaren.</span><span class="sxs-lookup"><span data-stu-id="37bd3-134">Specifies the container name.</span></span>
<span data-ttu-id="37bd3-135">Om container namn är tomt visar cmdleten alla behållare.</span><span class="sxs-lookup"><span data-stu-id="37bd3-135">If container name is empty, the cmdlet lists all the containers.</span></span>
<span data-ttu-id="37bd3-136">Annars visas alla behållare som matchar det angivna namnet eller det vanliga namn mönstret.</span><span class="sxs-lookup"><span data-stu-id="37bd3-136">Otherwise, it lists all containers that match the specified name or the regular name pattern.</span></span>

```yaml
Type: String
Parameter Sets: ContainerName
Aliases: N, Container

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: True
```

### <span data-ttu-id="37bd3-137">-Prefix</span><span class="sxs-lookup"><span data-stu-id="37bd3-137">-Prefix</span></span>
<span data-ttu-id="37bd3-138">Anger ett prefix som används i namnet på den behållare eller de behållare som du vill hämta.</span><span class="sxs-lookup"><span data-stu-id="37bd3-138">Specifies a prefix used in the name of the container or containers you want to get.</span></span>
<span data-ttu-id="37bd3-139">Du kan använda den här för att hitta alla behållare som börjar med samma sträng, till exempel "min" eller "test".</span><span class="sxs-lookup"><span data-stu-id="37bd3-139">You can use this to find all containers that start with the same string, such as "my" or "test".</span></span>

```yaml
Type: String
Parameter Sets: ContainerPrefix
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37bd3-140">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="37bd3-140">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="37bd3-141">Anger timeout-intervall för tjänsten i sekunder för en begäran.</span><span class="sxs-lookup"><span data-stu-id="37bd3-141">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="37bd3-142">Om det angivna intervallet förflyter innan tjänsten bearbetar begäran returnerar lagrings tjänsten ett fel.</span><span class="sxs-lookup"><span data-stu-id="37bd3-142">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="37bd3-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37bd3-143">CommonParameters</span></span>
<span data-ttu-id="37bd3-144">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="37bd3-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37bd3-145">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="37bd3-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37bd3-146">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="37bd3-146">INPUTS</span></span>

### <span data-ttu-id="37bd3-147">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="37bd3-147">IStorageContext</span></span>

<span data-ttu-id="37bd3-148">Parametern ' context ' godkänner värdet av typen ' IStorageContext ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="37bd3-148">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="37bd3-149">Strängvärdet</span><span class="sxs-lookup"><span data-stu-id="37bd3-149">String</span></span>

<span data-ttu-id="37bd3-150">Parametern "name" accepterar värdet för typen String från pipeline</span><span class="sxs-lookup"><span data-stu-id="37bd3-150">Parameter 'Name' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="37bd3-151">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="37bd3-151">OUTPUTS</span></span>

### <span data-ttu-id="37bd3-152">Microsoft. WindowsAzure. commands. Common. Storage. ResourceModel. AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="37bd3-152">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageContainer</span></span>

## <span data-ttu-id="37bd3-153">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="37bd3-153">NOTES</span></span>

## <span data-ttu-id="37bd3-154">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="37bd3-154">RELATED LINKS</span></span>

[<span data-ttu-id="37bd3-155">New-AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="37bd3-155">New-AzureStorageContainer</span></span>](./New-AzureStorageContainer.md)

[<span data-ttu-id="37bd3-156">Remove-AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="37bd3-156">Remove-AzureStorageContainer</span></span>](./Remove-AzureStorageContainer.md)

[<span data-ttu-id="37bd3-157">Set-AzureStorageContainerAcl</span><span class="sxs-lookup"><span data-stu-id="37bd3-157">Set-AzureStorageContainerAcl</span></span>](./Set-AzureStorageContainerAcl.md)


