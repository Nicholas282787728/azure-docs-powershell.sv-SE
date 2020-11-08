---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: C1648DC3-8CFD-4487-A080-D9BE25DAD258
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/get-azurestoragefilecopystate
schema: 2.0.0
ms.openlocfilehash: 61e633bc0890a8971b0be9d1b5950d990d32e8f4
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93930026"
---
# <span data-ttu-id="3b9ce-101">Get-AzureStorageFileCopyState</span><span class="sxs-lookup"><span data-stu-id="3b9ce-101">Get-AzureStorageFileCopyState</span></span>

## <span data-ttu-id="3b9ce-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3b9ce-102">SYNOPSIS</span></span>
<span data-ttu-id="3b9ce-103">Hämtar tillståndet för en kopiering.</span><span class="sxs-lookup"><span data-stu-id="3b9ce-103">Gets the state of a copy operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3b9ce-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3b9ce-104">SYNTAX</span></span>

### <span data-ttu-id="3b9ce-105">ShareName</span><span class="sxs-lookup"><span data-stu-id="3b9ce-105">ShareName</span></span>
```
Get-AzureStorageFileCopyState [-ShareName] <String> [-FilePath] <String> [-WaitForComplete]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="3b9ce-106">Fil</span><span class="sxs-lookup"><span data-stu-id="3b9ce-106">File</span></span>
```
Get-AzureStorageFileCopyState [-File] <CloudFile> [-WaitForComplete] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

## <span data-ttu-id="3b9ce-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3b9ce-107">DESCRIPTION</span></span>
<span data-ttu-id="3b9ce-108">Cmdleten **Get-AzureStorageFileCopyState** får statusen för en Azure Storage File Copy-åtgärd.</span><span class="sxs-lookup"><span data-stu-id="3b9ce-108">The **Get-AzureStorageFileCopyState** cmdlet gets the state of an Azure Storage file copy operation.</span></span>

## <span data-ttu-id="3b9ce-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3b9ce-109">EXAMPLES</span></span>

### <span data-ttu-id="3b9ce-110">Exempel 1: Hämta kopierings status efter fil namn</span><span class="sxs-lookup"><span data-stu-id="3b9ce-110">Example 1: Get the copy state by file name</span></span>
```
PS C:\>Get-AzureStorageFileCopyState -ShareName "ContosoShare" -FilePath "ContosoFile"
```

<span data-ttu-id="3b9ce-111">Det här kommandot får statusen för kopierings åtgärden för en fil som har det angivna namnet.</span><span class="sxs-lookup"><span data-stu-id="3b9ce-111">This command gets the state of the copy operation for a file that has the specified name.</span></span>

## <span data-ttu-id="3b9ce-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3b9ce-112">PARAMETERS</span></span>

### <span data-ttu-id="3b9ce-113">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="3b9ce-113">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="3b9ce-114">Anger tids gräns för klient sidan, i sekunder, för en tjänst förfrågan.</span><span class="sxs-lookup"><span data-stu-id="3b9ce-114">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="3b9ce-115">Om det föregående samtalet inte fungerar under det angivna intervallet, försöker den här cmdleten igen.</span><span class="sxs-lookup"><span data-stu-id="3b9ce-115">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="3b9ce-116">Om denna cmdlet inte får ett lyckat svar innan intervallet går ut returneras ett fel.</span><span class="sxs-lookup"><span data-stu-id="3b9ce-116">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="3b9ce-117">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="3b9ce-117">-ConcurrentTaskCount</span></span>
<span data-ttu-id="3b9ce-118">Anger maximalt antal samtidiga nätverks samtal.</span><span class="sxs-lookup"><span data-stu-id="3b9ce-118">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="3b9ce-119">Du kan använda den här parametern för att begränsa samtidigheten för att reglera den lokala processorn och bandbredds användning genom att ange det maximala antalet simultana nätverks samtal.</span><span class="sxs-lookup"><span data-stu-id="3b9ce-119">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="3b9ce-120">Det angivna värdet är ett absolut antal och multipliceras inte med antalet kärnor.</span><span class="sxs-lookup"><span data-stu-id="3b9ce-120">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="3b9ce-121">Den här parametern kan hjälpa till att minska nätverks anslutnings problem i miljöer med liten bandbredd, till exempel 100 kilobit per sekund.</span><span class="sxs-lookup"><span data-stu-id="3b9ce-121">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="3b9ce-122">Standardvärdet är 10.</span><span class="sxs-lookup"><span data-stu-id="3b9ce-122">The default value is 10.</span></span>

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

### <span data-ttu-id="3b9ce-123">-Kontext</span><span class="sxs-lookup"><span data-stu-id="3b9ce-123">-Context</span></span>
<span data-ttu-id="3b9ce-124">Anger en Azure Storage-kontext.</span><span class="sxs-lookup"><span data-stu-id="3b9ce-124">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="3b9ce-125">Använd cmdleten [New-AzureStorageContext](./New-AzureStorageContext.md) för att få en kontext.</span><span class="sxs-lookup"><span data-stu-id="3b9ce-125">To obtain a context, use the [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="3b9ce-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b9ce-126">-DefaultProfile</span></span>
<span data-ttu-id="3b9ce-127">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="3b9ce-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3b9ce-128">-Fil</span><span class="sxs-lookup"><span data-stu-id="3b9ce-128">-File</span></span>
<span data-ttu-id="3b9ce-129">Anger ett **CloudFile** -objekt.</span><span class="sxs-lookup"><span data-stu-id="3b9ce-129">Specifies a **CloudFile** object.</span></span>
<span data-ttu-id="3b9ce-130">Du kan skapa en moln fil eller skaffa en genom att använda Get-AzureStorageFile cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3b9ce-130">You can create a cloud file or obtain one by using the Get-AzureStorageFile cmdlet.</span></span>

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

### <span data-ttu-id="3b9ce-131">-Sökväg</span><span class="sxs-lookup"><span data-stu-id="3b9ce-131">-FilePath</span></span>
<span data-ttu-id="3b9ce-132">Anger sökvägen till filen i förhållande till en Azure Storage-resurs.</span><span class="sxs-lookup"><span data-stu-id="3b9ce-132">Specifies the path of the file relative to an Azure Storage share.</span></span>

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

### <span data-ttu-id="3b9ce-133">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="3b9ce-133">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="3b9ce-134">Anger längden på tids gränsen för en server del av en begäran.</span><span class="sxs-lookup"><span data-stu-id="3b9ce-134">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="3b9ce-135">-ShareName</span><span class="sxs-lookup"><span data-stu-id="3b9ce-135">-ShareName</span></span>
<span data-ttu-id="3b9ce-136">Anger namnet på en resurs.</span><span class="sxs-lookup"><span data-stu-id="3b9ce-136">Specifies the name of a share.</span></span>

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

### <span data-ttu-id="3b9ce-137">-WaitForComplete</span><span class="sxs-lookup"><span data-stu-id="3b9ce-137">-WaitForComplete</span></span>
<span data-ttu-id="3b9ce-138">Anger att denna cmdlet väntar på att kopieringen ska slutföras.</span><span class="sxs-lookup"><span data-stu-id="3b9ce-138">Indicates that this cmdlet waits for the copy to finish.</span></span>
<span data-ttu-id="3b9ce-139">Om du inte anger den här parametern returnerar denna cmdlet ett resultat omedelbart.</span><span class="sxs-lookup"><span data-stu-id="3b9ce-139">If you do not specify this parameter, this cmdlet returns a result immediately.</span></span>

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

### <span data-ttu-id="3b9ce-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b9ce-140">CommonParameters</span></span>
<span data-ttu-id="3b9ce-141">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3b9ce-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b9ce-142">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3b9ce-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b9ce-143">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3b9ce-143">INPUTS</span></span>

### <span data-ttu-id="3b9ce-144">Microsoft. WindowsAzure. Storage. File. CloudFile</span><span class="sxs-lookup"><span data-stu-id="3b9ce-144">Microsoft.WindowsAzure.Storage.File.CloudFile</span></span>
<span data-ttu-id="3b9ce-145">Parametrar: fil (ByValue)</span><span class="sxs-lookup"><span data-stu-id="3b9ce-145">Parameters: File (ByValue)</span></span>

### <span data-ttu-id="3b9ce-146">Microsoft. Azure. commands. Common. verifikation. abstraktioner. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="3b9ce-146">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="3b9ce-147">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3b9ce-147">OUTPUTS</span></span>

### <span data-ttu-id="3b9ce-148">Microsoft. WindowsAzure. Storage. File. CloudFile</span><span class="sxs-lookup"><span data-stu-id="3b9ce-148">Microsoft.WindowsAzure.Storage.File.CloudFile</span></span>

## <span data-ttu-id="3b9ce-149">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3b9ce-149">NOTES</span></span>

## <span data-ttu-id="3b9ce-150">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3b9ce-150">RELATED LINKS</span></span>

[<span data-ttu-id="3b9ce-151">Get-AzureStorageFile</span><span class="sxs-lookup"><span data-stu-id="3b9ce-151">Get-AzureStorageFile</span></span>](./Get-AzureStorageFile.md)

[<span data-ttu-id="3b9ce-152">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="3b9ce-152">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="3b9ce-153">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="3b9ce-153">Start-AzureStorageFileCopy</span></span>](./Start-AzureStorageFileCopy.md)

[<span data-ttu-id="3b9ce-154">Stopp-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="3b9ce-154">Stop-AzureStorageFileCopy</span></span>](./Stop-AzureStorageFileCopy.md)