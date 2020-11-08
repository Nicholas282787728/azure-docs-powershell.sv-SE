---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azdatalakegen2item
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzDataLakeGen2Item.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzDataLakeGen2Item.md
ms.openlocfilehash: 06bb30dd98c491267675893192f61d4eb61529bf
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94092402"
---
# <span data-ttu-id="678f5-101">Remove-AzDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="678f5-101">Remove-AzDataLakeGen2Item</span></span>

## <span data-ttu-id="678f5-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="678f5-102">SYNOPSIS</span></span>
<span data-ttu-id="678f5-103">Ta bort en fil eller katalog.</span><span class="sxs-lookup"><span data-stu-id="678f5-103">Remove a file or directory.</span></span>

## <span data-ttu-id="678f5-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="678f5-104">SYNTAX</span></span>

### <span data-ttu-id="678f5-105">ReceiveManual (standard)</span><span class="sxs-lookup"><span data-stu-id="678f5-105">ReceiveManual (Default)</span></span>
```
Remove-AzDataLakeGen2Item [-FileSystem] <String> [-Path] <String> [-Force] [-AsJob] [-PassThru]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="678f5-106">ItemPipeline</span><span class="sxs-lookup"><span data-stu-id="678f5-106">ItemPipeline</span></span>
```
Remove-AzDataLakeGen2Item -InputObject <AzureDataLakeGen2Item> [-Force] [-AsJob] [-PassThru]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="678f5-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="678f5-107">DESCRIPTION</span></span>
<span data-ttu-id="678f5-108">Cmdleten **Remove-AzDataLakeGen2Item** tar bort en fil eller katalog från ett lagrings konto.</span><span class="sxs-lookup"><span data-stu-id="678f5-108">The **Remove-AzDataLakeGen2Item** cmdlet removes a file or directory from a Storage account.</span></span>
<span data-ttu-id="678f5-109">Denna cmdlet fungerar bara om hierarkisk namnrymd är aktiverat för lagrings kontot.</span><span class="sxs-lookup"><span data-stu-id="678f5-109">This cmdlet only works if Hierarchical Namespace is enabled for the Storage account.</span></span> <span data-ttu-id="678f5-110">Den här typen av konto kan skapas med kör "New-AzStorageAccount"-cmdlet med "-EnableHierarchicalNamespace $true".</span><span class="sxs-lookup"><span data-stu-id="678f5-110">This kind of account can be created by run "New-AzStorageAccount" cmdlet with "-EnableHierarchicalNamespace $true".</span></span>

## <span data-ttu-id="678f5-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="678f5-111">EXAMPLES</span></span>

### <span data-ttu-id="678f5-112">Exempel 1: tar bort en katalog</span><span class="sxs-lookup"><span data-stu-id="678f5-112">Example 1: Removes a directory</span></span>
```
PS C:\>Remove-AzDataLakeGen2tem -FileSystem "filesystem1" -Path "dir1/"
```

<span data-ttu-id="678f5-113">Det här kommandot tar bort en katalog från ett fil system.</span><span class="sxs-lookup"><span data-stu-id="678f5-113">This command removes a directory from a Filesystem.</span></span>

### <span data-ttu-id="678f5-114">Exempel 2: tar bort en fil utan fråga</span><span class="sxs-lookup"><span data-stu-id="678f5-114">Example 2: Removes a file without prompt</span></span>
```
PS C:\>Remove-AzDataLakeGen2tem -FileSystem "filesystem1" -Path "dir1/file1" -Force
```

<span data-ttu-id="678f5-115">Det här kommandot tar bort en katalog från ett filesystem utan att fråga.</span><span class="sxs-lookup"><span data-stu-id="678f5-115">This command removes a directory from a Filesystem, without prompt.</span></span>

### <span data-ttu-id="678f5-116">Exempel 3: ta bort alla objekt i ett filesystem med pipeline</span><span class="sxs-lookup"><span data-stu-id="678f5-116">Example 3: Remove all items in a Filesystem with pipeline</span></span>
```
PS C:\>Get-AzDataLakeGen2ChildItem -FileSystem "filesystem1" | Remove-AzDataLakeGen2Item -Force
```

<span data-ttu-id="678f5-117">Det här kommandot tar bort alla objekt i ett filesystem med pipeline.</span><span class="sxs-lookup"><span data-stu-id="678f5-117">This command removes all items in a Filesystem with pipeline.</span></span>

## <span data-ttu-id="678f5-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="678f5-118">PARAMETERS</span></span>

### <span data-ttu-id="678f5-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="678f5-119">-AsJob</span></span>
<span data-ttu-id="678f5-120">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="678f5-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="678f5-121">-Kontext</span><span class="sxs-lookup"><span data-stu-id="678f5-121">-Context</span></span>
<span data-ttu-id="678f5-122">Kontext objekt för Azure-lagring</span><span class="sxs-lookup"><span data-stu-id="678f5-122">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="678f5-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="678f5-123">-DefaultProfile</span></span>
<span data-ttu-id="678f5-124">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="678f5-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="678f5-125">-Fil system</span><span class="sxs-lookup"><span data-stu-id="678f5-125">-FileSystem</span></span>
<span data-ttu-id="678f5-126">Fil Systems namn</span><span class="sxs-lookup"><span data-stu-id="678f5-126">FileSystem name</span></span>

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

### <span data-ttu-id="678f5-127">-Force</span><span class="sxs-lookup"><span data-stu-id="678f5-127">-Force</span></span>
<span data-ttu-id="678f5-128">Tvinga att ta bort fil systemet och allt innehåll i det</span><span class="sxs-lookup"><span data-stu-id="678f5-128">Force to remove the Filesystem and all content in it</span></span>

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

### <span data-ttu-id="678f5-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="678f5-129">-InputObject</span></span>
<span data-ttu-id="678f5-130">Azure Datalake Gen2 objekt objekt som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="678f5-130">Azure Datalake Gen2 Item Object to remove.</span></span>

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

### <span data-ttu-id="678f5-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="678f5-131">-PassThru</span></span>
<span data-ttu-id="678f5-132">Returnera om det angivna fil systemet har tagits bort</span><span class="sxs-lookup"><span data-stu-id="678f5-132">Return whether the specified Filesystem is successfully removed</span></span>

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

### <span data-ttu-id="678f5-133">-Path</span><span class="sxs-lookup"><span data-stu-id="678f5-133">-Path</span></span>
<span data-ttu-id="678f5-134">Sökvägen i angivet filesystem som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="678f5-134">The path in the specified Filesystem that should be removed.</span></span>
<span data-ttu-id="678f5-135">Kan vara en fil eller katalog i formatet ' katalog/file.txt ' eller ' directory1/directory2/'</span><span class="sxs-lookup"><span data-stu-id="678f5-135">Can be a file or directory In the format 'directory/file.txt' or 'directory1/directory2/'</span></span>

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

### <span data-ttu-id="678f5-136">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="678f5-136">-Confirm</span></span>
<span data-ttu-id="678f5-137">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="678f5-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="678f5-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="678f5-138">-WhatIf</span></span>
<span data-ttu-id="678f5-139">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="678f5-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="678f5-140">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="678f5-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="678f5-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="678f5-141">CommonParameters</span></span>
<span data-ttu-id="678f5-142">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="678f5-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="678f5-143">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="678f5-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="678f5-144">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="678f5-144">INPUTS</span></span>

### <span data-ttu-id="678f5-145">System. String</span><span class="sxs-lookup"><span data-stu-id="678f5-145">System.String</span></span>

### <span data-ttu-id="678f5-146">Microsoft. WindowsAzure. commands. Common. Storage. ResourceModel. AzureDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="678f5-146">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item</span></span>

### <span data-ttu-id="678f5-147">Microsoft. Azure. commands. Common. verifikation. abstraktioner. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="678f5-147">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="678f5-148">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="678f5-148">OUTPUTS</span></span>

### <span data-ttu-id="678f5-149">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="678f5-149">System.Boolean</span></span>

## <span data-ttu-id="678f5-150">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="678f5-150">NOTES</span></span>

## <span data-ttu-id="678f5-151">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="678f5-151">RELATED LINKS</span></span>
