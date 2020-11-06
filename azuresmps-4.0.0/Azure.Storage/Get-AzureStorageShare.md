---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: FD3A0013-4365-4E65-891C-5C50A9D5658C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7e816d29784ea8b2e69ba4b36162938f7a82007d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93572348"
---
# <span data-ttu-id="3f127-101">Get-AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="3f127-101">Get-AzureStorageShare</span></span>

## <span data-ttu-id="3f127-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3f127-102">SYNOPSIS</span></span>
<span data-ttu-id="3f127-103">Hämtar en lista över fil resurser.</span><span class="sxs-lookup"><span data-stu-id="3f127-103">Gets a list of file shares.</span></span>

## <span data-ttu-id="3f127-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3f127-104">SYNTAX</span></span>

### <span data-ttu-id="3f127-105">MatchingPrefix (standard)</span><span class="sxs-lookup"><span data-stu-id="3f127-105">MatchingPrefix (Default)</span></span>
```
Get-AzureStorageShare [[-Prefix] <String>] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="3f127-106">Anslutningsspecifika</span><span class="sxs-lookup"><span data-stu-id="3f127-106">Specific</span></span>
```
Get-AzureStorageShare [-Name] <String> [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="3f127-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3f127-107">DESCRIPTION</span></span>
<span data-ttu-id="3f127-108">Cmdleten **Get-AzureStorageShare** hämtar en lista över fil resurser för ett lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="3f127-108">The **Get-AzureStorageShare** cmdlet gets a list of file shares for a storage account.</span></span>

## <span data-ttu-id="3f127-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3f127-109">EXAMPLES</span></span>

### <span data-ttu-id="3f127-110">Exempel 1: Hämta en fil resurs</span><span class="sxs-lookup"><span data-stu-id="3f127-110">Example 1: Get a file share</span></span>
```
PS C:\>Get-AzureStorageShare -Name "ContosoShare06"
```

<span data-ttu-id="3f127-111">Det här kommandot får fil resursen som heter ContosoShare06.</span><span class="sxs-lookup"><span data-stu-id="3f127-111">This command gets the file share named ContosoShare06.</span></span>

### <span data-ttu-id="3f127-112">Exempel 2: Hämta alla fil resurser som börjar med en sträng</span><span class="sxs-lookup"><span data-stu-id="3f127-112">Example 2: Get all file shares that begin with a string</span></span>
```
PS C:\>Get-AzureStorageShare -Prefix "Contoso"
```

<span data-ttu-id="3f127-113">Det här kommandot får alla fil resurser som har namn som börjar med contoso.</span><span class="sxs-lookup"><span data-stu-id="3f127-113">This command gets all file shares that have names that begin with Contoso.</span></span>

### <span data-ttu-id="3f127-114">Exempel 3: Hämta alla fil resurser i en viss kontext</span><span class="sxs-lookup"><span data-stu-id="3f127-114">Example 3: Get all file shares in a specified context</span></span>
```
PS C:\>$Context = New-AzureStorageContext -Local
PS C:\> Get-AzureStorageShare -Context $Context
```

<span data-ttu-id="3f127-115">I det första kommandot används cmdleten **New-AzureStorageContext** för att skapa en kontext med den *lokala* parametern och sedan lagras kontext objekt i variabeln $context.</span><span class="sxs-lookup"><span data-stu-id="3f127-115">The first command uses the **New-AzureStorageContext** cmdlet to create a context by using the *Local* parameter, and then stores that context object in the $Context variable.</span></span>

<span data-ttu-id="3f127-116">Det andra kommandot får fil resurserna för det kontext objekt som lagras i $Context.</span><span class="sxs-lookup"><span data-stu-id="3f127-116">The second command gets the file shares for the context object stored in $Context.</span></span>

## <span data-ttu-id="3f127-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3f127-117">PARAMETERS</span></span>

### <span data-ttu-id="3f127-118">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="3f127-118">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="3f127-119">Anger tids gräns för klient sidan, i sekunder, för en tjänst förfrågan.</span><span class="sxs-lookup"><span data-stu-id="3f127-119">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="3f127-120">Om det föregående samtalet inte fungerar under det angivna intervallet, försöker den här cmdleten igen.</span><span class="sxs-lookup"><span data-stu-id="3f127-120">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="3f127-121">Om denna cmdlet inte får ett lyckat svar innan intervallet går ut returneras ett fel.</span><span class="sxs-lookup"><span data-stu-id="3f127-121">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="3f127-122">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="3f127-122">-ConcurrentTaskCount</span></span>
<span data-ttu-id="3f127-123">Anger maximalt antal samtidiga nätverks samtal.</span><span class="sxs-lookup"><span data-stu-id="3f127-123">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="3f127-124">Du kan använda den här parametern för att begränsa samtidigheten för att reglera den lokala processorn och bandbredds användning genom att ange det maximala antalet simultana nätverks samtal.</span><span class="sxs-lookup"><span data-stu-id="3f127-124">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="3f127-125">Det angivna värdet är ett absolut antal och multipliceras inte med antalet kärnor.</span><span class="sxs-lookup"><span data-stu-id="3f127-125">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="3f127-126">Den här parametern kan hjälpa till att minska nätverks anslutnings problem i miljöer med liten bandbredd, till exempel 100 kilobit per sekund.</span><span class="sxs-lookup"><span data-stu-id="3f127-126">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="3f127-127">Standardvärdet är 10.</span><span class="sxs-lookup"><span data-stu-id="3f127-127">The default value is 10.</span></span>

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

### <span data-ttu-id="3f127-128">-Kontext</span><span class="sxs-lookup"><span data-stu-id="3f127-128">-Context</span></span>
<span data-ttu-id="3f127-129">Anger en Azure Storage-kontext.</span><span class="sxs-lookup"><span data-stu-id="3f127-129">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="3f127-130">Använd cmdleten [New-AzureStorageContext](./New-AzureStorageContext.md) för att få en kontext.</span><span class="sxs-lookup"><span data-stu-id="3f127-130">To obtain a context, use the [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="3f127-131">-Namn</span><span class="sxs-lookup"><span data-stu-id="3f127-131">-Name</span></span>
<span data-ttu-id="3f127-132">Anger namnet på fil resursen.</span><span class="sxs-lookup"><span data-stu-id="3f127-132">Specifies the name of the file share.</span></span>
<span data-ttu-id="3f127-133">Denna cmdlet hämtar fil resursen som den här parametern anger, eller ingenting om du anger namnet på en fil resurs som inte finns.</span><span class="sxs-lookup"><span data-stu-id="3f127-133">This cmdlet gets the file share that this parameter specifies, or nothing if you specify the name of a file share that does not exist.</span></span>

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

### <span data-ttu-id="3f127-134">-Prefix</span><span class="sxs-lookup"><span data-stu-id="3f127-134">-Prefix</span></span>
<span data-ttu-id="3f127-135">Anger prefixet för fil resurser.</span><span class="sxs-lookup"><span data-stu-id="3f127-135">Specifies the prefix for file shares.</span></span>
<span data-ttu-id="3f127-136">Denna cmdlet hämtar fil resurser som matchar det prefix som den här parametern anger, eller inga fildelningar om inga fil resurser matchar angivet prefix.</span><span class="sxs-lookup"><span data-stu-id="3f127-136">This cmdlet gets file shares that match the prefix that this parameter specifies, or no file shares if no file shares match the specified prefix.</span></span>

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

### <span data-ttu-id="3f127-137">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="3f127-137">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="3f127-138">Anger längden på tids gränsen för en server del av en begäran.</span><span class="sxs-lookup"><span data-stu-id="3f127-138">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="3f127-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f127-139">CommonParameters</span></span>
<span data-ttu-id="3f127-140">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3f127-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f127-141">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3f127-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f127-142">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3f127-142">INPUTS</span></span>

## <span data-ttu-id="3f127-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3f127-143">OUTPUTS</span></span>

## <span data-ttu-id="3f127-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3f127-144">NOTES</span></span>

## <span data-ttu-id="3f127-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3f127-145">RELATED LINKS</span></span>

[<span data-ttu-id="3f127-146">New-AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="3f127-146">New-AzureStorageShare</span></span>](./New-AzureStorageShare.md)

[<span data-ttu-id="3f127-147">Remove-AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="3f127-147">Remove-AzureStorageShare</span></span>](./Remove-AzureStorageShare.md)
