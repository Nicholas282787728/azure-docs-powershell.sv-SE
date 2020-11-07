---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 00CCA9B8-7C57-4FC0-9BD1-5FC16010E820
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/move-azurermdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Move-AzureRmDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Move-AzureRmDataLakeStoreItem.md
ms.openlocfilehash: 5e6fb437833db3f4278335f67693d084c2d6d95b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93755880"
---
# <span data-ttu-id="f73e2-101">Move-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="f73e2-101">Move-AzureRmDataLakeStoreItem</span></span>

## <span data-ttu-id="f73e2-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f73e2-102">SYNOPSIS</span></span>
<span data-ttu-id="f73e2-103">Flyttar eller byter namn på en fil eller mapp i data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="f73e2-103">Moves or renames a file or folder in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f73e2-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f73e2-104">SYNTAX</span></span>

```
Move-AzureRmDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-Destination] <DataLakeStorePathInstance> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f73e2-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f73e2-105">DESCRIPTION</span></span>
<span data-ttu-id="f73e2-106">Cmdleten **Move-AzureRmDataLakeStoreItem** flyttar eller byter namn på en fil eller mapp i data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="f73e2-106">The **Move-AzureRmDataLakeStoreItem** cmdlet moves or renames a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="f73e2-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f73e2-107">EXAMPLES</span></span>

### <span data-ttu-id="f73e2-108">Exempel 1: flytta och byta namn på ett objekt</span><span class="sxs-lookup"><span data-stu-id="f73e2-108">Example 1: Move and rename an item</span></span>
```
PS C:\>Move-AzureRmDataLakeStoreItem -AccountName "ContosoADL" -Path "/Original/Path/File.txt" -Destination "/New/Path/RenamedFile.txt"
```

<span data-ttu-id="f73e2-109">Det här kommandot byter namn på objektet File.txt till RenamedFile.txt och flyttar det till en annan mapp.</span><span class="sxs-lookup"><span data-stu-id="f73e2-109">This command renames the item File.txt to RenamedFile.txt and moves it to a different folder.</span></span>

## <span data-ttu-id="f73e2-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f73e2-110">PARAMETERS</span></span>

### <span data-ttu-id="f73e2-111">-Konto</span><span class="sxs-lookup"><span data-stu-id="f73e2-111">-Account</span></span>
<span data-ttu-id="f73e2-112">Anger namnet på data Lake Store-kontot.</span><span class="sxs-lookup"><span data-stu-id="f73e2-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="f73e2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f73e2-113">-DefaultProfile</span></span>
<span data-ttu-id="f73e2-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f73e2-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f73e2-115">-Mål</span><span class="sxs-lookup"><span data-stu-id="f73e2-115">-Destination</span></span>
<span data-ttu-id="f73e2-116">Anger sökvägen till data Lake Store dit objektet ska flyttas, med början med rot katalogen (/).</span><span class="sxs-lookup"><span data-stu-id="f73e2-116">Specifies the Data Lake Store path to which to move the item, starting with the root directory (/).</span></span>

```yaml
Type: DataLakeStorePathInstance
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f73e2-117">-Force</span><span class="sxs-lookup"><span data-stu-id="f73e2-117">-Force</span></span>
<span data-ttu-id="f73e2-118">Anger att den här åtgärden kan skriva över målfilen om den redan finns.</span><span class="sxs-lookup"><span data-stu-id="f73e2-118">Indicates that this operation can overwrite the destination file if it already exists.</span></span>

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

### <span data-ttu-id="f73e2-119">-Path</span><span class="sxs-lookup"><span data-stu-id="f73e2-119">-Path</span></span>
<span data-ttu-id="f73e2-120">Anger data Lake Store-sökvägen för det objekt som ska flyttas eller byta namn, från rot katalogen (/).</span><span class="sxs-lookup"><span data-stu-id="f73e2-120">Specifies the Data Lake Store path of the item to move or rename, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="f73e2-121">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="f73e2-121">-Confirm</span></span>
<span data-ttu-id="f73e2-122">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="f73e2-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f73e2-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f73e2-123">-WhatIf</span></span>
<span data-ttu-id="f73e2-124">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="f73e2-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f73e2-125">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="f73e2-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f73e2-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f73e2-126">CommonParameters</span></span>
<span data-ttu-id="f73e2-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f73e2-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f73e2-128">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f73e2-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f73e2-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f73e2-129">INPUTS</span></span>

### <span data-ttu-id="f73e2-130">Ingen</span><span class="sxs-lookup"><span data-stu-id="f73e2-130">None</span></span>
<span data-ttu-id="f73e2-131">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="f73e2-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f73e2-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f73e2-132">OUTPUTS</span></span>

### <span data-ttu-id="f73e2-133">strängvärdet</span><span class="sxs-lookup"><span data-stu-id="f73e2-133">string</span></span>
<span data-ttu-id="f73e2-134">Den fullständiga sökvägen till den flyttade filen eller mappen.</span><span class="sxs-lookup"><span data-stu-id="f73e2-134">The full path to the moved file or folder.</span></span>

## <span data-ttu-id="f73e2-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f73e2-135">NOTES</span></span>

## <span data-ttu-id="f73e2-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f73e2-136">RELATED LINKS</span></span>

[<span data-ttu-id="f73e2-137">Get-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="f73e2-137">Get-AzureRmDataLakeStoreItem</span></span>](./Get-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="f73e2-138">Exportera-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="f73e2-138">Export-AzureRmDataLakeStoreItem</span></span>](./Export-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="f73e2-139">Import-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="f73e2-139">Import-AzureRmDataLakeStoreItem</span></span>](./Import-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="f73e2-140">New-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="f73e2-140">New-AzureRmDataLakeStoreItem</span></span>](./New-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="f73e2-141">Remove-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="f73e2-141">Remove-AzureRmDataLakeStoreItem</span></span>](./Remove-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="f73e2-142">Test-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="f73e2-142">Test-AzureRmDataLakeStoreItem</span></span>](./Test-AzureRmDataLakeStoreItem.md)


