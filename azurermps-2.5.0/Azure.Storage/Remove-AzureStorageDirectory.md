---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: 53988D79-1F8B-4138-9F92-2912D418C121
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/remove-azurestoragedirectory
schema: 2.0.0
ms.openlocfilehash: e615f89d84a6f241e1a2a1ba44706c7f9a5310d8
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93929993"
---
# <span data-ttu-id="b5b8b-101">Remove-AzureStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="b5b8b-101">Remove-AzureStorageDirectory</span></span>

## <span data-ttu-id="b5b8b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b5b8b-102">SYNOPSIS</span></span>
<span data-ttu-id="b5b8b-103">Tar bort en katalog.</span><span class="sxs-lookup"><span data-stu-id="b5b8b-103">Deletes a directory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b5b8b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b5b8b-104">SYNTAX</span></span>

### <span data-ttu-id="b5b8b-105">Resurs namn (standard)</span><span class="sxs-lookup"><span data-stu-id="b5b8b-105">ShareName (Default)</span></span>
```
Remove-AzureStorageDirectory [-ShareName] <String> [-Path] <String> [-PassThru] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b5b8b-106">Resurserna</span><span class="sxs-lookup"><span data-stu-id="b5b8b-106">Share</span></span>
```
Remove-AzureStorageDirectory [-Share] <CloudFileShare> [-Path] <String> [-PassThru]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b5b8b-107">Katalogen</span><span class="sxs-lookup"><span data-stu-id="b5b8b-107">Directory</span></span>
```
Remove-AzureStorageDirectory [-Directory] <CloudFileDirectory> [[-Path] <String>] [-PassThru]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b5b8b-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b5b8b-108">DESCRIPTION</span></span>
<span data-ttu-id="b5b8b-109">Cmdleten **Remove-AzureStorageDirectory** tar bort en katalog.</span><span class="sxs-lookup"><span data-stu-id="b5b8b-109">The **Remove-AzureStorageDirectory** cmdlet deletes a directory.</span></span>

## <span data-ttu-id="b5b8b-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b5b8b-110">EXAMPLES</span></span>

### <span data-ttu-id="b5b8b-111">Exempel 1: ta bort en mapp</span><span class="sxs-lookup"><span data-stu-id="b5b8b-111">Example 1: Delete a folder</span></span>
```
PS C:\>Remove-AzureStorageDirectory -ShareName "ContosoShare06" -Path "ContosoWorkingFolder"
```

<span data-ttu-id="b5b8b-112">Det här kommandot tar bort mappen som heter ContosoWorkingFolder från fil resursen med namnet ContosoShare06.</span><span class="sxs-lookup"><span data-stu-id="b5b8b-112">This command deletes the folder named ContosoWorkingFolder from the file share named ContosoShare06.</span></span>

## <span data-ttu-id="b5b8b-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b5b8b-113">PARAMETERS</span></span>

### <span data-ttu-id="b5b8b-114">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="b5b8b-114">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="b5b8b-115">Anger tids gräns för klient sidan, i sekunder, för en tjänst förfrågan.</span><span class="sxs-lookup"><span data-stu-id="b5b8b-115">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="b5b8b-116">Om det föregående samtalet inte fungerar under det angivna intervallet, försöker den här cmdleten igen.</span><span class="sxs-lookup"><span data-stu-id="b5b8b-116">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="b5b8b-117">Om denna cmdlet inte får ett lyckat svar innan intervallet går ut returneras ett fel.</span><span class="sxs-lookup"><span data-stu-id="b5b8b-117">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="b5b8b-118">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="b5b8b-118">-ConcurrentTaskCount</span></span>
<span data-ttu-id="b5b8b-119">Anger maximalt antal samtidiga nätverks samtal.</span><span class="sxs-lookup"><span data-stu-id="b5b8b-119">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="b5b8b-120">Du kan använda den här parametern för att begränsa samtidigheten för att reglera den lokala processorn och bandbredds användning genom att ange det maximala antalet simultana nätverks samtal.</span><span class="sxs-lookup"><span data-stu-id="b5b8b-120">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="b5b8b-121">Det angivna värdet är ett absolut antal och multipliceras inte med antalet kärnor.</span><span class="sxs-lookup"><span data-stu-id="b5b8b-121">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="b5b8b-122">Den här parametern kan hjälpa till att minska nätverks anslutnings problem i miljöer med liten bandbredd, till exempel 100 kilobit per sekund.</span><span class="sxs-lookup"><span data-stu-id="b5b8b-122">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="b5b8b-123">Standardvärdet är 10.</span><span class="sxs-lookup"><span data-stu-id="b5b8b-123">The default value is 10.</span></span>

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

### <span data-ttu-id="b5b8b-124">-Kontext</span><span class="sxs-lookup"><span data-stu-id="b5b8b-124">-Context</span></span>
<span data-ttu-id="b5b8b-125">Anger en Azure Storage-kontext.</span><span class="sxs-lookup"><span data-stu-id="b5b8b-125">Specifies an Azure storage context.</span></span>
<span data-ttu-id="b5b8b-126">Använd cmdleten [New-AzureStorageContext](./New-AzureStorageContext.md) för att få en lagrings kontext.</span><span class="sxs-lookup"><span data-stu-id="b5b8b-126">To obtain a storage context, use the [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="b5b8b-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5b8b-127">-DefaultProfile</span></span>
<span data-ttu-id="b5b8b-128">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b5b8b-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b5b8b-129">-Katalog</span><span class="sxs-lookup"><span data-stu-id="b5b8b-129">-Directory</span></span>
<span data-ttu-id="b5b8b-130">Anger en mapp som ett **CloudFileDirectory** -objekt.</span><span class="sxs-lookup"><span data-stu-id="b5b8b-130">Specifies a folder as a **CloudFileDirectory** object.</span></span>
<span data-ttu-id="b5b8b-131">Denna cmdlet tar bort den mapp som anges i den här parametern.</span><span class="sxs-lookup"><span data-stu-id="b5b8b-131">This cmdlet removes the folder that this parameter specifies.</span></span>
<span data-ttu-id="b5b8b-132">Använd New-AzureStorageDirectory cmdlet för att få en katalog.</span><span class="sxs-lookup"><span data-stu-id="b5b8b-132">To obtain a directory, use the New-AzureStorageDirectory cmdlet.</span></span>
<span data-ttu-id="b5b8b-133">Du kan också använda cmdleten **Get-AzureStorageFile** för att få en katalog.</span><span class="sxs-lookup"><span data-stu-id="b5b8b-133">You can also use the **Get-AzureStorageFile** cmdlet to obtain a directory.</span></span>

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

### <span data-ttu-id="b5b8b-134">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b5b8b-134">-PassThru</span></span>
<span data-ttu-id="b5b8b-135">Anger att om denna cmdlet lyckas returneras ett värde för $True.</span><span class="sxs-lookup"><span data-stu-id="b5b8b-135">Indicates that, if this cmdlet succeeds, it returns a value of $True.</span></span>
<span data-ttu-id="b5b8b-136">Om du anger den här parametern och om cmdleten Miss lyckas på grund av ett olämpligt värde för parametern _Path_ returneras ett fel.</span><span class="sxs-lookup"><span data-stu-id="b5b8b-136">If you specify this parameter, and if the cmdlet is unsuccessful because of an inappropriate value for the _Path_ parameter, the cmdlet returns an error.</span></span>
<span data-ttu-id="b5b8b-137">Om du inte anger den här parametern returnerar denna cmdlet inte ett värde.</span><span class="sxs-lookup"><span data-stu-id="b5b8b-137">If you do not specify this parameter, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="b5b8b-138">-Path</span><span class="sxs-lookup"><span data-stu-id="b5b8b-138">-Path</span></span>
<span data-ttu-id="b5b8b-139">Anger sökvägen till en mapp.</span><span class="sxs-lookup"><span data-stu-id="b5b8b-139">Specifies the path of a folder.</span></span>
<span data-ttu-id="b5b8b-140">Om mappen som den här parametern anger är tom tar denna cmdlet bort den mappen.</span><span class="sxs-lookup"><span data-stu-id="b5b8b-140">If the folder that this parameter specifies is empty, this cmdlet deletes that folder.</span></span>
<span data-ttu-id="b5b8b-141">Om mappen inte är tom gör denna cmdlet ingen ändring och returnerar ett fel.</span><span class="sxs-lookup"><span data-stu-id="b5b8b-141">If the folder is not empty, this cmdlet makes no change, and returns an error.</span></span>

```yaml
Type: System.String
Parameter Sets: ShareName, Share
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Directory
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5b8b-142">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="b5b8b-142">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="b5b8b-143">Anger längden på tids gränsen för en server del av en begäran.</span><span class="sxs-lookup"><span data-stu-id="b5b8b-143">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="b5b8b-144">-Dela</span><span class="sxs-lookup"><span data-stu-id="b5b8b-144">-Share</span></span>
<span data-ttu-id="b5b8b-145">Anger ett **CloudFileShare** -objekt.</span><span class="sxs-lookup"><span data-stu-id="b5b8b-145">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="b5b8b-146">Denna cmdlet tar bort en mapp under fil resursen som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="b5b8b-146">This cmdlet removes a folder under the file share that this parameter specifies.</span></span>
<span data-ttu-id="b5b8b-147">För att hämta ett **CloudFileShare** -objekt, Använd cmdleten Get-AzureStorageShare.</span><span class="sxs-lookup"><span data-stu-id="b5b8b-147">To obtain a **CloudFileShare** object, use the Get-AzureStorageShare cmdlet.</span></span>
<span data-ttu-id="b5b8b-148">Det här objektet innehåller lagrings kontexten.</span><span class="sxs-lookup"><span data-stu-id="b5b8b-148">This object contains the storage context.</span></span>
<span data-ttu-id="b5b8b-149">Om du anger den här parametern ska du inte ange en *kontext* parameter.</span><span class="sxs-lookup"><span data-stu-id="b5b8b-149">If you specify this parameter, do not specify the *Context* parameter.</span></span>

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

### <span data-ttu-id="b5b8b-150">-ShareName</span><span class="sxs-lookup"><span data-stu-id="b5b8b-150">-ShareName</span></span>
<span data-ttu-id="b5b8b-151">Anger namnet på fil resursen.</span><span class="sxs-lookup"><span data-stu-id="b5b8b-151">Specifies the name of the file share.</span></span>
<span data-ttu-id="b5b8b-152">Denna cmdlet tar bort en mapp under fil resursen som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="b5b8b-152">This cmdlet removes a folder under the file share that this parameter specifies.</span></span>

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

### <span data-ttu-id="b5b8b-153">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="b5b8b-153">-Confirm</span></span>
<span data-ttu-id="b5b8b-154">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="b5b8b-154">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5b8b-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b5b8b-155">-WhatIf</span></span>
<span data-ttu-id="b5b8b-156">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="b5b8b-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b5b8b-157">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="b5b8b-157">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5b8b-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5b8b-158">CommonParameters</span></span>
<span data-ttu-id="b5b8b-159">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b5b8b-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5b8b-160">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b5b8b-160">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5b8b-161">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b5b8b-161">INPUTS</span></span>

### <span data-ttu-id="b5b8b-162">Microsoft. WindowsAzure. Storage. File. CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="b5b8b-162">Microsoft.WindowsAzure.Storage.File.CloudFileShare</span></span>
<span data-ttu-id="b5b8b-163">Parametrar: dela (ByValue)</span><span class="sxs-lookup"><span data-stu-id="b5b8b-163">Parameters: Share (ByValue)</span></span>

### <span data-ttu-id="b5b8b-164">Microsoft. WindowsAzure. Storage. File. CloudFileDirectory</span><span class="sxs-lookup"><span data-stu-id="b5b8b-164">Microsoft.WindowsAzure.Storage.File.CloudFileDirectory</span></span>
<span data-ttu-id="b5b8b-165">Parametrar: katalog (ByValue)</span><span class="sxs-lookup"><span data-stu-id="b5b8b-165">Parameters: Directory (ByValue)</span></span>

### <span data-ttu-id="b5b8b-166">System. String</span><span class="sxs-lookup"><span data-stu-id="b5b8b-166">System.String</span></span>

### <span data-ttu-id="b5b8b-167">Microsoft. Azure. commands. Common. verifikation. abstraktioner. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="b5b8b-167">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="b5b8b-168">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b5b8b-168">OUTPUTS</span></span>

### <span data-ttu-id="b5b8b-169">Microsoft. WindowsAzure. Storage. File. CloudFileDirectory</span><span class="sxs-lookup"><span data-stu-id="b5b8b-169">Microsoft.WindowsAzure.Storage.File.CloudFileDirectory</span></span>

## <span data-ttu-id="b5b8b-170">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b5b8b-170">NOTES</span></span>

## <span data-ttu-id="b5b8b-171">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b5b8b-171">RELATED LINKS</span></span>

[<span data-ttu-id="b5b8b-172">Get-AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="b5b8b-172">Get-AzureStorageShare</span></span>](./Get-AzureStorageShare.md)

[<span data-ttu-id="b5b8b-173">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="b5b8b-173">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="b5b8b-174">New-AzureStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="b5b8b-174">New-AzureStorageDirectory</span></span>](./New-AzureStorageDirectory.md)
