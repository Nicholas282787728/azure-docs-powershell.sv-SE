---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 6FF04E82-4921-4F7B-83D0-6997316BC5FD
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstoragecontainersastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageContainerSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageContainerSASToken.md
ms.openlocfilehash: 4e265fab8df3abd897c27131e0673241ce37b946
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94270401"
---
# <span data-ttu-id="4ac07-101">New-AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="4ac07-101">New-AzStorageContainerSASToken</span></span>

## <span data-ttu-id="4ac07-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4ac07-102">SYNOPSIS</span></span>
<span data-ttu-id="4ac07-103">Skapar en SAS-token för en Azure Storage-behållare.</span><span class="sxs-lookup"><span data-stu-id="4ac07-103">Generates an SAS token for an Azure storage container.</span></span>

## <span data-ttu-id="4ac07-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4ac07-104">SYNTAX</span></span>

### <span data-ttu-id="4ac07-105">SasPolicy</span><span class="sxs-lookup"><span data-stu-id="4ac07-105">SasPolicy</span></span>
```
New-AzStorageContainerSASToken [-Name] <String> -Policy <String> [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4ac07-106">SasPermission</span><span class="sxs-lookup"><span data-stu-id="4ac07-106">SasPermission</span></span>
```
New-AzStorageContainerSASToken [-Name] <String> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4ac07-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4ac07-107">DESCRIPTION</span></span>
<span data-ttu-id="4ac07-108">**New-AzStorageContainerSASToken-** cmdleten genererar en SAS-token (Shared Access signatur) för en Azure Storage-behållare.</span><span class="sxs-lookup"><span data-stu-id="4ac07-108">The **New-AzStorageContainerSASToken** cmdlet generates a Shared Access Signature (SAS) token for an Azure storage container.</span></span>

## <span data-ttu-id="4ac07-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4ac07-109">EXAMPLES</span></span>

### <span data-ttu-id="4ac07-110">Exempel 1: generera en SAS-token för behållare med fullständig behörighet för container</span><span class="sxs-lookup"><span data-stu-id="4ac07-110">Example 1: Generate a container SAS token with full container permission</span></span>
```
PS C:\>New-AzStorageContainerSASToken -Name "Test" -Permission rwdl
```

<span data-ttu-id="4ac07-111">I det här exemplet skapas en SAS-token för behållare med fullständig behörighet för behållaren.</span><span class="sxs-lookup"><span data-stu-id="4ac07-111">This example generates a container SAS token with full container permission.</span></span>

### <span data-ttu-id="4ac07-112">Exempel 2: generera en SAS-token med flera behållare per pipeline</span><span class="sxs-lookup"><span data-stu-id="4ac07-112">Example 2: Generate multiple container SAS token by pipeline</span></span>
```
PS C:\>Get-AzStorageContainer -Container test* | New-AzStorageContainerSASToken -Permission rwdl
```

<span data-ttu-id="4ac07-113">I det här exemplet skapas SAS-token med flera behållare med hjälp av pipeline.</span><span class="sxs-lookup"><span data-stu-id="4ac07-113">This example generates multiple container SAS tokens by using the pipeline.</span></span>

### <span data-ttu-id="4ac07-114">Exempel 3: skapa SAS-token för behållare med delad åtkomst policy</span><span class="sxs-lookup"><span data-stu-id="4ac07-114">Example 3: Generate container SAS token with shared access policy</span></span>
```
PS C:\>New-AzStorageContainerSASToken -Name "Test" -Policy "PolicyName"
```

<span data-ttu-id="4ac07-115">I det här exemplet skapas en SAS-token för behållare med delad åtkomst policy.</span><span class="sxs-lookup"><span data-stu-id="4ac07-115">This example generates a container SAS token with shared access policy.</span></span>

### <span data-ttu-id="4ac07-116">Exempel 3: generera en SAS-token för användar identitet med lagrings kontext baserad på OAuth-autentisering</span><span class="sxs-lookup"><span data-stu-id="4ac07-116">Example 3: Generate a User Identity container SAS token with storage context based on OAuth authentication</span></span>
```
PS C:\> $ctx = New-AzStorageContext -StorageAccountName $accountName -UseConnectedAccount
PS C:\> $StartTime = Get-Date
PS C:\> $EndTime = $startTime.AddDays(6)
PS C:\> New-AzStorageContainerSASToken -Name "ContainerName" -Permission rwd -StartTime $StartTime -ExpiryTime $EndTime -context $ctx
```

<span data-ttu-id="4ac07-117">I det här exemplet skapas en SAS-token för användar identitets behållare med lagrings kontext baserad på OAuth-autentisering</span><span class="sxs-lookup"><span data-stu-id="4ac07-117">This example generates a User Identity container SAS token with storage context based on OAuth authentication</span></span>

## <span data-ttu-id="4ac07-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4ac07-118">PARAMETERS</span></span>

### <span data-ttu-id="4ac07-119">-Kontext</span><span class="sxs-lookup"><span data-stu-id="4ac07-119">-Context</span></span>
<span data-ttu-id="4ac07-120">Anger en Azure Storage-kontext.</span><span class="sxs-lookup"><span data-stu-id="4ac07-120">Specifies an Azure storage context.</span></span>
<span data-ttu-id="4ac07-121">Du kan skapa det med hjälp av New-AzStorageContext cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4ac07-121">You can create it by using the New-AzStorageContext cmdlet.</span></span>
<span data-ttu-id="4ac07-122">När lagrings kontexten baseras på OAuth-autentisering genererar en SAS-token för användar-ID-behållare.</span><span class="sxs-lookup"><span data-stu-id="4ac07-122">When the storage context is based on OAuth authentication, will generates a User Identity container SAS token.</span></span>

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

### <span data-ttu-id="4ac07-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ac07-123">-DefaultProfile</span></span>
<span data-ttu-id="4ac07-124">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="4ac07-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4ac07-125">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="4ac07-125">-ExpiryTime</span></span>
<span data-ttu-id="4ac07-126">Anger den tid då den delade åtkomst-signaturen blir ogiltig.</span><span class="sxs-lookup"><span data-stu-id="4ac07-126">Specifies the time at which the shared access signature becomes invalid.</span></span>
<span data-ttu-id="4ac07-127">Om användaren anger start tiden men inte utgångs tiden, anges start tiden plus en timme.</span><span class="sxs-lookup"><span data-stu-id="4ac07-127">If the user sets the start time but not the expiry time, the expiry time is set to the start time plus one hour.</span></span>
<span data-ttu-id="4ac07-128">Om varken start tiden eller utgångs tiden har angetts anges den aktuella tiden plus en timme.</span><span class="sxs-lookup"><span data-stu-id="4ac07-128">If neither the start time nor the expiry time is specified, the expiry time is set to the current time plus one hour.</span></span>
<span data-ttu-id="4ac07-129">När lagrings kontexten baseras på OAuth-autentisering måste förfallo tiden vara på 7 dagar från aktuell tid och får inte vara tidigare än den aktuella tiden.</span><span class="sxs-lookup"><span data-stu-id="4ac07-129">When the storage context is based on OAuth authentication, the expire time must be in 7 days from current time, and must not be earlier than current time.</span></span>

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

### <span data-ttu-id="4ac07-130">-FullUri</span><span class="sxs-lookup"><span data-stu-id="4ac07-130">-FullUri</span></span>
<span data-ttu-id="4ac07-131">Anger att denna cmdlet returnerar full BLOB URI och signatur för delad åtkomst.</span><span class="sxs-lookup"><span data-stu-id="4ac07-131">Indicates that this cmdlet return the full blob URI and the shared access signature token.</span></span>

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

### <span data-ttu-id="4ac07-132">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="4ac07-132">-IPAddressOrRange</span></span>
<span data-ttu-id="4ac07-133">Anger IP-adressen eller intervallet med IP-adresser som begär Anden ska accepteras från, till exempel 168.1.5.65 eller 168.1.5.60-168.1.5.70.</span><span class="sxs-lookup"><span data-stu-id="4ac07-133">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="4ac07-134">Intervallet är inkluderat.</span><span class="sxs-lookup"><span data-stu-id="4ac07-134">The range is inclusive.</span></span>

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

### <span data-ttu-id="4ac07-135">-Namn</span><span class="sxs-lookup"><span data-stu-id="4ac07-135">-Name</span></span>
<span data-ttu-id="4ac07-136">Anger ett namn på en Azure-lagringsenhet.</span><span class="sxs-lookup"><span data-stu-id="4ac07-136">Specifies an Azure storage container name.</span></span>

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

### <span data-ttu-id="4ac07-137">-Tillstånd</span><span class="sxs-lookup"><span data-stu-id="4ac07-137">-Permission</span></span>
<span data-ttu-id="4ac07-138">Anger behörigheter för en lagrings behållare.</span><span class="sxs-lookup"><span data-stu-id="4ac07-138">Specifies permissions for a storage container.</span></span>
<span data-ttu-id="4ac07-139">Det är viktigt att Observera att det här är en sträng, till exempel `rwd` (för läsning, skrivning och borttagning).</span><span class="sxs-lookup"><span data-stu-id="4ac07-139">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

```yaml
Type: System.String
Parameter Sets: SasPermission
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ac07-140">-Princip</span><span class="sxs-lookup"><span data-stu-id="4ac07-140">-Policy</span></span>
<span data-ttu-id="4ac07-141">Anger en åtkomst policy för Azure.</span><span class="sxs-lookup"><span data-stu-id="4ac07-141">Specifies an Azure Stored Access Policy.</span></span>

```yaml
Type: System.String
Parameter Sets: SasPolicy
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ac07-142">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="4ac07-142">-Protocol</span></span>
<span data-ttu-id="4ac07-143">Anger det protokoll som tillåts för en begäran.</span><span class="sxs-lookup"><span data-stu-id="4ac07-143">Specifies the protocol permitted for a request.</span></span>
<span data-ttu-id="4ac07-144">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="4ac07-144">The acceptable values for this parameter are:</span></span>
* <span data-ttu-id="4ac07-145">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="4ac07-145">HttpsOnly</span></span>
* <span data-ttu-id="4ac07-146">HttpsOrHttp standardvärdet är HttpsOrHttp.</span><span class="sxs-lookup"><span data-stu-id="4ac07-146">HttpsOrHttp The default value is HttpsOrHttp.</span></span>

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

### <span data-ttu-id="4ac07-147">-StartTime</span><span class="sxs-lookup"><span data-stu-id="4ac07-147">-StartTime</span></span>
<span data-ttu-id="4ac07-148">Anger den tid då den delade Access-signaturen blir giltig.</span><span class="sxs-lookup"><span data-stu-id="4ac07-148">Specifies the time at which the shared access signature becomes valid.</span></span>

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

### <span data-ttu-id="4ac07-149">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="4ac07-149">-Confirm</span></span>
<span data-ttu-id="4ac07-150">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="4ac07-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4ac07-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4ac07-151">-WhatIf</span></span>
<span data-ttu-id="4ac07-152">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="4ac07-152">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4ac07-153">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="4ac07-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4ac07-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ac07-154">CommonParameters</span></span>
<span data-ttu-id="4ac07-155">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4ac07-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ac07-156">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4ac07-156">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ac07-157">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4ac07-157">INPUTS</span></span>

### <span data-ttu-id="4ac07-158">System. String</span><span class="sxs-lookup"><span data-stu-id="4ac07-158">System.String</span></span>

### <span data-ttu-id="4ac07-159">Microsoft. Azure. commands. Common. verifikation. abstraktioner. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="4ac07-159">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="4ac07-160">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4ac07-160">OUTPUTS</span></span>

### <span data-ttu-id="4ac07-161">System. String</span><span class="sxs-lookup"><span data-stu-id="4ac07-161">System.String</span></span>

## <span data-ttu-id="4ac07-162">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4ac07-162">NOTES</span></span>

## <span data-ttu-id="4ac07-163">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4ac07-163">RELATED LINKS</span></span>

[<span data-ttu-id="4ac07-164">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="4ac07-164">New-AzStorageBlobSASToken</span></span>](./New-AzStorageBlobSASToken.md)
