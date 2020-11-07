---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: B10B1F5D-5566-4129-9D42-05A6D3B72C9E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/export-azurermdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Export-AzureRmDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Export-AzureRmDataLakeStoreItem.md
ms.openlocfilehash: 907e4e92b511349011b27cb8aaf7588b8e495220
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93755604"
---
# <span data-ttu-id="479f5-101">Export-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="479f5-101">Export-AzureRmDataLakeStoreItem</span></span>

## <span data-ttu-id="479f5-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="479f5-102">SYNOPSIS</span></span>
<span data-ttu-id="479f5-103">Laddar ned en fil från data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="479f5-103">Downloads a file from Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="479f5-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="479f5-104">SYNTAX</span></span>

### <span data-ttu-id="479f5-105">NoDiagnosticLogging (standard)</span><span class="sxs-lookup"><span data-stu-id="479f5-105">NoDiagnosticLogging (Default)</span></span>
```
Export-AzureRmDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Destination] <String>
 [-Recurse] [-Resume] [[-PerFileThreadCount] <Int32>] [[-ConcurrentFileCount] <Int32>] [[-Concurrency] <Int32>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="479f5-106">IncludeDiagnosticLogging</span><span class="sxs-lookup"><span data-stu-id="479f5-106">IncludeDiagnosticLogging</span></span>
```
Export-AzureRmDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Destination] <String>
 [-Recurse] [-Resume] [[-PerFileThreadCount] <Int32>] [[-ConcurrentFileCount] <Int32>] [[-Concurrency] <Int32>] [-Force]
 [-DiagnosticLogLevel <LogLevel>] -DiagnosticLogPath <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="479f5-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="479f5-107">DESCRIPTION</span></span>
<span data-ttu-id="479f5-108">Cmdleten **export-AzureRmDataLakeStoreItem** laddar ned en fil från data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="479f5-108">The **Export-AzureRmDataLakeStoreItem** cmdlet downloads a file from Data Lake Store.</span></span>

## <span data-ttu-id="479f5-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="479f5-109">EXAMPLES</span></span>

### <span data-ttu-id="479f5-110">Exempel 1: Hämta ett objekt från data Lake Store</span><span class="sxs-lookup"><span data-stu-id="479f5-110">Example 1: Download an item from the Data Lake Store</span></span>
```
PS C:\>Export-AzureRmDataLakeStoreItem -AccountName "ContosoADL" -Path /myFiles/TestSource.csv -Destination "C:\Test.csv" -Concurrency 4
```

<span data-ttu-id="479f5-111">Det här kommandot laddar ned filen TestSource.csv från data Lake Store till C:\Test.csv med en concurrency på 4.</span><span class="sxs-lookup"><span data-stu-id="479f5-111">This command downloads the file TestSource.csv from the Data Lake Store to C:\Test.csv with a concurrency of 4.</span></span>

## <span data-ttu-id="479f5-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="479f5-112">PARAMETERS</span></span>

### <span data-ttu-id="479f5-113">-Konto</span><span class="sxs-lookup"><span data-stu-id="479f5-113">-Account</span></span>
<span data-ttu-id="479f5-114">Anger namnet på data Lake Store-kontot.</span><span class="sxs-lookup"><span data-stu-id="479f5-114">Specifies the name of the Data Lake Store account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="479f5-115">-Concurrency</span><span class="sxs-lookup"><span data-stu-id="479f5-115">-Concurrency</span></span>
<span data-ttu-id="479f5-116">Anger hur många filer eller delar som ska laddas ned parallellt.</span><span class="sxs-lookup"><span data-stu-id="479f5-116">Indicates the number of files or chunks to download in parallel.</span></span> <span data-ttu-id="479f5-117">Standard beräknas som en bästa ansträngning baserat på Systemspecifikationer.</span><span class="sxs-lookup"><span data-stu-id="479f5-117">Default will be computed as a best effort based on system specifications.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="479f5-118">-ConcurrentFileCount</span><span class="sxs-lookup"><span data-stu-id="479f5-118">-ConcurrentFileCount</span></span>
<span data-ttu-id="479f5-119">Anger det maximala antalet filer som laddas ned parallellt för en mapp nedladdning.</span><span class="sxs-lookup"><span data-stu-id="479f5-119">Indicates the maximum number of files to download in parallel for a folder download.</span></span>  <span data-ttu-id="479f5-120">Standard beräknas som en bästa ansträngning baserat på mapp-och fil storlek</span><span class="sxs-lookup"><span data-stu-id="479f5-120">Default will be computed as a best effort based on folder and file size</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="479f5-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="479f5-121">-DefaultProfile</span></span>
<span data-ttu-id="479f5-122">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="479f5-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="479f5-123">-Mål</span><span class="sxs-lookup"><span data-stu-id="479f5-123">-Destination</span></span>
<span data-ttu-id="479f5-124">Anger den lokala fil Sök vägen som filen ska hämtas till.</span><span class="sxs-lookup"><span data-stu-id="479f5-124">Specifies the local file path to which to download the file.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="479f5-125">-DiagnosticLogLevel</span><span class="sxs-lookup"><span data-stu-id="479f5-125">-DiagnosticLogLevel</span></span>
<span data-ttu-id="479f5-126">Anger om den diagnostiska loggnings nivå som ska användas för att registrera händelser under fil-eller mapp-importen.</span><span class="sxs-lookup"><span data-stu-id="479f5-126">Optionally indicates the diagnostic log level to use to record events during the file or folder import.</span></span> <span data-ttu-id="479f5-127">Standard är ett fel.</span><span class="sxs-lookup"><span data-stu-id="479f5-127">Default is Error.</span></span>

```yaml
Type: LogLevel
Parameter Sets: IncludeDiagnosticLogging
Aliases: 
Accepted values: Debug, Information, Error, None

Required: False
Position: Named
Default value: Error
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="479f5-128">-DiagnosticLogPath</span><span class="sxs-lookup"><span data-stu-id="479f5-128">-DiagnosticLogPath</span></span>
<span data-ttu-id="479f5-129">Anger sökvägen till Diagnostikrapporten för att spela in händelser för fil-eller mapp.</span><span class="sxs-lookup"><span data-stu-id="479f5-129">Specifies the path for the diagnostic log to record events to during the file or folder import.</span></span>

```yaml
Type: String
Parameter Sets: IncludeDiagnosticLogging
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="479f5-130">-Force</span><span class="sxs-lookup"><span data-stu-id="479f5-130">-Force</span></span>
<span data-ttu-id="479f5-131">Anger att den här åtgärden kan skriva över målfilen om den redan finns.</span><span class="sxs-lookup"><span data-stu-id="479f5-131">Indicates that this operation can overwrite the destination file if it already exists.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="479f5-132">-Path</span><span class="sxs-lookup"><span data-stu-id="479f5-132">-Path</span></span>
<span data-ttu-id="479f5-133">Anger sökvägen för det objekt som ska hämtas från data Lake Store från rot katalogen (/).</span><span class="sxs-lookup"><span data-stu-id="479f5-133">Specifies the path of the item to download from the Data Lake Store, starting from the root directory (/).</span></span>

```yaml
Type: DataLakeStorePathInstance
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="479f5-134">-PerFileThreadCount</span><span class="sxs-lookup"><span data-stu-id="479f5-134">-PerFileThreadCount</span></span>
<span data-ttu-id="479f5-135">Anger maximalt antal trådar som ska användas per fil.</span><span class="sxs-lookup"><span data-stu-id="479f5-135">Indicates the maximum number of threads to use per file.</span></span>  <span data-ttu-id="479f5-136">Standard beräknas som en bästa ansträngning baserat på mapp-och fil storlek</span><span class="sxs-lookup"><span data-stu-id="479f5-136">Default will be computed as a best effort based on folder and file size</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="479f5-137">-Recurse</span><span class="sxs-lookup"><span data-stu-id="479f5-137">-Recurse</span></span>
<span data-ttu-id="479f5-138">Anger att en mapp som laddas ned är rekursiv.</span><span class="sxs-lookup"><span data-stu-id="479f5-138">Indicates that a folder download is recursive.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="479f5-139">-Fortsätt</span><span class="sxs-lookup"><span data-stu-id="479f5-139">-Resume</span></span>
<span data-ttu-id="479f5-140">Anger att filen/filerna som kopieras är en fortsättning på en tidigare nedladdning.</span><span class="sxs-lookup"><span data-stu-id="479f5-140">Indicates that the file(s) being copied are a continuation of a previous download.</span></span>
<span data-ttu-id="479f5-141">Detta gör att systemet försöker återuppta från den senaste filen som inte laddats ned helt.</span><span class="sxs-lookup"><span data-stu-id="479f5-141">This will cause the system to attempt to resume from the last file that was not fully downloaded.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="479f5-142">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="479f5-142">-Confirm</span></span>
<span data-ttu-id="479f5-143">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="479f5-143">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="479f5-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="479f5-144">-WhatIf</span></span>
<span data-ttu-id="479f5-145">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="479f5-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="479f5-146">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="479f5-146">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="479f5-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="479f5-147">CommonParameters</span></span>
<span data-ttu-id="479f5-148">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="479f5-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="479f5-149">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="479f5-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="479f5-150">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="479f5-150">INPUTS</span></span>

### <span data-ttu-id="479f5-151">Ingen</span><span class="sxs-lookup"><span data-stu-id="479f5-151">None</span></span>
<span data-ttu-id="479f5-152">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="479f5-152">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="479f5-153">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="479f5-153">OUTPUTS</span></span>

### <span data-ttu-id="479f5-154">strängvärdet</span><span class="sxs-lookup"><span data-stu-id="479f5-154">string</span></span>
<span data-ttu-id="479f5-155">Sökvägen till filen eller mappen laddades ner till.</span><span class="sxs-lookup"><span data-stu-id="479f5-155">The path where the file or folder was downloaded to.</span></span>

## <span data-ttu-id="479f5-156">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="479f5-156">NOTES</span></span>

## <span data-ttu-id="479f5-157">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="479f5-157">RELATED LINKS</span></span>

[<span data-ttu-id="479f5-158">Get-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="479f5-158">Get-AzureRmDataLakeStoreItem</span></span>](./Get-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="479f5-159">Import-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="479f5-159">Import-AzureRmDataLakeStoreItem</span></span>](./Import-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="479f5-160">Anslut-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="479f5-160">Join-AzureRmDataLakeStoreItem</span></span>](./Join-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="479f5-161">Move-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="479f5-161">Move-AzureRmDataLakeStoreItem</span></span>](./Move-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="479f5-162">New-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="479f5-162">New-AzureRmDataLakeStoreItem</span></span>](./New-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="479f5-163">Remove-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="479f5-163">Remove-AzureRmDataLakeStoreItem</span></span>](./Remove-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="479f5-164">Test-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="479f5-164">Test-AzureRmDataLakeStoreItem</span></span>](./Test-AzureRmDataLakeStoreItem.md)


