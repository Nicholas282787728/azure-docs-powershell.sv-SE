---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 585371E3-D4CE-452E-B0B0-92B3ABD127E7
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstorageblobsastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageBlobSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageBlobSASToken.md
ms.openlocfilehash: ff97ccbe74d7f9a0005d2ad4d8b2cd44ad0da7e5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93920937"
---
# <span data-ttu-id="2e6f4-101">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="2e6f4-101">New-AzStorageBlobSASToken</span></span>

## <span data-ttu-id="2e6f4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2e6f4-102">SYNOPSIS</span></span>
<span data-ttu-id="2e6f4-103">Skapar en SAS-token för en Azure Storage blob.</span><span class="sxs-lookup"><span data-stu-id="2e6f4-103">Generates a SAS token for an Azure storage blob.</span></span>

## <span data-ttu-id="2e6f4-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2e6f4-104">SYNTAX</span></span>

### <span data-ttu-id="2e6f4-105">BlobNameWithPermission (standard)</span><span class="sxs-lookup"><span data-stu-id="2e6f4-105">BlobNameWithPermission (Default)</span></span>
```
New-AzStorageBlobSASToken [-Container] <String> [-Blob] <String> [-Permission <String>]
 [-Protocol <SharedAccessProtocol>] [-IPAddressOrRange <String>] [-StartTime <DateTime>]
 [-ExpiryTime <DateTime>] [-FullUri] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2e6f4-106">BlobPipelineWithPolicy</span><span class="sxs-lookup"><span data-stu-id="2e6f4-106">BlobPipelineWithPolicy</span></span>
```
New-AzStorageBlobSASToken -CloudBlob <CloudBlob> -Policy <String> [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2e6f4-107">BlobPipelineWithPermission</span><span class="sxs-lookup"><span data-stu-id="2e6f4-107">BlobPipelineWithPermission</span></span>
```
New-AzStorageBlobSASToken -CloudBlob <CloudBlob> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2e6f4-108">BlobNameWithPolicy</span><span class="sxs-lookup"><span data-stu-id="2e6f4-108">BlobNameWithPolicy</span></span>
```
New-AzStorageBlobSASToken [-Container] <String> [-Blob] <String> -Policy <String>
 [-Protocol <SharedAccessProtocol>] [-IPAddressOrRange <String>] [-StartTime <DateTime>]
 [-ExpiryTime <DateTime>] [-FullUri] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2e6f4-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2e6f4-109">DESCRIPTION</span></span>
<span data-ttu-id="2e6f4-110">**New-AzStorageBlobSASToken-** cmdleten genererar en SAS-token (Shared Access signatur) för en Azure Storage blob.</span><span class="sxs-lookup"><span data-stu-id="2e6f4-110">The **New-AzStorageBlobSASToken** cmdlet generates a Shared Access Signature (SAS) token for an Azure storage blob.</span></span>

## <span data-ttu-id="2e6f4-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2e6f4-111">EXAMPLES</span></span>

### <span data-ttu-id="2e6f4-112">Exempel 1: generera en BLOB SAS-token med fullständig BLOB-behörighet</span><span class="sxs-lookup"><span data-stu-id="2e6f4-112">Example 1: Generate a blob SAS token with full blob permission</span></span>
```
PS C:\>New-AzStorageBlobSASToken -Container "ContainerName" -Blob "BlobName" -Permission rwd
```

<span data-ttu-id="2e6f4-113">I det här exemplet skapas en BLOB SAS-token med full BLOB-behörighet.</span><span class="sxs-lookup"><span data-stu-id="2e6f4-113">This example generates a blob SAS token with full blob permission.</span></span>

### <span data-ttu-id="2e6f4-114">Exempel 2: generera en BLOB SAS-token med livs längd</span><span class="sxs-lookup"><span data-stu-id="2e6f4-114">Example 2: Generate a blob SAS token with life time</span></span>
```
PS C:\> $StartTime = Get-Date
PS C:\> $EndTime = $startTime.AddHours(2.0)
PS C:\> New-AzStorageBlobSASToken -Container "ContainerName" -Blob "BlobName" -Permission rwd -StartTime $StartTime -ExpiryTime $EndTime
```

<span data-ttu-id="2e6f4-115">I det här exemplet skapas en BLOB SAS-token med livs längd.</span><span class="sxs-lookup"><span data-stu-id="2e6f4-115">This example generates a blob SAS token with life time.</span></span>

## <span data-ttu-id="2e6f4-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2e6f4-116">PARAMETERS</span></span>

### <span data-ttu-id="2e6f4-117">-BLOB</span><span class="sxs-lookup"><span data-stu-id="2e6f4-117">-Blob</span></span>
<span data-ttu-id="2e6f4-118">Anger lagringsreplik-namnet.</span><span class="sxs-lookup"><span data-stu-id="2e6f4-118">Specifies the storage blob name.</span></span>

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

### <span data-ttu-id="2e6f4-119">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="2e6f4-119">-CloudBlob</span></span>
<span data-ttu-id="2e6f4-120">Anger **CloudBlob** -objektet.</span><span class="sxs-lookup"><span data-stu-id="2e6f4-120">Specifies the **CloudBlob** object.</span></span>
<span data-ttu-id="2e6f4-121">Om du vill hämta ett **CloudBlob** -objekt använder du cmdleten [Get-AzStorageBlob](./Get-AzStorageBlob.md) .</span><span class="sxs-lookup"><span data-stu-id="2e6f4-121">To obtain a **CloudBlob** object, use the [Get-AzStorageBlob](./Get-AzStorageBlob.md) cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Storage.Blob.CloudBlob
Parameter Sets: BlobPipelineWithPolicy, BlobPipelineWithPermission
Aliases: ICloudBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e6f4-122">-Container</span><span class="sxs-lookup"><span data-stu-id="2e6f4-122">-Container</span></span>
<span data-ttu-id="2e6f4-123">Anger namnet på lagrings behållaren.</span><span class="sxs-lookup"><span data-stu-id="2e6f4-123">Specifies the storage container name.</span></span>

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

### <span data-ttu-id="2e6f4-124">-Kontext</span><span class="sxs-lookup"><span data-stu-id="2e6f4-124">-Context</span></span>
<span data-ttu-id="2e6f4-125">Anger lagrings kontexten.</span><span class="sxs-lookup"><span data-stu-id="2e6f4-125">Specifies the storage context.</span></span>

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

### <span data-ttu-id="2e6f4-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e6f4-126">-DefaultProfile</span></span>
<span data-ttu-id="2e6f4-127">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="2e6f4-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2e6f4-128">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="2e6f4-128">-ExpiryTime</span></span>
<span data-ttu-id="2e6f4-129">Anger när signaturen för delad åtkomst upphör.</span><span class="sxs-lookup"><span data-stu-id="2e6f4-129">Specifies when the shared access signature expires.</span></span>

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

### <span data-ttu-id="2e6f4-130">-FullUri</span><span class="sxs-lookup"><span data-stu-id="2e6f4-130">-FullUri</span></span>
<span data-ttu-id="2e6f4-131">Anger att denna cmdlet returnerar full BLOB URI och signatur för delad åtkomst.</span><span class="sxs-lookup"><span data-stu-id="2e6f4-131">Indicates that this cmdlet return the full blob URI and the shared access signature token.</span></span>

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

### <span data-ttu-id="2e6f4-132">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="2e6f4-132">-IPAddressOrRange</span></span>
<span data-ttu-id="2e6f4-133">Anger IP-adressen eller intervallet med IP-adresser som begär Anden ska accepteras från, till exempel 168.1.5.65 eller 168.1.5.60-168.1.5.70.</span><span class="sxs-lookup"><span data-stu-id="2e6f4-133">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="2e6f4-134">Intervallet är inkluderat.</span><span class="sxs-lookup"><span data-stu-id="2e6f4-134">The range is inclusive.</span></span>

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

### <span data-ttu-id="2e6f4-135">-Tillstånd</span><span class="sxs-lookup"><span data-stu-id="2e6f4-135">-Permission</span></span>
<span data-ttu-id="2e6f4-136">Anger behörigheterna för en lagrings-blob.</span><span class="sxs-lookup"><span data-stu-id="2e6f4-136">Specifies the permissions for a storage blob.</span></span> <span data-ttu-id="2e6f4-137">Det är viktigt att Observera att det här är en sträng, till exempel `rwd` (för läsning, skrivning och borttagning).</span><span class="sxs-lookup"><span data-stu-id="2e6f4-137">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span> 

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

### <span data-ttu-id="2e6f4-138">-Princip</span><span class="sxs-lookup"><span data-stu-id="2e6f4-138">-Policy</span></span>
<span data-ttu-id="2e6f4-139">Anger en åtkomst policy för Azure.</span><span class="sxs-lookup"><span data-stu-id="2e6f4-139">Specifies an Azure Stored Access Policy.</span></span>

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

### <span data-ttu-id="2e6f4-140">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="2e6f4-140">-Protocol</span></span>
<span data-ttu-id="2e6f4-141">Anger det protokoll som tillåts för en begäran.</span><span class="sxs-lookup"><span data-stu-id="2e6f4-141">Specifies the protocol permitted for a request.</span></span>
<span data-ttu-id="2e6f4-142">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="2e6f4-142">The acceptable values for this parameter are:</span></span>
* <span data-ttu-id="2e6f4-143">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="2e6f4-143">HttpsOnly</span></span>
* <span data-ttu-id="2e6f4-144">HttpsOrHttp standardvärdet är HttpsOrHttp.</span><span class="sxs-lookup"><span data-stu-id="2e6f4-144">HttpsOrHttp The default value is HttpsOrHttp.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Storage.SharedAccessProtocol]
Parameter Sets: (All)
Aliases:
Accepted values: HttpsOnly, HttpsOrHttp

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e6f4-145">-StartTime</span><span class="sxs-lookup"><span data-stu-id="2e6f4-145">-StartTime</span></span>
<span data-ttu-id="2e6f4-146">Anger den tid då den delade Access-signaturen blir giltig.</span><span class="sxs-lookup"><span data-stu-id="2e6f4-146">Specifies the time at which the shared access signature becomes valid.</span></span>

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

### <span data-ttu-id="2e6f4-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e6f4-147">CommonParameters</span></span>
<span data-ttu-id="2e6f4-148">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2e6f4-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e6f4-149">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2e6f4-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e6f4-150">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2e6f4-150">INPUTS</span></span>

### <span data-ttu-id="2e6f4-151">Microsoft. Azure. Storage. blob. CloudBlob</span><span class="sxs-lookup"><span data-stu-id="2e6f4-151">Microsoft.Azure.Storage.Blob.CloudBlob</span></span>

### <span data-ttu-id="2e6f4-152">Microsoft. Azure. commands. Common. verifikation. abstraktioner. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="2e6f4-152">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="2e6f4-153">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2e6f4-153">OUTPUTS</span></span>

### <span data-ttu-id="2e6f4-154">System. String</span><span class="sxs-lookup"><span data-stu-id="2e6f4-154">System.String</span></span>

## <span data-ttu-id="2e6f4-155">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2e6f4-155">NOTES</span></span>

## <span data-ttu-id="2e6f4-156">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2e6f4-156">RELATED LINKS</span></span>

[<span data-ttu-id="2e6f4-157">Get-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="2e6f4-157">Get-AzStorageBlob</span></span>](./Get-AzStorageBlob.md)

[<span data-ttu-id="2e6f4-158">New-AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="2e6f4-158">New-AzStorageContainerSASToken</span></span>](./New-AzStorageContainerSASToken.md)
