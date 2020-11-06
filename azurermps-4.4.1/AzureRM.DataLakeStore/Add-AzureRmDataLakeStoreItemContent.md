---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: B008028D-27FC-4469-BE71-54F7218C068B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Add-AzureRmDataLakeStoreItemContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Add-AzureRmDataLakeStoreItemContent.md
ms.openlocfilehash: 4ce79044793bbecc76d72fab015166ccc3d8fba6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574685"
---
# <span data-ttu-id="11460-101">Add-AzureRmDataLakeStoreItemContent</span><span class="sxs-lookup"><span data-stu-id="11460-101">Add-AzureRmDataLakeStoreItemContent</span></span>

## <span data-ttu-id="11460-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="11460-102">SYNOPSIS</span></span>
<span data-ttu-id="11460-103">Lägger till innehåll i ett objekt i en data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="11460-103">Adds content to an item in a Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="11460-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="11460-104">SYNTAX</span></span>

```
Add-AzureRmDataLakeStoreItemContent [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Value] <Object>
 [[-Encoding] <FileSystemCmdletProviderEncoding>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="11460-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="11460-105">DESCRIPTION</span></span>
<span data-ttu-id="11460-106">Cmdleten **Add-AzureRmDataLakeStoreItemContent** lägger till innehåll i ett objekt i en Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="11460-106">The **Add-AzureRmDataLakeStoreItemContent** cmdlet adds content to an item in an Azure Data Lake Store.</span></span>

## <span data-ttu-id="11460-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="11460-107">EXAMPLES</span></span>

### <span data-ttu-id="11460-108">Exempel 1: lägga till innehåll i en fil</span><span class="sxs-lookup"><span data-stu-id="11460-108">Example 1: Add content to a file</span></span>
```
PS C:\>Add-AzureRmDataLakeStoreItemContent -AccountName "ContosoADLS" -Path /abc/myFile.txt -Value "My content here"
```

<span data-ttu-id="11460-109">Det här kommandot lägger till innehåll i filen myFile.txt.</span><span class="sxs-lookup"><span data-stu-id="11460-109">This command adds content to the file myFile.txt.</span></span>

## <span data-ttu-id="11460-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="11460-110">PARAMETERS</span></span>

### <span data-ttu-id="11460-111">-Konto</span><span class="sxs-lookup"><span data-stu-id="11460-111">-Account</span></span>
<span data-ttu-id="11460-112">Anger namnet på data Lake Store-kontot.</span><span class="sxs-lookup"><span data-stu-id="11460-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="11460-113">-Kodning</span><span class="sxs-lookup"><span data-stu-id="11460-113">-Encoding</span></span>
<span data-ttu-id="11460-114">Anger kodningen för det objekt som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="11460-114">Specifies the encoding for the item to create.</span></span>
<span data-ttu-id="11460-115">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="11460-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="11460-116">Känd</span><span class="sxs-lookup"><span data-stu-id="11460-116">Unknown</span></span>
- <span data-ttu-id="11460-117">Strängvärdet</span><span class="sxs-lookup"><span data-stu-id="11460-117">String</span></span>
- <span data-ttu-id="11460-118">Unicode</span><span class="sxs-lookup"><span data-stu-id="11460-118">Unicode</span></span>
- <span data-ttu-id="11460-119">SBCS</span><span class="sxs-lookup"><span data-stu-id="11460-119">Byte</span></span>
- <span data-ttu-id="11460-120">BigEndianUnicode</span><span class="sxs-lookup"><span data-stu-id="11460-120">BigEndianUnicode</span></span>
- <span data-ttu-id="11460-121">SKICKADE</span><span class="sxs-lookup"><span data-stu-id="11460-121">UTF8</span></span>
- <span data-ttu-id="11460-122">UTF7</span><span class="sxs-lookup"><span data-stu-id="11460-122">UTF7</span></span>
- <span data-ttu-id="11460-123">Teckenuppsättning</span><span class="sxs-lookup"><span data-stu-id="11460-123">Ascii</span></span>
- <span data-ttu-id="11460-124">Vis</span><span class="sxs-lookup"><span data-stu-id="11460-124">Default</span></span>
- <span data-ttu-id="11460-125">Koms</span><span class="sxs-lookup"><span data-stu-id="11460-125">Oem</span></span>
- <span data-ttu-id="11460-126">BigEndianUTF32</span><span class="sxs-lookup"><span data-stu-id="11460-126">BigEndianUTF32</span></span>

```yaml
Type: Microsoft.PowerShell.Commands.FileSystemCmdletProviderEncoding
Parameter Sets: (All)
Aliases: 
Accepted values: Unknown, String, Unicode, Byte, BigEndianUnicode, UTF8, UTF7, UTF32, Ascii, Default, Oem, BigEndianUTF32

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11460-127">-Path</span><span class="sxs-lookup"><span data-stu-id="11460-127">-Path</span></span>
<span data-ttu-id="11460-128">Anger data Lake Store-sökvägen för det objekt som ska ändras, från rot katalogen (/).</span><span class="sxs-lookup"><span data-stu-id="11460-128">Specifies the Data Lake Store path of the item to modify, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="11460-129">-Värde</span><span class="sxs-lookup"><span data-stu-id="11460-129">-Value</span></span>
<span data-ttu-id="11460-130">Anger vilket innehåll som ska läggas till objektet.</span><span class="sxs-lookup"><span data-stu-id="11460-130">Specifies the content to add to the item.</span></span>

```yaml
Type: System.Object
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="11460-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11460-131">-DefaultProfile</span></span>
<span data-ttu-id="11460-132">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="11460-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="11460-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11460-133">CommonParameters</span></span>
<span data-ttu-id="11460-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="11460-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11460-135">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="11460-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11460-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="11460-136">INPUTS</span></span>

### <span data-ttu-id="11460-137">Serverobjektet</span><span class="sxs-lookup"><span data-stu-id="11460-137">Object</span></span>
<span data-ttu-id="11460-138">Parametern ' värde ' godkänner värdet för typen ' object ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="11460-138">Parameter 'Value' accepts value of type 'Object' from the pipeline</span></span>

## <span data-ttu-id="11460-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="11460-139">OUTPUTS</span></span>

### <span data-ttu-id="11460-140">bool</span><span class="sxs-lookup"><span data-stu-id="11460-140">bool</span></span>
<span data-ttu-id="11460-141">Returnerar true vid framgång.</span><span class="sxs-lookup"><span data-stu-id="11460-141">Returns true on success.</span></span>

## <span data-ttu-id="11460-142">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="11460-142">NOTES</span></span>

## <span data-ttu-id="11460-143">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="11460-143">RELATED LINKS</span></span>

[<span data-ttu-id="11460-144">Get-AzureRmDataLakeStoreItemContent</span><span class="sxs-lookup"><span data-stu-id="11460-144">Get-AzureRmDataLakeStoreItemContent</span></span>](./Get-AzureRmDataLakeStoreItemContent.md)


