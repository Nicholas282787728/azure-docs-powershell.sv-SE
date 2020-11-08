---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azdatalakegen2item
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzDataLakeGen2Item.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzDataLakeGen2Item.md
ms.openlocfilehash: 26f3dbc3462688458647e2e9676916063ffa3586
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94258505"
---
# <span data-ttu-id="3dd4e-101">New-AzDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="3dd4e-101">New-AzDataLakeGen2Item</span></span>

## <span data-ttu-id="3dd4e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3dd4e-102">SYNOPSIS</span></span>
<span data-ttu-id="3dd4e-103">Skapa en fil eller katalog i ett fil system.</span><span class="sxs-lookup"><span data-stu-id="3dd4e-103">Create a file or directory in a filesystem.</span></span>

## <span data-ttu-id="3dd4e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3dd4e-104">SYNTAX</span></span>

### <span data-ttu-id="3dd4e-105">Fil (standard)</span><span class="sxs-lookup"><span data-stu-id="3dd4e-105">File (Default)</span></span>
```
New-AzDataLakeGen2Item [-FileSystem] <String> [-Path] <String> -Source <String> [-Umask <String>]
 [-Permission <String>] [-Property <Hashtable>] [-Metadata <Hashtable>] [-Force] [-AsJob]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3dd4e-106">Katalogen</span><span class="sxs-lookup"><span data-stu-id="3dd4e-106">Directory</span></span>
```
New-AzDataLakeGen2Item [-FileSystem] <String> [-Path] <String> [-Directory] [-Umask <String>]
 [-Permission <String>] [-Property <Hashtable>] [-Metadata <Hashtable>] [-Force] [-AsJob]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3dd4e-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3dd4e-107">DESCRIPTION</span></span>
<span data-ttu-id="3dd4e-108">Cmdleten **New-AzDataLakeGen2Item** skapar en fil eller katalog i ett fil system i ett Azure Storage-konto.</span><span class="sxs-lookup"><span data-stu-id="3dd4e-108">The **New-AzDataLakeGen2Item** cmdlet creates a file or directory in a Filesystem in an Azure storage account.</span></span>
<span data-ttu-id="3dd4e-109">Denna cmdlet fungerar bara om hierarkisk namnrymd är aktiverat för lagrings kontot.</span><span class="sxs-lookup"><span data-stu-id="3dd4e-109">This cmdlet only works if Hierarchical Namespace is enabled for the Storage account.</span></span> <span data-ttu-id="3dd4e-110">Den här typen av konto kan skapas med kör "New-AzStorageAccount"-cmdlet med "-EnableHierarchicalNamespace $true".</span><span class="sxs-lookup"><span data-stu-id="3dd4e-110">This kind of account can be created by run "New-AzStorageAccount" cmdlet with "-EnableHierarchicalNamespace $true".</span></span>

## <span data-ttu-id="3dd4e-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3dd4e-111">EXAMPLES</span></span>

### <span data-ttu-id="3dd4e-112">Exempel 1: skapa en katalog med angiven behörighet, umask, egenskaper och metadata</span><span class="sxs-lookup"><span data-stu-id="3dd4e-112">Example 1: Create a directory with specified permission, Umask, properties, and metadata</span></span>
```
PS C:\>New-AzDataLakeGen2Item -FileSystem "testfilesystem" -Path "dir1/dir2/" -Directory -Permission rwxrwxrwx -Umask ---rw---- -Property @{"CacheControl" = "READ"; "ContentDisposition" = "True"} -Metadata  @{"tag1" = "value1"; "tag2" = "value2" }

   FileSystem Name: filesystem1

Path                 IsDirectory  Length          LastModified         Permissions  Owner                Group               
----                 -----------  ------          ------------         -----------  -----                -----               
dir1/dir2            True                         2020-03-23 09:15:56Z rwx---rwx    $superuser           $superuser
```

<span data-ttu-id="3dd4e-113">Det här kommandot skapar en katalog med angiven behörighet, umask, egenskaper och metadata</span><span class="sxs-lookup"><span data-stu-id="3dd4e-113">This command creates a directory with specified Permission, Umask, properties, and metadata</span></span>

### <span data-ttu-id="3dd4e-114">Exempel 2: skapa (överföra) en data Lake File från en lokal källfil och cmdleten körs i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="3dd4e-114">Example 2: Create(upload) a data lake file from a local source file, and the cmdlet runs in background</span></span>
```
PS C:\> $task = New-AzDataLakeGen2Item  -FileSystem "testfilesystem" -Path "dir1/dir2/file1" -Source "c:\sourcefile.txt" -Force -asjob
PS C:\> $task | Wait-Job
PS C:\> $task.Output

   FileSystem Name: filesystem1

Path                 IsDirectory  Length          LastModified         Permissions  Owner                Group                
----                 -----------  ------          ------------         -----------  -----                -----               
dir1/dir2/file1      False        14400000        2020-03-23 09:19:13Z rw-r-----    $superuser           $superuser
```

<span data-ttu-id="3dd4e-115">Det här kommandot skapar (laddar upp) en data Lake File från en lokal källfil och cmdleten körs i bakgrunden.</span><span class="sxs-lookup"><span data-stu-id="3dd4e-115">This command creates(upload) a data lake file from a local source file, and the cmdlet runs in background.</span></span>

## <span data-ttu-id="3dd4e-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3dd4e-116">PARAMETERS</span></span>

### <span data-ttu-id="3dd4e-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3dd4e-117">-AsJob</span></span>
<span data-ttu-id="3dd4e-118">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="3dd4e-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3dd4e-119">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="3dd4e-119">-ConcurrentTaskCount</span></span>
<span data-ttu-id="3dd4e-120">Totalt antal samtidiga asynkrona uppgifter.</span><span class="sxs-lookup"><span data-stu-id="3dd4e-120">The total amount of concurrent async tasks.</span></span> <span data-ttu-id="3dd4e-121">Standardvärdet är 10.</span><span class="sxs-lookup"><span data-stu-id="3dd4e-121">The default value is 10.</span></span>

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

### <span data-ttu-id="3dd4e-122">-Kontext</span><span class="sxs-lookup"><span data-stu-id="3dd4e-122">-Context</span></span>
<span data-ttu-id="3dd4e-123">Kontext objekt för Azure-lagring</span><span class="sxs-lookup"><span data-stu-id="3dd4e-123">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="3dd4e-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3dd4e-124">-DefaultProfile</span></span>
<span data-ttu-id="3dd4e-125">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="3dd4e-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3dd4e-126">-Katalog</span><span class="sxs-lookup"><span data-stu-id="3dd4e-126">-Directory</span></span>
<span data-ttu-id="3dd4e-127">Visar att detta nya objekt är en katalog och inte en fil.</span><span class="sxs-lookup"><span data-stu-id="3dd4e-127">Indicates that this new item is a directory and not a file.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Directory
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3dd4e-128">-Fil system</span><span class="sxs-lookup"><span data-stu-id="3dd4e-128">-FileSystem</span></span>
<span data-ttu-id="3dd4e-129">Fil Systems namn</span><span class="sxs-lookup"><span data-stu-id="3dd4e-129">FileSystem name</span></span>

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

### <span data-ttu-id="3dd4e-130">-Force</span><span class="sxs-lookup"><span data-stu-id="3dd4e-130">-Force</span></span>
<span data-ttu-id="3dd4e-131">Om du har lyckats skapas ett nytt objekt utan några instruktioner</span><span class="sxs-lookup"><span data-stu-id="3dd4e-131">If passed then new item is created without any prompt</span></span>

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

### <span data-ttu-id="3dd4e-132">-Metadata</span><span class="sxs-lookup"><span data-stu-id="3dd4e-132">-Metadata</span></span>
<span data-ttu-id="3dd4e-133">Anger metadata för den katalog eller fil som har skapats.</span><span class="sxs-lookup"><span data-stu-id="3dd4e-133">Specifies metadata for the created directory or file.</span></span>

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

### <span data-ttu-id="3dd4e-134">-Path</span><span class="sxs-lookup"><span data-stu-id="3dd4e-134">-Path</span></span>
<span data-ttu-id="3dd4e-135">Sökvägen i angivet filesystem som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="3dd4e-135">The path in the specified Filesystem that should be create.</span></span>
<span data-ttu-id="3dd4e-136">Kan vara en fil eller katalog i formatet ' katalog/file.txt ' eller ' directory1/directory2/'</span><span class="sxs-lookup"><span data-stu-id="3dd4e-136">Can be a file or directory In the format 'directory/file.txt' or 'directory1/directory2/'</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3dd4e-137">-Tillstånd</span><span class="sxs-lookup"><span data-stu-id="3dd4e-137">-Permission</span></span>
<span data-ttu-id="3dd4e-138">Anger POSIX-behörigheter för fil ägaren, gruppen fil ägande, och andra.</span><span class="sxs-lookup"><span data-stu-id="3dd4e-138">Sets POSIX access permissions for the file owner, the file owning group, and others.</span></span>
<span data-ttu-id="3dd4e-139">Varje klass kan beviljas Läs-, Skriv-eller kör behörighet.</span><span class="sxs-lookup"><span data-stu-id="3dd4e-139">Each class may be granted read, write, or execute permission.</span></span>
<span data-ttu-id="3dd4e-140">Symbolisk (rwxrw-RW-) stöds.</span><span class="sxs-lookup"><span data-stu-id="3dd4e-140">Symbolic (rwxrw-rw-) is supported.</span></span>

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

### <span data-ttu-id="3dd4e-141">-Egenskap</span><span class="sxs-lookup"><span data-stu-id="3dd4e-141">-Property</span></span>
<span data-ttu-id="3dd4e-142">Anger egenskaper för den skapade katalogen eller filen.</span><span class="sxs-lookup"><span data-stu-id="3dd4e-142">Specifies properties for the created directory or file.</span></span> <span data-ttu-id="3dd4e-143">De egenskaper som stöds för filen är: CacheControl, ContentDisposition, ContentEncoding, ContentLanguage, ContentMD5, ContentType.</span><span class="sxs-lookup"><span data-stu-id="3dd4e-143">The supported properties for file are: CacheControl, ContentDisposition, ContentEncoding, ContentLanguage, ContentMD5, ContentType.</span></span>
<span data-ttu-id="3dd4e-144">De egenskaper som stöds för katalogen är: CacheControl, ContentDisposition, ContentEncoding, ContentLanguage.</span><span class="sxs-lookup"><span data-stu-id="3dd4e-144">The supported properties for directory are: CacheControl, ContentDisposition, ContentEncoding, ContentLanguage.</span></span>

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

### <span data-ttu-id="3dd4e-145">-Källa</span><span class="sxs-lookup"><span data-stu-id="3dd4e-145">-Source</span></span>
<span data-ttu-id="3dd4e-146">Ange sökväg till den lokala käll filen som ska laddas upp till en Datalake Gen2-fil.</span><span class="sxs-lookup"><span data-stu-id="3dd4e-146">Specify the local source file path which will be upload to a Datalake Gen2 file.</span></span>

```yaml
Type: System.String
Parameter Sets: File
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3dd4e-147">-Umask</span><span class="sxs-lookup"><span data-stu-id="3dd4e-147">-Umask</span></span>
<span data-ttu-id="3dd4e-148">När du skapar ett nytt objekt och den överordnade katalogen inte har en standard-ACL, begränsar umask behörigheterna för den fil eller katalog som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="3dd4e-148">When creating New Item and the parent directory does not have a default ACL, the umask restricts the permissions of the file or directory to be created.</span></span>
<span data-ttu-id="3dd4e-149">Den resulterande behörigheten tillhandahålls av p & ^ u, där p är behörigheten och du är umask.</span><span class="sxs-lookup"><span data-stu-id="3dd4e-149">The resulting permission is given by p & ^u, where p is the permission and u is the umask.</span></span>
<span data-ttu-id="3dd4e-150">Symbolisk (rwxrw-RW-) stöds.</span><span class="sxs-lookup"><span data-stu-id="3dd4e-150">Symbolic (rwxrw-rw-) is supported.</span></span>

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

### <span data-ttu-id="3dd4e-151">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="3dd4e-151">-Confirm</span></span>
<span data-ttu-id="3dd4e-152">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="3dd4e-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3dd4e-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3dd4e-153">-WhatIf</span></span>
<span data-ttu-id="3dd4e-154">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="3dd4e-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3dd4e-155">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="3dd4e-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3dd4e-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3dd4e-156">CommonParameters</span></span>
<span data-ttu-id="3dd4e-157">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3dd4e-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3dd4e-158">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3dd4e-158">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3dd4e-159">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3dd4e-159">INPUTS</span></span>

### <span data-ttu-id="3dd4e-160">System. String</span><span class="sxs-lookup"><span data-stu-id="3dd4e-160">System.String</span></span>

### <span data-ttu-id="3dd4e-161">Microsoft. Azure. commands. Common. verifikation. abstraktioner. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="3dd4e-161">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="3dd4e-162">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3dd4e-162">OUTPUTS</span></span>

### <span data-ttu-id="3dd4e-163">Microsoft. WindowsAzure. commands. Common. Storage. ResourceModel. AzureDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="3dd4e-163">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item</span></span>

## <span data-ttu-id="3dd4e-164">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3dd4e-164">NOTES</span></span>

## <span data-ttu-id="3dd4e-165">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3dd4e-165">RELATED LINKS</span></span>
