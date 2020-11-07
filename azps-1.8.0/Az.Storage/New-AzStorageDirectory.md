---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 65962F9A-CC79-4B8B-9208-A993708FD36F
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstoragedirectory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageDirectory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageDirectory.md
ms.openlocfilehash: 76d66d31856b2889484f1d786ef81295e8f27bc1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93746338"
---
# <span data-ttu-id="3caa1-101">New-AzStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="3caa1-101">New-AzStorageDirectory</span></span>

## <span data-ttu-id="3caa1-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3caa1-102">SYNOPSIS</span></span>
<span data-ttu-id="3caa1-103">Skapar en katalog.</span><span class="sxs-lookup"><span data-stu-id="3caa1-103">Creates a directory.</span></span>

## <span data-ttu-id="3caa1-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3caa1-104">SYNTAX</span></span>

### <span data-ttu-id="3caa1-105">Resurs namn (standard)</span><span class="sxs-lookup"><span data-stu-id="3caa1-105">ShareName (Default)</span></span>
```
New-AzStorageDirectory [-ShareName] <String> [-Path] <String> [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="3caa1-106">Resurserna</span><span class="sxs-lookup"><span data-stu-id="3caa1-106">Share</span></span>
```
New-AzStorageDirectory [-Share] <CloudFileShare> [-Path] <String> [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="3caa1-107">Katalogen</span><span class="sxs-lookup"><span data-stu-id="3caa1-107">Directory</span></span>
```
New-AzStorageDirectory [-Directory] <CloudFileDirectory> [-Path] <String> [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

## <span data-ttu-id="3caa1-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3caa1-108">DESCRIPTION</span></span>
<span data-ttu-id="3caa1-109">Cmdleten **New-AzStorageDirectory** skapar en katalog.</span><span class="sxs-lookup"><span data-stu-id="3caa1-109">The **New-AzStorageDirectory** cmdlet creates a directory.</span></span>
<span data-ttu-id="3caa1-110">Denna cmdlet returnerar ett **CloudFileDirectory** -objekt.</span><span class="sxs-lookup"><span data-stu-id="3caa1-110">This cmdlet returns a **CloudFileDirectory** object.</span></span>

## <span data-ttu-id="3caa1-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3caa1-111">EXAMPLES</span></span>

### <span data-ttu-id="3caa1-112">Exempel 1: skapa en mapp i en fil resurs</span><span class="sxs-lookup"><span data-stu-id="3caa1-112">Example 1: Create a folder in a file share</span></span>
```
PS C:\>New-AzStorageDirectory -ShareName "ContosoShare06" -Path "ContosoWorkingFolder"
```

<span data-ttu-id="3caa1-113">Det här kommandot skapar en mapp med namnet ContosoWorkingFolder i fil resursen som heter ContosoShare06.</span><span class="sxs-lookup"><span data-stu-id="3caa1-113">This command creates a folder named ContosoWorkingFolder in the file share named ContosoShare06.</span></span>

### <span data-ttu-id="3caa1-114">Exempel 2: skapa en mapp i en fil resurs som anges i ett fildelnings objekt</span><span class="sxs-lookup"><span data-stu-id="3caa1-114">Example 2: Create a folder in a file share specified in a file share object</span></span>
```
PS C:\>Get-AzStorageShare -Name "ContosoShare06" | New-AzStorageDirectory -Path "ContosoWorkingFolder"
```

<span data-ttu-id="3caa1-115">Det här kommandot använder cmdleten **Get-AzStorageShare** för att få fil resursen som heter ContosoShare06 och skickar den sedan till den aktuella cmdleten med operatören.</span><span class="sxs-lookup"><span data-stu-id="3caa1-115">This command uses the **Get-AzStorageShare** cmdlet to get the file share named ContosoShare06, and then passes it to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="3caa1-116">Den aktuella cmdleten skapar mappen som heter ContosoWorkingFolder i ContosoShare06.</span><span class="sxs-lookup"><span data-stu-id="3caa1-116">The current cmdlet creates the folder named ContosoWorkingFolder in ContosoShare06.</span></span>

## <span data-ttu-id="3caa1-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3caa1-117">PARAMETERS</span></span>

### <span data-ttu-id="3caa1-118">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="3caa1-118">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="3caa1-119">Anger tids gräns för klient sidan, i sekunder, för en tjänst förfrågan.</span><span class="sxs-lookup"><span data-stu-id="3caa1-119">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="3caa1-120">Om det föregående samtalet inte fungerar under det angivna intervallet, försöker den här cmdleten igen.</span><span class="sxs-lookup"><span data-stu-id="3caa1-120">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="3caa1-121">Om denna cmdlet inte får ett lyckat svar innan intervallet går ut returneras ett fel.</span><span class="sxs-lookup"><span data-stu-id="3caa1-121">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="3caa1-122">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="3caa1-122">-ConcurrentTaskCount</span></span>
<span data-ttu-id="3caa1-123">Anger maximalt antal samtidiga nätverks samtal.</span><span class="sxs-lookup"><span data-stu-id="3caa1-123">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="3caa1-124">Du kan använda den här parametern för att begränsa samtidigheten för att reglera den lokala processorn och bandbredds användning genom att ange det maximala antalet simultana nätverks samtal.</span><span class="sxs-lookup"><span data-stu-id="3caa1-124">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="3caa1-125">Det angivna värdet är ett absolut antal och multipliceras inte med antalet kärnor.</span><span class="sxs-lookup"><span data-stu-id="3caa1-125">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="3caa1-126">Den här parametern kan hjälpa till att minska nätverks anslutnings problem i miljöer med liten bandbredd, till exempel 100 kilobit per sekund.</span><span class="sxs-lookup"><span data-stu-id="3caa1-126">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="3caa1-127">Standardvärdet är 10.</span><span class="sxs-lookup"><span data-stu-id="3caa1-127">The default value is 10.</span></span>

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

### <span data-ttu-id="3caa1-128">-Kontext</span><span class="sxs-lookup"><span data-stu-id="3caa1-128">-Context</span></span>
<span data-ttu-id="3caa1-129">Anger en Azure Storage-kontext.</span><span class="sxs-lookup"><span data-stu-id="3caa1-129">Specifies an Azure storage context.</span></span>
<span data-ttu-id="3caa1-130">Använd cmdleten [New-AzStorageContext](./New-AzStorageContext.md) för att få en lagrings kontext.</span><span class="sxs-lookup"><span data-stu-id="3caa1-130">To obtain a storage context, use the [New-AzStorageContext](./New-AzStorageContext.md) cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: ShareName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3caa1-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3caa1-131">-DefaultProfile</span></span>
<span data-ttu-id="3caa1-132">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="3caa1-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3caa1-133">-Katalog</span><span class="sxs-lookup"><span data-stu-id="3caa1-133">-Directory</span></span>
<span data-ttu-id="3caa1-134">Anger en mapp som ett **CloudFileDirectory** -objekt.</span><span class="sxs-lookup"><span data-stu-id="3caa1-134">Specifies a folder as a **CloudFileDirectory** object.</span></span>
<span data-ttu-id="3caa1-135">Denna cmdlet skapar mappen på den plats som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="3caa1-135">This cmdlet creates the folder in the location that this parameter specifies.</span></span>
<span data-ttu-id="3caa1-136">Använd New-AzStorageDirectory cmdlet för att få en katalog.</span><span class="sxs-lookup"><span data-stu-id="3caa1-136">To obtain a directory, use the New-AzStorageDirectory cmdlet.</span></span>
<span data-ttu-id="3caa1-137">Du kan också använda Get-AzStorageFile cmdlet för att få en katalog.</span><span class="sxs-lookup"><span data-stu-id="3caa1-137">You can also use the Get-AzStorageFile cmdlet to obtain a directory.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.File.CloudFileDirectory
Parameter Sets: Directory
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3caa1-138">-Path</span><span class="sxs-lookup"><span data-stu-id="3caa1-138">-Path</span></span>
<span data-ttu-id="3caa1-139">Anger sökvägen till en mapp.</span><span class="sxs-lookup"><span data-stu-id="3caa1-139">Specifies the path of a folder.</span></span>
<span data-ttu-id="3caa1-140">Denna cmdlet skapar en mapp för sökvägen som anges i denna cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3caa1-140">This cmdlet creates a folder for the path that this cmdlet specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3caa1-141">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="3caa1-141">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="3caa1-142">Anger längden på tids gränsen för en server del av en begäran.</span><span class="sxs-lookup"><span data-stu-id="3caa1-142">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="3caa1-143">-Dela</span><span class="sxs-lookup"><span data-stu-id="3caa1-143">-Share</span></span>
<span data-ttu-id="3caa1-144">Anger ett **CloudFileShare** -objekt.</span><span class="sxs-lookup"><span data-stu-id="3caa1-144">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="3caa1-145">Denna cmdlet skapar en mapp i fil resursen som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="3caa1-145">This cmdlet creates a folder in the file share that this parameter specifies.</span></span>
<span data-ttu-id="3caa1-146">För att hämta ett **CloudFileShare** -objekt, Använd cmdleten Get-AzStorageShare.</span><span class="sxs-lookup"><span data-stu-id="3caa1-146">To obtain a **CloudFileShare** object, use the Get-AzStorageShare cmdlet.</span></span>
<span data-ttu-id="3caa1-147">Det här objektet innehåller lagrings kontexten.</span><span class="sxs-lookup"><span data-stu-id="3caa1-147">This object contains the storage context.</span></span>
<span data-ttu-id="3caa1-148">Om du anger den här parametern ska du inte ange en *kontext* parameter.</span><span class="sxs-lookup"><span data-stu-id="3caa1-148">If you specify this parameter, do not specify the *Context* parameter.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.File.CloudFileShare
Parameter Sets: Share
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3caa1-149">-ShareName</span><span class="sxs-lookup"><span data-stu-id="3caa1-149">-ShareName</span></span>
<span data-ttu-id="3caa1-150">Anger namnet på fil resursen.</span><span class="sxs-lookup"><span data-stu-id="3caa1-150">Specifies the name of the file share.</span></span>
<span data-ttu-id="3caa1-151">Denna cmdlet skapar en mapp i fil resursen som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="3caa1-151">This cmdlet creates a folder in the file share that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ShareName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3caa1-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3caa1-152">CommonParameters</span></span>
<span data-ttu-id="3caa1-153">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3caa1-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3caa1-154">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3caa1-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3caa1-155">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3caa1-155">INPUTS</span></span>

### <span data-ttu-id="3caa1-156">Microsoft. WindowsAzure. Storage. File. CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="3caa1-156">Microsoft.WindowsAzure.Storage.File.CloudFileShare</span></span>

### <span data-ttu-id="3caa1-157">Microsoft. WindowsAzure. Storage. File. CloudFileDirectory</span><span class="sxs-lookup"><span data-stu-id="3caa1-157">Microsoft.WindowsAzure.Storage.File.CloudFileDirectory</span></span>

### <span data-ttu-id="3caa1-158">System. String</span><span class="sxs-lookup"><span data-stu-id="3caa1-158">System.String</span></span>

### <span data-ttu-id="3caa1-159">Microsoft. Azure. commands. Common. verifikation. abstraktioner. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="3caa1-159">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="3caa1-160">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3caa1-160">OUTPUTS</span></span>

### <span data-ttu-id="3caa1-161">Microsoft. WindowsAzure. Storage. File. CloudFileDirectory</span><span class="sxs-lookup"><span data-stu-id="3caa1-161">Microsoft.WindowsAzure.Storage.File.CloudFileDirectory</span></span>

## <span data-ttu-id="3caa1-162">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3caa1-162">NOTES</span></span>

## <span data-ttu-id="3caa1-163">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3caa1-163">RELATED LINKS</span></span>

[<span data-ttu-id="3caa1-164">Get-AzStorageFile</span><span class="sxs-lookup"><span data-stu-id="3caa1-164">Get-AzStorageFile</span></span>](./Get-AzStorageFile.md)

[<span data-ttu-id="3caa1-165">Get-AzStorageShare</span><span class="sxs-lookup"><span data-stu-id="3caa1-165">Get-AzStorageShare</span></span>](./Get-AzStorageShare.md)

[<span data-ttu-id="3caa1-166">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="3caa1-166">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="3caa1-167">New-AzStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="3caa1-167">New-AzStorageDirectory</span></span>](./New-AzStorageDirectory.md)

[<span data-ttu-id="3caa1-168">Remove-AzStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="3caa1-168">Remove-AzStorageDirectory</span></span>](./Remove-AzStorageDirectory.md)
