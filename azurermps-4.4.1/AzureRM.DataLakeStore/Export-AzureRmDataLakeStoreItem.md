---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: B10B1F5D-5566-4129-9D42-05A6D3B72C9E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Export-AzureRmDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Export-AzureRmDataLakeStoreItem.md
ms.openlocfilehash: febcec4d309e849e3b259fc2d80b3129ca7b65f6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93582487"
---
# <span data-ttu-id="5af5c-101">Export-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="5af5c-101">Export-AzureRmDataLakeStoreItem</span></span>

## <span data-ttu-id="5af5c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5af5c-102">SYNOPSIS</span></span>
<span data-ttu-id="5af5c-103">Laddar ned en fil från data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="5af5c-103">Downloads a file from Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5af5c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5af5c-104">SYNTAX</span></span>

### <span data-ttu-id="5af5c-105">Ingen diagnostikloggning (standard)</span><span class="sxs-lookup"><span data-stu-id="5af5c-105">No diagnostic logging (Default)</span></span>
```
Export-AzureRmDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Destination] <String>
 [-Recurse] [-Resume] [[-PerFileThreadCount] <Int32>] [[-ConcurrentFileCount] <Int32>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5af5c-106">Inkludera diagnostikloggning</span><span class="sxs-lookup"><span data-stu-id="5af5c-106">Include diagnostic logging</span></span>
```
Export-AzureRmDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Destination] <String>
 [-Recurse] [-Resume] [[-PerFileThreadCount] <Int32>] [[-ConcurrentFileCount] <Int32>] [-Force]
 [-DiagnosticLogLevel <LogLevel>] -DiagnosticLogPath <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5af5c-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5af5c-107">DESCRIPTION</span></span>
<span data-ttu-id="5af5c-108">Cmdleten **export-AzureRmDataLakeStoreItem** laddar ned en fil från data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="5af5c-108">The **Export-AzureRmDataLakeStoreItem** cmdlet downloads a file from Data Lake Store.</span></span>

## <span data-ttu-id="5af5c-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5af5c-109">EXAMPLES</span></span>

### <span data-ttu-id="5af5c-110">Exempel 1: Hämta ett objekt från data Lake Store</span><span class="sxs-lookup"><span data-stu-id="5af5c-110">Example 1: Download an item from the Data Lake Store</span></span>
```
PS C:\>Export-AzureRmDataLakeStoreItem -AccountName "ContosoADL" -Path /myFiles/TestSource.csv -Destination "C:\Test.csv"
```

<span data-ttu-id="5af5c-111">Det här kommandot laddar ned filen TestSource.csv från data Lake Store till C:\Test.csv.</span><span class="sxs-lookup"><span data-stu-id="5af5c-111">This command downloads the file TestSource.csv from the Data Lake Store to C:\Test.csv.</span></span>

## <span data-ttu-id="5af5c-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5af5c-112">PARAMETERS</span></span>

### <span data-ttu-id="5af5c-113">-Konto</span><span class="sxs-lookup"><span data-stu-id="5af5c-113">-Account</span></span>
<span data-ttu-id="5af5c-114">Anger namnet på data Lake Store-kontot.</span><span class="sxs-lookup"><span data-stu-id="5af5c-114">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="5af5c-115">-ConcurrentFileCount</span><span class="sxs-lookup"><span data-stu-id="5af5c-115">-ConcurrentFileCount</span></span>
<span data-ttu-id="5af5c-116">Anger det högsta antalet filer som laddas ned parallellt för en mapp nedladdning.</span><span class="sxs-lookup"><span data-stu-id="5af5c-116">Specifies the maximum number of files to download in parallel for a folder download.</span></span>
<span data-ttu-id="5af5c-117">Standardvärdet är fem (5).</span><span class="sxs-lookup"><span data-stu-id="5af5c-117">The default value is five (5).</span></span>

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

### <span data-ttu-id="5af5c-118">-Mål</span><span class="sxs-lookup"><span data-stu-id="5af5c-118">-Destination</span></span>
<span data-ttu-id="5af5c-119">Anger den lokala fil Sök vägen som filen ska hämtas till.</span><span class="sxs-lookup"><span data-stu-id="5af5c-119">Specifies the local file path to which to download the file.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5af5c-120">-DiagnosticLogLevel</span><span class="sxs-lookup"><span data-stu-id="5af5c-120">-DiagnosticLogLevel</span></span>
<span data-ttu-id="5af5c-121">Anger om den diagnostiska loggnings nivå som ska användas för att registrera händelser under fil-eller mapp-importen.</span><span class="sxs-lookup"><span data-stu-id="5af5c-121">Optionally indicates the diagnostic log level to use to record events during the file or folder import.</span></span> <span data-ttu-id="5af5c-122">Standard är ett fel.</span><span class="sxs-lookup"><span data-stu-id="5af5c-122">Default is Error.</span></span>

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

### <span data-ttu-id="5af5c-123">-DiagnosticLogPath</span><span class="sxs-lookup"><span data-stu-id="5af5c-123">-DiagnosticLogPath</span></span>
<span data-ttu-id="5af5c-124">Anger sökvägen till Diagnostikrapporten för att spela in händelser för fil-eller mapp.</span><span class="sxs-lookup"><span data-stu-id="5af5c-124">Specifies the path for the diagnostic log to record events to during the file or folder import.</span></span>

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

### <span data-ttu-id="5af5c-125">-Force</span><span class="sxs-lookup"><span data-stu-id="5af5c-125">-Force</span></span>
<span data-ttu-id="5af5c-126">Anger att den här åtgärden kan skriva över målfilen om den redan finns.</span><span class="sxs-lookup"><span data-stu-id="5af5c-126">Indicates that this operation can overwrite the destination file if it already exists.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5af5c-127">-Path</span><span class="sxs-lookup"><span data-stu-id="5af5c-127">-Path</span></span>
<span data-ttu-id="5af5c-128">Anger sökvägen för det objekt som ska hämtas från data Lake Store från rot katalogen (/).</span><span class="sxs-lookup"><span data-stu-id="5af5c-128">Specifies the path of the item to download from the Data Lake Store, starting from the root directory (/).</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5af5c-129">-PerFileThreadCount</span><span class="sxs-lookup"><span data-stu-id="5af5c-129">-PerFileThreadCount</span></span>
<span data-ttu-id="5af5c-130">Anger maximalt antal trådar som ska användas per fil.</span><span class="sxs-lookup"><span data-stu-id="5af5c-130">Specifies the maximum number of threads to use per file.</span></span>
<span data-ttu-id="5af5c-131">Standardvärdet är tio (10).</span><span class="sxs-lookup"><span data-stu-id="5af5c-131">The default value is ten (10).</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5af5c-132">-Recurse</span><span class="sxs-lookup"><span data-stu-id="5af5c-132">-Recurse</span></span>
<span data-ttu-id="5af5c-133">Anger att en mapp som laddas ned är rekursiv.</span><span class="sxs-lookup"><span data-stu-id="5af5c-133">Indicates that a folder download is recursive.</span></span>

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

### <span data-ttu-id="5af5c-134">-Fortsätt</span><span class="sxs-lookup"><span data-stu-id="5af5c-134">-Resume</span></span>
<span data-ttu-id="5af5c-135">Anger att filen eller filerna som kopieras är en fortsättning på en tidigare nedladdning.</span><span class="sxs-lookup"><span data-stu-id="5af5c-135">Indicates that the file or files being copied are a continuation of a previous download.</span></span>
<span data-ttu-id="5af5c-136">Nedladdningen fortsätter från den senaste filen som inte laddats ned helt.</span><span class="sxs-lookup"><span data-stu-id="5af5c-136">The download attempts to resume from the last file that was not fully downloaded.</span></span>

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

### <span data-ttu-id="5af5c-137">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="5af5c-137">-Confirm</span></span>
<span data-ttu-id="5af5c-138">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="5af5c-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5af5c-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5af5c-139">-WhatIf</span></span>
<span data-ttu-id="5af5c-140">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="5af5c-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5af5c-141">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="5af5c-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5af5c-142">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5af5c-142">-DefaultProfile</span></span>
<span data-ttu-id="5af5c-143">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="5af5c-143">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5af5c-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5af5c-144">CommonParameters</span></span>
<span data-ttu-id="5af5c-145">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5af5c-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5af5c-146">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5af5c-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5af5c-147">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5af5c-147">INPUTS</span></span>

## <span data-ttu-id="5af5c-148">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5af5c-148">OUTPUTS</span></span>

### <span data-ttu-id="5af5c-149">strängvärdet</span><span class="sxs-lookup"><span data-stu-id="5af5c-149">string</span></span>
<span data-ttu-id="5af5c-150">Sökvägen till filen eller mappen laddades ner till.</span><span class="sxs-lookup"><span data-stu-id="5af5c-150">The path where the file or folder was downloaded to.</span></span>

## <span data-ttu-id="5af5c-151">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5af5c-151">NOTES</span></span>

## <span data-ttu-id="5af5c-152">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5af5c-152">RELATED LINKS</span></span>

[<span data-ttu-id="5af5c-153">Get-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="5af5c-153">Get-AzureRmDataLakeStoreItem</span></span>](./Get-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="5af5c-154">Import-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="5af5c-154">Import-AzureRmDataLakeStoreItem</span></span>](./Import-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="5af5c-155">Anslut-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="5af5c-155">Join-AzureRmDataLakeStoreItem</span></span>](./Join-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="5af5c-156">Move-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="5af5c-156">Move-AzureRmDataLakeStoreItem</span></span>](./Move-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="5af5c-157">New-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="5af5c-157">New-AzureRmDataLakeStoreItem</span></span>](./New-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="5af5c-158">Remove-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="5af5c-158">Remove-AzureRmDataLakeStoreItem</span></span>](./Remove-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="5af5c-159">Test-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="5af5c-159">Test-AzureRmDataLakeStoreItem</span></span>](./Test-AzureRmDataLakeStoreItem.md)


