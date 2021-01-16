---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 288B7B56-B934-45AF-BF56-4EB0DD827522
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azstoragecorsrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageCORSRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageCORSRule.md
ms.openlocfilehash: d7951e53c7cbd8c799c7158bb3cc5c3fabb5b039
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98521978"
---
# <span data-ttu-id="6f96f-101">Set-AzStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="6f96f-101">Set-AzStorageCORSRule</span></span>

## <span data-ttu-id="6f96f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6f96f-102">SYNOPSIS</span></span>
<span data-ttu-id="6f96f-103">Anger CORS-regler för en typ av lagrings tjänst.</span><span class="sxs-lookup"><span data-stu-id="6f96f-103">Sets the CORS rules for a type of Storage service.</span></span>

## <span data-ttu-id="6f96f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6f96f-104">SYNTAX</span></span>

```
Set-AzStorageCORSRule [-ServiceType] <StorageServiceType> -CorsRules <PSCorsRule[]> [-PassThru]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="6f96f-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6f96f-105">DESCRIPTION</span></span>
<span data-ttu-id="6f96f-106">Cmdleten **set-AzStorageCORSRule** anger CORS-regler för en typ av Azure Storage service.</span><span class="sxs-lookup"><span data-stu-id="6f96f-106">The **Set-AzStorageCORSRule** cmdlet sets the Cross-Origin Resource Sharing (CORS) rules for a type of Azure Storage service.</span></span>
<span data-ttu-id="6f96f-107">Typerna av lagrings tjänster för denna cmdlet är BLOB, tabell, kö och fil.</span><span class="sxs-lookup"><span data-stu-id="6f96f-107">The types of storage services for this cmdlet are Blob, Table, Queue, and File.</span></span>
<span data-ttu-id="6f96f-108">Denna cmdlet skriver över de befintliga reglerna.</span><span class="sxs-lookup"><span data-stu-id="6f96f-108">This cmdlet overwrites the existing rules.</span></span>
<span data-ttu-id="6f96f-109">Om du vill se de aktuella reglerna kan du använda Get-AzStorageCORSRule cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6f96f-109">To see the current rules, use the Get-AzStorageCORSRule cmdlet.</span></span>

## <span data-ttu-id="6f96f-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6f96f-110">EXAMPLES</span></span>

### <span data-ttu-id="6f96f-111">Exempel 1: tilldela CORS-regler till Blob-tjänsten</span><span class="sxs-lookup"><span data-stu-id="6f96f-111">Example 1: Assign CORS rules to the blob service</span></span>
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
PS C:\> Set-AzStorageCORSRule -ServiceType Blob -CorsRules $CorsRules
```

<span data-ttu-id="6f96f-112">Det första kommandot tilldelar en uppsättning regler till $CorsRules variabel.</span><span class="sxs-lookup"><span data-stu-id="6f96f-112">The first command assigns an array of rules to the $CorsRules variable.</span></span>
<span data-ttu-id="6f96f-113">Det här kommandot använder standarden utökas över flera rader i det här blocket.</span><span class="sxs-lookup"><span data-stu-id="6f96f-113">This command uses standard extends over several lines in this code block.</span></span>
<span data-ttu-id="6f96f-114">Det andra kommandot tilldelar reglerna i $CorsRules till typen blob-tjänst.</span><span class="sxs-lookup"><span data-stu-id="6f96f-114">The second command assigns the rules in $CorsRules to the Blob service type.</span></span>

### <span data-ttu-id="6f96f-115">Exempel 2: ändra egenskaper för en CORS-regel för Blob-tjänsten</span><span class="sxs-lookup"><span data-stu-id="6f96f-115">Example 2: Change properties of a CORS rule for blob service</span></span>
```
PS C:\>$CorsRules = Get-AzStorageCORSRule -ServiceType Blob
PS C:\> $CorsRules[0].AllowedHeaders = @("x-ms-blob-content-type", "x-ms-blob-content-disposition")
PS C:\> $CorsRules[0].AllowedMethods = @("Get", "Connect", "Merge")
PS C:\> Set-AzStorageCORSRule -ServiceType Blob -CorsRules $CorsRules
```

<span data-ttu-id="6f96f-116">Det första kommandot får de aktuella CORS-reglerna för BLOB-typen genom att använda cmdleten **Get-AzStorageCORSRule** .</span><span class="sxs-lookup"><span data-stu-id="6f96f-116">The first command gets the current CORS rules for the Blob type by using the **Get-AzStorageCORSRule** cmdlet.</span></span>
<span data-ttu-id="6f96f-117">Kommandot lagrar reglerna i $CorsRules mat ris variabel.</span><span class="sxs-lookup"><span data-stu-id="6f96f-117">The command stores the rules in the $CorsRules array variable.</span></span>
<span data-ttu-id="6f96f-118">Det andra och tredje kommandot ändrar den första regeln i $CorsRules.</span><span class="sxs-lookup"><span data-stu-id="6f96f-118">The second and third commands modify the first rule in $CorsRules.</span></span>
<span data-ttu-id="6f96f-119">Det sista kommandot tilldelar reglerna i $CorsRules till typen blob-tjänst.</span><span class="sxs-lookup"><span data-stu-id="6f96f-119">The final command assigns the rules in $CorsRules to the Blob service type.</span></span>
<span data-ttu-id="6f96f-120">De reviderade reglerna ersätter de aktuella CORS-reglerna.</span><span class="sxs-lookup"><span data-stu-id="6f96f-120">The revised rules overwrite the current CORS rules.</span></span>

## <span data-ttu-id="6f96f-121">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6f96f-121">PARAMETERS</span></span>

### <span data-ttu-id="6f96f-122">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="6f96f-122">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="6f96f-123">Anger tids gräns för klient sidan, i sekunder, för en tjänst förfrågan.</span><span class="sxs-lookup"><span data-stu-id="6f96f-123">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="6f96f-124">Om det föregående samtalet inte fungerar under det angivna intervallet, försöker den här cmdleten igen.</span><span class="sxs-lookup"><span data-stu-id="6f96f-124">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="6f96f-125">Om denna cmdlet inte får ett lyckat svar innan intervallet går ut returneras ett fel.</span><span class="sxs-lookup"><span data-stu-id="6f96f-125">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: ClientTimeoutPerRequestInSeconds

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f96f-126">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="6f96f-126">-ConcurrentTaskCount</span></span>
<span data-ttu-id="6f96f-127">Anger maximalt antal samtidiga nätverks samtal.</span><span class="sxs-lookup"><span data-stu-id="6f96f-127">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="6f96f-128">Du kan använda den här parametern för att begränsa samtidigheten för att reglera den lokala processorn och bandbredds användning genom att ange det maximala antalet simultana nätverks samtal.</span><span class="sxs-lookup"><span data-stu-id="6f96f-128">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="6f96f-129">Det angivna värdet är ett absolut antal och multipliceras inte med antalet kärnor.</span><span class="sxs-lookup"><span data-stu-id="6f96f-129">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="6f96f-130">Den här parametern kan hjälpa till att minska nätverks anslutnings problem i miljöer med liten bandbredd, till exempel 100 kilobit per sekund.</span><span class="sxs-lookup"><span data-stu-id="6f96f-130">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="6f96f-131">Standardvärdet är 10.</span><span class="sxs-lookup"><span data-stu-id="6f96f-131">The default value is 10.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f96f-132">-Kontext</span><span class="sxs-lookup"><span data-stu-id="6f96f-132">-Context</span></span>
<span data-ttu-id="6f96f-133">Anger en Azure Storage-kontext.</span><span class="sxs-lookup"><span data-stu-id="6f96f-133">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="6f96f-134">Använd New-AzStorageContext cmdlet för att få en kontext.</span><span class="sxs-lookup"><span data-stu-id="6f96f-134">To obtain a context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="6f96f-135">-CorsRules</span><span class="sxs-lookup"><span data-stu-id="6f96f-135">-CorsRules</span></span>
<span data-ttu-id="6f96f-136">Anger en matris med CORS-regler.</span><span class="sxs-lookup"><span data-stu-id="6f96f-136">Specifies an array of CORS rules.</span></span>
<span data-ttu-id="6f96f-137">Du kan hämta befintliga regler med hjälp av Get-AzStorageCORSRule cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6f96f-137">You can retrieve the existing rules using the Get-AzStorageCORSRule cmdlet.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSCorsRule[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f96f-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f96f-138">-DefaultProfile</span></span>
<span data-ttu-id="6f96f-139">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="6f96f-139">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6f96f-140">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6f96f-140">-PassThru</span></span>
<span data-ttu-id="6f96f-141">Anger att denna cmdlet returnerar ett booleskt värde som visar att åtgärden lyckades.</span><span class="sxs-lookup"><span data-stu-id="6f96f-141">Indicates that this cmdlet returns a Boolean that reflects the success of the operation.</span></span>
<span data-ttu-id="6f96f-142">Denna cmdlet returnerar som standard inget värde.</span><span class="sxs-lookup"><span data-stu-id="6f96f-142">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="6f96f-143">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="6f96f-143">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="6f96f-144">Anger längden på tids gränsen för en server del av en begäran.</span><span class="sxs-lookup"><span data-stu-id="6f96f-144">Specifies the length of the time-out period for the server part of a request.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: ServerTimeoutPerRequestInSeconds

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f96f-145">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="6f96f-145">-ServiceType</span></span>
<span data-ttu-id="6f96f-146">Anger typen för Azure Storage-tjänsten för vilken denna cmdlet tilldelar regler.</span><span class="sxs-lookup"><span data-stu-id="6f96f-146">Specifies the Azure Storage service type for which this cmdlet assigns rules.</span></span>
<span data-ttu-id="6f96f-147">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="6f96f-147">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="6f96f-148">Object</span><span class="sxs-lookup"><span data-stu-id="6f96f-148">Blob</span></span> 
- <span data-ttu-id="6f96f-149">Tabell</span><span class="sxs-lookup"><span data-stu-id="6f96f-149">Table</span></span> 
- <span data-ttu-id="6f96f-150">Svarskö</span><span class="sxs-lookup"><span data-stu-id="6f96f-150">Queue</span></span> 
- <span data-ttu-id="6f96f-151">Fil</span><span class="sxs-lookup"><span data-stu-id="6f96f-151">File</span></span>

```yaml
Type: Microsoft.WindowsAzure.Commands.Storage.Common.StorageServiceType
Parameter Sets: (All)
Aliases:
Accepted values: Blob, Table, Queue, File

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f96f-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f96f-152">CommonParameters</span></span>
<span data-ttu-id="6f96f-153">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6f96f-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f96f-154">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6f96f-154">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f96f-155">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6f96f-155">INPUTS</span></span>

### <span data-ttu-id="6f96f-156">Microsoft. Azure. commands. Common. verifikation. abstraktioner. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="6f96f-156">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="6f96f-157">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6f96f-157">OUTPUTS</span></span>

### <span data-ttu-id="6f96f-158">Microsoft. WindowsAzure. commands. Storage. Model. ResourceModel. PSCorsRule</span><span class="sxs-lookup"><span data-stu-id="6f96f-158">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSCorsRule</span></span>

## <span data-ttu-id="6f96f-159">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6f96f-159">NOTES</span></span>

## <span data-ttu-id="6f96f-160">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6f96f-160">RELATED LINKS</span></span>

[<span data-ttu-id="6f96f-161">Get-AzStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="6f96f-161">Get-AzStorageCORSRule</span></span>](./Get-AzStorageCORSRule.md)

[<span data-ttu-id="6f96f-162">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="6f96f-162">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="6f96f-163">Remove-AzStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="6f96f-163">Remove-AzStorageCORSRule</span></span>](./Remove-AzStorageCORSRule.md)


