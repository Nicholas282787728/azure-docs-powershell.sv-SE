---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: FD3A0013-4365-4E65-891C-5C50A9D5658C
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/get-azurestorageshare
schema: 2.0.0
ms.openlocfilehash: 7ddc117ca7f8af55fbfad6362d8b7a024369809e
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93929145"
---
# <span data-ttu-id="d68a4-101">Get-AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="d68a4-101">Get-AzureStorageShare</span></span>

## <span data-ttu-id="d68a4-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d68a4-102">SYNOPSIS</span></span>
<span data-ttu-id="d68a4-103">Hämtar en lista över fil resurser.</span><span class="sxs-lookup"><span data-stu-id="d68a4-103">Gets a list of file shares.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d68a4-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d68a4-104">SYNTAX</span></span>

### <span data-ttu-id="d68a4-105">MatchingPrefix (standard)</span><span class="sxs-lookup"><span data-stu-id="d68a4-105">MatchingPrefix (Default)</span></span>
```
Get-AzureStorageShare [[-Prefix] <String>] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="d68a4-106">Anslutningsspecifika</span><span class="sxs-lookup"><span data-stu-id="d68a4-106">Specific</span></span>
```
Get-AzureStorageShare [-Name] <String> [[-SnapshotTime] <DateTimeOffset>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="d68a4-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d68a4-107">DESCRIPTION</span></span>
<span data-ttu-id="d68a4-108">Cmdleten **Get-AzureStorageShare** hämtar en lista över fil resurser för ett lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="d68a4-108">The **Get-AzureStorageShare** cmdlet gets a list of file shares for a storage account.</span></span>

## <span data-ttu-id="d68a4-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d68a4-109">EXAMPLES</span></span>

### <span data-ttu-id="d68a4-110">Exempel 1: Hämta en fil resurs</span><span class="sxs-lookup"><span data-stu-id="d68a4-110">Example 1: Get a file share</span></span>
```
PS C:\>Get-AzureStorageShare -Name "ContosoShare06"
```

<span data-ttu-id="d68a4-111">Det här kommandot får fil resursen som heter ContosoShare06.</span><span class="sxs-lookup"><span data-stu-id="d68a4-111">This command gets the file share named ContosoShare06.</span></span>

### <span data-ttu-id="d68a4-112">Exempel 2: Hämta alla fil resurser som börjar med en sträng</span><span class="sxs-lookup"><span data-stu-id="d68a4-112">Example 2: Get all file shares that begin with a string</span></span>
```
PS C:\>Get-AzureStorageShare -Prefix "Contoso"
```

<span data-ttu-id="d68a4-113">Det här kommandot får alla fil resurser som har namn som börjar med contoso.</span><span class="sxs-lookup"><span data-stu-id="d68a4-113">This command gets all file shares that have names that begin with Contoso.</span></span>

### <span data-ttu-id="d68a4-114">Exempel 3: Hämta alla fil resurser i en viss kontext</span><span class="sxs-lookup"><span data-stu-id="d68a4-114">Example 3: Get all file shares in a specified context</span></span>
```
PS C:\>$Context = New-AzureStorageContext -Local
PS C:\> Get-AzureStorageShare -Context $Context
```

<span data-ttu-id="d68a4-115">I det första kommandot används cmdleten **New-AzureStorageContext** för att skapa en kontext med den *lokala* parametern och sedan lagras kontext objekt i variabeln $context.</span><span class="sxs-lookup"><span data-stu-id="d68a4-115">The first command uses the **New-AzureStorageContext** cmdlet to create a context by using the *Local* parameter, and then stores that context object in the $Context variable.</span></span>
<span data-ttu-id="d68a4-116">Det andra kommandot får fil resurserna för det kontext objekt som lagras i $Context.</span><span class="sxs-lookup"><span data-stu-id="d68a4-116">The second command gets the file shares for the context object stored in $Context.</span></span>

### <span data-ttu-id="d68a4-117">Exempel 4: skapa en fil resurs bild med ett visst resurs namn och SnapshotTime</span><span class="sxs-lookup"><span data-stu-id="d68a4-117">Example 4: Get a file share snapshot with specific share name and SnapshotTime</span></span>
```
PS C:\>Get-AzureStorageShare -Name "ContosoShare06" -SnapshotTime "6/16/2017 9:48:41 AM +00:00"
```

<span data-ttu-id="d68a4-118">Det här kommandot får en ögonblicks bild för fil delning med specifika resurs namn och SnapshotTime.</span><span class="sxs-lookup"><span data-stu-id="d68a4-118">This command gets a file share snapshot with specific share name and SnapshotTime.</span></span>

## <span data-ttu-id="d68a4-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d68a4-119">PARAMETERS</span></span>

### <span data-ttu-id="d68a4-120">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="d68a4-120">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="d68a4-121">Anger tids gräns för klient sidan, i sekunder, för en tjänst förfrågan.</span><span class="sxs-lookup"><span data-stu-id="d68a4-121">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="d68a4-122">Om det föregående samtalet inte fungerar under det angivna intervallet, försöker den här cmdleten igen.</span><span class="sxs-lookup"><span data-stu-id="d68a4-122">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="d68a4-123">Om denna cmdlet inte får ett lyckat svar innan intervallet går ut returneras ett fel.</span><span class="sxs-lookup"><span data-stu-id="d68a4-123">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="d68a4-124">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="d68a4-124">-ConcurrentTaskCount</span></span>
<span data-ttu-id="d68a4-125">Anger maximalt antal samtidiga nätverks samtal.</span><span class="sxs-lookup"><span data-stu-id="d68a4-125">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="d68a4-126">Du kan använda den här parametern för att begränsa samtidigheten för att reglera den lokala processorn och bandbredds användning genom att ange det maximala antalet simultana nätverks samtal.</span><span class="sxs-lookup"><span data-stu-id="d68a4-126">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="d68a4-127">Det angivna värdet är ett absolut antal och multipliceras inte med antalet kärnor.</span><span class="sxs-lookup"><span data-stu-id="d68a4-127">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="d68a4-128">Den här parametern kan hjälpa till att minska nätverks anslutnings problem i miljöer med liten bandbredd, till exempel 100 kilobit per sekund.</span><span class="sxs-lookup"><span data-stu-id="d68a4-128">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="d68a4-129">Standardvärdet är 10.</span><span class="sxs-lookup"><span data-stu-id="d68a4-129">The default value is 10.</span></span>

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

### <span data-ttu-id="d68a4-130">-Kontext</span><span class="sxs-lookup"><span data-stu-id="d68a4-130">-Context</span></span>
<span data-ttu-id="d68a4-131">Anger en Azure Storage-kontext.</span><span class="sxs-lookup"><span data-stu-id="d68a4-131">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="d68a4-132">Använd cmdleten [New-AzureStorageContext](./New-AzureStorageContext.md) för att få en kontext.</span><span class="sxs-lookup"><span data-stu-id="d68a4-132">To obtain a context, use the [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="d68a4-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d68a4-133">-DefaultProfile</span></span>
<span data-ttu-id="d68a4-134">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d68a4-134">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d68a4-135">-Namn</span><span class="sxs-lookup"><span data-stu-id="d68a4-135">-Name</span></span>
<span data-ttu-id="d68a4-136">Anger namnet på fil resursen.</span><span class="sxs-lookup"><span data-stu-id="d68a4-136">Specifies the name of the file share.</span></span>
<span data-ttu-id="d68a4-137">Denna cmdlet hämtar fil resursen som den här parametern anger, eller ingenting om du anger namnet på en fil resurs som inte finns.</span><span class="sxs-lookup"><span data-stu-id="d68a4-137">This cmdlet gets the file share that this parameter specifies, or nothing if you specify the name of a file share that does not exist.</span></span>

```yaml
Type: System.String
Parameter Sets: Specific
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d68a4-138">-Prefix</span><span class="sxs-lookup"><span data-stu-id="d68a4-138">-Prefix</span></span>
<span data-ttu-id="d68a4-139">Anger prefixet för fil resurser.</span><span class="sxs-lookup"><span data-stu-id="d68a4-139">Specifies the prefix for file shares.</span></span>
<span data-ttu-id="d68a4-140">Denna cmdlet hämtar fil resurser som matchar det prefix som den här parametern anger, eller inga fildelningar om inga fil resurser matchar angivet prefix.</span><span class="sxs-lookup"><span data-stu-id="d68a4-140">This cmdlet gets file shares that match the prefix that this parameter specifies, or no file shares if no file shares match the specified prefix.</span></span>

```yaml
Type: System.String
Parameter Sets: MatchingPrefix
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d68a4-141">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="d68a4-141">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="d68a4-142">Anger längden på tids gränsen för en server del av en begäran.</span><span class="sxs-lookup"><span data-stu-id="d68a4-142">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="d68a4-143">-SnapshotTime</span><span class="sxs-lookup"><span data-stu-id="d68a4-143">-SnapshotTime</span></span>
<span data-ttu-id="d68a4-144">SnapshotTime av den ögonblicks bild för fil resursen som ska tas emot.</span><span class="sxs-lookup"><span data-stu-id="d68a4-144">SnapshotTime of the file share snapshot to be received.</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: Specific
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d68a4-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d68a4-145">CommonParameters</span></span>
<span data-ttu-id="d68a4-146">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d68a4-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d68a4-147">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d68a4-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d68a4-148">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d68a4-148">INPUTS</span></span>

### <span data-ttu-id="d68a4-149">Microsoft. Azure. commands. Common. verifikation. abstraktioner. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="d68a4-149">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="d68a4-150">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d68a4-150">OUTPUTS</span></span>

### <span data-ttu-id="d68a4-151">Microsoft. WindowsAzure. Storage. File. CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="d68a4-151">Microsoft.WindowsAzure.Storage.File.CloudFileShare</span></span>

## <span data-ttu-id="d68a4-152">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d68a4-152">NOTES</span></span>

## <span data-ttu-id="d68a4-153">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d68a4-153">RELATED LINKS</span></span>

[<span data-ttu-id="d68a4-154">New-AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="d68a4-154">New-AzureStorageShare</span></span>](./New-AzureStorageShare.md)

[<span data-ttu-id="d68a4-155">Remove-AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="d68a4-155">Remove-AzureStorageShare</span></span>](./Remove-AzureStorageShare.md)
