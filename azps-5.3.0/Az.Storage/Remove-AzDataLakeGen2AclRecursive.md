---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azdatalakegen2aclrecursive
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzDataLakeGen2AclRecursive.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzDataLakeGen2AclRecursive.md
ms.openlocfilehash: cb2c409ae2bbe7734c433de74ef4a21c368221e1
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98525321"
---
# <span data-ttu-id="8a916-101">Remove-AzDataLakeGen2AclRecursive</span><span class="sxs-lookup"><span data-stu-id="8a916-101">Remove-AzDataLakeGen2AclRecursive</span></span>

## <span data-ttu-id="8a916-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8a916-102">SYNOPSIS</span></span>
<span data-ttu-id="8a916-103">Ta bort ACL rekursivt på den angivna sökvägen.</span><span class="sxs-lookup"><span data-stu-id="8a916-103">Remove ACL recursively on the specified path.</span></span> 

## <span data-ttu-id="8a916-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8a916-104">SYNTAX</span></span>

```
Remove-AzDataLakeGen2AclRecursive [-FileSystem] <String> [[-Path] <String>] [-ContinuationToken <String>]
 -Acl <PSPathAccessControlEntry[]> [-ContinueOnFailure] [-BatchSize <Int32>] [-MaxBatchCount <Int32>] [-AsJob]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8a916-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8a916-105">DESCRIPTION</span></span>
<span data-ttu-id="8a916-106">Cmdleten **Remove-AzDataLakeGen2AclRecursive** tar bort ACL rekursivt på den angivna sökvägen.</span><span class="sxs-lookup"><span data-stu-id="8a916-106">The **Remove-AzDataLakeGen2AclRecursive** cmdlet removes ACL recursively on the specified path.</span></span> <span data-ttu-id="8a916-107">ACL-posterna i den ursprungliga ACL-listan, som har samma AccessControlType, DefaultScope och EntityId med postacl-poster (till och med olika behörigheter) få LBE tas bort.</span><span class="sxs-lookup"><span data-stu-id="8a916-107">The ACL entries in original ACL, which has same AccessControlType, DefaultScope and EntityId with input ACL entries (even with different permission) wil lbe removed.</span></span>

## <span data-ttu-id="8a916-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8a916-108">EXAMPLES</span></span>

### <span data-ttu-id="8a916-109">Exempel 1: ta bort ACL rekursivt på en root directiry i fil systemet</span><span class="sxs-lookup"><span data-stu-id="8a916-109">Example 1: Remove ACL recursively on a root directiry of filesystem</span></span>
```
PS C:\>$acl = Set-AzDataLakeGen2ItemAclObject -AccessControlType user -EntityId $id -Permission r-x -DefaultScope
PS C:\>$acl = Set-AzDataLakeGen2ItemAclObject -AccessControlType user -EntityId $id -Permission r-x -InputObject $acl
PS C:\> Remove-AzDataLakeGen2AclRecursive -FileSystem "filesystem1" -Acl $acl -Context $ctx
WARNING: To find the ACL Entry to remove, will only compare AccessControlType, DefaultScope and EntityId, will omit Permission.

FailedEntries                   : 
TotalDirectoriesSuccessfulCount : 7
TotalFilesSuccessfulCount       : 5
TotalFailureCount               : 0
ContinuationToken               :
```

<span data-ttu-id="8a916-110">Det här kommandot skapar först ett ACL-objekt med 2 ACL-poster och tar sedan bort ACL rekursivt i en rot Katalog i ett fil system.</span><span class="sxs-lookup"><span data-stu-id="8a916-110">This command first creates an ACL object with 2 acl entries, then removes ACL recursively on a root directory of a file system.</span></span>

### <span data-ttu-id="8a916-111">Exempel 2: ta bort ACL rekursivt i en katalog</span><span class="sxs-lookup"><span data-stu-id="8a916-111">Example 2: Remove ACL recursively on a directory</span></span>
```
PS C:\> $result = Remove-AzDataLakeGen2AclRecursive -FileSystem "filesystem1" -Path "dir1" -Acl $acl  -Context $ctx
WARNING: To find the ACL Entry to remove, will only compare AccessControlType, DefaultScope and EntityId, will omit Permission.

PS C:\> $result

FailedEntries                   : {dir1/dir2/file4}
TotalDirectoriesSuccessfulCount : 500
TotalFilesSuccessfulCount       : 2500
TotalFailureCount               : 1
ContinuationToken               : VBaHi5TfyO2ai1wYTRhIL2FjbGNibjA2c3RmATAxRDVEN0UzRENFQzZCRTAvYWRsc3Rlc3QyATAxRDY2M0ZCQTZBN0JGQTkvZGlyMC9kaXIxL2ZpbGUzFgAAAA==

PS C:\> $result.FailedEntries

Name            IsDirectory ErrorMessage                                                                   
----            ----------- ------------                                                                   
dir0/dir2/file4       False This request is not authorized to perform this operation using this permission.

# user need fix the failed item , then can resume with ContinuationToken

PS C:\> $result = Remove-AzDataLakeGen2AclRecursive -FileSystem "filesystem1" -Path "dir1" -Acl $acl -ContinuationToken $result.ContinuationToken -Context $ctx
WARNING: To find the ACL Entry to remove, will only compare AccessControlType, DefaultScope and EntityId, will omit Permission.

PS C:\> $result

FailedEntries                   : 
TotalDirectoriesSuccessfulCount : 100
TotalFilesSuccessfulCount       : 1000
TotalFailureCount               : 0
ContinuationToken               :
```

<span data-ttu-id="8a916-112">Detta kommando tar först bort ACL rekursivt i en katalog och sedan fortsätter med ContinuationToken efter att användaren åtgärdat den misslyckade filen.</span><span class="sxs-lookup"><span data-stu-id="8a916-112">This command first removes ACL recursively on a directory and failed, then resume with ContinuationToken after user fix the failed file.</span></span>

### <span data-ttu-id="8a916-113">Exempel 3: ta bort ACL rekursivt för segment</span><span class="sxs-lookup"><span data-stu-id="8a916-113">Example 3: Remove ACL recursively chunk by chunk</span></span>
```
$token = $null
$TotalDirectoriesSuccess = 0
$TotalFilesSuccess = 0
$totalFailure = 0
$FailedEntries = New-Object System.Collections.Generic.List[System.Object]
do
{
    $result = Remove-AzDataLakeGen2AclRecursive -FileSystem "filesystem1" -Path "dir1" -Acl $acl  -BatchSize 1000 -MaxBatchCount 50 -ContinuationToken $token -Context $ctx

    # echo $result
    $TotalFilesSuccess += $result.TotalFilesSuccessfulCount
    $TotalDirectoriesSuccess += $result.TotalDirectoriesSuccessfulCount
    $totalFailure += $result.TotalFailureCount
    $FailedEntries += $result.FailedEntries
    $token = $result.ContinuationToken
}while (($token -ne $null) -and ($result.TotalFailureCount -eq 0))
echo ""
echo "[Result Summary]"
echo "TotalDirectoriesSuccessfulCount: `t$($TotalDirectoriesSuccess)"
echo "TotalFilesSuccessfulCount: `t`t`t$($TotalFilesSuccess)"
echo "TotalFailureCount: `t`t`t`t`t$($totalFailure)"
echo "ContinuationToken: `t`t`t`t`t$($token)"
echo "FailedEntries:"$($FailedEntries | ft)
```

<span data-ttu-id="8a916-114">Det här manuset tar bort ACL-rescursively för segment, med segment storlek som BatchSize \* MaxBatchCount.</span><span class="sxs-lookup"><span data-stu-id="8a916-114">This script will remove ACL rescursively on directory chunk by chunk, with chunk size as BatchSize \* MaxBatchCount.</span></span> <span data-ttu-id="8a916-115">Segment storleken är 50000 i det här skriptet.</span><span class="sxs-lookup"><span data-stu-id="8a916-115">Chunk size is 50000 in this script.</span></span>

### <span data-ttu-id="8a916-116">Exempel 4: ta bort ACL rekursivt i en katalog och ContinueOnFailure och fortsätt sedan från en person</span><span class="sxs-lookup"><span data-stu-id="8a916-116">Example 4: Remove ACL recursively on a directory and ContinueOnFailure, then resume from failures one by one</span></span>
```
PS C:\> $result = Remove-AzDataLakeGen2AclRecursive -FileSystem "filesystem1" -Path "dir1" -Acl $acl -ContinueOnFailure -Context $ctx

PS C:\> $result

FailedEntries                   : {dir0/dir1/file1, dir0/dir2/file4}
TotalDirectoriesSuccessfulCount : 100
TotalFilesSuccessfulCount       : 500
TotalFailureCount               : 2
ContinuationToken               : VBaHi5TfyO2ai1wYTRhIL2FjbGNibjA2c3RmATAxRDVEN0UzRENFQzZCRTAvYWRsc3Rlc3QyATAxRDY2M0ZCQTZBN0JGQTkvZGlyMC9kaXIxL2ZpbGUzFgAAAA==

PS C:\> $result.FailedEntries

Name            IsDirectory ErrorMessage                                                                   
----            ----------- ------------                                                                   
dir0/dir1/file1       False This request is not authorized to perform this operation using this permission.
dir0/dir2/file4       False This request is not authorized to perform this operation using this permission.

# user need fix the failed item , then can resume with ContinuationToken

PS C:\> foreach ($path in $result.FailedEntries.Name)
        {
            # user code to fix failed entry in $path
            
            #set ACL again
            Remove-AzDataLakeGen2AclRecursive -FileSystem "filesystem1" -Path $path -Acl $acl -Context $ctx
        }
```

<span data-ttu-id="8a916-117">Det här kommandot tar först bort ACL rekursivt till en katalog med ContinueOnFailure, och vissa objekt misslyckades, och sedan återuppta de misslyckade objekten en och en.</span><span class="sxs-lookup"><span data-stu-id="8a916-117">This command first removes ACL recursively to a directory with ContinueOnFailure, and some items failed, then resume the failed items one by one.</span></span>

## <span data-ttu-id="8a916-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8a916-118">PARAMETERS</span></span>

### <span data-ttu-id="8a916-119">-ACL</span><span class="sxs-lookup"><span data-stu-id="8a916-119">-Acl</span></span>
<span data-ttu-id="8a916-120">POSIX-åtkomstkontroll för att aktivera rekursivt för filen eller katalogen.</span><span class="sxs-lookup"><span data-stu-id="8a916-120">The POSIX access control list to set recursively for the file or directory.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSPathAccessControlEntry[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a916-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8a916-121">-AsJob</span></span>
<span data-ttu-id="8a916-122">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="8a916-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8a916-123">-BatchSize</span><span class="sxs-lookup"><span data-stu-id="8a916-123">-BatchSize</span></span>
<span data-ttu-id="8a916-124">Om data uppsättningens storlek överskrider batchstorleken är det uppdelat i flera begär Anden så att förlopp kan spåras.</span><span class="sxs-lookup"><span data-stu-id="8a916-124">If data set size exceeds batch size then operation will be split into multiple requests so that progress can be tracked.</span></span>
<span data-ttu-id="8a916-125">Batchstorleken måste vara mellan 1 och 2000.</span><span class="sxs-lookup"><span data-stu-id="8a916-125">Batch size should be between 1 and 2000.</span></span>
<span data-ttu-id="8a916-126">Standardvärdet är 2000.</span><span class="sxs-lookup"><span data-stu-id="8a916-126">Default is 2000.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a916-127">-Kontext</span><span class="sxs-lookup"><span data-stu-id="8a916-127">-Context</span></span>
<span data-ttu-id="8a916-128">Kontext objekt för Azure-lagring</span><span class="sxs-lookup"><span data-stu-id="8a916-128">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="8a916-129">-ContinuationToken</span><span class="sxs-lookup"><span data-stu-id="8a916-129">-ContinuationToken</span></span>
<span data-ttu-id="8a916-130">Fortsättnings-token.</span><span class="sxs-lookup"><span data-stu-id="8a916-130">Continuation Token.</span></span>

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

### <span data-ttu-id="8a916-131">-ContinueOnFailure</span><span class="sxs-lookup"><span data-stu-id="8a916-131">-ContinueOnFailure</span></span>
<span data-ttu-id="8a916-132">Ställ in den här parametern för att ignorera fel och fortsätta proceeing med operationen på andra underenheter i katalogen.</span><span class="sxs-lookup"><span data-stu-id="8a916-132">Set this parameter to ignore failures and continue proceeing with the operation on other sub-entities of the directory.</span></span> <span data-ttu-id="8a916-133">Standard åtgärden avbryts om du stöter på fel.</span><span class="sxs-lookup"><span data-stu-id="8a916-133">Default the operation will terminate quickly on encountering failures.</span></span>

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

### <span data-ttu-id="8a916-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a916-134">-DefaultProfile</span></span>
<span data-ttu-id="8a916-135">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="8a916-135">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8a916-136">-Fil system</span><span class="sxs-lookup"><span data-stu-id="8a916-136">-FileSystem</span></span>
<span data-ttu-id="8a916-137">Fil Systems namn</span><span class="sxs-lookup"><span data-stu-id="8a916-137">FileSystem name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8a916-138">-MaxBatchCount</span><span class="sxs-lookup"><span data-stu-id="8a916-138">-MaxBatchCount</span></span>
<span data-ttu-id="8a916-139">Maximalt antal batchar som en åtkomst kontroll åtgärd för enskild ändring kan utföra.</span><span class="sxs-lookup"><span data-stu-id="8a916-139">Maximum number of batches that single change Access Control operation can execute.</span></span> <span data-ttu-id="8a916-140">Om data uppsättningens storlek överskrider MaxBatchCount multiplicera BatchSize returnerar fortsättnings-token.</span><span class="sxs-lookup"><span data-stu-id="8a916-140">If data set size exceeds MaxBatchCount multiply BatchSize, continuation token will be return.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a916-141">-Path</span><span class="sxs-lookup"><span data-stu-id="8a916-141">-Path</span></span>
<span data-ttu-id="8a916-142">Sökvägen i angivet FileSystem som ändrar ACL rekursivt.</span><span class="sxs-lookup"><span data-stu-id="8a916-142">The path in the specified FileSystem that to change Acl recursively.</span></span>
<span data-ttu-id="8a916-143">Kan vara en fil eller en katalog.</span><span class="sxs-lookup"><span data-stu-id="8a916-143">Can be a file or directory.</span></span>
<span data-ttu-id="8a916-144">I formatet ' katalog/file.txt ' eller ' directory1/directory2/'.</span><span class="sxs-lookup"><span data-stu-id="8a916-144">In the format 'directory/file.txt' or 'directory1/directory2/'.</span></span>
<span data-ttu-id="8a916-145">Hoppa över ange den här parametern för att ändra ACL rekursivt från rot katalogen i fil systemet.</span><span class="sxs-lookup"><span data-stu-id="8a916-145">Skip set this parameter to change Acl recursively from root directory of the Filesystem.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8a916-146">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="8a916-146">-Confirm</span></span>
<span data-ttu-id="8a916-147">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="8a916-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8a916-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8a916-148">-WhatIf</span></span>
<span data-ttu-id="8a916-149">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="8a916-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8a916-150">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="8a916-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8a916-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a916-151">CommonParameters</span></span>
<span data-ttu-id="8a916-152">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8a916-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a916-153">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8a916-153">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a916-154">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8a916-154">INPUTS</span></span>

### <span data-ttu-id="8a916-155">System. String</span><span class="sxs-lookup"><span data-stu-id="8a916-155">System.String</span></span>

### <span data-ttu-id="8a916-156">Microsoft. Azure. commands. Common. verifikation. abstraktioner. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="8a916-156">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="8a916-157">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8a916-157">OUTPUTS</span></span>

### <span data-ttu-id="8a916-158">System. String</span><span class="sxs-lookup"><span data-stu-id="8a916-158">System.String</span></span>

## <span data-ttu-id="8a916-159">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8a916-159">NOTES</span></span>

## <span data-ttu-id="8a916-160">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8a916-160">RELATED LINKS</span></span>
