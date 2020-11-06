---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: FD3A0013-4365-4E65-891C-5C50A9D5658C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageShare.md
gitcommit: https://github.com/Azure/azure-powershell/blob/173e94aec59d7f539b72e43e90e5e7f8ba5f62bc
ms.openlocfilehash: 65ba11bcbe26ce91ce4c9ff2f84dc0cff30e125c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573808"
---
# <span data-ttu-id="e070e-101">Get-AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="e070e-101">Get-AzureStorageShare</span></span>

## <span data-ttu-id="e070e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e070e-102">SYNOPSIS</span></span>
<span data-ttu-id="e070e-103">Hämtar en lista över fil resurser.</span><span class="sxs-lookup"><span data-stu-id="e070e-103">Gets a list of file shares.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e070e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e070e-104">SYNTAX</span></span>

### <span data-ttu-id="e070e-105">MatchingPrefix (standard)</span><span class="sxs-lookup"><span data-stu-id="e070e-105">MatchingPrefix (Default)</span></span>
```
Get-AzureStorageShare [[-Prefix] <String>] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="e070e-106">Anslutningsspecifika</span><span class="sxs-lookup"><span data-stu-id="e070e-106">Specific</span></span>
```
Get-AzureStorageShare [-Name] <String> [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="e070e-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e070e-107">DESCRIPTION</span></span>
<span data-ttu-id="e070e-108">Cmdleten **Get-AzureStorageShare** hämtar en lista över fil resurser för ett lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="e070e-108">The **Get-AzureStorageShare** cmdlet gets a list of file shares for a storage account.</span></span>

## <span data-ttu-id="e070e-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e070e-109">EXAMPLES</span></span>

### <span data-ttu-id="e070e-110">Exempel 1: Hämta en fil resurs</span><span class="sxs-lookup"><span data-stu-id="e070e-110">Example 1: Get a file share</span></span>
```
PS C:\>Get-AzureStorageShare -Name "ContosoShare06"
```

<span data-ttu-id="e070e-111">Det här kommandot får fil resursen som heter ContosoShare06.</span><span class="sxs-lookup"><span data-stu-id="e070e-111">This command gets the file share named ContosoShare06.</span></span>

### <span data-ttu-id="e070e-112">Exempel 2: Hämta alla fil resurser som börjar med en sträng</span><span class="sxs-lookup"><span data-stu-id="e070e-112">Example 2: Get all file shares that begin with a string</span></span>
```
PS C:\>Get-AzureStorageShare -Prefix "Contoso"
```

<span data-ttu-id="e070e-113">Det här kommandot får alla fil resurser som har namn som börjar med contoso.</span><span class="sxs-lookup"><span data-stu-id="e070e-113">This command gets all file shares that have names that begin with Contoso.</span></span>

### <span data-ttu-id="e070e-114">Exempel 3: Hämta alla fil resurser i en viss kontext</span><span class="sxs-lookup"><span data-stu-id="e070e-114">Example 3: Get all file shares in a specified context</span></span>
```
PS C:\>$Context = New-AzureStorageContext -Local
PS C:\> Get-AzureStorageShare -Context $Context
```

<span data-ttu-id="e070e-115">I det första kommandot används cmdleten **New-AzureStorageContext** för att skapa en kontext med den *lokala* parametern och sedan lagras kontext objekt i variabeln $context.</span><span class="sxs-lookup"><span data-stu-id="e070e-115">The first command uses the **New-AzureStorageContext** cmdlet to create a context by using the *Local* parameter, and then stores that context object in the $Context variable.</span></span>

<span data-ttu-id="e070e-116">Det andra kommandot får fil resurserna för det kontext objekt som lagras i $Context.</span><span class="sxs-lookup"><span data-stu-id="e070e-116">The second command gets the file shares for the context object stored in $Context.</span></span>

## <span data-ttu-id="e070e-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e070e-117">PARAMETERS</span></span>

### <span data-ttu-id="e070e-118">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="e070e-118">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="e070e-119">Anger tids gräns för klient sidan, i sekunder, för en tjänst förfrågan.</span><span class="sxs-lookup"><span data-stu-id="e070e-119">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="e070e-120">Om det föregående samtalet inte fungerar under det angivna intervallet, försöker den här cmdleten igen.</span><span class="sxs-lookup"><span data-stu-id="e070e-120">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="e070e-121">Om denna cmdlet inte får ett lyckat svar innan intervallet går ut returneras ett fel.</span><span class="sxs-lookup"><span data-stu-id="e070e-121">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="e070e-122">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="e070e-122">-ConcurrentTaskCount</span></span>
<span data-ttu-id="e070e-123">Anger maximalt antal samtidiga nätverks samtal.</span><span class="sxs-lookup"><span data-stu-id="e070e-123">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="e070e-124">Du kan använda den här parametern för att begränsa samtidigheten för att reglera den lokala processorn och bandbredds användning genom att ange det maximala antalet simultana nätverks samtal.</span><span class="sxs-lookup"><span data-stu-id="e070e-124">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="e070e-125">Det angivna värdet är ett absolut antal och multipliceras inte med antalet kärnor.</span><span class="sxs-lookup"><span data-stu-id="e070e-125">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="e070e-126">Den här parametern kan hjälpa till att minska nätverks anslutnings problem i miljöer med liten bandbredd, till exempel 100 kilobit per sekund.</span><span class="sxs-lookup"><span data-stu-id="e070e-126">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="e070e-127">Standardvärdet är 10.</span><span class="sxs-lookup"><span data-stu-id="e070e-127">The default value is 10.</span></span>

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

### <span data-ttu-id="e070e-128">-Kontext</span><span class="sxs-lookup"><span data-stu-id="e070e-128">-Context</span></span>
<span data-ttu-id="e070e-129">Anger en Azure Storage-kontext.</span><span class="sxs-lookup"><span data-stu-id="e070e-129">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="e070e-130">Använd cmdleten [New-AzureStorageContext](./New-AzureStorageContext.md) för att få en kontext.</span><span class="sxs-lookup"><span data-stu-id="e070e-130">To obtain a context, use the [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="e070e-131">-Namn</span><span class="sxs-lookup"><span data-stu-id="e070e-131">-Name</span></span>
<span data-ttu-id="e070e-132">Anger namnet på fil resursen.</span><span class="sxs-lookup"><span data-stu-id="e070e-132">Specifies the name of the file share.</span></span>
<span data-ttu-id="e070e-133">Denna cmdlet hämtar fil resursen som den här parametern anger, eller ingenting om du anger namnet på en fil resurs som inte finns.</span><span class="sxs-lookup"><span data-stu-id="e070e-133">This cmdlet gets the file share that this parameter specifies, or nothing if you specify the name of a file share that does not exist.</span></span>

```yaml
Type: String
Parameter Sets: Specific
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e070e-134">-Prefix</span><span class="sxs-lookup"><span data-stu-id="e070e-134">-Prefix</span></span>
<span data-ttu-id="e070e-135">Anger prefixet för fil resurser.</span><span class="sxs-lookup"><span data-stu-id="e070e-135">Specifies the prefix for file shares.</span></span>
<span data-ttu-id="e070e-136">Denna cmdlet hämtar fil resurser som matchar det prefix som den här parametern anger, eller inga fildelningar om inga fil resurser matchar angivet prefix.</span><span class="sxs-lookup"><span data-stu-id="e070e-136">This cmdlet gets file shares that match the prefix that this parameter specifies, or no file shares if no file shares match the specified prefix.</span></span>

```yaml
Type: String
Parameter Sets: MatchingPrefix
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e070e-137">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="e070e-137">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="e070e-138">Anger längden på tids gränsen för en server del av en begäran.</span><span class="sxs-lookup"><span data-stu-id="e070e-138">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="e070e-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e070e-139">CommonParameters</span></span>
<span data-ttu-id="e070e-140">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e070e-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e070e-141">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e070e-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e070e-142">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e070e-142">INPUTS</span></span>

### <span data-ttu-id="e070e-143">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="e070e-143">IStorageContext</span></span>

<span data-ttu-id="e070e-144">Parametern ' context ' godkänner värdet av typen ' IStorageContext ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="e070e-144">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

## <span data-ttu-id="e070e-145">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e070e-145">OUTPUTS</span></span>

## <span data-ttu-id="e070e-146">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e070e-146">NOTES</span></span>

## <span data-ttu-id="e070e-147">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e070e-147">RELATED LINKS</span></span>

[<span data-ttu-id="e070e-148">New-AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="e070e-148">New-AzureStorageShare</span></span>](./New-AzureStorageShare.md)

[<span data-ttu-id="e070e-149">Remove-AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="e070e-149">Remove-AzureStorageShare</span></span>](./Remove-AzureStorageShare.md)
