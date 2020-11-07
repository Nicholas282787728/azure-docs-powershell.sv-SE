---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: B008028D-27FC-4469-BE71-54F7218C068B
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/add-azdatalakestoreitemcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Add-AzDataLakeStoreItemContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Add-AzDataLakeStoreItemContent.md
ms.openlocfilehash: 1727c0960d90a8566d2247e8d8e091f6ce66f9b5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93754310"
---
# <span data-ttu-id="d2c29-101">Add-AzDataLakeStoreItemContent</span><span class="sxs-lookup"><span data-stu-id="d2c29-101">Add-AzDataLakeStoreItemContent</span></span>

## <span data-ttu-id="d2c29-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d2c29-102">SYNOPSIS</span></span>
<span data-ttu-id="d2c29-103">Lägger till innehåll i ett objekt i en data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="d2c29-103">Adds content to an item in a Data Lake Store.</span></span>

## <span data-ttu-id="d2c29-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d2c29-104">SYNTAX</span></span>

```
Add-AzDataLakeStoreItemContent [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Value] <Object>
 [[-Encoding] <Encoding>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d2c29-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d2c29-105">DESCRIPTION</span></span>
<span data-ttu-id="d2c29-106">Cmdleten **Add-AzDataLakeStoreItemContent** lägger till innehåll i ett objekt i en Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="d2c29-106">The **Add-AzDataLakeStoreItemContent** cmdlet adds content to an item in an Azure Data Lake Store.</span></span>

## <span data-ttu-id="d2c29-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d2c29-107">EXAMPLES</span></span>

### <span data-ttu-id="d2c29-108">Exempel 1: lägga till innehåll i en fil</span><span class="sxs-lookup"><span data-stu-id="d2c29-108">Example 1: Add content to a file</span></span>
```
PS C:\>Add-AzDataLakeStoreItemContent -AccountName "ContosoADLS" -Path /abc/myFile.txt -Value "My content here"
```

<span data-ttu-id="d2c29-109">Det här kommandot lägger till innehåll i filen myFile.txt.</span><span class="sxs-lookup"><span data-stu-id="d2c29-109">This command adds content to the file myFile.txt.</span></span>

## <span data-ttu-id="d2c29-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d2c29-110">PARAMETERS</span></span>

### <span data-ttu-id="d2c29-111">-Konto</span><span class="sxs-lookup"><span data-stu-id="d2c29-111">-Account</span></span>
<span data-ttu-id="d2c29-112">Anger namnet på data Lake Store-kontot.</span><span class="sxs-lookup"><span data-stu-id="d2c29-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="d2c29-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2c29-113">-DefaultProfile</span></span>
<span data-ttu-id="d2c29-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="d2c29-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d2c29-115">-Kodning</span><span class="sxs-lookup"><span data-stu-id="d2c29-115">-Encoding</span></span>
<span data-ttu-id="d2c29-116">Anger kodningen för det objekt som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="d2c29-116">Specifies the encoding for the item to create.</span></span>
<span data-ttu-id="d2c29-117">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="d2c29-117">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="d2c29-118">Känd</span><span class="sxs-lookup"><span data-stu-id="d2c29-118">Unknown</span></span>
- <span data-ttu-id="d2c29-119">Strängvärdet</span><span class="sxs-lookup"><span data-stu-id="d2c29-119">String</span></span>
- <span data-ttu-id="d2c29-120">Unicode</span><span class="sxs-lookup"><span data-stu-id="d2c29-120">Unicode</span></span>
- <span data-ttu-id="d2c29-121">SBCS</span><span class="sxs-lookup"><span data-stu-id="d2c29-121">Byte</span></span>
- <span data-ttu-id="d2c29-122">BigEndianUnicode</span><span class="sxs-lookup"><span data-stu-id="d2c29-122">BigEndianUnicode</span></span>
- <span data-ttu-id="d2c29-123">SKICKADE</span><span class="sxs-lookup"><span data-stu-id="d2c29-123">UTF8</span></span>
- <span data-ttu-id="d2c29-124">UTF7</span><span class="sxs-lookup"><span data-stu-id="d2c29-124">UTF7</span></span>
- <span data-ttu-id="d2c29-125">Teckenuppsättning</span><span class="sxs-lookup"><span data-stu-id="d2c29-125">Ascii</span></span>
- <span data-ttu-id="d2c29-126">Vis</span><span class="sxs-lookup"><span data-stu-id="d2c29-126">Default</span></span>
- <span data-ttu-id="d2c29-127">Koms</span><span class="sxs-lookup"><span data-stu-id="d2c29-127">Oem</span></span>
- <span data-ttu-id="d2c29-128">BigEndianUTF32</span><span class="sxs-lookup"><span data-stu-id="d2c29-128">BigEndianUTF32</span></span>

```yaml
Type: System.Text.Encoding
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d2c29-129">-Path</span><span class="sxs-lookup"><span data-stu-id="d2c29-129">-Path</span></span>
<span data-ttu-id="d2c29-130">Anger data Lake Store-sökvägen för det objekt som ska ändras, från rot katalogen (/).</span><span class="sxs-lookup"><span data-stu-id="d2c29-130">Specifies the Data Lake Store path of the item to modify, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="d2c29-131">-Värde</span><span class="sxs-lookup"><span data-stu-id="d2c29-131">-Value</span></span>
<span data-ttu-id="d2c29-132">Anger vilket innehåll som ska läggas till objektet.</span><span class="sxs-lookup"><span data-stu-id="d2c29-132">Specifies the content to add to the item.</span></span>

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

### <span data-ttu-id="d2c29-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2c29-133">CommonParameters</span></span>
<span data-ttu-id="d2c29-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d2c29-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2c29-135">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d2c29-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2c29-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d2c29-136">INPUTS</span></span>

### <span data-ttu-id="d2c29-137">System. String</span><span class="sxs-lookup"><span data-stu-id="d2c29-137">System.String</span></span>

### <span data-ttu-id="d2c29-138">Microsoft. Azure. commands. DataLakeStore. Models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="d2c29-138">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="d2c29-139">System. Object</span><span class="sxs-lookup"><span data-stu-id="d2c29-139">System.Object</span></span>

### <span data-ttu-id="d2c29-140">System. text. Encoding</span><span class="sxs-lookup"><span data-stu-id="d2c29-140">System.Text.Encoding</span></span>

## <span data-ttu-id="d2c29-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d2c29-141">OUTPUTS</span></span>

### <span data-ttu-id="d2c29-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d2c29-142">System.Boolean</span></span>

## <span data-ttu-id="d2c29-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d2c29-143">NOTES</span></span>

## <span data-ttu-id="d2c29-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d2c29-144">RELATED LINKS</span></span>

[<span data-ttu-id="d2c29-145">Get-AzDataLakeStoreItemContent</span><span class="sxs-lookup"><span data-stu-id="d2c29-145">Get-AzDataLakeStoreItemContent</span></span>](./Get-AzDataLakeStoreItemContent.md)


