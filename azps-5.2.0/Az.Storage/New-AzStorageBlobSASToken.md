---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 585371E3-D4CE-452E-B0B0-92B3ABD127E7
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstorageblobsastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageBlobSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageBlobSASToken.md
ms.openlocfilehash: fb349f2c5c8d394fb7af31190f58ea2ee10425ba
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98404131"
---
# <span data-ttu-id="57434-101">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="57434-101">New-AzStorageBlobSASToken</span></span>

## <span data-ttu-id="57434-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="57434-102">SYNOPSIS</span></span>
<span data-ttu-id="57434-103">Skapar en SAS-token för en Azure Storage blob.</span><span class="sxs-lookup"><span data-stu-id="57434-103">Generates a SAS token for an Azure storage blob.</span></span>

## <span data-ttu-id="57434-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="57434-104">SYNTAX</span></span>

### <span data-ttu-id="57434-105">BlobNameWithPermission (standard)</span><span class="sxs-lookup"><span data-stu-id="57434-105">BlobNameWithPermission (Default)</span></span>
```
New-AzStorageBlobSASToken [-Container] <String> [-Blob] <String> [-Permission <String>]
 [-Protocol <SharedAccessProtocol>] [-IPAddressOrRange <String>] [-StartTime <DateTime>]
 [-ExpiryTime <DateTime>] [-FullUri] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="57434-106">BlobPipelineWithPolicy</span><span class="sxs-lookup"><span data-stu-id="57434-106">BlobPipelineWithPolicy</span></span>
```
New-AzStorageBlobSASToken -CloudBlob <CloudBlob> [-BlobBaseClient <BlobBaseClient>] -Policy <String>
 [-Protocol <SharedAccessProtocol>] [-IPAddressOrRange <String>] [-StartTime <DateTime>]
 [-ExpiryTime <DateTime>] [-FullUri] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="57434-107">BlobPipelineWithPermission</span><span class="sxs-lookup"><span data-stu-id="57434-107">BlobPipelineWithPermission</span></span>
```
New-AzStorageBlobSASToken -CloudBlob <CloudBlob> [-BlobBaseClient <BlobBaseClient>] [-Permission <String>]
 [-Protocol <SharedAccessProtocol>] [-IPAddressOrRange <String>] [-StartTime <DateTime>]
 [-ExpiryTime <DateTime>] [-FullUri] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="57434-108">BlobNameWithPolicy</span><span class="sxs-lookup"><span data-stu-id="57434-108">BlobNameWithPolicy</span></span>
```
New-AzStorageBlobSASToken [-Container] <String> [-Blob] <String> -Policy <String>
 [-Protocol <SharedAccessProtocol>] [-IPAddressOrRange <String>] [-StartTime <DateTime>]
 [-ExpiryTime <DateTime>] [-FullUri] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="57434-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="57434-109">DESCRIPTION</span></span>
<span data-ttu-id="57434-110">**New-AzStorageBlobSASToken-** cmdleten genererar en SAS-token (Shared Access signatur) för en Azure Storage blob.</span><span class="sxs-lookup"><span data-stu-id="57434-110">The **New-AzStorageBlobSASToken** cmdlet generates a Shared Access Signature (SAS) token for an Azure storage blob.</span></span>

## <span data-ttu-id="57434-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="57434-111">EXAMPLES</span></span>

### <span data-ttu-id="57434-112">Exempel 1: generera en BLOB SAS-token med fullständig BLOB-behörighet</span><span class="sxs-lookup"><span data-stu-id="57434-112">Example 1: Generate a blob SAS token with full blob permission</span></span>
```
PS C:\>New-AzStorageBlobSASToken -Container "ContainerName" -Blob "BlobName" -Permission rwd
```

<span data-ttu-id="57434-113">I det här exemplet skapas en BLOB SAS-token med full BLOB-behörighet.</span><span class="sxs-lookup"><span data-stu-id="57434-113">This example generates a blob SAS token with full blob permission.</span></span>

### <span data-ttu-id="57434-114">Exempel 2: generera en BLOB SAS-token med livs längd</span><span class="sxs-lookup"><span data-stu-id="57434-114">Example 2: Generate a blob SAS token with life time</span></span>
```
PS C:\> $StartTime = Get-Date
PS C:\> $EndTime = $startTime.AddHours(2.0)
PS C:\> New-AzStorageBlobSASToken -Container "ContainerName" -Blob "BlobName" -Permission rwd -StartTime $StartTime -ExpiryTime $EndTime
```

<span data-ttu-id="57434-115">I det här exemplet skapas en BLOB SAS-token med livs längd.</span><span class="sxs-lookup"><span data-stu-id="57434-115">This example generates a blob SAS token with life time.</span></span>

### <span data-ttu-id="57434-116">Exempel 3: skapa en SAS-token för användar identitet med lagrings kontext baserad på OAuth-autentisering</span><span class="sxs-lookup"><span data-stu-id="57434-116">Example 3: Generate a User Identity SAS token with storage context based on OAuth authentication</span></span>
```
PS C:\> $ctx = New-AzStorageContext -StorageAccountName $accountName -UseConnectedAccount
PS C:\> $StartTime = Get-Date
PS C:\> $EndTime = $startTime.AddDays(6)
PS C:\> New-AzStorageBlobSASToken -Container "ContainerName" -Blob "BlobName" -Permission rwd -StartTime $StartTime -ExpiryTime $EndTime -context $ctx
```

<span data-ttu-id="57434-117">Det här exemplet genererar en SAS-token för User Identity BLOB med lagrings kontext baserad på OAuth-autentisering</span><span class="sxs-lookup"><span data-stu-id="57434-117">This example generates a User Identity blob SAS token with storage context based on OAuth authentication</span></span>

## <span data-ttu-id="57434-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="57434-118">PARAMETERS</span></span>

### <span data-ttu-id="57434-119">-BLOB</span><span class="sxs-lookup"><span data-stu-id="57434-119">-Blob</span></span>
<span data-ttu-id="57434-120">Anger lagringsreplik-namnet.</span><span class="sxs-lookup"><span data-stu-id="57434-120">Specifies the storage blob name.</span></span>

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

### <span data-ttu-id="57434-121">-BlobBaseClient</span><span class="sxs-lookup"><span data-stu-id="57434-121">-BlobBaseClient</span></span>
<span data-ttu-id="57434-122">BlobBaseClient-objekt</span><span class="sxs-lookup"><span data-stu-id="57434-122">BlobBaseClient Object</span></span>

```yaml
Type: Azure.Storage.Blobs.Specialized.BlobBaseClient
Parameter Sets: BlobPipelineWithPolicy, BlobPipelineWithPermission
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57434-123">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="57434-123">-CloudBlob</span></span>
<span data-ttu-id="57434-124">Anger **CloudBlob** -objektet.</span><span class="sxs-lookup"><span data-stu-id="57434-124">Specifies the **CloudBlob** object.</span></span>
<span data-ttu-id="57434-125">Om du vill hämta ett **CloudBlob** -objekt använder du cmdleten [Get-AzStorageBlob](./Get-AzStorageBlob.md) .</span><span class="sxs-lookup"><span data-stu-id="57434-125">To obtain a **CloudBlob** object, use the [Get-AzStorageBlob](./Get-AzStorageBlob.md) cmdlet.</span></span>

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

### <span data-ttu-id="57434-126">-Container</span><span class="sxs-lookup"><span data-stu-id="57434-126">-Container</span></span>
<span data-ttu-id="57434-127">Anger namnet på lagrings behållaren.</span><span class="sxs-lookup"><span data-stu-id="57434-127">Specifies the storage container name.</span></span>

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

### <span data-ttu-id="57434-128">-Kontext</span><span class="sxs-lookup"><span data-stu-id="57434-128">-Context</span></span>
<span data-ttu-id="57434-129">Anger lagrings kontexten.</span><span class="sxs-lookup"><span data-stu-id="57434-129">Specifies the storage context.</span></span>
<span data-ttu-id="57434-130">När lagrings kontexten baseras på OAuth-autentisering genererar en User Identity BLOB SAS-token.</span><span class="sxs-lookup"><span data-stu-id="57434-130">When the storage context is based on OAuth authentication, will generates a User Identity blob SAS token.</span></span>

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

### <span data-ttu-id="57434-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57434-131">-DefaultProfile</span></span>
<span data-ttu-id="57434-132">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="57434-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="57434-133">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="57434-133">-ExpiryTime</span></span>
<span data-ttu-id="57434-134">Anger när signaturen för delad åtkomst upphör.</span><span class="sxs-lookup"><span data-stu-id="57434-134">Specifies when the shared access signature expires.</span></span>
<span data-ttu-id="57434-135">När lagrings kontexten baseras på OAuth-autentisering måste förfallo tiden vara på 7 dagar från aktuell tid och får inte vara tidigare än den aktuella tiden.</span><span class="sxs-lookup"><span data-stu-id="57434-135">When the storage context is based on OAuth authentication, the expire time must be in 7 days from current time, and must not be earlier than current time.</span></span>

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

### <span data-ttu-id="57434-136">-FullUri</span><span class="sxs-lookup"><span data-stu-id="57434-136">-FullUri</span></span>
<span data-ttu-id="57434-137">Anger att denna cmdlet returnerar full BLOB URI och signatur för delad åtkomst.</span><span class="sxs-lookup"><span data-stu-id="57434-137">Indicates that this cmdlet return the full blob URI and the shared access signature token.</span></span>

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

### <span data-ttu-id="57434-138">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="57434-138">-IPAddressOrRange</span></span>
<span data-ttu-id="57434-139">Anger IP-adressen eller intervallet med IP-adresser som begär Anden ska accepteras från, till exempel 168.1.5.65 eller 168.1.5.60-168.1.5.70.</span><span class="sxs-lookup"><span data-stu-id="57434-139">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="57434-140">Intervallet är inkluderat.</span><span class="sxs-lookup"><span data-stu-id="57434-140">The range is inclusive.</span></span>

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

### <span data-ttu-id="57434-141">-Tillstånd</span><span class="sxs-lookup"><span data-stu-id="57434-141">-Permission</span></span>
<span data-ttu-id="57434-142">Anger behörigheterna för en lagrings-blob.</span><span class="sxs-lookup"><span data-stu-id="57434-142">Specifies the permissions for a storage blob.</span></span> <span data-ttu-id="57434-143">Det är viktigt att Observera att det här är en sträng, till exempel `rwd` (för läsning, skrivning och borttagning).</span><span class="sxs-lookup"><span data-stu-id="57434-143">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span> 

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

### <span data-ttu-id="57434-144">-Princip</span><span class="sxs-lookup"><span data-stu-id="57434-144">-Policy</span></span>
<span data-ttu-id="57434-145">Anger en åtkomst policy för Azure.</span><span class="sxs-lookup"><span data-stu-id="57434-145">Specifies an Azure Stored Access Policy.</span></span>

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

### <span data-ttu-id="57434-146">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="57434-146">-Protocol</span></span>
<span data-ttu-id="57434-147">Anger det protokoll som tillåts för en begäran.</span><span class="sxs-lookup"><span data-stu-id="57434-147">Specifies the protocol permitted for a request.</span></span>
<span data-ttu-id="57434-148">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="57434-148">The acceptable values for this parameter are:</span></span>
* <span data-ttu-id="57434-149">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="57434-149">HttpsOnly</span></span>
* <span data-ttu-id="57434-150">HttpsOrHttp standardvärdet är HttpsOrHttp.</span><span class="sxs-lookup"><span data-stu-id="57434-150">HttpsOrHttp The default value is HttpsOrHttp.</span></span>

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

### <span data-ttu-id="57434-151">-StartTime</span><span class="sxs-lookup"><span data-stu-id="57434-151">-StartTime</span></span>
<span data-ttu-id="57434-152">Anger den tid då den delade Access-signaturen blir giltig.</span><span class="sxs-lookup"><span data-stu-id="57434-152">Specifies the time at which the shared access signature becomes valid.</span></span>

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

### <span data-ttu-id="57434-153">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="57434-153">-Confirm</span></span>
<span data-ttu-id="57434-154">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="57434-154">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57434-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="57434-155">-WhatIf</span></span>
<span data-ttu-id="57434-156">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="57434-156">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="57434-157">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="57434-157">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57434-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57434-158">CommonParameters</span></span>
<span data-ttu-id="57434-159">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="57434-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57434-160">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="57434-160">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57434-161">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="57434-161">INPUTS</span></span>

### <span data-ttu-id="57434-162">Microsoft. Azure. Storage. blob. CloudBlob</span><span class="sxs-lookup"><span data-stu-id="57434-162">Microsoft.Azure.Storage.Blob.CloudBlob</span></span>

### <span data-ttu-id="57434-163">Microsoft. Azure. commands. Common. verifikation. abstraktioner. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="57434-163">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="57434-164">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="57434-164">OUTPUTS</span></span>

### <span data-ttu-id="57434-165">System. String</span><span class="sxs-lookup"><span data-stu-id="57434-165">System.String</span></span>

## <span data-ttu-id="57434-166">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="57434-166">NOTES</span></span>

## <span data-ttu-id="57434-167">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="57434-167">RELATED LINKS</span></span>

[<span data-ttu-id="57434-168">Get-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="57434-168">Get-AzStorageBlob</span></span>](./Get-AzStorageBlob.md)

[<span data-ttu-id="57434-169">New-AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="57434-169">New-AzStorageContainerSASToken</span></span>](./New-AzStorageContainerSASToken.md)
