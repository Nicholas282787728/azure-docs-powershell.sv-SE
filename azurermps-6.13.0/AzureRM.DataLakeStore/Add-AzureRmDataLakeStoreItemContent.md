---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: B008028D-27FC-4469-BE71-54F7218C068B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/add-azurermdatalakestoreitemcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Add-AzureRmDataLakeStoreItemContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Add-AzureRmDataLakeStoreItemContent.md
ms.openlocfilehash: ed931444940b86c04e027eb88da9266c7af20206
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93580160"
---
# <span data-ttu-id="1990b-101">Add-AzureRmDataLakeStoreItemContent</span><span class="sxs-lookup"><span data-stu-id="1990b-101">Add-AzureRmDataLakeStoreItemContent</span></span>

## <span data-ttu-id="1990b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1990b-102">SYNOPSIS</span></span>
<span data-ttu-id="1990b-103">Lägger till innehåll i ett objekt i en data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="1990b-103">Adds content to an item in a Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1990b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1990b-104">SYNTAX</span></span>

```
Add-AzureRmDataLakeStoreItemContent [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Value] <Object>
 [[-Encoding] <FileSystemCmdletProviderEncoding>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1990b-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1990b-105">DESCRIPTION</span></span>
<span data-ttu-id="1990b-106">Cmdleten **Add-AzureRmDataLakeStoreItemContent** lägger till innehåll i ett objekt i en Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="1990b-106">The **Add-AzureRmDataLakeStoreItemContent** cmdlet adds content to an item in an Azure Data Lake Store.</span></span>

## <span data-ttu-id="1990b-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1990b-107">EXAMPLES</span></span>

### <span data-ttu-id="1990b-108">Exempel 1: lägga till innehåll i en fil</span><span class="sxs-lookup"><span data-stu-id="1990b-108">Example 1: Add content to a file</span></span>
```
PS C:\>Add-AzureRmDataLakeStoreItemContent -AccountName "ContosoADLS" -Path /abc/myFile.txt -Value "My content here"
```

<span data-ttu-id="1990b-109">Det här kommandot lägger till innehåll i filen myFile.txt.</span><span class="sxs-lookup"><span data-stu-id="1990b-109">This command adds content to the file myFile.txt.</span></span>

## <span data-ttu-id="1990b-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1990b-110">PARAMETERS</span></span>

### <span data-ttu-id="1990b-111">-Konto</span><span class="sxs-lookup"><span data-stu-id="1990b-111">-Account</span></span>
<span data-ttu-id="1990b-112">Anger namnet på data Lake Store-kontot.</span><span class="sxs-lookup"><span data-stu-id="1990b-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="1990b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1990b-113">-DefaultProfile</span></span>
<span data-ttu-id="1990b-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="1990b-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1990b-115">-Kodning</span><span class="sxs-lookup"><span data-stu-id="1990b-115">-Encoding</span></span>
<span data-ttu-id="1990b-116">Anger kodningen för det objekt som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="1990b-116">Specifies the encoding for the item to create.</span></span>
<span data-ttu-id="1990b-117">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="1990b-117">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="1990b-118">Känd</span><span class="sxs-lookup"><span data-stu-id="1990b-118">Unknown</span></span>
- <span data-ttu-id="1990b-119">Strängvärdet</span><span class="sxs-lookup"><span data-stu-id="1990b-119">String</span></span>
- <span data-ttu-id="1990b-120">Unicode</span><span class="sxs-lookup"><span data-stu-id="1990b-120">Unicode</span></span>
- <span data-ttu-id="1990b-121">SBCS</span><span class="sxs-lookup"><span data-stu-id="1990b-121">Byte</span></span>
- <span data-ttu-id="1990b-122">BigEndianUnicode</span><span class="sxs-lookup"><span data-stu-id="1990b-122">BigEndianUnicode</span></span>
- <span data-ttu-id="1990b-123">SKICKADE</span><span class="sxs-lookup"><span data-stu-id="1990b-123">UTF8</span></span>
- <span data-ttu-id="1990b-124">UTF7</span><span class="sxs-lookup"><span data-stu-id="1990b-124">UTF7</span></span>
- <span data-ttu-id="1990b-125">Teckenuppsättning</span><span class="sxs-lookup"><span data-stu-id="1990b-125">Ascii</span></span>
- <span data-ttu-id="1990b-126">Vis</span><span class="sxs-lookup"><span data-stu-id="1990b-126">Default</span></span>
- <span data-ttu-id="1990b-127">Koms</span><span class="sxs-lookup"><span data-stu-id="1990b-127">Oem</span></span>
- <span data-ttu-id="1990b-128">BigEndianUTF32</span><span class="sxs-lookup"><span data-stu-id="1990b-128">BigEndianUTF32</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.FileSystemCmdletProviderEncoding
Parameter Sets: (All)
Aliases:
Accepted values: Unknown, String, Unicode, Byte, BigEndianUnicode, UTF8, UTF7, UTF32, Ascii, Default, Oem, BigEndianUTF32

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1990b-129">-Path</span><span class="sxs-lookup"><span data-stu-id="1990b-129">-Path</span></span>
<span data-ttu-id="1990b-130">Anger data Lake Store-sökvägen för det objekt som ska ändras, från rot katalogen (/).</span><span class="sxs-lookup"><span data-stu-id="1990b-130">Specifies the Data Lake Store path of the item to modify, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="1990b-131">-Värde</span><span class="sxs-lookup"><span data-stu-id="1990b-131">-Value</span></span>
<span data-ttu-id="1990b-132">Anger vilket innehåll som ska läggas till objektet.</span><span class="sxs-lookup"><span data-stu-id="1990b-132">Specifies the content to add to the item.</span></span>

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

### <span data-ttu-id="1990b-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1990b-133">CommonParameters</span></span>
<span data-ttu-id="1990b-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1990b-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1990b-135">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1990b-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1990b-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1990b-136">INPUTS</span></span>

### <span data-ttu-id="1990b-137">System. String</span><span class="sxs-lookup"><span data-stu-id="1990b-137">System.String</span></span>

### <span data-ttu-id="1990b-138">Microsoft. Azure. commands. DataLakeStore. Models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="1990b-138">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="1990b-139">System. Object</span><span class="sxs-lookup"><span data-stu-id="1990b-139">System.Object</span></span>

### <span data-ttu-id="1990b-140">Microsoft. Azure. commands. DataLakeStore. Models. FileSystemCmdletProviderEncoding</span><span class="sxs-lookup"><span data-stu-id="1990b-140">Microsoft.Azure.Commands.DataLakeStore.Models.FileSystemCmdletProviderEncoding</span></span>

## <span data-ttu-id="1990b-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1990b-141">OUTPUTS</span></span>

### <span data-ttu-id="1990b-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="1990b-142">System.Boolean</span></span>

## <span data-ttu-id="1990b-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1990b-143">NOTES</span></span>

## <span data-ttu-id="1990b-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1990b-144">RELATED LINKS</span></span>

[<span data-ttu-id="1990b-145">Get-AzureRmDataLakeStoreItemContent</span><span class="sxs-lookup"><span data-stu-id="1990b-145">Get-AzureRmDataLakeStoreItemContent</span></span>](./Get-AzureRmDataLakeStoreItemContent.md)


