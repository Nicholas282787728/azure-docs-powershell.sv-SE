---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 6FF04E82-4921-4F7B-83D0-6997316BC5FD
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/new-azurestoragecontainersastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageContainerSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageContainerSASToken.md
ms.openlocfilehash: 0e8ad44ebbd8a5585626de27317caa14b408f87a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93581243"
---
# <span data-ttu-id="10361-101">New-AzureStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="10361-101">New-AzureStorageContainerSASToken</span></span>

## <span data-ttu-id="10361-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="10361-102">SYNOPSIS</span></span>
<span data-ttu-id="10361-103">Skapar en SAS-token för en Azure Storage-behållare.</span><span class="sxs-lookup"><span data-stu-id="10361-103">Generates an SAS token for an Azure storage container.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="10361-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="10361-104">SYNTAX</span></span>

### <span data-ttu-id="10361-105">SasPolicy</span><span class="sxs-lookup"><span data-stu-id="10361-105">SasPolicy</span></span>
```
New-AzureStorageContainerSASToken [-Name] <String> -Policy <String> [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [<CommonParameters>]
```

### <span data-ttu-id="10361-106">SasPermission</span><span class="sxs-lookup"><span data-stu-id="10361-106">SasPermission</span></span>
```
New-AzureStorageContainerSASToken [-Name] <String> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [<CommonParameters>]
```

## <span data-ttu-id="10361-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="10361-107">DESCRIPTION</span></span>
<span data-ttu-id="10361-108">**New-AzureStorageContainerSASToken-** cmdleten genererar en SAS-token (Shared Access signatur) för en Azure Storage-behållare.</span><span class="sxs-lookup"><span data-stu-id="10361-108">The **New-AzureStorageContainerSASToken** cmdlet generates a Shared Access Signature (SAS) token for an Azure storage container.</span></span>

## <span data-ttu-id="10361-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="10361-109">EXAMPLES</span></span>

### <span data-ttu-id="10361-110">Exempel 1: generera en SAS-token för behållare med fullständig behörighet för container</span><span class="sxs-lookup"><span data-stu-id="10361-110">Example 1: Generate a container SAS token with full container permission</span></span>
```
PS C:\>New-AzureStorageContainerSASToken -Name "Test" -Permission rwdl
```

<span data-ttu-id="10361-111">I det här exemplet skapas en SAS-token för behållare med fullständig behörighet för behållaren.</span><span class="sxs-lookup"><span data-stu-id="10361-111">This example generates a container SAS token with full container permission.</span></span>

### <span data-ttu-id="10361-112">Exempel 2: generera en SAS-token med flera behållare per pipeline</span><span class="sxs-lookup"><span data-stu-id="10361-112">Example 2: Generate multiple container SAS token by pipeline</span></span>
```
PS C:\>Get-AzureStorageContainer -Container test* | New-AzureStorageContainerSASToken -Permission rwdl
```

<span data-ttu-id="10361-113">I det här exemplet skapas SAS-token med flera behållare med hjälp av pipeline.</span><span class="sxs-lookup"><span data-stu-id="10361-113">This example generates multiple container SAS tokens by using the pipeline.</span></span>

### <span data-ttu-id="10361-114">Exempel 3: skapa SAS-token för behållare med delad åtkomst policy</span><span class="sxs-lookup"><span data-stu-id="10361-114">Example 3: Generate container SAS token with shared access policy</span></span>
```
PS C:\>New-AzureStorageContainerSASToken -Name "Test" -Policy "PolicyName"
```

<span data-ttu-id="10361-115">I det här exemplet skapas en SAS-token för behållare med delad åtkomst policy.</span><span class="sxs-lookup"><span data-stu-id="10361-115">This example generates a container SAS token with shared access policy.</span></span>

## <span data-ttu-id="10361-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="10361-116">PARAMETERS</span></span>

### <span data-ttu-id="10361-117">-Kontext</span><span class="sxs-lookup"><span data-stu-id="10361-117">-Context</span></span>
<span data-ttu-id="10361-118">Anger en Azure Storage-kontext.</span><span class="sxs-lookup"><span data-stu-id="10361-118">Specifies an Azure storage context.</span></span>
<span data-ttu-id="10361-119">Du kan skapa det med hjälp av New-AzureStorageContext cmdlet.</span><span class="sxs-lookup"><span data-stu-id="10361-119">You can create it by using the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="10361-120">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="10361-120">-ExpiryTime</span></span>
<span data-ttu-id="10361-121">Anger den tid då den delade åtkomst-signaturen blir ogiltig.</span><span class="sxs-lookup"><span data-stu-id="10361-121">Specifies the time at which the shared access signature becomes invalid.</span></span>

<span data-ttu-id="10361-122">Om användaren anger start tiden men inte utgångs tiden, anges start tiden plus en timme.</span><span class="sxs-lookup"><span data-stu-id="10361-122">If the user sets the start time but not the expiry time, the expiry time is set to the start time plus one hour.</span></span>
<span data-ttu-id="10361-123">Om varken start tiden eller utgångs tiden har angetts anges den aktuella tiden plus en timme.</span><span class="sxs-lookup"><span data-stu-id="10361-123">If neither the start time nor the expiry time is specified, the expiry time is set to the current time plus one hour.</span></span>

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

### <span data-ttu-id="10361-124">-FullUri</span><span class="sxs-lookup"><span data-stu-id="10361-124">-FullUri</span></span>
<span data-ttu-id="10361-125">Anger att denna cmdlet returnerar full BLOB URI och signatur för delad åtkomst.</span><span class="sxs-lookup"><span data-stu-id="10361-125">Indicates that this cmdlet return the full blob URI and the shared access signature token.</span></span>

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

### <span data-ttu-id="10361-126">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="10361-126">-IPAddressOrRange</span></span>
<span data-ttu-id="10361-127">Anger IP-adressen eller intervallet med IP-adresser som begär Anden ska accepteras från, till exempel 168.1.5.65 eller 168.1.5.60-168.1.5.70.</span><span class="sxs-lookup"><span data-stu-id="10361-127">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="10361-128">Intervallet är inkluderat.</span><span class="sxs-lookup"><span data-stu-id="10361-128">The range is inclusive.</span></span>

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

### <span data-ttu-id="10361-129">-Namn</span><span class="sxs-lookup"><span data-stu-id="10361-129">-Name</span></span>
<span data-ttu-id="10361-130">Anger ett namn på en Azure-lagringsenhet.</span><span class="sxs-lookup"><span data-stu-id="10361-130">Specifies an Azure storage container name.</span></span>

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

### <span data-ttu-id="10361-131">-Tillstånd</span><span class="sxs-lookup"><span data-stu-id="10361-131">-Permission</span></span>
<span data-ttu-id="10361-132">Anger behörigheter för en lagrings behållare.</span><span class="sxs-lookup"><span data-stu-id="10361-132">Specifies permissions for a storage container.</span></span>

```yaml
Type: String
Parameter Sets: SasPermission
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10361-133">-Princip</span><span class="sxs-lookup"><span data-stu-id="10361-133">-Policy</span></span>
<span data-ttu-id="10361-134">Anger en åtkomst policy för Azure.</span><span class="sxs-lookup"><span data-stu-id="10361-134">Specifies an Azure Stored Access Policy.</span></span>

```yaml
Type: String
Parameter Sets: SasPolicy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10361-135">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="10361-135">-Protocol</span></span>
<span data-ttu-id="10361-136">Anger det protokoll som tillåts för en begäran.</span><span class="sxs-lookup"><span data-stu-id="10361-136">Specifies the protocol permitted for a request.</span></span>
<span data-ttu-id="10361-137">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="10361-137">The acceptable values for this parameter are:</span></span>
* <span data-ttu-id="10361-138">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="10361-138">HttpsOnly</span></span>
* <span data-ttu-id="10361-139">HttpsOrHttp</span><span class="sxs-lookup"><span data-stu-id="10361-139">HttpsOrHttp</span></span>

<span data-ttu-id="10361-140">Standardvärdet är HttpsOrHttp.</span><span class="sxs-lookup"><span data-stu-id="10361-140">The default value is HttpsOrHttp.</span></span>

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

### <span data-ttu-id="10361-141">-StartTime</span><span class="sxs-lookup"><span data-stu-id="10361-141">-StartTime</span></span>
<span data-ttu-id="10361-142">Anger den tid då den delade Access-signaturen blir giltig.</span><span class="sxs-lookup"><span data-stu-id="10361-142">Specifies the time at which the shared access signature becomes valid.</span></span>

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

### <span data-ttu-id="10361-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10361-143">CommonParameters</span></span>
<span data-ttu-id="10361-144">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="10361-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10361-145">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="10361-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10361-146">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="10361-146">INPUTS</span></span>

### <span data-ttu-id="10361-147">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="10361-147">IStorageContext</span></span>

<span data-ttu-id="10361-148">Parametern ' context ' godkänner värdet av typen ' IStorageContext ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="10361-148">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="10361-149">Strängvärdet</span><span class="sxs-lookup"><span data-stu-id="10361-149">String</span></span>

<span data-ttu-id="10361-150">Parametern "name" accepterar värdet för typen String från pipeline</span><span class="sxs-lookup"><span data-stu-id="10361-150">Parameter 'Name' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="10361-151">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="10361-151">OUTPUTS</span></span>

### <span data-ttu-id="10361-152">System. String</span><span class="sxs-lookup"><span data-stu-id="10361-152">System.String</span></span>

## <span data-ttu-id="10361-153">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="10361-153">NOTES</span></span>

## <span data-ttu-id="10361-154">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="10361-154">RELATED LINKS</span></span>

[<span data-ttu-id="10361-155">New-AzureStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="10361-155">New-AzureStorageBlobSASToken</span></span>](./New-AzureStorageBlobSASToken.md)