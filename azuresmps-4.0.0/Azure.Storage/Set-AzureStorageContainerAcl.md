---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: BDEEF1EA-A785-4E17-9887-C2000BDFCF57
online version: ''
schema: 2.0.0
ms.openlocfilehash: fa33f6ba457ad51504cc9005f70f0e4c8f529359
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93572480"
---
# <span data-ttu-id="cf1af-101">Set-AzureStorageContainerAcl</span><span class="sxs-lookup"><span data-stu-id="cf1af-101">Set-AzureStorageContainerAcl</span></span>

## <span data-ttu-id="cf1af-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="cf1af-102">SYNOPSIS</span></span>
<span data-ttu-id="cf1af-103">Ställer in offentlig åtkomst till en lagrings behållare.</span><span class="sxs-lookup"><span data-stu-id="cf1af-103">Sets the public access permission to a storage container.</span></span>

## <span data-ttu-id="cf1af-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="cf1af-104">SYNTAX</span></span>

```
Set-AzureStorageContainerAcl [-Name] <String> [-Permission] <BlobContainerPublicAccessType> [-PassThru]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="cf1af-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="cf1af-105">DESCRIPTION</span></span>
<span data-ttu-id="cf1af-106">Cmdleten **set-AzureStorageContainerAcl** anger offentlig åtkomst behörighet för den angivna lagrings behållaren i Azure.</span><span class="sxs-lookup"><span data-stu-id="cf1af-106">The **Set-AzureStorageContainerAcl** cmdlet sets the public access permission to the specified storage container in Azure.</span></span>

## <span data-ttu-id="cf1af-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="cf1af-107">EXAMPLES</span></span>

### <span data-ttu-id="cf1af-108">Exempel 1: ange ACL för Azure Storage-behållare med namn</span><span class="sxs-lookup"><span data-stu-id="cf1af-108">Example 1: Set azure storage container ACL by name</span></span>
```
PS C:\>Set-AzureStorageContainerAcl -Container "Container01" -Permission Off -PassThru
```

<span data-ttu-id="cf1af-109">Det här kommandot skapar en behållare som inte har offentlig åtkomst.</span><span class="sxs-lookup"><span data-stu-id="cf1af-109">This command creates a container that has no public access.</span></span>

### <span data-ttu-id="cf1af-110">Exempel 2: ange ACL för Azure Storage-behållare genom att använda pipeline</span><span class="sxs-lookup"><span data-stu-id="cf1af-110">Example 2: Set azure storage container ACL by using the pipeline</span></span>
```
PS C:\>Get-AzureStorageContainer container* | Set-AzureStorageContainerAcl -Permission Blob -PassThru
```

<span data-ttu-id="cf1af-111">Det här kommandot får alla lagrings behållare vars namn börjar med en container och skickar sedan resultatet i pipeline för att ställa in behörigheten för alla till BLOB-åtkomst.</span><span class="sxs-lookup"><span data-stu-id="cf1af-111">This command gets all storage containers whose name starts with container and then passes the result on the pipeline to set the permission for them all to Blob access.</span></span>

## <span data-ttu-id="cf1af-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="cf1af-112">PARAMETERS</span></span>

### <span data-ttu-id="cf1af-113">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="cf1af-113">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="cf1af-114">Anger tids gräns för klient sidan, i sekunder, för en tjänst förfrågan.</span><span class="sxs-lookup"><span data-stu-id="cf1af-114">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="cf1af-115">Om det föregående samtalet inte fungerar under det angivna intervallet, försöker den här cmdleten igen.</span><span class="sxs-lookup"><span data-stu-id="cf1af-115">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="cf1af-116">Om denna cmdlet inte får ett lyckat svar innan intervallet går ut returneras ett fel.</span><span class="sxs-lookup"><span data-stu-id="cf1af-116">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="cf1af-117">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="cf1af-117">-ConcurrentTaskCount</span></span>
<span data-ttu-id="cf1af-118">Anger maximalt antal samtidiga nätverks samtal.</span><span class="sxs-lookup"><span data-stu-id="cf1af-118">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="cf1af-119">Du kan använda den här parametern för att begränsa samtidigheten för att reglera den lokala processorn och bandbredds användning genom att ange det maximala antalet simultana nätverks samtal.</span><span class="sxs-lookup"><span data-stu-id="cf1af-119">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="cf1af-120">Det angivna värdet är ett absolut antal och multipliceras inte med antalet kärnor.</span><span class="sxs-lookup"><span data-stu-id="cf1af-120">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="cf1af-121">Den här parametern kan hjälpa till att minska nätverks anslutnings problem i miljöer med liten bandbredd, till exempel 100 kilobit per sekund.</span><span class="sxs-lookup"><span data-stu-id="cf1af-121">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="cf1af-122">Standardvärdet är 10.</span><span class="sxs-lookup"><span data-stu-id="cf1af-122">The default value is 10.</span></span>

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

### <span data-ttu-id="cf1af-123">-Kontext</span><span class="sxs-lookup"><span data-stu-id="cf1af-123">-Context</span></span>
<span data-ttu-id="cf1af-124">Anger Azure Storage-kontexten.</span><span class="sxs-lookup"><span data-stu-id="cf1af-124">Specifies the Azure storage context.</span></span>
<span data-ttu-id="cf1af-125">Du kan skapa det med hjälp av New-AzureStorageContext cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cf1af-125">You can create it by using the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="cf1af-126">-Namn</span><span class="sxs-lookup"><span data-stu-id="cf1af-126">-Name</span></span>
<span data-ttu-id="cf1af-127">Anger ett namn på en behållare.</span><span class="sxs-lookup"><span data-stu-id="cf1af-127">Specifies a container name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, Container

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cf1af-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cf1af-128">-PassThru</span></span>
<span data-ttu-id="cf1af-129">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="cf1af-129">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="cf1af-130">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="cf1af-130">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf1af-131">-Tillstånd</span><span class="sxs-lookup"><span data-stu-id="cf1af-131">-Permission</span></span>
<span data-ttu-id="cf1af-132">Anger nivån för offentlig åtkomst till den här behållaren.</span><span class="sxs-lookup"><span data-stu-id="cf1af-132">Specifies the level of public access to this container.</span></span>
<span data-ttu-id="cf1af-133">Som standard kan bara en container och alla BLOB-objekt nås av lagrings kontots ägare.</span><span class="sxs-lookup"><span data-stu-id="cf1af-133">By default, the container and any blobs in it can be accessed only by the owner of the storage account.</span></span>
<span data-ttu-id="cf1af-134">Om du vill ge anonyma användare Läs behörigheter till en behållare och dess BLOB-objekt kan du ange behållar behörigheter för att aktivera offentlig åtkomst.</span><span class="sxs-lookup"><span data-stu-id="cf1af-134">To grant anonymous users read permissions to a container and its blobs, you can set the container permissions to enable public access.</span></span>
<span data-ttu-id="cf1af-135">Anonyma användare kan läsa BLOB i en offentligt tillgänglig container utan att autentisera begäran.</span><span class="sxs-lookup"><span data-stu-id="cf1af-135">Anonymous users can read blobs in a publicly available container without authenticating the request.</span></span>
<span data-ttu-id="cf1af-136">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="cf1af-136">The acceptable values for this parameter are:</span></span>

<span data-ttu-id="cf1af-137">--Container.</span><span class="sxs-lookup"><span data-stu-id="cf1af-137">--Container.</span></span>
<span data-ttu-id="cf1af-138">Ger fullständig Läs åtkomst till en behållare och dess blob.</span><span class="sxs-lookup"><span data-stu-id="cf1af-138">Provides full read access to a container and its blobs.</span></span>
<span data-ttu-id="cf1af-139">Klienter kan räkna upp blobs i behållaren via anonym begäran men kan inte räkna upp behållare i lagrings kontot.</span><span class="sxs-lookup"><span data-stu-id="cf1af-139">Clients can enumerate blobs in the container through anonymous request, but cannot enumerate containers in the storage account.</span></span> <span data-ttu-id="cf1af-140">--Blob.</span><span class="sxs-lookup"><span data-stu-id="cf1af-140">--Blob.</span></span>
<span data-ttu-id="cf1af-141">Ger Läs åtkomst till BLOB-data i en behållare via anonym begäran, men ger inte åtkomst till behållar data.</span><span class="sxs-lookup"><span data-stu-id="cf1af-141">Provides read access to blob data in a container through anonymous request, but does not provide access to container data.</span></span>
<span data-ttu-id="cf1af-142">Klienter kan inte räkna upp blobbar i behållaren med anonym begäran.</span><span class="sxs-lookup"><span data-stu-id="cf1af-142">Clients cannot enumerate blobs in the container by using anonymous request.</span></span> <span data-ttu-id="cf1af-143">-Av.</span><span class="sxs-lookup"><span data-stu-id="cf1af-143">--Off.</span></span>
<span data-ttu-id="cf1af-144">Begränsar åtkomst till lagrings kontots ägare.</span><span class="sxs-lookup"><span data-stu-id="cf1af-144">Restricts access to only the storage account owner.</span></span>

```yaml
Type: BlobContainerPublicAccessType
Parameter Sets: (All)
Aliases: PublicAccess
Accepted values: Off, Container, Blob

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf1af-145">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="cf1af-145">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="cf1af-146">Anger timeout-intervall för tjänsten i sekunder för en begäran.</span><span class="sxs-lookup"><span data-stu-id="cf1af-146">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="cf1af-147">Om det angivna intervallet förflyter innan tjänsten bearbetar begäran returnerar lagrings tjänsten ett fel.</span><span class="sxs-lookup"><span data-stu-id="cf1af-147">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>
<span data-ttu-id="cf1af-148">Timeout för servern för varje begäran.</span><span class="sxs-lookup"><span data-stu-id="cf1af-148">Server side time out for each request.</span></span>

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

### <span data-ttu-id="cf1af-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf1af-149">CommonParameters</span></span>
<span data-ttu-id="cf1af-150">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cf1af-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf1af-151">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cf1af-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf1af-152">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="cf1af-152">INPUTS</span></span>

## <span data-ttu-id="cf1af-153">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="cf1af-153">OUTPUTS</span></span>

## <span data-ttu-id="cf1af-154">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="cf1af-154">NOTES</span></span>

## <span data-ttu-id="cf1af-155">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="cf1af-155">RELATED LINKS</span></span>

[<span data-ttu-id="cf1af-156">Get-AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="cf1af-156">Get-AzureStorageContainer</span></span>](./Get-AzureStorageContainer.md)

[<span data-ttu-id="cf1af-157">New-AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="cf1af-157">New-AzureStorageContainer</span></span>](./New-AzureStorageContainer.md)

[<span data-ttu-id="cf1af-158">Remove-AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="cf1af-158">Remove-AzureStorageContainer</span></span>](./Remove-AzureStorageContainer.md)


