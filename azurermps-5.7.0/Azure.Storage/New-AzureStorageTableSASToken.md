---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 3CFA6E31-E243-4B22-AE8F-1942DD324639
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/new-azurestoragetablesastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageTableSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageTableSASToken.md
ms.openlocfilehash: 76ed7737acb26cd713aa84b26a743f3e5e43874f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93755894"
---
# <span data-ttu-id="3c096-101">New-AzureStorageTableSASToken</span><span class="sxs-lookup"><span data-stu-id="3c096-101">New-AzureStorageTableSASToken</span></span>

## <span data-ttu-id="3c096-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3c096-102">SYNOPSIS</span></span>
<span data-ttu-id="3c096-103">Skapar en SAS-token för en Azure Storage-tabell.</span><span class="sxs-lookup"><span data-stu-id="3c096-103">Generates an SAS token for an Azure Storage table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3c096-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3c096-104">SYNTAX</span></span>

### <span data-ttu-id="3c096-105">SasPolicy</span><span class="sxs-lookup"><span data-stu-id="3c096-105">SasPolicy</span></span>
```
New-AzureStorageTableSASToken [-Name] <String> -Policy <String> [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-StartPartitionKey <String>] [-StartRowKey <String>] [-EndPartitionKey <String>] [-EndRowKey <String>]
 [-Context <IStorageContext>] [<CommonParameters>]
```

### <span data-ttu-id="3c096-106">SasPermission</span><span class="sxs-lookup"><span data-stu-id="3c096-106">SasPermission</span></span>
```
New-AzureStorageTableSASToken [-Name] <String> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-StartPartitionKey <String>] [-StartRowKey <String>] [-EndPartitionKey <String>] [-EndRowKey <String>]
 [-Context <IStorageContext>] [<CommonParameters>]
```

## <span data-ttu-id="3c096-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3c096-107">DESCRIPTION</span></span>
<span data-ttu-id="3c096-108">**New-AzureStorageTableSASToken** cmdlet skapar en SAS-token (Shared Access signatur) för en Azure Storage-tabell.</span><span class="sxs-lookup"><span data-stu-id="3c096-108">The **New-AzureStorageTableSASToken** cmdlet generates a Shared Access Signature (SAS) token for an Azure Storage table.</span></span>

## <span data-ttu-id="3c096-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3c096-109">EXAMPLES</span></span>

### <span data-ttu-id="3c096-110">Exempel 1: skapa en SAS-token som har fullständig behörighet för en tabell</span><span class="sxs-lookup"><span data-stu-id="3c096-110">Example 1: Generate an SAS token that has full permissions for a table</span></span>
```
C:\PS>New-AzureStorageTableSASToken -Name "ContosoResources" -Permission "raud"
```

<span data-ttu-id="3c096-111">Det här kommandot skapar en SAS-token med fullständig behörighet för tabellen med namnet ContosoResources.</span><span class="sxs-lookup"><span data-stu-id="3c096-111">This command generates an SAS token with full permissions for the table named ContosoResources.</span></span>
<span data-ttu-id="3c096-112">Denna token är för läsa, lägga till, uppdatera och ta bort behörigheter.</span><span class="sxs-lookup"><span data-stu-id="3c096-112">That token is for read, add, update, and delete permissions.</span></span>

### <span data-ttu-id="3c096-113">Exempel 2: skapa en SAS-token för ett stort antal partitioner</span><span class="sxs-lookup"><span data-stu-id="3c096-113">Example 2: Generate an SAS token for a range of partitions</span></span>
```
C:\PS>New-AzureStorageTableSASToken -Name "ContosoResources" -Permission "raud" -StartPartitionKey "a" -EndPartitionKey "b"
```

<span data-ttu-id="3c096-114">Det här kommandot genererar och SAS-token med fullständig behörighet för tabellen med namnet ContosoResources.</span><span class="sxs-lookup"><span data-stu-id="3c096-114">This command generates and SAS token with full permissions for the table named ContosoResources.</span></span>
<span data-ttu-id="3c096-115">Kommandot begränsar token till det område som parametrarna för *StartPartitionKey* och *EndPartitionKey* anger.</span><span class="sxs-lookup"><span data-stu-id="3c096-115">The command limits the token to the range that the *StartPartitionKey* and *EndPartitionKey* parameters specify.</span></span>

### <span data-ttu-id="3c096-116">Exempel 3: skapa en SAS-token som har en lagrad åtkomst princip för en tabell</span><span class="sxs-lookup"><span data-stu-id="3c096-116">Example 3: Generate an SAS token that has a stored access policy for a table</span></span>
```
C:\PS>New-AzureStorageTableSASToken -Name "ContosoResources" -Policy "ClientPolicy01"
```

<span data-ttu-id="3c096-117">Det här kommandot skapar en SAS-token för tabellen med namnet ContosoResources.</span><span class="sxs-lookup"><span data-stu-id="3c096-117">This command generates an SAS token for the table named ContosoResources.</span></span>
<span data-ttu-id="3c096-118">Kommandot anger den lagrade åtkomst principen med namnet ClientPolicy01.</span><span class="sxs-lookup"><span data-stu-id="3c096-118">The command specifies the stored access policy named ClientPolicy01.</span></span>

## <span data-ttu-id="3c096-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3c096-119">PARAMETERS</span></span>

### <span data-ttu-id="3c096-120">-Kontext</span><span class="sxs-lookup"><span data-stu-id="3c096-120">-Context</span></span>
<span data-ttu-id="3c096-121">Anger en Azure Storage-kontext.</span><span class="sxs-lookup"><span data-stu-id="3c096-121">Specifies an Azure storage context.</span></span>
<span data-ttu-id="3c096-122">Använd New-AzureStorageContext cmdlet för att få en lagrings kontext.</span><span class="sxs-lookup"><span data-stu-id="3c096-122">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="3c096-123">-EndPartitionKey</span><span class="sxs-lookup"><span data-stu-id="3c096-123">-EndPartitionKey</span></span>
<span data-ttu-id="3c096-124">Anger partitionsfunktionen för slutet av intervallet för den token som denna cmdlet skapar.</span><span class="sxs-lookup"><span data-stu-id="3c096-124">Specifies the partition key of the end of the range for the token that this cmdlet creates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: endpk

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c096-125">-EndRowKey</span><span class="sxs-lookup"><span data-stu-id="3c096-125">-EndRowKey</span></span>
<span data-ttu-id="3c096-126">Anger rad nyckeln för slutet av intervallet för den token som denna cmdlet skapar.</span><span class="sxs-lookup"><span data-stu-id="3c096-126">Specifies the row key for the end of the range for the token that this cmdlet creates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: endrk

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c096-127">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="3c096-127">-ExpiryTime</span></span>
<span data-ttu-id="3c096-128">Anger när SAS-token upphör att gälla.</span><span class="sxs-lookup"><span data-stu-id="3c096-128">Specifies when the SAS token expires.</span></span>

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

### <span data-ttu-id="3c096-129">-FullUri</span><span class="sxs-lookup"><span data-stu-id="3c096-129">-FullUri</span></span>
<span data-ttu-id="3c096-130">Anger att denna cmdlet returnerar den fullständiga köns URI: n med SAS-token.</span><span class="sxs-lookup"><span data-stu-id="3c096-130">Indicates that this cmdlet returns the full queue URI with the SAS token.</span></span>

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

### <span data-ttu-id="3c096-131">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="3c096-131">-IPAddressOrRange</span></span>
<span data-ttu-id="3c096-132">Anger IP-adressen eller intervallet med IP-adresser som begär Anden ska accepteras från, till exempel 168.1.5.65 eller 168.1.5.60-168.1.5.70.</span><span class="sxs-lookup"><span data-stu-id="3c096-132">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="3c096-133">Intervallet är inkluderat.</span><span class="sxs-lookup"><span data-stu-id="3c096-133">The range is inclusive.</span></span>

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

### <span data-ttu-id="3c096-134">-Namn</span><span class="sxs-lookup"><span data-stu-id="3c096-134">-Name</span></span>
<span data-ttu-id="3c096-135">Anger namnet på en Azure Storage-tabell.</span><span class="sxs-lookup"><span data-stu-id="3c096-135">Specifies the name of an Azure Storage table.</span></span>
<span data-ttu-id="3c096-136">Denna cmdlet skapar en SAS-token för tabellen som anges av den här parametern.</span><span class="sxs-lookup"><span data-stu-id="3c096-136">This cmdlet creates an SAS token for the table that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, Table

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3c096-137">-Tillstånd</span><span class="sxs-lookup"><span data-stu-id="3c096-137">-Permission</span></span>
<span data-ttu-id="3c096-138">Anger behörigheter för en Azure Storage-tabell.</span><span class="sxs-lookup"><span data-stu-id="3c096-138">Specifies permissions for an Azure Storage table.</span></span>

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

### <span data-ttu-id="3c096-139">-Princip</span><span class="sxs-lookup"><span data-stu-id="3c096-139">-Policy</span></span>
<span data-ttu-id="3c096-140">Anger en lagrad åtkomst princip som innehåller behörigheter för denna SAS-token.</span><span class="sxs-lookup"><span data-stu-id="3c096-140">Specifies a stored access policy, which includes the permissions for this SAS token.</span></span>

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

### <span data-ttu-id="3c096-141">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="3c096-141">-Protocol</span></span>
<span data-ttu-id="3c096-142">Anger det protokoll som tillåts för en begäran.</span><span class="sxs-lookup"><span data-stu-id="3c096-142">Specifies the protocol permitted for a request.</span></span>
<span data-ttu-id="3c096-143">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="3c096-143">The acceptable values for this parameter are:</span></span>
* <span data-ttu-id="3c096-144">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="3c096-144">HttpsOnly</span></span>
* <span data-ttu-id="3c096-145">HttpsOrHttp</span><span class="sxs-lookup"><span data-stu-id="3c096-145">HttpsOrHttp</span></span>

<span data-ttu-id="3c096-146">Standardvärdet är HttpsOrHttp.</span><span class="sxs-lookup"><span data-stu-id="3c096-146">The default value is HttpsOrHttp.</span></span>

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

### <span data-ttu-id="3c096-147">-StartPartitionKey</span><span class="sxs-lookup"><span data-stu-id="3c096-147">-StartPartitionKey</span></span>
<span data-ttu-id="3c096-148">Anger partitionstypen för början av intervallet för den token som denna cmdlet skapar.</span><span class="sxs-lookup"><span data-stu-id="3c096-148">Specifies the partition key of the start of the range for the token that this cmdlet creates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: startpk

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c096-149">-StartRowKey</span><span class="sxs-lookup"><span data-stu-id="3c096-149">-StartRowKey</span></span>
<span data-ttu-id="3c096-150">Anger rad nyckeln för början av intervallet för den token som denna cmdlet skapar.</span><span class="sxs-lookup"><span data-stu-id="3c096-150">Specifies the row key for the start of the range for the token that this cmdlet creates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: startrk

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c096-151">-StartTime</span><span class="sxs-lookup"><span data-stu-id="3c096-151">-StartTime</span></span>
<span data-ttu-id="3c096-152">Anger när SAS-token blir giltiga.</span><span class="sxs-lookup"><span data-stu-id="3c096-152">Specifies when the SAS token becomes valid.</span></span>

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

### <span data-ttu-id="3c096-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c096-153">CommonParameters</span></span>
<span data-ttu-id="3c096-154">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3c096-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c096-155">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3c096-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c096-156">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3c096-156">INPUTS</span></span>

### <span data-ttu-id="3c096-157">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="3c096-157">IStorageContext</span></span>

<span data-ttu-id="3c096-158">Parametern ' context ' godkänner värdet av typen ' IStorageContext ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="3c096-158">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="3c096-159">Strängvärdet</span><span class="sxs-lookup"><span data-stu-id="3c096-159">String</span></span>

<span data-ttu-id="3c096-160">Parametern "name" accepterar värdet för typen String från pipeline</span><span class="sxs-lookup"><span data-stu-id="3c096-160">Parameter 'Name' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="3c096-161">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3c096-161">OUTPUTS</span></span>

### <span data-ttu-id="3c096-162">System. String</span><span class="sxs-lookup"><span data-stu-id="3c096-162">System.String</span></span>

## <span data-ttu-id="3c096-163">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3c096-163">NOTES</span></span>

## <span data-ttu-id="3c096-164">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3c096-164">RELATED LINKS</span></span>

[<span data-ttu-id="3c096-165">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="3c096-165">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)
