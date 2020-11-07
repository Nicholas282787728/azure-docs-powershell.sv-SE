---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: BDEEF1EA-A785-4E17-9887-C2000BDFCF57
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azstoragecontaineracl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageContainerAcl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageContainerAcl.md
ms.openlocfilehash: 2ed750f2206389a4951efacb153c287e9e80ac8a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93743572"
---
# <span data-ttu-id="3fea4-101">Set-AzStorageContainerAcl</span><span class="sxs-lookup"><span data-stu-id="3fea4-101">Set-AzStorageContainerAcl</span></span>

## <span data-ttu-id="3fea4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3fea4-102">SYNOPSIS</span></span>
<span data-ttu-id="3fea4-103">Ställer in offentlig åtkomst till en lagrings behållare.</span><span class="sxs-lookup"><span data-stu-id="3fea4-103">Sets the public access permission to a storage container.</span></span>

## <span data-ttu-id="3fea4-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3fea4-104">SYNTAX</span></span>

```
Set-AzStorageContainerAcl [-Name] <String> [-Permission] <BlobContainerPublicAccessType> [-PassThru]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="3fea4-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3fea4-105">DESCRIPTION</span></span>
<span data-ttu-id="3fea4-106">Cmdleten **set-AzStorageContainerAcl** anger offentlig åtkomst behörighet för den angivna lagrings behållaren i Azure.</span><span class="sxs-lookup"><span data-stu-id="3fea4-106">The **Set-AzStorageContainerAcl** cmdlet sets the public access permission to the specified storage container in Azure.</span></span>

## <span data-ttu-id="3fea4-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3fea4-107">EXAMPLES</span></span>

### <span data-ttu-id="3fea4-108">Exempel 1: ange ACL för Azure Storage-behållare med namn</span><span class="sxs-lookup"><span data-stu-id="3fea4-108">Example 1: Set azure storage container ACL by name</span></span>
```
PS C:\>Set-AzStorageContainerAcl -Container "Container01" -Permission Off -PassThru
```

<span data-ttu-id="3fea4-109">Det här kommandot skapar en behållare som inte har offentlig åtkomst.</span><span class="sxs-lookup"><span data-stu-id="3fea4-109">This command creates a container that has no public access.</span></span>

### <span data-ttu-id="3fea4-110">Exempel 2: ange ACL för Azure Storage-behållare genom att använda pipeline</span><span class="sxs-lookup"><span data-stu-id="3fea4-110">Example 2: Set azure storage container ACL by using the pipeline</span></span>
```
PS C:\>Get-AzStorageContainer container* | Set-AzStorageContainerAcl -Permission Blob -PassThru
```

<span data-ttu-id="3fea4-111">Det här kommandot får alla lagrings behållare vars namn börjar med en container och skickar sedan resultatet i pipeline för att ställa in behörigheten för alla till BLOB-åtkomst.</span><span class="sxs-lookup"><span data-stu-id="3fea4-111">This command gets all storage containers whose name starts with container and then passes the result on the pipeline to set the permission for them all to Blob access.</span></span>

## <span data-ttu-id="3fea4-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3fea4-112">PARAMETERS</span></span>

### <span data-ttu-id="3fea4-113">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="3fea4-113">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="3fea4-114">Anger tids gräns för klient sidan, i sekunder, för en tjänst förfrågan.</span><span class="sxs-lookup"><span data-stu-id="3fea4-114">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="3fea4-115">Om det föregående samtalet inte fungerar under det angivna intervallet, försöker den här cmdleten igen.</span><span class="sxs-lookup"><span data-stu-id="3fea4-115">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="3fea4-116">Om denna cmdlet inte får ett lyckat svar innan intervallet går ut returneras ett fel.</span><span class="sxs-lookup"><span data-stu-id="3fea4-116">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="3fea4-117">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="3fea4-117">-ConcurrentTaskCount</span></span>
<span data-ttu-id="3fea4-118">Anger maximalt antal samtidiga nätverks samtal.</span><span class="sxs-lookup"><span data-stu-id="3fea4-118">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="3fea4-119">Du kan använda den här parametern för att begränsa samtidigheten för att reglera den lokala processorn och bandbredds användning genom att ange det maximala antalet simultana nätverks samtal.</span><span class="sxs-lookup"><span data-stu-id="3fea4-119">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="3fea4-120">Det angivna värdet är ett absolut antal och multipliceras inte med antalet kärnor.</span><span class="sxs-lookup"><span data-stu-id="3fea4-120">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="3fea4-121">Den här parametern kan hjälpa till att minska nätverks anslutnings problem i miljöer med liten bandbredd, till exempel 100 kilobit per sekund.</span><span class="sxs-lookup"><span data-stu-id="3fea4-121">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="3fea4-122">Standardvärdet är 10.</span><span class="sxs-lookup"><span data-stu-id="3fea4-122">The default value is 10.</span></span>

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

### <span data-ttu-id="3fea4-123">-Kontext</span><span class="sxs-lookup"><span data-stu-id="3fea4-123">-Context</span></span>
<span data-ttu-id="3fea4-124">Anger Azure Storage-kontexten.</span><span class="sxs-lookup"><span data-stu-id="3fea4-124">Specifies the Azure storage context.</span></span>
<span data-ttu-id="3fea4-125">Du kan skapa det med hjälp av New-AzStorageContext cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3fea4-125">You can create it by using the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="3fea4-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3fea4-126">-DefaultProfile</span></span>
<span data-ttu-id="3fea4-127">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="3fea4-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3fea4-128">-Namn</span><span class="sxs-lookup"><span data-stu-id="3fea4-128">-Name</span></span>
<span data-ttu-id="3fea4-129">Anger ett namn på en behållare.</span><span class="sxs-lookup"><span data-stu-id="3fea4-129">Specifies a container name.</span></span>

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

### <span data-ttu-id="3fea4-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3fea4-130">-PassThru</span></span>
<span data-ttu-id="3fea4-131">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="3fea4-131">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="3fea4-132">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="3fea4-132">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3fea4-133">-Tillstånd</span><span class="sxs-lookup"><span data-stu-id="3fea4-133">-Permission</span></span>
<span data-ttu-id="3fea4-134">Anger nivån för offentlig åtkomst till den här behållaren.</span><span class="sxs-lookup"><span data-stu-id="3fea4-134">Specifies the level of public access to this container.</span></span>
<span data-ttu-id="3fea4-135">Som standard kan bara en container och alla BLOB-objekt nås av lagrings kontots ägare.</span><span class="sxs-lookup"><span data-stu-id="3fea4-135">By default, the container and any blobs in it can be accessed only by the owner of the storage account.</span></span>
<span data-ttu-id="3fea4-136">Om du vill ge anonyma användare Läs behörigheter till en behållare och dess BLOB-objekt kan du ange behållar behörigheter för att aktivera offentlig åtkomst.</span><span class="sxs-lookup"><span data-stu-id="3fea4-136">To grant anonymous users read permissions to a container and its blobs, you can set the container permissions to enable public access.</span></span>
<span data-ttu-id="3fea4-137">Anonyma användare kan läsa BLOB i en offentligt tillgänglig container utan att autentisera begäran.</span><span class="sxs-lookup"><span data-stu-id="3fea4-137">Anonymous users can read blobs in a publicly available container without authenticating the request.</span></span>
<span data-ttu-id="3fea4-138">De godkända värdena för den här parametern är:--container.</span><span class="sxs-lookup"><span data-stu-id="3fea4-138">The acceptable values for this parameter are: --Container.</span></span>
<span data-ttu-id="3fea4-139">Ger fullständig Läs åtkomst till en behållare och dess blob.</span><span class="sxs-lookup"><span data-stu-id="3fea4-139">Provides full read access to a container and its blobs.</span></span>
<span data-ttu-id="3fea4-140">Klienter kan räkna upp blobs i behållaren via anonym begäran men kan inte räkna upp behållare i lagrings kontot.</span><span class="sxs-lookup"><span data-stu-id="3fea4-140">Clients can enumerate blobs in the container through anonymous request, but cannot enumerate containers in the storage account.</span></span> <span data-ttu-id="3fea4-141">--Blob.</span><span class="sxs-lookup"><span data-stu-id="3fea4-141">--Blob.</span></span>
<span data-ttu-id="3fea4-142">Ger Läs åtkomst till BLOB-data i en behållare via anonym begäran, men ger inte åtkomst till behållar data.</span><span class="sxs-lookup"><span data-stu-id="3fea4-142">Provides read access to blob data in a container through anonymous request, but does not provide access to container data.</span></span>
<span data-ttu-id="3fea4-143">Klienter kan inte räkna upp blobbar i behållaren med anonym begäran.</span><span class="sxs-lookup"><span data-stu-id="3fea4-143">Clients cannot enumerate blobs in the container by using anonymous request.</span></span> <span data-ttu-id="3fea4-144">-Av.</span><span class="sxs-lookup"><span data-stu-id="3fea4-144">--Off.</span></span>
<span data-ttu-id="3fea4-145">Begränsar åtkomst till lagrings kontots ägare.</span><span class="sxs-lookup"><span data-stu-id="3fea4-145">Restricts access to only the storage account owner.</span></span>

```yaml
Type: Microsoft.Azure.Storage.Blob.BlobContainerPublicAccessType
Parameter Sets: (All)
Aliases: PublicAccess
Accepted values: Off, Container, Blob, Unknown

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3fea4-146">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="3fea4-146">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="3fea4-147">Anger timeout-intervall för tjänsten i sekunder för en begäran.</span><span class="sxs-lookup"><span data-stu-id="3fea4-147">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="3fea4-148">Om det angivna intervallet förflyter innan tjänsten bearbetar begäran returnerar lagrings tjänsten ett fel.</span><span class="sxs-lookup"><span data-stu-id="3fea4-148">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>
<span data-ttu-id="3fea4-149">Timeout för servern för varje begäran.</span><span class="sxs-lookup"><span data-stu-id="3fea4-149">Server side time out for each request.</span></span>

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

### <span data-ttu-id="3fea4-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3fea4-150">CommonParameters</span></span>
<span data-ttu-id="3fea4-151">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3fea4-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3fea4-152">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3fea4-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3fea4-153">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3fea4-153">INPUTS</span></span>

### <span data-ttu-id="3fea4-154">System. String</span><span class="sxs-lookup"><span data-stu-id="3fea4-154">System.String</span></span>

### <span data-ttu-id="3fea4-155">Microsoft. Azure. commands. Common. verifikation. abstraktioner. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="3fea4-155">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="3fea4-156">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3fea4-156">OUTPUTS</span></span>

### <span data-ttu-id="3fea4-157">Microsoft. WindowsAzure. commands. Common. Storage. ResourceModel. AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="3fea4-157">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageContainer</span></span>

## <span data-ttu-id="3fea4-158">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3fea4-158">NOTES</span></span>

## <span data-ttu-id="3fea4-159">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3fea4-159">RELATED LINKS</span></span>

[<span data-ttu-id="3fea4-160">Get-AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="3fea4-160">Get-AzStorageContainer</span></span>](./Get-AzStorageContainer.md)

[<span data-ttu-id="3fea4-161">New-AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="3fea4-161">New-AzStorageContainer</span></span>](./New-AzStorageContainer.md)

[<span data-ttu-id="3fea4-162">Remove-AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="3fea4-162">Remove-AzStorageContainer</span></span>](./Remove-AzStorageContainer.md)

