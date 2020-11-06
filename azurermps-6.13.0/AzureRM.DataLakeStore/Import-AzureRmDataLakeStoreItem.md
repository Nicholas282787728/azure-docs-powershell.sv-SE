---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 90630395-8747-4446-A879-323274811956
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/import-azurermdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Import-AzureRmDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Import-AzureRmDataLakeStoreItem.md
ms.openlocfilehash: 91e7969600f387a95f46cad02f87cf6466f2c642
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575219"
---
# <span data-ttu-id="7134e-101">Import-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="7134e-101">Import-AzureRmDataLakeStoreItem</span></span>

## <span data-ttu-id="7134e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7134e-102">SYNOPSIS</span></span>
<span data-ttu-id="7134e-103">Laddar upp en lokal fil eller katalog till en data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="7134e-103">Uploads a local file or directory to a Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7134e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7134e-104">SYNTAX</span></span>

### <span data-ttu-id="7134e-105">NoDiagnosticLogging (standard)</span><span class="sxs-lookup"><span data-stu-id="7134e-105">NoDiagnosticLogging (Default)</span></span>
```
Import-AzureRmDataLakeStoreItem [-Account] <String> [-Path] <String> [-Destination] <DataLakeStorePathInstance>
 [-Recurse] [-Resume] [-ForceBinary] [-Force] [-Concurrency <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7134e-106">IncludeDiagnosticLogging</span><span class="sxs-lookup"><span data-stu-id="7134e-106">IncludeDiagnosticLogging</span></span>
```
Import-AzureRmDataLakeStoreItem [-Account] <String> [-Path] <String> [-Destination] <DataLakeStorePathInstance>
 [-Recurse] [-Resume] [-ForceBinary] [-Force] [-Concurrency <Int32>] [-DiagnosticLogLevel <LogLevel>]
 -DiagnosticLogPath <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7134e-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7134e-107">DESCRIPTION</span></span>
<span data-ttu-id="7134e-108">Cmdleten **import-AzureRmDataLakeStoreItem** laddar upp en lokal fil eller katalog till en data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="7134e-108">The **Import-AzureRmDataLakeStoreItem** cmdlet uploads a local file or directory to a Data Lake Store.</span></span>

## <span data-ttu-id="7134e-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7134e-109">EXAMPLES</span></span>

### <span data-ttu-id="7134e-110">Exempel 1: Ladda upp en fil</span><span class="sxs-lookup"><span data-stu-id="7134e-110">Example 1: Upload a file</span></span>
```
PS C:\>Import-AzureRmDataLakeStoreItem -AccountName "ContosoADL" -Path "C:\SrcFile.csv" -Destination "/MyFiles/File.csv" -Concurrency 4
```

<span data-ttu-id="7134e-111">Det här kommandot laddar upp filen SrcFile.csv och lägger till den i mappen Mina filer i data Lake Store som File.csv med en concurrency på 4.</span><span class="sxs-lookup"><span data-stu-id="7134e-111">This command uploads the file SrcFile.csv and adds it to the MyFiles folder in the Data Lake Store as File.csv with a concurrency of 4.</span></span>

## <span data-ttu-id="7134e-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7134e-112">PARAMETERS</span></span>

### <span data-ttu-id="7134e-113">-Konto</span><span class="sxs-lookup"><span data-stu-id="7134e-113">-Account</span></span>
<span data-ttu-id="7134e-114">Anger namnet på data Lake Store-kontot.</span><span class="sxs-lookup"><span data-stu-id="7134e-114">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="7134e-115">-Concurrency</span><span class="sxs-lookup"><span data-stu-id="7134e-115">-Concurrency</span></span>
<span data-ttu-id="7134e-116">Anger antalet filer eller delar som ska överföras parallellt.</span><span class="sxs-lookup"><span data-stu-id="7134e-116">Indicates the number of files or chunks to upload in parallel.</span></span> <span data-ttu-id="7134e-117">Standard beräknas som en bästa ansträngning baserat på Systemspecifikationer.</span><span class="sxs-lookup"><span data-stu-id="7134e-117">Default will be computed as a best effort based on system specifications.</span></span>

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

### <span data-ttu-id="7134e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7134e-118">-DefaultProfile</span></span>
<span data-ttu-id="7134e-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="7134e-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7134e-120">-Mål</span><span class="sxs-lookup"><span data-stu-id="7134e-120">-Destination</span></span>
<span data-ttu-id="7134e-121">Anger sökvägen till data Lake Store dit du vill ladda upp en fil eller mapp från rot katalogen (/).</span><span class="sxs-lookup"><span data-stu-id="7134e-121">Specifies the Data Lake Store path to which to upload a file or folder, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="7134e-122">-DiagnosticLogLevel</span><span class="sxs-lookup"><span data-stu-id="7134e-122">-DiagnosticLogLevel</span></span>
<span data-ttu-id="7134e-123">Anger om den diagnostiska loggnings nivå som ska användas för att registrera händelser under fil-eller mapp-importen.</span><span class="sxs-lookup"><span data-stu-id="7134e-123">Optionally indicates the diagnostic log level to use to record events during the file or folder import.</span></span> <span data-ttu-id="7134e-124">Standard är ett fel.</span><span class="sxs-lookup"><span data-stu-id="7134e-124">Default is Error.</span></span>

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

### <span data-ttu-id="7134e-125">-DiagnosticLogPath</span><span class="sxs-lookup"><span data-stu-id="7134e-125">-DiagnosticLogPath</span></span>
<span data-ttu-id="7134e-126">Anger sökvägen till Diagnostikrapporten för att spela in händelser för fil-eller mapp.</span><span class="sxs-lookup"><span data-stu-id="7134e-126">Specifies the path for the diagnostic log to record events to during the file or folder import.</span></span>

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

### <span data-ttu-id="7134e-127">-Force</span><span class="sxs-lookup"><span data-stu-id="7134e-127">-Force</span></span>
<span data-ttu-id="7134e-128">Anger att den här åtgärden kan skriva över målfilen om den redan finns.</span><span class="sxs-lookup"><span data-stu-id="7134e-128">Indicates that this operation can overwrite the destination file if it already exists.</span></span>

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

### <span data-ttu-id="7134e-129">-ForceBinary</span><span class="sxs-lookup"><span data-stu-id="7134e-129">-ForceBinary</span></span>
<span data-ttu-id="7134e-130">Anger att filen/filerna som kopieras ska kopieras utan att den nya raden bevaras i tillägg.</span><span class="sxs-lookup"><span data-stu-id="7134e-130">Indicates that the file(s) being copied should be copied with no concern for new line preservation across appends.</span></span>

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

### <span data-ttu-id="7134e-131">-Path</span><span class="sxs-lookup"><span data-stu-id="7134e-131">-Path</span></span>
<span data-ttu-id="7134e-132">Anger den lokala sökvägen till filen eller mappen som ska laddas upp.</span><span class="sxs-lookup"><span data-stu-id="7134e-132">Specifies the local path of the file or folder to upload.</span></span>

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

### <span data-ttu-id="7134e-133">-Recurse</span><span class="sxs-lookup"><span data-stu-id="7134e-133">-Recurse</span></span>
<span data-ttu-id="7134e-134">Anger att den här åtgärden ska ladda upp alla objekt i alla undermappar.</span><span class="sxs-lookup"><span data-stu-id="7134e-134">Indicates that this operation should upload all items in all subfolders.</span></span>

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

### <span data-ttu-id="7134e-135">-Fortsätt</span><span class="sxs-lookup"><span data-stu-id="7134e-135">-Resume</span></span>
<span data-ttu-id="7134e-136">Anger att filen/filerna som kopieras är en fortsättning på en tidigare uppladdning.</span><span class="sxs-lookup"><span data-stu-id="7134e-136">Indicates that the file(s) being copied are a continuation of a previous upload.</span></span> <span data-ttu-id="7134e-137">Detta kommer att göra att systemet försöker återuppta från den senaste filen som inte hade laddats upp helt.</span><span class="sxs-lookup"><span data-stu-id="7134e-137">This will cause the system to attempt to resume from the last file that was not fully uploaded.</span></span>

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

### <span data-ttu-id="7134e-138">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="7134e-138">-Confirm</span></span>
<span data-ttu-id="7134e-139">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="7134e-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7134e-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7134e-140">-WhatIf</span></span>
<span data-ttu-id="7134e-141">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="7134e-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7134e-142">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="7134e-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7134e-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7134e-143">CommonParameters</span></span>
<span data-ttu-id="7134e-144">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7134e-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7134e-145">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7134e-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7134e-146">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7134e-146">INPUTS</span></span>

### <span data-ttu-id="7134e-147">System. String</span><span class="sxs-lookup"><span data-stu-id="7134e-147">System.String</span></span>

### <span data-ttu-id="7134e-148">Microsoft. Azure. commands. DataLakeStore. Models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="7134e-148">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="7134e-149">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="7134e-149">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="7134e-150">System. Int32</span><span class="sxs-lookup"><span data-stu-id="7134e-150">System.Int32</span></span>

### <span data-ttu-id="7134e-151">Microsoft. Azure. commands. DataLakeStore. Models. LogLevel</span><span class="sxs-lookup"><span data-stu-id="7134e-151">Microsoft.Azure.Commands.DataLakeStore.Models.LogLevel</span></span>

## <span data-ttu-id="7134e-152">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7134e-152">OUTPUTS</span></span>

### <span data-ttu-id="7134e-153">System. String</span><span class="sxs-lookup"><span data-stu-id="7134e-153">System.String</span></span>
<span data-ttu-id="7134e-154">Den fullständiga sökvägen till den uppladdade filen eller mappen.</span><span class="sxs-lookup"><span data-stu-id="7134e-154">The full path in the Data Lake Store account to the uploaded file or folder.</span></span>

## <span data-ttu-id="7134e-155">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7134e-155">NOTES</span></span>

## <span data-ttu-id="7134e-156">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7134e-156">RELATED LINKS</span></span>

[<span data-ttu-id="7134e-157">Get-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="7134e-157">Get-AzureRmDataLakeStoreItem</span></span>](./Get-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="7134e-158">Exportera-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="7134e-158">Export-AzureRmDataLakeStoreItem</span></span>](./Export-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="7134e-159">Anslut-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="7134e-159">Join-AzureRmDataLakeStoreItem</span></span>](./Join-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="7134e-160">Move-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="7134e-160">Move-AzureRmDataLakeStoreItem</span></span>](./Move-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="7134e-161">New-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="7134e-161">New-AzureRmDataLakeStoreItem</span></span>](./New-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="7134e-162">Remove-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="7134e-162">Remove-AzureRmDataLakeStoreItem</span></span>](./Remove-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="7134e-163">Test-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="7134e-163">Test-AzureRmDataLakeStoreItem</span></span>](./Test-AzureRmDataLakeStoreItem.md)


