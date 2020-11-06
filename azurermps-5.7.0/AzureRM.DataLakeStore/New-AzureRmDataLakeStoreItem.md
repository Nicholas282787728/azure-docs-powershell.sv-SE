---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: A8222AB8-0003-4AC6-8114-294ABE8054CE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/new-azurermdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/New-AzureRmDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/New-AzureRmDataLakeStoreItem.md
ms.openlocfilehash: 2dc2d18fc0bc09fd7e9477115f4212aeb2452bbb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574300"
---
# <span data-ttu-id="a9359-101">New-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="a9359-101">New-AzureRmDataLakeStoreItem</span></span>

## <span data-ttu-id="a9359-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a9359-102">SYNOPSIS</span></span>
<span data-ttu-id="a9359-103">Skapar en ny fil eller mapp i data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="a9359-103">Creates a new file or folder in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a9359-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a9359-104">SYNTAX</span></span>

```
New-AzureRmDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance> [[-Value] <Object>]
 [[-Encoding] <FileSystemCmdletProviderEncoding>] [-Folder] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a9359-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a9359-105">DESCRIPTION</span></span>
<span data-ttu-id="a9359-106">Cmdleten **New-AzureRmDataLakeStoreItem** skapar en ny fil eller mapp i data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="a9359-106">The **New-AzureRmDataLakeStoreItem** cmdlet creates a new file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="a9359-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a9359-107">EXAMPLES</span></span>

### <span data-ttu-id="a9359-108">Exempel 1: skapa en ny fil och en ny mapp</span><span class="sxs-lookup"><span data-stu-id="a9359-108">Example 1: Create a new file and a new folder</span></span>
```
PS C:\>New-AzureRmDataLakeStoreItem -AccountName "ContosoADL" -Path "/NewFile.txt"
PS C:\> New-AzureRmDataLakeStoreItem -AccountName "ContosoADL" -Path "/NewFolder" -Folder
```

<span data-ttu-id="a9359-109">Det första kommandot skapar filen NewFile.txt för det angivna kontot.</span><span class="sxs-lookup"><span data-stu-id="a9359-109">The first command creates the file NewFile.txt for the specified account.</span></span>

<span data-ttu-id="a9359-110">Det andra kommandot skapar mappen NewFolder i rotmappen.</span><span class="sxs-lookup"><span data-stu-id="a9359-110">The second command creates the folder NewFolder at the root folder.</span></span>

## <span data-ttu-id="a9359-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a9359-111">PARAMETERS</span></span>

### <span data-ttu-id="a9359-112">-Konto</span><span class="sxs-lookup"><span data-stu-id="a9359-112">-Account</span></span>
<span data-ttu-id="a9359-113">Anger namnet på data Lake Store-kontot.</span><span class="sxs-lookup"><span data-stu-id="a9359-113">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="a9359-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9359-114">-DefaultProfile</span></span>
<span data-ttu-id="a9359-115">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a9359-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a9359-116">-Kodning</span><span class="sxs-lookup"><span data-stu-id="a9359-116">-Encoding</span></span>
<span data-ttu-id="a9359-117">Anger kodningen för det objekt som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="a9359-117">Specifies the encoding for the item to create.</span></span>
<span data-ttu-id="a9359-118">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="a9359-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="a9359-119">Känd</span><span class="sxs-lookup"><span data-stu-id="a9359-119">Unknown</span></span>
- <span data-ttu-id="a9359-120">Strängvärdet</span><span class="sxs-lookup"><span data-stu-id="a9359-120">String</span></span>
- <span data-ttu-id="a9359-121">Unicode</span><span class="sxs-lookup"><span data-stu-id="a9359-121">Unicode</span></span>
- <span data-ttu-id="a9359-122">SBCS</span><span class="sxs-lookup"><span data-stu-id="a9359-122">Byte</span></span>
- <span data-ttu-id="a9359-123">BigEndianUnicode</span><span class="sxs-lookup"><span data-stu-id="a9359-123">BigEndianUnicode</span></span>
- <span data-ttu-id="a9359-124">SKICKADE</span><span class="sxs-lookup"><span data-stu-id="a9359-124">UTF8</span></span>
- <span data-ttu-id="a9359-125">UTF7</span><span class="sxs-lookup"><span data-stu-id="a9359-125">UTF7</span></span>
- <span data-ttu-id="a9359-126">Teckenuppsättning</span><span class="sxs-lookup"><span data-stu-id="a9359-126">Ascii</span></span>
- <span data-ttu-id="a9359-127">Vis</span><span class="sxs-lookup"><span data-stu-id="a9359-127">Default</span></span>
- <span data-ttu-id="a9359-128">Koms</span><span class="sxs-lookup"><span data-stu-id="a9359-128">Oem</span></span>
- <span data-ttu-id="a9359-129">BigEndianUTF32</span><span class="sxs-lookup"><span data-stu-id="a9359-129">BigEndianUTF32</span></span>

```yaml
Type: FileSystemCmdletProviderEncoding
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9359-130">-Mappen</span><span class="sxs-lookup"><span data-stu-id="a9359-130">-Folder</span></span>
<span data-ttu-id="a9359-131">Anger att den här åtgärden skapar en mapp.</span><span class="sxs-lookup"><span data-stu-id="a9359-131">Indicates that this operation creates a folder.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9359-132">-Force</span><span class="sxs-lookup"><span data-stu-id="a9359-132">-Force</span></span>
<span data-ttu-id="a9359-133">Anger att den här åtgärden kan skriva över målobjektet om det redan finns.</span><span class="sxs-lookup"><span data-stu-id="a9359-133">Indicates that this operation can overwrite the destination item if it already exists.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9359-134">-Path</span><span class="sxs-lookup"><span data-stu-id="a9359-134">-Path</span></span>
<span data-ttu-id="a9359-135">Anger data Lake Store-sökvägen för det objekt som ska skapas, från rot katalogen (/).</span><span class="sxs-lookup"><span data-stu-id="a9359-135">Specifies the Data Lake Store path of the item to create, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="a9359-136">-Värde</span><span class="sxs-lookup"><span data-stu-id="a9359-136">-Value</span></span>
<span data-ttu-id="a9359-137">Anger vilket innehåll som ska läggas till i det objekt som du skapar.</span><span class="sxs-lookup"><span data-stu-id="a9359-137">Specifies the content to add to the item you create.</span></span>

```yaml
Type: Object
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a9359-138">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="a9359-138">-Confirm</span></span>
<span data-ttu-id="a9359-139">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="a9359-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a9359-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a9359-140">-WhatIf</span></span>
<span data-ttu-id="a9359-141">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="a9359-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a9359-142">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="a9359-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a9359-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9359-143">CommonParameters</span></span>
<span data-ttu-id="a9359-144">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a9359-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9359-145">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a9359-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9359-146">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a9359-146">INPUTS</span></span>

### <span data-ttu-id="a9359-147">Serverobjektet</span><span class="sxs-lookup"><span data-stu-id="a9359-147">Object</span></span>
<span data-ttu-id="a9359-148">Parametern ' värde ' godkänner värdet för typen ' object ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="a9359-148">Parameter 'Value' accepts value of type 'Object' from the pipeline</span></span>

## <span data-ttu-id="a9359-149">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a9359-149">OUTPUTS</span></span>

### <span data-ttu-id="a9359-150">strängvärdet</span><span class="sxs-lookup"><span data-stu-id="a9359-150">string</span></span>
<span data-ttu-id="a9359-151">Den fullständiga sökvägen till den skapade filen eller mappen.</span><span class="sxs-lookup"><span data-stu-id="a9359-151">The full path to the created file or folder.</span></span>

## <span data-ttu-id="a9359-152">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a9359-152">NOTES</span></span>

## <span data-ttu-id="a9359-153">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a9359-153">RELATED LINKS</span></span>

[<span data-ttu-id="a9359-154">Get-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="a9359-154">Get-AzureRmDataLakeStoreItem</span></span>](./Get-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="a9359-155">Exportera-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="a9359-155">Export-AzureRmDataLakeStoreItem</span></span>](./Export-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="a9359-156">Import-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="a9359-156">Import-AzureRmDataLakeStoreItem</span></span>](./Import-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="a9359-157">New-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="a9359-157">New-AzureRmDataLakeStoreItem</span></span>](./New-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="a9359-158">Remove-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="a9359-158">Remove-AzureRmDataLakeStoreItem</span></span>](./Remove-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="a9359-159">Test-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="a9359-159">Test-AzureRmDataLakeStoreItem</span></span>](./Test-AzureRmDataLakeStoreItem.md)


