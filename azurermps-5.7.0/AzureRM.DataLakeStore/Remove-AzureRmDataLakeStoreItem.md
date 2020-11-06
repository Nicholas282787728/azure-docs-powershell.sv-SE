---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 164DC871-0F0C-4E71-A37A-2B85CE65C2C4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/remove-azurermdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Remove-AzureRmDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Remove-AzureRmDataLakeStoreItem.md
ms.openlocfilehash: 40477ad0635f1b832e7d95e459b27102dc68f8db
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573448"
---
# <span data-ttu-id="4febd-101">Remove-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="4febd-101">Remove-AzureRmDataLakeStoreItem</span></span>

## <span data-ttu-id="4febd-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4febd-102">SYNOPSIS</span></span>
<span data-ttu-id="4febd-103">Tar bort en fil eller mapp i data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="4febd-103">Deletes a file or folder in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4febd-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4febd-104">SYNTAX</span></span>

```
Remove-AzureRmDataLakeStoreItem [-Account] <String> [-Paths] <DataLakeStorePathInstance[]> [-Recurse] [-Clean]
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4febd-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4febd-105">DESCRIPTION</span></span>
<span data-ttu-id="4febd-106">Cmdleten **Remove-AzureRmDataLakeStoreItem** tar bort en fil eller mapp i data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="4febd-106">The **Remove-AzureRmDataLakeStoreItem** cmdlet deletes a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="4febd-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4febd-107">EXAMPLES</span></span>

### <span data-ttu-id="4febd-108">Exempel 1: ta bort flera objekt</span><span class="sxs-lookup"><span data-stu-id="4febd-108">Example 1: Remove multiple items</span></span>
```
PS C:\>Remove-AzureRmDataLakeStoreItem -AccountName "ContosoADL" -Paths "/File01.txt","/MyFiles/File.csv"
```

<span data-ttu-id="4febd-109">Det här kommandot tar bort filerna File01.txt och File.csv från data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="4febd-109">This command removes the files File01.txt and File.csv from the Data Lake Store.</span></span>

## <span data-ttu-id="4febd-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4febd-110">PARAMETERS</span></span>

### <span data-ttu-id="4febd-111">-Konto</span><span class="sxs-lookup"><span data-stu-id="4febd-111">-Account</span></span>
<span data-ttu-id="4febd-112">Anger namnet på data Lake Store-kontot.</span><span class="sxs-lookup"><span data-stu-id="4febd-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="4febd-113">-Rengör</span><span class="sxs-lookup"><span data-stu-id="4febd-113">-Clean</span></span>
<span data-ttu-id="4febd-114">Anger att användaren vill ta bort allt innehåll i mappen, men inte själva mappen</span><span class="sxs-lookup"><span data-stu-id="4febd-114">Indicates the user wants to remove all of the contents of the folder, but not the folder itself</span></span>

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

### <span data-ttu-id="4febd-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4febd-115">-DefaultProfile</span></span>
<span data-ttu-id="4febd-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="4febd-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4febd-117">-Force</span><span class="sxs-lookup"><span data-stu-id="4febd-117">-Force</span></span>
<span data-ttu-id="4febd-118">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="4febd-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="4febd-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4febd-119">-PassThru</span></span>
<span data-ttu-id="4febd-120">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="4febd-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="4febd-121">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="4febd-121">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4febd-122">-Banor</span><span class="sxs-lookup"><span data-stu-id="4febd-122">-Paths</span></span>
<span data-ttu-id="4febd-123">Anger en matris med data Lake Store-sökvägar för de filer som ska tas bort, från och med rot katalogen (/).</span><span class="sxs-lookup"><span data-stu-id="4febd-123">Specifies an array of Data Lake Store paths of the files to remove, starting with the root directory (/).</span></span>

```yaml
Type: DataLakeStorePathInstance[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4febd-124">-Recurse</span><span class="sxs-lookup"><span data-stu-id="4febd-124">-Recurse</span></span>
<span data-ttu-id="4febd-125">Indikerar att den här åtgärden tar bort alla objekt i målmappen, inklusive undermappar.</span><span class="sxs-lookup"><span data-stu-id="4febd-125">Indicates that this operation deletes all items in the target folder, including subfolders.</span></span>
<span data-ttu-id="4febd-126">Om du inte anger parametern *rengör* tas även målmappen bort.</span><span class="sxs-lookup"><span data-stu-id="4febd-126">Unless you specify the *Clean* parameter, the target folder is also deleted.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4febd-127">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="4febd-127">-Confirm</span></span>
<span data-ttu-id="4febd-128">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="4febd-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4febd-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4febd-129">-WhatIf</span></span>
<span data-ttu-id="4febd-130">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="4febd-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4febd-131">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="4febd-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4febd-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4febd-132">CommonParameters</span></span>
<span data-ttu-id="4febd-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4febd-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4febd-134">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4febd-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4febd-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4febd-135">INPUTS</span></span>

### <span data-ttu-id="4febd-136">Ingen</span><span class="sxs-lookup"><span data-stu-id="4febd-136">None</span></span>
<span data-ttu-id="4febd-137">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="4febd-137">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="4febd-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4febd-138">OUTPUTS</span></span>

### <span data-ttu-id="4febd-139">bool</span><span class="sxs-lookup"><span data-stu-id="4febd-139">bool</span></span>
<span data-ttu-id="4febd-140">Om PassThru anges returnerar resultatet av åtgärden.</span><span class="sxs-lookup"><span data-stu-id="4febd-140">If PassThru is specified, returns the result of the operation.</span></span>

## <span data-ttu-id="4febd-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4febd-141">NOTES</span></span>

## <span data-ttu-id="4febd-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4febd-142">RELATED LINKS</span></span>

[<span data-ttu-id="4febd-143">Get-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="4febd-143">Get-AzureRmDataLakeStoreItem</span></span>](./Get-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="4febd-144">Exportera-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="4febd-144">Export-AzureRmDataLakeStoreItem</span></span>](./Export-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="4febd-145">Import-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="4febd-145">Import-AzureRmDataLakeStoreItem</span></span>](./Import-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="4febd-146">Anslut-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="4febd-146">Join-AzureRmDataLakeStoreItem</span></span>](./Join-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="4febd-147">New-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="4febd-147">New-AzureRmDataLakeStoreItem</span></span>](./New-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="4febd-148">Test-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="4febd-148">Test-AzureRmDataLakeStoreItem</span></span>](./Test-AzureRmDataLakeStoreItem.md)


