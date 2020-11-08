---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/update-azdatalakegen2item
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzDataLakeGen2Item.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzDataLakeGen2Item.md
ms.openlocfilehash: 6af68da41e1d5ea212d23d0cbc2296a68a6fa7e5
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94269846"
---
# <span data-ttu-id="c1625-101">Update-AzDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="c1625-101">Update-AzDataLakeGen2Item</span></span>

## <span data-ttu-id="c1625-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c1625-102">SYNOPSIS</span></span>
<span data-ttu-id="c1625-103">Uppdatera en fil eller katalog på egenskaper, metadata, behörigheter, ACL och ägare.</span><span class="sxs-lookup"><span data-stu-id="c1625-103">Update a file or directory on properties, metadata, permission, ACL, and owner.</span></span>

## <span data-ttu-id="c1625-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c1625-104">SYNTAX</span></span>

### <span data-ttu-id="c1625-105">ReceiveManual (standard)</span><span class="sxs-lookup"><span data-stu-id="c1625-105">ReceiveManual (Default)</span></span>
```
Update-AzDataLakeGen2Item [-FileSystem] <String> [-Path <String>] [-Permission <String>] [-Owner <String>]
 [-Group <String>] [-Property <Hashtable>] [-Metadata <Hashtable>] [-Acl <PSPathAccessControlEntry[]>]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c1625-106">ItemPipeline</span><span class="sxs-lookup"><span data-stu-id="c1625-106">ItemPipeline</span></span>
```
Update-AzDataLakeGen2Item -InputObject <AzureDataLakeGen2Item> [-Permission <String>] [-Owner <String>]
 [-Group <String>] [-Property <Hashtable>] [-Metadata <Hashtable>] [-Acl <PSPathAccessControlEntry[]>]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c1625-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c1625-107">DESCRIPTION</span></span>
<span data-ttu-id="c1625-108">Cmdleten **Update-AzDataLakeGen2Item** uppdaterar en fil eller katalog på egenskaper, metadata, behörigheter, ACL och ägare.</span><span class="sxs-lookup"><span data-stu-id="c1625-108">The **Update-AzDataLakeGen2Item** cmdlet updates a file or directory on properties, metadata, permission, ACL, and owner.</span></span>
<span data-ttu-id="c1625-109">Denna cmdlet fungerar bara om hierarkisk namnrymd är aktiverat för lagrings kontot.</span><span class="sxs-lookup"><span data-stu-id="c1625-109">This cmdlet only works if Hierarchical Namespace is enabled for the Storage account.</span></span> <span data-ttu-id="c1625-110">Den här typen av konto kan skapas med kör "New-AzStorageAccount"-cmdlet med "-EnableHierarchicalNamespace $true".</span><span class="sxs-lookup"><span data-stu-id="c1625-110">This kind of account can be created by run "New-AzStorageAccount" cmdlet with "-EnableHierarchicalNamespace $true".</span></span>

## <span data-ttu-id="c1625-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c1625-111">EXAMPLES</span></span>

### <span data-ttu-id="c1625-112">Exempel 1: skapa ett ACL-objekt med 3 ACL-post och uppdatera ACL till alla objekt i ett filesystem rekursivt</span><span class="sxs-lookup"><span data-stu-id="c1625-112">Example 1: Create an ACL object with 3 ACL entry, and update ACL to all items in a Filesystem recursively</span></span>
```
PS C:\>$acl = New-AzDataLakeGen2ItemAclObject -AccessControlType user -Permission rwx 
PS C:\>$acl = New-AzDataLakeGen2ItemAclObject -AccessControlType group -Permission rw- -InputObject $acl 
PS C:\>$acl = New-AzDataLakeGen2ItemAclObject -AccessControlType other -Permission "rw-" -InputObject $acl
PS C:\>Get-AzDataLakeGen2ChildItem -FileSystem "filesystem1" -Recurse | Update-AzDataLakeGen2Item -ACL $acl

   FileSystem Name: filesystem1

Path                 IsDirectory  Length          LastModified         Permissions  Owner                Group               
----                 -----------  ------          ------------         -----------  -----                -----               
dir1                 True                         2020-03-13 13:07:34Z rwxrw-rw-    $superuser           $superuser           
dir1/file1           False        1024            2020-03-23 09:29:18Z rwxrw-rw-    $superuser           $superuser          
dir2                 True                         2020-03-23 09:28:36Z rwxrw-rw-    $superuser           $superuser
```

<span data-ttu-id="c1625-113">Det här kommandot skapar först ett ACL-objekt med 3 ACL-post (Använd-InputObject-parametern för att lägga till ACL-posten i befintligt ACL-objekt) och sedan hämta alla objekt i ett filesystem och uppdatera ACL för objekten.</span><span class="sxs-lookup"><span data-stu-id="c1625-113">This command first creates an ACL object with 3 acl entry (use -InputObject parameter to add acl entry to existing acl object), then get all items in a filesystem and update acl on the items.</span></span>

### <span data-ttu-id="c1625-114">Exempel 2: uppdatera alla egenskaper för en fil och visa dem</span><span class="sxs-lookup"><span data-stu-id="c1625-114">Example 2: Update all properties on a file, and show them</span></span>
```
PS C:\> $file = Update-AzDataLakeGen2Item -FileSystem "filesystem1" -Path "dir1/file1" `
                 -Acl $acl `
                 -Property @{"ContentType" = "image/jpeg"; "ContentMD5" = "i727sP7HigloQDsqadNLHw=="; "ContentEncoding" = "UDF8"; "CacheControl" = "READ"; "ContentDisposition" = "True"; "ContentLanguage" = "EN-US"} `
                 -Metadata  @{"tag1" = "value1"; "tag2" = "value2" } `
                 -Permission rw-rw-rwx `
                 -Owner '$superuser' `
                 -Group '$superuser'

PS C:\> $file

   FileSystem Name: filesystem1

Path                 IsDirectory  Length          LastModified         Permissions  Owner                Group               
----                 -----------  ------          ------------         -----------  -----                -----               
dir1/file1           False        1024            2020-03-23 09:57:33Z rwxrw-rw-    $superuser           $superuser          

PS C:\> $file.ACL

DefaultScope AccessControlType EntityId Permissions
------------ ----------------- -------- -----------
False        User                       rwx        
False        Group                      rw-        
False        Other                      rw-        

PS C:\> $file.Permissions

Owner        : Execute, Write, Read
Group        : Write, Read
Other        : Write, Read
StickyBit    : False
ExtendedAcls : False

PS C:\> $file.Properties.Metadata

Key  Value 
---  ----- 
tag2 value2
tag1 value1

PS C:\> $file.Properties


LastModified          : 3/23/2020 9:57:33 AM +00:00
CreatedOn             : 3/23/2020 9:29:18 AM +00:00
Metadata              : {[tag2, value2], [tag1, value1]}
CopyCompletedOn       : 1/1/0001 12:00:00 AM +00:00
CopyStatusDescription : 
CopyId                : 
CopyProgress          : 
CopySource            : 
CopyStatus            : Pending
IsIncrementalCopy     : False
LeaseDuration         : Infinite
LeaseState            : Available
LeaseStatus           : Unlocked
ContentLength         : 1024
ContentType           : image/jpeg
ETag                  : "0x8D7CF109B9878CC"
ContentHash           : {139, 189, 187, 176...}
ContentEncoding       : UDF8
ContentDisposition    : True
ContentLanguage       : EN-US
CacheControl          : READ
AcceptRanges          : bytes
IsServerEncrypted     : True
EncryptionKeySha256   : 
AccessTier            : Cool
ArchiveStatus         : 
AccessTierChangedOn   : 1/1/0001 12:00:00 AM +00:00
```

<span data-ttu-id="c1625-115">Det här kommandot uppdaterar alla egenskaper för en fil (ACL, behörigheter, ägare, grupp, metadata, egenskap kan uppdateras med valfri conbination) och visar dem i PowerShell-konsolen.</span><span class="sxs-lookup"><span data-stu-id="c1625-115">This command updates all properties on a file (ACL, permission,owner, group, metadata, property can be updated with any conbination), and show them in Powershell console.</span></span>

### <span data-ttu-id="c1625-116">Exempel 3: lägga till en ACL-post i en katalog</span><span class="sxs-lookup"><span data-stu-id="c1625-116">Example 3: Add an ACL entry to a directory</span></span>
```
## Get the origin ACL
PS C:\> $acl = (Get-AzDataLakeGen2Item -FileSystem "filesystem1" -Path 'dir1/dir3/').ACL

# Update permission of a new ACL entry (if ACL entry with same AccessControlType/EntityId/DefaultScope not exist, will add a new ACL entry, else update permission of existing ACL entry)
PS C:\> $acl = Set-AzDataLakeGen2ItemAclObject -AccessControlType user -EntityId $id -Permission rw- -InputObject $acl  

# set the new acl to the directory
PS C:\> update-AzDataLakeGen2Item -FileSystem "filesystem1" -Path 'dir1/dir3/' -ACL $acl

   FileSystem Name: filesystem1

Path                 IsDirectory  Length          LastModified         Permissions  Owner                Group               
----                 -----------  ------          ------------         -----------  -----                -----               
dir1/dir3            True                         2020-03-23 09:34:31Z rwxrw-rw-+   $superuser           $superuser
```

<span data-ttu-id="c1625-117">Det här kommandot ger ACL från en katalog, uppdaterar/lägger till en ACL-post och återgår till katalogen.</span><span class="sxs-lookup"><span data-stu-id="c1625-117">This command gets ACL from a directory, updates/adds an ACL entry, and sets back to the directory.</span></span>
<span data-ttu-id="c1625-118">Om det finns en ACL-post med samma AccessControlType/EntityId/DefaultScope ska du lägga till en ny ACL-post, annars uppdatera behörigheten för befintlig ACL-post.</span><span class="sxs-lookup"><span data-stu-id="c1625-118">If ACL entry with same AccessControlType/EntityId/DefaultScope not exist, will add a new ACL entry, else update permission of existing ACL entry.</span></span>

## <span data-ttu-id="c1625-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c1625-119">PARAMETERS</span></span>

### <span data-ttu-id="c1625-120">-ACL</span><span class="sxs-lookup"><span data-stu-id="c1625-120">-Acl</span></span>
<span data-ttu-id="c1625-121">Ställer in åtkomst kontroll rättigheter för POSIX för filer och kataloger.</span><span class="sxs-lookup"><span data-stu-id="c1625-121">Sets POSIX access control rights on files and directories.</span></span>
<span data-ttu-id="c1625-122">Skapa det här objektet med New-AzDataLakeGen2ItemAclObject.</span><span class="sxs-lookup"><span data-stu-id="c1625-122">Create this object with New-AzDataLakeGen2ItemAclObject.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSPathAccessControlEntry[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1625-123">-Kontext</span><span class="sxs-lookup"><span data-stu-id="c1625-123">-Context</span></span>
<span data-ttu-id="c1625-124">Kontext objekt för Azure-lagring</span><span class="sxs-lookup"><span data-stu-id="c1625-124">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="c1625-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1625-125">-DefaultProfile</span></span>
<span data-ttu-id="c1625-126">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c1625-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c1625-127">-Fil system</span><span class="sxs-lookup"><span data-stu-id="c1625-127">-FileSystem</span></span>
<span data-ttu-id="c1625-128">Fil Systems namn</span><span class="sxs-lookup"><span data-stu-id="c1625-128">FileSystem name</span></span>

```yaml
Type: System.String
Parameter Sets: ReceiveManual
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c1625-129">-Grupp</span><span class="sxs-lookup"><span data-stu-id="c1625-129">-Group</span></span>
<span data-ttu-id="c1625-130">Ställer in den ägandea gruppen för blobben.</span><span class="sxs-lookup"><span data-stu-id="c1625-130">Sets the owning group of the blob.</span></span>

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

### <span data-ttu-id="c1625-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c1625-131">-InputObject</span></span>
<span data-ttu-id="c1625-132">Azure Datalake Gen2 objekt objekt att uppdatera</span><span class="sxs-lookup"><span data-stu-id="c1625-132">Azure Datalake Gen2 Item Object to update</span></span>

```yaml
Type: Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item
Parameter Sets: ItemPipeline
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c1625-133">-Metadata</span><span class="sxs-lookup"><span data-stu-id="c1625-133">-Metadata</span></span>
<span data-ttu-id="c1625-134">Anger metadata för katalogen eller filen.</span><span class="sxs-lookup"><span data-stu-id="c1625-134">Specifies metadata for the directory or file.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1625-135">-Owner</span><span class="sxs-lookup"><span data-stu-id="c1625-135">-Owner</span></span>
<span data-ttu-id="c1625-136">Anger ägaren till blobben.</span><span class="sxs-lookup"><span data-stu-id="c1625-136">Sets the owner of the blob.</span></span>

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

### <span data-ttu-id="c1625-137">-Path</span><span class="sxs-lookup"><span data-stu-id="c1625-137">-Path</span></span>
<span data-ttu-id="c1625-138">Sökvägen i angivet filesystem som ska uppdateras.</span><span class="sxs-lookup"><span data-stu-id="c1625-138">The path in the specified Filesystem that should be updated.</span></span>
<span data-ttu-id="c1625-139">Kan vara en fil eller katalog i formatet ' katalog/file.txt ' eller ' directory1/directory2/'.</span><span class="sxs-lookup"><span data-stu-id="c1625-139">Can be a file or directory In the format 'directory/file.txt' or 'directory1/directory2/'.</span></span>
<span data-ttu-id="c1625-140">Om du inte anger den här parametern uppdateras fil systemets rot Katalog.</span><span class="sxs-lookup"><span data-stu-id="c1625-140">Not specify this parameter will update the root directory of the Filesystem.</span></span>

```yaml
Type: System.String
Parameter Sets: ReceiveManual
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c1625-141">-Tillstånd</span><span class="sxs-lookup"><span data-stu-id="c1625-141">-Permission</span></span>
<span data-ttu-id="c1625-142">Anger POSIX-behörigheter för fil ägaren, gruppen fil ägande, och andra.</span><span class="sxs-lookup"><span data-stu-id="c1625-142">Sets POSIX access permissions for the file owner, the file owning group, and others.</span></span>
<span data-ttu-id="c1625-143">Varje klass kan beviljas Läs-, Skriv-eller kör behörighet.</span><span class="sxs-lookup"><span data-stu-id="c1625-143">Each class may be granted read, write, or execute permission.</span></span>
<span data-ttu-id="c1625-144">Symbolisk (rwxrw-RW-) stöds.</span><span class="sxs-lookup"><span data-stu-id="c1625-144">Symbolic (rwxrw-rw-) is supported.</span></span>
<span data-ttu-id="c1625-145">Ogiltigt tillsammans med ACL.</span><span class="sxs-lookup"><span data-stu-id="c1625-145">Invalid in conjunction with Acl.</span></span>

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

### <span data-ttu-id="c1625-146">-Egenskap</span><span class="sxs-lookup"><span data-stu-id="c1625-146">-Property</span></span>
<span data-ttu-id="c1625-147">Anger egenskaper för katalogen eller filen.</span><span class="sxs-lookup"><span data-stu-id="c1625-147">Specifies properties for the directory or file.</span></span> <span data-ttu-id="c1625-148">De egenskaper som stöds för filen är: CacheControl, ContentDisposition, ContentEncoding, ContentLanguage, ContentMD5, ContentType.</span><span class="sxs-lookup"><span data-stu-id="c1625-148">The supported properties for file are: CacheControl, ContentDisposition, ContentEncoding, ContentLanguage, ContentMD5, ContentType.</span></span>
<span data-ttu-id="c1625-149">De egenskaper som stöds för katalogen är: CacheControl, ContentDisposition, ContentEncoding, ContentLanguage.</span><span class="sxs-lookup"><span data-stu-id="c1625-149">The supported properties for directory are: CacheControl, ContentDisposition, ContentEncoding, ContentLanguage.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1625-150">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="c1625-150">-Confirm</span></span>
<span data-ttu-id="c1625-151">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="c1625-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c1625-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c1625-152">-WhatIf</span></span>
<span data-ttu-id="c1625-153">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="c1625-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c1625-154">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="c1625-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c1625-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1625-155">CommonParameters</span></span>
<span data-ttu-id="c1625-156">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c1625-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1625-157">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c1625-157">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1625-158">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c1625-158">INPUTS</span></span>

### <span data-ttu-id="c1625-159">System. String</span><span class="sxs-lookup"><span data-stu-id="c1625-159">System.String</span></span>

### <span data-ttu-id="c1625-160">Microsoft. WindowsAzure. commands. Common. Storage. ResourceModel. AzureDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="c1625-160">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item</span></span>

### <span data-ttu-id="c1625-161">Microsoft. Azure. commands. Common. verifikation. abstraktioner. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="c1625-161">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="c1625-162">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c1625-162">OUTPUTS</span></span>

### <span data-ttu-id="c1625-163">Microsoft. WindowsAzure. commands. Common. Storage. ResourceModel. AzureDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="c1625-163">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item</span></span>

## <span data-ttu-id="c1625-164">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c1625-164">NOTES</span></span>

## <span data-ttu-id="c1625-165">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c1625-165">RELATED LINKS</span></span>
