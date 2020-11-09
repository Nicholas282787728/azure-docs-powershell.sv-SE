---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: B10B1F5D-5566-4129-9D42-05A6D3B72C9E
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/export-azdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Export-AzDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Export-AzDataLakeStoreItem.md
ms.openlocfilehash: e0bac2f22249b27442c75da7879f6a6cf85e7da7
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94320603"
---
# <span data-ttu-id="9ff83-101">Export-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="9ff83-101">Export-AzDataLakeStoreItem</span></span>

## <span data-ttu-id="9ff83-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9ff83-102">SYNOPSIS</span></span>
<span data-ttu-id="9ff83-103">Laddar ned en fil från data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="9ff83-103">Downloads a file from Data Lake Store.</span></span>

## <span data-ttu-id="9ff83-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9ff83-104">SYNTAX</span></span>

### <span data-ttu-id="9ff83-105">NoDiagnosticLogging (standard)</span><span class="sxs-lookup"><span data-stu-id="9ff83-105">NoDiagnosticLogging (Default)</span></span>
```
Export-AzDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Destination] <String>
 [-Recurse] [-Resume] [-Force] [-Concurrency <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9ff83-106">IncludeDiagnosticLogging</span><span class="sxs-lookup"><span data-stu-id="9ff83-106">IncludeDiagnosticLogging</span></span>
```
Export-AzDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Destination] <String>
 [-Recurse] [-Resume] [-Force] [-Concurrency <Int32>] [-DiagnosticLogLevel <LogLevel>]
 -DiagnosticLogPath <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9ff83-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9ff83-107">DESCRIPTION</span></span>
<span data-ttu-id="9ff83-108">Cmdleten **export-AzDataLakeStoreItem** laddar ned en fil från data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="9ff83-108">The **Export-AzDataLakeStoreItem** cmdlet downloads a file from Data Lake Store.</span></span>

## <span data-ttu-id="9ff83-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9ff83-109">EXAMPLES</span></span>

### <span data-ttu-id="9ff83-110">Exempel 1: Hämta ett objekt från data Lake Store</span><span class="sxs-lookup"><span data-stu-id="9ff83-110">Example 1: Download an item from the Data Lake Store</span></span>
```
PS C:\>Export-AzDataLakeStoreItem -AccountName "ContosoADL" -Path /myFiles/TestSource.csv -Destination "C:\Test.csv" -Concurrency 4
```

<span data-ttu-id="9ff83-111">Det här kommandot laddar ned filen TestSource.csv från data Lake Store till C:\Test.csv med en concurrency på 4.</span><span class="sxs-lookup"><span data-stu-id="9ff83-111">This command downloads the file TestSource.csv from the Data Lake Store to C:\Test.csv with a concurrency of 4.</span></span>

## <span data-ttu-id="9ff83-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9ff83-112">PARAMETERS</span></span>

### <span data-ttu-id="9ff83-113">-Konto</span><span class="sxs-lookup"><span data-stu-id="9ff83-113">-Account</span></span>
<span data-ttu-id="9ff83-114">Anger namnet på data Lake Store-kontot.</span><span class="sxs-lookup"><span data-stu-id="9ff83-114">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="9ff83-115">-Concurrency</span><span class="sxs-lookup"><span data-stu-id="9ff83-115">-Concurrency</span></span>
<span data-ttu-id="9ff83-116">Anger hur många filer eller delar som ska laddas ned parallellt.</span><span class="sxs-lookup"><span data-stu-id="9ff83-116">Indicates the number of files or chunks to download in parallel.</span></span> <span data-ttu-id="9ff83-117">Standard beräknas som en bästa ansträngning baserat på Systemspecifikationer.</span><span class="sxs-lookup"><span data-stu-id="9ff83-117">Default will be computed as a best effort based on system specifications.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9ff83-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ff83-118">-DefaultProfile</span></span>
<span data-ttu-id="9ff83-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="9ff83-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ff83-120">-Mål</span><span class="sxs-lookup"><span data-stu-id="9ff83-120">-Destination</span></span>
<span data-ttu-id="9ff83-121">Anger den lokala fil Sök vägen som filen ska hämtas till.</span><span class="sxs-lookup"><span data-stu-id="9ff83-121">Specifies the local file path to which to download the file.</span></span>

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

### <span data-ttu-id="9ff83-122">-DiagnosticLogLevel</span><span class="sxs-lookup"><span data-stu-id="9ff83-122">-DiagnosticLogLevel</span></span>
<span data-ttu-id="9ff83-123">Anger om den diagnostiska loggnings nivå som ska användas för att registrera händelser under fil-eller mapp-importen.</span><span class="sxs-lookup"><span data-stu-id="9ff83-123">Optionally indicates the diagnostic log level to use to record events during the file or folder import.</span></span> <span data-ttu-id="9ff83-124">Standard är ett fel.</span><span class="sxs-lookup"><span data-stu-id="9ff83-124">Default is Error.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.LogLevel
Parameter Sets: IncludeDiagnosticLogging
Aliases:
Accepted values: Debug, Information, Error, None

Required: False
Position: Named
Default value: Error
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9ff83-125">-DiagnosticLogPath</span><span class="sxs-lookup"><span data-stu-id="9ff83-125">-DiagnosticLogPath</span></span>
<span data-ttu-id="9ff83-126">Anger sökvägen till Diagnostikrapporten för att spela in händelser för fil-eller mapp.</span><span class="sxs-lookup"><span data-stu-id="9ff83-126">Specifies the path for the diagnostic log to record events to during the file or folder import.</span></span>

```yaml
Type: System.String
Parameter Sets: IncludeDiagnosticLogging
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9ff83-127">-Force</span><span class="sxs-lookup"><span data-stu-id="9ff83-127">-Force</span></span>
<span data-ttu-id="9ff83-128">Anger att den här åtgärden kan skriva över målfilen om den redan finns.</span><span class="sxs-lookup"><span data-stu-id="9ff83-128">Indicates that this operation can overwrite the destination file if it already exists.</span></span>

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

### <span data-ttu-id="9ff83-129">-Path</span><span class="sxs-lookup"><span data-stu-id="9ff83-129">-Path</span></span>
<span data-ttu-id="9ff83-130">Anger sökvägen för det objekt som ska hämtas från data Lake Store från rot katalogen (/).</span><span class="sxs-lookup"><span data-stu-id="9ff83-130">Specifies the path of the item to download from the Data Lake Store, starting from the root directory (/).</span></span>

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

### <span data-ttu-id="9ff83-131">-Recurse</span><span class="sxs-lookup"><span data-stu-id="9ff83-131">-Recurse</span></span>
<span data-ttu-id="9ff83-132">Anger att en mapp som laddas ned är rekursiv.</span><span class="sxs-lookup"><span data-stu-id="9ff83-132">Indicates that a folder download is recursive.</span></span>

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

### <span data-ttu-id="9ff83-133">-Fortsätt</span><span class="sxs-lookup"><span data-stu-id="9ff83-133">-Resume</span></span>
<span data-ttu-id="9ff83-134">Anger att filen/filerna som kopieras är en fortsättning på en tidigare nedladdning.</span><span class="sxs-lookup"><span data-stu-id="9ff83-134">Indicates that the file(s) being copied are a continuation of a previous download.</span></span>
<span data-ttu-id="9ff83-135">Detta gör att systemet försöker återuppta från den senaste filen som inte laddats ned helt.</span><span class="sxs-lookup"><span data-stu-id="9ff83-135">This will cause the system to attempt to resume from the last file that was not fully downloaded.</span></span>

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

### <span data-ttu-id="9ff83-136">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="9ff83-136">-Confirm</span></span>
<span data-ttu-id="9ff83-137">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="9ff83-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9ff83-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9ff83-138">-WhatIf</span></span>
<span data-ttu-id="9ff83-139">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="9ff83-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9ff83-140">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="9ff83-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9ff83-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ff83-141">CommonParameters</span></span>
<span data-ttu-id="9ff83-142">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9ff83-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ff83-143">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9ff83-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ff83-144">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9ff83-144">INPUTS</span></span>

### <span data-ttu-id="9ff83-145">System. String</span><span class="sxs-lookup"><span data-stu-id="9ff83-145">System.String</span></span>

### <span data-ttu-id="9ff83-146">Microsoft. Azure. commands. DataLakeStore. Models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="9ff83-146">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="9ff83-147">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="9ff83-147">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="9ff83-148">System. Int32</span><span class="sxs-lookup"><span data-stu-id="9ff83-148">System.Int32</span></span>

### <span data-ttu-id="9ff83-149">Microsoft. Azure. commands. DataLakeStore. Models. LogLevel</span><span class="sxs-lookup"><span data-stu-id="9ff83-149">Microsoft.Azure.Commands.DataLakeStore.Models.LogLevel</span></span>

## <span data-ttu-id="9ff83-150">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9ff83-150">OUTPUTS</span></span>

### <span data-ttu-id="9ff83-151">System. String</span><span class="sxs-lookup"><span data-stu-id="9ff83-151">System.String</span></span>

## <span data-ttu-id="9ff83-152">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9ff83-152">NOTES</span></span>

## <span data-ttu-id="9ff83-153">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9ff83-153">RELATED LINKS</span></span>

[<span data-ttu-id="9ff83-154">Get-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="9ff83-154">Get-AzDataLakeStoreItem</span></span>](./Get-AzDataLakeStoreItem.md)

[<span data-ttu-id="9ff83-155">Import-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="9ff83-155">Import-AzDataLakeStoreItem</span></span>](./Import-AzDataLakeStoreItem.md)

[<span data-ttu-id="9ff83-156">Anslut-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="9ff83-156">Join-AzDataLakeStoreItem</span></span>](./Join-AzDataLakeStoreItem.md)

[<span data-ttu-id="9ff83-157">Move-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="9ff83-157">Move-AzDataLakeStoreItem</span></span>](./Move-AzDataLakeStoreItem.md)

[<span data-ttu-id="9ff83-158">New-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="9ff83-158">New-AzDataLakeStoreItem</span></span>](./New-AzDataLakeStoreItem.md)

[<span data-ttu-id="9ff83-159">Remove-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="9ff83-159">Remove-AzDataLakeStoreItem</span></span>](./Remove-AzDataLakeStoreItem.md)

[<span data-ttu-id="9ff83-160">Test-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="9ff83-160">Test-AzDataLakeStoreItem</span></span>](./Test-AzDataLakeStoreItem.md)


