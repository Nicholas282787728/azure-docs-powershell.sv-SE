---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: 585371E3-D4CE-452E-B0B0-92B3ABD127E7
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/new-azurestorageblobsastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageBlobSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageBlobSASToken.md
ms.openlocfilehash: 60c93d851e173dd8ee8a5f33ff96bb4e2e12299b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93579220"
---
# <span data-ttu-id="806bf-101">New-AzureStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="806bf-101">New-AzureStorageBlobSASToken</span></span>

## <span data-ttu-id="806bf-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="806bf-102">SYNOPSIS</span></span>
<span data-ttu-id="806bf-103">Skapar en SAS-token för en Azure Storage blob.</span><span class="sxs-lookup"><span data-stu-id="806bf-103">Generates a SAS token for an Azure storage blob.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="806bf-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="806bf-104">SYNTAX</span></span>

### <span data-ttu-id="806bf-105">BlobNameWithPermission (standard)</span><span class="sxs-lookup"><span data-stu-id="806bf-105">BlobNameWithPermission (Default)</span></span>
```
New-AzureStorageBlobSASToken [-Container] <String> [-Blob] <String> [-Permission <String>]
 [-Protocol <SharedAccessProtocol>] [-IPAddressOrRange <String>] [-StartTime <DateTime>]
 [-ExpiryTime <DateTime>] [-FullUri] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="806bf-106">BlobPipelineWithPolicy</span><span class="sxs-lookup"><span data-stu-id="806bf-106">BlobPipelineWithPolicy</span></span>
```
New-AzureStorageBlobSASToken -CloudBlob <CloudBlob> -Policy <String> [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="806bf-107">BlobPipelineWithPermission</span><span class="sxs-lookup"><span data-stu-id="806bf-107">BlobPipelineWithPermission</span></span>
```
New-AzureStorageBlobSASToken -CloudBlob <CloudBlob> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="806bf-108">BlobNameWithPolicy</span><span class="sxs-lookup"><span data-stu-id="806bf-108">BlobNameWithPolicy</span></span>
```
New-AzureStorageBlobSASToken [-Container] <String> [-Blob] <String> -Policy <String>
 [-Protocol <SharedAccessProtocol>] [-IPAddressOrRange <String>] [-StartTime <DateTime>]
 [-ExpiryTime <DateTime>] [-FullUri] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="806bf-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="806bf-109">DESCRIPTION</span></span>
<span data-ttu-id="806bf-110">**New-AzureStorageBlobSASToken-** cmdleten genererar en SAS-token (Shared Access signatur) för en Azure Storage blob.</span><span class="sxs-lookup"><span data-stu-id="806bf-110">The **New-AzureStorageBlobSASToken** cmdlet generates a Shared Access Signature (SAS) token for an Azure storage blob.</span></span>

## <span data-ttu-id="806bf-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="806bf-111">EXAMPLES</span></span>

### <span data-ttu-id="806bf-112">Exempel 1: generera en BLOB SAS-token med fullständig BLOB-behörighet</span><span class="sxs-lookup"><span data-stu-id="806bf-112">Example 1: Generate a blob SAS token with full blob permission</span></span>
```
PS C:\>New-AzureStorageBlobSASToken -Container "ContainerName" -Blob "BlobName" -Permission rwd
```

<span data-ttu-id="806bf-113">I det här exemplet skapas en BLOB SAS-token med full BLOB-behörighet.</span><span class="sxs-lookup"><span data-stu-id="806bf-113">This example generates a blob SAS token with full blob permission.</span></span>

### <span data-ttu-id="806bf-114">Exempel 2: generera en BLOB SAS-token med livs längd</span><span class="sxs-lookup"><span data-stu-id="806bf-114">Example 2: Generate a blob SAS token with life time</span></span>
```
PS C:\> $StartTime = Get-Date
PS C:\> $EndTime = $startTime.AddHours(2.0)
PS C:\> New-AzureStorageBlobSASToken -Container "ContainerName" -Blob "BlobName" -Permission rwd -StartTime $StartTime -ExpiryTime $EndTime
```

<span data-ttu-id="806bf-115">I det här exemplet skapas en BLOB SAS-token med livs längd.</span><span class="sxs-lookup"><span data-stu-id="806bf-115">This example generates a blob SAS token with life time.</span></span>

## <span data-ttu-id="806bf-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="806bf-116">PARAMETERS</span></span>

### <span data-ttu-id="806bf-117">-BLOB</span><span class="sxs-lookup"><span data-stu-id="806bf-117">-Blob</span></span>
<span data-ttu-id="806bf-118">Anger lagringsreplik-namnet.</span><span class="sxs-lookup"><span data-stu-id="806bf-118">Specifies the storage blob name.</span></span>

```yaml
Type: System.String
Parameter Sets: BlobNameWithPermission, BlobNameWithPolicy
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="806bf-119">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="806bf-119">-CloudBlob</span></span>
<span data-ttu-id="806bf-120">Anger **CloudBlob** -objektet.</span><span class="sxs-lookup"><span data-stu-id="806bf-120">Specifies the **CloudBlob** object.</span></span>
<span data-ttu-id="806bf-121">Om du vill hämta ett **CloudBlob** -objekt använder du cmdleten [Get-AzureStorageBlob](./Get-AzureStorageBlob.md) .</span><span class="sxs-lookup"><span data-stu-id="806bf-121">To obtain a **CloudBlob** object, use the [Get-AzureStorageBlob](./Get-AzureStorageBlob.md) cmdlet.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.Blob.CloudBlob
Parameter Sets: BlobPipelineWithPolicy, BlobPipelineWithPermission
Aliases: ICloudBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="806bf-122">-Container</span><span class="sxs-lookup"><span data-stu-id="806bf-122">-Container</span></span>
<span data-ttu-id="806bf-123">Anger namnet på lagrings behållaren.</span><span class="sxs-lookup"><span data-stu-id="806bf-123">Specifies the storage container name.</span></span>

```yaml
Type: System.String
Parameter Sets: BlobNameWithPermission, BlobNameWithPolicy
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="806bf-124">-Kontext</span><span class="sxs-lookup"><span data-stu-id="806bf-124">-Context</span></span>
<span data-ttu-id="806bf-125">Anger lagrings kontexten.</span><span class="sxs-lookup"><span data-stu-id="806bf-125">Specifies the storage context.</span></span>

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

### <span data-ttu-id="806bf-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="806bf-126">-DefaultProfile</span></span>
<span data-ttu-id="806bf-127">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="806bf-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="806bf-128">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="806bf-128">-ExpiryTime</span></span>
<span data-ttu-id="806bf-129">Anger när signaturen för delad åtkomst upphör.</span><span class="sxs-lookup"><span data-stu-id="806bf-129">Specifies when the shared access signature expires.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="806bf-130">-FullUri</span><span class="sxs-lookup"><span data-stu-id="806bf-130">-FullUri</span></span>
<span data-ttu-id="806bf-131">Anger att denna cmdlet returnerar full BLOB URI och signatur för delad åtkomst.</span><span class="sxs-lookup"><span data-stu-id="806bf-131">Indicates that this cmdlet return the full blob URI and the shared access signature token.</span></span>

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

### <span data-ttu-id="806bf-132">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="806bf-132">-IPAddressOrRange</span></span>
<span data-ttu-id="806bf-133">Anger IP-adressen eller intervallet med IP-adresser som begär Anden ska accepteras från, till exempel 168.1.5.65 eller 168.1.5.60-168.1.5.70.</span><span class="sxs-lookup"><span data-stu-id="806bf-133">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="806bf-134">Intervallet är inkluderat.</span><span class="sxs-lookup"><span data-stu-id="806bf-134">The range is inclusive.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="806bf-135">-Tillstånd</span><span class="sxs-lookup"><span data-stu-id="806bf-135">-Permission</span></span>
<span data-ttu-id="806bf-136">Anger behörigheterna för en lagrings-blob.</span><span class="sxs-lookup"><span data-stu-id="806bf-136">Specifies the permissions for a storage blob.</span></span> <span data-ttu-id="806bf-137">Det är viktigt att Observera att det här är en sträng, till exempel `rwd` (för läsning, skrivning och borttagning).</span><span class="sxs-lookup"><span data-stu-id="806bf-137">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span> 

```yaml
Type: System.String
Parameter Sets: BlobNameWithPermission, BlobPipelineWithPermission
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="806bf-138">-Princip</span><span class="sxs-lookup"><span data-stu-id="806bf-138">-Policy</span></span>
<span data-ttu-id="806bf-139">Anger en åtkomst policy för Azure.</span><span class="sxs-lookup"><span data-stu-id="806bf-139">Specifies an Azure Stored Access Policy.</span></span>

```yaml
Type: System.String
Parameter Sets: BlobPipelineWithPolicy, BlobNameWithPolicy
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="806bf-140">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="806bf-140">-Protocol</span></span>
<span data-ttu-id="806bf-141">Anger det protokoll som tillåts för en begäran.</span><span class="sxs-lookup"><span data-stu-id="806bf-141">Specifies the protocol permitted for a request.</span></span>
<span data-ttu-id="806bf-142">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="806bf-142">The acceptable values for this parameter are:</span></span>
* <span data-ttu-id="806bf-143">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="806bf-143">HttpsOnly</span></span>
* <span data-ttu-id="806bf-144">HttpsOrHttp standardvärdet är HttpsOrHttp.</span><span class="sxs-lookup"><span data-stu-id="806bf-144">HttpsOrHttp The default value is HttpsOrHttp.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.WindowsAzure.Storage.SharedAccessProtocol]
Parameter Sets: (All)
Aliases:
Accepted values: HttpsOnly, HttpsOrHttp

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="806bf-145">-StartTime</span><span class="sxs-lookup"><span data-stu-id="806bf-145">-StartTime</span></span>
<span data-ttu-id="806bf-146">Anger den tid då den delade Access-signaturen blir giltig.</span><span class="sxs-lookup"><span data-stu-id="806bf-146">Specifies the time at which the shared access signature becomes valid.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="806bf-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="806bf-147">CommonParameters</span></span>
<span data-ttu-id="806bf-148">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="806bf-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="806bf-149">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="806bf-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="806bf-150">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="806bf-150">INPUTS</span></span>

### <span data-ttu-id="806bf-151">Microsoft. WindowsAzure. Storage. blob. CloudBlob</span><span class="sxs-lookup"><span data-stu-id="806bf-151">Microsoft.WindowsAzure.Storage.Blob.CloudBlob</span></span>

### <span data-ttu-id="806bf-152">Microsoft. Azure. commands. Common. verifikation. abstraktioner. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="806bf-152">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="806bf-153">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="806bf-153">OUTPUTS</span></span>

### <span data-ttu-id="806bf-154">System. String</span><span class="sxs-lookup"><span data-stu-id="806bf-154">System.String</span></span>

## <span data-ttu-id="806bf-155">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="806bf-155">NOTES</span></span>

## <span data-ttu-id="806bf-156">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="806bf-156">RELATED LINKS</span></span>

[<span data-ttu-id="806bf-157">Get-AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="806bf-157">Get-AzureStorageBlob</span></span>](./Get-AzureStorageBlob.md)

[<span data-ttu-id="806bf-158">New-AzureStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="806bf-158">New-AzureStorageContainerSASToken</span></span>](./New-AzureStorageContainerSASToken.md)
