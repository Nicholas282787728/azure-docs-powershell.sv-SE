---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: FF3AD436-CA33-4A52-8580-D2345D80A231
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/remove-azurestorageshare
schema: 2.0.0
ms.openlocfilehash: 07ab4071d89e1ba97d4c824bd98012fae70a79de
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93931073"
---
# <span data-ttu-id="a96f5-101">Remove-AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="a96f5-101">Remove-AzureStorageShare</span></span>

## <span data-ttu-id="a96f5-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a96f5-102">SYNOPSIS</span></span>
<span data-ttu-id="a96f5-103">Tar bort en fil resurs.</span><span class="sxs-lookup"><span data-stu-id="a96f5-103">Deletes a file share.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a96f5-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a96f5-104">SYNTAX</span></span>

### <span data-ttu-id="a96f5-105">Resurs namn (standard)</span><span class="sxs-lookup"><span data-stu-id="a96f5-105">ShareName (Default)</span></span>
```
Remove-AzureStorageShare [-Name] <String> [-IncludeAllSnapshot] [-Force] [-PassThru]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a96f5-106">Resurserna</span><span class="sxs-lookup"><span data-stu-id="a96f5-106">Share</span></span>
```
Remove-AzureStorageShare [-Share] <CloudFileShare> [-IncludeAllSnapshot] [-Force] [-PassThru]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a96f5-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a96f5-107">DESCRIPTION</span></span>
<span data-ttu-id="a96f5-108">Cmdleten **Remove-AzureStorageShare** tar bort en fil resurs.</span><span class="sxs-lookup"><span data-stu-id="a96f5-108">The **Remove-AzureStorageShare** cmdlet deletes a file share.</span></span>

## <span data-ttu-id="a96f5-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a96f5-109">EXAMPLES</span></span>

### <span data-ttu-id="a96f5-110">Exempel 1: ta bort en fil resurs</span><span class="sxs-lookup"><span data-stu-id="a96f5-110">Example 1: Remove a file share</span></span>
```
PS C:\>Remove-AzureStorageShare -Name "ContosoShare06"
```

<span data-ttu-id="a96f5-111">Det här kommandot tar bort fil resursen som heter ContosoShare06.</span><span class="sxs-lookup"><span data-stu-id="a96f5-111">This command removes the file share named ContosoShare06.</span></span>

### <span data-ttu-id="a96f5-112">Exempel 2: ta bort en fil resurs och alla dess stillbilder</span><span class="sxs-lookup"><span data-stu-id="a96f5-112">Example 2: Remove a file share and all its snapshots</span></span>
```
PS C:\>Remove-AzureStorageShare -Name "ContosoShare06" -IncludeAllSnapshot
```

<span data-ttu-id="a96f5-113">Det här kommandot tar bort fil resursen med namnet ContosoShare06 och alla dess stillbilder.</span><span class="sxs-lookup"><span data-stu-id="a96f5-113">This command removes the file share named ContosoShare06 and all its snapshots.</span></span>

## <span data-ttu-id="a96f5-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a96f5-114">PARAMETERS</span></span>

### <span data-ttu-id="a96f5-115">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="a96f5-115">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="a96f5-116">Anger tids gräns för klient sidan, i sekunder, för en tjänst förfrågan.</span><span class="sxs-lookup"><span data-stu-id="a96f5-116">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="a96f5-117">Om det föregående samtalet inte fungerar under det angivna intervallet, försöker den här cmdleten igen.</span><span class="sxs-lookup"><span data-stu-id="a96f5-117">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="a96f5-118">Om denna cmdlet inte får ett lyckat svar innan intervallet går ut returneras ett fel.</span><span class="sxs-lookup"><span data-stu-id="a96f5-118">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="a96f5-119">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="a96f5-119">-ConcurrentTaskCount</span></span>
<span data-ttu-id="a96f5-120">Anger maximalt antal samtidiga nätverks samtal.</span><span class="sxs-lookup"><span data-stu-id="a96f5-120">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="a96f5-121">Du kan använda den här parametern för att begränsa samtidigheten för att reglera den lokala processorn och bandbredds användning genom att ange det maximala antalet simultana nätverks samtal.</span><span class="sxs-lookup"><span data-stu-id="a96f5-121">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="a96f5-122">Det angivna värdet är ett absolut antal och multipliceras inte med antalet kärnor.</span><span class="sxs-lookup"><span data-stu-id="a96f5-122">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="a96f5-123">Den här parametern kan hjälpa till att minska nätverks anslutnings problem i miljöer med liten bandbredd, till exempel 100 kilobit per sekund.</span><span class="sxs-lookup"><span data-stu-id="a96f5-123">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="a96f5-124">Standardvärdet är 10.</span><span class="sxs-lookup"><span data-stu-id="a96f5-124">The default value is 10.</span></span>

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

### <span data-ttu-id="a96f5-125">-Kontext</span><span class="sxs-lookup"><span data-stu-id="a96f5-125">-Context</span></span>
<span data-ttu-id="a96f5-126">Anger en Azure Storage-kontext.</span><span class="sxs-lookup"><span data-stu-id="a96f5-126">Specifies an Azure storage context.</span></span>
<span data-ttu-id="a96f5-127">Använd cmdleten [New-AzureStorageContext](./New-AzureStorageContext.md) för att få en lagrings kontext.</span><span class="sxs-lookup"><span data-stu-id="a96f5-127">To obtain a storage context, use the [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="a96f5-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a96f5-128">-DefaultProfile</span></span>
<span data-ttu-id="a96f5-129">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a96f5-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a96f5-130">-Force</span><span class="sxs-lookup"><span data-stu-id="a96f5-130">-Force</span></span>
<span data-ttu-id="a96f5-131">Tvinga att ta bort resursen med alla dess stillbilder samt allt innehåll.</span><span class="sxs-lookup"><span data-stu-id="a96f5-131">Force to remove the share with all of its snapshots, and all content.</span></span>

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

### <span data-ttu-id="a96f5-132">-IncludeAllSnapshot</span><span class="sxs-lookup"><span data-stu-id="a96f5-132">-IncludeAllSnapshot</span></span>
<span data-ttu-id="a96f5-133">Ta bort fil resursen med alla stillbilder</span><span class="sxs-lookup"><span data-stu-id="a96f5-133">Remove File Share with all of its snapshots</span></span>

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

### <span data-ttu-id="a96f5-134">-Namn</span><span class="sxs-lookup"><span data-stu-id="a96f5-134">-Name</span></span>
<span data-ttu-id="a96f5-135">Anger namnet på fil resursen.</span><span class="sxs-lookup"><span data-stu-id="a96f5-135">Specifies the name of the file share.</span></span>
<span data-ttu-id="a96f5-136">Denna cmdlet tar bort fil resursen som anges av den här parametern.</span><span class="sxs-lookup"><span data-stu-id="a96f5-136">This cmdlet deletes the file share that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ShareName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a96f5-137">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a96f5-137">-PassThru</span></span>
<span data-ttu-id="a96f5-138">Anger att denna cmdlet returnerar ett **booleskt** värde som visar att åtgärden lyckades.</span><span class="sxs-lookup"><span data-stu-id="a96f5-138">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="a96f5-139">Denna cmdlet returnerar som standard inget värde.</span><span class="sxs-lookup"><span data-stu-id="a96f5-139">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="a96f5-140">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="a96f5-140">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="a96f5-141">Anger längden på tids gränsen för en server del av en begäran.</span><span class="sxs-lookup"><span data-stu-id="a96f5-141">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="a96f5-142">-Dela</span><span class="sxs-lookup"><span data-stu-id="a96f5-142">-Share</span></span>
<span data-ttu-id="a96f5-143">Anger ett **CloudFileShare** -objekt.</span><span class="sxs-lookup"><span data-stu-id="a96f5-143">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="a96f5-144">Denna cmdlet tar bort det objekt som anges av den här parametern.</span><span class="sxs-lookup"><span data-stu-id="a96f5-144">This cmdlet removes the object that this parameter specifies.</span></span>
<span data-ttu-id="a96f5-145">För att hämta ett **CloudFileShare** -objekt, Använd cmdleten Get-AzureStorageShare.</span><span class="sxs-lookup"><span data-stu-id="a96f5-145">To obtain a **CloudFileShare** object, use the Get-AzureStorageShare cmdlet.</span></span>
<span data-ttu-id="a96f5-146">Det här objektet innehåller lagrings kontexten.</span><span class="sxs-lookup"><span data-stu-id="a96f5-146">This object contains the storage context.</span></span>
<span data-ttu-id="a96f5-147">Om du anger den här parametern ska du inte ange en *kontext* parameter.</span><span class="sxs-lookup"><span data-stu-id="a96f5-147">If you specify this parameter, do not specify the *Context* parameter.</span></span>

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

### <span data-ttu-id="a96f5-148">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="a96f5-148">-Confirm</span></span>
<span data-ttu-id="a96f5-149">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="a96f5-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a96f5-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a96f5-150">-WhatIf</span></span>
<span data-ttu-id="a96f5-151">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="a96f5-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a96f5-152">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="a96f5-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a96f5-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a96f5-153">CommonParameters</span></span>
<span data-ttu-id="a96f5-154">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a96f5-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a96f5-155">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a96f5-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a96f5-156">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a96f5-156">INPUTS</span></span>

### <span data-ttu-id="a96f5-157">System. String</span><span class="sxs-lookup"><span data-stu-id="a96f5-157">System.String</span></span>

### <span data-ttu-id="a96f5-158">Microsoft. WindowsAzure. Storage. File. CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="a96f5-158">Microsoft.WindowsAzure.Storage.File.CloudFileShare</span></span>
<span data-ttu-id="a96f5-159">Parametrar: dela (ByValue)</span><span class="sxs-lookup"><span data-stu-id="a96f5-159">Parameters: Share (ByValue)</span></span>

### <span data-ttu-id="a96f5-160">Microsoft. Azure. commands. Common. verifikation. abstraktioner. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="a96f5-160">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="a96f5-161">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a96f5-161">OUTPUTS</span></span>

### <span data-ttu-id="a96f5-162">Microsoft. WindowsAzure. Storage. File. CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="a96f5-162">Microsoft.WindowsAzure.Storage.File.CloudFileShare</span></span>

## <span data-ttu-id="a96f5-163">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a96f5-163">NOTES</span></span>

## <span data-ttu-id="a96f5-164">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a96f5-164">RELATED LINKS</span></span>

[<span data-ttu-id="a96f5-165">Get-AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="a96f5-165">Get-AzureStorageShare</span></span>](./Get-AzureStorageShare.md)

[<span data-ttu-id="a96f5-166">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="a96f5-166">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="a96f5-167">New-AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="a96f5-167">New-AzureStorageShare</span></span>](./New-AzureStorageShare.md)
