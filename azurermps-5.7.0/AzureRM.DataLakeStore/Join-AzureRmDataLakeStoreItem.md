---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 4E9EA2E9-4BE2-4530-BC2B-D369C016CD8C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/join-azurermdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Join-AzureRmDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Join-AzureRmDataLakeStoreItem.md
ms.openlocfilehash: c321c605977e09f119d19e5c4ced44261c3de0cd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93575667"
---
# <span data-ttu-id="3b3ff-101">Join-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="3b3ff-101">Join-AzureRmDataLakeStoreItem</span></span>

## <span data-ttu-id="3b3ff-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3b3ff-102">SYNOPSIS</span></span>
<span data-ttu-id="3b3ff-103">Ansluter en eller flera filer för att skapa en fil i data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="3b3ff-103">Joins one or more files to create one file in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3b3ff-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3b3ff-104">SYNTAX</span></span>

```
Join-AzureRmDataLakeStoreItem [-Account] <String> [-Paths] <DataLakeStorePathInstance[]>
 [-Destination] <DataLakeStorePathInstance> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3b3ff-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3b3ff-105">DESCRIPTION</span></span>
<span data-ttu-id="3b3ff-106">Cmdleten **Join-AzureRmDataLakeStoreItem** ansluter till en eller flera filer för att skapa en fil i data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="3b3ff-106">The **Join-AzureRmDataLakeStoreItem** cmdlet joins one or more files to create one file in Data Lake Store.</span></span>

## <span data-ttu-id="3b3ff-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3b3ff-107">EXAMPLES</span></span>

### <span data-ttu-id="3b3ff-108">Exempel 1: koppla ihop två objekt</span><span class="sxs-lookup"><span data-stu-id="3b3ff-108">Example 1: Join two items</span></span>
```
PS C:\>Join-AzureRmDataLakeStoreItem -AccountName "ContosoADL" -Paths "/MyFiles/File01.txt","/MyFiles/File02.txt" -Destination "/MyFiles/CombinedFile.txt"
```

<span data-ttu-id="3b3ff-109">Det här kommandot ansluter File01.txt och File02.txt för att skapa filen CombinedFile.txt.</span><span class="sxs-lookup"><span data-stu-id="3b3ff-109">This command joins File01.txt and File02.txt to create the file CombinedFile.txt.</span></span>

## <span data-ttu-id="3b3ff-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3b3ff-110">PARAMETERS</span></span>

### <span data-ttu-id="3b3ff-111">-Konto</span><span class="sxs-lookup"><span data-stu-id="3b3ff-111">-Account</span></span>
<span data-ttu-id="3b3ff-112">Anger namnet på data Lake Store-kontot.</span><span class="sxs-lookup"><span data-stu-id="3b3ff-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="3b3ff-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b3ff-113">-DefaultProfile</span></span>
<span data-ttu-id="3b3ff-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="3b3ff-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3b3ff-115">-Mål</span><span class="sxs-lookup"><span data-stu-id="3b3ff-115">-Destination</span></span>
<span data-ttu-id="3b3ff-116">Anger sökvägen till data Lake Store för det kopplade objektet, från rot katalogen (/).</span><span class="sxs-lookup"><span data-stu-id="3b3ff-116">Specifies the Data Lake Store path for the joined item, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="3b3ff-117">-Force</span><span class="sxs-lookup"><span data-stu-id="3b3ff-117">-Force</span></span>
<span data-ttu-id="3b3ff-118">Anger att den här åtgärden kan skriva över målfilen om den redan finns.</span><span class="sxs-lookup"><span data-stu-id="3b3ff-118">Indicates that this operation can overwrite the destination file if it already exists.</span></span>

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

### <span data-ttu-id="3b3ff-119">-Banor</span><span class="sxs-lookup"><span data-stu-id="3b3ff-119">-Paths</span></span>
<span data-ttu-id="3b3ff-120">Anger en matris med data Lake Store-sökvägar för de filer som ska kombineras, från och med rot katalogen (/).</span><span class="sxs-lookup"><span data-stu-id="3b3ff-120">Specifies an array of Data Lake Store paths of the files to combine, starting with the root directory (/).</span></span>

```yaml
Type: DataLakeStorePathInstance[]
Parameter Sets: (All)
Aliases: Path

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b3ff-121">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="3b3ff-121">-Confirm</span></span>
<span data-ttu-id="3b3ff-122">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="3b3ff-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3b3ff-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3b3ff-123">-WhatIf</span></span>
<span data-ttu-id="3b3ff-124">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="3b3ff-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3b3ff-125">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="3b3ff-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3b3ff-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b3ff-126">CommonParameters</span></span>
<span data-ttu-id="3b3ff-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3b3ff-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b3ff-128">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3b3ff-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b3ff-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3b3ff-129">INPUTS</span></span>

### <span data-ttu-id="3b3ff-130">Ingen</span><span class="sxs-lookup"><span data-stu-id="3b3ff-130">None</span></span>
<span data-ttu-id="3b3ff-131">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="3b3ff-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="3b3ff-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3b3ff-132">OUTPUTS</span></span>

### <span data-ttu-id="3b3ff-133">strängvärdet</span><span class="sxs-lookup"><span data-stu-id="3b3ff-133">string</span></span>
<span data-ttu-id="3b3ff-134">Den fullständiga sökvägen till den resulterande filen från kopplade filer.</span><span class="sxs-lookup"><span data-stu-id="3b3ff-134">The full path to the resulting file from the joined files.</span></span>

## <span data-ttu-id="3b3ff-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3b3ff-135">NOTES</span></span>

## <span data-ttu-id="3b3ff-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3b3ff-136">RELATED LINKS</span></span>

[<span data-ttu-id="3b3ff-137">Get-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="3b3ff-137">Get-AzureRmDataLakeStoreItem</span></span>](./Get-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="3b3ff-138">Exportera-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="3b3ff-138">Export-AzureRmDataLakeStoreItem</span></span>](./Export-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="3b3ff-139">Import-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="3b3ff-139">Import-AzureRmDataLakeStoreItem</span></span>](./Import-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="3b3ff-140">New-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="3b3ff-140">New-AzureRmDataLakeStoreItem</span></span>](./New-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="3b3ff-141">Remove-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="3b3ff-141">Remove-AzureRmDataLakeStoreItem</span></span>](./Remove-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="3b3ff-142">Test-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="3b3ff-142">Test-AzureRmDataLakeStoreItem</span></span>](./Test-AzureRmDataLakeStoreItem.md)


