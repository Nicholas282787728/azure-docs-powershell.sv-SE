---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/update-azdatalakegen2aclrecursive
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzDataLakeGen2AclRecursive.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzDataLakeGen2AclRecursive.md
ms.openlocfilehash: 80b1816dff686db7e84bf876fd74f9642389b42f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98419915"
---
# <span data-ttu-id="b208e-101">Update-AzDataLakeGen2AclRecursive</span><span class="sxs-lookup"><span data-stu-id="b208e-101">Update-AzDataLakeGen2AclRecursive</span></span>

## <span data-ttu-id="b208e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b208e-102">SYNOPSIS</span></span>
<span data-ttu-id="b208e-103">Uppdatera ACL rekursivt på den angivna sökvägen.</span><span class="sxs-lookup"><span data-stu-id="b208e-103">Update ACL recursively on the specified path.</span></span> 

## <span data-ttu-id="b208e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b208e-104">SYNTAX</span></span>

```
Update-AzDataLakeGen2AclRecursive [-FileSystem] <String> [[-Path] <String>] [-ContinuationToken <String>]
 -Acl <PSPathAccessControlEntry[]> [-ContinueOnFailure] [-BatchSize <Int32>] [-MaxBatchCount <Int32>] [-AsJob]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b208e-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b208e-105">DESCRIPTION</span></span>
<span data-ttu-id="b208e-106">**Update-AzDataLakeGen2AclRecursive** CMDLET uppdaterar ACL rekursivt på den angivna sökvägen.</span><span class="sxs-lookup"><span data-stu-id="b208e-106">The **Update-AzDataLakeGen2AclRecursive** cmdlet updates ACL recursively on the specified path.</span></span> <span data-ttu-id="b208e-107">Inmatnings åtkomst kontrol listan sammanfogar den ursprungliga ACL: en om ACL-posten med samma AccessControlType/EntityId/DefaultScope finns, uppdaterings behörighet. annars lägger du till en ny ACL-post.</span><span class="sxs-lookup"><span data-stu-id="b208e-107">The input ACL will merge the the original ACL: If ACL entry with same AccessControlType/EntityId/DefaultScope exist, update permission; else add a new ACL entry.</span></span>

## <span data-ttu-id="b208e-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b208e-108">EXAMPLES</span></span>

### <span data-ttu-id="b208e-109">Exempel 1: uppdatera ACL rekursivt på en root directiry i fil systemet</span><span class="sxs-lookup"><span data-stu-id="b208e-109">Example 1: Update ACL recursively on a root directiry of filesystem</span></span>
```
PS C:\>$acl = New-AzDataLakeGen2ItemAclObject -AccessControlType user -Permission rwx 
PS C:\>$acl = New-AzDataLakeGen2ItemAclObject -AccessControlType group -Permission rw- -InputObject $acl 
PS C:\>$acl = New-AzDataLakeGen2ItemAclObject -AccessControlType other -Permission "rw-" -InputObject $acl
PS C:\> Update-AzDataLakeGen2AclRecursive -FileSystem "filesystem1" -Acl $acl -Context $ctx

FailedEntries                   : 
TotalDirectoriesSuccessfulCount : 7
TotalFilesSuccessfulCount       : 5
TotalFailureCount               : 0
ContinuationToken               :
```

<span data-ttu-id="b208e-110">Det här kommandot skapar först ett ACL-objekt med 3 ACL-poster och uppdaterar ACL rekursivt i en rot Katalog i ett fil system.</span><span class="sxs-lookup"><span data-stu-id="b208e-110">This command first creates an ACL object with 3 acl entries, then updates ACL recursively on a root directory of a file system.</span></span>

### <span data-ttu-id="b208e-111">Exempel 2: uppdatera ACL rekursivt i en katalog och fortsätt från ett fel med ContinuationToken</span><span class="sxs-lookup"><span data-stu-id="b208e-111">Example 2: Update ACL recursively on a directory, and resume from failure with ContinuationToken</span></span>
```
PS C:\> $result = Update-AzDataLakeGen2AclRecursive -FileSystem "filesystem1" -Path "dir1" -Acl $acl  -Context $ctx

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

PS C:\> $result = Update-AzDataLakeGen2AclRecursive -FileSystem "filesystem1" -Path "dir1" -Acl $acl -ContinuationToken $result.ContinuationToken -Context $ctx

PS C:\> $result

FailedEntries                   : 
TotalDirectoriesSuccessfulCount : 100
TotalFilesSuccessfulCount       : 1000
TotalFailureCount               : 0
ContinuationToken               :
```

<span data-ttu-id="b208e-112">Detta kommando uppdaterar först ACL rekursivt till en katalog och sedan fortsätter du med ContinuationToken efter att användaren åtgärdat den misslyckade filen.</span><span class="sxs-lookup"><span data-stu-id="b208e-112">This command first updateds ACL recursively to a directory and failed, then resume with ContinuationToken after user fix the failed file.</span></span>

### <span data-ttu-id="b208e-113">Exempel 3: uppdatera ACL rekursivt efter segment</span><span class="sxs-lookup"><span data-stu-id="b208e-113">Example 3: Update ACL recursively chunk by chunk</span></span>
```
$ContinueOnFailure = $true # Set it to $false if want to terminate the operation quickly on encountering failures
$token = $null
$TotalDirectoriesSuccess = 0
$TotalFilesSuccess = 0
$totalFailure = 0
$FailedEntries = New-Object System.Collections.Generic.List[System.Object]
do
{
    
    if ($ContinueOnFailure)
    {
        $result = Update-AzDataLakeGen2AclRecursive -FileSystem "filesystem1" -Path "dir1" -Acl $acl  -BatchSize 100 -MaxBatchCount 50 -ContinuationToken $token -Context $ctx -ContinueOnFailure
    }
    else
    {
        $result = Update-AzDataLakeGen2AclRecursive -FileSystem "filesystem1" -Path "dir1" -Acl $acl  -BatchSize 100 -MaxBatchCount 50 -ContinuationToken $token -Context $ctx
    }

    # echo $result
    $TotalFilesSuccess += $result.TotalFilesSuccessfulCount
    $TotalDirectoriesSuccess += $result.TotalDirectoriesSuccessfulCount
    $totalFailure += $result.TotalFailureCount
    $FailedEntries += $result.FailedEntries
    $token = $result.ContinuationToken
}while (($token -ne $null) -and (($ContinueOnFailure) -or ($result.TotalFailureCount -eq 0)))
echo ""
echo "[Result Summary]"
echo "TotalDirectoriesSuccessfulCount: `t$($TotalDirectoriesSuccess)"
echo "TotalFilesSuccessfulCount: `t`t`t$($TotalFilesSuccess)"
echo "TotalFailureCount: `t`t`t`t`t$($totalFailure)"
echo "ContinuationToken: `t`t`t`t`t$($token)"
echo "FailedEntries:"$($FailedEntries | ft)
```

<span data-ttu-id="b208e-114">Det här manuset uppdaterar ACL-rescursively för segment, med segment storlek som BatchSize \* MaxBatchCount.</span><span class="sxs-lookup"><span data-stu-id="b208e-114">This script will update ACL rescursively on directory chunk by chunk, with chunk size as BatchSize \* MaxBatchCount.</span></span> <span data-ttu-id="b208e-115">Segment storleken är 5000 i det här skriptet.</span><span class="sxs-lookup"><span data-stu-id="b208e-115">Chunk size is 5000 in this script.</span></span>

### <span data-ttu-id="b208e-116">Exempel 4: uppdatera ACL rekursivt i en katalog och ContinueOnFailure och fortsätt sedan från en person</span><span class="sxs-lookup"><span data-stu-id="b208e-116">Example 4: Update ACL recursively on a directory and ContinueOnFailure, then resume from failures one by one</span></span>
```
PS C:\> $result = Update-AzDataLakeGen2AclRecursive -FileSystem "filesystem1" -Path "dir1" -Acl $acl -ContinueOnFailure -Context $ctx

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
            Set-AzDataLakeGen2AclRecursive -FileSystem "filesystem1" -Path $path -Acl $acl -Context $ctx
        }
```

<span data-ttu-id="b208e-117">Detta kommando uppdaterar först ACL rekursivt till en katalog med ContinueOnFailure, och vissa objekt misslyckades, återuppta de misslyckade objekten en och en.</span><span class="sxs-lookup"><span data-stu-id="b208e-117">This command first updateds ACL recursively to a directory with ContinueOnFailure, and some items failed, then resume the failed items one by one.</span></span>

## <span data-ttu-id="b208e-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b208e-118">PARAMETERS</span></span>

### <span data-ttu-id="b208e-119">-ACL</span><span class="sxs-lookup"><span data-stu-id="b208e-119">-Acl</span></span>
<span data-ttu-id="b208e-120">POSIX-åtkomstkontroll för att aktivera rekursivt för filen eller katalogen.</span><span class="sxs-lookup"><span data-stu-id="b208e-120">The POSIX access control list to set recursively for the file or directory.</span></span>

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

### <span data-ttu-id="b208e-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b208e-121">-AsJob</span></span>
<span data-ttu-id="b208e-122">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="b208e-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b208e-123">-BatchSize</span><span class="sxs-lookup"><span data-stu-id="b208e-123">-BatchSize</span></span>
<span data-ttu-id="b208e-124">Om data uppsättningens storlek överskrider batchstorleken är det uppdelat i flera begär Anden så att förlopp kan spåras.</span><span class="sxs-lookup"><span data-stu-id="b208e-124">If data set size exceeds batch size then operation will be split into multiple requests so that progress can be tracked.</span></span>
<span data-ttu-id="b208e-125">Batchstorleken måste vara mellan 1 och 2000.</span><span class="sxs-lookup"><span data-stu-id="b208e-125">Batch size should be between 1 and 2000.</span></span>
<span data-ttu-id="b208e-126">Standardvärdet är 2000.</span><span class="sxs-lookup"><span data-stu-id="b208e-126">Default is 2000.</span></span>

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

### <span data-ttu-id="b208e-127">-Kontext</span><span class="sxs-lookup"><span data-stu-id="b208e-127">-Context</span></span>
<span data-ttu-id="b208e-128">Kontext objekt för Azure-lagring</span><span class="sxs-lookup"><span data-stu-id="b208e-128">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="b208e-129">-ContinuationToken</span><span class="sxs-lookup"><span data-stu-id="b208e-129">-ContinuationToken</span></span>
<span data-ttu-id="b208e-130">Fortsättnings-token.</span><span class="sxs-lookup"><span data-stu-id="b208e-130">Continuation Token.</span></span>

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

### <span data-ttu-id="b208e-131">-ContinueOnFailure</span><span class="sxs-lookup"><span data-stu-id="b208e-131">-ContinueOnFailure</span></span>
<span data-ttu-id="b208e-132">Ställ in den här parametern för att ignorera fel och fortsätta proceeing med operationen på andra underenheter i katalogen.</span><span class="sxs-lookup"><span data-stu-id="b208e-132">Set this parameter to ignore failures and continue proceeing with the operation on other sub-entities of the directory.</span></span> <span data-ttu-id="b208e-133">Standard åtgärden avbryts om du stöter på fel.</span><span class="sxs-lookup"><span data-stu-id="b208e-133">Default the operation will terminate quickly on encountering failures.</span></span>

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

### <span data-ttu-id="b208e-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b208e-134">-DefaultProfile</span></span>
<span data-ttu-id="b208e-135">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b208e-135">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b208e-136">-Fil system</span><span class="sxs-lookup"><span data-stu-id="b208e-136">-FileSystem</span></span>
<span data-ttu-id="b208e-137">Fil Systems namn</span><span class="sxs-lookup"><span data-stu-id="b208e-137">FileSystem name</span></span>

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

### <span data-ttu-id="b208e-138">-MaxBatchCount</span><span class="sxs-lookup"><span data-stu-id="b208e-138">-MaxBatchCount</span></span>
<span data-ttu-id="b208e-139">Maximalt antal batchar som en åtkomst kontroll åtgärd för enskild ändring kan utföra.</span><span class="sxs-lookup"><span data-stu-id="b208e-139">Maximum number of batches that single change Access Control operation can execute.</span></span> <span data-ttu-id="b208e-140">Om data uppsättningens storlek överskrider MaxBatchCount multiplicera BatchSize returnerar fortsättnings-token.</span><span class="sxs-lookup"><span data-stu-id="b208e-140">If data set size exceeds MaxBatchCount multiply BatchSize, continuation token will be return.</span></span>

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

### <span data-ttu-id="b208e-141">-Path</span><span class="sxs-lookup"><span data-stu-id="b208e-141">-Path</span></span>
<span data-ttu-id="b208e-142">Sökvägen i angivet FileSystem som ändrar ACL rekursivt.</span><span class="sxs-lookup"><span data-stu-id="b208e-142">The path in the specified FileSystem that to change Acl recursively.</span></span>
<span data-ttu-id="b208e-143">Kan vara en fil eller en katalog.</span><span class="sxs-lookup"><span data-stu-id="b208e-143">Can be a file or directory.</span></span>
<span data-ttu-id="b208e-144">I formatet ' katalog/file.txt ' eller ' directory1/directory2/'.</span><span class="sxs-lookup"><span data-stu-id="b208e-144">In the format 'directory/file.txt' or 'directory1/directory2/'.</span></span>
<span data-ttu-id="b208e-145">Hoppa över ange den här parametern för att ändra ACL rekursivt från rot katalogen i fil systemet.</span><span class="sxs-lookup"><span data-stu-id="b208e-145">Skip set this parameter to change Acl recursively from root directory of the Filesystem.</span></span>

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

### <span data-ttu-id="b208e-146">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="b208e-146">-Confirm</span></span>
<span data-ttu-id="b208e-147">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="b208e-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b208e-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b208e-148">-WhatIf</span></span>
<span data-ttu-id="b208e-149">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="b208e-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b208e-150">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="b208e-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b208e-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b208e-151">CommonParameters</span></span>
<span data-ttu-id="b208e-152">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b208e-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b208e-153">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b208e-153">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b208e-154">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b208e-154">INPUTS</span></span>

### <span data-ttu-id="b208e-155">System. String</span><span class="sxs-lookup"><span data-stu-id="b208e-155">System.String</span></span>

### <span data-ttu-id="b208e-156">Microsoft. Azure. commands. Common. verifikation. abstraktioner. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="b208e-156">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="b208e-157">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b208e-157">OUTPUTS</span></span>

### <span data-ttu-id="b208e-158">System. String</span><span class="sxs-lookup"><span data-stu-id="b208e-158">System.String</span></span>

## <span data-ttu-id="b208e-159">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b208e-159">NOTES</span></span>

## <span data-ttu-id="b208e-160">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b208e-160">RELATED LINKS</span></span>
