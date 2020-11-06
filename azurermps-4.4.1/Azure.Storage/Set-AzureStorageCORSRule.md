---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 288B7B56-B934-45AF-BF56-4EB0DD827522
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageCORSRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageCORSRule.md
gitcommit: https://github.com/Azure/azure-powershell/blob/1fa63f743120d7a7cd6cbb28ee43cd0f4c654af9
ms.openlocfilehash: 9b3bc0f9a0d0345662f63ef8387239e0792057e3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93583935"
---
# <span data-ttu-id="5bf28-101">Set-AzureStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="5bf28-101">Set-AzureStorageCORSRule</span></span>

## <span data-ttu-id="5bf28-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5bf28-102">SYNOPSIS</span></span>
<span data-ttu-id="5bf28-103">Anger CORS-regler för en typ av lagrings tjänst.</span><span class="sxs-lookup"><span data-stu-id="5bf28-103">Sets the CORS rules for a type of Storage service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5bf28-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5bf28-104">SYNTAX</span></span>

```
Set-AzureStorageCORSRule [-ServiceType] <StorageServiceType> -CorsRules <PSCorsRule[]> [-PassThru]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="5bf28-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5bf28-105">DESCRIPTION</span></span>
<span data-ttu-id="5bf28-106">Cmdleten **set-AzureStorageCORSRule** anger CORS-regler för en typ av Azure Storage service.</span><span class="sxs-lookup"><span data-stu-id="5bf28-106">The **Set-AzureStorageCORSRule** cmdlet sets the Cross-Origin Resource Sharing (CORS) rules for a type of Azure Storage service.</span></span>
<span data-ttu-id="5bf28-107">Typerna av lagrings tjänster för denna cmdlet är BLOB, tabell, kö och fil.</span><span class="sxs-lookup"><span data-stu-id="5bf28-107">The types of storage services for this cmdlet are Blob, Table, Queue, and File.</span></span>
<span data-ttu-id="5bf28-108">Denna cmdlet skriver över de befintliga reglerna.</span><span class="sxs-lookup"><span data-stu-id="5bf28-108">This cmdlet overwrites the existing rules.</span></span>
<span data-ttu-id="5bf28-109">Om du vill se de aktuella reglerna kan du använda Get-AzureStorageCORSRule cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5bf28-109">To see the current rules, use the Get-AzureStorageCORSRule cmdlet.</span></span>

## <span data-ttu-id="5bf28-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5bf28-110">EXAMPLES</span></span>

### <span data-ttu-id="5bf28-111">Exempel 1: tilldela CORS-regler till Blob-tjänsten</span><span class="sxs-lookup"><span data-stu-id="5bf28-111">Example 1: Assign CORS rules to the blob service</span></span>
```
PS C:\>$CorsRules = (@{
    AllowedHeaders=@("x-ms-blob-content-type","x-ms-blob-content-disposition");
    AllowedOrigins=@("*");
    MaxAgeInSeconds=30;
    AllowedMethods=@("Get","Connect")},
    @{
    AllowedOrigins=@("http://www.fabrikam.com","http://www.contoso.com"); 
    ExposedHeaders=@("x-ms-meta-data*","x-ms-meta-customheader"); 
    AllowedHeaders=@("x-ms-meta-target*","x-ms-meta-customheader");
    MaxAgeInSeconds=30;
    AllowedMethods=@("Put")})
PS C:\> Set-AzureStorageCORSRule -ServiceType Blob -CorsRules $CorsRules
```

<span data-ttu-id="5bf28-112">Det första kommandot tilldelar en uppsättning regler till $CorsRules variabel.</span><span class="sxs-lookup"><span data-stu-id="5bf28-112">The first command assigns an array of rules to the $CorsRules variable.</span></span>
<span data-ttu-id="5bf28-113">Det här kommandot använder standarden utökas över flera rader i det här blocket.</span><span class="sxs-lookup"><span data-stu-id="5bf28-113">This command uses standard extends over several lines in this code block.</span></span>

<span data-ttu-id="5bf28-114">Det andra kommandot tilldelar reglerna i $CorsRules till typen blob-tjänst.</span><span class="sxs-lookup"><span data-stu-id="5bf28-114">The second command assigns the rules in $CorsRules to the Blob service type.</span></span>

### <span data-ttu-id="5bf28-115">Exempel 2: ändra egenskaper för en CORS-regel för Blob-tjänsten</span><span class="sxs-lookup"><span data-stu-id="5bf28-115">Example 2: Change properties of a CORS rule for blob service</span></span>
```
PS C:\>$CorsRules = Get-AzureStorageCORSRule -ServiceType Blob
PS C:\> $CorsRules[0].AllowedHeaders = @("x-ms-blob-content-type", "x-ms-blob-content-disposition")
PS C:\> $CorsRules[0].AllowedMethods = @("Get", "Connect", "Merge")
PS C:\> Set-AzureStorageCORSRule -ServiceType Blob -CorsRules $CorsRules
```

<span data-ttu-id="5bf28-116">Det första kommandot får de aktuella CORS-reglerna för BLOB-typen genom att använda cmdleten **Get-AzureStorageCORSRule** .</span><span class="sxs-lookup"><span data-stu-id="5bf28-116">The first command gets the current CORS rules for the Blob type by using the **Get-AzureStorageCORSRule** cmdlet.</span></span>
<span data-ttu-id="5bf28-117">Kommandot lagrar reglerna i $CorsRules mat ris variabel.</span><span class="sxs-lookup"><span data-stu-id="5bf28-117">The command stores the rules in the $CorsRules array variable.</span></span>

<span data-ttu-id="5bf28-118">Det andra och tredje kommandot ändrar den första regeln i $CorsRules.</span><span class="sxs-lookup"><span data-stu-id="5bf28-118">The second and third commands modify the first rule in $CorsRules.</span></span>

<span data-ttu-id="5bf28-119">Det sista kommandot tilldelar reglerna i $CorsRules till typen blob-tjänst.</span><span class="sxs-lookup"><span data-stu-id="5bf28-119">The final command assigns the rules in $CorsRules to the Blob service type.</span></span>
<span data-ttu-id="5bf28-120">De reviderade reglerna ersätter de aktuella CORS-reglerna.</span><span class="sxs-lookup"><span data-stu-id="5bf28-120">The revised rules overwrite the current CORS rules.</span></span>

## <span data-ttu-id="5bf28-121">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5bf28-121">PARAMETERS</span></span>

### <span data-ttu-id="5bf28-122">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="5bf28-122">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="5bf28-123">Anger tids gräns för klient sidan, i sekunder, för en tjänst förfrågan.</span><span class="sxs-lookup"><span data-stu-id="5bf28-123">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="5bf28-124">Om det föregående samtalet inte fungerar under det angivna intervallet, försöker den här cmdleten igen.</span><span class="sxs-lookup"><span data-stu-id="5bf28-124">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="5bf28-125">Om denna cmdlet inte får ett lyckat svar innan intervallet går ut returneras ett fel.</span><span class="sxs-lookup"><span data-stu-id="5bf28-125">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5bf28-126">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="5bf28-126">-ConcurrentTaskCount</span></span>
<span data-ttu-id="5bf28-127">Anger maximalt antal samtidiga nätverks samtal.</span><span class="sxs-lookup"><span data-stu-id="5bf28-127">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="5bf28-128">Du kan använda den här parametern för att begränsa samtidigheten för att reglera den lokala processorn och bandbredds användning genom att ange det maximala antalet simultana nätverks samtal.</span><span class="sxs-lookup"><span data-stu-id="5bf28-128">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="5bf28-129">Det angivna värdet är ett absolut antal och multipliceras inte med antalet kärnor.</span><span class="sxs-lookup"><span data-stu-id="5bf28-129">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="5bf28-130">Den här parametern kan hjälpa till att minska nätverks anslutnings problem i miljöer med liten bandbredd, till exempel 100 kilobit per sekund.</span><span class="sxs-lookup"><span data-stu-id="5bf28-130">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="5bf28-131">Standardvärdet är 10.</span><span class="sxs-lookup"><span data-stu-id="5bf28-131">The default value is 10.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5bf28-132">-Kontext</span><span class="sxs-lookup"><span data-stu-id="5bf28-132">-Context</span></span>
<span data-ttu-id="5bf28-133">Anger en Azure Storage-kontext.</span><span class="sxs-lookup"><span data-stu-id="5bf28-133">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="5bf28-134">Använd New-AzureStorageContext cmdlet för att få en kontext.</span><span class="sxs-lookup"><span data-stu-id="5bf28-134">To obtain a context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="5bf28-135">-CorsRules</span><span class="sxs-lookup"><span data-stu-id="5bf28-135">-CorsRules</span></span>
<span data-ttu-id="5bf28-136">Anger en matris med CORS-regler.</span><span class="sxs-lookup"><span data-stu-id="5bf28-136">Specifies an array of CORS rules.</span></span>
<span data-ttu-id="5bf28-137">Du kan hämta befintliga regler med hjälp av Get-AzureStorageCORSRule cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5bf28-137">You can retrieve the existing rules using the Get-AzureStorageCORSRule cmdlet.</span></span>

```yaml
Type: PSCorsRule[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5bf28-138">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5bf28-138">-PassThru</span></span>
<span data-ttu-id="5bf28-139">Anger att denna cmdlet returnerar ett booleskt värde som visar att åtgärden lyckades.</span><span class="sxs-lookup"><span data-stu-id="5bf28-139">Indicates that this cmdlet returns a Boolean that reflects the success of the operation.</span></span>
<span data-ttu-id="5bf28-140">Denna cmdlet returnerar som standard inget värde.</span><span class="sxs-lookup"><span data-stu-id="5bf28-140">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="5bf28-141">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="5bf28-141">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="5bf28-142">Anger längden på tids gränsen för en server del av en begäran.</span><span class="sxs-lookup"><span data-stu-id="5bf28-142">Specifies the length of the time-out period for the server part of a request.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5bf28-143">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="5bf28-143">-ServiceType</span></span>
<span data-ttu-id="5bf28-144">Anger typen för Azure Storage-tjänsten för vilken denna cmdlet tilldelar regler.</span><span class="sxs-lookup"><span data-stu-id="5bf28-144">Specifies the Azure Storage service type for which this cmdlet assigns rules.</span></span>
<span data-ttu-id="5bf28-145">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="5bf28-145">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="5bf28-146">Object</span><span class="sxs-lookup"><span data-stu-id="5bf28-146">Blob</span></span> 
- <span data-ttu-id="5bf28-147">Tabell</span><span class="sxs-lookup"><span data-stu-id="5bf28-147">Table</span></span> 
- <span data-ttu-id="5bf28-148">Svarskö</span><span class="sxs-lookup"><span data-stu-id="5bf28-148">Queue</span></span> 
- <span data-ttu-id="5bf28-149">Fil</span><span class="sxs-lookup"><span data-stu-id="5bf28-149">File</span></span>

```yaml
Type: StorageServiceType
Parameter Sets: (All)
Aliases: 
Accepted values: Blob, Table, Queue, File

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5bf28-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5bf28-150">CommonParameters</span></span>
<span data-ttu-id="5bf28-151">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5bf28-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5bf28-152">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5bf28-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5bf28-153">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5bf28-153">INPUTS</span></span>

### <span data-ttu-id="5bf28-154">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="5bf28-154">IStorageContext</span></span>

<span data-ttu-id="5bf28-155">Parametern ' context ' godkänner värdet av typen ' IStorageContext ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="5bf28-155">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

## <span data-ttu-id="5bf28-156">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5bf28-156">OUTPUTS</span></span>

### <span data-ttu-id="5bf28-157">Microsoft. WindowsAzure. commands. Storage. Model. ResourceModel. PSCorsRule</span><span class="sxs-lookup"><span data-stu-id="5bf28-157">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSCorsRule</span></span>

## <span data-ttu-id="5bf28-158">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5bf28-158">NOTES</span></span>

## <span data-ttu-id="5bf28-159">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5bf28-159">RELATED LINKS</span></span>

[<span data-ttu-id="5bf28-160">Get-AzureStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="5bf28-160">Get-AzureStorageCORSRule</span></span>](./Get-AzureStorageCORSRule.md)

[<span data-ttu-id="5bf28-161">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="5bf28-161">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="5bf28-162">Remove-AzureStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="5bf28-162">Remove-AzureStorageCORSRule</span></span>](./Remove-AzureStorageCORSRule.md)


