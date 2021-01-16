---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 53988D79-1F8B-4138-9F92-2912D418C121
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azstoragedirectory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageDirectory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageDirectory.md
ms.openlocfilehash: 3ac8cb302c65fd42fdd699588b71bc1b081cc9d2
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98522006"
---
# <span data-ttu-id="303ab-101">Remove-AzStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="303ab-101">Remove-AzStorageDirectory</span></span>

## <span data-ttu-id="303ab-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="303ab-102">SYNOPSIS</span></span>
<span data-ttu-id="303ab-103">Tar bort en katalog.</span><span class="sxs-lookup"><span data-stu-id="303ab-103">Deletes a directory.</span></span>

## <span data-ttu-id="303ab-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="303ab-104">SYNTAX</span></span>

### <span data-ttu-id="303ab-105">Resurs namn (standard)</span><span class="sxs-lookup"><span data-stu-id="303ab-105">ShareName (Default)</span></span>
```
Remove-AzStorageDirectory [-ShareName] <String> [-Path] <String> [-PassThru] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="303ab-106">Resurserna</span><span class="sxs-lookup"><span data-stu-id="303ab-106">Share</span></span>
```
Remove-AzStorageDirectory [-Share] <CloudFileShare> [-Path] <String> [-PassThru]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="303ab-107">Katalogen</span><span class="sxs-lookup"><span data-stu-id="303ab-107">Directory</span></span>
```
Remove-AzStorageDirectory [-Directory] <CloudFileDirectory> [[-Path] <String>] [-PassThru]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="303ab-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="303ab-108">DESCRIPTION</span></span>
<span data-ttu-id="303ab-109">Cmdleten **Remove-AzStorageDirectory** tar bort en katalog.</span><span class="sxs-lookup"><span data-stu-id="303ab-109">The **Remove-AzStorageDirectory** cmdlet deletes a directory.</span></span>

## <span data-ttu-id="303ab-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="303ab-110">EXAMPLES</span></span>

### <span data-ttu-id="303ab-111">Exempel 1: ta bort en mapp</span><span class="sxs-lookup"><span data-stu-id="303ab-111">Example 1: Delete a folder</span></span>
```
PS C:\>Remove-AzStorageDirectory -ShareName "ContosoShare06" -Path "ContosoWorkingFolder"
```

<span data-ttu-id="303ab-112">Det här kommandot tar bort mappen som heter ContosoWorkingFolder från fil resursen med namnet ContosoShare06.</span><span class="sxs-lookup"><span data-stu-id="303ab-112">This command deletes the folder named ContosoWorkingFolder from the file share named ContosoShare06.</span></span>

## <span data-ttu-id="303ab-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="303ab-113">PARAMETERS</span></span>

### <span data-ttu-id="303ab-114">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="303ab-114">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="303ab-115">Anger tids gräns för klient sidan, i sekunder, för en tjänst förfrågan.</span><span class="sxs-lookup"><span data-stu-id="303ab-115">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="303ab-116">Om det föregående samtalet inte fungerar under det angivna intervallet, försöker den här cmdleten igen.</span><span class="sxs-lookup"><span data-stu-id="303ab-116">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="303ab-117">Om denna cmdlet inte får ett lyckat svar innan intervallet går ut returneras ett fel.</span><span class="sxs-lookup"><span data-stu-id="303ab-117">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="303ab-118">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="303ab-118">-ConcurrentTaskCount</span></span>
<span data-ttu-id="303ab-119">Anger maximalt antal samtidiga nätverks samtal.</span><span class="sxs-lookup"><span data-stu-id="303ab-119">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="303ab-120">Du kan använda den här parametern för att begränsa samtidigheten för att reglera den lokala processorn och bandbredds användning genom att ange det maximala antalet simultana nätverks samtal.</span><span class="sxs-lookup"><span data-stu-id="303ab-120">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="303ab-121">Det angivna värdet är ett absolut antal och multipliceras inte med antalet kärnor.</span><span class="sxs-lookup"><span data-stu-id="303ab-121">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="303ab-122">Den här parametern kan hjälpa till att minska nätverks anslutnings problem i miljöer med liten bandbredd, till exempel 100 kilobit per sekund.</span><span class="sxs-lookup"><span data-stu-id="303ab-122">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="303ab-123">Standardvärdet är 10.</span><span class="sxs-lookup"><span data-stu-id="303ab-123">The default value is 10.</span></span>

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

### <span data-ttu-id="303ab-124">-Kontext</span><span class="sxs-lookup"><span data-stu-id="303ab-124">-Context</span></span>
<span data-ttu-id="303ab-125">Anger en Azure Storage-kontext.</span><span class="sxs-lookup"><span data-stu-id="303ab-125">Specifies an Azure storage context.</span></span>
<span data-ttu-id="303ab-126">Använd cmdleten [New-AzStorageContext](./New-AzStorageContext.md) för att få en lagrings kontext.</span><span class="sxs-lookup"><span data-stu-id="303ab-126">To obtain a storage context, use the [New-AzStorageContext](./New-AzStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="303ab-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="303ab-127">-DefaultProfile</span></span>
<span data-ttu-id="303ab-128">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="303ab-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="303ab-129">-Katalog</span><span class="sxs-lookup"><span data-stu-id="303ab-129">-Directory</span></span>
<span data-ttu-id="303ab-130">Anger en mapp som ett **CloudFileDirectory** -objekt.</span><span class="sxs-lookup"><span data-stu-id="303ab-130">Specifies a folder as a **CloudFileDirectory** object.</span></span>
<span data-ttu-id="303ab-131">Denna cmdlet tar bort den mapp som anges i den här parametern.</span><span class="sxs-lookup"><span data-stu-id="303ab-131">This cmdlet removes the folder that this parameter specifies.</span></span>
<span data-ttu-id="303ab-132">Använd New-AzStorageDirectory cmdlet för att få en katalog.</span><span class="sxs-lookup"><span data-stu-id="303ab-132">To obtain a directory, use the New-AzStorageDirectory cmdlet.</span></span>
<span data-ttu-id="303ab-133">Du kan också använda cmdleten **Get-AzStorageFile** för att få en katalog.</span><span class="sxs-lookup"><span data-stu-id="303ab-133">You can also use the **Get-AzStorageFile** cmdlet to obtain a directory.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFileDirectory
Parameter Sets: Directory
Aliases: CloudFileDirectory

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="303ab-134">-PassThru</span><span class="sxs-lookup"><span data-stu-id="303ab-134">-PassThru</span></span>
<span data-ttu-id="303ab-135">Anger att om denna cmdlet lyckas returneras ett värde för $True.</span><span class="sxs-lookup"><span data-stu-id="303ab-135">Indicates that, if this cmdlet succeeds, it returns a value of $True.</span></span>
<span data-ttu-id="303ab-136">Om du anger den här parametern och om cmdleten Miss lyckas på grund av ett olämpligt värde för parametern _Path_ returneras ett fel.</span><span class="sxs-lookup"><span data-stu-id="303ab-136">If you specify this parameter, and if the cmdlet is unsuccessful because of an inappropriate value for the _Path_ parameter, the cmdlet returns an error.</span></span>
<span data-ttu-id="303ab-137">Om du inte anger den här parametern returnerar denna cmdlet inte ett värde.</span><span class="sxs-lookup"><span data-stu-id="303ab-137">If you do not specify this parameter, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="303ab-138">-Path</span><span class="sxs-lookup"><span data-stu-id="303ab-138">-Path</span></span>
<span data-ttu-id="303ab-139">Anger sökvägen till en mapp.</span><span class="sxs-lookup"><span data-stu-id="303ab-139">Specifies the path of a folder.</span></span>
<span data-ttu-id="303ab-140">Om mappen som den här parametern anger är tom tar denna cmdlet bort den mappen.</span><span class="sxs-lookup"><span data-stu-id="303ab-140">If the folder that this parameter specifies is empty, this cmdlet deletes that folder.</span></span>
<span data-ttu-id="303ab-141">Om mappen inte är tom gör denna cmdlet ingen ändring och returnerar ett fel.</span><span class="sxs-lookup"><span data-stu-id="303ab-141">If the folder is not empty, this cmdlet makes no change, and returns an error.</span></span>

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

### <span data-ttu-id="303ab-142">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="303ab-142">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="303ab-143">Anger längden på tids gränsen för en server del av en begäran.</span><span class="sxs-lookup"><span data-stu-id="303ab-143">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="303ab-144">-Dela</span><span class="sxs-lookup"><span data-stu-id="303ab-144">-Share</span></span>
<span data-ttu-id="303ab-145">Anger ett **CloudFileShare** -objekt.</span><span class="sxs-lookup"><span data-stu-id="303ab-145">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="303ab-146">Denna cmdlet tar bort en mapp under fil resursen som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="303ab-146">This cmdlet removes a folder under the file share that this parameter specifies.</span></span>
<span data-ttu-id="303ab-147">För att hämta ett **CloudFileShare** -objekt, Använd cmdleten Get-AzStorageShare.</span><span class="sxs-lookup"><span data-stu-id="303ab-147">To obtain a **CloudFileShare** object, use the Get-AzStorageShare cmdlet.</span></span>
<span data-ttu-id="303ab-148">Det här objektet innehåller lagrings kontexten.</span><span class="sxs-lookup"><span data-stu-id="303ab-148">This object contains the storage context.</span></span>
<span data-ttu-id="303ab-149">Om du anger den här parametern ska du inte ange en *kontext* parameter.</span><span class="sxs-lookup"><span data-stu-id="303ab-149">If you specify this parameter, do not specify the *Context* parameter.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFileShare
Parameter Sets: Share
Aliases: CloudFileShare

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="303ab-150">-ShareName</span><span class="sxs-lookup"><span data-stu-id="303ab-150">-ShareName</span></span>
<span data-ttu-id="303ab-151">Anger namnet på fil resursen.</span><span class="sxs-lookup"><span data-stu-id="303ab-151">Specifies the name of the file share.</span></span>
<span data-ttu-id="303ab-152">Denna cmdlet tar bort en mapp under fil resursen som den här parametern anger.</span><span class="sxs-lookup"><span data-stu-id="303ab-152">This cmdlet removes a folder under the file share that this parameter specifies.</span></span>

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

### <span data-ttu-id="303ab-153">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="303ab-153">-Confirm</span></span>
<span data-ttu-id="303ab-154">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="303ab-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="303ab-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="303ab-155">-WhatIf</span></span>
<span data-ttu-id="303ab-156">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="303ab-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="303ab-157">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="303ab-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="303ab-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="303ab-158">CommonParameters</span></span>
<span data-ttu-id="303ab-159">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="303ab-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="303ab-160">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="303ab-160">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="303ab-161">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="303ab-161">INPUTS</span></span>

### <span data-ttu-id="303ab-162">Microsoft. Azure. Storage. File. CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="303ab-162">Microsoft.Azure.Storage.File.CloudFileShare</span></span>

### <span data-ttu-id="303ab-163">Microsoft. Azure. Storage. File. CloudFileDirectory</span><span class="sxs-lookup"><span data-stu-id="303ab-163">Microsoft.Azure.Storage.File.CloudFileDirectory</span></span>

### <span data-ttu-id="303ab-164">System. String</span><span class="sxs-lookup"><span data-stu-id="303ab-164">System.String</span></span>

### <span data-ttu-id="303ab-165">Microsoft. Azure. commands. Common. verifikation. abstraktioner. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="303ab-165">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="303ab-166">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="303ab-166">OUTPUTS</span></span>

### <span data-ttu-id="303ab-167">Microsoft. WindowsAzure. commands. Common. Storage. ResourceModel. AzureStorageFileDirectory</span><span class="sxs-lookup"><span data-stu-id="303ab-167">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageFileDirectory</span></span>

## <span data-ttu-id="303ab-168">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="303ab-168">NOTES</span></span>

## <span data-ttu-id="303ab-169">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="303ab-169">RELATED LINKS</span></span>

[<span data-ttu-id="303ab-170">Get-AzStorageShare</span><span class="sxs-lookup"><span data-stu-id="303ab-170">Get-AzStorageShare</span></span>](./Get-AzStorageShare.md)

[<span data-ttu-id="303ab-171">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="303ab-171">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="303ab-172">New-AzStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="303ab-172">New-AzStorageDirectory</span></span>](./New-AzStorageDirectory.md)
