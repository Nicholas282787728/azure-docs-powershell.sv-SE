---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: 3AC3F8DE-E25D-41AE-9083-5C459A4C8CD0
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/stop-azurestoragefilecopy
schema: 2.0.0
ms.openlocfilehash: c0db10c24f019a9f91efd4ad9ec6805ffc3b0208
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93928925"
---
# <span data-ttu-id="c5364-101">Stop-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="c5364-101">Stop-AzureStorageFileCopy</span></span>

## <span data-ttu-id="c5364-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c5364-102">SYNOPSIS</span></span>
<span data-ttu-id="c5364-103">Stoppar en kopierings åtgärd till angiven målfil.</span><span class="sxs-lookup"><span data-stu-id="c5364-103">Stops a copy operation to the specified destination file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c5364-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c5364-104">SYNTAX</span></span>

### <span data-ttu-id="c5364-105">ShareName</span><span class="sxs-lookup"><span data-stu-id="c5364-105">ShareName</span></span>
```
Stop-AzureStorageFileCopy [-ShareName] <String> [-FilePath] <String> [-CopyId <String>] [-Force]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c5364-106">Fil</span><span class="sxs-lookup"><span data-stu-id="c5364-106">File</span></span>
```
Stop-AzureStorageFileCopy [-File] <CloudFile> [-CopyId <String>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c5364-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c5364-107">DESCRIPTION</span></span>
<span data-ttu-id="c5364-108">Cmdleten **Stop-AzureStorageFileCopy** slutar kopiera en fil till en målfil.</span><span class="sxs-lookup"><span data-stu-id="c5364-108">The **Stop-AzureStorageFileCopy** cmdlet stops copying a file to a destination file.</span></span>

## <span data-ttu-id="c5364-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c5364-109">EXAMPLES</span></span>

### <span data-ttu-id="c5364-110">Exempel 1: stoppa en kopiering</span><span class="sxs-lookup"><span data-stu-id="c5364-110">Example 1: Stop a copy operation</span></span>
```
PS C:\>Stop-AzureStorageFileCopy -ShareName "ContosoShare" -FilePath "FilePath" -CopyId "CopyId"
```

<span data-ttu-id="c5364-111">Det här kommandot avslutar kopiering av en fil med det angivna namnet.</span><span class="sxs-lookup"><span data-stu-id="c5364-111">This command stops copying a file that has the specified name.</span></span>

## <span data-ttu-id="c5364-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c5364-112">PARAMETERS</span></span>

### <span data-ttu-id="c5364-113">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="c5364-113">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="c5364-114">Anger tids gräns för klient sidan, i sekunder, för en tjänst förfrågan.</span><span class="sxs-lookup"><span data-stu-id="c5364-114">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="c5364-115">Om det föregående samtalet inte fungerar under det angivna intervallet, försöker den här cmdleten igen.</span><span class="sxs-lookup"><span data-stu-id="c5364-115">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="c5364-116">Om denna cmdlet inte får ett lyckat svar innan intervallet går ut returneras ett fel.</span><span class="sxs-lookup"><span data-stu-id="c5364-116">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="c5364-117">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="c5364-117">-ConcurrentTaskCount</span></span>
<span data-ttu-id="c5364-118">Anger maximalt antal samtidiga nätverks samtal.</span><span class="sxs-lookup"><span data-stu-id="c5364-118">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="c5364-119">Du kan använda den här parametern för att begränsa samtidigheten för att reglera den lokala processorn och bandbredds användning genom att ange det maximala antalet simultana nätverks samtal.</span><span class="sxs-lookup"><span data-stu-id="c5364-119">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="c5364-120">Det angivna värdet är ett absolut antal och multipliceras inte med antalet kärnor.</span><span class="sxs-lookup"><span data-stu-id="c5364-120">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="c5364-121">Den här parametern kan hjälpa till att minska nätverks anslutnings problem i miljöer med liten bandbredd, till exempel 100 kilobit per sekund.</span><span class="sxs-lookup"><span data-stu-id="c5364-121">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="c5364-122">Standardvärdet är 10.</span><span class="sxs-lookup"><span data-stu-id="c5364-122">The default value is 10.</span></span>

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

### <span data-ttu-id="c5364-123">-Kontext</span><span class="sxs-lookup"><span data-stu-id="c5364-123">-Context</span></span>
<span data-ttu-id="c5364-124">Anger en Azure Storage-kontext.</span><span class="sxs-lookup"><span data-stu-id="c5364-124">Specifies an Azure storage context.</span></span>
<span data-ttu-id="c5364-125">Använd cmdleten [New-AzureStorageContext](./New-AzureStorageContext.md) för att få en lagrings kontext.</span><span class="sxs-lookup"><span data-stu-id="c5364-125">To obtain a storage context, use the [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="c5364-126">-CopyId</span><span class="sxs-lookup"><span data-stu-id="c5364-126">-CopyId</span></span>
<span data-ttu-id="c5364-127">Anger ID för kopierings åtgärden.</span><span class="sxs-lookup"><span data-stu-id="c5364-127">Specifies the ID of the copy operation.</span></span>

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

### <span data-ttu-id="c5364-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5364-128">-DefaultProfile</span></span>
<span data-ttu-id="c5364-129">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c5364-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c5364-130">-Fil</span><span class="sxs-lookup"><span data-stu-id="c5364-130">-File</span></span>
<span data-ttu-id="c5364-131">Anger ett **CloudFile** -objekt.</span><span class="sxs-lookup"><span data-stu-id="c5364-131">Specifies a **CloudFile** object.</span></span>
<span data-ttu-id="c5364-132">Du kan skapa en moln fil eller skaffa en genom att använda Get-AzureStorageFile cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c5364-132">You can create a cloud file or obtain one by using the Get-AzureStorageFile cmdlet.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.File.CloudFile
Parameter Sets: File
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c5364-133">-Sökväg</span><span class="sxs-lookup"><span data-stu-id="c5364-133">-FilePath</span></span>
<span data-ttu-id="c5364-134">Anger sökvägen till en fil.</span><span class="sxs-lookup"><span data-stu-id="c5364-134">Specifies the path of a file.</span></span>

```yaml
Type: System.String
Parameter Sets: ShareName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5364-135">-Force</span><span class="sxs-lookup"><span data-stu-id="c5364-135">-Force</span></span>
<span data-ttu-id="c5364-136">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="c5364-136">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="c5364-137">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="c5364-137">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="c5364-138">Anger längden på tids gränsen för en server del av en begäran.</span><span class="sxs-lookup"><span data-stu-id="c5364-138">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="c5364-139">-ShareName</span><span class="sxs-lookup"><span data-stu-id="c5364-139">-ShareName</span></span>
<span data-ttu-id="c5364-140">Anger namnet på en resurs.</span><span class="sxs-lookup"><span data-stu-id="c5364-140">Specifies the name of a share.</span></span>

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

### <span data-ttu-id="c5364-141">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="c5364-141">-Confirm</span></span>
<span data-ttu-id="c5364-142">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="c5364-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c5364-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c5364-143">-WhatIf</span></span>
<span data-ttu-id="c5364-144">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="c5364-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c5364-145">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="c5364-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c5364-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5364-146">CommonParameters</span></span>
<span data-ttu-id="c5364-147">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c5364-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5364-148">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c5364-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5364-149">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c5364-149">INPUTS</span></span>

### <span data-ttu-id="c5364-150">Microsoft. WindowsAzure. Storage. File. CloudFile</span><span class="sxs-lookup"><span data-stu-id="c5364-150">Microsoft.WindowsAzure.Storage.File.CloudFile</span></span>
<span data-ttu-id="c5364-151">Parametrar: fil (ByValue)</span><span class="sxs-lookup"><span data-stu-id="c5364-151">Parameters: File (ByValue)</span></span>

### <span data-ttu-id="c5364-152">Microsoft. Azure. commands. Common. verifikation. abstraktioner. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="c5364-152">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="c5364-153">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c5364-153">OUTPUTS</span></span>

### <span data-ttu-id="c5364-154">System. Void</span><span class="sxs-lookup"><span data-stu-id="c5364-154">System.Void</span></span>

## <span data-ttu-id="c5364-155">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c5364-155">NOTES</span></span>

## <span data-ttu-id="c5364-156">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c5364-156">RELATED LINKS</span></span>

[<span data-ttu-id="c5364-157">Get-AzureStorageFile</span><span class="sxs-lookup"><span data-stu-id="c5364-157">Get-AzureStorageFile</span></span>](./Get-AzureStorageFile.md)

[<span data-ttu-id="c5364-158">Get-AzureStorageFileCopyState</span><span class="sxs-lookup"><span data-stu-id="c5364-158">Get-AzureStorageFileCopyState</span></span>](./Get-AzureStorageFileCopyState.md)

[<span data-ttu-id="c5364-159">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="c5364-159">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="c5364-160">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="c5364-160">Start-AzureStorageFileCopy</span></span>](./Start-AzureStorageFileCopy.md)