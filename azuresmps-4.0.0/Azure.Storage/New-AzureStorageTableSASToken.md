---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 3CFA6E31-E243-4B22-AE8F-1942DD324639
online version: ''
schema: 2.0.0
ms.openlocfilehash: 39870fe9fe9ac4223bccf15908c960db29d25252
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93572536"
---
# <span data-ttu-id="01e13-101">New-AzureStorageTableSASToken</span><span class="sxs-lookup"><span data-stu-id="01e13-101">New-AzureStorageTableSASToken</span></span>

## <span data-ttu-id="01e13-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="01e13-102">SYNOPSIS</span></span>
<span data-ttu-id="01e13-103">Skapar en SAS-token för en Azure Storage-tabell.</span><span class="sxs-lookup"><span data-stu-id="01e13-103">Generates an SAS token for an Azure Storage table.</span></span>

## <span data-ttu-id="01e13-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="01e13-104">SYNTAX</span></span>

### <span data-ttu-id="01e13-105">SasPolicy</span><span class="sxs-lookup"><span data-stu-id="01e13-105">SasPolicy</span></span>
```
New-AzureStorageTableSASToken [-Name] <String> -Policy <String> [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-StartPartitionKey <String>] [-StartRowKey <String>] [-EndPartitionKey <String>] [-EndRowKey <String>]
 [-Context <IStorageContext>] [<CommonParameters>]
```

### <span data-ttu-id="01e13-106">SasPermission</span><span class="sxs-lookup"><span data-stu-id="01e13-106">SasPermission</span></span>
```
New-AzureStorageTableSASToken [-Name] <String> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-StartPartitionKey <String>] [-StartRowKey <String>] [-EndPartitionKey <String>] [-EndRowKey <String>]
 [-Context <IStorageContext>] [<CommonParameters>]
```

## <span data-ttu-id="01e13-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="01e13-107">DESCRIPTION</span></span>
<span data-ttu-id="01e13-108">**New-AzureStorageTableSASToken** cmdlet skapar en SAS-token (Shared Access signatur) för en Azure Storage-tabell.</span><span class="sxs-lookup"><span data-stu-id="01e13-108">The **New-AzureStorageTableSASToken** cmdlet generates a Shared Access Signature (SAS) token for an Azure Storage table.</span></span>

## <span data-ttu-id="01e13-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="01e13-109">EXAMPLES</span></span>

### <span data-ttu-id="01e13-110">Exempel 1: skapa en SAS-token som har fullständig behörighet för en tabell</span><span class="sxs-lookup"><span data-stu-id="01e13-110">Example 1: Generate an SAS token that has full permissions for a table</span></span>
```
C:\PS>New-AzureStorageTableSASToken -Name "ContosoResources" -Permission "raud"
```

<span data-ttu-id="01e13-111">Det här kommandot skapar en SAS-token med fullständig behörighet för tabellen med namnet ContosoResources.</span><span class="sxs-lookup"><span data-stu-id="01e13-111">This command generates an SAS token with full permissions for the table named ContosoResources.</span></span>
<span data-ttu-id="01e13-112">Denna token är för läsa, lägga till, uppdatera och ta bort behörigheter.</span><span class="sxs-lookup"><span data-stu-id="01e13-112">That token is for read, add, update, and delete permissions.</span></span>

### <span data-ttu-id="01e13-113">Exempel 2: skapa en SAS-token för ett stort antal partitioner</span><span class="sxs-lookup"><span data-stu-id="01e13-113">Example 2: Generate an SAS token for a range of partitions</span></span>
```
C:\PS>New-AzureStorageTableSASToken -Name "ContosoResources" -Permission "raud" -StartPartitionKey "a" -EndPartitionKey "b"
```

<span data-ttu-id="01e13-114">Det här kommandot genererar och SAS-token med fullständig behörighet för tabellen med namnet ContosoResources.</span><span class="sxs-lookup"><span data-stu-id="01e13-114">This command generates and SAS token with full permissions for the table named ContosoResources.</span></span>
<span data-ttu-id="01e13-115">Kommandot begränsar token till det område som parametrarna för *StartPartitionKey* och *EndPartitionKey* anger.</span><span class="sxs-lookup"><span data-stu-id="01e13-115">The command limits the token to the range that the *StartPartitionKey* and *EndPartitionKey* parameters specify.</span></span>

### <span data-ttu-id="01e13-116">Exempel 3: skapa en SAS-token som har en lagrad åtkomst princip för en tabell</span><span class="sxs-lookup"><span data-stu-id="01e13-116">Example 3: Generate an SAS token that has a stored access policy for a table</span></span>
```
C:\PS>New-AzureStorageTableSASToken -Name "ContosoResources" -Policy "ClientPolicy01"
```

<span data-ttu-id="01e13-117">Det här kommandot skapar en SAS-token för tabellen med namnet ContosoResources.</span><span class="sxs-lookup"><span data-stu-id="01e13-117">This command generates an SAS token for the table named ContosoResources.</span></span>
<span data-ttu-id="01e13-118">Kommandot anger den lagrade åtkomst principen med namnet ClientPolicy01.</span><span class="sxs-lookup"><span data-stu-id="01e13-118">The command specifies the stored access policy named ClientPolicy01.</span></span>

## <span data-ttu-id="01e13-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="01e13-119">PARAMETERS</span></span>

### <span data-ttu-id="01e13-120">-Kontext</span><span class="sxs-lookup"><span data-stu-id="01e13-120">-Context</span></span>
<span data-ttu-id="01e13-121">Anger en Azure Storage-kontext.</span><span class="sxs-lookup"><span data-stu-id="01e13-121">Specifies an Azure storage context.</span></span>
<span data-ttu-id="01e13-122">Använd New-AzureStorageContext cmdlet för att få en lagrings kontext.</span><span class="sxs-lookup"><span data-stu-id="01e13-122">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="01e13-123">-EndPartitionKey</span><span class="sxs-lookup"><span data-stu-id="01e13-123">-EndPartitionKey</span></span>
<span data-ttu-id="01e13-124">Anger partitionsfunktionen för slutet av intervallet för den token som denna cmdlet skapar.</span><span class="sxs-lookup"><span data-stu-id="01e13-124">Specifies the partition key of the end of the range for the token that this cmdlet creates.</span></span>

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

### <span data-ttu-id="01e13-125">-EndRowKey</span><span class="sxs-lookup"><span data-stu-id="01e13-125">-EndRowKey</span></span>
<span data-ttu-id="01e13-126">Anger rad nyckeln för slutet av intervallet för den token som denna cmdlet skapar.</span><span class="sxs-lookup"><span data-stu-id="01e13-126">Specifies the row key for the end of the range for the token that this cmdlet creates.</span></span>

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

### <span data-ttu-id="01e13-127">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="01e13-127">-ExpiryTime</span></span>
<span data-ttu-id="01e13-128">Anger när SAS-token upphör att gälla.</span><span class="sxs-lookup"><span data-stu-id="01e13-128">Specifies when the SAS token expires.</span></span>

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

### <span data-ttu-id="01e13-129">-FullUri</span><span class="sxs-lookup"><span data-stu-id="01e13-129">-FullUri</span></span>
<span data-ttu-id="01e13-130">Anger att denna cmdlet returnerar den fullständiga köns URI: n med SAS-token.</span><span class="sxs-lookup"><span data-stu-id="01e13-130">Indicates that this cmdlet returns the full queue URI with the SAS token.</span></span>

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

### <span data-ttu-id="01e13-131">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="01e13-131">-IPAddressOrRange</span></span>
<span data-ttu-id="01e13-132">Anger IP-adressen eller intervallet med IP-adresser som begär Anden ska accepteras från, till exempel 168.1.5.65 eller 168.1.5.60-168.1.5.70.</span><span class="sxs-lookup"><span data-stu-id="01e13-132">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="01e13-133">Intervallet är inkluderat.</span><span class="sxs-lookup"><span data-stu-id="01e13-133">The range is inclusive.</span></span>

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

### <span data-ttu-id="01e13-134">-Namn</span><span class="sxs-lookup"><span data-stu-id="01e13-134">-Name</span></span>
<span data-ttu-id="01e13-135">Anger namnet på en Azure Storage-tabell.</span><span class="sxs-lookup"><span data-stu-id="01e13-135">Specifies the name of an Azure Storage table.</span></span>
<span data-ttu-id="01e13-136">Denna cmdlet skapar en SAS-token för tabellen som anges av den här parametern.</span><span class="sxs-lookup"><span data-stu-id="01e13-136">This cmdlet creates an SAS token for the table that this parameter specifies.</span></span>

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

### <span data-ttu-id="01e13-137">-Tillstånd</span><span class="sxs-lookup"><span data-stu-id="01e13-137">-Permission</span></span>
<span data-ttu-id="01e13-138">Anger behörigheter för en Azure Storage-tabell.</span><span class="sxs-lookup"><span data-stu-id="01e13-138">Specifies permissions for an Azure Storage table.</span></span>

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

### <span data-ttu-id="01e13-139">-Princip</span><span class="sxs-lookup"><span data-stu-id="01e13-139">-Policy</span></span>
<span data-ttu-id="01e13-140">Anger en lagrad åtkomst princip som innehåller behörigheter för denna SAS-token.</span><span class="sxs-lookup"><span data-stu-id="01e13-140">Specifies a stored access policy, which includes the permissions for this SAS token.</span></span>

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

### <span data-ttu-id="01e13-141">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="01e13-141">-Protocol</span></span>
<span data-ttu-id="01e13-142">Anger det protokoll som tillåts för en begäran.</span><span class="sxs-lookup"><span data-stu-id="01e13-142">Specifies the protocol permitted for a request.</span></span>
<span data-ttu-id="01e13-143">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="01e13-143">The acceptable values for this parameter are:</span></span>
* <span data-ttu-id="01e13-144">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="01e13-144">HttpsOnly</span></span>
* <span data-ttu-id="01e13-145">HttpsOrHttp</span><span class="sxs-lookup"><span data-stu-id="01e13-145">HttpsOrHttp</span></span>

<span data-ttu-id="01e13-146">Standardvärdet är HttpsOrHttp.</span><span class="sxs-lookup"><span data-stu-id="01e13-146">The default value is HttpsOrHttp.</span></span>

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

### <span data-ttu-id="01e13-147">-StartPartitionKey</span><span class="sxs-lookup"><span data-stu-id="01e13-147">-StartPartitionKey</span></span>
<span data-ttu-id="01e13-148">Anger partitionstypen för början av intervallet för den token som denna cmdlet skapar.</span><span class="sxs-lookup"><span data-stu-id="01e13-148">Specifies the partition key of the start of the range for the token that this cmdlet creates.</span></span>

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

### <span data-ttu-id="01e13-149">-StartRowKey</span><span class="sxs-lookup"><span data-stu-id="01e13-149">-StartRowKey</span></span>
<span data-ttu-id="01e13-150">Anger rad nyckeln för början av intervallet för den token som denna cmdlet skapar.</span><span class="sxs-lookup"><span data-stu-id="01e13-150">Specifies the row key for the start of the range for the token that this cmdlet creates.</span></span>

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

### <span data-ttu-id="01e13-151">-StartTime</span><span class="sxs-lookup"><span data-stu-id="01e13-151">-StartTime</span></span>
<span data-ttu-id="01e13-152">Anger när SAS-token blir giltiga.</span><span class="sxs-lookup"><span data-stu-id="01e13-152">Specifies when the SAS token becomes valid.</span></span>

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

### <span data-ttu-id="01e13-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01e13-153">CommonParameters</span></span>
<span data-ttu-id="01e13-154">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="01e13-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01e13-155">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="01e13-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01e13-156">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="01e13-156">INPUTS</span></span>

## <span data-ttu-id="01e13-157">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="01e13-157">OUTPUTS</span></span>

## <span data-ttu-id="01e13-158">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="01e13-158">NOTES</span></span>

## <span data-ttu-id="01e13-159">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="01e13-159">RELATED LINKS</span></span>

[<span data-ttu-id="01e13-160">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="01e13-160">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)
