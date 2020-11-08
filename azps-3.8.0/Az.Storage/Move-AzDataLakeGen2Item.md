---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/move-azdatalakegen2item
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Move-AzDataLakeGen2Item.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Move-AzDataLakeGen2Item.md
ms.openlocfilehash: b8d46d85d00f00afdfa326b22a759f60af7b5bbe
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94090879"
---
# <span data-ttu-id="f2f37-101">Move-AzDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="f2f37-101">Move-AzDataLakeGen2Item</span></span>

## <span data-ttu-id="f2f37-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f2f37-102">SYNOPSIS</span></span>
<span data-ttu-id="f2f37-103">Flytta en fil eller katalog till en annan fil eller katalog på samma lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="f2f37-103">Move a file or directory to another a file or directory in same Storage account.</span></span>

## <span data-ttu-id="f2f37-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f2f37-104">SYNTAX</span></span>

### <span data-ttu-id="f2f37-105">ReceiveManual (standard)</span><span class="sxs-lookup"><span data-stu-id="f2f37-105">ReceiveManual (Default)</span></span>
```
Move-AzDataLakeGen2Item [-FileSystem] <String> [-Path] <String> -DestFileSystem <String> -DestPath <String>
 [-Force] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f2f37-106">ItemPipeline</span><span class="sxs-lookup"><span data-stu-id="f2f37-106">ItemPipeline</span></span>
```
Move-AzDataLakeGen2Item -InputObject <AzureDataLakeGen2Item> -DestFileSystem <String> -DestPath <String>
 [-Force] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f2f37-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f2f37-107">DESCRIPTION</span></span>
<span data-ttu-id="f2f37-108">Cmdleten **Move-AzDataLakeGen2Item** flyttar en fil eller katalog till en annan fil eller katalog på samma lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="f2f37-108">The **Move-AzDataLakeGen2Item** cmdlet moves a a file or directory to another a file or directory in same Storage account.</span></span>
<span data-ttu-id="f2f37-109">Denna cmdlet fungerar bara om hierarkisk namnrymd är aktiverat för lagrings kontot.</span><span class="sxs-lookup"><span data-stu-id="f2f37-109">This cmdlet only works if Hierarchical Namespace is enabled for the Storage account.</span></span> <span data-ttu-id="f2f37-110">Den här typen av konto kan skapas med kör "New-AzStorageAccount"-cmdlet med "-EnableHierarchicalNamespace $true".</span><span class="sxs-lookup"><span data-stu-id="f2f37-110">This kind of account can be created by run "New-AzStorageAccount" cmdlet with "-EnableHierarchicalNamespace $true".</span></span>

## <span data-ttu-id="f2f37-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f2f37-111">EXAMPLES</span></span>

### <span data-ttu-id="f2f37-112">Exempel 1: flytta en vikning i samma filesystem</span><span class="sxs-lookup"><span data-stu-id="f2f37-112">Example 1: Move a fold in same Filesystem</span></span>
```
PS C:\> Move-AzDataLakeGen2Item -FileSystem "filesystem1" -Path "dir1/" -DestFileSystem "filesystem1" -DestPath "dir3/"

   FileSystem Name: filesystem1

Path                 IsDirectory  Length          LastModified         Permissions  Owner                Group               
----                 -----------  ------          ------------         -----------  -----                -----               
dir3                 True                         2020-03-13 13:07:34Z rwxrw-rw-    $superuser           $superuser
```

<span data-ttu-id="f2f37-113">Det här kommandot flyttar katalogen ' dir1 ' till katalogen ' dir3 ' i samma fil system.</span><span class="sxs-lookup"><span data-stu-id="f2f37-113">This command move directory 'dir1' to directory 'dir3' in the same Filesystem.</span></span>

### <span data-ttu-id="f2f37-114">Exempel 2: flytta en fil via pipeline till ett annat fil system med samma lagrings konto utan att fråga</span><span class="sxs-lookup"><span data-stu-id="f2f37-114">Example 2: Move a file by pipeline, to another Filesystem in the same Storage account without prompt</span></span>
```
PS C:\> Get-AzDataLakeGen2Item -FileSystem "filesystem1" -Path "dir1/file1" | Move-AzDataLakeGen2Item -DestFileSystem "filesystem2" -DestPath "dir2/file2" -Force

   FileSystem Name: filesystem2

Path                 IsDirectory  Length          LastModified         Permissions  Owner                Group               
----                 -----------  ------          ------------         -----------  -----                -----               
dir2/file2           False        1024            2020-03-23 09:57:33Z rwxrw-rw-    $superuser           $superuser
```

<span data-ttu-id="f2f37-115">Det här kommandot flyttar filen ' dir1/fil1 ' i ' filesystem1 ' till filen ' dir2/fil2 ' i ' filesystem2 ' på samma lagrings konto utan fråga.</span><span class="sxs-lookup"><span data-stu-id="f2f37-115">This command move file 'dir1/file1' in 'filesystem1' to file 'dir2/file2' in 'filesystem2' in the same Storage account without prompt.</span></span>

## <span data-ttu-id="f2f37-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f2f37-116">PARAMETERS</span></span>

### <span data-ttu-id="f2f37-117">-Kontext</span><span class="sxs-lookup"><span data-stu-id="f2f37-117">-Context</span></span>
<span data-ttu-id="f2f37-118">Kontext objekt för Azure-lagring</span><span class="sxs-lookup"><span data-stu-id="f2f37-118">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="f2f37-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2f37-119">-DefaultProfile</span></span>
<span data-ttu-id="f2f37-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f2f37-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f2f37-121">-DestFileSystem</span><span class="sxs-lookup"><span data-stu-id="f2f37-121">-DestFileSystem</span></span>
<span data-ttu-id="f2f37-122">Mål fil namn</span><span class="sxs-lookup"><span data-stu-id="f2f37-122">Dest FileSystem name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2f37-123">-DestPath</span><span class="sxs-lookup"><span data-stu-id="f2f37-123">-DestPath</span></span>
<span data-ttu-id="f2f37-124">Mål-BLOB</span><span class="sxs-lookup"><span data-stu-id="f2f37-124">Dest Blob path</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2f37-125">-Fil system</span><span class="sxs-lookup"><span data-stu-id="f2f37-125">-FileSystem</span></span>
<span data-ttu-id="f2f37-126">Fil Systems namn</span><span class="sxs-lookup"><span data-stu-id="f2f37-126">FileSystem name</span></span>

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

### <span data-ttu-id="f2f37-127">-Force</span><span class="sxs-lookup"><span data-stu-id="f2f37-127">-Force</span></span>
<span data-ttu-id="f2f37-128">Tvinga fram överskrivning av destinationen.</span><span class="sxs-lookup"><span data-stu-id="f2f37-128">Force to over write the destination.</span></span>

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

### <span data-ttu-id="f2f37-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f2f37-129">-InputObject</span></span>
<span data-ttu-id="f2f37-130">Azure Datalake Gen2 objekt objekt att flytta från.</span><span class="sxs-lookup"><span data-stu-id="f2f37-130">Azure Datalake Gen2 Item Object to move from.</span></span>

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

### <span data-ttu-id="f2f37-131">-Path</span><span class="sxs-lookup"><span data-stu-id="f2f37-131">-Path</span></span>
<span data-ttu-id="f2f37-132">Sökvägen i angivet filesystem som ska flyttas från.</span><span class="sxs-lookup"><span data-stu-id="f2f37-132">The path in the specified Filesystem that should be move from.</span></span>
<span data-ttu-id="f2f37-133">Kan vara en fil eller katalog i formatet ' katalog/file.txt ' eller ' directory1/directory2/'</span><span class="sxs-lookup"><span data-stu-id="f2f37-133">Can be a file or directory In the format 'directory/file.txt' or 'directory1/directory2/'</span></span>

```yaml
Type: System.String
Parameter Sets: ReceiveManual
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f2f37-134">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="f2f37-134">-Confirm</span></span>
<span data-ttu-id="f2f37-135">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="f2f37-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f2f37-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f2f37-136">-WhatIf</span></span>
<span data-ttu-id="f2f37-137">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="f2f37-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f2f37-138">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="f2f37-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f2f37-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2f37-139">CommonParameters</span></span>
<span data-ttu-id="f2f37-140">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f2f37-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2f37-141">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f2f37-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2f37-142">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f2f37-142">INPUTS</span></span>

### <span data-ttu-id="f2f37-143">System. String</span><span class="sxs-lookup"><span data-stu-id="f2f37-143">System.String</span></span>

### <span data-ttu-id="f2f37-144">Microsoft. WindowsAzure. commands. Common. Storage. ResourceModel. AzureDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="f2f37-144">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item</span></span>

### <span data-ttu-id="f2f37-145">Microsoft. Azure. commands. Common. verifikation. abstraktioner. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="f2f37-145">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="f2f37-146">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f2f37-146">OUTPUTS</span></span>

### <span data-ttu-id="f2f37-147">Microsoft. WindowsAzure. commands. Common. Storage. ResourceModel. AzureDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="f2f37-147">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item</span></span>

## <span data-ttu-id="f2f37-148">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f2f37-148">NOTES</span></span>

## <span data-ttu-id="f2f37-149">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f2f37-149">RELATED LINKS</span></span>
