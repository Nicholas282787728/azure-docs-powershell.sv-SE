---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 164DC871-0F0C-4E71-A37A-2B85CE65C2C4
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Remove-AzureRmDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Remove-AzureRmDataLakeStoreItem.md
ms.openlocfilehash: da26deb246fc90a1b83b63c47560dd5912616d62
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93583324"
---
# <span data-ttu-id="5dcac-101">Remove-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="5dcac-101">Remove-AzureRmDataLakeStoreItem</span></span>

## <span data-ttu-id="5dcac-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5dcac-102">SYNOPSIS</span></span>
<span data-ttu-id="5dcac-103">Tar bort en fil eller mapp i data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="5dcac-103">Deletes a file or folder in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5dcac-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5dcac-104">SYNTAX</span></span>

```
Remove-AzureRmDataLakeStoreItem [-Account] <String> [-Paths] <DataLakeStorePathInstance[]> [-Recurse] [-Clean]
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5dcac-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5dcac-105">DESCRIPTION</span></span>
<span data-ttu-id="5dcac-106">Cmdleten **Remove-AzureRmDataLakeStoreItem** tar bort en fil eller mapp i data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="5dcac-106">The **Remove-AzureRmDataLakeStoreItem** cmdlet deletes a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="5dcac-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5dcac-107">EXAMPLES</span></span>

### <span data-ttu-id="5dcac-108">Exempel 1: ta bort flera objekt</span><span class="sxs-lookup"><span data-stu-id="5dcac-108">Example 1: Remove multiple items</span></span>
```
PS C:\>Remove-AzureRmDataLakeStoreItem -AccountName "ContosoADL" -Paths "/File01.txt","/MyFiles/File.csv"
```

<span data-ttu-id="5dcac-109">Det här kommandot tar bort filerna File01.txt och File.csv från data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="5dcac-109">This command removes the files File01.txt and File.csv from the Data Lake Store.</span></span>

## <span data-ttu-id="5dcac-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5dcac-110">PARAMETERS</span></span>

### <span data-ttu-id="5dcac-111">-Konto</span><span class="sxs-lookup"><span data-stu-id="5dcac-111">-Account</span></span>
<span data-ttu-id="5dcac-112">Anger namnet på data Lake Store-kontot.</span><span class="sxs-lookup"><span data-stu-id="5dcac-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="5dcac-113">-Rengör</span><span class="sxs-lookup"><span data-stu-id="5dcac-113">-Clean</span></span>
<span data-ttu-id="5dcac-114">Indikerar att den här åtgärden tar bort allt innehåll i målmappen och behåller mappen.</span><span class="sxs-lookup"><span data-stu-id="5dcac-114">Indicates that this operation removes all of the contents of the target folder and retains the folder.</span></span>
<span data-ttu-id="5dcac-115">Använd den här parametern med parametern *recurse* .</span><span class="sxs-lookup"><span data-stu-id="5dcac-115">Use this parameter with the *Recurse* parameter.</span></span>

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

### <span data-ttu-id="5dcac-116">-Force</span><span class="sxs-lookup"><span data-stu-id="5dcac-116">-Force</span></span>
<span data-ttu-id="5dcac-117">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="5dcac-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="5dcac-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5dcac-118">-PassThru</span></span>
<span data-ttu-id="5dcac-119">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="5dcac-119">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="5dcac-120">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="5dcac-120">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="5dcac-121">-Banor</span><span class="sxs-lookup"><span data-stu-id="5dcac-121">-Paths</span></span>
<span data-ttu-id="5dcac-122">Anger en matris med data Lake Store-sökvägar för de filer som ska tas bort, från och med rot katalogen (/).</span><span class="sxs-lookup"><span data-stu-id="5dcac-122">Specifies an array of Data Lake Store paths of the files to remove, starting with the root directory (/).</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5dcac-123">-Recurse</span><span class="sxs-lookup"><span data-stu-id="5dcac-123">-Recurse</span></span>
<span data-ttu-id="5dcac-124">Indikerar att den här åtgärden tar bort alla objekt i målmappen, inklusive undermappar.</span><span class="sxs-lookup"><span data-stu-id="5dcac-124">Indicates that this operation deletes all items in the target folder, including subfolders.</span></span>
<span data-ttu-id="5dcac-125">Om du inte anger parametern *rengör* tas även målmappen bort.</span><span class="sxs-lookup"><span data-stu-id="5dcac-125">Unless you specify the *Clean* parameter, the target folder is also deleted.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5dcac-126">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="5dcac-126">-Confirm</span></span>
<span data-ttu-id="5dcac-127">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="5dcac-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5dcac-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5dcac-128">-WhatIf</span></span>
<span data-ttu-id="5dcac-129">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="5dcac-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5dcac-130">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="5dcac-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5dcac-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5dcac-131">-DefaultProfile</span></span>
<span data-ttu-id="5dcac-132">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="5dcac-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5dcac-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5dcac-133">CommonParameters</span></span>
<span data-ttu-id="5dcac-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5dcac-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5dcac-135">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5dcac-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5dcac-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5dcac-136">INPUTS</span></span>

## <span data-ttu-id="5dcac-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5dcac-137">OUTPUTS</span></span>

### <span data-ttu-id="5dcac-138">bool</span><span class="sxs-lookup"><span data-stu-id="5dcac-138">bool</span></span>
<span data-ttu-id="5dcac-139">Om PassThru anges returnerar resultatet av åtgärden.</span><span class="sxs-lookup"><span data-stu-id="5dcac-139">If PassThru is specified, returns the result of the operation.</span></span>

## <span data-ttu-id="5dcac-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5dcac-140">NOTES</span></span>

## <span data-ttu-id="5dcac-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5dcac-141">RELATED LINKS</span></span>

[<span data-ttu-id="5dcac-142">Get-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="5dcac-142">Get-AzureRmDataLakeStoreItem</span></span>](./Get-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="5dcac-143">Exportera-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="5dcac-143">Export-AzureRmDataLakeStoreItem</span></span>](./Export-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="5dcac-144">Import-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="5dcac-144">Import-AzureRmDataLakeStoreItem</span></span>](./Import-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="5dcac-145">Anslut-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="5dcac-145">Join-AzureRmDataLakeStoreItem</span></span>](./Join-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="5dcac-146">New-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="5dcac-146">New-AzureRmDataLakeStoreItem</span></span>](./New-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="5dcac-147">Test-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="5dcac-147">Test-AzureRmDataLakeStoreItem</span></span>](./Test-AzureRmDataLakeStoreItem.md)


