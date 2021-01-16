---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 2B12BC19-EF8F-43F5-AF04-C570FEEA1AE6
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageContainer.md
ms.openlocfilehash: faccb7c040b628899746973bcf4c54bb01b8d555
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98418787"
---
# <span data-ttu-id="2406f-101">New-AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="2406f-101">New-AzStorageContainer</span></span>

## <span data-ttu-id="2406f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2406f-102">SYNOPSIS</span></span>
<span data-ttu-id="2406f-103">Skapar en Azure Storage-behållare.</span><span class="sxs-lookup"><span data-stu-id="2406f-103">Creates an Azure storage container.</span></span>

## <span data-ttu-id="2406f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2406f-104">SYNTAX</span></span>

### <span data-ttu-id="2406f-105">ContainerName (standard)</span><span class="sxs-lookup"><span data-stu-id="2406f-105">ContainerName (Default)</span></span>
```
New-AzStorageContainer [-Name] <String> [[-Permission] <BlobContainerPublicAccessType>]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="2406f-106">EncryptionScope</span><span class="sxs-lookup"><span data-stu-id="2406f-106">EncryptionScope</span></span>
```
New-AzStorageContainer [-Name] <String> [[-Permission] <BlobContainerPublicAccessType>]
 -DefaultEncryptionScope <String> -PreventEncryptionScopeOverride <Boolean> [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="2406f-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2406f-107">DESCRIPTION</span></span>
<span data-ttu-id="2406f-108">Cmdleten **New-AzStorageContainer** skapar en Azure Storage-behållare.</span><span class="sxs-lookup"><span data-stu-id="2406f-108">The **New-AzStorageContainer** cmdlet creates an Azure storage container.</span></span>

## <span data-ttu-id="2406f-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2406f-109">EXAMPLES</span></span>

### <span data-ttu-id="2406f-110">Exempel 1: skapa en Azure Storage-behållare</span><span class="sxs-lookup"><span data-stu-id="2406f-110">Example 1: Create an Azure storage container</span></span>
```
PS C:\>New-AzStorageContainer -Name "ContainerName" -Permission Off
```

<span data-ttu-id="2406f-111">Det här kommandot skapar en lagrings behållare.</span><span class="sxs-lookup"><span data-stu-id="2406f-111">This command creates a storage container.</span></span>

### <span data-ttu-id="2406f-112">Exempel 2: skapa flera Azure Storage-behållare</span><span class="sxs-lookup"><span data-stu-id="2406f-112">Example 2: Create multiple Azure storage containers</span></span>
```
PS C:\>"container1 container2 container3".split() | New-AzStorageContainer -Permission Container
```

<span data-ttu-id="2406f-113">I det här exemplet skapas flera lagrings behållare.</span><span class="sxs-lookup"><span data-stu-id="2406f-113">This example creates multiple storage containers.</span></span>
<span data-ttu-id="2406f-114">Den använder metoden **Split** i **klassen .net och** skickar sedan namnen i pipeline.</span><span class="sxs-lookup"><span data-stu-id="2406f-114">It uses the **Split** method of the .NET **String** class and then passes the names on the pipeline.</span></span>

### <span data-ttu-id="2406f-115">Exempel 3: skapa en Azure-lagringsenhet med krypterings omfång</span><span class="sxs-lookup"><span data-stu-id="2406f-115">Example 3: Create an Azure storage container with Encryption Scope</span></span>
```
PS C:\> $container = New-AzStorageContainer  -Name "mycontainer" -DefaultEncryptionScope "myencryptscope" -PreventEncryptionScopeOverride $true 

PS C:\> $container.BlobContainerProperties.DefaultEncryptionScope
myencryptscope

PS C:\> $container.BlobContainerProperties.PreventEncryptionScopeOverride
True
```

<span data-ttu-id="2406f-116">Det här kommandot skapar en lagrings behållare med standard krypterings omfattning som myencryptscope och förverterad BLOB-uppladdning med olika krypterings omfång till den här behållaren.</span><span class="sxs-lookup"><span data-stu-id="2406f-116">This command creates a storage container, with default Encryption Scope as myencryptscope, and prevert blob upload with different Encryption Scope to this container.</span></span>

## <span data-ttu-id="2406f-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2406f-117">PARAMETERS</span></span>

### <span data-ttu-id="2406f-118">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="2406f-118">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="2406f-119">Anger tids gräns för klient sidan, i sekunder, för en tjänst förfrågan.</span><span class="sxs-lookup"><span data-stu-id="2406f-119">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="2406f-120">Om det föregående samtalet inte fungerar under det angivna intervallet, försöker den här cmdleten igen.</span><span class="sxs-lookup"><span data-stu-id="2406f-120">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="2406f-121">Om denna cmdlet inte får ett lyckat svar innan intervallet går ut returneras ett fel.</span><span class="sxs-lookup"><span data-stu-id="2406f-121">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="2406f-122">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="2406f-122">-ConcurrentTaskCount</span></span>
<span data-ttu-id="2406f-123">Anger maximalt antal samtidiga nätverks samtal.</span><span class="sxs-lookup"><span data-stu-id="2406f-123">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="2406f-124">Du kan använda den här parametern för att begränsa samtidigheten för att reglera den lokala processorn och bandbredds användning genom att ange det maximala antalet simultana nätverks samtal.</span><span class="sxs-lookup"><span data-stu-id="2406f-124">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="2406f-125">Det angivna värdet är ett absolut antal och multipliceras inte med antalet kärnor.</span><span class="sxs-lookup"><span data-stu-id="2406f-125">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="2406f-126">Den här parametern kan hjälpa till att minska nätverks anslutnings problem i miljöer med liten bandbredd, till exempel 100 kilobit per sekund.</span><span class="sxs-lookup"><span data-stu-id="2406f-126">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="2406f-127">Standardvärdet är 10.</span><span class="sxs-lookup"><span data-stu-id="2406f-127">The default value is 10.</span></span>

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

### <span data-ttu-id="2406f-128">-Kontext</span><span class="sxs-lookup"><span data-stu-id="2406f-128">-Context</span></span>
<span data-ttu-id="2406f-129">Anger en kontext för den nya behållaren.</span><span class="sxs-lookup"><span data-stu-id="2406f-129">Specifies a context for the new container.</span></span>

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

### <span data-ttu-id="2406f-130">-DefaultEncryptionScope</span><span class="sxs-lookup"><span data-stu-id="2406f-130">-DefaultEncryptionScope</span></span>
<span data-ttu-id="2406f-131">Använd den angivna krypterings omfattningen för alla skrivningar.</span><span class="sxs-lookup"><span data-stu-id="2406f-131">Default the container to use specified encryption scope for all writes.</span></span>

```yaml
Type: System.String
Parameter Sets: EncryptionScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2406f-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2406f-132">-DefaultProfile</span></span>
<span data-ttu-id="2406f-133">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="2406f-133">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2406f-134">-Namn</span><span class="sxs-lookup"><span data-stu-id="2406f-134">-Name</span></span>
<span data-ttu-id="2406f-135">Anger ett namn för den nya behållaren.</span><span class="sxs-lookup"><span data-stu-id="2406f-135">Specifies a name for the new container.</span></span>

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

### <span data-ttu-id="2406f-136">-Tillstånd</span><span class="sxs-lookup"><span data-stu-id="2406f-136">-Permission</span></span>
<span data-ttu-id="2406f-137">Anger nivån för offentlig åtkomst till den här behållaren.</span><span class="sxs-lookup"><span data-stu-id="2406f-137">Specifies the level of public access to this container.</span></span>
<span data-ttu-id="2406f-138">Som standard kan bara en container och alla BLOB-objekt nås av lagrings kontots ägare.</span><span class="sxs-lookup"><span data-stu-id="2406f-138">By default, the container and any blobs in it can be accessed only by the owner of the storage account.</span></span>
<span data-ttu-id="2406f-139">Om du vill ge anonyma användare Läs behörigheter till en behållare och dess BLOB-objekt kan du ange behållar behörigheter för att aktivera offentlig åtkomst.</span><span class="sxs-lookup"><span data-stu-id="2406f-139">To grant anonymous users read permissions to a container and its blobs, you can set the container permissions to enable public access.</span></span>
<span data-ttu-id="2406f-140">Anonyma användare kan läsa BLOB i en offentligt tillgänglig container utan att autentisera begäran.</span><span class="sxs-lookup"><span data-stu-id="2406f-140">Anonymous users can read blobs in a publicly available container without authenticating the request.</span></span>
<span data-ttu-id="2406f-141">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="2406f-141">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="2406f-142">Beh.</span><span class="sxs-lookup"><span data-stu-id="2406f-142">Container.</span></span>
<span data-ttu-id="2406f-143">Ger fullständig Läs åtkomst till en behållare och dess blob.</span><span class="sxs-lookup"><span data-stu-id="2406f-143">Provides full read access to a container and its blobs.</span></span>
<span data-ttu-id="2406f-144">Klienter kan räkna upp blobs i behållaren via anonym begäran men kan inte räkna upp behållare i lagrings kontot.</span><span class="sxs-lookup"><span data-stu-id="2406f-144">Clients can enumerate blobs in the container through anonymous request, but cannot enumerate containers in the storage account.</span></span> 
- <span data-ttu-id="2406f-145">Object.</span><span class="sxs-lookup"><span data-stu-id="2406f-145">Blob.</span></span>
<span data-ttu-id="2406f-146">Ger Läs åtkomst till BLOB-data över hela en behållare via anonym begäran, men ger inte åtkomst till behållar data.</span><span class="sxs-lookup"><span data-stu-id="2406f-146">Provides read access to blob data throughout a container through anonymous request, but does not provide access to container data.</span></span>
<span data-ttu-id="2406f-147">Klienter kan inte räkna upp blobbar i behållaren med anonym begäran.</span><span class="sxs-lookup"><span data-stu-id="2406f-147">Clients cannot enumerate blobs in the container by using anonymous request.</span></span> 
- <span data-ttu-id="2406f-148">Ras.</span><span class="sxs-lookup"><span data-stu-id="2406f-148">Off.</span></span>
<span data-ttu-id="2406f-149">Vilka begränsar åtkomsten till lagrings kontots ägare.</span><span class="sxs-lookup"><span data-stu-id="2406f-149">Which restricts access to only the storage account owner.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Storage.Blob.BlobContainerPublicAccessType]
Parameter Sets: (All)
Aliases: PublicAccess
Accepted values: Off, Container, Blob, Unknown

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2406f-150">-PreventEncryptionScopeOverride</span><span class="sxs-lookup"><span data-stu-id="2406f-150">-PreventEncryptionScopeOverride</span></span>
<span data-ttu-id="2406f-151">Blockera åsidosättning av krypterings omfång från standard behållare.</span><span class="sxs-lookup"><span data-stu-id="2406f-151">Block override of encryption scope from the container default.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: EncryptionScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2406f-152">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="2406f-152">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="2406f-153">Anger timeout-intervall för tjänsten i sekunder för en begäran.</span><span class="sxs-lookup"><span data-stu-id="2406f-153">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="2406f-154">Om det angivna intervallet förflyter innan tjänsten bearbetar begäran returnerar lagrings tjänsten ett fel.</span><span class="sxs-lookup"><span data-stu-id="2406f-154">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="2406f-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2406f-155">CommonParameters</span></span>
<span data-ttu-id="2406f-156">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2406f-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2406f-157">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2406f-157">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2406f-158">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2406f-158">INPUTS</span></span>

### <span data-ttu-id="2406f-159">System. String</span><span class="sxs-lookup"><span data-stu-id="2406f-159">System.String</span></span>

### <span data-ttu-id="2406f-160">Microsoft. Azure. commands. Common. verifikation. abstraktioner. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="2406f-160">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="2406f-161">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2406f-161">OUTPUTS</span></span>

### <span data-ttu-id="2406f-162">Microsoft. WindowsAzure. commands. Common. Storage. ResourceModel. AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="2406f-162">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageContainer</span></span>

## <span data-ttu-id="2406f-163">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2406f-163">NOTES</span></span>

## <span data-ttu-id="2406f-164">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2406f-164">RELATED LINKS</span></span>

[<span data-ttu-id="2406f-165">Get-AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="2406f-165">Get-AzStorageContainer</span></span>](./Get-AzStorageContainer.md)

[<span data-ttu-id="2406f-166">Remove-AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="2406f-166">Remove-AzStorageContainer</span></span>](./Remove-AzStorageContainer.md)

[<span data-ttu-id="2406f-167">Set-AzStorageContainerAcl</span><span class="sxs-lookup"><span data-stu-id="2406f-167">Set-AzStorageContainerAcl</span></span>](./Set-AzStorageContainerAcl.md)


