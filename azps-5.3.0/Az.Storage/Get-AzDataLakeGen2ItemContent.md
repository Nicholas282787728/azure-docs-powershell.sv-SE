---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azdatalakegen2itemcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzDataLakeGen2ItemContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzDataLakeGen2ItemContent.md
ms.openlocfilehash: 9721305494ffd9b1d6a6f260008f050c9600437a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98420091"
---
# <span data-ttu-id="d9a0b-101">Get-AzDataLakeGen2ItemContent</span><span class="sxs-lookup"><span data-stu-id="d9a0b-101">Get-AzDataLakeGen2ItemContent</span></span>

## <span data-ttu-id="d9a0b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d9a0b-102">SYNOPSIS</span></span>
<span data-ttu-id="d9a0b-103">Ladda ned en fil.</span><span class="sxs-lookup"><span data-stu-id="d9a0b-103">Download a file.</span></span>

## <span data-ttu-id="d9a0b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d9a0b-104">SYNTAX</span></span>

### <span data-ttu-id="d9a0b-105">ReceiveManual (standard)</span><span class="sxs-lookup"><span data-stu-id="d9a0b-105">ReceiveManual (Default)</span></span>
```
Get-AzDataLakeGen2ItemContent [-FileSystem] <String> [-Path] <String> [-Destination <String>] [-CheckMd5]
 [-Force] [-AsJob] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d9a0b-106">ItemPipeline</span><span class="sxs-lookup"><span data-stu-id="d9a0b-106">ItemPipeline</span></span>
```
Get-AzDataLakeGen2ItemContent -InputObject <AzureDataLakeGen2Item> [-Destination <String>] [-CheckMd5] [-Force]
 [-AsJob] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d9a0b-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d9a0b-107">DESCRIPTION</span></span>
<span data-ttu-id="d9a0b-108">Cmdleten **Get-AzDataLakeGen2ItemContent** laddar ned en fil i ett fil system i ett Azure Storage-konto.</span><span class="sxs-lookup"><span data-stu-id="d9a0b-108">The **Get-AzDataLakeGen2ItemContent** cmdlet download a file in a Filesystem in an Azure storage account.</span></span>
<span data-ttu-id="d9a0b-109">Denna cmdlet fungerar bara om hierarkisk namnrymd är aktiverat för lagrings kontot.</span><span class="sxs-lookup"><span data-stu-id="d9a0b-109">This cmdlet only works if Hierarchical Namespace is enabled for the Storage account.</span></span> <span data-ttu-id="d9a0b-110">Den här typen av konto kan skapas med kör "New-AzStorageAccount"-cmdlet med "-EnableHierarchicalNamespace $true".</span><span class="sxs-lookup"><span data-stu-id="d9a0b-110">This kind of account can be created by run "New-AzStorageAccount" cmdlet with "-EnableHierarchicalNamespace $true".</span></span>

## <span data-ttu-id="d9a0b-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d9a0b-111">EXAMPLES</span></span>

### <span data-ttu-id="d9a0b-112">Exempel 1: Ladda ned en fil utan att fråga</span><span class="sxs-lookup"><span data-stu-id="d9a0b-112">Example 1: Download a file without prompt</span></span>
```
PS C:\> Get-AzDataLakeGen2ItemContent -FileSystem "filesystem1" -Path "dir1/file1" -Destination $localDestFile -Force

   FileSystem Name: filesystem1

Path                 IsDirectory  Length          LastModified         Permissions  Owner                Group               
----                 -----------  ------          ------------         -----------  -----                -----               
dir1/file1           False        1024            2020-03-23 09:29:18Z rwx---rwx    $superuser           $superuser
```

<span data-ttu-id="d9a0b-113">Det här kommandot laddar ned en fil till en lokal fil utan att fråga.</span><span class="sxs-lookup"><span data-stu-id="d9a0b-113">This command downloads a file to a local file without prompt.</span></span>

### <span data-ttu-id="d9a0b-114">Exempel 2: Hämta en fil, och sedan ladda ned filen till en lokal fil</span><span class="sxs-lookup"><span data-stu-id="d9a0b-114">Example 2: Get a file, then pipeline to download the file to a local file</span></span>
```
PS C:\> Get-AzDataLakeGen2Item -FileSystem "filesystem1" -Path "dir1/file1" |  Get-AzDataLakeGen2ItemContent -Destination $localDestFile 

   FileSystem Name: filesystem1

Path                 IsDirectory  Length          LastModified         Permissions  Owner                Group               
----                 -----------  ------          ------------         -----------  -----                -----               
dir1/file1           False        1024            2020-03-23 09:29:18Z rwx---rwx    $superuser           $superuser
```

<span data-ttu-id="d9a0b-115">Kommandot får först en fil och sedan kan du ladda ned filen till en lokal fil.</span><span class="sxs-lookup"><span data-stu-id="d9a0b-115">This command first gets a file, then pipeline to download the file to a local file.</span></span>

## <span data-ttu-id="d9a0b-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d9a0b-116">PARAMETERS</span></span>

### <span data-ttu-id="d9a0b-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d9a0b-117">-AsJob</span></span>
<span data-ttu-id="d9a0b-118">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="d9a0b-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d9a0b-119">-CheckMd5</span><span class="sxs-lookup"><span data-stu-id="d9a0b-119">-CheckMd5</span></span>
<span data-ttu-id="d9a0b-120">Kolla md5sum</span><span class="sxs-lookup"><span data-stu-id="d9a0b-120">check the md5sum</span></span>

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

### <span data-ttu-id="d9a0b-121">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="d9a0b-121">-ConcurrentTaskCount</span></span>
<span data-ttu-id="d9a0b-122">Totalt antal samtidiga asynkrona uppgifter.</span><span class="sxs-lookup"><span data-stu-id="d9a0b-122">The total amount of concurrent async tasks.</span></span>
<span data-ttu-id="d9a0b-123">Standardvärdet är 10.</span><span class="sxs-lookup"><span data-stu-id="d9a0b-123">The default value is 10.</span></span>

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

### <span data-ttu-id="d9a0b-124">-Kontext</span><span class="sxs-lookup"><span data-stu-id="d9a0b-124">-Context</span></span>
<span data-ttu-id="d9a0b-125">Kontext objekt för Azure-lagring</span><span class="sxs-lookup"><span data-stu-id="d9a0b-125">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="d9a0b-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9a0b-126">-DefaultProfile</span></span>
<span data-ttu-id="d9a0b-127">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d9a0b-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d9a0b-128">-Mål</span><span class="sxs-lookup"><span data-stu-id="d9a0b-128">-Destination</span></span>
<span data-ttu-id="d9a0b-129">Sökväg till lokal fil.</span><span class="sxs-lookup"><span data-stu-id="d9a0b-129">Destination local file path.</span></span>

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

### <span data-ttu-id="d9a0b-130">-Fil system</span><span class="sxs-lookup"><span data-stu-id="d9a0b-130">-FileSystem</span></span>
<span data-ttu-id="d9a0b-131">Fil Systems namn</span><span class="sxs-lookup"><span data-stu-id="d9a0b-131">FileSystem name</span></span>

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

### <span data-ttu-id="d9a0b-132">-Force</span><span class="sxs-lookup"><span data-stu-id="d9a0b-132">-Force</span></span>
<span data-ttu-id="d9a0b-133">Tvinga att skriva över befintlig BLOB eller fil</span><span class="sxs-lookup"><span data-stu-id="d9a0b-133">Force to overwrite the existing blob or file</span></span>

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

### <span data-ttu-id="d9a0b-134">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d9a0b-134">-InputObject</span></span>
<span data-ttu-id="d9a0b-135">Azure Datalake Gen2 objekt för nedladdning.</span><span class="sxs-lookup"><span data-stu-id="d9a0b-135">Azure Datalake Gen2 Item Object to download.</span></span>

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

### <span data-ttu-id="d9a0b-136">-Path</span><span class="sxs-lookup"><span data-stu-id="d9a0b-136">-Path</span></span>
<span data-ttu-id="d9a0b-137">Sökvägen i angivet filesystem som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="d9a0b-137">The path in the specified Filesystem that should be removed.</span></span>
<span data-ttu-id="d9a0b-138">Kan vara en fil eller katalog i formatet ' katalog/file.txt ' eller ' directory1/directory2/'</span><span class="sxs-lookup"><span data-stu-id="d9a0b-138">Can be a file or directory In the format 'directory/file.txt' or 'directory1/directory2/'</span></span>

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

### <span data-ttu-id="d9a0b-139">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="d9a0b-139">-Confirm</span></span>
<span data-ttu-id="d9a0b-140">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="d9a0b-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d9a0b-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d9a0b-141">-WhatIf</span></span>
<span data-ttu-id="d9a0b-142">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="d9a0b-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d9a0b-143">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="d9a0b-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d9a0b-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9a0b-144">CommonParameters</span></span>
<span data-ttu-id="d9a0b-145">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d9a0b-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9a0b-146">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d9a0b-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9a0b-147">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d9a0b-147">INPUTS</span></span>

### <span data-ttu-id="d9a0b-148">System. String</span><span class="sxs-lookup"><span data-stu-id="d9a0b-148">System.String</span></span>

### <span data-ttu-id="d9a0b-149">Microsoft. WindowsAzure. commands. Common. Storage. ResourceModel. AzureDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="d9a0b-149">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item</span></span>

### <span data-ttu-id="d9a0b-150">Microsoft. Azure. commands. Common. verifikation. abstraktioner. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="d9a0b-150">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="d9a0b-151">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d9a0b-151">OUTPUTS</span></span>

### <span data-ttu-id="d9a0b-152">Microsoft. WindowsAzure. commands. Common. Storage. ResourceModel. AzureDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="d9a0b-152">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item</span></span>

## <span data-ttu-id="d9a0b-153">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d9a0b-153">NOTES</span></span>

## <span data-ttu-id="d9a0b-154">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d9a0b-154">RELATED LINKS</span></span>
