---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: 3CFA6E31-E243-4B22-AE8F-1942DD324639
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/new-azurestoragetablesastoken
schema: 2.0.0
ms.openlocfilehash: 29c5cf9b48126d4b8544cf80ad6fa78acc51ae93
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93931566"
---
# <span data-ttu-id="2e943-101">New-AzureStorageTableSASToken</span><span class="sxs-lookup"><span data-stu-id="2e943-101">New-AzureStorageTableSASToken</span></span>

## <span data-ttu-id="2e943-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2e943-102">SYNOPSIS</span></span>
<span data-ttu-id="2e943-103">Skapar en SAS-token för en Azure Storage-tabell.</span><span class="sxs-lookup"><span data-stu-id="2e943-103">Generates an SAS token for an Azure Storage table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2e943-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2e943-104">SYNTAX</span></span>

### <span data-ttu-id="2e943-105">SasPolicy</span><span class="sxs-lookup"><span data-stu-id="2e943-105">SasPolicy</span></span>
```
New-AzureStorageTableSASToken [-Name] <String> -Policy <String> [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-StartPartitionKey <String>] [-StartRowKey <String>] [-EndPartitionKey <String>] [-EndRowKey <String>]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2e943-106">SasPermission</span><span class="sxs-lookup"><span data-stu-id="2e943-106">SasPermission</span></span>
```
New-AzureStorageTableSASToken [-Name] <String> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-StartPartitionKey <String>] [-StartRowKey <String>] [-EndPartitionKey <String>] [-EndRowKey <String>]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2e943-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2e943-107">DESCRIPTION</span></span>
<span data-ttu-id="2e943-108">**New-AzureStorageTableSASToken** cmdlet skapar en SAS-token (Shared Access signatur) för en Azure Storage-tabell.</span><span class="sxs-lookup"><span data-stu-id="2e943-108">The **New-AzureStorageTableSASToken** cmdlet generates a Shared Access Signature (SAS) token for an Azure Storage table.</span></span>

## <span data-ttu-id="2e943-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2e943-109">EXAMPLES</span></span>

### <span data-ttu-id="2e943-110">Exempel 1: skapa en SAS-token som har fullständig behörighet för en tabell</span><span class="sxs-lookup"><span data-stu-id="2e943-110">Example 1: Generate an SAS token that has full permissions for a table</span></span>
```
C:\PS>New-AzureStorageTableSASToken -Name "ContosoResources" -Permission "raud"
```

<span data-ttu-id="2e943-111">Det här kommandot skapar en SAS-token med fullständig behörighet för tabellen med namnet ContosoResources.</span><span class="sxs-lookup"><span data-stu-id="2e943-111">This command generates an SAS token with full permissions for the table named ContosoResources.</span></span>
<span data-ttu-id="2e943-112">Denna token är för läsa, lägga till, uppdatera och ta bort behörigheter.</span><span class="sxs-lookup"><span data-stu-id="2e943-112">That token is for read, add, update, and delete permissions.</span></span>

### <span data-ttu-id="2e943-113">Exempel 2: skapa en SAS-token för ett stort antal partitioner</span><span class="sxs-lookup"><span data-stu-id="2e943-113">Example 2: Generate an SAS token for a range of partitions</span></span>
```
C:\PS>New-AzureStorageTableSASToken -Name "ContosoResources" -Permission "raud" -StartPartitionKey "a" -EndPartitionKey "b"
```

<span data-ttu-id="2e943-114">Det här kommandot genererar och SAS-token med fullständig behörighet för tabellen med namnet ContosoResources.</span><span class="sxs-lookup"><span data-stu-id="2e943-114">This command generates and SAS token with full permissions for the table named ContosoResources.</span></span>
<span data-ttu-id="2e943-115">Kommandot begränsar token till det område som parametrarna för *StartPartitionKey* och *EndPartitionKey* anger.</span><span class="sxs-lookup"><span data-stu-id="2e943-115">The command limits the token to the range that the *StartPartitionKey* and *EndPartitionKey* parameters specify.</span></span>

### <span data-ttu-id="2e943-116">Exempel 3: skapa en SAS-token som har en lagrad åtkomst princip för en tabell</span><span class="sxs-lookup"><span data-stu-id="2e943-116">Example 3: Generate an SAS token that has a stored access policy for a table</span></span>
```
C:\PS>New-AzureStorageTableSASToken -Name "ContosoResources" -Policy "ClientPolicy01"
```

<span data-ttu-id="2e943-117">Det här kommandot skapar en SAS-token för tabellen med namnet ContosoResources.</span><span class="sxs-lookup"><span data-stu-id="2e943-117">This command generates an SAS token for the table named ContosoResources.</span></span>
<span data-ttu-id="2e943-118">Kommandot anger den lagrade åtkomst principen med namnet ClientPolicy01.</span><span class="sxs-lookup"><span data-stu-id="2e943-118">The command specifies the stored access policy named ClientPolicy01.</span></span>

## <span data-ttu-id="2e943-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2e943-119">PARAMETERS</span></span>

### <span data-ttu-id="2e943-120">-Kontext</span><span class="sxs-lookup"><span data-stu-id="2e943-120">-Context</span></span>
<span data-ttu-id="2e943-121">Anger en Azure Storage-kontext.</span><span class="sxs-lookup"><span data-stu-id="2e943-121">Specifies an Azure storage context.</span></span>
<span data-ttu-id="2e943-122">Använd New-AzureStorageContext cmdlet för att få en lagrings kontext.</span><span class="sxs-lookup"><span data-stu-id="2e943-122">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="2e943-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e943-123">-DefaultProfile</span></span>
<span data-ttu-id="2e943-124">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="2e943-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2e943-125">-EndPartitionKey</span><span class="sxs-lookup"><span data-stu-id="2e943-125">-EndPartitionKey</span></span>
<span data-ttu-id="2e943-126">Anger partitionsfunktionen för slutet av intervallet för den token som denna cmdlet skapar.</span><span class="sxs-lookup"><span data-stu-id="2e943-126">Specifies the partition key of the end of the range for the token that this cmdlet creates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: endpk

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e943-127">-EndRowKey</span><span class="sxs-lookup"><span data-stu-id="2e943-127">-EndRowKey</span></span>
<span data-ttu-id="2e943-128">Anger rad nyckeln för slutet av intervallet för den token som denna cmdlet skapar.</span><span class="sxs-lookup"><span data-stu-id="2e943-128">Specifies the row key for the end of the range for the token that this cmdlet creates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: endrk

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e943-129">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="2e943-129">-ExpiryTime</span></span>
<span data-ttu-id="2e943-130">Anger när SAS-token upphör att gälla.</span><span class="sxs-lookup"><span data-stu-id="2e943-130">Specifies when the SAS token expires.</span></span>

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

### <span data-ttu-id="2e943-131">-FullUri</span><span class="sxs-lookup"><span data-stu-id="2e943-131">-FullUri</span></span>
<span data-ttu-id="2e943-132">Anger att denna cmdlet returnerar den fullständiga köns URI: n med SAS-token.</span><span class="sxs-lookup"><span data-stu-id="2e943-132">Indicates that this cmdlet returns the full queue URI with the SAS token.</span></span>

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

### <span data-ttu-id="2e943-133">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="2e943-133">-IPAddressOrRange</span></span>
<span data-ttu-id="2e943-134">Anger IP-adressen eller intervallet med IP-adresser som begär Anden ska accepteras från, till exempel 168.1.5.65 eller 168.1.5.60-168.1.5.70.</span><span class="sxs-lookup"><span data-stu-id="2e943-134">Specifies the IP address or range of IP addresses from which to accept requests, such as 168.1.5.65 or 168.1.5.60-168.1.5.70.</span></span>
<span data-ttu-id="2e943-135">Intervallet är inkluderat.</span><span class="sxs-lookup"><span data-stu-id="2e943-135">The range is inclusive.</span></span>

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

### <span data-ttu-id="2e943-136">-Namn</span><span class="sxs-lookup"><span data-stu-id="2e943-136">-Name</span></span>
<span data-ttu-id="2e943-137">Anger namnet på en Azure Storage-tabell.</span><span class="sxs-lookup"><span data-stu-id="2e943-137">Specifies the name of an Azure Storage table.</span></span>
<span data-ttu-id="2e943-138">Denna cmdlet skapar en SAS-token för tabellen som anges av den här parametern.</span><span class="sxs-lookup"><span data-stu-id="2e943-138">This cmdlet creates an SAS token for the table that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Table

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2e943-139">-Tillstånd</span><span class="sxs-lookup"><span data-stu-id="2e943-139">-Permission</span></span>
<span data-ttu-id="2e943-140">Anger behörigheter för en Azure Storage-tabell.</span><span class="sxs-lookup"><span data-stu-id="2e943-140">Specifies permissions for an Azure Storage table.</span></span>
<span data-ttu-id="2e943-141">Det är viktigt att Observera att det här är en sträng, till exempel `rwd` (för läsning, skrivning och borttagning).</span><span class="sxs-lookup"><span data-stu-id="2e943-141">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

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

### <span data-ttu-id="2e943-142">-Princip</span><span class="sxs-lookup"><span data-stu-id="2e943-142">-Policy</span></span>
<span data-ttu-id="2e943-143">Anger en lagrad åtkomst princip som innehåller behörigheter för denna SAS-token.</span><span class="sxs-lookup"><span data-stu-id="2e943-143">Specifies a stored access policy, which includes the permissions for this SAS token.</span></span>

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

### <span data-ttu-id="2e943-144">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="2e943-144">-Protocol</span></span>
<span data-ttu-id="2e943-145">Anger det protokoll som tillåts för en begäran.</span><span class="sxs-lookup"><span data-stu-id="2e943-145">Specifies the protocol permitted for a request.</span></span>
<span data-ttu-id="2e943-146">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="2e943-146">The acceptable values for this parameter are:</span></span>
* <span data-ttu-id="2e943-147">HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="2e943-147">HttpsOnly</span></span>
* <span data-ttu-id="2e943-148">HttpsOrHttp standardvärdet är HttpsOrHttp.</span><span class="sxs-lookup"><span data-stu-id="2e943-148">HttpsOrHttp The default value is HttpsOrHttp.</span></span>

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

### <span data-ttu-id="2e943-149">-StartPartitionKey</span><span class="sxs-lookup"><span data-stu-id="2e943-149">-StartPartitionKey</span></span>
<span data-ttu-id="2e943-150">Anger partitionstypen för början av intervallet för den token som denna cmdlet skapar.</span><span class="sxs-lookup"><span data-stu-id="2e943-150">Specifies the partition key of the start of the range for the token that this cmdlet creates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: startpk

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e943-151">-StartRowKey</span><span class="sxs-lookup"><span data-stu-id="2e943-151">-StartRowKey</span></span>
<span data-ttu-id="2e943-152">Anger rad nyckeln för början av intervallet för den token som denna cmdlet skapar.</span><span class="sxs-lookup"><span data-stu-id="2e943-152">Specifies the row key for the start of the range for the token that this cmdlet creates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: startrk

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e943-153">-StartTime</span><span class="sxs-lookup"><span data-stu-id="2e943-153">-StartTime</span></span>
<span data-ttu-id="2e943-154">Anger när SAS-token blir giltiga.</span><span class="sxs-lookup"><span data-stu-id="2e943-154">Specifies when the SAS token becomes valid.</span></span>

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

### <span data-ttu-id="2e943-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e943-155">CommonParameters</span></span>
<span data-ttu-id="2e943-156">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2e943-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e943-157">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2e943-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e943-158">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2e943-158">INPUTS</span></span>

### <span data-ttu-id="2e943-159">System. String</span><span class="sxs-lookup"><span data-stu-id="2e943-159">System.String</span></span>

### <span data-ttu-id="2e943-160">Microsoft. Azure. commands. Common. verifikation. abstraktioner. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="2e943-160">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="2e943-161">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2e943-161">OUTPUTS</span></span>

### <span data-ttu-id="2e943-162">System. String</span><span class="sxs-lookup"><span data-stu-id="2e943-162">System.String</span></span>

## <span data-ttu-id="2e943-163">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2e943-163">NOTES</span></span>

## <span data-ttu-id="2e943-164">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2e943-164">RELATED LINKS</span></span>

[<span data-ttu-id="2e943-165">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="2e943-165">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)
