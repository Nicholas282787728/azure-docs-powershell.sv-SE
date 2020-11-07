---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 2B12BC19-EF8F-43F5-AF04-C570FEEA1AE6
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageContainer.md
ms.openlocfilehash: c95fcb42f403025399185f224a1438eac0f72867
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93746346"
---
# <span data-ttu-id="7514e-101">New-AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="7514e-101">New-AzStorageContainer</span></span>

## <span data-ttu-id="7514e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7514e-102">SYNOPSIS</span></span>
<span data-ttu-id="7514e-103">Skapar en Azure Storage-behållare.</span><span class="sxs-lookup"><span data-stu-id="7514e-103">Creates an Azure storage container.</span></span>

## <span data-ttu-id="7514e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7514e-104">SYNTAX</span></span>

```
New-AzStorageContainer [-Name] <String> [[-Permission] <BlobContainerPublicAccessType>]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="7514e-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7514e-105">DESCRIPTION</span></span>
<span data-ttu-id="7514e-106">Cmdleten **New-AzStorageContainer** skapar en Azure Storage-behållare.</span><span class="sxs-lookup"><span data-stu-id="7514e-106">The **New-AzStorageContainer** cmdlet creates an Azure storage container.</span></span>

## <span data-ttu-id="7514e-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7514e-107">EXAMPLES</span></span>

### <span data-ttu-id="7514e-108">Exempel 1: skapa en Azure Storage-behållare</span><span class="sxs-lookup"><span data-stu-id="7514e-108">Example 1: Create an Azure storage container</span></span>
```
PS C:\>New-AzStorageContainer -Name "ContainerName" -Permission Off
```

<span data-ttu-id="7514e-109">Det här kommandot skapar en lagrings behållare.</span><span class="sxs-lookup"><span data-stu-id="7514e-109">This command creates a storage container.</span></span>

### <span data-ttu-id="7514e-110">Exempel 2: skapa flera Azure Storage-behållare</span><span class="sxs-lookup"><span data-stu-id="7514e-110">Example 2: Create multiple Azure storage containers</span></span>
```
PS C:\>"container1 container2 container3".split() | New-AzStorageContainer -Permission Container
```

<span data-ttu-id="7514e-111">I det här exemplet skapas flera lagrings behållare.</span><span class="sxs-lookup"><span data-stu-id="7514e-111">This example creates multiple storage containers.</span></span>
<span data-ttu-id="7514e-112">Den använder metoden **Split** i **klassen .net och** skickar sedan namnen i pipeline.</span><span class="sxs-lookup"><span data-stu-id="7514e-112">It uses the **Split** method of the .NET **String** class and then passes the names on the pipeline.</span></span>

## <span data-ttu-id="7514e-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7514e-113">PARAMETERS</span></span>

### <span data-ttu-id="7514e-114">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="7514e-114">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="7514e-115">Anger tids gräns för klient sidan, i sekunder, för en tjänst förfrågan.</span><span class="sxs-lookup"><span data-stu-id="7514e-115">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="7514e-116">Om det föregående samtalet inte fungerar under det angivna intervallet, försöker den här cmdleten igen.</span><span class="sxs-lookup"><span data-stu-id="7514e-116">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="7514e-117">Om denna cmdlet inte får ett lyckat svar innan intervallet går ut returneras ett fel.</span><span class="sxs-lookup"><span data-stu-id="7514e-117">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="7514e-118">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="7514e-118">-ConcurrentTaskCount</span></span>
<span data-ttu-id="7514e-119">Anger maximalt antal samtidiga nätverks samtal.</span><span class="sxs-lookup"><span data-stu-id="7514e-119">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="7514e-120">Du kan använda den här parametern för att begränsa samtidigheten för att reglera den lokala processorn och bandbredds användning genom att ange det maximala antalet simultana nätverks samtal.</span><span class="sxs-lookup"><span data-stu-id="7514e-120">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="7514e-121">Det angivna värdet är ett absolut antal och multipliceras inte med antalet kärnor.</span><span class="sxs-lookup"><span data-stu-id="7514e-121">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="7514e-122">Den här parametern kan hjälpa till att minska nätverks anslutnings problem i miljöer med liten bandbredd, till exempel 100 kilobit per sekund.</span><span class="sxs-lookup"><span data-stu-id="7514e-122">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="7514e-123">Standardvärdet är 10.</span><span class="sxs-lookup"><span data-stu-id="7514e-123">The default value is 10.</span></span>

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

### <span data-ttu-id="7514e-124">-Kontext</span><span class="sxs-lookup"><span data-stu-id="7514e-124">-Context</span></span>
<span data-ttu-id="7514e-125">Anger en kontext för den nya behållaren.</span><span class="sxs-lookup"><span data-stu-id="7514e-125">Specifies a context for the new container.</span></span>

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

### <span data-ttu-id="7514e-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7514e-126">-DefaultProfile</span></span>
<span data-ttu-id="7514e-127">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="7514e-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7514e-128">-Namn</span><span class="sxs-lookup"><span data-stu-id="7514e-128">-Name</span></span>
<span data-ttu-id="7514e-129">Anger ett namn för den nya behållaren.</span><span class="sxs-lookup"><span data-stu-id="7514e-129">Specifies a name for the new container.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Container

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7514e-130">-Tillstånd</span><span class="sxs-lookup"><span data-stu-id="7514e-130">-Permission</span></span>
<span data-ttu-id="7514e-131">Anger nivån för offentlig åtkomst till den här behållaren.</span><span class="sxs-lookup"><span data-stu-id="7514e-131">Specifies the level of public access to this container.</span></span>
<span data-ttu-id="7514e-132">Som standard kan bara en container och alla BLOB-objekt nås av lagrings kontots ägare.</span><span class="sxs-lookup"><span data-stu-id="7514e-132">By default, the container and any blobs in it can be accessed only by the owner of the storage account.</span></span>
<span data-ttu-id="7514e-133">Om du vill ge anonyma användare Läs behörigheter till en behållare och dess BLOB-objekt kan du ange behållar behörigheter för att aktivera offentlig åtkomst.</span><span class="sxs-lookup"><span data-stu-id="7514e-133">To grant anonymous users read permissions to a container and its blobs, you can set the container permissions to enable public access.</span></span>
<span data-ttu-id="7514e-134">Anonyma användare kan läsa BLOB i en offentligt tillgänglig container utan att autentisera begäran.</span><span class="sxs-lookup"><span data-stu-id="7514e-134">Anonymous users can read blobs in a publicly available container without authenticating the request.</span></span>
<span data-ttu-id="7514e-135">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="7514e-135">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="7514e-136">Beh.</span><span class="sxs-lookup"><span data-stu-id="7514e-136">Container.</span></span>
<span data-ttu-id="7514e-137">Ger fullständig Läs åtkomst till en behållare och dess blob.</span><span class="sxs-lookup"><span data-stu-id="7514e-137">Provides full read access to a container and its blobs.</span></span>
<span data-ttu-id="7514e-138">Klienter kan räkna upp blobs i behållaren via anonym begäran men kan inte räkna upp behållare i lagrings kontot.</span><span class="sxs-lookup"><span data-stu-id="7514e-138">Clients can enumerate blobs in the container through anonymous request, but cannot enumerate containers in the storage account.</span></span> 
- <span data-ttu-id="7514e-139">Object.</span><span class="sxs-lookup"><span data-stu-id="7514e-139">Blob.</span></span>
<span data-ttu-id="7514e-140">Ger Läs åtkomst till BLOB-data över hela en behållare via anonym begäran, men ger inte åtkomst till behållar data.</span><span class="sxs-lookup"><span data-stu-id="7514e-140">Provides read access to blob data throughout a container through anonymous request, but does not provide access to container data.</span></span>
<span data-ttu-id="7514e-141">Klienter kan inte räkna upp blobbar i behållaren med anonym begäran.</span><span class="sxs-lookup"><span data-stu-id="7514e-141">Clients cannot enumerate blobs in the container by using anonymous request.</span></span> 
- <span data-ttu-id="7514e-142">Ras.</span><span class="sxs-lookup"><span data-stu-id="7514e-142">Off.</span></span>
<span data-ttu-id="7514e-143">Vilka begränsar åtkomsten till lagrings kontots ägare.</span><span class="sxs-lookup"><span data-stu-id="7514e-143">Which restricts access to only the storage account owner.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.WindowsAzure.Storage.Blob.BlobContainerPublicAccessType]
Parameter Sets: (All)
Aliases: PublicAccess
Accepted values: Off, Container, Blob, Unknown

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7514e-144">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="7514e-144">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="7514e-145">Anger timeout-intervall för tjänsten i sekunder för en begäran.</span><span class="sxs-lookup"><span data-stu-id="7514e-145">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="7514e-146">Om det angivna intervallet förflyter innan tjänsten bearbetar begäran returnerar lagrings tjänsten ett fel.</span><span class="sxs-lookup"><span data-stu-id="7514e-146">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="7514e-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7514e-147">CommonParameters</span></span>
<span data-ttu-id="7514e-148">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7514e-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7514e-149">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7514e-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7514e-150">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7514e-150">INPUTS</span></span>

### <span data-ttu-id="7514e-151">System. String</span><span class="sxs-lookup"><span data-stu-id="7514e-151">System.String</span></span>

### <span data-ttu-id="7514e-152">Microsoft. Azure. commands. Common. verifikation. abstraktioner. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="7514e-152">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="7514e-153">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7514e-153">OUTPUTS</span></span>

### <span data-ttu-id="7514e-154">Microsoft. WindowsAzure. commands. Common. Storage. ResourceModel. AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="7514e-154">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageContainer</span></span>

## <span data-ttu-id="7514e-155">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7514e-155">NOTES</span></span>

## <span data-ttu-id="7514e-156">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7514e-156">RELATED LINKS</span></span>

[<span data-ttu-id="7514e-157">Get-AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="7514e-157">Get-AzStorageContainer</span></span>](./Get-AzStorageContainer.md)

[<span data-ttu-id="7514e-158">Remove-AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="7514e-158">Remove-AzStorageContainer</span></span>](./Remove-AzStorageContainer.md)

[<span data-ttu-id="7514e-159">Set-AzStorageContainerAcl</span><span class="sxs-lookup"><span data-stu-id="7514e-159">Set-AzStorageContainerAcl</span></span>](./Set-AzStorageContainerAcl.md)


