---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 15DFF66F-3D78-422B-BA40-71058DE66BA2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/get-azurermdatalakestoreitemcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreItemContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreItemContent.md
ms.openlocfilehash: 28e314f5ac7306233c3e2a3619a1a332dd6f3314
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93755767"
---
# <span data-ttu-id="9e0bc-101">Get-AzureRmDataLakeStoreItemContent</span><span class="sxs-lookup"><span data-stu-id="9e0bc-101">Get-AzureRmDataLakeStoreItemContent</span></span>

## <span data-ttu-id="9e0bc-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9e0bc-102">SYNOPSIS</span></span>
<span data-ttu-id="9e0bc-103">Hämtar innehållet i en fil i data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="9e0bc-103">Gets the contents of a file in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9e0bc-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9e0bc-104">SYNTAX</span></span>

### <span data-ttu-id="9e0bc-105">PreviewFileContent (standard)</span><span class="sxs-lookup"><span data-stu-id="9e0bc-105">PreviewFileContent (Default)</span></span>
```
Get-AzureRmDataLakeStoreItemContent [-Account] <String> [-Path] <DataLakeStorePathInstance> [[-Offset] <Int64>]
 [[-Length] <Int64>] [[-Encoding] <FileSystemCmdletProviderEncoding>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9e0bc-106">PreviewFileRowsFromHead</span><span class="sxs-lookup"><span data-stu-id="9e0bc-106">PreviewFileRowsFromHead</span></span>
```
Get-AzureRmDataLakeStoreItemContent [-Account] <String> [-Path] <DataLakeStorePathInstance> [[-Head] <Int32>]
 [[-Encoding] <FileSystemCmdletProviderEncoding>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9e0bc-107">PreviewFileRowsFromTail</span><span class="sxs-lookup"><span data-stu-id="9e0bc-107">PreviewFileRowsFromTail</span></span>
```
Get-AzureRmDataLakeStoreItemContent [-Account] <String> [-Path] <DataLakeStorePathInstance> [[-Tail] <Int32>]
 [[-Encoding] <FileSystemCmdletProviderEncoding>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9e0bc-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9e0bc-108">DESCRIPTION</span></span>
<span data-ttu-id="9e0bc-109">Cmdleten **Get-AzureRmDataLakeStoreItemContent** hämtar innehållet i en fil i data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="9e0bc-109">The **Get-AzureRmDataLakeStoreItemContent** cmdlet gets the contents of a file in Data Lake Store.</span></span>

## <span data-ttu-id="9e0bc-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9e0bc-110">EXAMPLES</span></span>

### <span data-ttu-id="9e0bc-111">Exempel 1: hämta innehållet i en fil</span><span class="sxs-lookup"><span data-stu-id="9e0bc-111">Example 1: Get the contents of a file</span></span>
```
PS C:\>Get-AzureRmDataLakeStoreItemContent -AccountName "ContosoADL" -Path "/MyFile.txt"
```

<span data-ttu-id="9e0bc-112">Det här kommandot får innehållet i filen MyFile.txt i ContosoADL-kontot.</span><span class="sxs-lookup"><span data-stu-id="9e0bc-112">This command gets the contents of the file MyFile.txt in the ContosoADL account.</span></span>

### <span data-ttu-id="9e0bc-113">Exempel 2: Hämta de två första raderna i en fil</span><span class="sxs-lookup"><span data-stu-id="9e0bc-113">Example 2: Get the first two rows of a file</span></span>
```
PS C:\>Get-AzureRmDataLakeStoreItemContent -AccountName "ContosoADL" -Path "/MyFile.txt" -Head 2
```

<span data-ttu-id="9e0bc-114">Det här kommandot får de första två nya raderna avgränsade rader i filen MyFile.txt i ContosoADL-kontot.</span><span class="sxs-lookup"><span data-stu-id="9e0bc-114">This command gets the first two new line separated rows in the file MyFile.txt in the ContosoADL account.</span></span>

## <span data-ttu-id="9e0bc-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9e0bc-115">PARAMETERS</span></span>

### <span data-ttu-id="9e0bc-116">-Konto</span><span class="sxs-lookup"><span data-stu-id="9e0bc-116">-Account</span></span>
<span data-ttu-id="9e0bc-117">Anger namnet på data Lake Store-kontot.</span><span class="sxs-lookup"><span data-stu-id="9e0bc-117">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="9e0bc-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e0bc-118">-DefaultProfile</span></span>
<span data-ttu-id="9e0bc-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="9e0bc-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9e0bc-120">-Kodning</span><span class="sxs-lookup"><span data-stu-id="9e0bc-120">-Encoding</span></span>
<span data-ttu-id="9e0bc-121">Anger kodningen för det objekt som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="9e0bc-121">Specifies the encoding for the item to create.</span></span>
<span data-ttu-id="9e0bc-122">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="9e0bc-122">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="9e0bc-123">Känd</span><span class="sxs-lookup"><span data-stu-id="9e0bc-123">Unknown</span></span>
- <span data-ttu-id="9e0bc-124">Strängvärdet</span><span class="sxs-lookup"><span data-stu-id="9e0bc-124">String</span></span>
- <span data-ttu-id="9e0bc-125">Unicode</span><span class="sxs-lookup"><span data-stu-id="9e0bc-125">Unicode</span></span>
- <span data-ttu-id="9e0bc-126">SBCS</span><span class="sxs-lookup"><span data-stu-id="9e0bc-126">Byte</span></span>
- <span data-ttu-id="9e0bc-127">BigEndianUnicode</span><span class="sxs-lookup"><span data-stu-id="9e0bc-127">BigEndianUnicode</span></span>
- <span data-ttu-id="9e0bc-128">SKICKADE</span><span class="sxs-lookup"><span data-stu-id="9e0bc-128">UTF8</span></span>
- <span data-ttu-id="9e0bc-129">UTF7</span><span class="sxs-lookup"><span data-stu-id="9e0bc-129">UTF7</span></span>
- <span data-ttu-id="9e0bc-130">Teckenuppsättning</span><span class="sxs-lookup"><span data-stu-id="9e0bc-130">Ascii</span></span>
- <span data-ttu-id="9e0bc-131">Vis</span><span class="sxs-lookup"><span data-stu-id="9e0bc-131">Default</span></span>
- <span data-ttu-id="9e0bc-132">Koms</span><span class="sxs-lookup"><span data-stu-id="9e0bc-132">Oem</span></span>
- <span data-ttu-id="9e0bc-133">BigEndianUTF32</span><span class="sxs-lookup"><span data-stu-id="9e0bc-133">BigEndianUTF32</span></span>

```yaml
Type: FileSystemCmdletProviderEncoding
Parameter Sets: (All)
Aliases: 
Accepted values: Unknown, String, Unicode, Byte, BigEndianUnicode, UTF8, UTF7, UTF32, Ascii, Default, Oem, BigEndianUTF32

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e0bc-134">-Force</span><span class="sxs-lookup"><span data-stu-id="9e0bc-134">-Force</span></span>
<span data-ttu-id="9e0bc-135">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="9e0bc-135">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: PreviewFileContent
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e0bc-136">-Head</span><span class="sxs-lookup"><span data-stu-id="9e0bc-136">-Head</span></span>
<span data-ttu-id="9e0bc-137">Antalet rader (ny rad avgränsat) från början av filen som ska förhandsgranskas.</span><span class="sxs-lookup"><span data-stu-id="9e0bc-137">The number of rows (new line delimited) from the beginning of the file to preview.</span></span> <span data-ttu-id="9e0bc-138">Om ingen ny rad påträffas i det första 4 MB data returneras endast dessa data.</span><span class="sxs-lookup"><span data-stu-id="9e0bc-138">If no new line is encountered in the first 4mb of data, only that data will be returned.</span></span>

```yaml
Type: Int32
Parameter Sets: PreviewFileRowsFromHead
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e0bc-139">-Längd</span><span class="sxs-lookup"><span data-stu-id="9e0bc-139">-Length</span></span>
<span data-ttu-id="9e0bc-140">Anger längden i byte för innehållet som ska visas.</span><span class="sxs-lookup"><span data-stu-id="9e0bc-140">Specifies the length, in bytes, of the content to get.</span></span>

```yaml
Type: Int64
Parameter Sets: PreviewFileContent
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e0bc-141">-Offset</span><span class="sxs-lookup"><span data-stu-id="9e0bc-141">-Offset</span></span>
<span data-ttu-id="9e0bc-142">Anger antalet byte som ska hoppas över i en fil innan innehåll får plats.</span><span class="sxs-lookup"><span data-stu-id="9e0bc-142">Specifies the number of bytes to skip in a file before getting content.</span></span>

```yaml
Type: Int64
Parameter Sets: PreviewFileContent
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e0bc-143">-Path</span><span class="sxs-lookup"><span data-stu-id="9e0bc-143">-Path</span></span>
<span data-ttu-id="9e0bc-144">Anger data Lake Store-sökvägen för en fil, från rot katalogen (/).</span><span class="sxs-lookup"><span data-stu-id="9e0bc-144">Specifies the Data Lake Store path of a file, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="9e0bc-145">-Pilslut</span><span class="sxs-lookup"><span data-stu-id="9e0bc-145">-Tail</span></span>
<span data-ttu-id="9e0bc-146">Antalet rader (ny rad avgränsat) från slutet av filen för förhands granskning.</span><span class="sxs-lookup"><span data-stu-id="9e0bc-146">The number of rows (new line delimited) from the end of the file to preview.</span></span> <span data-ttu-id="9e0bc-147">Om ingen ny rad påträffas i det första 4 MB data returneras endast dessa data.</span><span class="sxs-lookup"><span data-stu-id="9e0bc-147">If no new line is encountered in the first 4mb of data, only that data will be returned.</span></span>

```yaml
Type: Int32
Parameter Sets: PreviewFileRowsFromTail
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e0bc-148">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="9e0bc-148">-Confirm</span></span>
<span data-ttu-id="9e0bc-149">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="9e0bc-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9e0bc-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9e0bc-150">-WhatIf</span></span>
<span data-ttu-id="9e0bc-151">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="9e0bc-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9e0bc-152">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="9e0bc-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9e0bc-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e0bc-153">CommonParameters</span></span>
<span data-ttu-id="9e0bc-154">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9e0bc-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e0bc-155">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9e0bc-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e0bc-156">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9e0bc-156">INPUTS</span></span>

### <span data-ttu-id="9e0bc-157">Ingen</span><span class="sxs-lookup"><span data-stu-id="9e0bc-157">None</span></span>
<span data-ttu-id="9e0bc-158">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="9e0bc-158">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="9e0bc-159">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9e0bc-159">OUTPUTS</span></span>

### <span data-ttu-id="9e0bc-160">byte []</span><span class="sxs-lookup"><span data-stu-id="9e0bc-160">byte[]</span></span>
<span data-ttu-id="9e0bc-161">Byte-dataströmmen för fil innehållet som hämtas.</span><span class="sxs-lookup"><span data-stu-id="9e0bc-161">The byte stream representation of the file contents retrieved.</span></span>

### <span data-ttu-id="9e0bc-162">strängvärdet</span><span class="sxs-lookup"><span data-stu-id="9e0bc-162">string</span></span>
<span data-ttu-id="9e0bc-163">Strängen (i angiven kodning) för fil innehållet som hämtas.</span><span class="sxs-lookup"><span data-stu-id="9e0bc-163">The string representation (in the specified encoding) of the file contents retrieved.</span></span>

## <span data-ttu-id="9e0bc-164">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9e0bc-164">NOTES</span></span>

## <span data-ttu-id="9e0bc-165">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9e0bc-165">RELATED LINKS</span></span>

