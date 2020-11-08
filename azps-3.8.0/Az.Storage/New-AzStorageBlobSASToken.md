---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 585371E3-D4CE-452E-B0B0-92B3ABD127E7
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstorageblobsastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageBlobSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageBlobSASToken.md
ms.openlocfilehash: 6bcb5163e31f2acbdd3e180cf76aef8fcfb33571
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94090863"
---
# <span data-ttu-id="39338-101">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="39338-101">New-AzStorageBlobSASToken</span></span>

## <span data-ttu-id="39338-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="39338-102">SYNOPSIS</span></span>
<span data-ttu-id="39338-103">Skapar en SAS-token för en Azure Storage blob.</span><span class="sxs-lookup"><span data-stu-id="39338-103">Generates a SAS token for an Azure storage blob.</span></span>

## <span data-ttu-id="39338-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="39338-104">SYNTAX</span></span>

### <span data-ttu-id="39338-105">BlobNameWithPermission (standard)</span><span class="sxs-lookup"><span data-stu-id="39338-105">BlobNameWithPermission (Default)</span></span>
```
New-AzStorageBlobSASToken [-Container] <String> [-Blob] <String> [-Permission <String>]
 [-Protocol <SharedAccessProtocol>] [-IPAddressOrRange <String>] [-StartTime <DateTime>]
 [-ExpiryTime <DateTime>] [-FullUri] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="39338-106">BlobPipelineWithPolicy</span><span class="sxs-lookup"><span data-stu-id="39338-106">BlobPipelineWithPolicy</span></span>
```
New-AzStorageBlobSASToken -CloudBlob <CloudBlob> -Policy <String> [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="39338-107">BlobPipelineWithPermission</span><span class="sxs-lookup"><span data-stu-id="39338-107">BlobPipelineWithPermission</span></span>
```
New-AzStorageBlobSASToken -CloudBlob <CloudBlob> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="39338-108">BlobNameWithPolicy</span><span class="sxs-lookup"><span data-stu-id="39338-108">BlobNameWithPolicy</span></span>
```
New-AzStorageBlobSASToken [-Container] <String> [-Blob] <String> -Policy <String>
 [-Protocol <SharedAccessProtocol>] [-IPAddressOrRange <String>] [-StartTime <DateTime>]
 [-ExpiryTime <DateTime>] [-FullUri] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="39338-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="39338-109">DESCRIPTION</span></span>
<span data-ttu-id="39338-110">**New-AzStorageBlobSASToken-** cmdleten genererar en SAS-token (Shared Access signatur) för en Azure Storage blob.</span><span class="sxs-lookup"><span data-stu-id="39338-110">The **New-AzStorageBlobSASToken** cmdlet generates a Shared Access Signature (SAS) token for an Azure storage blob.</span></span>

## <span data-ttu-id="39338-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="39338-111">EXAMPLES</span></span>

### <span data-ttu-id="39338-112">Exempel 1: generera en BLOB SAS-token med fullständig BLOB-behörighet</span><span class="sxs-lookup"><span data-stu-id="39338-112">Example 1: Generate a blob SAS token with full blob permission</span></span>
```
PS C:\>New-AzStorageBlobSASToken -Container "ContainerName" -Blob "BlobName" -Permission rwd
```

<span data-ttu-id="39338-113">I det här exemplet skapas en BLOB SAS-token med full BLOB-behörighet.</span><span class="sxs-lookup"><span data-stu-id="39338-113">This example generates a blob SAS token with full blob permission.</span></span>

### <span data-ttu-id="39338-114">Exempel 2: generera en BLOB SAS-token med livs längd</span><span class="sxs-lookup"><span data-stu-id="39338-114">Example 2: Generate a blob SAS token with life time</span></span>
```
PS C:\> $StartTime = Get-Date
PS C:\> $EndTime = $startTime.AddHours(2.0)
PS C:\> New-AzStorageBlobSASToken -Container "ContainerName" -Blob "BlobName" -Permission rwd -StartTime $StartTime -ExpiryTime $EndTime
```

<span data-ttu-id="39338-115">I det här exemplet skapas en BLOB SAS-token med livs längd.</span><span class="sxs-lookup"><span data-stu-id="39338-115">This example generates a blob SAS token with life time.</span></span>

### <span data-ttu-id="39338-116">Exempel 3: skapa en SAS-token för användar identitet med lagrings kontext baserad på OAuth-autentisering</span><span class="sxs-lookup"><span data-stu-id="39338-116">Example 3: Generate a User Identity SAS token with storage context based on OAuth authentication</span></span>
```
PS C:\> $ctx = New-AzStorageContext -StorageAccountName $accountName -UseConnectedAccount
PS C:\> $StartTime = Get-Date
PS C:\> $EndTime = $startTime.AddDays(6)
PS C:\> New-AzStorageBlobSASToken -Container "ContainerName" -Blob "BlobName" -Permission rwd -StartTime $StartTime -ExpiryTime $EndTime -context $ctx
```

<span data-ttu-id="39338-117">Det här exemplet genererar en SAS-token för User Identity BLOB med lagrings kontext baserad på OAuth-autentisering</span><span class="sxs-lookup"><span data-stu-id="39338-117">This example generates a User Identity blob SAS token with storage context based on OAuth authentication</span></span>

## <span data-ttu-id="39338-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="39338-118">PARAMETERS</span></span>

### <span data-ttu-id="39338-119">-BLOB</span><span class="sxs-lookup"><span data-stu-id="39338-119">-Blob</span></span>
<span data-ttu-id="39338-120">Anger lagringsreplik-namnet.</span><span class="sxs-lookup"><span data-stu-id="39338-120">Specifies the storage blob name.</span></span>

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

### <span data-ttu-id="39338-121">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="39338-121">-CloudBlob</span></span>
<span data-ttu-id="39338-122">Anger **CloudBlob** -objektet.</span><span class="sxs-lookup"><span data-stu-id="39338-122">Specifies the **CloudBlob** object.</span></span>
<span data-ttu-id="39338-123">Om du vill hämta ett **CloudBlob** -objekt använder du cmdleten [Get-AzStorageBlob](./Get-AzStorageBlob.md) .</span><span class="sxs-lookup"><span data-stu-id="39338-123">To obtain a **CloudBlob** object, use the [Get-AzStorageBlob](./Get-AzStorageBlob.md) cmdlet.</span></span>

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

### <span data-ttu-id="39338-124">-Container</span><span class="sxs-lookup"><span data-stu-id="39338-124">-Container</span></span>
<span data-ttu-id="39338-125">Anger namnet på lagrings behållaren.</span><span class="sxs-lookup"><span data-stu-id="39338-125">Specifies the storage container name.</span></span>

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

### <span data-ttu-id="39338-126">-Kontext</span><span class="sxs-lookup"><span data-stu-id="39338-126">-Context</span></span>
<span data-ttu-id="39338-127">Anger lagrings kontexten.</span><span class="sxs-lookup"><span data-stu-id="39338-127">Specifies the storage context.</span></span>
<span data-ttu-id="39338-128">När lagrings kontexten baseras på OAuth-autentisering genererar en User Identity BLOB SAS-token.</span><span class="sxs-lookup"><span data-stu-id="39338-128">When the storage context is based on OAuth authentication, will generates a User Identity blob SAS token.</span></span>

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

### <span data-ttu-id="39338-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39338-129">-DefaultProfile</span></span>
<span data-ttu-id="39338-130">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="39338-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="39338-131">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="39338-131">-ExpiryTime</span></span>
<span data-ttu-id="39338-132">Anger när signaturen för delad åtkomst upphör.</span><span class="sxs-lookup"><span data-stu-id="39338-132">Specifies when the shared access signature expires.</span></span>
<span data-ttu-id="39338-133">När lagrings kontexten baseras på OAuth-autentisering måste förfallo tiden vara på 7 dagar från aktuell tid och får inte vara tidigare än den aktuella tiden.</span><span class="sxs-lookup"><span data-stu-id="39338-133">When the storage context is based on OAuth authentication, the expire time must be in 7 days from current time, and must not be earlier than current time.</span></span>

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

### <span data-ttu-id="39338-134">-FullUri</span><span class="sxs-lookup"><span data-stu-id="39338-134">-FullUri</span></span>
<span data-ttu-id="39338-135">Anger att denna cmdlet returnerar full BLOB URI och signatur för delad åtkomst.</span><span class="sxs-lookup"><span data-stu-id="39338-135">Indicates that this cmdlet return the full blob URI and the shared access signature token.</span></span>

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

### <span data-ttu-id="39338-136">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="39338-136">-IPAddressOrRange</span></span>
<span data-ttu-id="39338-137">Anger IP-adressen eller intervallet med IP-adresser som begär Anden ska accepteras från, till exempel 168.1.5.65 eller 168.1.5.60-168.1.5.70.</span><span class="sxs-lookup"><span data-stu-id="39338-137">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="39338-138">Intervallet är inkluderat.</span><span class="sxs-lookup"><span data-stu-id="39338-138">The range is inclusive.</span></span>

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

### <span data-ttu-id="39338-139">-Tillstånd</span><span class="sxs-lookup"><span data-stu-id="39338-139">-Permission</span></span>
<span data-ttu-id="39338-140">Anger behörigheterna för en lagrings-blob.</span><span class="sxs-lookup"><span data-stu-id="39338-140">Specifies the permissions for a storage blob.</span></span> <span data-ttu-id="39338-141">Det är viktigt att Observera att det här är en sträng, till exempel `rwd` (för läsning, skrivning och borttagning).</span><span class="sxs-lookup"><span data-stu-id="39338-141">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span> 

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

### <span data-ttu-id="39338-142">-Princip</span><span class="sxs-lookup"><span data-stu-id="39338-142">-Policy</span></span>
<span data-ttu-id="39338-143">Anger en åtkomst policy för Azure.</span><span class="sxs-lookup"><span data-stu-id="39338-143">Specifies an Azure Stored Access Policy.</span></span>

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

### <span data-ttu-id="39338-144">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="39338-144">-Protocol</span></span>
<span data-ttu-id="39338-145">Anger det protokoll som tillåts för en begäran.</span><span class="sxs-lookup"><span data-stu-id="39338-145">Specifies the protocol permitted for a request.</span></span>
<span data-ttu-id="39338-146">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="39338-146">The acceptable values for this parameter are:</span></span>
* <span data-ttu-id="39338-147">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="39338-147">HttpsOnly</span></span>
* <span data-ttu-id="39338-148">HttpsOrHttp standardvärdet är HttpsOrHttp.</span><span class="sxs-lookup"><span data-stu-id="39338-148">HttpsOrHttp The default value is HttpsOrHttp.</span></span>

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

### <span data-ttu-id="39338-149">-StartTime</span><span class="sxs-lookup"><span data-stu-id="39338-149">-StartTime</span></span>
<span data-ttu-id="39338-150">Anger den tid då den delade Access-signaturen blir giltig.</span><span class="sxs-lookup"><span data-stu-id="39338-150">Specifies the time at which the shared access signature becomes valid.</span></span>

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

### <span data-ttu-id="39338-151">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="39338-151">-Confirm</span></span>
<span data-ttu-id="39338-152">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="39338-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="39338-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="39338-153">-WhatIf</span></span>
<span data-ttu-id="39338-154">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="39338-154">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="39338-155">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="39338-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="39338-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39338-156">CommonParameters</span></span>
<span data-ttu-id="39338-157">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="39338-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39338-158">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="39338-158">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39338-159">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="39338-159">INPUTS</span></span>

### <span data-ttu-id="39338-160">Microsoft. Azure. Storage. blob. CloudBlob</span><span class="sxs-lookup"><span data-stu-id="39338-160">Microsoft.Azure.Storage.Blob.CloudBlob</span></span>

### <span data-ttu-id="39338-161">Microsoft. Azure. commands. Common. verifikation. abstraktioner. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="39338-161">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="39338-162">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="39338-162">OUTPUTS</span></span>

### <span data-ttu-id="39338-163">System. String</span><span class="sxs-lookup"><span data-stu-id="39338-163">System.String</span></span>

## <span data-ttu-id="39338-164">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="39338-164">NOTES</span></span>

## <span data-ttu-id="39338-165">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="39338-165">RELATED LINKS</span></span>

[<span data-ttu-id="39338-166">Get-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="39338-166">Get-AzStorageBlob</span></span>](./Get-AzStorageBlob.md)

[<span data-ttu-id="39338-167">New-AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="39338-167">New-AzStorageContainerSASToken</span></span>](./New-AzStorageContainerSASToken.md)
