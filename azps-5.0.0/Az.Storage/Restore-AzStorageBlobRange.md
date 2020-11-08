---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/restore-azstorageblobrange
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Restore-AzStorageBlobRange.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Restore-AzStorageBlobRange.md
ms.openlocfilehash: ee8a8bd6a12d3f4aa1dc1624d0dc5c11de972b11
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94269017"
---
# <span data-ttu-id="6d575-101">Restore-AzStorageBlobRange</span><span class="sxs-lookup"><span data-stu-id="6d575-101">Restore-AzStorageBlobRange</span></span>

## <span data-ttu-id="6d575-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6d575-102">SYNOPSIS</span></span>
<span data-ttu-id="6d575-103">Återställer ett lagrings konto för specifika BLOB-intervall.</span><span class="sxs-lookup"><span data-stu-id="6d575-103">Restores a Storage account for specific blob ranges.</span></span>

## <span data-ttu-id="6d575-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6d575-104">SYNTAX</span></span>

### <span data-ttu-id="6d575-105">AccountName (standard)</span><span class="sxs-lookup"><span data-stu-id="6d575-105">AccountName (Default)</span></span>
```
Restore-AzStorageBlobRange [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -TimeToRestore <DateTime> [-BlobRestoreRange <PSBlobRestoreRange[]>] [-WaitForComplete] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6d575-106">AccountResourceId</span><span class="sxs-lookup"><span data-stu-id="6d575-106">AccountResourceId</span></span>
```
Restore-AzStorageBlobRange [-ResourceId] <String> -TimeToRestore <DateTime>
 [-BlobRestoreRange <PSBlobRestoreRange[]>] [-WaitForComplete] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6d575-107">AccountObject</span><span class="sxs-lookup"><span data-stu-id="6d575-107">AccountObject</span></span>
```
Restore-AzStorageBlobRange -StorageAccount <PSStorageAccount> -TimeToRestore <DateTime>
 [-BlobRestoreRange <PSBlobRestoreRange[]>] [-WaitForComplete] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6d575-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6d575-108">DESCRIPTION</span></span>
<span data-ttu-id="6d575-109">Cmdleten **restore-AzStorageBlobRange** återställer BLOB i ett lagrings konto för specifika BLOB-intervall.</span><span class="sxs-lookup"><span data-stu-id="6d575-109">The **Restore-AzStorageBlobRange** cmdlet restores blobs in a Storage account for specific blob ranges.</span></span>
<span data-ttu-id="6d575-110">Start intervallet är inkluderat och slut intervallet är exkluderat i BLOB Restore.</span><span class="sxs-lookup"><span data-stu-id="6d575-110">The start range is included, and the end range is excluded in blob restore.</span></span>

## <span data-ttu-id="6d575-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6d575-111">EXAMPLES</span></span>

### <span data-ttu-id="6d575-112">Exempel 1: påbörja återställning av BLOB-enheter i ett lagrings konto med specifika BLOB-intervall</span><span class="sxs-lookup"><span data-stu-id="6d575-112">Example 1: Start restores blobs in a Storage account with specific blob ranges</span></span>
```powershell
PS C:\> $range1 = New-AzStorageBlobRangeToRestore -StartRange container1/blob1 -EndRange container2/blob2
PS C:\> $range2 = New-AzStorageBlobRangeToRestore -StartRange container3/blob3 -EndRange container4/blob4
PS C:\> Restore-AzStorageBlobRange -ResourceGroupName "myresourcegoup" -StorageAccountName "mystorageaccount" -TimeToRestore (Get-Date).AddDays(-1) -BlobRestoreRange $range1,$range2

Status     RestoreId                            FailureReason Parameters.TimeToRestore     Parameters.BlobRanges                     
------     ---------                            ------------- ------------------------     ---------------------                     
InProgress 6ca55a8b-fca0-461a-8e4c-13927a9707e6               2020-02-10T13:58:44.6841810Z ["container1/blob1" -> "container2/blob2",...]

PS C:\> (Get-AzStorageAccount -ResourceGroupName $rgname -StorageAccountName $accountName -IncludeBlobRestoreStatus).BlobRestoreStatus 

Status   RestoreId                            FailureReason Parameters.TimeToRestore     Parameters.BlobRanges                     
------   ---------                            ------------- ------------------------     ---------------------                     
Complete 6ca55a8b-fca0-461a-8e4c-13927a9707e6               2020-02-10T13:58:44.6841810Z ["container1/blob1" -> "container2/blob2",...]
```

<span data-ttu-id="6d575-113">Detta kommando skapar först 2 BLOB-intervall och börjar sedan återställa BLOB-data i ett lagrings konto med 2 BLOB-intervallen sedan.</span><span class="sxs-lookup"><span data-stu-id="6d575-113">This command first creates 2 blob ranges, then start restores blobs in a Storage account with the 2 blob ranges from 1 day ago.</span></span> <span data-ttu-id="6d575-114">Användaren kan använda Get-AzStorageAccount för att spåra återställnings status senare.</span><span class="sxs-lookup"><span data-stu-id="6d575-114">User can use Get-AzStorageAccount to trace the restore status later.</span></span>

### <span data-ttu-id="6d575-115">Exempel 2: återställer alla BLOB i ett lagrings konto i Server delen</span><span class="sxs-lookup"><span data-stu-id="6d575-115">Example 2: Restores all blobs in a Storage account in the backend</span></span>
```powershell
PS C:\> $job = Restore-AzStorageBlobRange -ResourceGroupName "myresourcegoup" -StorageAccountName "mystorageaccount" -TimeToRestore (Get-Date).AddMinutes(-30) -WaitForComplete -asjob

PS C:\> $job | Wait-Job

PS C:\> $job.Output

Status   RestoreId                            FailureReason Parameters.TimeToRestore     Parameters.BlobRanges
------   ---------                            ------------- ------------------------     ---------------------
Complete 0387953a-bbe6-4602-818d-e661581ee44b               2020-08-28T07:11:33.9843100Z ["" -> ""]
```

<span data-ttu-id="6d575-116">Det här kommandot återställer alla blobbar i ett lagrings konto från 30 minuter sedan och väntar på återställningen.</span><span class="sxs-lookup"><span data-stu-id="6d575-116">This command restores all blobs in a Storage account from 30 minutes ago, and wait for the restore complete.</span></span> <span data-ttu-id="6d575-117">Eftersom återställda BLOB kan ta lång tid, köra det i Server delen med-AsJob-parametern och vänta tills jobbet är slutfört och visa resultatet.</span><span class="sxs-lookup"><span data-stu-id="6d575-117">Since restore blobs might take a long time, run it in the backend with -Asjob parameter, and then wait for the job complete and show the result.</span></span>

### <span data-ttu-id="6d575-118">Exempel 3: Återställ BLOB-intervallen direkt och vänta tills de är klara</span><span class="sxs-lookup"><span data-stu-id="6d575-118">Example 3: Restores blobs by input blob ranges directly, and wait for complete</span></span>
```powershell
PS C:\> Restore-AzStorageBlobRange -ResourceGroupName "myresourcegoup" -StorageAccountName "mystorageaccount" -WaitForComplete `
    -TimeToRestore (Get-Date).AddSeconds(-1) `
    -BlobRestoreRange @{StartRange="aaa/abc";EndRange="bbb/abc"},@{StartRange="bbb/acc";EndRange=""}
WARNING: Restore blob rang with Id 'd66d1d02-6e48-47ef-b516-0155dd8319c6' started. Restore blob ranges time to complete is dependent on the size of the restore.

Status   RestoreId                            FailureReason Parameters.TimeToRestore     Parameters.BlobRanges   
------   ---------                            ------------- ------------------------     ---------------------   
Complete d66d1d02-6e48-47ef-b516-0155dd8319c6               2020-02-10T14:17:46.8189116Z ["aaa/abc" -> "bbb/abc",...]
```

<span data-ttu-id="6d575-119">Det här kommandot återställer BLOB-värden i ett lagrings konto från 1 dag sedan, efter 2 BLOB-intervall direkt till Restore-AzStorageBlobRange cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6d575-119">This command restores blobs in a Storage account from 1 day ago, by input 2 blob ranges directly to the Restore-AzStorageBlobRange cmdlet.</span></span> <span data-ttu-id="6d575-120">Det här kommandot väntar på att återställningen är slutförd.</span><span class="sxs-lookup"><span data-stu-id="6d575-120">This command will wait for the restore complete.</span></span>

## <span data-ttu-id="6d575-121">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6d575-121">PARAMETERS</span></span>

### <span data-ttu-id="6d575-122">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6d575-122">-AsJob</span></span>
<span data-ttu-id="6d575-123">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="6d575-123">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6d575-124">-BlobRestoreRange</span><span class="sxs-lookup"><span data-stu-id="6d575-124">-BlobRestoreRange</span></span>
<span data-ttu-id="6d575-125">BLOB-området som ska återställas.</span><span class="sxs-lookup"><span data-stu-id="6d575-125">The blob range to Restore.</span></span>
<span data-ttu-id="6d575-126">Om du inte anger den här parametern återställs alla blob.</span><span class="sxs-lookup"><span data-stu-id="6d575-126">If not specify this parameter, will restore all blobs.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSBlobRestoreRange[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d575-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d575-127">-DefaultProfile</span></span>
<span data-ttu-id="6d575-128">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="6d575-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d575-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6d575-129">-ResourceGroupName</span></span>
<span data-ttu-id="6d575-130">Resurs grupps namn.</span><span class="sxs-lookup"><span data-stu-id="6d575-130">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d575-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6d575-131">-ResourceId</span></span>
<span data-ttu-id="6d575-132">Resurs-ID för lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="6d575-132">Storage Account Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d575-133">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="6d575-133">-StorageAccount</span></span>
<span data-ttu-id="6d575-134">Lagrings konto objekt</span><span class="sxs-lookup"><span data-stu-id="6d575-134">Storage account object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount
Parameter Sets: AccountObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6d575-135">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="6d575-135">-StorageAccountName</span></span>
<span data-ttu-id="6d575-136">Namn på lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="6d575-136">Storage Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases: AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d575-137">-TimeToRestore</span><span class="sxs-lookup"><span data-stu-id="6d575-137">-TimeToRestore</span></span>
<span data-ttu-id="6d575-138">Tiden för återställning av blobben.</span><span class="sxs-lookup"><span data-stu-id="6d575-138">The Time to Restore Blob.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d575-139">-WaitForComplete</span><span class="sxs-lookup"><span data-stu-id="6d575-139">-WaitForComplete</span></span>
<span data-ttu-id="6d575-140">Vänta på att återställningen slutförs</span><span class="sxs-lookup"><span data-stu-id="6d575-140">Wait for Restore task complete</span></span>

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

### <span data-ttu-id="6d575-141">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="6d575-141">-Confirm</span></span>
<span data-ttu-id="6d575-142">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="6d575-142">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d575-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6d575-143">-WhatIf</span></span>
<span data-ttu-id="6d575-144">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="6d575-144">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6d575-145">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="6d575-145">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d575-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d575-146">CommonParameters</span></span>
<span data-ttu-id="6d575-147">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6d575-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d575-148">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6d575-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d575-149">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6d575-149">INPUTS</span></span>

### <span data-ttu-id="6d575-150">System. String</span><span class="sxs-lookup"><span data-stu-id="6d575-150">System.String</span></span>

### <span data-ttu-id="6d575-151">Microsoft. Azure. commands. Management. Storage. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="6d575-151">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="6d575-152">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6d575-152">OUTPUTS</span></span>

### <span data-ttu-id="6d575-153">Microsoft. Azure. commands. Management. Storage. Models. PSBlobRestoreStatus</span><span class="sxs-lookup"><span data-stu-id="6d575-153">Microsoft.Azure.Commands.Management.Storage.Models.PSBlobRestoreStatus</span></span>

## <span data-ttu-id="6d575-154">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6d575-154">NOTES</span></span>

## <span data-ttu-id="6d575-155">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6d575-155">RELATED LINKS</span></span>
