---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 90630395-8747-4446-A879-323274811956
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/import-azdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Import-AzDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Import-AzDataLakeStoreItem.md
ms.openlocfilehash: c3ccb538446e7cb179e15f3af17d0cde03c4ab44
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93916873"
---
# <span data-ttu-id="460b8-101">Import-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="460b8-101">Import-AzDataLakeStoreItem</span></span>

## <span data-ttu-id="460b8-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="460b8-102">SYNOPSIS</span></span>
<span data-ttu-id="460b8-103">Laddar upp en lokal fil eller katalog till en data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="460b8-103">Uploads a local file or directory to a Data Lake Store.</span></span>

## <span data-ttu-id="460b8-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="460b8-104">SYNTAX</span></span>

### <span data-ttu-id="460b8-105">NoDiagnosticLogging (standard)</span><span class="sxs-lookup"><span data-stu-id="460b8-105">NoDiagnosticLogging (Default)</span></span>
```
Import-AzDataLakeStoreItem [-Account] <String> [-Path] <String> [-Destination] <DataLakeStorePathInstance>
 [-Recurse] [-Resume] [-ForceBinary] [-Force] [-Concurrency <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="460b8-106">IncludeDiagnosticLogging</span><span class="sxs-lookup"><span data-stu-id="460b8-106">IncludeDiagnosticLogging</span></span>
```
Import-AzDataLakeStoreItem [-Account] <String> [-Path] <String> [-Destination] <DataLakeStorePathInstance>
 [-Recurse] [-Resume] [-ForceBinary] [-Force] [-Concurrency <Int32>] [-DiagnosticLogLevel <LogLevel>]
 -DiagnosticLogPath <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="460b8-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="460b8-107">DESCRIPTION</span></span>
<span data-ttu-id="460b8-108">Cmdleten **import-AzDataLakeStoreItem** laddar upp en lokal fil eller katalog till en data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="460b8-108">The **Import-AzDataLakeStoreItem** cmdlet uploads a local file or directory to a Data Lake Store.</span></span>

## <span data-ttu-id="460b8-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="460b8-109">EXAMPLES</span></span>

### <span data-ttu-id="460b8-110">Exempel 1: Ladda upp en fil</span><span class="sxs-lookup"><span data-stu-id="460b8-110">Example 1: Upload a file</span></span>
```
PS C:\>Import-AzDataLakeStoreItem -AccountName "ContosoADL" -Path "C:\SrcFile.csv" -Destination "/MyFiles/File.csv" -Concurrency 4
```

<span data-ttu-id="460b8-111">Det här kommandot laddar upp filen SrcFile.csv och lägger till den i mappen Mina filer i data Lake Store som File.csv med en concurrency på 4.</span><span class="sxs-lookup"><span data-stu-id="460b8-111">This command uploads the file SrcFile.csv and adds it to the MyFiles folder in the Data Lake Store as File.csv with a concurrency of 4.</span></span>

## <span data-ttu-id="460b8-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="460b8-112">PARAMETERS</span></span>

### <span data-ttu-id="460b8-113">-Konto</span><span class="sxs-lookup"><span data-stu-id="460b8-113">-Account</span></span>
<span data-ttu-id="460b8-114">Anger namnet på data Lake Store-kontot.</span><span class="sxs-lookup"><span data-stu-id="460b8-114">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="460b8-115">-Concurrency</span><span class="sxs-lookup"><span data-stu-id="460b8-115">-Concurrency</span></span>
<span data-ttu-id="460b8-116">Anger antalet filer eller delar som ska överföras parallellt.</span><span class="sxs-lookup"><span data-stu-id="460b8-116">Indicates the number of files or chunks to upload in parallel.</span></span> <span data-ttu-id="460b8-117">Standard beräknas som en bästa ansträngning baserat på Systemspecifikationer.</span><span class="sxs-lookup"><span data-stu-id="460b8-117">Default will be computed as a best effort based on system specifications.</span></span>

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

### <span data-ttu-id="460b8-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="460b8-118">-DefaultProfile</span></span>
<span data-ttu-id="460b8-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="460b8-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="460b8-120">-Mål</span><span class="sxs-lookup"><span data-stu-id="460b8-120">-Destination</span></span>
<span data-ttu-id="460b8-121">Anger sökvägen till data Lake Store dit du vill ladda upp en fil eller mapp från rot katalogen (/).</span><span class="sxs-lookup"><span data-stu-id="460b8-121">Specifies the Data Lake Store path to which to upload a file or folder, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="460b8-122">-DiagnosticLogLevel</span><span class="sxs-lookup"><span data-stu-id="460b8-122">-DiagnosticLogLevel</span></span>
<span data-ttu-id="460b8-123">Anger om den diagnostiska loggnings nivå som ska användas för att registrera händelser under fil-eller mapp-importen.</span><span class="sxs-lookup"><span data-stu-id="460b8-123">Optionally indicates the diagnostic log level to use to record events during the file or folder import.</span></span> <span data-ttu-id="460b8-124">Standard är ett fel.</span><span class="sxs-lookup"><span data-stu-id="460b8-124">Default is Error.</span></span>

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

### <span data-ttu-id="460b8-125">-DiagnosticLogPath</span><span class="sxs-lookup"><span data-stu-id="460b8-125">-DiagnosticLogPath</span></span>
<span data-ttu-id="460b8-126">Anger sökvägen till Diagnostikrapporten för att spela in händelser för fil-eller mapp.</span><span class="sxs-lookup"><span data-stu-id="460b8-126">Specifies the path for the diagnostic log to record events to during the file or folder import.</span></span>

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

### <span data-ttu-id="460b8-127">-Force</span><span class="sxs-lookup"><span data-stu-id="460b8-127">-Force</span></span>
<span data-ttu-id="460b8-128">Anger att den här åtgärden kan skriva över målfilen om den redan finns.</span><span class="sxs-lookup"><span data-stu-id="460b8-128">Indicates that this operation can overwrite the destination file if it already exists.</span></span>

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

### <span data-ttu-id="460b8-129">-ForceBinary</span><span class="sxs-lookup"><span data-stu-id="460b8-129">-ForceBinary</span></span>
<span data-ttu-id="460b8-130">Anger att filen/filerna som kopieras ska kopieras utan att den nya raden bevaras i tillägg.</span><span class="sxs-lookup"><span data-stu-id="460b8-130">Indicates that the file(s) being copied should be copied with no concern for new line preservation across appends.</span></span>

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

### <span data-ttu-id="460b8-131">-Path</span><span class="sxs-lookup"><span data-stu-id="460b8-131">-Path</span></span>
<span data-ttu-id="460b8-132">Anger den lokala sökvägen till filen eller mappen som ska laddas upp.</span><span class="sxs-lookup"><span data-stu-id="460b8-132">Specifies the local path of the file or folder to upload.</span></span>

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

### <span data-ttu-id="460b8-133">-Recurse</span><span class="sxs-lookup"><span data-stu-id="460b8-133">-Recurse</span></span>
<span data-ttu-id="460b8-134">Anger att den här åtgärden ska ladda upp alla objekt i alla undermappar.</span><span class="sxs-lookup"><span data-stu-id="460b8-134">Indicates that this operation should upload all items in all subfolders.</span></span>

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

### <span data-ttu-id="460b8-135">-Fortsätt</span><span class="sxs-lookup"><span data-stu-id="460b8-135">-Resume</span></span>
<span data-ttu-id="460b8-136">Anger att filen/filerna som kopieras är en fortsättning på en tidigare uppladdning.</span><span class="sxs-lookup"><span data-stu-id="460b8-136">Indicates that the file(s) being copied are a continuation of a previous upload.</span></span> <span data-ttu-id="460b8-137">Detta kommer att göra att systemet försöker återuppta från den senaste filen som inte hade laddats upp helt.</span><span class="sxs-lookup"><span data-stu-id="460b8-137">This will cause the system to attempt to resume from the last file that was not fully uploaded.</span></span>

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

### <span data-ttu-id="460b8-138">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="460b8-138">-Confirm</span></span>
<span data-ttu-id="460b8-139">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="460b8-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="460b8-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="460b8-140">-WhatIf</span></span>
<span data-ttu-id="460b8-141">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="460b8-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="460b8-142">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="460b8-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="460b8-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="460b8-143">CommonParameters</span></span>
<span data-ttu-id="460b8-144">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="460b8-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="460b8-145">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="460b8-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="460b8-146">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="460b8-146">INPUTS</span></span>

### <span data-ttu-id="460b8-147">System. String</span><span class="sxs-lookup"><span data-stu-id="460b8-147">System.String</span></span>

### <span data-ttu-id="460b8-148">Microsoft. Azure. commands. DataLakeStore. Models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="460b8-148">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="460b8-149">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="460b8-149">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="460b8-150">System. Int32</span><span class="sxs-lookup"><span data-stu-id="460b8-150">System.Int32</span></span>

### <span data-ttu-id="460b8-151">Microsoft. Azure. commands. DataLakeStore. Models. LogLevel</span><span class="sxs-lookup"><span data-stu-id="460b8-151">Microsoft.Azure.Commands.DataLakeStore.Models.LogLevel</span></span>

## <span data-ttu-id="460b8-152">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="460b8-152">OUTPUTS</span></span>

### <span data-ttu-id="460b8-153">System. String</span><span class="sxs-lookup"><span data-stu-id="460b8-153">System.String</span></span>

## <span data-ttu-id="460b8-154">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="460b8-154">NOTES</span></span>

## <span data-ttu-id="460b8-155">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="460b8-155">RELATED LINKS</span></span>

[<span data-ttu-id="460b8-156">Get-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="460b8-156">Get-AzDataLakeStoreItem</span></span>](./Get-AzDataLakeStoreItem.md)

[<span data-ttu-id="460b8-157">Exportera-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="460b8-157">Export-AzDataLakeStoreItem</span></span>](./Export-AzDataLakeStoreItem.md)

[<span data-ttu-id="460b8-158">Anslut-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="460b8-158">Join-AzDataLakeStoreItem</span></span>](./Join-AzDataLakeStoreItem.md)

[<span data-ttu-id="460b8-159">Move-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="460b8-159">Move-AzDataLakeStoreItem</span></span>](./Move-AzDataLakeStoreItem.md)

[<span data-ttu-id="460b8-160">New-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="460b8-160">New-AzDataLakeStoreItem</span></span>](./New-AzDataLakeStoreItem.md)

[<span data-ttu-id="460b8-161">Remove-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="460b8-161">Remove-AzDataLakeStoreItem</span></span>](./Remove-AzDataLakeStoreItem.md)

[<span data-ttu-id="460b8-162">Test-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="460b8-162">Test-AzDataLakeStoreItem</span></span>](./Test-AzDataLakeStoreItem.md)


