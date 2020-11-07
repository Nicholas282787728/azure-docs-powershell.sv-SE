---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 00CCA9B8-7C57-4FC0-9BD1-5FC16010E820
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Move-AzureRmDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Move-AzureRmDataLakeStoreItem.md
ms.openlocfilehash: 5d975e70423e03e3ab17bbfc8631ff8e1f892cc0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756974"
---
# <span data-ttu-id="ba17a-101">Move-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="ba17a-101">Move-AzureRmDataLakeStoreItem</span></span>

## <span data-ttu-id="ba17a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ba17a-102">SYNOPSIS</span></span>
<span data-ttu-id="ba17a-103">Flyttar eller byter namn på en fil eller mapp i data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="ba17a-103">Moves or renames a file or folder in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ba17a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ba17a-104">SYNTAX</span></span>

```
Move-AzureRmDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-Destination] <DataLakeStorePathInstance> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ba17a-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ba17a-105">DESCRIPTION</span></span>
<span data-ttu-id="ba17a-106">Cmdleten **Move-AzureRmDataLakeStoreItem** flyttar eller byter namn på en fil eller mapp i data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="ba17a-106">The **Move-AzureRmDataLakeStoreItem** cmdlet moves or renames a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="ba17a-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ba17a-107">EXAMPLES</span></span>

### <span data-ttu-id="ba17a-108">Exempel 1: flytta och byta namn på ett objekt</span><span class="sxs-lookup"><span data-stu-id="ba17a-108">Example 1: Move and rename an item</span></span>
```
PS C:\>Move-AzureRmDataLakeStoreItem -AccountName "ContosoADL" -Path "/Original/Path/File.txt" -Destination "/New/Path/RenamedFile.txt"
```

<span data-ttu-id="ba17a-109">Det här kommandot byter namn på objektet File.txt till RenamedFile.txt och flyttar det till en annan mapp.</span><span class="sxs-lookup"><span data-stu-id="ba17a-109">This command renames the item File.txt to RenamedFile.txt and moves it to a different folder.</span></span>

## <span data-ttu-id="ba17a-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ba17a-110">PARAMETERS</span></span>

### <span data-ttu-id="ba17a-111">-Konto</span><span class="sxs-lookup"><span data-stu-id="ba17a-111">-Account</span></span>
<span data-ttu-id="ba17a-112">Anger namnet på data Lake Store-kontot.</span><span class="sxs-lookup"><span data-stu-id="ba17a-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="ba17a-113">-Mål</span><span class="sxs-lookup"><span data-stu-id="ba17a-113">-Destination</span></span>
<span data-ttu-id="ba17a-114">Anger sökvägen till data Lake Store dit objektet ska flyttas, med början med rot katalogen (/).</span><span class="sxs-lookup"><span data-stu-id="ba17a-114">Specifies the Data Lake Store path to which to move the item, starting with the root directory (/).</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ba17a-115">-Force</span><span class="sxs-lookup"><span data-stu-id="ba17a-115">-Force</span></span>
<span data-ttu-id="ba17a-116">Anger att den här åtgärden kan skriva över målfilen om den redan finns.</span><span class="sxs-lookup"><span data-stu-id="ba17a-116">Indicates that this operation can overwrite the destination file if it already exists.</span></span>

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

### <span data-ttu-id="ba17a-117">-Path</span><span class="sxs-lookup"><span data-stu-id="ba17a-117">-Path</span></span>
<span data-ttu-id="ba17a-118">Anger data Lake Store-sökvägen för det objekt som ska flyttas eller byta namn, från rot katalogen (/).</span><span class="sxs-lookup"><span data-stu-id="ba17a-118">Specifies the Data Lake Store path of the item to move or rename, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="ba17a-119">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="ba17a-119">-Confirm</span></span>
<span data-ttu-id="ba17a-120">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="ba17a-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ba17a-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ba17a-121">-WhatIf</span></span>
<span data-ttu-id="ba17a-122">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="ba17a-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ba17a-123">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="ba17a-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ba17a-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba17a-124">-DefaultProfile</span></span>
<span data-ttu-id="ba17a-125">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ba17a-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ba17a-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba17a-126">CommonParameters</span></span>
<span data-ttu-id="ba17a-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ba17a-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba17a-128">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ba17a-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba17a-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ba17a-129">INPUTS</span></span>

## <span data-ttu-id="ba17a-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ba17a-130">OUTPUTS</span></span>

### <span data-ttu-id="ba17a-131">strängvärdet</span><span class="sxs-lookup"><span data-stu-id="ba17a-131">string</span></span>
<span data-ttu-id="ba17a-132">Den fullständiga sökvägen till den flyttade filen eller mappen.</span><span class="sxs-lookup"><span data-stu-id="ba17a-132">The full path to the moved file or folder.</span></span>

## <span data-ttu-id="ba17a-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ba17a-133">NOTES</span></span>

## <span data-ttu-id="ba17a-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ba17a-134">RELATED LINKS</span></span>

[<span data-ttu-id="ba17a-135">Get-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="ba17a-135">Get-AzureRmDataLakeStoreItem</span></span>](./Get-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="ba17a-136">Exportera-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="ba17a-136">Export-AzureRmDataLakeStoreItem</span></span>](./Export-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="ba17a-137">Import-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="ba17a-137">Import-AzureRmDataLakeStoreItem</span></span>](./Import-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="ba17a-138">New-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="ba17a-138">New-AzureRmDataLakeStoreItem</span></span>](./New-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="ba17a-139">Remove-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="ba17a-139">Remove-AzureRmDataLakeStoreItem</span></span>](./Remove-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="ba17a-140">Test-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="ba17a-140">Test-AzureRmDataLakeStoreItem</span></span>](./Test-AzureRmDataLakeStoreItem.md)


