---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 15DFF66F-3D78-422B-BA40-71058DE66BA2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreItemContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreItemContent.md
ms.openlocfilehash: 3da97a14049671f8fff8bc03f7f32609f9b86984
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756984"
---
# <span data-ttu-id="e7ba8-101">Get-AzureRmDataLakeStoreItemContent</span><span class="sxs-lookup"><span data-stu-id="e7ba8-101">Get-AzureRmDataLakeStoreItemContent</span></span>

## <span data-ttu-id="e7ba8-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e7ba8-102">SYNOPSIS</span></span>
<span data-ttu-id="e7ba8-103">Hämtar innehållet i en fil i data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="e7ba8-103">Gets the contents of a file in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e7ba8-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e7ba8-104">SYNTAX</span></span>

### <span data-ttu-id="e7ba8-105">Förhandsgranska fil innehåll (standard)</span><span class="sxs-lookup"><span data-stu-id="e7ba8-105">Preview file content (Default)</span></span>
```
Get-AzureRmDataLakeStoreItemContent [-Account] <String> [-Path] <DataLakeStorePathInstance> [[-Offset] <Int64>]
 [[-Length] <Int64>] [[-Encoding] <FileSystemCmdletProviderEncoding>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e7ba8-106">Förhandsgranska fil rader från huvudet på filen</span><span class="sxs-lookup"><span data-stu-id="e7ba8-106">Preview file rows from the head of the file</span></span>
```
Get-AzureRmDataLakeStoreItemContent [-Account] <String> [-Path] <DataLakeStorePathInstance> [[-Head] <Int32>]
 [[-Encoding] <FileSystemCmdletProviderEncoding>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e7ba8-107">Förhandsgranska fil rader från slutet av filen</span><span class="sxs-lookup"><span data-stu-id="e7ba8-107">Preview file rows from the tail of the file</span></span>
```
Get-AzureRmDataLakeStoreItemContent [-Account] <String> [-Path] <DataLakeStorePathInstance> [[-Tail] <Int32>]
 [[-Encoding] <FileSystemCmdletProviderEncoding>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e7ba8-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e7ba8-108">DESCRIPTION</span></span>
<span data-ttu-id="e7ba8-109">Cmdleten **Get-AzureRmDataLakeStoreItemContent** hämtar innehållet i en fil i data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="e7ba8-109">The **Get-AzureRmDataLakeStoreItemContent** cmdlet gets the contents of a file in Data Lake Store.</span></span>

## <span data-ttu-id="e7ba8-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e7ba8-110">EXAMPLES</span></span>

### <span data-ttu-id="e7ba8-111">Exempel 1: hämta innehållet i en fil</span><span class="sxs-lookup"><span data-stu-id="e7ba8-111">Example 1: Get the contents of a file</span></span>
```
PS C:\>Get-AzureRmDataLakeStoreItemContent -AccountName "ContosoADL" -Path "/MyFile.txt"
```

<span data-ttu-id="e7ba8-112">Det här kommandot får innehållet i filen MyFile.txt i ContosoADL-kontot.</span><span class="sxs-lookup"><span data-stu-id="e7ba8-112">This command gets the contents of the file MyFile.txt in the ContosoADL account.</span></span>

### <span data-ttu-id="e7ba8-113">Exempel 2: Hämta de två första raderna i en fil</span><span class="sxs-lookup"><span data-stu-id="e7ba8-113">Example 2: Get the first two rows of a file</span></span>
```
PS C:\>Get-AzureRmDataLakeStoreItemContent -AccountName "ContosoADL" -Path "/MyFile.txt" -Head 2
```

<span data-ttu-id="e7ba8-114">Det här kommandot får de första två nya raderna avgränsade rader i filen MyFile.txt i ContosoADL-kontot.</span><span class="sxs-lookup"><span data-stu-id="e7ba8-114">This command gets the first two new line separated rows in the file MyFile.txt in the ContosoADL account.</span></span>

## <span data-ttu-id="e7ba8-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e7ba8-115">PARAMETERS</span></span>

### <span data-ttu-id="e7ba8-116">-Konto</span><span class="sxs-lookup"><span data-stu-id="e7ba8-116">-Account</span></span>
<span data-ttu-id="e7ba8-117">Anger namnet på data Lake Store-kontot.</span><span class="sxs-lookup"><span data-stu-id="e7ba8-117">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="e7ba8-118">-Kodning</span><span class="sxs-lookup"><span data-stu-id="e7ba8-118">-Encoding</span></span>
<span data-ttu-id="e7ba8-119">Anger kodningen för det objekt som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="e7ba8-119">Specifies the encoding for the item to create.</span></span>
<span data-ttu-id="e7ba8-120">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="e7ba8-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="e7ba8-121">Känd</span><span class="sxs-lookup"><span data-stu-id="e7ba8-121">Unknown</span></span>
- <span data-ttu-id="e7ba8-122">Strängvärdet</span><span class="sxs-lookup"><span data-stu-id="e7ba8-122">String</span></span>
- <span data-ttu-id="e7ba8-123">Unicode</span><span class="sxs-lookup"><span data-stu-id="e7ba8-123">Unicode</span></span>
- <span data-ttu-id="e7ba8-124">SBCS</span><span class="sxs-lookup"><span data-stu-id="e7ba8-124">Byte</span></span>
- <span data-ttu-id="e7ba8-125">BigEndianUnicode</span><span class="sxs-lookup"><span data-stu-id="e7ba8-125">BigEndianUnicode</span></span>
- <span data-ttu-id="e7ba8-126">SKICKADE</span><span class="sxs-lookup"><span data-stu-id="e7ba8-126">UTF8</span></span>
- <span data-ttu-id="e7ba8-127">UTF7</span><span class="sxs-lookup"><span data-stu-id="e7ba8-127">UTF7</span></span>
- <span data-ttu-id="e7ba8-128">Teckenuppsättning</span><span class="sxs-lookup"><span data-stu-id="e7ba8-128">Ascii</span></span>
- <span data-ttu-id="e7ba8-129">Vis</span><span class="sxs-lookup"><span data-stu-id="e7ba8-129">Default</span></span>
- <span data-ttu-id="e7ba8-130">Koms</span><span class="sxs-lookup"><span data-stu-id="e7ba8-130">Oem</span></span>
- <span data-ttu-id="e7ba8-131">BigEndianUTF32</span><span class="sxs-lookup"><span data-stu-id="e7ba8-131">BigEndianUTF32</span></span>

```yaml
Type: Microsoft.PowerShell.Commands.FileSystemCmdletProviderEncoding
Parameter Sets: (All)
Aliases: 
Accepted values: Unknown, String, Unicode, Byte, BigEndianUnicode, UTF8, UTF7, UTF32, Ascii, Default, Oem, BigEndianUTF32

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7ba8-132">-Force</span><span class="sxs-lookup"><span data-stu-id="e7ba8-132">-Force</span></span>
<span data-ttu-id="e7ba8-133">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="e7ba8-133">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Preview file content
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7ba8-134">-Head</span><span class="sxs-lookup"><span data-stu-id="e7ba8-134">-Head</span></span>
<span data-ttu-id="e7ba8-135">Antalet rader (ny rad avgränsat) från början av filen som ska förhandsgranskas.</span><span class="sxs-lookup"><span data-stu-id="e7ba8-135">The number of rows (new line delimited) from the beginning of the file to preview.</span></span> <span data-ttu-id="e7ba8-136">Om ingen ny rad påträffas i det första 4 MB data returneras endast dessa data.</span><span class="sxs-lookup"><span data-stu-id="e7ba8-136">If no new line is encountered in the first 4mb of data, only that data will be returned.</span></span>

```yaml
Type: System.Int32
Parameter Sets: Preview file rows from the head of the file
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7ba8-137">-Längd</span><span class="sxs-lookup"><span data-stu-id="e7ba8-137">-Length</span></span>
<span data-ttu-id="e7ba8-138">Anger längden i byte för innehållet som ska visas.</span><span class="sxs-lookup"><span data-stu-id="e7ba8-138">Specifies the length, in bytes, of the content to get.</span></span>

```yaml
Type: System.Int64
Parameter Sets: Preview file content
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7ba8-139">-Offset</span><span class="sxs-lookup"><span data-stu-id="e7ba8-139">-Offset</span></span>
<span data-ttu-id="e7ba8-140">Anger antalet byte som ska hoppas över i en fil innan innehåll får plats.</span><span class="sxs-lookup"><span data-stu-id="e7ba8-140">Specifies the number of bytes to skip in a file before getting content.</span></span>

```yaml
Type: System.Int64
Parameter Sets: Preview file content
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7ba8-141">-Path</span><span class="sxs-lookup"><span data-stu-id="e7ba8-141">-Path</span></span>
<span data-ttu-id="e7ba8-142">Anger data Lake Store-sökvägen för en fil, från rot katalogen (/).</span><span class="sxs-lookup"><span data-stu-id="e7ba8-142">Specifies the Data Lake Store path of a file, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="e7ba8-143">-Pilslut</span><span class="sxs-lookup"><span data-stu-id="e7ba8-143">-Tail</span></span>
<span data-ttu-id="e7ba8-144">Antalet rader (ny rad avgränsat) från slutet av filen för förhands granskning.</span><span class="sxs-lookup"><span data-stu-id="e7ba8-144">The number of rows (new line delimited) from the end of the file to preview.</span></span> <span data-ttu-id="e7ba8-145">Om ingen ny rad påträffas i det första 4 MB data returneras endast dessa data.</span><span class="sxs-lookup"><span data-stu-id="e7ba8-145">If no new line is encountered in the first 4mb of data, only that data will be returned.</span></span>

```yaml
Type: System.Int32
Parameter Sets: Preview file rows from the tail of the file
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7ba8-146">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="e7ba8-146">-Confirm</span></span>
<span data-ttu-id="e7ba8-147">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="e7ba8-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e7ba8-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e7ba8-148">-WhatIf</span></span>
<span data-ttu-id="e7ba8-149">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="e7ba8-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e7ba8-150">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="e7ba8-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e7ba8-151">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7ba8-151">-DefaultProfile</span></span>
<span data-ttu-id="e7ba8-152">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e7ba8-152">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e7ba8-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7ba8-153">CommonParameters</span></span>
<span data-ttu-id="e7ba8-154">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e7ba8-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7ba8-155">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e7ba8-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7ba8-156">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e7ba8-156">INPUTS</span></span>

## <span data-ttu-id="e7ba8-157">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e7ba8-157">OUTPUTS</span></span>

### <span data-ttu-id="e7ba8-158">byte []</span><span class="sxs-lookup"><span data-stu-id="e7ba8-158">byte[]</span></span>
<span data-ttu-id="e7ba8-159">Byte-dataströmmen för fil innehållet som hämtas.</span><span class="sxs-lookup"><span data-stu-id="e7ba8-159">The byte stream representation of the file contents retrieved.</span></span>

### <span data-ttu-id="e7ba8-160">strängvärdet</span><span class="sxs-lookup"><span data-stu-id="e7ba8-160">string</span></span>
<span data-ttu-id="e7ba8-161">Strängen (i angiven kodning) för fil innehållet som hämtas.</span><span class="sxs-lookup"><span data-stu-id="e7ba8-161">The string representation (in the specified encoding) of the file contents retrieved.</span></span>

## <span data-ttu-id="e7ba8-162">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e7ba8-162">NOTES</span></span>

## <span data-ttu-id="e7ba8-163">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e7ba8-163">RELATED LINKS</span></span>

