---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 15DFF66F-3D78-422B-BA40-71058DE66BA2
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/get-azdatalakestoreitemcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreItemContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreItemContent.md
ms.openlocfilehash: 857f91cd8847e97dadf90c063ffc7b0e0366dab9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93916882"
---
# <span data-ttu-id="24084-101">Get-AzDataLakeStoreItemContent</span><span class="sxs-lookup"><span data-stu-id="24084-101">Get-AzDataLakeStoreItemContent</span></span>

## <span data-ttu-id="24084-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="24084-102">SYNOPSIS</span></span>
<span data-ttu-id="24084-103">Hämtar innehållet i en fil i data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="24084-103">Gets the contents of a file in Data Lake Store.</span></span>

## <span data-ttu-id="24084-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="24084-104">SYNTAX</span></span>

### <span data-ttu-id="24084-105">PreviewFileContent (standard)</span><span class="sxs-lookup"><span data-stu-id="24084-105">PreviewFileContent (Default)</span></span>
```
Get-AzDataLakeStoreItemContent [-Account] <String> [-Path] <DataLakeStorePathInstance> [[-Offset] <Int64>]
 [[-Length] <Int64>] [[-Encoding] <Encoding>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="24084-106">PreviewFileRowsFromHead</span><span class="sxs-lookup"><span data-stu-id="24084-106">PreviewFileRowsFromHead</span></span>
```
Get-AzDataLakeStoreItemContent [-Account] <String> [-Path] <DataLakeStorePathInstance> [[-Head] <Int32>]
 [[-Encoding] <Encoding>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="24084-107">PreviewFileRowsFromTail</span><span class="sxs-lookup"><span data-stu-id="24084-107">PreviewFileRowsFromTail</span></span>
```
Get-AzDataLakeStoreItemContent [-Account] <String> [-Path] <DataLakeStorePathInstance> [[-Tail] <Int32>]
 [[-Encoding] <Encoding>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="24084-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="24084-108">DESCRIPTION</span></span>
<span data-ttu-id="24084-109">Cmdleten **Get-AzDataLakeStoreItemContent** hämtar innehållet i en fil i data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="24084-109">The **Get-AzDataLakeStoreItemContent** cmdlet gets the contents of a file in Data Lake Store.</span></span>

## <span data-ttu-id="24084-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="24084-110">EXAMPLES</span></span>

### <span data-ttu-id="24084-111">Exempel 1: hämta innehållet i en fil</span><span class="sxs-lookup"><span data-stu-id="24084-111">Example 1: Get the contents of a file</span></span>
```
PS C:\>Get-AzDataLakeStoreItemContent -AccountName "ContosoADL" -Path "/MyFile.txt"
```

<span data-ttu-id="24084-112">Det här kommandot får innehållet i filen MyFile.txt i ContosoADL-kontot.</span><span class="sxs-lookup"><span data-stu-id="24084-112">This command gets the contents of the file MyFile.txt in the ContosoADL account.</span></span>

### <span data-ttu-id="24084-113">Exempel 2: Hämta de två första raderna i en fil</span><span class="sxs-lookup"><span data-stu-id="24084-113">Example 2: Get the first two rows of a file</span></span>
```
PS C:\>Get-AzDataLakeStoreItemContent -AccountName "ContosoADL" -Path "/MyFile.txt" -Head 2
```

<span data-ttu-id="24084-114">Det här kommandot får de första två nya raderna avgränsade rader i filen MyFile.txt i ContosoADL-kontot.</span><span class="sxs-lookup"><span data-stu-id="24084-114">This command gets the first two new line separated rows in the file MyFile.txt in the ContosoADL account.</span></span>

## <span data-ttu-id="24084-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="24084-115">PARAMETERS</span></span>

### <span data-ttu-id="24084-116">-Konto</span><span class="sxs-lookup"><span data-stu-id="24084-116">-Account</span></span>
<span data-ttu-id="24084-117">Anger namnet på data Lake Store-kontot.</span><span class="sxs-lookup"><span data-stu-id="24084-117">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="24084-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24084-118">-DefaultProfile</span></span>
<span data-ttu-id="24084-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="24084-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="24084-120">-Kodning</span><span class="sxs-lookup"><span data-stu-id="24084-120">-Encoding</span></span>
<span data-ttu-id="24084-121">Anger kodningen för det objekt som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="24084-121">Specifies the encoding for the item to create.</span></span>
<span data-ttu-id="24084-122">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="24084-122">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="24084-123">Känd</span><span class="sxs-lookup"><span data-stu-id="24084-123">Unknown</span></span>
- <span data-ttu-id="24084-124">Strängvärdet</span><span class="sxs-lookup"><span data-stu-id="24084-124">String</span></span>
- <span data-ttu-id="24084-125">Unicode</span><span class="sxs-lookup"><span data-stu-id="24084-125">Unicode</span></span>
- <span data-ttu-id="24084-126">SBCS</span><span class="sxs-lookup"><span data-stu-id="24084-126">Byte</span></span>
- <span data-ttu-id="24084-127">BigEndianUnicode</span><span class="sxs-lookup"><span data-stu-id="24084-127">BigEndianUnicode</span></span>
- <span data-ttu-id="24084-128">SKICKADE</span><span class="sxs-lookup"><span data-stu-id="24084-128">UTF8</span></span>
- <span data-ttu-id="24084-129">UTF7</span><span class="sxs-lookup"><span data-stu-id="24084-129">UTF7</span></span>
- <span data-ttu-id="24084-130">Teckenuppsättning</span><span class="sxs-lookup"><span data-stu-id="24084-130">Ascii</span></span>
- <span data-ttu-id="24084-131">Vis</span><span class="sxs-lookup"><span data-stu-id="24084-131">Default</span></span>
- <span data-ttu-id="24084-132">Koms</span><span class="sxs-lookup"><span data-stu-id="24084-132">Oem</span></span>
- <span data-ttu-id="24084-133">BigEndianUTF32</span><span class="sxs-lookup"><span data-stu-id="24084-133">BigEndianUTF32</span></span>

```yaml
Type: System.Text.Encoding
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="24084-134">-Force</span><span class="sxs-lookup"><span data-stu-id="24084-134">-Force</span></span>
<span data-ttu-id="24084-135">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="24084-135">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: PreviewFileContent
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="24084-136">-Head</span><span class="sxs-lookup"><span data-stu-id="24084-136">-Head</span></span>
<span data-ttu-id="24084-137">Antalet rader (ny rad avgränsat) från början av filen som ska förhandsgranskas.</span><span class="sxs-lookup"><span data-stu-id="24084-137">The number of rows (new line delimited) from the beginning of the file to preview.</span></span> <span data-ttu-id="24084-138">Om ingen ny rad påträffas i det första 4 MB data returneras endast dessa data.</span><span class="sxs-lookup"><span data-stu-id="24084-138">If no new line is encountered in the first 4mb of data, only that data will be returned.</span></span>

```yaml
Type: System.Int32
Parameter Sets: PreviewFileRowsFromHead
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="24084-139">-Längd</span><span class="sxs-lookup"><span data-stu-id="24084-139">-Length</span></span>
<span data-ttu-id="24084-140">Anger längden i byte för innehållet som ska visas.</span><span class="sxs-lookup"><span data-stu-id="24084-140">Specifies the length, in bytes, of the content to get.</span></span>

```yaml
Type: System.Int64
Parameter Sets: PreviewFileContent
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="24084-141">-Offset</span><span class="sxs-lookup"><span data-stu-id="24084-141">-Offset</span></span>
<span data-ttu-id="24084-142">Anger antalet byte som ska hoppas över i en fil innan innehåll får plats.</span><span class="sxs-lookup"><span data-stu-id="24084-142">Specifies the number of bytes to skip in a file before getting content.</span></span>

```yaml
Type: System.Int64
Parameter Sets: PreviewFileContent
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="24084-143">-Path</span><span class="sxs-lookup"><span data-stu-id="24084-143">-Path</span></span>
<span data-ttu-id="24084-144">Anger data Lake Store-sökvägen för en fil, från rot katalogen (/).</span><span class="sxs-lookup"><span data-stu-id="24084-144">Specifies the Data Lake Store path of a file, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="24084-145">-Pilslut</span><span class="sxs-lookup"><span data-stu-id="24084-145">-Tail</span></span>
<span data-ttu-id="24084-146">Antalet rader (ny rad avgränsat) från slutet av filen för förhands granskning.</span><span class="sxs-lookup"><span data-stu-id="24084-146">The number of rows (new line delimited) from the end of the file to preview.</span></span> <span data-ttu-id="24084-147">Om ingen ny rad påträffas i det första 4 MB data returneras endast dessa data.</span><span class="sxs-lookup"><span data-stu-id="24084-147">If no new line is encountered in the first 4mb of data, only that data will be returned.</span></span>

```yaml
Type: System.Int32
Parameter Sets: PreviewFileRowsFromTail
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="24084-148">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="24084-148">-Confirm</span></span>
<span data-ttu-id="24084-149">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="24084-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="24084-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="24084-150">-WhatIf</span></span>
<span data-ttu-id="24084-151">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="24084-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="24084-152">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="24084-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="24084-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24084-153">CommonParameters</span></span>
<span data-ttu-id="24084-154">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="24084-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24084-155">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="24084-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24084-156">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="24084-156">INPUTS</span></span>

### <span data-ttu-id="24084-157">System. String</span><span class="sxs-lookup"><span data-stu-id="24084-157">System.String</span></span>

### <span data-ttu-id="24084-158">Microsoft. Azure. commands. DataLakeStore. Models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="24084-158">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="24084-159">System. Int32</span><span class="sxs-lookup"><span data-stu-id="24084-159">System.Int32</span></span>

### <span data-ttu-id="24084-160">System. Int64</span><span class="sxs-lookup"><span data-stu-id="24084-160">System.Int64</span></span>

### <span data-ttu-id="24084-161">System. text. Encoding</span><span class="sxs-lookup"><span data-stu-id="24084-161">System.Text.Encoding</span></span>

### <span data-ttu-id="24084-162">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="24084-162">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="24084-163">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="24084-163">OUTPUTS</span></span>

### <span data-ttu-id="24084-164">System. byte</span><span class="sxs-lookup"><span data-stu-id="24084-164">System.Byte</span></span>

### <span data-ttu-id="24084-165">System. String</span><span class="sxs-lookup"><span data-stu-id="24084-165">System.String</span></span>

## <span data-ttu-id="24084-166">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="24084-166">NOTES</span></span>

## <span data-ttu-id="24084-167">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="24084-167">RELATED LINKS</span></span>
