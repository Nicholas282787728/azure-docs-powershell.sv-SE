---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 90630395-8747-4446-A879-323274811956
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Import-AzureRmDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Import-AzureRmDataLakeStoreItem.md
ms.openlocfilehash: ed10d3ee7c5a35c039a19f44211c7c2fce08aa06
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756975"
---
# <span data-ttu-id="6d1a6-101">Import-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="6d1a6-101">Import-AzureRmDataLakeStoreItem</span></span>

## <span data-ttu-id="6d1a6-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6d1a6-102">SYNOPSIS</span></span>
<span data-ttu-id="6d1a6-103">Laddar upp en lokal fil eller katalog till en data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="6d1a6-103">Uploads a local file or directory to a Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6d1a6-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6d1a6-104">SYNTAX</span></span>

### <span data-ttu-id="6d1a6-105">Ingen diagnostikloggning (standard)</span><span class="sxs-lookup"><span data-stu-id="6d1a6-105">No diagnostic logging (Default)</span></span>
```
Import-AzureRmDataLakeStoreItem [-Account] <String> [-Path] <String> [-Destination] <DataLakeStorePathInstance>
 [-Recurse] [-Resume] [-ForceBinary] [[-PerFileThreadCount] <Int32>] [[-ConcurrentFileCount] <Int32>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6d1a6-106">Inkludera diagnostikloggning</span><span class="sxs-lookup"><span data-stu-id="6d1a6-106">Include diagnostic logging</span></span>
```
Import-AzureRmDataLakeStoreItem [-Account] <String> [-Path] <String> [-Destination] <DataLakeStorePathInstance>
 [-Recurse] [-Resume] [-ForceBinary] [[-PerFileThreadCount] <Int32>] [[-ConcurrentFileCount] <Int32>] [-Force]
 [-DiagnosticLogLevel <LogLevel>] -DiagnosticLogPath <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6d1a6-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6d1a6-107">DESCRIPTION</span></span>
<span data-ttu-id="6d1a6-108">Cmdleten **import-AzureRmDataLakeStoreItem** laddar upp en lokal fil eller katalog till en data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="6d1a6-108">The **Import-AzureRmDataLakeStoreItem** cmdlet uploads a local file or directory to a Data Lake Store.</span></span>

## <span data-ttu-id="6d1a6-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6d1a6-109">EXAMPLES</span></span>

### <span data-ttu-id="6d1a6-110">Exempel 1: Ladda upp en fil</span><span class="sxs-lookup"><span data-stu-id="6d1a6-110">Example 1: Upload a file</span></span>
```
PS C:\>Import-AzureRmDataLakeStoreItem -AccountName "ContosoADL" -Path "C:\SrcFile.csv" -Destination "/MyFiles/File.csv"
```

<span data-ttu-id="6d1a6-111">Det här kommandot laddar upp filen SrcFile.csv och lägger till den i mappen Mina filer i data Lake Store som File.csv.</span><span class="sxs-lookup"><span data-stu-id="6d1a6-111">This command uploads the file SrcFile.csv and adds it to the MyFiles folder in the Data Lake Store as File.csv.</span></span>

## <span data-ttu-id="6d1a6-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6d1a6-112">PARAMETERS</span></span>

### <span data-ttu-id="6d1a6-113">-Konto</span><span class="sxs-lookup"><span data-stu-id="6d1a6-113">-Account</span></span>
<span data-ttu-id="6d1a6-114">Anger namnet på data Lake Store-kontot.</span><span class="sxs-lookup"><span data-stu-id="6d1a6-114">Specifies the name of the Data Lake Store account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d1a6-115">-ConcurrentFileCount</span><span class="sxs-lookup"><span data-stu-id="6d1a6-115">-ConcurrentFileCount</span></span>
<span data-ttu-id="6d1a6-116">Ange maximalt antal filer som ska laddas upp parallellt för en uppladdning av en mapp.</span><span class="sxs-lookup"><span data-stu-id="6d1a6-116">Specify the maximum number of files to upload in parallel for a folder upload.</span></span>
<span data-ttu-id="6d1a6-117">Standardvärdet är fem (5).</span><span class="sxs-lookup"><span data-stu-id="6d1a6-117">The default value is five (5).</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d1a6-118">-Mål</span><span class="sxs-lookup"><span data-stu-id="6d1a6-118">-Destination</span></span>
<span data-ttu-id="6d1a6-119">Anger sökvägen till data Lake Store dit du vill ladda upp en fil eller mapp från rot katalogen (/).</span><span class="sxs-lookup"><span data-stu-id="6d1a6-119">Specifies the Data Lake Store path to which to upload a file or folder, starting with the root directory (/).</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d1a6-120">-DiagnosticLogLevel</span><span class="sxs-lookup"><span data-stu-id="6d1a6-120">-DiagnosticLogLevel</span></span>
<span data-ttu-id="6d1a6-121">Anger om den diagnostiska loggnings nivå som ska användas för att registrera händelser under fil-eller mapp-importen.</span><span class="sxs-lookup"><span data-stu-id="6d1a6-121">Optionally indicates the diagnostic log level to use to record events during the file or folder import.</span></span> <span data-ttu-id="6d1a6-122">Standard är ett fel.</span><span class="sxs-lookup"><span data-stu-id="6d1a6-122">Default is Error.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.LogLevel
Parameter Sets: Include diagnostic logging
Aliases: 
Accepted values: Debug, Information, Error, None

Required: False
Position: Named
Default value: Error
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d1a6-123">-DiagnosticLogPath</span><span class="sxs-lookup"><span data-stu-id="6d1a6-123">-DiagnosticLogPath</span></span>
<span data-ttu-id="6d1a6-124">Anger sökvägen till Diagnostikrapporten för att spela in händelser för fil-eller mapp.</span><span class="sxs-lookup"><span data-stu-id="6d1a6-124">Specifies the path for the diagnostic log to record events to during the file or folder import.</span></span>

```yaml
Type: System.String
Parameter Sets: Include diagnostic logging
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d1a6-125">-Force</span><span class="sxs-lookup"><span data-stu-id="6d1a6-125">-Force</span></span>
<span data-ttu-id="6d1a6-126">Anger att den här åtgärden kan skriva över målfilen om den redan finns.</span><span class="sxs-lookup"><span data-stu-id="6d1a6-126">Indicates that this operation can overwrite the destination file if it already exists.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d1a6-127">-ForceBinary</span><span class="sxs-lookup"><span data-stu-id="6d1a6-127">-ForceBinary</span></span>
<span data-ttu-id="6d1a6-128">Anger att den här åtgärden laddar upp filen som en binär fil.</span><span class="sxs-lookup"><span data-stu-id="6d1a6-128">Indicates that this operation uploads the file as a binary file.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d1a6-129">-Path</span><span class="sxs-lookup"><span data-stu-id="6d1a6-129">-Path</span></span>
<span data-ttu-id="6d1a6-130">Anger den lokala sökvägen till filen eller mappen som ska laddas upp.</span><span class="sxs-lookup"><span data-stu-id="6d1a6-130">Specifies the local path of the file or folder to upload.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d1a6-131">-PerFileThreadCount</span><span class="sxs-lookup"><span data-stu-id="6d1a6-131">-PerFileThreadCount</span></span>
<span data-ttu-id="6d1a6-132">Anger maximalt antal trådar som ska användas per fil.</span><span class="sxs-lookup"><span data-stu-id="6d1a6-132">Specifies the maximum number of threads to use per file.</span></span>
<span data-ttu-id="6d1a6-133">Standardvärdet är tio (10).</span><span class="sxs-lookup"><span data-stu-id="6d1a6-133">The default value is ten (10).</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d1a6-134">-Recurse</span><span class="sxs-lookup"><span data-stu-id="6d1a6-134">-Recurse</span></span>
<span data-ttu-id="6d1a6-135">Anger att den här åtgärden ska ladda upp alla objekt i alla undermappar.</span><span class="sxs-lookup"><span data-stu-id="6d1a6-135">Indicates that this operation should upload all items in all subfolders.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d1a6-136">-Fortsätt</span><span class="sxs-lookup"><span data-stu-id="6d1a6-136">-Resume</span></span>
<span data-ttu-id="6d1a6-137">Anger att åtgärden ska återuppta en tidigare avbruten eller misslyckad uppladdning.</span><span class="sxs-lookup"><span data-stu-id="6d1a6-137">Indicates that this operation should resume a previously canceled or failed upload.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d1a6-138">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="6d1a6-138">-Confirm</span></span>
<span data-ttu-id="6d1a6-139">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="6d1a6-139">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d1a6-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6d1a6-140">-WhatIf</span></span>
<span data-ttu-id="6d1a6-141">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="6d1a6-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6d1a6-142">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="6d1a6-142">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d1a6-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d1a6-143">-DefaultProfile</span></span>
<span data-ttu-id="6d1a6-144">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="6d1a6-144">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6d1a6-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d1a6-145">CommonParameters</span></span>
<span data-ttu-id="6d1a6-146">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6d1a6-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d1a6-147">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6d1a6-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d1a6-148">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6d1a6-148">INPUTS</span></span>

## <span data-ttu-id="6d1a6-149">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6d1a6-149">OUTPUTS</span></span>

### <span data-ttu-id="6d1a6-150">strängvärdet</span><span class="sxs-lookup"><span data-stu-id="6d1a6-150">string</span></span>
<span data-ttu-id="6d1a6-151">Den fullständiga sökvägen till den uppladdade filen eller mappen.</span><span class="sxs-lookup"><span data-stu-id="6d1a6-151">The full path in the Data Lake Store account to the uploaded file or folder.</span></span>

## <span data-ttu-id="6d1a6-152">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6d1a6-152">NOTES</span></span>

## <span data-ttu-id="6d1a6-153">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6d1a6-153">RELATED LINKS</span></span>

[<span data-ttu-id="6d1a6-154">Get-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="6d1a6-154">Get-AzureRmDataLakeStoreItem</span></span>](./Get-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="6d1a6-155">Exportera-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="6d1a6-155">Export-AzureRmDataLakeStoreItem</span></span>](./Export-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="6d1a6-156">Anslut-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="6d1a6-156">Join-AzureRmDataLakeStoreItem</span></span>](./Join-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="6d1a6-157">Move-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="6d1a6-157">Move-AzureRmDataLakeStoreItem</span></span>](./Move-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="6d1a6-158">New-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="6d1a6-158">New-AzureRmDataLakeStoreItem</span></span>](./New-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="6d1a6-159">Remove-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="6d1a6-159">Remove-AzureRmDataLakeStoreItem</span></span>](./Remove-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="6d1a6-160">Test-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="6d1a6-160">Test-AzureRmDataLakeStoreItem</span></span>](./Test-AzureRmDataLakeStoreItem.md)


