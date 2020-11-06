---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 90C3DF13-0010-49B6-A8CD-C6AC34BC3EFA
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageContainer.md
gitcommit: https://github.com/Azure/azure-powershell/blob/1fa63f743120d7a7cd6cbb28ee43cd0f4c654af9
ms.openlocfilehash: c94c9b9d04745fe22c8836be1858c59c253d4b63
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93581588"
---
# <span data-ttu-id="92e84-101">Get-AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="92e84-101">Get-AzureStorageContainer</span></span>

## <span data-ttu-id="92e84-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="92e84-102">SYNOPSIS</span></span>
<span data-ttu-id="92e84-103">Visar lagrings behållarna.</span><span class="sxs-lookup"><span data-stu-id="92e84-103">Lists the storage containers.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="92e84-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="92e84-104">SYNTAX</span></span>

### <span data-ttu-id="92e84-105">ContainerName (standard)</span><span class="sxs-lookup"><span data-stu-id="92e84-105">ContainerName (Default)</span></span>
```
Get-AzureStorageContainer [[-Name] <String>] [-MaxCount <Int32>] [-ContinuationToken <BlobContinuationToken>]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="92e84-106">ContainerPrefix</span><span class="sxs-lookup"><span data-stu-id="92e84-106">ContainerPrefix</span></span>
```
Get-AzureStorageContainer -Prefix <String> [-MaxCount <Int32>] [-ContinuationToken <BlobContinuationToken>]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="92e84-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="92e84-107">DESCRIPTION</span></span>
<span data-ttu-id="92e84-108">Cmdleten **Get-AzureStorageContainer** innehåller lagrings containrarna som är kopplade till lagrings kontot i Azure.</span><span class="sxs-lookup"><span data-stu-id="92e84-108">The **Get-AzureStorageContainer** cmdlet lists the storage containers associated with the storage account in Azure.</span></span>

## <span data-ttu-id="92e84-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="92e84-109">EXAMPLES</span></span>

### <span data-ttu-id="92e84-110">Exempel 1: skaffa Azure Storage BLOB efter namn</span><span class="sxs-lookup"><span data-stu-id="92e84-110">Example 1: Get Azure Storage blob by name</span></span>
```
PS C:\>Get-AzureStorageContainer -Name container*
```

<span data-ttu-id="92e84-111">I det här exemplet används ett jokertecken för att returnera en lista över alla behållare med ett namn som börjar med en container.</span><span class="sxs-lookup"><span data-stu-id="92e84-111">This example uses a wildcard character to return a list of all containers with a name that starts with container.</span></span>

### <span data-ttu-id="92e84-112">Exempel 2: Hämta en Azure Storage-behållare efter container namn</span><span class="sxs-lookup"><span data-stu-id="92e84-112">Example 2: Get Azure Storage container by container name prefix</span></span>
```
PS C:\>Get-AzureStorageContainer -Prefix "container"
```

<span data-ttu-id="92e84-113">I det här exemplet används parametern *prefix* för att returnera en lista över alla behållare med ett namn som börjar med en container.</span><span class="sxs-lookup"><span data-stu-id="92e84-113">This example uses the *Prefix* parameter to return a list of all containers with a name that starts with container.</span></span>

## <span data-ttu-id="92e84-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="92e84-114">PARAMETERS</span></span>

### <span data-ttu-id="92e84-115">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="92e84-115">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="92e84-116">Anger tids gräns för klient sidan, i sekunder, för en tjänst förfrågan.</span><span class="sxs-lookup"><span data-stu-id="92e84-116">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="92e84-117">Om det föregående samtalet inte fungerar under det angivna intervallet, försöker den här cmdleten igen.</span><span class="sxs-lookup"><span data-stu-id="92e84-117">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="92e84-118">Om denna cmdlet inte får ett lyckat svar innan intervallet går ut returneras ett fel.</span><span class="sxs-lookup"><span data-stu-id="92e84-118">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="92e84-119">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="92e84-119">-ConcurrentTaskCount</span></span>
<span data-ttu-id="92e84-120">Anger maximalt antal samtidiga nätverks samtal.</span><span class="sxs-lookup"><span data-stu-id="92e84-120">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="92e84-121">Du kan använda den här parametern för att begränsa samtidigheten för att reglera den lokala processorn och bandbredds användning genom att ange det maximala antalet simultana nätverks samtal.</span><span class="sxs-lookup"><span data-stu-id="92e84-121">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="92e84-122">Det angivna värdet är ett absolut antal och multipliceras inte med antalet kärnor.</span><span class="sxs-lookup"><span data-stu-id="92e84-122">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="92e84-123">Den här parametern kan hjälpa till att minska nätverks anslutnings problem i miljöer med liten bandbredd, till exempel 100 kilobit per sekund.</span><span class="sxs-lookup"><span data-stu-id="92e84-123">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="92e84-124">Standardvärdet är 10.</span><span class="sxs-lookup"><span data-stu-id="92e84-124">The default value is 10.</span></span>

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

### <span data-ttu-id="92e84-125">-Kontext</span><span class="sxs-lookup"><span data-stu-id="92e84-125">-Context</span></span>
<span data-ttu-id="92e84-126">Anger lagrings kontexten.</span><span class="sxs-lookup"><span data-stu-id="92e84-126">Specifies the storage context.</span></span>
<span data-ttu-id="92e84-127">För att skapa den kan du använda New-AzureStorageContext cmdlet.</span><span class="sxs-lookup"><span data-stu-id="92e84-127">To create it, you can use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="92e84-128">-ContinuationToken</span><span class="sxs-lookup"><span data-stu-id="92e84-128">-ContinuationToken</span></span>
<span data-ttu-id="92e84-129">Anger ett fortsättnings-token för BLOB-listan.</span><span class="sxs-lookup"><span data-stu-id="92e84-129">Specifies a continuation token for the blob list.</span></span>

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

### <span data-ttu-id="92e84-130">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="92e84-130">-MaxCount</span></span>
<span data-ttu-id="92e84-131">Anger det maximala antalet objekt som denna cmdlet returnerar.</span><span class="sxs-lookup"><span data-stu-id="92e84-131">Specifies the maximum number of objects that this cmdlet returns.</span></span>

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

### <span data-ttu-id="92e84-132">-Namn</span><span class="sxs-lookup"><span data-stu-id="92e84-132">-Name</span></span>
<span data-ttu-id="92e84-133">Anger namnet på behållaren.</span><span class="sxs-lookup"><span data-stu-id="92e84-133">Specifies the container name.</span></span>
<span data-ttu-id="92e84-134">Om container namn är tomt visar cmdleten alla behållare.</span><span class="sxs-lookup"><span data-stu-id="92e84-134">If container name is empty, the cmdlet lists all the containers.</span></span>
<span data-ttu-id="92e84-135">Annars visas alla behållare som matchar det angivna namnet eller det vanliga namn mönstret.</span><span class="sxs-lookup"><span data-stu-id="92e84-135">Otherwise, it lists all containers that match the specified name or the regular name pattern.</span></span>

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

### <span data-ttu-id="92e84-136">-Prefix</span><span class="sxs-lookup"><span data-stu-id="92e84-136">-Prefix</span></span>
<span data-ttu-id="92e84-137">Anger ett prefix som används i namnet på den behållare eller de behållare som du vill hämta.</span><span class="sxs-lookup"><span data-stu-id="92e84-137">Specifies a prefix used in the name of the container or containers you want to get.</span></span>
<span data-ttu-id="92e84-138">Du kan använda den här för att hitta alla behållare som börjar med samma sträng, till exempel "min" eller "test".</span><span class="sxs-lookup"><span data-stu-id="92e84-138">You can use this to find all containers that start with the same string, such as "my" or "test".</span></span>

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

### <span data-ttu-id="92e84-139">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="92e84-139">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="92e84-140">Anger timeout-intervall för tjänsten i sekunder för en begäran.</span><span class="sxs-lookup"><span data-stu-id="92e84-140">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="92e84-141">Om det angivna intervallet förflyter innan tjänsten bearbetar begäran returnerar lagrings tjänsten ett fel.</span><span class="sxs-lookup"><span data-stu-id="92e84-141">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="92e84-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92e84-142">CommonParameters</span></span>
<span data-ttu-id="92e84-143">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="92e84-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92e84-144">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="92e84-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92e84-145">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="92e84-145">INPUTS</span></span>

### <span data-ttu-id="92e84-146">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="92e84-146">IStorageContext</span></span>

<span data-ttu-id="92e84-147">Parametern ' context ' godkänner värdet av typen ' IStorageContext ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="92e84-147">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="92e84-148">Strängvärdet</span><span class="sxs-lookup"><span data-stu-id="92e84-148">String</span></span>

<span data-ttu-id="92e84-149">Parametern "name" accepterar värdet för typen String från pipeline</span><span class="sxs-lookup"><span data-stu-id="92e84-149">Parameter 'Name' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="92e84-150">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="92e84-150">OUTPUTS</span></span>

### <span data-ttu-id="92e84-151">Microsoft. WindowsAzure. commands. Common. Storage. ResourceModel. AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="92e84-151">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageContainer</span></span>

## <span data-ttu-id="92e84-152">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="92e84-152">NOTES</span></span>

## <span data-ttu-id="92e84-153">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="92e84-153">RELATED LINKS</span></span>

[<span data-ttu-id="92e84-154">New-AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="92e84-154">New-AzureStorageContainer</span></span>](./New-AzureStorageContainer.md)

[<span data-ttu-id="92e84-155">Remove-AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="92e84-155">Remove-AzureStorageContainer</span></span>](./Remove-AzureStorageContainer.md)

[<span data-ttu-id="92e84-156">Set-AzureStorageContainerAcl</span><span class="sxs-lookup"><span data-stu-id="92e84-156">Set-AzureStorageContainerAcl</span></span>](./Set-AzureStorageContainerAcl.md)


