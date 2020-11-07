---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 585371E3-D4CE-452E-B0B0-92B3ABD127E7
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/new-azurestorageblobsastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageBlobSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageBlobSASToken.md
ms.openlocfilehash: d75111b27b03317f757cbf0def4d9d66c43427c3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756535"
---
# <span data-ttu-id="15e54-101">New-AzureStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="15e54-101">New-AzureStorageBlobSASToken</span></span>

## <span data-ttu-id="15e54-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="15e54-102">SYNOPSIS</span></span>
<span data-ttu-id="15e54-103">Skapar en SAS-token för en Azure Storage blob.</span><span class="sxs-lookup"><span data-stu-id="15e54-103">Generates a SAS token for an Azure storage blob.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="15e54-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="15e54-104">SYNTAX</span></span>

### <span data-ttu-id="15e54-105">BlobNameWithPermission (standard)</span><span class="sxs-lookup"><span data-stu-id="15e54-105">BlobNameWithPermission (Default)</span></span>
```
New-AzureStorageBlobSASToken [-Container] <String> [-Blob] <String> [-Permission <String>]
 [-Protocol <SharedAccessProtocol>] [-IPAddressOrRange <String>] [-StartTime <DateTime>]
 [-ExpiryTime <DateTime>] [-FullUri] [-Context <IStorageContext>] [<CommonParameters>]
```

### <span data-ttu-id="15e54-106">BlobPipelineWithPolicy</span><span class="sxs-lookup"><span data-stu-id="15e54-106">BlobPipelineWithPolicy</span></span>
```
New-AzureStorageBlobSASToken -CloudBlob <CloudBlob> -Policy <String> [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [<CommonParameters>]
```

### <span data-ttu-id="15e54-107">BlobPipelineWithPermission</span><span class="sxs-lookup"><span data-stu-id="15e54-107">BlobPipelineWithPermission</span></span>
```
New-AzureStorageBlobSASToken -CloudBlob <CloudBlob> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [<CommonParameters>]
```

### <span data-ttu-id="15e54-108">BlobNameWithPolicy</span><span class="sxs-lookup"><span data-stu-id="15e54-108">BlobNameWithPolicy</span></span>
```
New-AzureStorageBlobSASToken [-Container] <String> [-Blob] <String> -Policy <String>
 [-Protocol <SharedAccessProtocol>] [-IPAddressOrRange <String>] [-StartTime <DateTime>]
 [-ExpiryTime <DateTime>] [-FullUri] [-Context <IStorageContext>] [<CommonParameters>]
```

## <span data-ttu-id="15e54-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="15e54-109">DESCRIPTION</span></span>
<span data-ttu-id="15e54-110">**New-AzureStorageBlobSASToken-** cmdleten genererar en SAS-token (Shared Access signatur) för en Azure Storage blob.</span><span class="sxs-lookup"><span data-stu-id="15e54-110">The **New-AzureStorageBlobSASToken** cmdlet generates a Shared Access Signature (SAS) token for an Azure storage blob.</span></span>

## <span data-ttu-id="15e54-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="15e54-111">EXAMPLES</span></span>

### <span data-ttu-id="15e54-112">Exempel 1: generera en BLOB SAS-token med fullständig BLOB-behörighet</span><span class="sxs-lookup"><span data-stu-id="15e54-112">Example 1: Generate a blob SAS token with full blob permission</span></span>
```
PS C:\>New-AzureStorageBlobSASToken -Container "ContainerName" -Blob "BlobName" -Permission rwd
```

<span data-ttu-id="15e54-113">I det här exemplet skapas en BLOB SAS-token med full BLOB-behörighet.</span><span class="sxs-lookup"><span data-stu-id="15e54-113">This example generates a blob SAS token with full blob permission.</span></span>

### <span data-ttu-id="15e54-114">Exempel 2: generera en BLOB SAS-token med livs längd</span><span class="sxs-lookup"><span data-stu-id="15e54-114">Example 2: Generate a blob SAS token with life time</span></span>
```
PS C:\> $StartTime = Get-Date
PS C:\> $EndTime = $startTime.AddHours(2.0)
PS C:\> New-AzureStorageBlobSASToken -Container "ContainerName" -Blob "BlobName" -Permission rwd -StartTime $StartTime -ExpiryTime $EndTime
```

<span data-ttu-id="15e54-115">I det här exemplet skapas en BLOB SAS-token med livs längd.</span><span class="sxs-lookup"><span data-stu-id="15e54-115">This example generates a blob SAS token with life time.</span></span>

## <span data-ttu-id="15e54-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="15e54-116">PARAMETERS</span></span>

### <span data-ttu-id="15e54-117">-BLOB</span><span class="sxs-lookup"><span data-stu-id="15e54-117">-Blob</span></span>
<span data-ttu-id="15e54-118">Anger lagringsreplik-namnet.</span><span class="sxs-lookup"><span data-stu-id="15e54-118">Specifies the storage blob name.</span></span>

```yaml
Type: String
Parameter Sets: BlobNameWithPermission, BlobNameWithPolicy
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15e54-119">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="15e54-119">-CloudBlob</span></span>
<span data-ttu-id="15e54-120">Anger **CloudBlob** -objektet.</span><span class="sxs-lookup"><span data-stu-id="15e54-120">Specifies the **CloudBlob** object.</span></span>
<span data-ttu-id="15e54-121">Om du vill hämta ett **CloudBlob** -objekt använder du cmdleten [Get-AzureStorageBlob](./Get-AzureStorageBlob.md) .</span><span class="sxs-lookup"><span data-stu-id="15e54-121">To obtain a **CloudBlob** object, use the [Get-AzureStorageBlob](./Get-AzureStorageBlob.md) cmdlet.</span></span>

```yaml
Type: CloudBlob
Parameter Sets: BlobPipelineWithPolicy, BlobPipelineWithPermission
Aliases: ICloudBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15e54-122">-Container</span><span class="sxs-lookup"><span data-stu-id="15e54-122">-Container</span></span>
<span data-ttu-id="15e54-123">Anger namnet på lagrings behållaren.</span><span class="sxs-lookup"><span data-stu-id="15e54-123">Specifies the storage container name.</span></span>

```yaml
Type: String
Parameter Sets: BlobNameWithPermission, BlobNameWithPolicy
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15e54-124">-Kontext</span><span class="sxs-lookup"><span data-stu-id="15e54-124">-Context</span></span>
<span data-ttu-id="15e54-125">Anger lagrings kontexten.</span><span class="sxs-lookup"><span data-stu-id="15e54-125">Specifies the storage context.</span></span>

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

### <span data-ttu-id="15e54-126">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="15e54-126">-ExpiryTime</span></span>
<span data-ttu-id="15e54-127">Anger när signaturen för delad åtkomst upphör.</span><span class="sxs-lookup"><span data-stu-id="15e54-127">Specifies when the shared access signature expires.</span></span>

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

### <span data-ttu-id="15e54-128">-FullUri</span><span class="sxs-lookup"><span data-stu-id="15e54-128">-FullUri</span></span>
<span data-ttu-id="15e54-129">Anger att denna cmdlet returnerar full BLOB URI och signatur för delad åtkomst.</span><span class="sxs-lookup"><span data-stu-id="15e54-129">Indicates that this cmdlet return the full blob URI and the shared access signature token.</span></span>

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

### <span data-ttu-id="15e54-130">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="15e54-130">-IPAddressOrRange</span></span>
<span data-ttu-id="15e54-131">Anger IP-adressen eller intervallet med IP-adresser som begär Anden ska accepteras från, till exempel 168.1.5.65 eller 168.1.5.60-168.1.5.70.</span><span class="sxs-lookup"><span data-stu-id="15e54-131">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="15e54-132">Intervallet är inkluderat.</span><span class="sxs-lookup"><span data-stu-id="15e54-132">The range is inclusive.</span></span>

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

### <span data-ttu-id="15e54-133">-Tillstånd</span><span class="sxs-lookup"><span data-stu-id="15e54-133">-Permission</span></span>
<span data-ttu-id="15e54-134">Anger behörigheterna för en lagrings-blob.</span><span class="sxs-lookup"><span data-stu-id="15e54-134">Specifies the permissions for a storage blob.</span></span>

```yaml
Type: String
Parameter Sets: BlobNameWithPermission, BlobPipelineWithPermission
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15e54-135">-Princip</span><span class="sxs-lookup"><span data-stu-id="15e54-135">-Policy</span></span>
<span data-ttu-id="15e54-136">Anger en åtkomst policy för Azure.</span><span class="sxs-lookup"><span data-stu-id="15e54-136">Specifies an Azure Stored Access Policy.</span></span>

```yaml
Type: String
Parameter Sets: BlobPipelineWithPolicy, BlobNameWithPolicy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15e54-137">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="15e54-137">-Protocol</span></span>
<span data-ttu-id="15e54-138">Anger det protokoll som tillåts för en begäran.</span><span class="sxs-lookup"><span data-stu-id="15e54-138">Specifies the protocol permitted for a request.</span></span>
<span data-ttu-id="15e54-139">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="15e54-139">The acceptable values for this parameter are:</span></span>
* <span data-ttu-id="15e54-140">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="15e54-140">HttpsOnly</span></span>
* <span data-ttu-id="15e54-141">HttpsOrHttp</span><span class="sxs-lookup"><span data-stu-id="15e54-141">HttpsOrHttp</span></span>

<span data-ttu-id="15e54-142">Standardvärdet är HttpsOrHttp.</span><span class="sxs-lookup"><span data-stu-id="15e54-142">The default value is HttpsOrHttp.</span></span>

```yaml
Type: SharedAccessProtocol
Parameter Sets: (All)
Aliases: 
Accepted values: HttpsOnly, HttpsOrHttp

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15e54-143">-StartTime</span><span class="sxs-lookup"><span data-stu-id="15e54-143">-StartTime</span></span>
<span data-ttu-id="15e54-144">Anger den tid då den delade Access-signaturen blir giltig.</span><span class="sxs-lookup"><span data-stu-id="15e54-144">Specifies the time at which the shared access signature becomes valid.</span></span>

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

### <span data-ttu-id="15e54-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15e54-145">CommonParameters</span></span>
<span data-ttu-id="15e54-146">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="15e54-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15e54-147">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="15e54-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15e54-148">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="15e54-148">INPUTS</span></span>

### <span data-ttu-id="15e54-149">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="15e54-149">IStorageContext</span></span>

<span data-ttu-id="15e54-150">Parametern ' context ' godkänner värdet av typen ' IStorageContext ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="15e54-150">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

## <span data-ttu-id="15e54-151">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="15e54-151">OUTPUTS</span></span>

### <span data-ttu-id="15e54-152">System. String</span><span class="sxs-lookup"><span data-stu-id="15e54-152">System.String</span></span>

## <span data-ttu-id="15e54-153">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="15e54-153">NOTES</span></span>

## <span data-ttu-id="15e54-154">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="15e54-154">RELATED LINKS</span></span>

[<span data-ttu-id="15e54-155">Get-AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="15e54-155">Get-AzureStorageBlob</span></span>](./Get-AzureStorageBlob.md)

[<span data-ttu-id="15e54-156">New-AzureStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="15e54-156">New-AzureStorageContainerSASToken</span></span>](./New-AzureStorageContainerSASToken.md)
