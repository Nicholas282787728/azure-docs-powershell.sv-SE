---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 90C3DF13-0010-49B6-A8CD-C6AC34BC3EFA
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageContainer.md
ms.openlocfilehash: 0c26899b772fd21772b625cb057e141071767002
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94088965"
---
# <span data-ttu-id="b8ef4-101">Get-AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="b8ef4-101">Get-AzStorageContainer</span></span>

## <span data-ttu-id="b8ef4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b8ef4-102">SYNOPSIS</span></span>
<span data-ttu-id="b8ef4-103">Visar lagrings behållarna.</span><span class="sxs-lookup"><span data-stu-id="b8ef4-103">Lists the storage containers.</span></span>

## <span data-ttu-id="b8ef4-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b8ef4-104">SYNTAX</span></span>

### <span data-ttu-id="b8ef4-105">ContainerName (standard)</span><span class="sxs-lookup"><span data-stu-id="b8ef4-105">ContainerName (Default)</span></span>
```
Get-AzStorageContainer [[-Name] <String>] [-MaxCount <Int32>] [-ContinuationToken <BlobContinuationToken>]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="b8ef4-106">ContainerPrefix</span><span class="sxs-lookup"><span data-stu-id="b8ef4-106">ContainerPrefix</span></span>
```
Get-AzStorageContainer -Prefix <String> [-MaxCount <Int32>] [-ContinuationToken <BlobContinuationToken>]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="b8ef4-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b8ef4-107">DESCRIPTION</span></span>
<span data-ttu-id="b8ef4-108">Cmdleten **Get-AzStorageContainer** innehåller lagrings containrarna som är kopplade till lagrings kontot i Azure.</span><span class="sxs-lookup"><span data-stu-id="b8ef4-108">The **Get-AzStorageContainer** cmdlet lists the storage containers associated with the storage account in Azure.</span></span>

## <span data-ttu-id="b8ef4-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b8ef4-109">EXAMPLES</span></span>

### <span data-ttu-id="b8ef4-110">Exempel 1: skaffa Azure Storage BLOB efter namn</span><span class="sxs-lookup"><span data-stu-id="b8ef4-110">Example 1: Get Azure Storage blob by name</span></span>
```
PS C:\>Get-AzStorageContainer -Name container*
```

<span data-ttu-id="b8ef4-111">I det här exemplet används ett jokertecken för att returnera en lista över alla behållare med ett namn som börjar med en container.</span><span class="sxs-lookup"><span data-stu-id="b8ef4-111">This example uses a wildcard character to return a list of all containers with a name that starts with container.</span></span>

### <span data-ttu-id="b8ef4-112">Exempel 2: Hämta en Azure Storage-behållare efter container namn</span><span class="sxs-lookup"><span data-stu-id="b8ef4-112">Example 2: Get Azure Storage container by container name prefix</span></span>
```
PS C:\>Get-AzStorageContainer -Prefix "container"
```

<span data-ttu-id="b8ef4-113">I det här exemplet används parametern *prefix* för att returnera en lista över alla behållare med ett namn som börjar med en container.</span><span class="sxs-lookup"><span data-stu-id="b8ef4-113">This example uses the *Prefix* parameter to return a list of all containers with a name that starts with container.</span></span>

## <span data-ttu-id="b8ef4-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b8ef4-114">PARAMETERS</span></span>

### <span data-ttu-id="b8ef4-115">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="b8ef4-115">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="b8ef4-116">Anger tids gräns för klient sidan, i sekunder, för en tjänst förfrågan.</span><span class="sxs-lookup"><span data-stu-id="b8ef4-116">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="b8ef4-117">Om det föregående samtalet inte fungerar under det angivna intervallet, försöker den här cmdleten igen.</span><span class="sxs-lookup"><span data-stu-id="b8ef4-117">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="b8ef4-118">Om denna cmdlet inte får ett lyckat svar innan intervallet går ut returneras ett fel.</span><span class="sxs-lookup"><span data-stu-id="b8ef4-118">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: ClientTimeoutPerRequestInSeconds

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8ef4-119">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="b8ef4-119">-ConcurrentTaskCount</span></span>
<span data-ttu-id="b8ef4-120">Anger maximalt antal samtidiga nätverks samtal.</span><span class="sxs-lookup"><span data-stu-id="b8ef4-120">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="b8ef4-121">Du kan använda den här parametern för att begränsa samtidigheten för att reglera den lokala processorn och bandbredds användning genom att ange det maximala antalet simultana nätverks samtal.</span><span class="sxs-lookup"><span data-stu-id="b8ef4-121">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="b8ef4-122">Det angivna värdet är ett absolut antal och multipliceras inte med antalet kärnor.</span><span class="sxs-lookup"><span data-stu-id="b8ef4-122">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="b8ef4-123">Den här parametern kan hjälpa till att minska nätverks anslutnings problem i miljöer med liten bandbredd, till exempel 100 kilobit per sekund.</span><span class="sxs-lookup"><span data-stu-id="b8ef4-123">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="b8ef4-124">Standardvärdet är 10.</span><span class="sxs-lookup"><span data-stu-id="b8ef4-124">The default value is 10.</span></span>

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

### <span data-ttu-id="b8ef4-125">-Kontext</span><span class="sxs-lookup"><span data-stu-id="b8ef4-125">-Context</span></span>
<span data-ttu-id="b8ef4-126">Anger lagrings kontexten.</span><span class="sxs-lookup"><span data-stu-id="b8ef4-126">Specifies the storage context.</span></span>
<span data-ttu-id="b8ef4-127">För att skapa den kan du använda New-AzStorageContext cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b8ef4-127">To create it, you can use the New-AzStorageContext cmdlet.</span></span>
<span data-ttu-id="b8ef4-128">Behörigheter för behållarna hämtas inte när du använder en lagrings kontext skapad från SAS-token eftersom behörigheter för en fråge behållare kräver nyckel för lagrings konto nyckeln.</span><span class="sxs-lookup"><span data-stu-id="b8ef4-128">The container permissions won't be retrieved when you use a storage context created from SAS Token, because query container permissions requires Storage account key permission.</span></span>

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

### <span data-ttu-id="b8ef4-129">-ContinuationToken</span><span class="sxs-lookup"><span data-stu-id="b8ef4-129">-ContinuationToken</span></span>
<span data-ttu-id="b8ef4-130">Anger ett fortsättnings-token för BLOB-listan.</span><span class="sxs-lookup"><span data-stu-id="b8ef4-130">Specifies a continuation token for the blob list.</span></span>

```yaml
Type: Microsoft.Azure.Storage.Blob.BlobContinuationToken
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8ef4-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8ef4-131">-DefaultProfile</span></span>
<span data-ttu-id="b8ef4-132">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b8ef4-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8ef4-133">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="b8ef4-133">-MaxCount</span></span>
<span data-ttu-id="b8ef4-134">Anger det maximala antalet objekt som denna cmdlet returnerar.</span><span class="sxs-lookup"><span data-stu-id="b8ef4-134">Specifies the maximum number of objects that this cmdlet returns.</span></span>

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

### <span data-ttu-id="b8ef4-135">-Namn</span><span class="sxs-lookup"><span data-stu-id="b8ef4-135">-Name</span></span>
<span data-ttu-id="b8ef4-136">Anger namnet på behållaren.</span><span class="sxs-lookup"><span data-stu-id="b8ef4-136">Specifies the container name.</span></span>
<span data-ttu-id="b8ef4-137">Om container namn är tomt visar cmdleten alla behållare.</span><span class="sxs-lookup"><span data-stu-id="b8ef4-137">If container name is empty, the cmdlet lists all the containers.</span></span>
<span data-ttu-id="b8ef4-138">Annars visas alla behållare som matchar det angivna namnet eller det vanliga namn mönstret.</span><span class="sxs-lookup"><span data-stu-id="b8ef4-138">Otherwise, it lists all containers that match the specified name or the regular name pattern.</span></span>

```yaml
Type: System.String
Parameter Sets: ContainerName
Aliases: N, Container

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b8ef4-139">-Prefix</span><span class="sxs-lookup"><span data-stu-id="b8ef4-139">-Prefix</span></span>
<span data-ttu-id="b8ef4-140">Anger ett prefix som används i namnet på den behållare eller de behållare som du vill hämta.</span><span class="sxs-lookup"><span data-stu-id="b8ef4-140">Specifies a prefix used in the name of the container or containers you want to get.</span></span>
<span data-ttu-id="b8ef4-141">Du kan använda den här för att hitta alla behållare som börjar med samma sträng, till exempel "min" eller "test".</span><span class="sxs-lookup"><span data-stu-id="b8ef4-141">You can use this to find all containers that start with the same string, such as "my" or "test".</span></span>

```yaml
Type: System.String
Parameter Sets: ContainerPrefix
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8ef4-142">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="b8ef4-142">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="b8ef4-143">Anger timeout-intervall för tjänsten i sekunder för en begäran.</span><span class="sxs-lookup"><span data-stu-id="b8ef4-143">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="b8ef4-144">Om det angivna intervallet förflyter innan tjänsten bearbetar begäran returnerar lagrings tjänsten ett fel.</span><span class="sxs-lookup"><span data-stu-id="b8ef4-144">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: ServerTimeoutPerRequestInSeconds

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8ef4-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8ef4-145">CommonParameters</span></span>
<span data-ttu-id="b8ef4-146">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b8ef4-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8ef4-147">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b8ef4-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8ef4-148">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b8ef4-148">INPUTS</span></span>

### <span data-ttu-id="b8ef4-149">System. String</span><span class="sxs-lookup"><span data-stu-id="b8ef4-149">System.String</span></span>

### <span data-ttu-id="b8ef4-150">Microsoft. Azure. commands. Common. verifikation. abstraktioner. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="b8ef4-150">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="b8ef4-151">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b8ef4-151">OUTPUTS</span></span>

### <span data-ttu-id="b8ef4-152">Microsoft. WindowsAzure. commands. Common. Storage. ResourceModel. AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="b8ef4-152">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageContainer</span></span>

## <span data-ttu-id="b8ef4-153">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b8ef4-153">NOTES</span></span>

## <span data-ttu-id="b8ef4-154">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b8ef4-154">RELATED LINKS</span></span>

[<span data-ttu-id="b8ef4-155">New-AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="b8ef4-155">New-AzStorageContainer</span></span>](./New-AzStorageContainer.md)

[<span data-ttu-id="b8ef4-156">Remove-AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="b8ef4-156">Remove-AzStorageContainer</span></span>](./Remove-AzStorageContainer.md)

[<span data-ttu-id="b8ef4-157">Set-AzStorageContainerAcl</span><span class="sxs-lookup"><span data-stu-id="b8ef4-157">Set-AzStorageContainerAcl</span></span>](./Set-AzStorageContainerAcl.md)


