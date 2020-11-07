---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: C1648DC3-8CFD-4487-A080-D9BE25DAD258
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstoragefilecopystate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageFileCopyState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageFileCopyState.md
ms.openlocfilehash: 8620045690b69d0e9829e240e99766c73ed43b6a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93746386"
---
# <span data-ttu-id="02538-101">Get-AzStorageFileCopyState</span><span class="sxs-lookup"><span data-stu-id="02538-101">Get-AzStorageFileCopyState</span></span>

## <span data-ttu-id="02538-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="02538-102">SYNOPSIS</span></span>
<span data-ttu-id="02538-103">Hämtar tillståndet för en kopiering.</span><span class="sxs-lookup"><span data-stu-id="02538-103">Gets the state of a copy operation.</span></span>

## <span data-ttu-id="02538-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="02538-104">SYNTAX</span></span>

### <span data-ttu-id="02538-105">ShareName</span><span class="sxs-lookup"><span data-stu-id="02538-105">ShareName</span></span>
```
Get-AzStorageFileCopyState [-ShareName] <String> [-FilePath] <String> [-WaitForComplete]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="02538-106">Fil</span><span class="sxs-lookup"><span data-stu-id="02538-106">File</span></span>
```
Get-AzStorageFileCopyState [-File] <CloudFile> [-WaitForComplete] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

## <span data-ttu-id="02538-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="02538-107">DESCRIPTION</span></span>
<span data-ttu-id="02538-108">Cmdleten **Get-AzStorageFileCopyState** får statusen för en Azure Storage File Copy-åtgärd.</span><span class="sxs-lookup"><span data-stu-id="02538-108">The **Get-AzStorageFileCopyState** cmdlet gets the state of an Azure Storage file copy operation.</span></span>

## <span data-ttu-id="02538-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="02538-109">EXAMPLES</span></span>

### <span data-ttu-id="02538-110">Exempel 1: Hämta kopierings status efter fil namn</span><span class="sxs-lookup"><span data-stu-id="02538-110">Example 1: Get the copy state by file name</span></span>
```
PS C:\>Get-AzStorageFileCopyState -ShareName "ContosoShare" -FilePath "ContosoFile"
```

<span data-ttu-id="02538-111">Det här kommandot får statusen för kopierings åtgärden för en fil som har det angivna namnet.</span><span class="sxs-lookup"><span data-stu-id="02538-111">This command gets the state of the copy operation for a file that has the specified name.</span></span>

## <span data-ttu-id="02538-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="02538-112">PARAMETERS</span></span>

### <span data-ttu-id="02538-113">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="02538-113">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="02538-114">Anger tids gräns för klient sidan, i sekunder, för en tjänst förfrågan.</span><span class="sxs-lookup"><span data-stu-id="02538-114">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="02538-115">Om det föregående samtalet inte fungerar under det angivna intervallet, försöker den här cmdleten igen.</span><span class="sxs-lookup"><span data-stu-id="02538-115">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="02538-116">Om denna cmdlet inte får ett lyckat svar innan intervallet går ut returneras ett fel.</span><span class="sxs-lookup"><span data-stu-id="02538-116">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="02538-117">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="02538-117">-ConcurrentTaskCount</span></span>
<span data-ttu-id="02538-118">Anger maximalt antal samtidiga nätverks samtal.</span><span class="sxs-lookup"><span data-stu-id="02538-118">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="02538-119">Du kan använda den här parametern för att begränsa samtidigheten för att reglera den lokala processorn och bandbredds användning genom att ange det maximala antalet simultana nätverks samtal.</span><span class="sxs-lookup"><span data-stu-id="02538-119">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="02538-120">Det angivna värdet är ett absolut antal och multipliceras inte med antalet kärnor.</span><span class="sxs-lookup"><span data-stu-id="02538-120">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="02538-121">Den här parametern kan hjälpa till att minska nätverks anslutnings problem i miljöer med liten bandbredd, till exempel 100 kilobit per sekund.</span><span class="sxs-lookup"><span data-stu-id="02538-121">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="02538-122">Standardvärdet är 10.</span><span class="sxs-lookup"><span data-stu-id="02538-122">The default value is 10.</span></span>

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

### <span data-ttu-id="02538-123">-Kontext</span><span class="sxs-lookup"><span data-stu-id="02538-123">-Context</span></span>
<span data-ttu-id="02538-124">Anger en Azure Storage-kontext.</span><span class="sxs-lookup"><span data-stu-id="02538-124">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="02538-125">Använd cmdleten [New-AzStorageContext](./New-AzStorageContext.md) för att få en kontext.</span><span class="sxs-lookup"><span data-stu-id="02538-125">To obtain a context, use the [New-AzStorageContext](./New-AzStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="02538-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02538-126">-DefaultProfile</span></span>
<span data-ttu-id="02538-127">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="02538-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="02538-128">-Fil</span><span class="sxs-lookup"><span data-stu-id="02538-128">-File</span></span>
<span data-ttu-id="02538-129">Anger ett **CloudFile** -objekt.</span><span class="sxs-lookup"><span data-stu-id="02538-129">Specifies a **CloudFile** object.</span></span>
<span data-ttu-id="02538-130">Du kan skapa en moln fil eller skaffa en genom att använda Get-AzStorageFile cmdlet.</span><span class="sxs-lookup"><span data-stu-id="02538-130">You can create a cloud file or obtain one by using the Get-AzStorageFile cmdlet.</span></span>

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

### <span data-ttu-id="02538-131">-Sökväg</span><span class="sxs-lookup"><span data-stu-id="02538-131">-FilePath</span></span>
<span data-ttu-id="02538-132">Anger sökvägen till filen i förhållande till en Azure Storage-resurs.</span><span class="sxs-lookup"><span data-stu-id="02538-132">Specifies the path of the file relative to an Azure Storage share.</span></span>

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

### <span data-ttu-id="02538-133">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="02538-133">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="02538-134">Anger längden på tids gränsen för en server del av en begäran.</span><span class="sxs-lookup"><span data-stu-id="02538-134">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="02538-135">-ShareName</span><span class="sxs-lookup"><span data-stu-id="02538-135">-ShareName</span></span>
<span data-ttu-id="02538-136">Anger namnet på en resurs.</span><span class="sxs-lookup"><span data-stu-id="02538-136">Specifies the name of a share.</span></span>

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

### <span data-ttu-id="02538-137">-WaitForComplete</span><span class="sxs-lookup"><span data-stu-id="02538-137">-WaitForComplete</span></span>
<span data-ttu-id="02538-138">Anger att denna cmdlet väntar på att kopieringen ska slutföras.</span><span class="sxs-lookup"><span data-stu-id="02538-138">Indicates that this cmdlet waits for the copy to finish.</span></span>
<span data-ttu-id="02538-139">Om du inte anger den här parametern returnerar denna cmdlet ett resultat omedelbart.</span><span class="sxs-lookup"><span data-stu-id="02538-139">If you do not specify this parameter, this cmdlet returns a result immediately.</span></span>

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

### <span data-ttu-id="02538-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02538-140">CommonParameters</span></span>
<span data-ttu-id="02538-141">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="02538-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02538-142">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="02538-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02538-143">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="02538-143">INPUTS</span></span>

### <span data-ttu-id="02538-144">Microsoft. WindowsAzure. Storage. File. CloudFile</span><span class="sxs-lookup"><span data-stu-id="02538-144">Microsoft.WindowsAzure.Storage.File.CloudFile</span></span>

### <span data-ttu-id="02538-145">Microsoft. Azure. commands. Common. verifikation. abstraktioner. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="02538-145">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="02538-146">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="02538-146">OUTPUTS</span></span>

### <span data-ttu-id="02538-147">Microsoft. WindowsAzure. Storage. File. CloudFile</span><span class="sxs-lookup"><span data-stu-id="02538-147">Microsoft.WindowsAzure.Storage.File.CloudFile</span></span>

## <span data-ttu-id="02538-148">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="02538-148">NOTES</span></span>

## <span data-ttu-id="02538-149">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="02538-149">RELATED LINKS</span></span>

[<span data-ttu-id="02538-150">Get-AzStorageFile</span><span class="sxs-lookup"><span data-stu-id="02538-150">Get-AzStorageFile</span></span>](./Get-AzStorageFile.md)

[<span data-ttu-id="02538-151">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="02538-151">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="02538-152">Start-AzStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="02538-152">Start-AzStorageFileCopy</span></span>](./Start-AzStorageFileCopy.md)

[<span data-ttu-id="02538-153">Stopp-AzStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="02538-153">Stop-AzStorageFileCopy</span></span>](./Stop-AzStorageFileCopy.md)
